---
title: Browser support
date: March 22, 2018
author: 
categories: 
url: https://make.wordpress.org/core/handbook/best-practices/browser-support/
---

Last 1 Android versions.  
Last 1 ChromeAndroid versions.  
Last 2 Chrome versions.  
Last 2 Firefox versions.  
Last 2 Safari versions.  
Last 2 iOS versions.  
Last 2 Edge versions.  
Last 2 Opera versions.  
Browsers with > 1% usage based on [can I use browser usage table](https://caniuse.com/usage-table)

The above configuration is also available in the [`@wordpress/browserslist-config`](https://github.com/WordPress/gutenberg/tree/master/packages/browserslist-config) module for [Browserslist](https://www.npmjs.com/package/browserslist) compatible tooling.

Changelog
---------

WordPress 5.8 – [Removed support for IE 11](https://make.wordpress.org/core/2021/04/22/ie-11-support-phase-out-plan/) ([#53077](https://core.trac.wordpress.org/ticket/53077)

#### [Remove IE11 from the list of supported browsers](https://core.trac.wordpress.org/ticket/53077)

Ticket #53077

IE11 will no longer be supported by WordPress starting in version 5.8.

The \`browserslist\` array needs to be updated to reflect this.

For context, see:  
\- https://make.wordpress.org/core/2021/03/04/discussion-dropping-support-for-ie11/  
\- https: \[…\]

##### Last 2 Comments

*   slackbot — 8:54 pm on February 16, 2022
    
    _This ticket was mentioned in [​Slack](https://make.wordpress.org/chat/) in #core by sergey. <a class="ext-link" href="https://wordpress.slack.com/archives/core/p1645044846283699 \[…\]_
    
*   slackbot — 3:44 pm on July 19, 2021
    
    _This ticket was mentioned in [​Slack](https://make.wordpress.org/chat/) in #core by jeffpaul. <a class="ext-link" href="https://wordpress.slack.com/archives/core/p16267094643708 \[…\]_
    

Owner: desrosjType: defect (bug)Status: closedComponent: Build/Test ToolsSeverity: normalUpdated: 4 years ago

)

WordPress 4.8 – [Removed support for IE 8, 9, and 10](https://make.wordpress.org/core/2017/04/23/target-browser-coverage/)

WordPress 4.4 – Removed support for IE 7 ([#18199](https://core.trac.wordpress.org/ticket/18199)

#### [Deprecate IE7 in the Admin](https://core.trac.wordpress.org/ticket/18199)

Ticket #18199

markjaquith:  
\> Everyone hates IE7. It’s insecure. Let’s make it go away. Also, dropping IE6 didn’t give us much beyond goodwill, because most of the hacks we needed for IE6, we also need for IE7. So we could actually clean up our CSS a bit \[…\]

##### Last 2 Comments

*   SergeyBiryukov — 6:22 pm on October 12, 2015
    
    From a [​recent discussion](https://wordpress.slack.com/archives/core/p1443209122004342), for reference:
    
    > desrosj: Is there a list of browsers/ \[…\]
    
*   aaroncampbell — 3:54 pm on October 12, 2015
    
    *   **keywords** _needs-patch_ removed
    *   **status** changed from _new_ to _closed_
    \[…\]
    

Reporter: nacinType: enhancementStatus: closedComponent: AdministrationSeverity: normalUpdated: 10 years ago

)

WordPress 3.2 – [Removed support for IE 6](https://make.wordpress.org/core/2011/03/18/wordpress-3-2-the-plan-faster-lighter/)