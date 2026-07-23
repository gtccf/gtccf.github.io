# gtccf.github.io
GTCCF website, generated with Jekyll.

This is basically a static HTML site with includes so that the header and
footer don't need to be updated on every page individually. Each page on the
site should have these lines at the top:
```
---
title: (Whatever page title you want)
layout: default
---
```
Everything following this is just HTML that will be substituted in place of the
`{{ content }}` marker in `_layouts/default.html`.
[Jekyll](http://jekyllrb.com) can do a lot more, but includes are pretty much
all we use as of August 2015.

## Setting up a dev environment
You will need a modern version of Ruby (e.g., Ruby 3.x) and Bundler to preview the site.

### Prerequisites (All Platforms)
We use Bundler to manage dependencies (Jekyll and other gems) cleanly.

### On Mac
* Install Homebrew from https://brew.sh/
* Install `rbenv` to manage Ruby versions, and install Ruby 3.3.4 (or use your preferred Ruby version manager):
  ```bash
  brew install rbenv
  rbenv install 3.3.4
  ```
* Set up your local Ruby version to match the project's `.ruby-version` file.
* Install Bundler:
  ```bash
  gem install bundler
  ```
* Install the project's dependencies:
  ```bash
  bundle install
  ```

### On Windows
* Download the installer from https://rubyinstaller.org/
* Run `gem install bundler`
* Run `bundle install`

### On Linux
* Install Ruby 3.x using your package manager or a manager like `rbenv` or `rvm`.
* Run `gem install bundler`
* Run `bundle install`

## Previewing the site
* Open up a terminal in the root folder of this repository.
* Run the development server with:
  ```bash
  bundle exec jekyll serve
  ```
* In your browser, navigate to http://localhost:4000/
* Edit the site source in your favorite text editor.
* The site should automatically update a few seconds after you save a file. You'll need to refresh the page to see changes.

## Publishing changes
Just commit your changes in Git and push to this repository. The live site
should update within a few minutes.

## Navigation
The navigation bar is programmatically generated from `_data/nav.yml`. This
allows setting the `active` class on the current page, which would otherwise be
impossible. If you want to change the links in the navigation, edit that file.
If you need to change the styling or layout (beyond just rearranging the order
of the links) you should look at `_includes/nav.html`.

## Creating redirects
Occasionally you may want to create a redirect or a short link. For example,
http://www.gtccf.org/lifegroups redirects to a Google form. The code for this
can be found
[here](https://github.com/gtccf/gtccf.github.io/blob/23f223fe18bf94bb261f414a535149c36fcaebf5/lifegroups/index.html).
