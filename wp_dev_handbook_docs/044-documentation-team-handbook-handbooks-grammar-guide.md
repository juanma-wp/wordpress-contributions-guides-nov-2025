---
title: Documentation Grammar Guide
date: April 24, 2019
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/documentation-team-handbook/handbooks-grammar-guide/
---

This is a draft version and we’re looking to improve it with community feedback.

### [General](#general)

Use American English spelling (_\-ize_ and _\-or_, not _\-ise_ and _-our_).

Write in the active voice whenever possible.

When referring to either the block editor or the classic editor, qualify the editor the first time (_block_ editor or _classic_ editor), then use _editor_ by itself after that.

With the verb _log in_, the correct preposition is _to_. Write _log in to_, not _log into_.

Write _homepage_ as one word (not _home page_).

### [Quotation Marks](#quotation-marks)

Do not use quotation marks for emphasis. Phrases in quotation marks may be interpreted by readers as irony or sarcasm.

Similarly, do not use quotation marks to indicate a command or something the user needs to type. The user may mistakenly assume the quotation marks are part of the command. Instead, use backticks (\`) to create an inline code block: `npm install react`.

Quotation marks should be used only for direct quotes and the titles of documents.

### [Capitalization](#capitalization)

Always capitalize WordPress (and remember to capitalize the _P_).

Capitalize _Classic Editor_ when referring to the plugin. Do not capitalize it otherwise (_classic editor_).

Capitalize the names of pages, links, plugins, and buttons (_the Save button, the Posts page_). 

Do not capitalize regular nouns, including WordPress elements: theme, plugin, page, block, user, administrator. 

Do not capitalize a word just to add emphasis to it. Instead, place it in **boldface** or _italics_.

### [Hyphenation](#hyphenation)

In general, don’t hyphenate compound adjectives unless it clears up ambiguity or makes the sentence more readable (_small-business owner_ but _open source software_). 

Do not hyphenate compounds with an adverb ending in _\-ly_ (_a nicely formatted document_)_._

Hyphenate the adjectives _back-end_ and _front-end_ (a _back-end developer_). Note that the nouns are _back end_ and _front end._

Do not hyphenate _login._ Note that _login_ is a noun or adjective; the verb is _log in_ (_Go to the login page to log in_).

### [Lists](#lists)

Use a **colon** (:) to introduce a list when it is preceded by a full sentence. Do not use a colon otherwise, even if you are introducing a bulleted list. It can interrupt the flow of reading.

**Correct**

The following basic options are supported by this plugin: `order`, `orderby`, and `column_id`.

This plugin supports the `order`, `orderby`, and `column_id` options.

**Incorrect**

The following basic options are supported by this plugin, `order`, `orderby`, and `column_id`.

The options this plugin supports are: `order`, `orderby`, and `column_id`.

### [Oxford Comma](#oxford-comma)

Use the Oxford comma, which means including the final comma before _and_ or _or_ in a list: _apples, oranges_**_, and_** _bananas_.

Rearrange ambiguous sentences, such as _My brother, the teacher, and Mr. Green came to dinner_. If the brother is also the teacher, this would be better as _Mr Green and my brother, the teacher, came to dinner._

### [Consistency](#consistency)

Above all, be consistent. In addition to applying the above grammar rules consistently, it’s important to use terms and vocabulary consistently so as not to confuse the reader. This also makes it much easier for the localization team to translate the document.

In the following example, we use the terms _data_, _ID_, _iteration_, and _query_ consistently.

**Correct**

To retrieve the data for all of the posts, don’t iterate through the array of IDs. This would result in a separate query being made for each ID on each iteration. It is much more efficient to make a single query that fetches all the data at once.

**Incorrect**

To retrieve the data for all of the posts, don’t iterate through the array of IDs. This would result in a separate SQL query being made for each post on each loop.  It is much more efficient to make one request to the database that fetches all the results at once.