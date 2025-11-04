---
title: Submitting a Patch
date: July 12, 2012
author: 
categories: 
url: https://make.wordpress.org/core/handbook/tutorials/trac/submitting-a-patch/
---

[Overview](#overview)
---------------------

Once you’ve edited the file and tested it, you need to create a patch and upload it to the corresponding Trac ticket so other people can see and test the changes. You can create a _patch_ a number of ways.

When using an IDE or a Subversion client a patch can be created directly by the application. The patch should be created from the root directory (the folder that contains the `/src` directory, the `wp-config-sample.php` file, etc.).

### [Windows](#windows)

**If you are on Windows,** consider using [Tortoise SVN](http://tortoisesvn.net/). You can [read our tutorial on creating a patch with Tortoise SVN](https://make.wordpress.org/core/handbook/tutorials/working-with-patches/#creating-a-patch-with-tortoisesvn).

### [Mac/Linux Command Line](#mac-linux-command-line)

From [Mark Jaquith’s Tutorial](http://markjaquith.wordpress.com/2005/11/02/my-wordpress-toolbox/)

Make a patch, for filename.php:

`$ svn diff filename.php > filename.diff`

Make a patch for all files modified in the checkout:

`$ svn diff > big_patch.diff`

Apply a patch from someone else:

`$ patch -p0 < patch.diff`

There are some GUI options for the Mac, as well — you just need it to create patch files (Versions cannot, for example).

Also: [creating SVN patches using Git](http://scribu.net/wordpress/svn-patches-from-git.html), from Cristi Burca.

[Submitting a patch via GitHub](#submitting-a-patch-via-github)
---------------------------------------------------------------

If you prefer using GitHub for code reviews and collaboration, the WordPress core code is available as a [GitHub mirror](https://github.com/wordpress/wordpress-develop) where you can submit patches.

1.  Fork the GitHub mirror to your own account using the **Fork** option at the top of the GitHub page.
2.  Clone your fork to your local computer. Replace `your-username` with your GitHub username.

`git clone git@github.com:your-username/wordpress-develop.git`

3.  Create a new branch to work on a specific Trac ticket — never work directly on trunk. Name it after the Trac ticket number and a brief description of the change.

`git checkout -b 44722-fix-issue-in-component`

4.  Make your code changes, commit them, and push your branch to your fork.

`git push origin 44722-fix-issue-in-component`

5.  Go to your fork on GitHub. If your GitHub account is linked to your WordPress.org profile, GitHub will prompt you to open a Pull Request. Make sure the title includes the Trac ticket number (e.g., [#44722](https://core.trac.wordpress.org/ticket/44722): Fix X issue in Y component).

While first forking the mirror and then cloning it locally is recommended, if you’ve already cloned the `wordpress/wordpress-develop` mirror, you can add your fork as a remote repository using git remote add.

`git remote add fork git@github.com:your-username/wordpress-develop.git`

You’ll then still be able to create a local branch, but will need to push to the correct remote.

To learn more about working with remote repositories, see the [GitHub documentation](https://docs.github.com/en/get-started/git-basics/managing-remote-repositories).

For more details on GitHub integration, see the [GitHub Pull Requests for Code Review documentation](https://make.wordpress.org/core/handbook/contribute/git/github-pull-requests-for-code-review/).