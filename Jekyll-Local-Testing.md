# Testing your site locally before building on github

#### To test your site locally, you’ll need:
- ruby
- the github-pages gem

#### Installing ruby

In Mac OS X, older versions of ruby will already be installed. Use the Ruby Version Manager (RVM) to have a more recent version.
In Windows, use RubyInstaller. 

#### Installing the github-pages gem

Run the following command:
* gem install github-pages
This will install the github-pages gem and all dependencies (including jekyll).

To update the gem, type:
* gem update github-pages

#### Testing your site locally

To construct and test your site locally, go into the directory and type
* ng build

This will create the dist folder. Then type:
* jekyll build

This will copy from the dist folder and create (or modify) a _site/ directory, containing everything from assets/, and then the index.md and all pages/*.md files, converted to html. (So there’ll be _site/index.html and the various _site/pages/*.html.)

#### "Serving" the site

This will first run build, and so it does not need to be preceded by jekyll build. Make sure you run first: **ng build**
* jekyll serve

#### Observation:

Building the dist folder with the following command will make the server to serve the website from the wrong base-href. That is why when testing locally, you only build your site using "ng build": 
ng build --prod --base-href https://alextelespanwork.github.io/my-cool-proj/