---
title: Updating and creating new screenshots
date: March 7, 2024
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/get-involved/onboarding-sessions/updating-and-creating-new-screenshots/
---

**Table of contents**:

*   What do I need?
*   Reviewing the screenshots
*   Updating existing screenshots
*   Creating new screenshots
*   Screenshots versus videos (GIFs)

**What do I need?**

*   **Fresh WordPress install**, the default theme and no additional plugins – [WordPress Playground](https://playground.wordpress.net/), [InstaWP](https://instawp.com/)
*   **Screenshot tool** with annotation abilities – [Awesome Screen recorder and screenshot](https://www.awesomescreenshot.com/) ([Microsoft app](https://apps.microsoft.com/detail/9pbc89bq10zq?hl=en-US&gl=US), [Mac App Store](https://apps.apple.com/us/app/awesome-screenshot-recorder/id1531282066?mt=12), [Chrome extention](https://chromewebstore.google.com/detail/awesome-screen-recorder-s/nlipoenfbbikpbjkfpfillcgkoblgpmj?pli=1)), [Nimbus screenshot](https://nimbusweb.me/screenshot/) (has extensions for all major browsers)

**Reviewing the screenshots**

When the new WordPress version is released, we want to make sure all the screenshots in the documentation match what’s in the latest WordPress dashboard. Compare screenshots in the documentation article to the dashboard in the fresh WordPress install with the latest version.

Any user-facing change means we need a new screenshot:

*   **things are added** – new buttons, text, controls, settings, etc.
*   **things are removed** – things visible in screenshots no longer exist in the dashboard.
*   **things are moved** – things visible in screenshots no longer exist in that place.
*   **things look differently** – things in screenshots are in the same place in the dashboard, but they look differently (e.g., the editor background is changed due to a different default theme; icons in the toolbar are changed, etc.)

**Updating existing screenshots**

When creating a new screenshot, it’s important to cover the same area as the existing screenshot or, if things have moved to a different place, cover the same interface.

Some screenshots are annotated. It is preferred to use the same annotation for new screenshots as well.

All screenshots should be uploaded in the comment section of the appropriate GitHub issue, after which someone will review them and update the article. Here are some [examples of completed issues](https://github.com/WordPress/Documentation-Issue-Tracker/issues?q=label%3A%22needs+screenshots%22+is%3Aclosed+label%3A%22good+first+issue%22+label%3A%22user+documentation+%28HelpHub%29%22) for updating screenshots.

**Creating new screenshots**

Sometimes, a feature is new, and there is no existing screenshot. Depending on the feature, showcasing it might need more than one screenshot.

When creating a new screenshot, ensure you capture enough of the surroundings to make it easier for end-users to locate it. Use annotations if necessary. Follow the order of actions in order to use the feature successfully.

All screenshots should be uploaded in the comment section of the appropriate GitHub issue, after which someone will review them and update the article.

**Screenshots versus videos (GIFs)**

If the feature is complex and requires a significant number of screenshots, consider recording a video demoing its usage. This video can be converted to GIF and accompanied by one or two screenshots if necessary.

Upload the video (GIF) in the comment section of the appropriate GitHub issue, after which someone will review it and update the article.