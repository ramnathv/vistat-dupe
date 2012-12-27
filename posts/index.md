---
title: About Vistat
---

Statistical graphics are powerful in terms of conveying information. When we see a good graph, we often wonder how it was made (e.g. the [one below](http://stackoverflow.com/q/12675147/559676) via xkcd).

![via xkcd](http://imgs.xkcd.com/comics/front_door.png)

Vistat aims to be a journal-like website, publishing code to reproduce useful or interesting graphs. It is based on Github/Jekyll, and graphs are generated dynamically through the R package [**knitr**](http://yihui.name/knitr), hence reproducibility is guaranteed.

## Latest 5 posts

<style>
ul.posts {
  margin-top: 15px;
}
ul.posts li {
  list-style: none
}
ul.posts hr {
  margin: 5px 5px;
}
ul.posts span {
  font-size: 12px;
  color: #999;
}
</style>

<ul class="posts">
{{# pages }}
 {{# date }}
 <li>
  <span class='pull-right'>{{date}}</span> 
  <a href="{{link}}">{{{ title }}}</a>
  <hr/>
 </li>
 {{/ date }}
{{/ pages }}
</ul>

## How to contribute

You can [fork the repository](https://github.com/supstat/vistat) on Github, add your article to the `_source` directory and submit a pull request to us. We will run your code and upload images. For more details, see [about](about.html).

## Copyright

All the content in this website is licensed under [CC BY-NC-SA 3.0](http://creativecommons.org/licenses/by-nc-sa/3.0/). This site is hosted on [GitHub](https://github.com) Pages using the [Dinky theme](https://github.com/sodabrew/theme-dinky) for [Jekyll Bootstrap](http://jekyllbootstrap.com).
