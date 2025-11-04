---
title: JavaScript: QUnit
date: October 2, 2015
author: 
categories: 
url: https://make.wordpress.org/core/handbook/testing/automated-testing/qunit/
---

> QUnit is a JavaScript unit testing framework.

[Installation](#installation)
-----------------------------

**1\. Set up your install.** Follow one of the guides to setup your local install [https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/).

**2\. Install WordPress via SVN** Install WordPress via SVN or Git [https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/](https://make.wordpress.org/core/handbook/tutorials/installing-wordpress-locally/from-svn/).

[Running the QUnit Test Suite](#running-the-qunit-test-suite)
-------------------------------------------------------------

From your now installed and configured WordPress testing installation navigate to `/tests/qunit/index.html`.

If your locally setup domain is `http://wp-test.dev` then `http://wp-test.dev/tests/qunit/index.html` is the URL you want.

You can also run the tests directly in the browser without setting up a web server, append `/tests/qunit/index.html` to the the file path of your repo check out, for example `file:///Users/myusername/dev/develop.svn.wordpress.org/trunk/tests/qunit/index.html`