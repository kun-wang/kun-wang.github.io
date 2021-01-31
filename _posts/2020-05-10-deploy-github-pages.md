---
layout: post
date: 2020-05-10
title: Setup up Github Pages with Jekyll
tags: jekyll,github pages
---

References: [Building the Site with TeXt and Jekyll Scholar](http://zhepeiw.com/2018/12/23/blog1.html)

## Features

### News Center

### Bibliography

Unfortunately, **Yuan Yong**'s template does not come with automatic bibliography support. To enable such support, we incorporate [Jekyll Scholar](https://github.com/inukshuk/jekyll-scholar) into the site. It is a Jekyll extension that converts bibtex to bibliography formatted according to the settings.



## Deployment

An annoying fact is that Github Pages does not support Jekyll Scholar under the default workflow, but it is possible to host the site on Github Pages as introduced in [this example](http://davidensinger.com/2013/07/automating-jekyll-deployment-to-github-pages-with-rake/). By default, Github Pages is built from the `master` branch. The trick is that we push the source files to a separate branch (say `source`) to remote and keep only the generated content of the `_site/` directories to the `master` branch. How can we do this?

#### Setup the source branch

We assume now there is only a master branch there. On the first time to setup the deployment, we should first create a [Rakefile](https://github.com/zhepeiw/zhepeiw.github.io/blob/source/Rakefile) at the root of the repository. Then, we create and switch to a separate branch, (i.e., `source`) with

```git
git checkout -b source
```

Now we are on the source branch. Do remember to run the command

```git
bundle exec jekyll serve
```

so that the directory `_site/` is in its latest version.

#### Automatic Deployment

We run

```git
rake commit
```

to commit the changes to the source branch locally and

```git
rake deploy
```

to push the `_site` directory to remote `master` and the source to remote `source`. We can also combine the two steps into one by running

```git
rake commit_deploy
```

#### Remarks

It is possible that after the `rake deploy` command, there will be the following warning

```javascript
Pushing to git@github.com:xxx.git
To git@github.com:xxx.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'git@github.com:xxx.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Merge the remote changes (e.g. 'git pull')
hint: before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

This is possibly because you change something online, resulting conflict. If you do not wish to merge the remote branch into your local branch, and want to do a force push, use the push command with `-f`

```git
git push -f origin <branch>
```

where `branch` is the remote branch I want to merge.