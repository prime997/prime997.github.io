---
layout: post
category: code
tags: jekyll rouge pygments css
---

Syntax highlighting makes code snippets easier to read. 
For example, string literals are displayed in a different color,

```javascript
const string = "A string primitive";
```
 
or blocks of comments are a lighter color 

```html
<!-- This is a comment. Comments are not displayed in the browser -->

<p>This is a paragraph.</p> 
```

making it easier to focus on uncommented code.

At the time of writing, 
[GitHub Pages](https://pages.github.com) supports Jekyll [Version 3.8.7](https://pages.github.com/versions/).
Jekyll 3 supports the [Rouge](https://github.com/rouge-ruby/rouge) syntax highlighter, 
which is compatible with [Pygments](https://pygments.org/).[^1] 
Consequently, Jekyll static websites hosted on GitHub Pages will highlight syntax in code blocks by default.

When GitHub builds your website, 
if your theme doesn't have a CSS file for syntax highlighting, 
GitHub generates a default syntax highlighting CSS file. 

This default CSS isn't generated when building the website locally. 
Syntax highlighting won't appear on [a local build of a Jekyll website]({% post_url 2020-06-10-jekyll-local-builds %}) unless a `.highlight` CSS class is defined.

From the [Git Command Line](https://git-scm.com/book/en/v2/Getting-Started-The-Command-Line), 
run

```
$ rougify style github > style.css
```

and add the file the command generates to your project's CSS file. 
Alternatively, download a [Pygment CSS theme](https://jwarby.github.io/jekyll-pygments-themes/languages/ruby.html) and add it to your CSS with the import command

```css
@import "default.css";
```

This website uses the `default.css` theme from the Pygments open-source project.

---

[^1]: [Pygments](https://pygments.org/) is an open-source syntax highlighting project. Pygments supports over 500 languages. The list of supported languages is listed [here](https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers).

*[CSS]: Cascading Style Sheet

