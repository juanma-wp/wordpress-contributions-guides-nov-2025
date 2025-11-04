---
title: Reporting an issue
date: January 6, 2020
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/workflows/reporting-an-issue/
---

Documentation team is in charge of several different projects. These projects use different tools for contributing and, therefore, reporting an issue has different workflow depending on the project.

This page is mainly for one-time and first time contributors. So, if you are just starting contributing to the Documentation team or you just want to report an issue you came across, this page should provide an easy-to-follow step-by step guide on how to do so.

The easiest way to report any kind of documentation issue is to go to [#docs](https://wordpress.slack.com/messages/docs/) Slack channel and just post. If you know which [Docs project](https://make.wordpress.org/docs/handbook/get-involved/current-docs-projects/) is this issue in, you can even ping the person responsible for it. See all our reps on our [team page](https://make.wordpress.org/docs/handbook/the-team/).

[HelpHub](#helphub)
-------------------

HelpHub is a working title for end user documentation located at [https://wordpress.org/documentation/](https://wordpress.org/documentation/). If you found an issue in an article there, here’s how to report it.

### [Content issue](#content-issue)

If you found a typo, outdated or incorrect information or screenshots, broken links or images, or any content related issue, please follow these steps:

*   Go to GitHub repo and check among existing issues if anyone has already started discussion – [https://github.com/WordPress/Documentation-Issue-Tracker/issues](https://github.com/WordPress/Documentation-Issue-Tracker/issues).
*   If not, open new issue. Click [New issue](https://github.com/WordPress/Documentation-Issue-Tracker/issues/new/choose) and select appropriate template such as
    *   Fix Doc Issue Report … for reporting a new issue
    *   New Doc Request … for requesting a new page

### [Development issue](#development-issue)

You found an article with broken layout or any similar unexpected behavior in rendering the content.

HelpHub development is maintained by [Milana Cap](https://profiles.wordpress.org/milana_cap/).

Reporting a development issue:

*   Go to meta Trac and check among existing HelpHub tickets if anyone has already reported the issue – [https://meta.trac.wordpress.org/query?status=!closed&component=HelpHub](https://meta.trac.wordpress.org/query?status=!closed&component=HelpHub)
*   If not, select “New Ticket”
*   Select “HelpHub” component from the dropdown
*   Make sure that “Summary” field does summarize the issue
*   In the “Description” field describe the problem with as much detail as possible (links and screenshots are welcome). If possible, description should follow template:
    *   Expected behavior
    *   Actual behavior

[DevHub](#devhub)
-----------------

DevHub is a working title for all developer’s documentation, a set of Handbooks located at [https://developer.wordpress.org/](https://developer.wordpress.org/). Not all projects (Handbooks) here are under Docsumentation’s team responsibility. REST API, WP-Cli and WordPress Coding Standards Handbooks are maintained by their respective teams. 

Themes Handbook is a shared responsibility between Documentation and Theme Review teams. Everything else: Code Reference, Block Editor, Common APIs and Plugins are maintained by the Documentation team. 

### [Code Reference](#code-reference)

Code reference is divided into 3 parts:

*   [Inline docs](#inline-docs)
*   [More Information](#more-information)
*   [User Notes](#user-notes)

#### [Inline Docs](#inline-docs)

Because of the nature of creation, Inline Docs is maintained by the Core team for a while now but it is still documentation. Read more about Inline docs in [Core team’s Handbook](https://make.wordpress.org/docs/handbook/code-reference/inline-documentation/).

Report the issue:

*   Go to Core Trac and check among existing tickets if anyone has already reported the issue – [https://core.trac.wordpress.org/query?status=!closed&focuses=~docs](https://core.trac.wordpress.org/query?status=!closed&focuses=~docs)
*   If not, open new ticket with focus docs
*   Select appropriate Component from the dropdown
*   If you have never open Trac ticket before, here’s a detailed guide – [https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/](https://make.wordpress.org/core/handbook/tutorials/trac/opening-a-ticket/)
*   Make sure that “Summary” field does summarize the issue
*   In “Description” field describe problem with as much detail as possible (links and screenshots are welcome)

#### [More Information](#more-information)

This section appears right between “Related” and “User Contributed Notes” sections. Its purpose is to further explain the code and its usage. It is not meant for code examples. This is what User notes are for.

The More Information section is maintained by [Julio Potier](https://profiles.wordpress.org/juliobox/).

For now the only way to report the issue is to post it in [#docs](https://wordpress.slack.com/messages/docs/) slack channel.

#### [User Notes](#user-notes)

User Notes are code snippets and examples of how to use the function, class, method or hook in question. They work exactly the same as comments. 

Post your example as you would post a comment. It will be held under moderation until it’s reviewed by Docs team. For proper PHP syntax highlighting use shortcode to wrap your code example:

```
[php][/php]
```

To report an issue with any of the already published notes, use the “Add feedback to this note” link. It is located right below the example and behaves as a reply to the comment. Just as the note itself, it will also be held for moderation. 

Once you reported an issue or posted your code example, please be patient. It is uncertain how much time we’ll need to review it as it depends on the current queue and how many Docs team members are available to work on it at that moment. You are always welcome to join the team and help with User Notes.

User Notes are maintained by [Jb Audras](https://profiles.wordpress.org/audrasjb/) and [Leo Germani](https://profiles.wordpress.org/leogermani/).

### [Block Editor Developer’s Handbook](#block-editor-developers-handbook)

Documentation for developing on top or with block editor lives on [GitHub](https://github.com/WordPress/gutenberg/tree/master/docs) from where it is parsed to our [Block Editor Handbook](https://developer.wordpress.org/block-editor/).

For contributing to Block Editor documentation, please refer to [this document](https://github.com/WordPress/gutenberg/blob/master/docs/contributors/document.md).

Report the issue with Block Editor’s documentation: 

*   Make sure the issue is not already open by checking [all the Docs issues](https://github.com/WordPress/gutenberg/issues?utf8=%E2%9C%93&q=is%3Aopen+is%3Aissue+label%3A%22%5BType%5D+Documentation%22+) on GitHub,
*   If no one reported it, open a [new issue](https://github.com/WordPress/gutenberg/issues/new/choose).

Documentation for developing with and on top of Block Editor is maintained by [Paul Barthmaier](https://profiles.wordpress.org/pbarthmaier/).

### [Common APIs Handbook](#common-apis-handbook)

The Handbook for [Common APIs](https://developer.wordpress.org/apis/) is maintained by [Leo Germani](https://profiles.wordpress.org/leogermani/). Reporting issues found in this Handbook is done in [#docs](https://wordpress.slack.com/messages/docs/) Slack channel.

### [Plugin Developer’s Handbook](#plugin-developers-handbook)

The Handbook for [developing a plugin](https://developer.wordpress.org/plugins/) is maintained by [theMikeD](https://profiles.wordpress.org/themiked/). Reporting issues found in this Handbook is done in [#docs](https://wordpress.slack.com/messages/docs/) Slack channel.

### [Theme Developer’s Handbook](#theme-developers-handbook)

The Handbook for developing a theme is shared responsibility between Documentation and Theme Review team. While we are happy to fix any issues found in this Handbook, we would recommend reporting issues to its Rep, [Ana Alfieri](https://profiles.wordpress.org/acalfieri/) from Theme Review team, directly in [#themereview](https://wordpress.slack.com/archives/C02RP4Y3K) Slack channel. 

[Documentation Team Handbook](#documentation-team-handbook)
-----------------------------------------------------------

This Handbook is maintained by [Akira Tachibana](https://profiles.wordpress.org/atachibana/) and [Milana Cap](https://profiles.wordpress.org/milana_cap/). If you have found any issues here please report it in [#docs](https://wordpress.slack.com/messages/docs/) Slack channel.