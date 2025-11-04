---
title: Examples Reviewing
date: July 16, 2015
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/code-reference/editing-articles/reviewing/
---

Note: This project was completed. Thank you for your contribution.

As outlined in the [Codex Migration](https://make.wordpress.org/docs/handbook/developer-resources/code-reference/codex-migration/) page, one of our primary contributor efforts as of 2015 is moving examples from Codex articles to their corresponding Code Reference articles. This effort is already in full-swing, and is a great way to contribute in small ways for big results.

We’re tracking migration of examples from function references in the Codex to the Code Reference in this spreadsheet:  
https://docs.google.com/spreadsheets/d/15hpEbbnuWJZ0DJafyCeG3CFRMtSxX1gY-RObrrjzzdw/edit#gid=0

In this sheet there are 1,110 functions listed, which constitute all of the functions that currently have a published reference page in the Codex right now. Not all of these pages have examples, but many of the ones that do are notated by the number of examples in the **\# Examples** column of the spreadsheet (counting examples is a work in progress).

### [Prerequisites](#prerequisites)

*   Your WordPress.org account must have been added as an editor role or above on the Developer Reference. Need to be added? Go to the [#docs](https://wordpress.slack.com/messages/docs/) channel on [slack](https://make.wordpress.org/chat/) and ask someone to add you.
*   You should have a working knowledge of PHP, HTML, and CSS, and have a good handle on core [coding](https://make.wordpress.org/core/handbook/best-practices/coding-standards/) and [inline documentation](https://make.wordpress.org/core/handbook/best-practices/inline-documentation-standards/) standards.

### [Getting Started](#getting-started)

#### [Reviewing Examples](#reviewing-examples)

1.  In the developer hub comments moderation screen, navigate to last page of the Pending comments view (start with the oldest submissions).
2.  On DevHub, code examples are submitted as comments and associated with reference articles for functions, hooks, classes, or methods. You can see which reference the example belongs to in the right column of the comments screen.
3.  In the spreadsheet, locate the function you’re currently reviewing examples for (the “Reviewer” column should be empty).
4.  Add your username to the **Reviewer** column to show that you’ve claimed that function’s examples for review.
5.  It’s best to only claim and work on a single function at a time, this ensures that effort doesn’t accidentally get wasted or overlap with another contributor.
6.  Once you’ve reviewed all total examples for a function, change the status to “Reviewed” in the spreadsheet. If you could only locate some of the supposed total number of examples, please do not change the status, but instead notate in the notes column how many examples have been reviewed.
7.  Lather, rinse, repeat.

### [When Reviewing Examples](#when-reviewing-examples)

1.  Examples should generally have a title of some sort just to prime people on what it demonstrates. Should be wrapped in `<strong>` tags.
2.  Code blocks should be wrapped in `<code></code>`, `[[php] [/php]]`, or `[[js] [/js]]` blocks. Opening and closing PHP tags are generally unnecessary unless you’re jumping between code and markup.
3.  Callback functions should be prefixed with `wpdocs_`
4.  Callback functions should follow core coding and inline documentation standards, and should have properly-formatted DocBlocks.
5.  Should use proper escaping, sanitization, and localization functions where needed. For localization functions, use a textdomain of ‘textdomain’.
6.  The code should work unless pseudo-code.