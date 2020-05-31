# Personal Website Notes

## Basic File Structure and Building the site
Short guide to building a simple static website using Jekyll
 - Starting from the [tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/), build a Gemfile using the `init bundle` in the ruby command line (CL) your working directory. 
 - Change the contents of the Gemfile using a text editor of your choice. On creation, the 7th line of the Gemfile is `gem = "rails"`. Change this to `gem = "jekyll"`. The reference to a repository can be deleted. (Note, the name of the gem is case-sensitive)
 - Create a simple index.html page in your working directory
 - Run `bundle install` in the ruby CL if not already done
 - The `jekyll build` command builds the site and outputs a static site to a directory called `_site`.
 - The `jekyll serve` command does the same thing except it rebuilds any time you make a change and runs a local web server at `http://localhost:4000`.

## Using Liquid
[Liquid](https://shopify.github.io/liquid/) creates a bridge between a HTML file and a data store. It does this by allowing us to access variables from within a template, or Liquid file, with a simple to use and readable syntax.

Liquid has 3 main parts: objects, tags, and filters.

### Objects
