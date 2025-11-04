---
title: Set up a local instance of HelpHub
date: September 29, 2020
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/get-involved/how-to-videos/set-up-a-local-instance-of-helphub/
---

**What is HelpHub?**

HelpHub is a code name for WordPress end user documentation. It lives at [wordpress.org/support](https://wordpress.org/support/).

**The problem of setting up HelpHub locally**

When set up locally, HelpHub will be a standalone WordPress install while WordPress.org is a network of networks. This network is sharing header and footer so the code we get from SVN is not a full website and we need to make some changes in files to make it work as a standalone website, while those changes, that we make, need to remain only in our local instance.

**Requirements**

*   [GIT](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
*   [SVN](https://docs.oracle.com/middleware/1213/core/MAVEN/config_svn.htm#MAVEN8817)
*   [Node.js and npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
*   local WordPress install
*   modified `allow_url_fopen` and `allow_url_include` values in php.ini file as noted in [Contributing docs](https://github.com/WordPress/HelpHub/blob/master/CONTRIBUTING.md#local-install).
*   [WP-CLI](https://make.wordpress.org/cli/handbook/guides/installing/) (optional)

**GIT Structure**

`master` branch will be used for getting updates from SVN, from production. Then those updates are rebased to the `developmen`t branch. This branch holds the changes we are going to make, which are needed for the website to function as a standalone. From the `development` branch, it’s advised that new (feature) branch is created, where bug fixes and feature code will be added. This part will not be covered with this tutorial but that is a general structure and workflow.

Plugins and theme

*   HelpHub theme – https://meta.svn.wordpress.org/sites/trunk/wordpress.org/public\_html/wp-content/themes/pub/wporg-support/
*   HelpHub plugin – https://meta.svn.wordpress.org/sites/trunk/wordpress.org/public\_html/wp-content/plugins/support-helphub/
*   bbPress – https://wordpress.org/plugins/bbpress/
*   WordPress Importer – https://wordpress.org/plugins/wordpress-importer/
*   Widget Importer & Exporter – https://wordpress.org/plugins/widget-importer-exporter/

Setup
-----

When everything is ready, use terminal to navigate to the root of your WordPress install and initiate GIT repository.

git init 

Get HelpHub theme and plugin.

svn checkout https://meta.svn.wordpress.org/sites/trunk/wordpress.org/public\_html/wp-content/themes/pub/wporg-support/ wp-content/themes/wporg-support

svn checkout https://meta.svn.wordpress.org/sites/trunk/wordpress.org/public\_html/wp-content/plugins/support-helphub/ wp-content/plugins/support-helphub/

Add these to your GIT repo and commit.

git add -A .

git commit -m "Production."

Create `development` branch, install and activate all needed plugins and theme with WP-CLI.

git checkout -b development

wp theme activate wporg-support

wp plugin activate support-helphub

wp plugin install --activate bbpress

wp plugin install --activate wordpress-importer

wp plugin install --activate widget-importer-exporter

Download and import [.xml file of exported staging database](https://raw.githubusercontent.com/WordPress/HelpHub/master/staging-database/helphub.wordpress.2019-01-14.xml), and do the same with [.wie file of exported staging widgets](https://raw.githubusercontent.com/WordPress/HelpHub/master/staging-database/Widget%20Importer%20%26%20Exporter/wp-helphub.com-widgets.wie). Other options can be found in [GitHub repo](https://github.com/WordPress/HelpHub/tree/master/staging-database). These databases are out of date, comparing to production, but we really need only some data to be able to work on bugs and features.

At this point you’ll have critical error on your local instance. Fix it with adding following in `wp-config.php` file (in the root dir of your WordPress install):

define( 'WP\_DEBUG', true );

define( 'WPORGPATH', 'https://wordpress.org/' );

Open `wp-content/themes/wporg-support/header.php` file and find this line `wporg_get_global_header();`. Right after add

do\_action( 'wp\_head' );

And outside of PHP tags:

<body <?php body\_class( array( 'single-handbook', 'make-docs' ) ); ?>>

You can add closing `</body>` and `</html>` tags in `wp-content/themes/wporg-support/footer.php` but that is not really necessary.

Navigate to the theme, install npm packages and run grunt.

cd wp-content/themes/wporg-support/

npm install

grunt build

Now add all this to your GIT repo and commit.

git add -A .

git commit -m "Local setup."

From here you can create new branch and work on new code or fix bug in old code. We will cover this process in another tutorial.