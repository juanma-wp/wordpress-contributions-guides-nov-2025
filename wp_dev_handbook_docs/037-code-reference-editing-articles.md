---
title: [OLD] Editing Articles
date: July 16, 2015
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/code-reference/editing-articles/
---

Note: This project was completed. Thank you for your contribution.

[Codex to Code Reference](#codex-to-code-reference)
---------------------------------------------------

As an example, let’s compare two pages of `add_action` to understand which sections are transferred to which areas:

**Codex (archives):**  
[https://codex.wordpress.org/index.php?title=Function\_Reference/add\_action&oldid=152725](https://codex.wordpress.org/index.php?title=Function_Reference/add_action&oldid=152725)  

**Code Reference:**  
[https://developer.wordpress.org/reference/functions/add\_action/](https://developer.wordpress.org/reference/functions/add_action/)

### [Description, Syntax, Parameters and Returns](#description-syntax-parameters-and-returns)

The Description, Syntax, Parameters and Returns should be converted to inline docs in the function header. These inline docs are automatically converted and added to the Code Reference.

For our example, refer to this source code. [https://core.trac.wordpress.org/browser/tags/5.2/src/wp-includes/plugin.php#L384](https://core.trac.wordpress.org/browser/tags/5.2/src/wp-includes/plugin.php#L384). As you can see, the function header includes description and @since, @param and @return tags. Those tags form the Description, Syntax, and Parameters for this function and have been automatically added to the Code Reference.

All functions already have inline docs but not with the same level of information as the Codex. A lot of information was dropped during initial function header creation.

To add/update inline docs, refer to this page:  
[https://make.wordpress.org/docs/handbook/code-reference/inline-documentation/](https://make.wordpress.org/docs/handbook/code-reference/inline-documentation/). You will need some development skills to build the environment and contribute.

Notes: Inline docs may not have enough syntax or space to describe every detail parameters or returned values. In these cases, use `Explanation` field.

### [Usage, Notes and Programming Topics](#usage-notes-and-programming-topics)

These should be migrated to the `Explanation` field of the Code Reference and are displayed in the “More Information” section.

Note: One line Usage such as the following do not need to be migrated due to its triviality.

```
<?php get_post_comments_feed_link( $post_id, $feed ) ?>
```

To add/edit the `Explanation` field, your WordPress.org account need to have an editor role or above added for the Developer Reference. To be added, go to the [#docs](https://wordpress.slack.com/messages/docs/) channel on [slack](https://make.wordpress.org/chat/) and ask one of the rep on [The Team](https://make.wordpress.org/docs/handbook/the-team/) to add you.

### [Usage Examples](#usage-examples)

Usage examples are migrated as the User Comments for each page.

Refer to this document for more details: [https://make.wordpress.org/docs/handbook/code-reference/editing-articles/migrating-from-codex/](https://make.wordpress.org/docs/handbook/code-reference/editing-articles/migrating-from-codex/)

[Getting Started](#getting-started)
-----------------------------------

We’re tracking the migration of the Codex to the Code Reference in this spreadsheet:   
[https://docs.google.com/spreadsheets/d/15hpEbbnuWJZ0DJafyCeG3CFRMtSxX1gY-RObrrjzzdw/edit#gid=1679372392](https://docs.google.com/spreadsheets/d/15hpEbbnuWJZ0DJafyCeG3CFRMtSxX1gY-RObrrjzzdw/edit#gid=1679372392)

### [First reserve the page where you want to edit.](#first-reserve-the-page-where-you-want-to-edit)

1.  In the tracking spreadsheet, search for ‘Partially done’ rows using the Status column (Column H).
2.  Enter your name in the Editor column (Column F) and change the Status column (Column H) to ‘In Progress’. If you don’t have write permission to the spreadsheet, please DM your Google account to @atachibana on #docs channel.

### [Compare Codex and Code Reference](#compare-codex-and-code-reference)

3.  Open Codex page and Code Reference page and compare them
4.  If Code Reference has full information of Codex, then OK
5.  If Code Reference does not have some information, refer above [Codex to Code Reference](#codex-to-code-reference) and migrate missing information on the Codex page to the Code Reference appropriately.

*   When you create a Ticket to modify the inline documentation, change the status to ‘Waiting’, and leave the ticket number in Notes (Column I).
*   If you cannot migrate every section, leave a comment in the Notes column (Column I) noting what’s left and change the Status to ‘Partially done’.

### [Redirect the page from Codex to Code Reference.](#redirect-the-page-from-codex-to-code-reference)

After the migration complete, redirect codex page to Code Reference.

#### [When the Codex page has a language locator](#when-the-codex-page-has-a-language-locator)

1.  From the Codex page, click Edit on right side menu.
2.  Put following message below the language locator, and comment out the current Codex contents using `<!--` and `-->`.

{{Languages|
{{en|WordPress Features}}
{{ja|WordPress Features}}
}}
This page was moved to https://developer.wordpress.org/reference/functions/(function name)/ except above language locator.

3.  Click Show Preview at the bottom of the page and confirm your changes.
4.  Enter the text “Transferred to DevHub” in the Summary box and click Save page.

#### [When the Codex page does not have a language locator](#when-the-codex-page-does-not-have-a-language-locator)

1.  From the Codex page, click Edit on right side menu.
2.  Put following tag at the top of the page, and adjust the URL.

{{#dotorgredirect: https://developer.wordpress.org/reference/functions/(function name)/}}

3.  Enter the text “Transferred to DevHub” in the Summary box and click Save page.

NOTE: Once you save the page, viewing the page will redirect you to the DevHub version of the page. If you want to modify the saved page, add `&action=edit` to the URL.  
e.g. [https://codex.wordpress.org/index.php?title=Function\_Reference/add\_action&action=edit](https://codex.wordpress.org/index.php?title=Function_Reference/add_action&action=edit)

### [Release this page](#release-this-page)

Change the “In Progress” status to “Done” (Column H).

[Progress Stats](#progress-stats)
---------------------------------

[https://docs.google.com/spreadsheets/d/15hpEbbnuWJZ0DJafyCeG3CFRMtSxX1gY-RObrrjzzdw/edit#gid=1576070270](https://docs.google.com/spreadsheets/d/15hpEbbnuWJZ0DJafyCeG3CFRMtSxX1gY-RObrrjzzdw/edit#gid=1576070270)