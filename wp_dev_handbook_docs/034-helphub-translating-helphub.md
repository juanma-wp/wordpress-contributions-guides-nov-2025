---
title: Translating HelpHub
date: October 14, 2018
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/helphub/translating-helphub/
---

HelpHub feature is available on [Rosetta](https://make.wordpress.org/polyglots/handbook/glossary/#rosetta) sites. **Locale teams can request activation on Polyglots P2** ([example](https://make.wordpress.org/polyglots/2020/12/02/helphub-plugin-on-zh_cn-rosetta-site/)), after putting together a team of volunteers to work on it.

For more background, refer to [HelpHub & Handbook i18n Updates](https://make.wordpress.org/polyglots/2019/07/30/helphub-handbook-i18n-updates/) (July 2019) and its linked posts, as well as [related meta trac tickets](https://meta.trac.wordpress.org/query?status=accepted&status=assigned&status=closed&status=new&status=reopened&status=reviewing&component=HelpHub&description=~plugin&summary=~rosetta&order=priority).

[HelpHub Migration Guide for Rosetta Sites](#helphub-migration-guide-for-rosetta-sites)
---------------------------------------------------------------------------------------

### [HelpHub Administrator](#helphub-administrator)

Polyglots Global Mentors can grant the first HelpHub Administrator role on a Rosetta site.

1.  Create a copy of [HelpHub Migration Worksheet (Template)](https://docs.google.com/spreadsheets/d/1It2w9pEv6X4CzIOFUilN5KnUxT06rI863750hjNdDvs/edit#gid=625788042) and enter the URL of the new spreadsheet to [HelpHub Migration Translation Status](https://docs.google.com/spreadsheets/d/1343cKHK5iV1TbOKuR57gcjkDV69xVik8QM_xjkJjDQI/edit?ts=5dddc3e0#gid=0) (column E of “Status” tab).
2.  Grant access to other contributors at the bottom of this page: `https://**LOCALE**.wordpress.org/support/users/**USERNAME**`
    
    ![](https://make.wordpress.org/docs/files/2019/09/helphub-role.png)
    
      
    (note: the dropdown will keep showing “no role for this site” until [#meta-4762](https://meta.trac.wordpress.org/ticket/4762) is fixed)
3.  Set up a call for help on your Rosetta site blog or your [`/team` P2](https://make.wordpress.org/polyglots/handbook/frequently-asked-questions/#how-to-activate-team-and-the-handbook-on-our-rosetta-site). Use the instruction described in the next section to clarify the steps for contributors (some examples can be found on the status spreadsheet, [column H](https://docs.google.com/spreadsheets/d/1343cKHK5iV1TbOKuR57gcjkDV69xVik8QM_xjkJjDQI/edit?ts=5dddc3e0#gid=0&range=H1)).

### [HelpHub Editor](#helphub-editor)

Here’s the instruction to contribute to HelpHub translation as an Editor.

**Note to HelpHub Administrator:** It’s a good idea to translate the steps below and insert relevant links for your locale.

1.  [Create a WordPress.org account](https://login.wordpress.org/register) if you don’t have one.
2.  Join documentation and/or translation channel on your [local Slack](https://make.wordpress.org/polyglots/handbook/about/teams/local-slacks/).
3.  Request HelpHub Editor role. Make sure to provide your WordPress.org username.
4.  Go to your locale’s Migration Worksheet.
5.  Pick an article, enter your name, and update the status.
6.  Go to `https://**LOCALE**.wordpress.org/support/wp-admin/edit.php?post_type=helphub_article` and start editing.
7.  Once some pages are published, a HelpHub Administrator can use the Customizer Widget to show HelpHub article on `/support/` landing page.
    1.  Select “Widgets” in the customizer.
    2.  Select the “Front page blocks” widget area.
    3.  Search for a “(HelpHub) Link block widget” and add it.
    4.  For dashicons reference, [use this link](https://developer.wordpress.org/resource/dashicons/).

![](https://make.wordpress.org/docs/files/2020/02/helphub-front-page-blocks.gif)

Setting up /support/ landing page through Customizer

### [Notes to Everyone](#notes-to-everyone)

1.  **Keep post slugs in English** for now so that current redirect rules will continue to work.
2.  All internal links should use **relative paths**.
3.  Report bugs to [Meta trac](https://meta.trac.wordpress.org), or ask in [#meta-helphub](https://wordpress.slack.com/messages/CG47GT4G2) / [#docs](https://wordpress.slack.com/messages/C02RP4WU5) Slack channels.
4.  Images that are not screenshots need to be recreated then translated (TBD).
5.  You can track the changes to English pages using the tools listed below.

[Tools](#tools)
---------------

*   [HelpHub latest Page Changes](https://wp-info.org/tools/helphubchanges.php): Lists recent updated pages
*   [HelpHub Updates](https://developerka.org/helphub-updates/): Compares last modified date with the translated page