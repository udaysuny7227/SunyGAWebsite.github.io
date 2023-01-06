Skip to content
Search or jump to…
Pull requests
Issues
Codespaces
Marketplace
Explore
 
@udaysuny7227 
pages-themes
/
architect
Public
Code
Issues
5
Pull requests
8
Actions
Security
Insights
architect/README.md
@parkr
parkr Update README.md
Latest commit fcd1fc6 on Jul 26, 2021
 History
 2 contributors
@benbalter@parkr
116 lines (75 sloc)  5.6 KB

The Architect theme
.github/workflows/ci.yaml Gem Version

Architect is a Jekyll theme for GitHub Pages. You can preview the theme to see what it looks like, or even use it today.

Thumbnail of Architect

Usage
To use the Architect theme:

Add the following to your site's _config.yml:

remote_theme: pages-themes/architect@v0.2.0
plugins:
- jekyll-remote-theme # add this line to the plugins list if you already have one
Optionally, if you'd like to preview your site on your computer, add the following to your site's Gemfile:

gem "github-pages", group: :jekyll_plugins
Customizing
Configuration variables
Architect will respect the following variables, if set in your site's _config.yml:

title: [The title of your site]
description: [A short description of your site's purpose]
Additionally, you may choose to set the following optional variables:

show_downloads: ["true" or "false" (unquoted) to indicate whether to provide a download URL]
google_analytics: [Your Google Analytics tracking ID]
Stylesheet
If you'd like to add your own custom styles:

Create a file called /assets/css/style.scss in your site
Add the following content to the top of the file, exactly as shown:
---
---

@import "{{ site.theme }}";
Add any custom CSS (or Sass, including imports) you'd like immediately after the @import line
Note: If you'd like to change the theme's Sass variables, you must set new values before the @import line in your stylesheet.

Layouts
If you'd like to change the theme's HTML layout:

For some changes such as a custom favicon, you can add custom files in your local _includes folder. The files provided with the theme provide a starting point and are included by the original layout template.
For more extensive changes, copy the original template from the theme's repository
(Pro-tip: click "raw" to make copying easier)
Create a file called /_layouts/default.html in your site
Paste the default layout content copied in the first step
Customize the layout as you'd like
Customizing Google Analytics code
Google has released several iterations to their Google Analytics code over the years since this theme was first created. If you would like to take advantage of the latest code, paste it into _includes/head-custom-google-analytics.html in your Jekyll site.

Overriding GitHub-generated URLs
Templates often rely on URLs supplied by GitHub such as links to your repository or links to download your project. If you'd like to override one or more default URLs:

Look at the template source to determine the name of the variable. It will be in the form of {{ site.github.zip_url }}.
Specify the URL that you'd like the template to use in your site's _config.yml. For example, if the variable was site.github.url, you'd add the following:
github:
  zip_url: http://example.com/download.zip
  another_url: another value
When your site is built, Jekyll will use the URL you specified, rather than the default one provided by GitHub.
Note: You must remove the site. prefix, and each variable name (after the github.) should be indent with two space below github:.

For more information, see the Jekyll variables documentation.

Roadmap
See the open issues for a list of proposed features (and known issues).

Project philosophy
The Architect theme is intended to make it quick and easy for GitHub Pages users to create their first (or 100th) website. The theme should meet the vast majority of users' needs out of the box, erring on the side of simplicity rather than flexibility, and provide users the opportunity to opt-in to additional complexity if they have specific needs or wish to further customize their experience (such as adding custom CSS or modifying the default layout). It should also look great, but that goes without saying.

Contributing
Interested in contributing to Architect? We'd love your help. Architect is an open source project, built one contribution at a time by users like you. See the CONTRIBUTING file for instructions on how to contribute.

Previewing the theme locally
If you'd like to preview the theme locally (for example, in the process of proposing a change):

Clone down the theme's repository (git clone https://github.com/pages-themes/architect)
cd into the theme's directory
Run script/bootstrap to install the necessary dependencies
Run bundle exec jekyll serve to start the preview server
Visit localhost:4000 in your browser to preview the theme
Running tests
The theme contains a minimal test suite, to ensure a site with the theme would build successfully. To run the tests, simply run script/cibuild. You'll need to run script/bootstrap once before the test script will work.

Footer
© 2023 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
architect/README.md at master · pages-themes/architect
