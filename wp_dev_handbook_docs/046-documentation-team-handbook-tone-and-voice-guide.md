---
title: Tone and Voice Guide
date: January 16, 2019
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/documentation-team-handbook/tone-and-voice-guide/
---

This is a draft version and we’re looking to improve it with community feedback.

**Tone** refers to the mood or attitude of a specific piece of writing. For example, your tone in a personal email might be more informal than one you send at work. **Voice** reflects overarching characteristics that shouldn’t change much between documents. The voice of WordPress and its community is _friendly but professional_.

This guide is mainly for English-language documentation. If you are not writing in English, please also refer to the [guidelines for your locale](https://make.wordpress.org/polyglots/handbook/tools/glotpress-translate-wordpress-org/list-of-glossaries-per-locale/).

[Voice](#voice)
---------------

**Be friendly**: In English, use contractions (_I’m_, _don’t_) and write in the second person. Use language that is accessible to your target audience. Avoid jargon.

**Be professional**: While writing in a friendly, accessible manner, be sure not to overdo it. Don’t use too many exclamation marks, and don’t use slang or web shorthand. Write concisely and use the active voice whenever possible.

In general, remember that documentation is translated into many languages. It’s important to write in consistent standard English and avoid cultural references and idioms. For example, users outside the US may not know what the Super Bowl is, and expressions like “dot your I’s and cross your T’s” are difficult to translate.

[Tone](#tone)
-------------

### [User Documentation](#user-documentation)

Users search the documentation for the answer to a question. Maintain a friendly, informal tone, but focus on being clear, concise, and very precise. Get to the point as quickly as possible. Explain technical terms, but be careful not to be condescending. To ensure clarity, start by briefly specifying the context of the current topic.

Keep in mind that many users are not native English speakers. Avoid long narrative paragraphs. Keep paragraphs short and focused, with consistent vocabulary and phrasing that is easy for all your readers to understand.

**Examples describing a functional component of the WordPress admin:**

Good example:

On the left side of the screen is the main navigation menu listing the administrative functions you can perform.

Bad example:

If you peek over at the left side, you’ll see a menu called main navigation, which is the main menu. This menu is a list of functions you as the administrator can do from the administration screen.

**Examples describing a technical implementation:**

Good example:

A cookie is a small piece of data used to remember information about you. When you visit a website, it sends a cookie to your browser, and your browser stores the cookie in a small file. The next time you visit the website, it uses that cookie to get information such as your preferred language.

Bad example:

When you visit a website, you probably want the website to remember some information about you so you don’t have to give it the information again. Websites can send your browser this kind of information so they remember you later. This information is called a cookie. I know what you’re thinking, a cookie is something you eat, right? Well, a computer cookie is different. It’s a tiny bit of data used by the website so that when you visit the website again, it gleans things from the cookie like what language you speak.

### [Developer Documentation](#developer-documentation)

Developers are often searching the documentation for an answer to a specific technical question. Your tone here should be direct and very precise. Use the same tone you would for user documentation, but you can assume a higher level of technical knowledge in your readers. In tutorials, it’s helpful to specify what technical knowledge is being assumed.

For a code reference, be as direct as possible. A conversational tone is less appropriate here.

Good example:

To retrieve an option, use the get\_option() function. It accepts two parameters: the option name and a default value to return if the option does not exist.

Bad example:

Sometimes you need to get a setting. This is easy if you use the get\_option() function and pass in two parameters (a parameter is a value passed to a function). One parameter is the name and the other parameter is a default value.

Good example:

#each: The #each method calls the provided function once for each element in the array. It returns the original array.

Bad example:

Next, let’s talk about the each method. This method calls a function for each element and returns an array.