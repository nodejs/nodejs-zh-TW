title: "npm 週報 #32 : multiplatform development, Hoodie, nodebots, wombat GIFs"
date:
tags:
categories: npm 週報
---

[Sign up for the Weekly](https://www.npmjs.com/npm-weekly?utm_campaign=newsletter20151012 "sign up for the npm Weekly") and get this sent to you instead!

[![](https://partners.npmjs.com/weekly/weekly32/weekly-header-grace-hopper.png "npm3 ♥ The Grace Hopper Celebration of Women in Computing")](http://gracehopper.anitaborg.org "npm3 ♥ The Grace Hopper Celebration of Women in Computing")

## OSS development: not just for Macs

[![a pun about Mavis teaching typing](https://partners.npmjs.com/weekly/weekly32/leno-gates-windows-1200x.jpg "a pun about Mavis teaching typing")](http://)

We ❤️ hipster hackers (and we’re typing this on a MacBook Pro while drinking cold-brew &c.), but stats don’t lie, and a large percentage of developers are still avid Windows users. After our own Ben Coe [broke Atom on Windows](https://github.com/atom/atom/issues/8559 "Atom won't start after upgrade · Issue #8559 · atom/atom") with one of [the open-source projects](https://github.com/bcoe/yargs "bcoe/yargs") he contributes to, he got motivated to test all of his libraries on Windows.

Good news: there are some awesome tools available that can help:

*   **[ievms](https://github.com/xdissent/ievms "xdissent/ievms")**: Microsoft provides disk images for testing on multiple versions of IE; these same images can be purposed for testing your Node.js applications.
*   **[appveyor](http://ci.appveyor.com/ "AppVeyor")**: Similar to [travis-ci.org](https://travis-ci.org "Travis CI - Test and Deploy Your Code with Confidence"), appveyor allows you to run Windows integration testing for free on your open-source projects.
*   **shims!** developers have published many Windows shims to npm. These libraries provide a developer with an identical API regardless of platform:
    *   **[win-spawn](https://www.npmjs.com/package/win-spawn "win-spawn")**: shim spawn API for running on Windows platforms.
    *   **[lcid](https://www.npmjs.com/package/lcid "lcid")**: mappings between standard locale identifiers and Windows locale identifiers.

[Jeff](http://github.com/jefflembeck "jefflembeck (Jeff Lembeck)") adds:

> IE’s VMs have saved my ass more times than I can count.

## package.json scripts: not just for JavaScript

[![hoodie-css/DEVELOPMENT.md at feature/build-automation · hoodiehq/hoodie-css](https://partners.npmjs.com/weekly/weekly32/hoodie-dog.jpg "hoodie-css/DEVELOPMENT.md at feature/build-automation · hoodiehq/hoodie-css")](https://github.com/hoodiehq/hoodie-css/blob/feature/build-automation/DEVELOPMENT.md "hoodie-css/DEVELOPMENT.md at feature/build-automation · hoodiehq/hoodie-css") [Hoodie](http://hood.ie "hood.ie") has a pretty swell mission:

> making the lives of frontend developers easier by abstracting away the backend and keeping you from worrying about backends

Write frontend code, hook it up to Hoodie’s API, and you’re off to the races.

Hoodie itself is built based on Node, so setting up the dev environment makes use of [scripts](https://docs.npmjs.com/cli/run-script "run-script | npm Documentation") defined in its `package.json`. Hoodie’s docs [helpfully spell out](https://github.com/hoodiehq/hoodie-css/blob/feature/build-automation/DEVELOPMENT.md "hoodie-css/DEVELOPMENT.md at feature/build-automation · hoodiehq/hoodie-css") what each script does, explain why the environment is set up as it is, and help you consider using npm as a build tool.

We especially like their reminder that the “scripts” in a `package.json` don’t _have_ to be JavaScript. Defining a command as a script tells npm to run the command whenever you use the script’s name as an argument to `npm run` — and it can be anything that’s executable from the console. It’s possible (and really useful) to hugely automate your builds without resorting to baroque tools.

Give [Hoodie’s writeup](https://github.com/hoodiehq/hoodie-css/blob/feature/build-automation/DEVELOPMENT.md "hoodie-css/DEVELOPMENT.md at feature/build-automation · hoodiehq/hoodie-css") a read and give scripts a whirl.

## robotics: not just for PhDs

Robots are crazy cool, but historically, the field of robotics has had some crazy high barriers to entry, not least of which are years of education and scads of funding. [Nodebots](https://github.com/nodebots/nodebots.io/wiki/What-Are-Nodebots "What Are Nodebots · nodebots/nodebots.io Wiki") represent a huge step forward in the accessibility and speed of hacking and robot building by using JavaScript to reduce the complexity of writing the code that operates robotic hardware.

If this sounds, well, crazy, check out [Raquel](https://twitter.com/rockbot "Raquel Vélez (@rockbot) | Twitter")’s [Strange Loop](http://www.thestrangeloop.com/index.html "Home - Strange Loop") talk, [No, Really … Robots and JavaScript?!](https://www.youtube.com/watch?v=3v75aX5-gSA&feature=youtu.be ""No, Really... Robots and JavaScript?!" by Raquel Vélez - YouTube"):

> Let’s discuss why, of all the languages on the planet, JavaScript is the perfect starting point for a future of robotics. As a roboticist-turned-web-developer, I will provide some deep insights not only into the world of robotics, but also into JavaScript and its server-side cousin, Node.js. We’ll talk about what JavaScript-enabled robots can already do, what they can’t do yet, and what they might be able to do with a bit of elbow grease.

Crazy!

## your inbox: not just for things that aren’t wombat GIFs

[![](https://partners.npmjs.com/weekly/weekly32/omgwombat.gif "eeeeeeee")](http://blog.npmjs.org/post/130644130685/how-to-email-daily-gifs-use-nodemailer-w-gmail?campaign=newsletter20151012 "How to email daily GIFs + use nodemailer w/ Gmail | The npm Blog")

Wombat emeritus [Shivani Negi](https://github.com/imshivs "imshivs (Shivani Negi)") has [a groovy step-by-step tutorial](http://blog.npmjs.org/post/130644130685/how-to-email-daily-gifs-use-nodemailer-w-gmail?campaign=newsletter20151012 "How to email daily GIFs + use nodemailer w/ Gmail | The npm Blog") that solves a major problem: namely, that your email inbox doesn’t have enough GIFs of baby wombats. And…

> along the way we’ll make use of Giphy, nodemailer, cron, Google’s Developer Console, and Heroku.

It’s another in a continuing series of posts to familiarize newer developers — which, statistically, [probably includes you](https://twitter.com/seldo/status/644932539635757056 "Laurie Voss on Twitter: "By npm's best estimates, 50% of node.js users started using node less than 12 months ago. We are a community of newbies."") — with the power & ease of using Node & npm to build neat things. Watch this space for more to come, and don’t be shy about letting us know what else you’d like to learn.

#### sponsored [[?](http://info.npmjs.com/sponsorship?utm_campaign=newsletter20151012 "sponsor the Weekly")]

## Hired: not just for Node engineers

[Hired](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent") connects software developers, data scientists, designers, and sales talent with over 2,500 vetted tech companies in 13 major tech hubs, probably including yours. Developers on Hired receive an average of 5 interview requests within a week. Looking for a job? [Check them out](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent").

原文：[npm weekly, #32](http://blog.npmjs.org/post/131029139785/npm-weekly-32-multiplatform-development-hoodie)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
