---
title: Updating Bundled Theme Versions
date: July 16, 2015
author: 
categories: 
url: https://make.wordpress.org/core/handbook/about/release-cycle/update-bundled-themes-2/
---

With each release, new bundled theme versions should be published to the WordPress.org theme directory when changes have been made.

Here is a list of steps that should be followed to prepare bundled themes to release a new version:

1.  Read each theme’s changelog in Trac, and create a changelog file with the highlights (used in Trac tickets, both core and theme review). The changelog should start at the last version of the theme released.
    *   [Twenty Twenty-Four log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyfour/)
    *   [Twenty Twenty-Three log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentythree/)
    *   [Twenty Twenty-Two log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentytwo/)
    *   [Twenty Twenty-One log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwentyone/)
    *   [Twenty Twenty log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwenty/)
    *   [Twenty Nineteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentynineteen/)
    *   [Twenty Seventeen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyseventeen/)
    *   [Twenty Sixteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentysixteen/)
    *   [Twenty Fifteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfifteen/)
    *   [Twenty Fourteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyfourteen/)
    *   [Twenty Thirteen log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentythirteen/)
    *   [Twenty Twelve log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentytwelve/)
    *   [Twenty Eleven log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyeleven/)
    *   [Twenty Ten log](https://core.trac.wordpress.org/log/trunk/src/wp-content/themes/twentyten/)
2.  Create a new core Trac ticket (like [#54783](https://core.trac.wordpress.org/ticket/54783)
    
    #### [Bump default theme versions for WordPress 5.9](https://core.trac.wordpress.org/ticket/54783)
    
    Ticket #54783
    
    The release of 5.9 will be accompanied by a release for all default themes. The new versions are as follows:
    
    Twenty Twenty-One: 1.5  
    Twenty Twenty: 1.9  
    Twenty Nineteen: 2.2  
    Twenty Seventeen: 2.9  
    Twenty Sixteen: 2.6  
    Twenty Fifteen: 3.1  
    Twenty \[…\]
    
    ##### Last 2 Comments
    
    *   desrosj — 3:19 pm on January 22, 2022
        
        *   **status** changed from _reopened_ to _closed_
        *   **resolution** set to _fixed_
        \[…\]
        
    *   prbot — 2:07 pm on January 22, 2022
        
        [​desrosj](https://github.com/desrosj) commented on [� \[…\]](https://github.com/WordPress/wordpress-develop/pull/2170#issuecomment-1019276727)
        
    
    Owner: desrosjType: task (blessed)Status: closedComponent: Bundled ThemeSeverity: normalUpdated: 4 years ago
    
    ) to bump the POT and versions for each theme.
3.  Locally, check out the current version of the theme from the WordPress.org theme directory, e.g., the largest number in each of these directories:
    *   [Twenty Twenty-Four](https://themes.svn.wordpress.org/twentytwentyfour/)
    *   [Twenty Twenty-Three](https://themes.svn.wordpress.org/twentytwentythree/)
    *   [Twenty Twenty-Two](https://themes.svn.wordpress.org/twentytwentytwo/)
    *   [Twenty Twenty-One](https://themes.svn.wordpress.org/twentytwentyone/)
    *   [Twenty Twenty](https://themes.svn.wordpress.org/twentytwenty/)
    *   [Twenty Nineteen](https://themes.svn.wordpress.org/twentynineteen/)
    *   [Twenty Seventeen](https://themes.svn.wordpress.org/twentyseventeen/)
    *   [Twenty Sixteen](https://themes.svn.wordpress.org/twentysixteen/)
    *   [Twenty Fifteen](https://themes.svn.wordpress.org/twentyfifteen/)
    *   [Twenty Fourteen](https://themes.svn.wordpress.org/twentyfourteen/)
    *   [Twenty Thirteen](https://themes.svn.wordpress.org/twentythirteen/)
    *   [Twenty Twelve](https://themes.svn.wordpress.org/twentytwelve/)
    *   [Twenty Eleven](https://themes.svn.wordpress.org/twentyeleven/)
    *   [Twenty Ten](https://themes.svn.wordpress.org/twentyten/)
4.  Compare with a diff tool to the theme versions in core trunk, is there anything to test or note specifically? Any big unexpected changes?
5.  Test! Load the themes on all recent versions of WordPress (five back is a good place to start). Run the [Theme Check plugin](https://wordpress.org/plugins/theme-check/), and check for any errors or things we didn’t catch in the core cycle.
6.  Bump the theme versions by 0.1 in core, in each stylesheet.
7.  For themes with a `package.json` and/or `composer.json` file, the `version` should be bumped by 0.1. The `package-lock.json` must also be updated by running `npm install`.
8.  Update “Tested up to” in each readme.
9.  If you’re updating Twenty Ten or Twenty Eleven, wait for the POT update for each theme to be committed, then proceed to make the ZIP packages (a committer is needed to trigger the POT files update). This can be done like this example `php makepot.php wp-theme ../../src/wp-content/themes/twentyeleven twentyeleven.pot`. Run that from the `tools/i18n` directory. For all other default themes, translations are managed by WordPress.org GlotPress, outside of the theme. So this step isn’t necessary for Twenty Twelve and later.
10.  Run the theme build script when one is present (currently Twenty Nineteen, Twenty Twenty, and Twenty Twenty-One). Some themes copy the version into generated files (RTL stylesheets, etc.).

[Creating Theme ZIP Files](#creating-theme-zip-files)
-----------------------------------------------------

The recommended way to create the Zip file for a bundled theme update is using the [Test Default Themes & Create ZIPs](https://github.com/WordPress/wordpress-develop/actions/workflows/test-and-zip-default-themes.yml) workflow. This workflow creates a ZIP file for each theme after performing several safety checks, such as ensuring there are no uncommitted changes to built files, and [checking for zero-byte files](https://core.trac.wordpress.org/changeset/56792).

This workflow should be manually run when the time has come to release the themes. All Core Committers have the ability to manually dispatch a run of the workflow. There are two input fields when clicking “Run workflow”:

*   Use workflow from – This should always be left as **trunk**. Changes to the workflow are not backported to older branches. So running from `trunk` is always preferred to ensure the latest logic is used.
*   The branch to create ZIP files from – This should be changed to the numbered branch that has the desired theme source code. Leaving this as `trunk` may result in undesired changes being included.

[![A screenshot of the GitHub Actions workflow interface. The Run workflow dropdown has been clicked, and the two fields explained in this post are visible followed by a "Run workflow" button.](https://make.wordpress.org/core/files/2015/07/test-default-themes-and-create-zips-workflow.png)](https://make.wordpress.org/core/files/2015/07/test-default-themes-and-create-zips-workflow.png)

After the workflow completes, the ZIP files will be attached to the workflow run and can be found on the [run’s summary page](https://github.com/WordPress/wordpress-develop/actions/runs/16759305233) as artifacts.

### [Alternate Method](#alternate-method)

The following method is documented as a backup method for historical reference but is no longer recommended as the default way to package theme releases. There are a few nuances that are easy to miss when bundling manually (such as accidentally changing the line endings for files depending on system type), so extra care should be taken.

*   `svn export` from core repository to a temporary location on your local hard drive.
*   Do another quick diff with the previous version for a final sanity check.
*   Zip it: `zip -r [name].zip name` **(Be sure the file name is the same as the theme directory path, otherwise the theme repository will consider the theme new on upload.)**

[Release Day and Deploying the Update to the Theme Directory](#release-day-and-deploying-the-update-to-the-theme-directory)
---------------------------------------------------------------------------------------------------------------------------

All contributors with WordPress Core commit access are able to upload new versions of the default themes to WordPress.org through the [theme uploader](https://wordpress.org/themes/getting-started/). Updates should be approved automatically after submitting provided all of the checks that confirm a new version is being uploaded pass. When releasing on the same day as a version of WordPress, coordinate with the release squad.

Here is a checklist to use when releasing themes.

*   Run through the above checklist to make sure every step has been accounted for.
*   Share a message in [#core](https://wordpress.slack.com/archives/C02RQBWTW) that you are beginning the theme release process. This does not need to be a `@here` mention.
*   Dispatch a run of the GitHub Actions Workflow.
*   Once it completes, ask for help testing and verifying the ZIP files for each theme receiving an update. Perform your own testing and verification.
*   Upload the themes one at a time to the [Theme Submission page](https://wordpress.org/themes/upload/).
*   Inspect the Theme Trac tickets created and examine the “Diff with previous version” for any unexpected changes.
*   Notify [#core](https://wordpress.slack.com/archives/C02RQBWTW) when you’ve completed the process and all themes are uploaded.

**Note**: theme updates will go live _automatically_ if manual intervention is not taken beforehand by the theme or meta team. If this is not desired, contact them first to prevent the go-live process. If needed: note in the ticket, “Do not approve yet, please. We’d like to coordinate with the core release_.”_

Ping the release lead to coordinate with the main release process. The updates should be approved automatically. If anything goes wrong, [@Otto42](https://profiles.wordpress.org/Otto42/) can help.

[Tips](#tips)
-------------

*   If a major version of WordPress is also being released with a new bundled theme, the oldest theme being bundled needs to be removed from the build script. **To keep packages sizes down, only the 3 most recent default themes should be included in WordPress packages.**
*   If a theme has any code changes, that means it should get a version number bump and changelog update. Not updating the version number means a new version of the theme can’t be uploaded to the theme directory.
*   Sometimes when looking at the diff of changes after a theme is uploaded, you may notice image or font files showing up as changed when they haven’t been changed. This is a [Trac oddity](https://wordpress.slack.com/archives/core-themes/p1471287983000406).
*   All default themes are marked as special cases on WordPress.org Themes Trac. Themes marked as special still show the theme check errors, but they upload anyway.