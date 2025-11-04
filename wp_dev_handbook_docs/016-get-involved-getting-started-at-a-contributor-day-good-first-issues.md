---
title: Good first issues
date: October 30, 2023
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/get-involved/getting-started-at-a-contributor-day/good-first-issues/
---

If this is your first time contributing to the Documentation team we have various kinds of [good first issues](https://github.com/WordPress/Documentation-Issue-Tracker/labels/good%20first%20issue) that can help you get started give you idea of what contributing to WordPress documentation might look like.

[Updating screenshots](#updating-screenshots)
---------------------------------------------

Most of articles have accompanying screenshots, which have to be updated every time a new WordPress version change something in that particular part of user interface. To create new screenshots, you’ll need a fresh install of the latest WordPress version. The easiest ways of doing this is using either [WordPress Playground](https://playground.wordpress.net/) or [InstaWP](https://app.instawp.io/onboard) service.

It is important that WordPress is in English and no additional plugins, or custom themes are used – only the default theme and settings. New screenshots should cover the same area of the screen as the old screenshots do so that change is clearly visible.

Updating screenshots for the WordPress end-user documentation.

[Updating videos](#updating-videos)
-----------------------------------

Same as with screenshots, many articles have videos or GIF images, showcasing the described feature. These should be updated if they are showing the feature or screen area that has changed in the most recent WordPress version.

[Checking headings capitalization](#checking-headings-capitalization)
---------------------------------------------------------------------

As a part of our official [documentation Style guide](https://make.wordpress.org/docs/style-guide/language-grammar/capitalization/#capitalization-in-titles-and-headings), all headings must be in a sentence case. To check these, open the article and take a look at all the headings. Copy the ones that don’t comply and paste them in the GitHub issue you’re working on.

[Checking image ALT attributes](#checking-image-alt-attributes)
---------------------------------------------------------------

Every image that appears in WordPress documentation has to have an [ALT attribute](https://make.wordpress.org/docs/style-guide/formatting/media/#alt-text). This is a part of our [Accessibility guidelines](https://make.wordpress.org/docs/style-guide/general-guidelines/accessibility/#media-accessibility). In the source code it can be found as `alt=""`:

```
<img ... alt="" ... />
```

If there’s no text inside the quotes, then the ALT attribute is considered empty and this is something we want to avoid. It should look something like this:

```
<img ... alt="This is the ALT attribute." ... />
```

In order to see the source code, you should right click on the image and select “Inspect”. It will open the source code and highlight the selected image tag.

Check the image ALT attributes by viewing the source code.