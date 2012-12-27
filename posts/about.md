---
title: About
---

This page shows you all the instructions on how to contribute to Vistat. Before you get started, you need to fork the [supstat/vistat](https://github.com/supstat/vistat) repository to your own Github account (click the `Fork` button). You are assumed to have basic knowledge of GIT and R.

## New Article

To start a new article, run

```bash
rake post title="A Title"
```

and you will get an [R Markdown](http://www.rstudio.com/ide/docs/authoring/using_markdown) (Rmd) file under `_source/` named `yyyy-mm-dd-a-title.Rmd`, which is a plain text file and you can edit it with your favorite text editor. At the moment, RStudio has the best support to Rmd files. Here is an [Rmd sample file](https://github.com/yihui/knitr-examples/blob/master/001-minimal.Rmd) and its [output](https://github.com/yihui/knitr-examples/blob/master/001-minimal.md).

If you do not have or understand `rake`, just copy an existing Rmd file, rename it and open with a text editor.

## Edit an Article

There are a few fields in the header such as `author` and `tags`; if you have multiple entries, use the comma to separate them, e.g. `author: [taiyun, yihui]`. Note all authors need to put their information in [`_config.yml`](https://github.com/supstat/vistat/blob/gh-pages/_config.yml), and input the author id's to the `author` field (the same applies to reviewers).

You can write math in the LaTeX syntax, e.g. `$\alpha+\beta$` renders inline like $\alpha+\beta$, and `$$f(x)=\frac{1}{\sqrt{2\pi}}e^{-x^2/2}$$` renders the display style

$$f(x)=\frac{1}{\sqrt{2\pi}}e^{-x^2/2}$$

If you want to generate animations, set `animation: true` in the preamble of the article and use the chunk option `fig.show='animate'` in the chunk header. Similarly, `d3: true` will load D3 in the page.

## Compilation

The executable script `_bin/knit` is essentially an R script. For Linux/Mac users, you can compile an Rmd file to md by

```bash
./_bin/knit _source/yyyy-mm-dd-your-post.Rmd
```

For Windows users, use `Rscript` instead:

```bash
Rscript ./_bin/knit _source/yyyy-mm-dd-your-post.Rmd
```

You can certainly compile the article inside your editor like RStudio, and the above approach is only necessary if you need animations to work.

## Preview

If you want to preview your article in the website, you can run

```bash
rake preview
```

which is basically a wapper to `jekyll --server --auto`. Of course you need to install Jekyll first.

## Submission

After you are done with an article, commit it to your forked repository and submit a pull request to us. We will get it reviewed and you will see comments online. Further revisions may be required, in which case you just make the revision and continue commit in the changes, and they will appear in the previous pull request.

Please commit the source file only (`*.Rmd`) and do not commit the output files (`*.md` and figures). We will re-compile the source files and upload images after we accept the article. Therefore if your article involves with special packages or data, you should add clear instructions on them in the article.

## Reviewers

Everyone is welcome to become a reviewer for Vistat. Reviews are public on Github.
