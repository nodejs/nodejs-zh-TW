title: "npm 週報 #9 2015-03-17"
tags:
categories: npm 週報
---

本週的 npm 最新消息，同樣也[可以透過 email 訂閱](https://www.npmjs.com/npm-weekly)。

## A hiccup in the CLI

Just a heads up for those of you who use npm shrinkwrap --dev, there was a minor bug in that command in last week’s npm@next, which was 2.7.2. Forrest patched it right up and tagged a new npm@next. Thanks to dan_abramov for the helpful report of this issue, and for testing out npm@next.

If you don’t know what npm@next is, it is the version of npm that will be released as the stable release the next week, at which point it is tagged npm@latest. When you run the command npm install -g npm, you get npm@latest. But if you want to be a tester for our new functionality and make sure that it’s as stable as it can be, you can use npm install -g npm@next to do that. We <3 our testers.

## What’s coming in npm@3

Speaking of npm shrinkwrap, with npm@3 using shrinkwraps will be more convenient. When you install or remove a module with --save in a project with a shrinkwrap, npm will automatically update the npm-shrinkwrap.json for you. As long as you use npm commands to manage your package.json dependencies (instead of hand-editing the dependencies), the npm-shrinkwrap.json will stay in sync.

## From the community

Have you ever been writing a module and an app that uses that module at the same time? Did you use npm link to do it? If not, you’ll probably want to check out this egghead.io video, Using npm link to use node modules that are “in progress”.

Ben Clinkinbeard, who recorded this screencast, was also behind the PR that made Angular work better with Browserify in the recent release 1.3.14 instantaneous-browserification. So thanks Ben!

## Pre-collection collections

We’re planning a feature for npm called collections. These will be user-written guides showing you how to use multiple packages together in one beautiful layout.

In the meantime, people have been rolling their own collections. Zeke has been collecting a bunch of these collections to see what people have been doing in the wild. If you have a collection, feel free to let us know there, and you’ll probably want to check out some of the collections that have already been added… they’re pretty neat.

原文：[npm weekly, #9](http://blog.npmjs.org/post/113882628280/npm-weekly-9)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
