### Usage

Note that `_pages/about.md` is built to `index.html` in the published site. There is therefore no need to have a separate index page for the project. If an index page does exist in the root directory then this will prevent `_pages/about.md` from being added to the built site.

For details, see 



### How to use



Reference: https://scriptedtea.com/tech/how-to-deploy-jekyll-to-github/



Step 1: run the following command to build the whole website

> jekyll build

Step 2: run the following command to double check the effect (alternative)

> jekyll serve

Step 3. change to directory "_site" and update the "gh-pages" branch

> cd _site
>
> git add .
>
> git commit -m "Commit Message Here"
>
> git push origin gh-pages



## Features

---

#### Ergonomic Publications

Your publications page is generated automatically from your BibTex bibliography. Simply edit `_data/papers.bib`. You can also add new `*.bib` files and customize the look of your publications however you like by editing `_pages/publications.md`.

Keep meta-information about your co-authors in `_data/coauthors.yml` and Jekyll will insert links to their webpages automatically.

## Credits

This site is powered by [Jekyll](https://jekyllrb.com/) using a modified version of the [Yong Yuan](http://yongyuan.name/)'s beautiful theme.

Some icons are loaded using [Font Awesome](http://fontawesome.io/).

List of publications is generated using [Jekyll Scholar](https://github.com/inukshuk/jekyll-scholar), inspired by [Mohamad Ghassany](https://www.mghassany.com/publications/).

The deployment procedure follows from [zhepeiw](http://zhepeiw.com/2018/12/23/blog1.html) and [al-folio](https://github.com/alshedivat/al-folio).
