---
title: Editing Articles
date: June 13, 2016
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/helphub/migrating-articles/
---

If you want to join the HelpHub editing tasks (Thank you!), there are some ways:

*   Working issues in the Documentation issue tracker
*   Proof Reading

[Working issues in the Documentation issue tracker](#working-issues-in-the-documentation-issue-tracker)
-------------------------------------------------------------------------------------------------------

The [Documentation issue tracker](https://github.com/WordPress/Documentation-Issue-Tracker) is the central place for contributing to WordPress documentation. No actual documentation is hosted in this repository. Its purpose is to track all the issues for any part of WordPress documentation.

For more details about Documentation issue tracker, refer [this page](https://make.wordpress.org/docs/handbook/github-repository-and-projects/documentation-issue-tracker/).

From Documentaion issue tracker, Look for issues of your interest. The [Good first issues](https://github.com/WordPress/Documentation-Issue-Tracker/labels/good%20first%20issue) tag would be a good candidate. See [this page](https://make.wordpress.org/docs/handbook/get-involved/getting-started-at-a-contributor-day/good-first-issues/) for more information.

Or, you may wish to consider the documentation work required for each version such as [WP 6.6 Documentation](https://github.com/orgs/WordPress/projects/202). For more information refer [this page](https://make.wordpress.org/docs/handbook/github-repository-and-projects/).

Once you have found an issue you want to work on, follow these steps:

1.  You browse issues and find what you like. Post in comment that you’d like to work on it and start working.
2.  Someone will assign you and move issue into “In progress” column.
3.  When your work is ready for review, post another comment mentioning @zzap , [@atachibana](https://profiles.wordpress.org/atachibana/) or someone else if you were discussing it with someone else.
4.  Someone will move issue to “Review” column. After review you’ll be either asked to fix something or if you’d like to update documentation yourself.
5.  When documentation is updated the issue is moved to “Done” column.

[Proof Reading](#proof-reading)
-------------------------------

Read HelpHub page and give us feedback. Any comments are welcome!

1.  Read any pages under the [https://wordpress.org/documentation](https://wordpress.org/documentation).
2.  If you find refinement points, technical errors, editing error etc., [report an issue](https://make.wordpress.org/docs/handbook/workflows/reporting-an-issue/).

Any comments are welcome. For example:

*   Unclear or wrong description
*   Missing steps, URL links
*   Ancient screenshots
*   Ancient description (ex. WordPress 2.x, MySQL 4.1, etc.)
*   Using of out of date Plugins or Themes

[Editing Hints](#editing-hints)
-------------------------------

If you find more inconsistencies or discovered something else we should inform the other migrators; do let us know!

*   **Default editor is Block Editor (Gutenberg).** Some articles were made via the Classic Editor and so will present itself as one single Classic Block. You should use the Copy all Content function on the Staging site and paste it into the Production site. You should then convert the article into actual blocks using the ‘Convert into Blocks’ function on the Production site.
*   When you copy and paste from the Codex, images remain linked to the Codex site. You should manually download images via the Codex site, and add to Media Library of the production site and replace the old contents.  
    **Note**: Check Link Settings of the image. It might point original Codex image as “<a href=” tag. Change it to “Media File”
*   Use simple language – understanding is key! For instructional text: delete long narratives and change them to bullet or numbered list.
*   Use semantic headings: No <H1> in the article content – start sections with H2s and work down from there where appropriate.
*   Add screenshots where appropriate – if the article is describing any user interface element then it _must_ include a screenshot.
*   **\[HelpHub Only, Not for Handbooks\]** Do not include https://wordpress.org when you make the link to other pages in HelpHub, Start from the next “/”. For example,
    *   /support/article/administration-screens/
    *   /support/article/glossary#absolute-path
    *   #roles (to jump in the same page)
    *   /support/wordpress-version/version-5-2/
*   If you find that you are unable to automatically link to articles; it’s because they are in draft mode and not published. You’ll have to do some manual copy and pasting.

If you need the help, Please ping [@Kenshino](https://profiles.wordpress.org/Kenshino/) or [@atachibana](https://profiles.wordpress.org/atachibana/) in [Slack](https://make.wordpress.org/chat/) in the [#docs](https://wordpress.slack.com/messages/docs/) channel.

[Reference](#reference)
-----------------------

*   [Handbooks & HelpHub Style and Formatting Guide](/docs/handbook/documentation-team-handbook/handbooks-style-and-formatting-guide/)

[Archives](#archives)
---------------------

Below projects were completed. Thanks.

[Getting Account](#getting-account)
-----------------------------------

To write/modify the pages under the [https://wordpress.org/support](https://wordpress.org/support), you have to get permission of write access. Send your WordPress.org account and e-mail address to [@atachibana](https://profiles.wordpress.org/atachibana/) on Slack via direct message.

[Gutenberg document modification](#gutenberg-document-modification)
-------------------------------------------------------------------

WordPress Version 5.0 introduced the Block Editor (code name: Gutenberg) instead of the Classic Editor. We need new pages for block editor based on existing page that assumes classic editor. Please modify the contents based on the block editor.

1.  Open the “Gutenberg Docs” tab of Spreadsheet: [https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=2125284625](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=2125284625)
2.  Reserve a target page. Type your name in ‘Writer/Editor’ and change Status to ‘In Process’.
3.  Click the link in ‘Block Editor Page’ column.
4.  Follow the instruction in ‘Tasks’ column. Or please write new article as you like
5.  Save as Draft (Do not Publish, yet)
6.  Change the Status of Spreadsheet to ‘Done’.

### [Transferring Codex page to HelpHub \[good first contribution\]](#transferring-codex-page-to-helphub-good-first-contribution)

As of Apr/2019, almost all migration were completed, and now we need show the warning text at the top of Codex page so that it can tell to visitor that this page was transferred to HelpHub. (e.g. Refer [this page](https://codex.wordpress.org/Contributing_to_WordPress))

Before actual adding the message, we need final review of contents and re-synchronize with the latest Codex contents.  
**Note: This task needs some experience on Codex and HelpHub.**

1\. Reserve the page for your process.  
1) From [this worksheet](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=835534324), search blank or Not Yet in “Transferred” column.  
2) Enter “In Progress”.

2\. Update Codex page so that include the warning message  
1) From codex page, click Edit on right side menu.  
2) Put following message below the language locator, and comment out the current Codex contents by “<–” and “–>”.

{{Languages|
{{en|WordPress Features}}
{{ja|WordPress Features}}
}}
This page was moved to https://wordpress.org/support/article/< HelpHub page> except above language locator.
<!--
... contents ...
-->

3) Click bottom Show preview and confirm your changes.  
4) Enter the text “Transferred to HelpHub” in the Summary box and click Save page.

3\. Release the page  
1) Change “In Progress” to “Done” at above Step 1-2).

4\. (Bonus) Enhance the comments from WCEU 2018 contributor day (Column T)

### [Transferring Version page \[good first contribution\]](#transferring-version-page-good-first-contribution)

As of May/2019, almost all Version page (or release notes) were migrated to HelpHub, and now we need transfer old Codex page to HelpHub page. Already, licking of [https://codex.wordpress.org/Version\_5.0](https://codex.wordpress.org/Version_5.0) is redirected to HelpHub page.

Follow below steps:

1\. Reserve the page for your process.  
1) From [this worksheet](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=1995801274), search blank or Not Yet in “Transferred” column.  
2) Enter “In Progress” into the cell.

2\. Insert transfer tab into Codex page  
1) From codex page, click Edit on right side menu.  
2) Put following tag at the top of the page, and replace `n-n-n` by matched version number. Refer [this page](https://codex.wordpress.org/Version_4.5&action=edit).

{{#dotorgredirect: https://wordpress.org/support/wordpress-version/version-n-n-n/}}

3) Enter the text “Transferred to HelpHub” in the Summary box and click Save page.

NOTE: Once you save the page, viewing the page will be redirected to HelpHub page. If you want to modify the saved page, add `&action=edit` to the URL.  
e.g. `https://codex.wordpress.org/Version_5.0&action=edit`

3\. Mark the complete  
1) Change “In Progress” to “Done” at above Step 1-2).  
.

### [Version pages migration](#version-pages-migration)

Please migrate Version pages or Release Notes such as “Version X.Y.Z” page in Codex to HelpHub site.

1.  Open the “Release Notes” tab of Spreadsheet: [https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=1995801274](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=1995801274)
2.  Put your name in ‘Migrator’ column and change the Status to ‘In Process’.
3.  Login to [https://wordpress.org/support](https://wordpress.org/support) (if you can’t, refer below ‘Getting Account’)
4.  From Toolbar, select New > WordPress Version. Or, From Dashboard, select WordPress Versions > Add New.
5.  Cut & Paste the contents from Codex page into the new page.
6.  Fix the links to Codex page to WordPress.org/support. Refer other migrated page such as [https://wordpress.org/support/wordpress-version/version-4-9-9/](https://wordpress.org/support/wordpress-version/version-4-9-9/).
7.  Save as Draft (Do not Publish, yet)
8.  Change the Status of Spreadsheet to ‘Done’.

### [Codex contents Migration](#codex-contents-migration)

Please migrate Codex pages of user documents to wordpress.org/support

1.  Open the “Phase-2 Contents” tab of Spreadsheet: [https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=55427733](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=554277336)6
2.  Reserve a target page. Type your name in ‘Migrator’ and change Status to ‘In Process’.
3.  Go to [https://wordpress.org/support](https://wordpress.org/support) and click New > Article from Toolbar.
4.  Cut & Paste the contents from Codex page into the new article page.
    *   Except development information such as function usages. HelpHub is general user guide. Those information should be moved to Theme/Plugin Developer Handbook.
5.  Modify the contents.
    1.  Replace link of Codex page by HelpHub Page.  
        Ref. [Phase-1 Contents](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=835534324) and [Phase-2 Contents](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=554277336) for its pair
    2.  Download images via the Codex page, and add to Media Library of HelpHub site and replace the old contents.
    3.  See also below “Editing Hints”
6.  Preview it and compare with Codex Page.
7.  Save as Draft (Do not Publish, yet)
8.  Change the Status of Spreadsheet to ‘Done’.

### [Transferring Codex page to HelpHub](#transferring-codex-page-to-helphub)

As of Apr/2019, almost all migration were completed, and now we need show the warning text at the top of Codex page so that it can tell to visitor that this page was transferred to HelpHub. (e.g. Refer [this page](https://codex.wordpress.org/Contributing_to_WordPress))

Before actual adding the message, we need final review of contents and re-synchronize with the latest Codex contents.  
**Note: This task needs some experience on Codex and HelpHub.**

1\. Reserve the page for your process.  
1) From [this worksheet](https://docs.google.com/spreadsheets/d/1PeHj7pSFLcdMbIC41JJdzEkl12TJT3mwWyzQv2mi01U/edit#gid=835534324), search blank or Not Yet in “Transferred” column.  
2) Enter “In Progress”.

2\. Update HelpHub page by recent changes on Codex page.  
After the migration from Codex to HelpHub, someone might have modified the Codex page. Reflect those recent changes to HelpHub page.  
1) From codex page, click History on right side menu.  
2) Put the first marker on January 2017  
3) Click Compare selected revisions

![](https://make.wordpress.org/docs/files/2019/04/codex-history-1024x288.png)

4) Confirm the recent changes and enhance them to HelpHub.  
5) Read whole documents and fix the error if exists.

3\. Update Codex page so that include the warning message  
1) From codex page, click Edit on right side menu.  
2) Put following message below the language locator, and comment out the current Codex contents by “<–” and “–>”.

This page was moved to https://wordpress.org/support/article/< HelpHub page> except above language locator.

3) Click bottom Show preview and confirm your changes.  
4) Enter the text “Transferred to HelpHub” in the Summary box and click Save page.

4\. Release the page  
1) Change “In Progress” to “Done” at above Step 1-2).