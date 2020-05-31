# Personal Website Notes

## Basic File Structure and Building the site
Short guide to building a simple static website using Jekyll
 - Starting from the [tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/), build a Gemfile using the `init bundle` in the ruby command line (CL) your working directory. 
 - Change the contents of the Gemfile using a text editor of your choice. On creation, the 7th line of the Gemfile is `gem = "rails"`. Change this to `gem = "jekyll"`. The reference to a repository can be deleted. (Note, the name of the gem is case-sensitive)
 - Create a simple index.html page in your working directory
 - Run `bundle install` in the ruby CL if not already done
 - The `jekyll build` command builds the site and outputs a static site to a directory called `_site`.
 - The `jekyll serve` command does the same thing except it rebuilds any time you make a change and runs a local web server at `http://localhost:4000`.

If using SVN tortoise, there's no need for a `.gitignore` file. The list of ignored files can be accessed in the `TortoiseSVN > Properties` menu.

## Using Liquid
[Liquid](https://shopify.github.io/liquid/) creates a bridge between a HTML file and a data store. It does this by allowing us to access variables from within a template, or Liquid file, with a simple to use and readable syntax.

Liquid has 3 main parts: objects, tags, and filters.

### Objects
Objects tell Liquid where to output content. They’re denoted by double curly braces: `{{` and `}}`. For example:

```
{{ page.title }}
```

Outputs a variable called `page.title` on the page.

### Tags

Tags create the logic and control flow for templates. They are denoted by curly braces and percent signs: `{%` and `%}`. For example:

```
{% if page.show_sidebar %}
  <div class="sidebar">
    sidebar content
  </div>
{% endif %}
```

Outputs the sidebar if `page.show_sidebar` is true. You can learn more about the tags available to Jekyll here.

### Filters

Filters change the output of a Liquid object. They are used within an output and are separated by a `|`. For example:

```
{{ "hi" | capitalize }}
```

Outputs Hi. You can learn more about the filters available to Jekyll here.


## Adding Liquid to the Website
To get our changes processed by Jekyll we need to add front matter to the top of the page:

```
---
# front matter tells Jekyll to process Liquid
---
```

# Front Matter
Front matter is a snippet of [YAML](https://yaml.org/) which sits between two triple-dashed lines at the top of a file. Front matter is used to set variables for the page, for example:

```
---
my_number: 5
---
```

Front matter variables are available in Liquid under the page variable. For example to output the variable above you would use: 

```
{{ page.my_number }}
```

# Layouts and Markdown
Layouts are located in the `_layouts` folder. They wrap the content of a page in HTML. The Front Matter variable 'layout' tells Liquid which layout template to use.

Jeykyll supports Markdown for faster and easier writing. Create a default template for the index pages, and create an about Markdown page that uses the default template.

# Includes
We can include html using the `include` command wrapped in `{% * %}` brackets. Any file that needs to be included is stored in the `_includes` folder. Note, Liquid will read the brackets even if they're commented out in the HTML.