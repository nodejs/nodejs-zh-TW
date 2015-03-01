title: "io.js 週報 2015.02.27"
tags:
categories: iojs 週報
---

_Note: version **1.4.0** was tagged and built but not released. A libuv bug was discovered in the process so the release was aborted. We have jumped to 1.4.1 to avoid confusion._
_注意：版本 **1.4.0** 已經編譯完成並標籤但是尚未釋出。在過程中一個 libuv 的臭蟲被發現所以這次的釋出將被棄置，我們將會升版號到 1.4.1 以避免造成混淆。_

## 主要更動

* **process** / **promises**: An`'unhandledRejection'` event is now emitted on `process` whenever a `Promise` is rejected and no error handler is attached to the `Promise` within a turn of the event loop. A `'rejectionHandled'` event is now emitted whenever a `Promise` was rejected and an error handler was attached to it later than after an event loop turn.  [#758](https://github.com/iojs/io.js/pull/758) (Petka Antonov)
* **streams**: you can now use regular streams as an underlying socket for `tls.connect()` [#926](https://github.com/iojs/io.js/pull/926) (Fedor Indutny)
* **http**: A new `'abort'` event emitted when a `http.ClientRequest` is aborted by the client. [#945](https://github.com/iojs/io.js/pull/945) (Evan Lucas)
* **V8**: Upgrade V8 to 4.1.0.21. Includes an embargoed fix, details should be available when embargo is lifted. A breaking ABI change has been held back from this upgrade, possibly to be included when io.js merges V8 4.2. See [#952](https://github.com/iojs/io.js/pull/952) for discussion.
* **npm**: Upgrade npm to 2.6.0. Includes features to support the new registry and to prepare for `npm@3`. See [npm CHANGELOG.md](https://github.com/npm/npm/blob/master/CHANGELOG.md#v260-2015-02-12) for details. Summary:
  * [#5068](https://github.com/npm/npm/issues/5068) Add new logout command, and make it do something useful on both bearer-based and basic-based authed clients.
  * [#6565](https://github.com/npm/npm/issues/6565) Warn that `peerDependency` behavior is changing and add a note to the docs.
  * [#7171](https://github.com/npm/npm/issues/7171) Warn that `engineStrict` in `package.json` will be going away in the next major version of npm (coming soon!)
* **libuv**: Upgrade to 1.4.2. See [libuv ChangeLog](https://github.com/libuv/libuv/blob/v1.x/ChangeLog) for details of fixes.

# ARM 提供 io.js 在 ARMv8 上的支援

ARM contacted Rod Vagg, lead of the io.js Build Working Group, to offer their support to the io.js project. ARM and their hardware partners are on track to make ARMv8 a viable server platform and the nimble nature of server-side JavaScript make it a perfect fit to run on the new ARM.

Since ARMv8 is already being adopted by mobile device manufacturers, newer versions of V8 already have good support. Because of V8's pivotal role in Android, io.js is perfectly suited to track that support, and even contribute to it given our new relationships with the V8 team.

From the beginning of the io.js project, Rod has championed the role of ARM for io.js, for IoT, hobbyist, and server use. We already have ARMv6 builds of each release for devices such as Raspberry Pi. and ARMv7 builds for many more popular devices (including the Online Labs ARM-based cloud platform, who have also offered help to io.js). ARMv8 is the logical extension of this, but also has exciting potential for server-side applications, particularly given the new 64-bit support.

The build team is in the process of being given access to the Linaro ARMv8 Server Cluster for integration with the io.js CI platform, which should eventually lead to regular ARMv8 binary releases.

# 社群更新

* [**和解提案**](https://github.com/iojs/io.js/issues/978)：io.js 著手開始進行對於 Node.js 基金會的和解草案。目前還是初期草案階段，因此來自社群的意見是非常重要的，請大家踴躍反饋。
* **New internal C++ Streams API**：一個全新的 [C++ Streams API] 在這週增加到 io.js 之中，允許你可以將 TLS stream 包裝成另一個 TLS stream。
* **io.js 路徑圖**：[路徑圖](https://github.com/iojs/io.js/blob/v1.x/ROADMAP.md) 是對 io.js 未來的規劃。它描述關於穩定性策略的規劃以及列出 io.js 的當務之急。
* **路徑圖的投影片已經完成等待翻譯**：一系列之於 io.js 路徑圖的投影片已經[完成可以進行翻譯](https://github.com/iojs/roadmap/issues/18)。你覺得你可以向周遭的群體做簡報嗎？留下你的意見，我們會與你協作幫你預備好簡報！
* **Microsoft io.js How-To for Azure Websites**: 微軟 發佈一篇關於他們 Azure 平台的[入門教程](http://azure.microsoft.com/en-us/documentation/articles/web-sites-nodejs-iojs/)，描述如何在 Azure 上使用 io.js。
* **Floobits moves to io.js**: 配對編程軟體 Floobits [將他們的平台轉移到 io.js](https://news.floobits.com/2015/02/23/on-moving-to-io.js/)，因為對於 Node 過於緩慢的釋出感到挫折，對於可以開始使用 ES6 的新功能而又不需要增加 `--harmony` 的參數，他們也覺得從 0.10.0 到 0.12.0 的改動並不是非常明顯。
* **Anand Mani Sankar's _Node.js vs io.js: Why the fork?!?_**: Anand 寫了一篇很不錯也相當客觀的 [io.js 近期歷史的文章](http://anandmanisankar.com/posts/nodejs-iojs-why-the-fork/#.VO82hE60PVw.twitter)，也提及我們希望藉由 io.js 實現什麼。可以幫助哪些沒有參與到社群之中的人可以瞭解目前的狀況。
* **iojs-jp - New io.js Japanese Blog**: iojs-jp 社群建立了[本地化的部落格](http://blog.iojs.jp/)，用當地的語言來傳遞  io.js 的消息。如果你感興趣，快去看看吧！
* **iojs-cn - New io.js Chinese Blog**: 類似於 iojs-jp 社群，iojs-cn 社群也成立了[本地化的部落格](http://cn.iojs.org/)，用中文來發佈關於 io.js 的文章。如果你對於 iojs-cn 或 iojs 中文新聞感到興趣的話，請不要錯過！
* **[檢閱路徑圖投影片](https://www.youtube.com/watch?v=etI_UD4wXlo)** - 在釋出前對 io.js 路徑圖簡報的檢閱，確保它有符合專案的目標。

# 對 io.js 的支援增加
* **[Wallby.js](http://wallabyjs.com/)**，一個 JavaScript 的即時測試函式庫，釋出了 1.0 版本並[增加對 io.js 的支援](http://dm.gl/2015/02/23/wallaby-version-one/)！
* **[jsdom](https://github.com/tmpvar/jsdom)**，針對 WHATWG DOM 和 HTML 標準的實作，剛釋出了 [4.0.0 版本](https://github.com/tmpvar/jsdom/blob/master/Changelog.md#400) 並且加入了 io.js 的依賴需求。
* **[give](https://github.com/mmalecki/give)** 的作者[發了一則推文](https://twitter.com/maciejmalecki/status/569629100215816192) 宣布新版的 give 將會增加對 io.js 的支援。Give 是基於 git 的 node.js/io.js 版本控制器。
* **Firebase Realtime Client**，Firebase 官方的 web/node.js 客戶端，[宣布](https://twitter.com/FirebaseRelease/status/570000737343647744) 他們將於 [2.2.1](https://www.firebase.com/docs/web/changelog.html#section-realtime-client) 開始支援 io.js。
* **Semaphore**，提供持續整合服務商，在 [2015/2/24 平台更新](https://semaphoreapp.com/blog/2015/02/17/platform-update-on-february-24th.html?utm_source=twitter&utm_medium=social&utm_content=platform_update_launch&utm_campaign=platformupdate)中[宣布](https://twitter.com/semaphoreapp/status/570987355005431809)將會支援 io.js。 
