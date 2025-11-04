---
title: Examples Migrating From Codex
date: July 16, 2015
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/code-reference/editing-articles/migrating-from-codex/
---

Note: This project was completed. Thank you for your contribution.

As outlined in the [Codex Migration](https://make.wordpress.org/docs/handbook/developer-resources/code-reference/codex-migration/) page, one of our primary contributor efforts as of 2015 is moving examples from Codex articles to their corresponding Code Reference articles. This effort is already in full-swing, and is a great way to contribute in small ways for big results.

To begin, we’re tracking migration of examples from function references in the Codex to the Code Reference in this spreadsheet:  
[https://docs.google.com/spreadsheets/d/15hpEbbnuWJZ0DJafyCeG3CFRMtSxX1gY-RObrrjzzdw/edit#gid=1679372392](https://docs.google.com/spreadsheets/d/15hpEbbnuWJZ0DJafyCeG3CFRMtSxX1gY-RObrrjzzdw/edit#gid=1679372392)

**Take note, in the above spreadsheet, there are multiple tabs (Functions, Classes, Hooks, Status), which you can select at the bottom.**

In the Functions tab, there are 1,110 functions listed, which constitute all of the functions that currently have a published reference page in the Codex right now. Not all of these pages have examples, but most do.

You might notice that the **\# Examples** column lists “Unknown” for a lot of references — counting examples is a work in progress. Examples don’t need to be pre-counted in order for a reference status to proceed, counting examples was previously used to assist in determining which references could be skipped for migrating examples.

So you want to migrate examples? There are a few simple steps to get started:

### [Prerequisites](#prerequisites)

*   You must have a WordPress.org account. Don’t have one? [Create an account](https://wordpress.org/support/register.php).
*   Some understanding of PHP and HTML is useful but not required.

### [Getting Started](#getting-started)

#### [Claiming a Function](#claiming-a-function)

1.  In the spreadsheet, locate a function not currently claimed by a contributor (the **Owner** column is empty).
2.  Add your name to the **Owner** column to show that you’ve claimed that function.
3.  It’s best to only claim and work on a single function at a time, this ensures that effort doesn’t accidentally get wasted or overlap with another contributor.

#### [Migrating Examples](#migrating-examples)

1.  Visit the Codex article for that function by navigating to the link in the **Codex** column for the function.
2.  Grok the page to locate any examples. Examples often have corresponding description text leading up to the example code (most have a title, short description and then code, you want all three), so it’s helpful to look for that text when trying to decide how many examples there are.
3.  Copy the example text and code to your clipboard either by right-clicking and selecting “Copy” or with your keyboard using Ctrl + C (Windows) or Cmd + C (Mac).
4.  Back in the spreadsheet, visit the the Code Reference article by navigating to the link in the **Reference** column for the function.
5.  At the bottom of the reference article in the Code Reference, look for a section called “User Contributed Notes”. There will be a link in that section, “Have a note to contribute?”. Click that link.
6.  Log in with your WordPress.org credentials if you haven’t already.
7.  A form for submitting a user contributed note should appear on your screen. Paste in the code example and text you copied from the Codex. If you feel comfortable, feel free to reformat the example text to provide proper emphasis. For the code example, it’s helpful to the reviewers to substitute any opening and closing PHP tags with
    
    1
    
    `&amp;amp;amp;amp;amp;amp;amp;amp;amp;lt;/code&amp;amp;amp;amp;amp;amp;amp;amp;amp;gt;` `and` `&amp;amp;amp;amp;amp;amp;amp;amp;amp;lt;code&amp;amp;amp;amp;amp;amp;amp;amp;amp;gt;`
    
    shortcodes – these are used on the front-end view for code syntax highlighting.
    
8.  When everything has been formatted, click the “Add Note” button.
9.  If there are multiple examples in the Codex article, repeat steps 3-8 until all examples have been submitted.

#### [Finishing Up](#finishing-up)

*   Once you’ve submitted all of the Codex examples, make sure to update the **Status** column of the spreadsheet marking the function as “Ready for Review”, then update the **\# Examples** column with the number of submitted examples (this is so reviewers can cross-reference completeness). You may also jot down any notes in the **Notes** column about notable other stuff that should come over later as an “Explanation” section. A reviewer will follow along later to validate and publish the example(s) you migrated.
*   All of the submitted examples are vetted before they’re published. Fixing the examples when submitted is a bonus, because it’s less work for the reviewers to do.
*   Congratulations! If you followed all of the steps above, you will have successfully migrated the examples for a function. Let’s migrate another one!