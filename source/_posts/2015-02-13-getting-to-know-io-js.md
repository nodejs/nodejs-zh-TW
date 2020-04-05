title: "初探 io.js"
date: 2015-02-13 21:24:18
tags:
categories: iojs 好文
---

就在上個星期，開始在 Twitter 上面釋出 [io.js](http://iojs.org) 相關訊息，io.js 是一個以 Joyent 手中的 [Node.js](http://nodejs.org/) 為基礎，並且與 npm 相容的 fork 出來的專案。

## 為何要 fork Node.js？

io.js 團隊大部分的成員來自於原本 [Node.js 核心團隊](https://github.com/iojs/io.js/blob/v1.x/README.md#current-project-team-members)。在八月時候成立了一個 [Node Forward] 目標就是嘗試讓社群協助 Node.js 的成長。

> 透過社群合作力量來影響 Node, JavaScript 以及他的 Ecosystem

而以下才是 Node.js 被社群 fork 出來的前情提要的首要指標，

> 有些問題的決定權只在某些人手上，並沒有被分散下去，但是這些人力是分散在不同的小專案，所以人力是無法滿足這些小專案的快速發展。這些都需要更多貢獻者來達到目標。 Node Forward 就是一個這樣組織，希望讓更多貢獻者可以解決以上問題。

最後社群的協助還是不能解決 Node 商業考量目的。基於以上種種理由 io.js 就如此誕生了。

[Isaac Schlueter](https://twitter.com/izs) Node.js 核心貢獻者之一，提供了很多[背後故事](http://blog.izs.me/post/104685388058/io-js)說明為何要 fork Node.js 的原因。

其中一個主要的理由，希望藉由這兩個不同專案 (io.js, Node.js) 未來終究有合併的一天。

<!-- more -->

### io.js 新特徵

首先 io.js 採用正確的[版本語意 (sermver)](http://semver.org/) ，從 1.0.0 開始，這就是最大跟 Node.js 的不同。

[jQuery blog](http://blog.jquery.com/2014/10/29/jquery-3-0-the-next-generations/) 對於這個部分發表了為什麼版本語意的重要性。

> 版本語意在版本控管上是一件很重要的事情。在通則上，semver 賦予開發者或者開發工具一個很好的方向，讓大家知道版本更新的指標方法。可以從版本號碼知道目前是 MAJOR, MINOR, PATCH 是有格式軌跡可循，讓大家可以方便參考。在 semver 中，如果 MAJOR 號碼改變，開發者就知道這個版本有可能 API 會改變。

### V8 engine 更換

io.js 更新了 V8 JavaScript engine，更新到 3.31.74.1。最明顯的特徵就是可以完整支援 ES6 特性，並且不需要再加上 `--harmony` 這個指標。

#### 相容 ES6 特性

在 io.js 可以很順暢的執行 ES6 功能，功能如下列表

* [Block scoping (`let`, `const`)](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-let-and-const-declarations)
* Collections ([`Map`](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-map-objects), [`WeakMap`](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-constructor-properties-of-the-global-object-weakmap), [`Set`](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-set-objects), [`WeakSet`](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-constructor-properties-of-the-global-object-weakset))
* [Generators](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-generator-function-definitions)
* [Binary and Octal literals](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-literals-numeric-literals)
* [Promises](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-promise-jobs)
* [New String methods](http://www.sitepoint.com/preparing-ecmascript-6-new-string-methods/)
* [Symbols](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-ecmascript-language-types-symbol-type)
* [Template strings](https://people.mozilla.org/~jorendorff/es6-draft.html#sec-static-semantics-templatestrings)

#### 新模組

io.js 增加幾個實驗性的核心模組

* [smalloc](https://iojs.org/api/smalloc.html): 讓您透過 allocation/deallocation/copying 存取外部記憶體
* [v8](https://iojs.org/api/v8.html): 暴露 iojs 中 v8 的 events and interfaces。

你可以在 [io.js changelog](https://github.com/iojs/io.js/blob/v1.x/CHANGELOG.md) 上看到這些完整列表。

### 開始使用 io.js

開始使用 io.js 在 Node.js 應用裡面，使用方法跟使用 Node.js 一樣，唯一差異就是執行名稱不一樣了

Node.js

```
$ node app.js
```

io.js

```
$ iojs app.js
```

#### Node 版本管理

[Node version manager (nvm)](https://github.com/creationix/nvm), 就是一個幫助管理不同 Node.js 版本的工具，現在已經可以支援 io.js ，你可以透過以下的指令，找到 io.js 目前可安裝版本，接著進行安裝 io.js

```
$ nvm ls-remote v1
  iojs-v1.0.0
  iojs-v1.0.1
  iojs-v1.0.2
  iojs-v1.0.3
```

然後在你的專案中，安裝各別不同的 io.js 版本。

  $ nvm install iojs-v1.0.3

**Note:** 在本文編寫的時期，本人建議透過 nvm 安裝 io.js。許多早期安裝 io.js 的使用者透過 io.js 的安裝方式還是會影響到 Node.js 原本正常運作。 nvm 可以讓你在不同版本之間運作順暢。

### 立刻體驗

想要開始嘗試 io.js 的 Atlassian Connect add-on? 你可以快速取得 HipChat add-on 進行運作 io.js 以及相關 ES6 特徵像是 Generators 這些，可以透過以下步驟執行，

1. 到[HipChat Add-ons Quick Start guide](https://www.hipchat.com/docs/apiv2/quick_start?utm_source=dac&amp;utm_medium=blog&amp;utm_campaign=getting-to-know-iojs) 根據畫面指示並且取得  add-on ，執行[atlassianlabs/ac-koa-hipchat](https://bitbucket.org/atlassianlabs/ac-koa-hipchat?utm_source=dac&amp;utm_medium=blog&amp;utm_campaign=getting-to-know-iojs) framework

2. `vagrant ssh` 設定 vagrant server , 透過指令進行安裝 nvm

```
$ curl https://raw.githubusercontent.com/creationix/nvm/v0.23.0/install.sh | bash
```

將著將會安裝 nvm ，安裝結束後需要輸入 `exit` 關閉掉終端機.

3.  開啟 `package.json` 並進行修改

```
  "scripts": {
   "web": "iojs web.js",
   "web-dev": "nodemon --harmony -e js,json,css,hbs web.js"
  },
```

4.  再次執行 `vagrant ssh` 重新開啟服務，並且重新啟動 Node.js 伺服器

```
$ cd project && npm start web
```

將會啟動 Koa HipChat add-on 伺服器，你可以透過註冊你的 add-on 在 HipChat room 裡面設定，透過以下網址，

```
https://xxxxxxxx.ngrok.com/addon/capabilities
```

如果你輸入 `/hello`，HipChat add-on 將會回應你一個 "HI" ，恭喜，目前已經成功透過 io.js 以及 ES6 相關的使用。

### 建議何時開始使用 io.js

這應該是最多人會問到的問題，現在就可以開始使用 io.js 了嗎？

就是現在，io.js 在本文編寫時期大約為 v1.0.3 ，還是屬於 `Unstable` 階段。像是 nvm 還是會有一些小問題。還沒有太多公司宣布他們開始支援 io.js 。如果你是一個早期使用者，並且開始嘗試一些自己的 add-ons ，並且將發現的 issue 工佈到 io.js issue 列表。 最後現在可能還是有點早切換到 io.js ，但是持續關注它也許接下來 io.js 會成為 JavaScript 伺服器平台流行趨勢。

### 補充

目前 io.js 已經進入 v1.2.0 版本，並且已經宣告穩定，目前也有許多廠商宣告支援 io.js，所以可以安心服用，如有任何問題，歡迎到 [io.js 官方 issue](https://github.com/iojs/io.js/issues) 進行討論或者 bug 回報
