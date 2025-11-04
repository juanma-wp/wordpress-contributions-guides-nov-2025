---
title: [OLD] Inline Documentation
date: February 27, 2014
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/code-reference/inline-documentation/
---

Note: This project was completed. Thank you for your contribution.

WordPress’ current inline documentation efforts really kicked off starting in the 3.7 release cycle, and gained momentum as the hook docs initiative progressed. The inline documentation, or “inline docs” initiative is a hybrid project, reporting to the Core, Documentation, and Developer Hub teams.

[What is inline documentation?](#what-is-inline-documentation)
--------------------------------------------------------------

Inline documentation provides both necessary and useful information in the form of inline-comments, doc blocks, and more within the source code of WordPress itself.

The inline documentation is parsed with each release, and that documentation is displayed in the Code Reference at developer.wordpress.org.

[How to get involved](#how-to-get-involved)
-------------------------------------------

Inline documentation is considered to be “technical” documentation, so some familiarity with the WordPress codebase will be necessary – you have to understand the code to write about it.

1\. Familiarize yourself with the [PHP Documentation Standard](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/), as well as the [formatting guidelines](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/#formatting-guidelines) and [documenting tips](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/#documenting-tips).

2\. Set up a local copy of the developer version of the WordPress codebase using [Varying Vagrant Vagrants](https://make.wordpress.org/core/handbook/tutorials/installing-a-local-server/installing-vvv/) (VVV). WordPress is versioning using SVN, but you can also use Git (the VVV link for how to do that).

3\. Read [Opening a Ticket](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/) to learn how to create a Trac ticket.

4\. Creating patches:

*   Always update your local copy of WordPress trunk before editing the file and creating patches. Use `svn up` or `git pull`, as appropriate.
*   Generate the patch from the root directory of your WordPress SVN or Git checkout. For example, `svn diff dir/filename.php > function_name.diff`.

5\. How to submit a patch

There is one patch to report the inline documentation failures and   
For example, [#48303](https://core.trac.wordpress.org/ticket/48303) is such patch for the WordPress 5.4.

*   Add Comment and attach patch file.

6\. You can also contribute to [inline docs-related Trac tickets](https://core.trac.wordpress.org/query?status=!closed&focuses=~docs) that need iteration.

*   If a ticket is marked **needs-patch** or **needs-refresh**, it’s possible the existing patch(es) might just need a touch-up or be refreshed against the latest trunk. Every little bit helps!

[Points of contact](#points-of-contact)
---------------------------------------

For any questions, pop by the [#docs](https://wordpress.slack.com/messages/docs/) or [#core-docs](https://wordpress.slack.com/messages/core-docs) channels in [Slack](https://make.wordpress.org/chat/).

[Resources](#resources)
-----------------------

*   [PHP Documentation Standard](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/php/)
*   [Adam Brown’s Hooks Database](http://adambrown.info/p/wp_hooks) (useful for hints on the `@since` versions of hooks)

[How to open new document ticket](#how-to-open-new-document-ticket)
-------------------------------------------------------------------

Basically, there is one ticket to report the inline documentation failures and improvements. But, if you need create new ticket for some reason, follow below steps:

1.  Read [Opening a Ticket](https://make.wordpress.org/core/handbook/working-with-trac/opening-a-ticket/) to learn how to create a Trac ticket.
2.  Create a [new ticket](https://core.trac.wordpress.org/newticket) on Core Trac for the file:
    *   Suggested _Title_ formats could be “PHPDoc correction for path/to/file.php” or “Improve documentation for path/to/file.php”.
    *   The _Type_ should be **defect (bug)**.
    *   Assign the ticket to the _Component_ the file is associated with.
    *   Leave the _Version_ blank.
    *   Add the **docs** _Focus_ by clicking on it.
3.  Upload your patch to the Trac ticket you created, and add the keyword **has-patch**.
4.  Make sure to leave a comment describing your newly-uploaded patch. Simply uploading patches doesn’t trigger a notification for anyone watching the ticket.

Note: Documentation changes should not mix with code changes (even whitespacing) unless the ticket specifically calls for both.