title: "npm 週報 #19 npm is massive + new lifecycle events"
tags:
categories: npm 週報
---

你希望可以[收到](https://www.npmjs.com/npm-weekly) npm 最新更新的消息嗎？

## npm is massive

![](http://38.media.tumblr.com/4c617284c1b80a823a29f8833f69e62c/tumblr_inline_nq45wnrjGF1t68bpr_540.gif)

We were blown away by Understanding npm, the visualization Hugh Kennedy put together for NodeSource’s N|Sight project… and here’s Dan Shaw’s explanation of it, npm is Massive.

## CLI 有什麼新功能？

We haven’t had a weekly for a few weeks, so we didn’t get to mention the new life cycle hooks, preversion and postversion. Whenever you type npm version to bump the version number in your package.json file and add the tag in git, any preversion package scripts that are defined in package.json will be run beforehand and postversion will be run afterwards.

This will be especially handy for things like transpiling your ES6 code to ES5 before releasing it… and Lin will be talking about just that at jQuerySF next week.

## why we sponsored jsconf’s live transcription

Isaac explains why npm values live transcription at conferences and why we sponsored it at JSConf this year.

## an avalanche of humans

so many humans…

A few weeks back, Kat Marchán joined the CLI team. Kat not only has tool development experience, but she also has lots of experience working with front end build systems, which we’re really excited about as we start gearing up for solid front-end support.

Then Shivani Negi came on as our summer intern. She’s getting acquainted with the npm codebase to see what she wants to focus on.

Full stack developer Jeff Lembeck joined the WWW team. He’ll be helping us as we make the right package easier to discover using the web site.

As VP of Marketing, Kasey Byrne is taking charge of the marketing efforts for products like npm private modules and npm Enterprise.

Emily Ross-Brown is joining as our first Executive Assistant to the C-team and helping make the executives more effective.

Stephanie Snopek is joining the support team to help you with any questions you send to support@npmjs.com or @npm_support.

Plus, a bonus human will be joining next week.

## designers, would you like to be an npm human?

We’re currently looking for a UX/UI designer to help us with the design of some chunky and challenging features. Is this you?

## a handy list of modules from nodeconf

NodeConf was last week. Lots of useful things came out of it, but one that we wanted to share was this list of cool modules. We especially like the participatory modules section, which includes modules for making your modules better. Thanks to Beau Gunderson for sharing his notes.

原文：[npm Weekly, #19]http://blog.npmjs.org/post/121795139990/npm-weekly-19-npm-is-massive-new-lifecycle)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
