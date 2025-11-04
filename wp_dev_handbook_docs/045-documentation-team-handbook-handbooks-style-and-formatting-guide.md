---
title: Handbooks & HelpHub Style and Formatting Guide
date: February 7, 2013
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/documentation-team-handbook/handbooks-style-and-formatting-guide/
---

In order to maintain consistency across the handbooks, please follow this style guide. The aim of the guide is to help you to create documents that are readable and useful to all readers. Advanced users should be able to scan the document and pick out what they need. But you still need to include the detail to help novice users.

[Style](#style)
---------------

Write in an **informal but knowledgeable manner**. The reader should feel that this is a friend explaining something clearly to them.

Explain what you need to in **as few words as possible**.

Always write in the **second person**, i.e. you, not we, addressing the reader as though they were sitting beside you.

**Correct**

_Log in to your WordPress Admin Screens._

**Incorrect**

_Next, we need to log in to WordPress._

[Content](#content)
-------------------

Stick to **one topic per article**. Don’t diverge into other topics, but link to them where relevant.

**Example**

_This article will show you how to get started contributing to WordPress via Github. Before you get started, you’ll need to have a local server. You can learn how to do it in [this article on installing WordPress locally](https://make.wordpress.org/core/handbook/tutorials-and-guides/installing-wordpress-locally/)._

When writing articles, **stick to one major point per paragraph**. This will help to maintain the clarity of the document. A good idea is to plan out what you’re going to write beforehand by writing down each point you want to make.

[Formatting](#formatting)
-------------------------

*   Use **bold** to make important points stand out or to indicate instructions: e.g. **Navigate to Pages > Add New**
*   If you want to alert the user to something, use the following short codes:  
    `[ info ]`  
    
    This is an informational message and uses the “info” short code.
    
      
    `[ tip ]`  
    
    Use the “tip” short code to highlight tips.
    
      
    `[ alert ]`  
    
    The “alert” short code is for alerting readers to important messages.
    
      
    `[ warning ]`  
    
    When something is particularly precarious, use the “warning” short code.
    
      
    `[ tutorial ]`  
    
    Tutorial lessons should use this shortcode, but must continue on from previous tutorials.
    
*   Use ordered and unordered **lists**
*   Use **heading tags** in the correct order from h2 – h6
*   When referring to **menu items**, use the format Pages > Add New
*   Use **Blocks**.  
    WordPress v5.0 will introduce the Block Editor (code name Gutenberg). Contents are broken down into individual blocks (image, lists, paragraph, headings etc).  If you are migrating or editing articles that are using Classic Block, feel free to convert them into actual separate blocks.

How to deal with file names:

\[preserved\_text 5ce7c31ec4642f252291d006cfc6097c /\]

To insert code examples, wrap the code in the correct shortcode. For example:

*   `_[__php__]__[__/php__]_`
*   `_[__html__]__[__/html__]_`

Functions, hooks, methods, classes, and variables should all be wrapped in the <code> HTML tag and properly linked to the code reference. Links should start _inside_ the code tag.

When a page is complete, there should be no links to the Codex, unless the document does not exist on developer.wordpress.org.

[Layout](#layout)
-----------------

### [Images](#images)

Images should be full size. Don’t include thumbnails that readers have to click on to see unless absolutely necessary. To take screenshots that look great, resize your browser window. By resizing down, you can take screenshots of the specific areas of the screen that you are referring to.

### [Articles](#articles)

**Avoid huge chunks of text.** Make your article paragraphs short and to the point. Use headings where relevant to make it easy for people to scan.

### [Tutorials](#tutorials)

Tutorials should always be **written in a clear, logical fashion**. You should do the following:

*   Have an **introductory paragraph** that tells the reader to what they will do.
*   Include a list of anything that they will **need**.
*   Each step should have **one clear task**.
*   Each step should have a **header that states concisely what the task is**.
*   Each step header should be **numbered** and wrapped in the **appropriate heading** tag.
*   Where relevant, include **screenshots**.

The following example demonstrates a simple tutorial for downloading BuddyPress and uploading to WordPress using FTP.

> **1\. Download BuddyPress & Unzip**
> 
> Navigate to the WordPress plugin repository and **download BuddyPress**. Unzip to a folder that you can easily find on your computer.
> 
> ![A screenshot of the BuddyPress download button](https://make.wordpress.org/docs/files/2013/02/bp1.jpg)
> 
> **2\. Upload via SFTP to wp-content/plugins/**
> 
> **Open up your favorite SFTP program** (FileZilla, for example). Input your SFTP login details. If you do not have these, you will be able to get them from your web host.
> 
> Once you are logged in to your server, **navigate to wp-content/plugins/**. On your local server, locate the unzipped BuddyPress folder. Drag and drop the folder to your remote website.
> 
> ![A screenshot of Filezilla. An arrow points from the files on the local server to the remote server](https://make.wordpress.org/docs/files/2013/02/bp2.jpg)
> 
> **3\. Activate the Plugin**
> 
> Log in to WordPress. **Navigate to Plugins**. Locate the BuddyPress plugin and **click the activate link**.
> 
> ![A screenshot of the activate plugin button. Activate is highlighted](https://make.wordpress.org/docs/files/2013/02/bp3.jpg)

[Accessibility](#accessibility)
-------------------------------

### [Images](#images-2)

Try to keep in mind that not everyone will be able to see your screenshots or other explanatory images. So please do not rely on them too heavily.

#### [Gifs](#gifs)

Autoplay of movements are not accessible and it should be possible for users to control animations, videos, sound and so on. 

Following solutions are suggested:

1.  Use video instead of gifs. Videos can be controlled by users with play and stop, including going back and forth inside the videos.
2.  If videos are not possible and it has to be a gif (for example because the content needs to be make again), provide a thumbnail instead the gif with a play icon and let the gif play, when clicking the play button (and make it also possible to stop it). So it would be possible to consume the gif, but also to read the post calmly with no distraction.

### [Links](#links)

When creating link text, be aware that links can be rendered out of context in some user agents (e.g. the Links List in the [JAWS screenreader](http://en.wikipedia.org/wiki/JAWS_%28screen_reader%29)). So avoid generic text like “here” or “this”, and ensure that link text describes the resource that you are pointing to. On pages that contain multiple links, ensure that each link text is unique – unless you are linking to the same resource in more than once place.

### [Abbreviations](#abbreviations)

Avoid the use of jargon, abbreviations and acronyms whenever possible. If you really do need to use an abbreviation, use the full, expanded version first, followed by the abbreviation in parentheses (brackets). Alternatively, use correct abbreviation markup such as:

> `<abbr title="World Wide Web Consortium">W3C</abbr>`