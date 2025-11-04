---
title: [OLD] HelpHub Development
date: June 13, 2016
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/helphub/helphub-development/
---

Note: This project was completed. Thank you for your contribution.

Development is being managed through [GitHub](https://github.com/Kenshino/HelpHub). Guidelines for development are fleshed out in the repo readme, but if you would like to get involved there then please ping @milana\_cap (zzap in Slack) in the [#docs channel on Slack](https://wordpress.slack.com/messages/docs/).

To setup HelpHub development environment on your local computer, please refer the `CONTRIBUTING.md` in above [repository](https://github.com/Kenshino/HelpHub) or [Contributing to the Docs Team (HelpHub)](https://github.com/Kenshino/HelpHub/blob/master/CONTRIBUTING.md).

The latest code from the repository’s master branch will be uploaded to the staging site regularly.

We use ZenHub for project management, see [https://github.com/WordPress/HelpHub/issues/79](https://github.com/WordPress/HelpHub/issues/79) for help on using it.

[Contributing Code](#contributing-code)
---------------------------------------

Like any other website, HelpHub requires design and development work. Your contributions in these areas can assure that HelpHub is as performant and usable as possible.

To facilitate the work of many volunteer developers, HelpHub uses [Varying Vagrant Vagrants (VVV)](https://varyingvagrantvagrants.org/) so developers can easily create a local WordPress environment. Follow the steps in this section to create your development environment and contribute code to the HelpHub project.

[The workflow of getting started](#the-workflow-of-getting-started)
-------------------------------------------------------------------

First thing to start contributing is to set up your local environment. You can choose whichever environment works for you, the main thing is to have fresh WordPress install. You can also follow our [VVV setup below](#installing-vvv).

Once you have WordPress install in your local environment ready, fork [GitHub repository](https://github.com/WordPress/HelpHub), clone your fork to local environment and import database and widget settings. 

Follow instructions in [CONTRIBUTING.md](https://github.com/WordPress/HelpHub/blob/master/CONTRIBUTING.md) file. If you run into problems, get error messages or find the instructions incomplete or incorrect then this is the opportunity for your first contribution. 

If you know how to fix the problem and what’s missing or is incorrect, edit document in your fork and create pull request to HelpHub repo. Do this even if you are not sure if your fix is completely correct or applicable to every OS. We will review it and ask for changes if needed.

If you don’t know how to fix the problem, please ask for help in #docs channel or send direct message to @milana\_cap (zzap in Slack). Once the problem is fixed it would be great if you could update the GitHub document. 

Now you are ready for first development task.

[Installing VVV](#installing-vvv)
---------------------------------

### [Overview](#overview)

The objectives of the procedure described here are to:

1.  create a local WordPress installation where you can do development and design work and
2.  contribute that work to the HelpHub project.

This process uses [Vagrant](https://www.vagrantup.com/), which allows you to create a sandboxed development environment on your computer. Vagrant provides an environment that isn’t specific to WordPress (or any other application), so you’ll also use [VVV](https://varyingvagrantvagrants.org/) to configure your Vagrant environment specifically for WordPress development.

### [Installing and Configuring VVV](#installing-and-configuring-vvv)

1.  **Install Vagrant.** Download Vagrant from [this site](https://www.vagrantup.com/downloads.html) and install it on your machine.
2.  **Install Virtualbox.** Download VirtualBox from [this site](https://www.virtualbox.org/wiki/Downloads) and install it on your machine.
3.  **Install Vagrant plugins.**  You will need 2 vagrant plugins to run VVV, install them using: `vagrant plugin install vagrant-hostsupdater vagrant-triggers`.
4.  **Install and Launch VVV.** [Follow the VVV setup instructions here](https://varyingvagrantvagrants.org/docs/en-US/installation/)

### [Using Your Local Development Environment](#using-your-local-development-environment)

VVV is now running locally, which means you can access several versions of the WordPress application and the WordPress core source code. Click the links below to explore your VVV environment.

*   [http://vvv.test](http://vvv.test) Your VVV home page. Links to local dev sites and admin tools.
*   [http://local.wordpress.test/](http://local.wordpress.test/) for WordPress stable.
*   [http://local.wordpress-trunk.test/](http://local.wordpress-trunk.test/) for WordPress trunk.
*   [http://src.wordpress-develop.test/](http://src.wordpress-develop.test/) for trunk WordPress development files.
*   [http://build.wordpress-develop.dev/](http://build.wordpress-develop.test/) for the version of those development files built with Grunt.

You can use your IDE to change any of the files in the environment, developing features and bugfixes and testing them locally. To learn how to contribute your changes back to the HelpHub project, see the next section.

[Using GitHub to Contribute Code to HelpHub](#using-github-to-contribute-code-to-helphub)
-----------------------------------------------------------------------------------------

If you’re interested in contributing to HelpHub as a developer or designer, you can assign yourself an [issue from the GitHub repo](https://github.com/Kenshino/HelpHub/issues) and contribute code to fix a bug or add a feature.

1.  **Fork the project.** Create a fork of the HelpHub source code from [https://github.com/Kenshino/HelpHub](https://github.com/Kenshino/HelpHub). This fork is where you’ll commit any changes that you intend to contribute to the HelpHub project.
2.  **Create a local environment.** See “**Installing and Configuring VVV**” above.
3.  **Backup wp-content.** In your development environment, rename wp-content to something. Later, you will need the current theme contents to access the Administration Screen.  
    For example, if you have installed VVV under `~/vagrant-local`.  
    `$ cd ~/vagrant-local/www/wordpress-develop/public_html/src`  
    `$ mv wp-content wp-content-original`
4.  **Clone your fork locally.** Clone your fork of the HelpHub repo as a wp-content.  
    `$ git clone https://github.com/[githubusername]/HelpHub.git wp-content`
5.  **Copy back your current theme.** If your environment is new one, it must be “Twenty Seventeen”.  
    `$ cp -r wp-content-original/themes/twentyseventeen wp-content/themes/twentyseventeen`
6.  **Switch your theme to HelpHub.** From Web browser, access [http://src.wordpress-develop.dev/wp-admin (Administration Screens)](http://src.wordpress-develop.dev/wp-admin) and switch your theme to HelpHub.  
    After that you may remove your old theme files or wp-content-original folder you made in above Step 3.
7.  **Import the HelpHub data.** HelpHub’s source code includes a database export (helphub.wordpress.{DATE}.xml). Import this data into your local WordPress site to add a snapshot of the content.  
    For more detail info, refer [CONTRIBUTING.md in the GitHub repo](https://github.com/Kenshino/HelpHub/blob/master/CONTRIBUTING.md).
8.  **Make your changes in VVV.** Develop and test your feature or bugfix in your VVV clone.
9.  **Commit your changes.** Commit your revised code to your HelpHub fork.
10.  **Create a pull request.** Request to merge your commits into the HelpHub repo from your fork.

[Development Guidelines](#development-guidelines)
-------------------------------------------------

To make the site usable, and to keep our codebase manageable, we’re committed to these guidelines and standards.

*   **Accessibility** HelpHub should be usable by all, including users with physical and cognitive disabilities, and those using assistive technologies. Our work must not create any obstacles or limit the access of these users. We embrace tools and processes that facilitate creating an accessible HelpHub, and we value design and testing that maximize accessiblity.
*   **Responsive Design** We’re committed to designing, building and maintaining a site that is usable on devices of varying sizes and platforms.
*   **Standardized Code** We adhere to the [WordPress Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/). We aim to create code that is consistent and readable. The HTML, CSS, PHP and Javascript created by the WordPress community should always follow the appropriate coding standard.