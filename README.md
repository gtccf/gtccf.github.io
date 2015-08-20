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
You will need Ruby 2.1 and the Jekyll rubygem to preview the site.

### On Windows
* Download the installer from http://rubyinstaller.org/
* `gem install jekyll`

### On Mac
* Install Homebrew from http://brew.sh/
* `brew update`
* `brew install rvm`
* `rvm install 2.1.0`
* `rvm use 2.1.0`
* `gem install jekyll`

### On Linux
You should already know how to do this. Your distro probably will not have a
recent enough version, so you'll need to install it another way such as through
rvm.

## Previewing the site
* Open up a terminal in the root folder of this repository.
* `jekyll serve -w`
* In your browser, navigate to http://localhost:4000/
* Edit the site source in your favorite text editor.
* The site should automatically update a few seconds after you save a file.
  You'll need to refresh the page to see changes.

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
