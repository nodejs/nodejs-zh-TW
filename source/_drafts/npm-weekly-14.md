title: "npm 週報 #14"
tags:
categories: npm 週報
---

## cordova 套件轉移到 npm

![](http://36.media.tumblr.com/2d401fa2e2e47128436526ca89754ace/tumblr_inline_nnl6v1YPDr1t68bpr_400.png)

Continuing the trend of frameworks moving their plugins to npm, Apache Cordova announced that it will use npm for its core plugins and is encouraging plugin developers to do the same. If you’re a Cordova dev, read their [instructions](http://cordova.apache.org/announcements/2015/04/21/plugins-release-and-move-to-npm.html) to find out how.

## CLI 消息

npm@next brings us up to version 2.9.0. There were two nanofeatures introduced. When you run npm outdated or npm update local modules will be included, and the prefix before the version in git version tags added by npm version is now configurable.

## deploying github pages

Are you maintaining a GitHub pages site? You can make your deployment process a little smoother using [npm run scripts](https://docs.npmjs.com/cli/run-script). Jessica Lord has a [great example](https://github.com/jlord/git-it/blob/master/package.json#L14-L17) in the git-it package.

原文：[npm Weekly, #13](http://blog.npmjs.org/post/117716297055/npm-weekly-14)，作者：[@LINCLARK](http://linclark.tumblr.com/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
