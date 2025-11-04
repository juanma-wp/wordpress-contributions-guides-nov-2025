---
title: Documentation issue tracker
date: June 27, 2023
author: 
categories: 
url: https://make.wordpress.org/docs/handbook/github-repository-and-projects/documentation-issue-tracker/
---

The [Documentation issue tracker](https://github.com/WordPress/Documentation-Issue-Tracker) is the central place for contributing to WordPress documentation. No actual documentation is hosted in this repository. Its purpose is to track all the issues for any part of WordPress documentation. Therefore, the most used functionality is its [issues](https://github.com/WordPress/Documentation-Issue-Tracker/issues) and [automatisation](https://github.com/WordPress/Documentation-Issue-Tracker/tree/main/.github).

[Labels](#labels)
-----------------

As with any other project management tool, the Documentation issue tracker uses several issue labels for easier filtering out the issues. Depending on what you want to filter, you will find labels for various criteria.

### [Version-based](#version-based)

Some documentation is done as updates for new WordPress releases. These are the numbered labelled, representing the WordPress version.

Some examples are [6.0](https://github.com/WordPress/Documentation-Issue-Tracker/labels/6.0), [6.1](https://github.com/WordPress/Documentation-Issue-Tracker/labels/6.1), [6.2](https://github.com/WordPress/Documentation-Issue-Tracker/labels/6.2) etc.

### [Project-based](#project-based)

The Documentation team maintains several projects, and each has its label. The main project division is:

*   [user documentation (HelpHub)](https://github.com/WordPress/Documentation-Issue-Tracker/labels/user%20documentation%20%28HelpHub%29)
*   [developer documentation (DevHub)](https://github.com/WordPress/Documentation-Issue-Tracker/labels/developer%20documentation%20%28DevHub%29)
*   [advanced administration](https://github.com/WordPress/Documentation-Issue-Tracker/labels/advanced%20administration)
*   [contributor documentation](https://github.com/WordPress/Documentation-Issue-Tracker/labels/contributor%20documentation)

Developer documentation is further divided into [apis](https://github.com/WordPress/Documentation-Issue-Tracker/labels/apis), [code reference](https://github.com/WordPress/Documentation-Issue-Tracker/labels/code%20reference), [mobile app](https://github.com/WordPress/Documentation-Issue-Tracker/labels/mobile%20app), [plugins](https://github.com/WordPress/Documentation-Issue-Tracker/labels/plugins), [themes](https://github.com/WordPress/Documentation-Issue-Tracker/labels/themes) etc., but there are other project labels, such as [external links](https://github.com/WordPress/Documentation-Issue-Tracker/labels/external%20links) etc.

### [Status-based](#status-based)

Depending on the status of the issue itself, the repo has four different labels:

*   [\[Status\] To do](https://github.com/WordPress/Documentation-Issue-Tracker/labels/%5BStatus%5D%20To%20do)
*   [\[Status\] In progress](https://github.com/WordPress/Documentation-Issue-Tracker/labels/%5BStatus%5D%20In%20progress)
*   [\[Status\] Review](https://github.com/WordPress/Documentation-Issue-Tracker/labels/%5BStatus%5D%20Review)
*   [\[Status\] Done](https://github.com/WordPress/Documentation-Issue-Tracker/labels/%5BStatus%5D%20Done)

### [Type of work](#type-of-work)

Labels for the type of work usually represent the amount or complexity of needed work, such as [typo](https://github.com/WordPress/Documentation-Issue-Tracker/labels/typo), [tracking issue](https://github.com/WordPress/Documentation-Issue-Tracker/labels/tracking%20issue) (an issue which tracks progress on several related issues), [needs screenshots](https://github.com/WordPress/Documentation-Issue-Tracker/labels/needs%20screenshots), [new document](https://github.com/WordPress/Documentation-Issue-Tracker/labels/new%20document), [migration from Codex](https://github.com/WordPress/Documentation-Issue-Tracker/labels/migration%20from%20Codex) etc.

### [Helpers](#helpers)

Helper, or “other” labels, help narrow the search further. Some examples are [good first issue](https://github.com/WordPress/Documentation-Issue-Tracker/labels/good%20first%20issue), [internal tasks](https://github.com/WordPress/Documentation-Issue-Tracker/labels/internal%20tasks), [triage](https://github.com/WordPress/Documentation-Issue-Tracker/labels/triage) etc.

[Automatisation](#automatisation)
---------------------------------

The Documentation issue tracker repository is connected to several project boards via automatisation, but also, some processes inside the repo itself are automated.

### [Add issues to projects](#add-issues-to-projects)

When certain labels are applied to the issue, the issue gets automatically added to the appropriate project. Some examples are:

*   Labels `HelpHub feedback` and `user documentation (HelpHub)` will send the issue to the [End-user documentation](https://github.com/orgs/WordPress/projects/90) project board. The workflow can be found in [.github/workflows/add-issue-to-end-user-docs.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/add-issue-to-end-user-docs.yml)
*   Label `6.3` will send the issue to the [WP 6.3 Documentation](https://github.com/orgs/WordPress/projects/108) project board. The workflow can be found in [.github/workflows/add-to-6-3-project.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/add-to-6-3-project.yml)
*   Label `advanced administration` will send the issue to the [Advanced administration handbook](https://github.com/orgs/WordPress/projects/47) project board. The workflow can be found in [.github/workflows/add-to-advanced-administration-project.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/add-to-advanced-administration-project.yml)
*   Label `contributor documentation` will send the issue to the [Documentation team Handbook](https://github.com/orgs/WordPress/projects/43) project board. The workflow can be found in [.github/workflows/add-to-docs-handbook-project.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/add-to-docs-handbook-project.yml)

On success, the issue will have something like this:

[![Labels and project for the issue.](https://make.wordpress.org/docs/files/2023/06/add-to-project.png)](https://make.wordpress.org/docs/files/2023/06/add-to-project.png)

### [Label issues](#label-issues)

Status-based labels are automated in the following way:

*   `[Status] To do` label is applied to every newly created issue. This is set in our issue templates: [new-doc.md](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/ISSUE_TEMPLATE/new-doc.md), [doc-issue-fix.md](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/ISSUE_TEMPLATE/doc-issue-fix.md), and [helphub-feedback-reports.md](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/ISSUE_TEMPLATE/helphub-feedback-reports.md).
*   `[Status] In progress` label is applied to the issue when the issue is assigned, AND has `[Status] To do` label. It is done in [label-when-assigned.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/label-when-assigned.yml) workflow.
*   The issue is transferred from `[Status] In progress` to `[Status] Review` label when a comment is created and contains `/review`, AND has `[Status] In progress` label. It is done in [label-when-commented.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/label-when-commented.yml) workflow.
*   Every closed issue will automatically be transferred to `[Status] Done` label. This is done in [label-when-closed.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/label-when-closed.yml) workflow.

Complete work on automated labelling can be found in [#882](https://github.com/WordPress/Documentation-Issue-Tracker/issues/882) issue.

The workflow looks like this:

[![GitHub bot changing labels for the issue.](https://make.wordpress.org/docs/files/2023/06/status-labels.png)](https://make.wordpress.org/docs/files/2023/06/status-labels.png)

### [Notify team](#notify-team)

[Team members in charge of specific documentation projects](https://make.wordpress.org/docs/handbook/the-team/) will be notified in a comment when a label for their project is applied. This is done in [notify-team-on-label.yml](https://github.com/WordPress/Documentation-Issue-Tracker/blob/main/.github/workflows/notify-team-on-label.yml) workflow.

This is an example of the notification:

[![GitHub bot comment mentioning Themes project reps because label themes was applied to the issue.](https://make.wordpress.org/docs/files/2023/06/Theme-Handbook-Overhaul-Getting-Started-Quick-start-guide-·-Issue-878-·-WordPress-Documentation-Issue-Tracker-1024x169.png)](https://make.wordpress.org/docs/files/2023/06/Theme-Handbook-Overhaul-Getting-Started-Quick-start-guide-·-Issue-878-·-WordPress-Documentation-Issue-Tracker.png)