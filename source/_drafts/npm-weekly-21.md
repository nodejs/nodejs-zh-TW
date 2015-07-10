title: "npm 週報 #21 : npm 3 更新 + react.js 元件工具"
tags:
categories: npm 週報
---

[Sign up](https://www.npmjs.com/npm-weekly) for the weekly.

## npm 3 beta testers

If you’re an npm@3 beta tester, be advised: the tags for downloading the latest and next versions of npm@3 have changed. They are now `npm@3.x-next` and `npm@3.x-latest`. Checkout the [CHANGELOG](https://github.com/npm/npm/blob/master/CHANGELOG.md) for more info. Also, thank you to all of you for helping us squash all those bugs!

[Kat](https://twitter.com/maybekatz) also snuck a lot of things into npm@2 while [Forrest](https://twitter.com/othiym23) was away, so checkout those in the [CHANGELOG](https://github.com/npm/npm/blob/master/CHANGELOG.md#v2130-2015-07-02).

## npm 3 beta brings good news for windows users

[Rebecca](https://twitter.com/ReBeccaOrg) [talked to InfoQ](http://www.infoq.com/news/2015/06/npm) about npm@3, particularly how the changes to the installation process will help Windows users.

## private modules post-mortem

We’ve alerted private modules users via email, but in case you missed it there was a security issue with private modules last week. Metadata about private modules was leaked, but package contents and private user information were not. Read more in the [post-mortem](http://status.npmjs.org/incidents/6r2jr0dd9kd5).

## react podcast on webpack vs. browserify

If you’re working with React.js components, you’ll probably want to listen to the React Podcast on [Webpack vs Browserify](http://reactpodcast.com/2015/06/webpack-vs-browserify/) as tools for managing your front-end dependencies. The discussion starts around the 7-minute mark.

On the same subject, [Lin](https://twitter.com/linclark) explained how you can [use Browserify with npm (and Babel)](https://youtu.be/Tjwm9yPzBGg?t=6913) for front-end package management at jQuerySF last month and will be talking about Webpack at [React Rally](http://www.reactrally.com/) in August.

## npm is now my snippet database

In his AMA, [Sindre Sorhus](https://twitter.com/sindresorhus) explains how he uses npm as a way to [capture his code snippets](https://github.com/sindresorhus/ama/issues/10#issuecomment-117766328).

Why copy-paste when you can require it and with the benefit of having a clear intent. Fixing a bug in a snippet means updating one module instead of manually fixing all the instances where the snippet is used.


原文：[npm Weekly, #21](http://blog.npmjs.org/post/123564120105/npm-weekly-21-npm-3-updates-react-js)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
