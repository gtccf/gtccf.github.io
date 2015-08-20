# gtccf.github.io
GTCCF website, generated with Jekyll.

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
You should already know how to do this. Your distro probably will not have a recent enough version, so you'll need to install it another way such as through rvm.

## Previewing the site
* Open up a terminal in the root folder of this repository.
* `jekyll serve -w`
* In your browser, navigate to http://localhost:4000/
* Edit the site source in your favorite text editor.
* The site should automatically update a few seconds after you save a file. You'll need to refresh the page to see changes.

## Publishing changes
Just commit your changes in Git and push to this repository. The live site should update within a few minutes.
