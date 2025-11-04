---
title: Post & Comment Guidelines
date: March 10, 2016
author: 
categories: 
url: https://make.wordpress.org/core/handbook/best-practices/post-comment-guidelines/
---

These guidelines were [initially proposed on make/core](https://make.wordpress.org/core/2015/09/30/proposal-makecore-post-guidelines/). If you have questions or feedback, please join Slack and ask in [#core](https://wordpress.slack.com/messages/C02RQBWTW).

[Introduction](#introduction)
-----------------------------

The Make WordPress Core Blog (make/core) is the official blog of the WordPress core team. It is read by thousands of people, many of whom may not know the intricacies of core, or understand the process of core development.

Most make/core posts must serve one of two goals:

1.  Generate feedback (including testing) from the developer community
2.  Ensure developers know about changes and can plan accordingly
3.  Sharing upcoming scheduled events like bug scrubs or meetings with specific focuses

In order to ensure the best experience possible for the developer community, the guidelines on this page are written with unexperienced readers in mind.

[Posting](#posting)
-------------------

### [Getting Access to Post](#getting-access-to-post)

Access to posting and editing on make/core is managed in the [#core room in Slack](https://wordpress.slack.com/archives/C02RQBWTW). It is best to have someone who already has access to ask on your behalf, but if you feel you should have access to create a post, please don’t hesitate to ask for yourself. The same process is used for changing roles. Before access is granted, please do a small self-audit of your security:

*   Make sure you have a strong password on WordPress.org: it should be long, random, and stored in the password manager of your choice.
    *   Bad: X\*7z7XL{kZvky7E(
    *   Good: aLy%t;67zvy3VdFwVPKA@VGV?i7oq.63Lj.2aKZ@Tw3\].Eu4kVUJJVGyXH7oRL\*a
*   Make sure you have two-factor auth enabled for your WordPress.org account. It’s also a very good idea to enable it for any service you use, since hackers will often leverage access to a low priority account to gain access to a high priority account.

### [When to Write a Post](#when-to-write-a-post)

Posting on make/core should be a common occurrence for committers, component maintainers, and other core contributors. There are many kinds of posts that should be written on a schedule:

*   **API changes.** There are a few examples of API changes that should be announced on Make/Core, including: new filters/actions, changed order of hooks, substantial enhancements to queries (the _Boone Gorges Rule_), changing the purpose of a parameter in a hook, new general helper functions, or any other significant changes in a release. These posts are commonly referred to as “developer notes” (or “dev notes”). Dev notes should be published on Make/Core no later than the end of the first beta period of the release shipping the change to ensure developers are aware of upcoming changes. Grouping related changes into one post to accepted, so long as the post does not become too long. For example, a single post called “Customizer changes in WordPress 4.2” is fine, rather than individual changes about each commit. If in doubt, use the weekly devchat to discuss your proposed post(s). See the [Writing Developer Notes page](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/) for more specific details about dev notes.
*   **Meeting announcements.** Regular devchat meetings do not need to be announced, but an agenda post is helpful to developers who do not regularly follow the release. Other meetings should receive an initial post on make/core announcing the meeting, but do not need weekly announcements.
*   **Meeting notes.** Do you hold regular or one-off meetings? Post notes from your meeting on make/core to ensure those that couldn’t attend have an easy way to provide feedback. Devchats almost always receive an accompanying summary post for those who can’t attend. Component chats and feature plugin chats should also have summary posts after meetings.
*   **Feature Plugin-related posts.** Introducing your feature plugin idea to the world is best done at a weekly devchat or one of the semi-regular feature plugin chats. Once proposed, a post on make/core can make sense, depending on the stage of the idea. Merge proposals should also make their way to make/core, when asked for from a release lead.

Keep in mind that feedback on make/core will almost always be greater than that in Trac tickets. Announcing changes and posting early and often is helpful to the entire community.

### [Peer Review](#peer-review)

Whether it’s your first time posting or your millionth, it is strongly encouraged to ask a trusted member of the team to proofread a post before publishing it. This can be anyone, but at least one Core Committer, editor on the site, or team rep is preferred. Peer review (like code review) helps make sure your words are clear and working as intended, but also helps identify any phrases that might not translate well. Some posts (like weekly agendas) do not necessarily need peer review, but if it’s your first few times posting on make/core, it doesn’t hurt to ask.

It’s also good practice to seek confirmation with the original reviewers that their feedback has been addressed before publishing. Since reviewers are given props at the bottom of each post, it’s important that they feel their concerns were heard and considered. It’s very common for multiple revisions to be made before everyone is happy with the contents of a post.

Feature plugin merge proposals should _always_ be read by the release lead (or designee) before posting. Release [developer notes](https://make.wordpress.org/core/handbook/tutorials/writing-developer-notes/) should be read by the release lead (or designee) before publishing.

See the Giving Proper Credit (Props) section below for information on how to make sure the proofreaders/peer reviewers are recognized.

### [Style and Substance](#style-and-substance)

The make/core blog is the official voice of the core team. As a result, you should keep your personal thoughts out of the body of the post, leaving them for the comments. Furthermore, **first person pronouns should be avoided**.

Similarly, **the word “we” should be avoided** in posts, unless its made very clear which group is speaking. An example of this is listing attendees of a meeting and, in the summary post, noting that “we, those present at the meeting” made a decision or agreed on a plan of action.

If you’re proposing a roadmap or making a request for comments, make sure to **highlight the draft/proposal status** in both the title and opening paragraph. This helps to avoid confusion about the status of your proposal.

Many people reading make/core don’t speak English as a first language. Keep that in mind when deciding how to phrase your post. For make/core, it’s always better to write simple instead of smart. In general, the tone should be similar to WordPress: Friendly.

_Check out the [Text-based Communication in Open Source](https://wordpress.org/contributor-training/lesson/text-based-communication-in-open-source/) and [Best Practices for Global Collaboration](https://wordpress.org/contributor-training/lesson/best-practices-for-global-collaboration/) pages on the [WordPress Contributor Training](https://wordpress.org/contributor-training/) site for more tips and best practices._

### [Giving Proper Credit (Props)](#giving-proper-credit-props)

When a post is finally published, it goes out under one person’s name. However, posts are often the combined efforts of several contributors who deserve to be recognized. Noting who helped bring a post to a publishable state can also provide important context to readers and helps them understand who they would be addressing in discussion.

At the bottom of your post, include a footnote like so:

_Props @desrosj and @jeffpaul for providing historical background, @chanthaboune and @andreamiddleton for proofreading._

### [Tagging and Other Specifics](#tagging-and-other-specifics)

For each of the following types of post, there are some things to keep in mind:

*   **Component-related posts.** Almost all posts relate to a component. Please tag component-related posts with the component name. If your post covers multiple components, use multiple tags!
*   **API changes.** All API changes should be tagged with the related release number, the component name, and “dev-notes” to indicate that it is a note for developers.
*   **Release announcements.** All posts related to a specific release – including agendas, meeting summaries, API changes, week in core, etc – should be tagged with the related release.
*   **Feature plugins and other projects.** Each of these type of post should be consistently tagged with a project name. For example, if you’re working on a redesign of the admin called “MP6,” tag all related posts with MP6.
*   **Meeting announcements.** When posting about a meeting ahead of time (aka, not summary notes), use the [time shortcode](https://make.wordpress.org/meta/2013/04/03/time-shortcode-for-make-p2s/) so that readers know exactly when the meeting will take place in their local time.
*   **Table of contents:** Posts are generally meant to be read as organized by the author from beginning to end. Because of this, a table of contents should not be included within most posts. Other content such as the Field Guide, pages in the Handbook, etc., are meant to serve as canonical reference materials. A table of contents is more appropriate and acceptable within these contexts. If you begin to think a ToC is necessary in a post that you’re authoring, step back and consider whether the information should be published to the Handbook, or the [Developer Hub](https://developer.wordpress.org/) so the post can summarize the high level summary, detail motivations, and explain rationale.

### [Proposals](#proposals)

When writing up an idea aimed at generating feedback and assessing a potential change from the core contributor community it is important that it is clear that what is being written is a proposal and not a final decision. To help achieve that, proposals must include the word “Proposal” at the start of the title and include text in the body explaining that a final decision has not yet been made.

### [Comments on Posts](#comments-on-posts)

Comments on posts will automatically close after 180 days (about 6 months). If you need to keep comments open, you can use the tag `#keep-comments-open` but this should only be used with a specific timeframe in mind rather than allowing comments to stay open forever.

[Comments](#comments)
---------------------

Discussion and criticism of ideas are important to the long-term success of WordPress. In support of this, all make/core posts have open comments. As a result, **commenters should be respectful and professional**, understanding that many other commenters and readers do not speak English as a first language. At times, it may make sense to over-communicate and be extra polite to ensure no misunderstandings occur.

If a comment is disrespectful and/or unprofessional, it may be edited at the discretion of the core team.

Editing of a comment will be done with the approval of at least two blog administrators. When a comment is edited, only the offending section will be edited with the intent of retaining as much of the expressed opinion. The administrators who edit the offending comment will add an editor’s note stating the reason for editing and the names of the administrators who took action. Additionally, the administrator doing the editing should retain a screenshot of the unedited comment, which can be uploaded to the Media Library on make/core, if necessary.

Comments will only be deleted when the offending comment is clearly spam that was not properly moderated.