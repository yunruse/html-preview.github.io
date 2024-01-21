<!--
SPDX-FileCopyrightText: 2012 - 2021 Jerzy Głowacki <jerzyglowacki@gmail.com>

SPDX-License-Identifier: Apache-2.0
-->

# GitHub & BitBucket HTML Preview

[![License: Apache-2.0](
    https://img.shields.io/badge/License-Apache--2.0-blue.svg)](
    LICENSE.txt)
[![REUSE status](
    https://api.reuse.software/badge/github.com/osegermany/git-forge-html-preview)](
    https://api.reuse.software/info/github.com/osegermany/git-forge-html-preview)

Many GitHub repositories don't use GitHub Pages to host their HTML files. **GitHub & BitBucket HTML Preview** allows you to render those files without cloning or downloading whole repositories. It is a client-side solution using a CORS proxy to fetch assets.

If you try to open raw version of any HTML, CSS or JS file in a web browser directly from GitHub, all you will see is a source code. GitHub forces them to use the "text/plain" content-type, so they cannot be interpreted. This script overrides it by using a CORS proxy.

## Usage

In order to use it, just prepend this fragment to the URL of any HTML file: **[https://htmlpreview.github.io/?](https://htmlpreview.github.io/?)** e.g.:

 - https://htmlpreview.github.io/?https://github.com/twbs/bootstrap/gh-pages/2.3.2/index.html
 - https://htmlpreview.github.io/?https://github.com/documentcloud/backbone/blob/master/examples/todos/index.html

What it does is: load HTML using CORS proxy, then process all links, frames, scripts and styles, and load each of them using CORS proxy, so they can be evaluated by the browser.

**GitHub & BitBucket HTML Preview** was tested under the latest Google Chrome and Mozilla Firefox.
