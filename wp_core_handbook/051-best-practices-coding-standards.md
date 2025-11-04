---
title: WordPress Coding Standards
date: April 25, 2019
author: 
categories: 
url: https://make.wordpress.org/core/handbook/best-practices/coding-standards/
---

The purpose of the WordPress Coding Standards is to create a baseline for collaboration and review within various aspects of the WordPress open source project and community, from core code to themes to plugins.

The WordPress community developed the standards contained in this section of the handbook, and those standards are part of the best practices that developers and core contributors are recommended to follow.

[Why have coding standards?](#why-have-coding-standards)
--------------------------------------------------------

Coding standards help avoid common coding errors, improve the readability of code, and simplify modification. They ensure that files within the project appear as if they were created by a single person.

Following the standards means anyone will be able to understand a section of code and modify it, if needed, without regard to when it was written or by whom.

If you are planning to contribute to WordPress core, you need to familiarize yourself with these standards, as any code you submit will need to comply with them.

[Language-specific Standards](#language-specific-standards)
-----------------------------------------------------------

*   [CSS Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/css/)
*   [HTML Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/html/)
*   [JavaScript Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/javascript/)
*   [PHP Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/)

[Accessibility Standards](#accessibility-standards)
---------------------------------------------------

WordPress is committed to meeting the [Web Content Accessibility Guidelines (WCAG) at level AA](https://www.w3.org/TR/WCAG20/) for all new and updated code. We’ve provided a [quick guide to common accessibility issues](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/accessibility/) you should be aware of when creating patches or feature plug-ins.

[Where do the coding standards \_not\_ apply?](#where-do-the-coding-standards-_not_-apply)
------------------------------------------------------------------------------------------

Third-party libraries are not subject to these standards, even when integrated with the primary project. This includes instances like WordPress core, where multiple third-party libraries are incorporated into its codebase.