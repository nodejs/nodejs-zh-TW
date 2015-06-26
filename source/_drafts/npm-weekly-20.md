title: "npm 週報 #20 npm 3 來了!"
tags:
categories: npm 週報
---

你希望可以[直接收到](https://www.npmjs.com/npm-weekly) npm 最新更新的消息嗎？

## just hours away from npm@3!

![](http://40.media.tumblr.com/b94cebf75ced4e981031b414bbec3d6e/tumblr_inline_nqisluM4il1t68bpr_500.png)

The eagerly anticipated npm 3 will have an official npm release today (or early tomorrow morning, depending on your time zone).

A few things to note:

1.  When you use the command `npm install -g npm`, it will still download npm@2 until we’ve moved npm@3 out of beta. You can download the beta using `npm install -g npm@3.0-latest`.
2.  npm@3 is going to be in beta until we’re comfortable with its stability and the effect of the breaking changes on the community.
3.  One of those breaking changes is the way `peerDependencies` works. If you have a module that uses peerDependencies, please make sure you understand the changes. We will be writing a blog post about this soon.

If you’re chomping at the bit to find out about all the changes and new features, you can check out the draft [CHANGELOG](https://github.com/npm/npm/blob/multi-stage/CHANGELOG.md).

## moving towards better front-end support

npm is now the registry of choice for many front-end communities, but we still have a way to go before the front-end experience is seamless. We’ve [talked about this](http://blog.npmjs.org/post/101775448305/npm-and-front-end-packaging) before, and the changes to peerDependencies were a small step in that direction.

[Forrest](https://twitter.com/othiym23), the CLI team lead, will be updating the CLI roadmap to include plans for better support for front-end use cases over the next couple of major releases.

In the meantime, folks are playing around with ideas in userland. One that caught our eye recently was [Aria Stewart](https://twitter.com/aredridel)’s [copy-browser-modules](https://www.npmjs.com/package/copy-browser-modules). If you try it out, let us know how it works for you :)

## bonus human

We had an avalanche of humans last week and promised another bonus human for this week. The bonus human has arrived! [Chris Dickinson](https://twitter.com/isntitvacant) has joined the registry team. He’ll be spending some of his time tracking down issues in Node that affect the registry (& vice versa). He’ll also be helping us introduce [npm private modules](https://www.npmjs.com/private-modules) support for organizations and teams, which we’re very excited for, and continuing his Node.js contributions.

## npm registry deep dive

If you’re interested in finding out more about the registry and how it works, you should check out [CJ](https://twitter.com/ceejbot)’s [registry deep dive](https://www.youtube.com/watch?v=mGh3lW9oAgk) from NodeConf One-Shot Oslo a few weeks ago.


原文：[npm Weekly, #20](http://blog.npmjs.org/post/122450408965/npm-weekly-20-npm-3-is-here-ish)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
