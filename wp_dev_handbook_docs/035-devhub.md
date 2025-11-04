---
title: Devhub
date: February 27, 2014
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/devhub/
---

Devhub is the project name for [developer.wordpress.org](http://developer.wordpress.org), which was deployed and is still under active development. A [full project specification is available on the Make/Meta blog](https://make.wordpress.org/meta/2013/08/14/developer-wordpress-org-specification/).

Devhub is a new home for developer documentation on WordPress.org. It comprises:

*   an auto-generated code reference
*   targeted handbooks for developers

The project requires the following types of contributors:

*   PHP developers
*   front-end developers
*   designers and UXers
*   anyone who wishes to provide feedback

[What needs to be worked on](#what-needs-to-be-worked-on)
---------------------------------------------------------

*   improvements to WP-Parser
*   enhancements to the site, including upvoting and commenting
*   improvements to the theme, including the code reference and handbooks
*   testing and feedback

[To get involved](#to-get-involved)
-----------------------------------

You can get involved in the following ways:

*   join the [#meta-devhub](https://wordpress.slack.com/messages/meta-devhub/) channel on [Slack](https://make.wordpress.org/chat/)
*   find a ticket on the [Developer Hub](https://meta.trac.wordpress.org/query?status=!closed&component=Developer+Hub) trac component or an issue in the [Developer Resources](https://github.com/WordPress/wporg-developer/issues) GitHub repository
*   submit a pull request to [WP-Parser](https://github.com/WordPress/phpdoc-parser) on Github
*   read up on the [devhub tag](https://make.wordpress.org/docs/tag/devhub) on make/docs

[Setting up your development environment](#setting-up-your-development-environment)
-----------------------------------------------------------------------------------

To develop on developer.wordpress.org you will need to set up your local development environment. Visit the [Developer Resources](https://github.com/WordPress/wporg-developer) GitHub repository for instructions.

### [Handbook Setup](#handbook-setup)

Handbooks are updated using cron and so it may be beneficial to install a plugin such as [WP Crontrol](https://en-ca.wordpress.org/plugins/wp-crontrol/) that allows viewing and running jobs in the WordPress admin.

Alternatively, jobs can be run as needed using WP CLI.

1

`wp` `cron` `event run devhub_blocks_import_all_markdown`