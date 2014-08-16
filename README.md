

## Overview

[Middleman](http://middlemanapp.com/) template with Haml, Compass, and
CoffeeScript.

It is shameless based on [Sauce](https://github.com/nikiliu/sauce).

Please download [Modernizr](http://modernizr.com) to your JS vendor dir for production, here comes only the development version.

This template includes:

  - Haml/Sass, Compass, CoffeeScript
  - Normalisation via `rails-assets-normalize-css`
  - [Modernizr](http://modernizr.com)
  - [Kube](http://imperavi.com/kube/) CSS Framework

## Installing / Updating

    # Clone the repo as a Middleman template
    git clone git@github.com:LeFnord/dip.git ~/.middleman/dip

    # Update to latest version
    cd ~/.middleman/dip/; git pull


## Usage

    # Scaffold a project using Sauce
    middleman init [my_project] --template=dip

    # Optionally remove default README and Git repository
    cd ~/.middleman/dip/; rm -rf README .git/

    # Fire up a local development server (LiveReload equipped)
    bundle exec middleman server

    # Build a production-ready version of your app
    bundle exec middleman build


## File Structure

    |-- source/
    |   |-- assets
    |   |    |-- images/
    |   |    |   |- sauce.png             # Sauce logo
    |   |    |
    |   |    |-- javascripts/
    |   |    |   |- modules/              # Individual JavaScript modules
    |   |    |   |- vendor/               # For any third-party plugins
    |   |    |   |
    |   |    |   |- application.coffee    # Manifest file
    |   |    |
    |   |    |-- stylesheets/
    |   |       |-- components/           # Individual Sass components
    |   |       |-- config/
    |   |       |   |- _colors.scss       # Color config
    |   |       |   |- _typography.scss   # Typography config
    |   |       |   |- _general.scss      # General config
    |   |       |   |- _media.scss        # Media query config
    |   |       |
    |   |       |-- vendor/               # third party
    |   |       |   |- kube.css           # CSS Framework
    |   |       |   |- kube.min.css       # CSS Framework
    |   |       |
    |   |       |- application.scss       # Manifest file
    |   |                                 
    |   |-- layouts/                      
    |   |   |- main.haml                  # Main layout
    |   |                                 
    |   |- favicon.ico                    # Sauce favicon
    |   |- index.haml                     # Default page
    |                                     
    |- .gitignore                         # Git ignore
    |- config.rb                          # Middleman config
    |- Gemfile                            # Dependencies
    |- Gemfile.lock                       # Last verified dependencies
    |- Rakefile                           # Rake tasks
    |- README.md                          # This README


## Publishing to gh-pages

Sauce includes [middleman-gh-pages](https://github.com/neo/middleman-gh-pages).

    # Publish a build to the gh-pages branch on GitHub
    bundle exec rake publish
