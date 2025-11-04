---
title: Documentation process during a major version release day
date: April 23, 2025
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/workflows/documentation-process-during-a-major-version-release/
---

Several documents need to be updated as part of the release process. While the articles can be drafted in advance, they will only be published after the official announcement has been made.

Refer to the core handbook for the complete overview of the [major version release process](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#release-day). All the items that need updating can be found in the ‘[Tell the World](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#tell-the-world)‘  and ‘[Post Release](https://make.wordpress.org/core/handbook/about/release-cycle/releasing-major-versions/#post-release)’ sections.

These tasks are the responsibility of the Release Documentation Lead(s). Assistance can be requested from the documentation team in the [Slack #docs channel](https://wordpress.slack.com/archives/C02RP4WU5).

[Tell the World](#tell-the-world)
---------------------------------

### [HelpHub Release](#helphub-release) 

The first item is the HelpHub Release or Version page under [WP Versions](https://wordpress.org/documentation/article/wordpress-versions/). 

A new version page is created by duplicating the previous version article—for example, [Version 6.8](https://wordpress.org/documentation/wordpress-version/version-6-8/). Specific items will need to be updated, and the release team will provide the necessary information. Refer to the notes on each item for guidance.

*   Add the name of the jazzer. The name will be given to the release lead on release-day.
*   Update the link to the official announcement.

On April 15, 2025, WordPress 6.8 “Cecil” was released to the public. For more information on this release, read the [WordPress 6.8 announcement](https://wordpress.org/news/2025/04/cecil).

*   Update the **db\_version** and the **Trac revision**. Ask in the Slack release team channel for the numbers.

For Version 6.8, the database version (**db\_version** in **wp\_options**) was `58975` and Trac revision was `60168`.

*   Update the link to the full list of tickets included in the release.

A [full list of tickets included in 6.8](https://core.trac.wordpress.org/milestone/6.8) can be found on [Trac](https://core.trac.wordpress.org/).

*   The **Installation/Update Information** doesn’t update.
*   The performance improvements link can be updated as soon as the post is live, usually the next day.
*   On the **Learn more about WordPress 6.x** section, update the links to the field guide and the feature showcase. Change the release number at the end of the sentence.

Explore the [WordPress 6.8 Field Guide](https://make.wordpress.org/core/2025/03/28/wordpress-6-8-field-guide/). Learn about the changes in this release with detailed developer notes to help you build with WordPress.Read the WordPress 6.8 Release Notes for information on installation, enhancements, fixed issues, release contributors, learning resources, and the list of file changes. Review the list of [performance improvements](https://make.wordpress.org/core/2025/04/16/wordpress-6-8-performance-improvements/).Visit the [feature showcase](https://wordpress.org/download/releases/6-8/) for a full overview of all the new features and enhancements in WordPress 6.8.

*   Add the **release squad** from the [WordPress 6.x Development Cycle](https://make.wordpress.org/core/6-8/) post and update the **release version number**. 

Every release comes to you from a dedicated team of enthusiastic contributors who help keep things on track and moving smoothly. The team that has led 6.8 is a cross-functional group of contributors who are always ready to champion ideas, remove blockers, and resolve issues.

*   Update the **changelog**. This is done the day of the release and the Triage Lead or the Tech Lead usually has the list of files that go in the changelog. These can be added at a later date.

**Updated packages**  
`@wordpress/a11y – 4.19.1  
@wordpress/annotations – 3.19.1  
@wordpress/api-fetch – 7.19.1  
@wordpress/autop – 4.19.1  
@wordpress/blob – 4.19.1` .. 

**List of files revised**  
Modified files:  
`license.txt  
readme.html  
wp-admin/about.php  
wp-admin/admin-functions.php ..`

### [WordPress Versions](#wordpress-versions)

The next document to update is the [WordPress Versions](https://wordpress.org/documentation/article/wordpress-versions/) page. For a major version, a new table block is added with the same columns and add the information:

*   Version 6.x links to the [minisite](https://wordpress.org/download/releases/6-8/).
*   Release date – add the date of the release.
*   Musician – enter the name given to the release, not the jazzer full name.
*   Changelog links to the HelpHub Release/Version release page.
*   Announcement links to the [formal releas](https://wordpress.org/news/2025/04/cecil/)e announcement.
*   DB version – enter the **db\_version** added in the HelpHub Release/Version release page.
*   Update the changelog at the bottom.

[![](https://make.wordpress.org/docs/files/2025/04/WP-versions_add-new-release-info-1024x383.png)](https://make.wordpress.org/docs/files/2025/04/WP-versions_add-new-release-info.png)

Example of what to add on a new WordPress release information block

[![](https://make.wordpress.org/docs/files/2025/04/WP-versions-changelog.png)](https://make.wordpress.org/docs/files/2025/04/WP-versions-changelog.png)

Example of changelog to update

*   The **Planned Versions** section is also updated with any information available.

[![](https://make.wordpress.org/docs/files/2025/04/WP-versions_Planned-Versions-1024x424.png)](https://make.wordpress.org/docs/files/2025/04/WP-versions_Planned-Versions.png)

Example of the planned versions block

[Post Release](#post-release)
-----------------------------

### [Roadmap](#roadmap)

Update the [Roadmap](https://wordpress.org/about/roadmap) by **removing the latest release** from the list of upcoming releases and **fix the dates** of any planned releases if the dates are known.

[![](https://make.wordpress.org/docs/files/2025/04/WP-Roadmap_Future-releases.png)](https://make.wordpress.org/docs/files/2025/04/WP-Roadmap_Future-releases.png)

Example of the Future releases as seen in the Roadmap page

### [History](#history)

Update the [History](https://wordpress.org/about/history) page by adding a new row to the table. Add the **version number** – it links to the official release announcement, add the **jazzer** (full name), and the **release date**.

[![](https://make.wordpress.org/docs/files/2025/04/WP-History-list.png)](https://make.wordpress.org/docs/files/2025/04/WP-History-list.png)

Example of the History page update

These two pages must be updated simultaneously, as they will be pushed to the sandbox together to maintain version control. For more details, see [Updating content on WordPress.org](https://make.wordpress.org/meta/handbook/about/projects/wordpress-org/updating-content-on-wordpress-org/).

### [Learn about WordPress origins and version history](#learn-about-wordpress-origins-and-version-history)

Update the article [Learn about WordPress origins and version history](https://wordpress.org/documentation/article/learn-about-wordpress-and-version-history/): 

*   Add the year if it is the first release of the year. If it is not the first, add the version number next to the announcement
*   Link the version number to the formal [release announcement](https://wordpress.org/news/2025/04/cecil/)
*   Begin the paragraph with the version number and name linked to [version page](https://wordpress.org/documentation/wordpress-version/version-6.8/)
*   Add the number of contributors
*   Copy/paste the first paragraph from the release announcement.
*   Add a link to the jazzer’s wikipedia page

**2025 – Announcement:** [6.8](https://wordpress.org/news/2025/04/cecil/)[Version 6.8 (Cecil):](https://wordpress.org/documentation/wordpress-version/version-6.8/) **(>900 contributors)** Each WordPress release celebrates an artist who has left an indelible mark on music.  WordPress 6.8, code-named “Cecil,” honors the legendary pianist and jazz pioneer [Cecil Taylor.](https://en.wikipedia.org/wiki/Cecil_Taylor)