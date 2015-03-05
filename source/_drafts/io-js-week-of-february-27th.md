title: "io.js 週報 2015.02.27"
tags:
categories: iojs 週報
---

_注意：版本 **1.4.0** 已經編譯完成並加上標籤但是尚未釋出。在過程中一個 libuv 的臭蟲被發現所以這次的釋出將被棄置，我們將會提升版本號到 1.4.1 以避免造成混淆。_

## 主要更動

* **process** / **promises**：每當有 `Promise` 被回絕而且沒有在 `Promise` 上附加錯誤處理程式，現在 `process` 會在該輪的事件迴圈內發出一個 `'unhandledRejection'` 事件。而每當 `Promise` 被回絕而且它有附加錯誤處理程式時，現在它會在下一輪事件迴圈發出一個 `'rejectionHandled'` 事件。  [#758](https://github.com/iojs/io.js/pull/758) (Petka Antonov)
* **streams**：你現在可以使用正規的 stream 作為 `tls.connect()` 的底層 socket [#926](https://github.com/iojs/io.js/pull/926) (Fedor Indutny)
* **http**：當 `http.ClientRequest` 被客戶端棄置的時候，會發出一個新的 `'abort'` 事件。 [#945](https://github.com/iojs/io.js/pull/945) (Evan Lucas)
* **V8**：升級 V8 版本到 4.1.0.21。包含一個 embargoed 的修補，當 embargo 被解除時應該可以得到細節的資訊。有一個 破壞性的 ABI 變更不會在這次的升級之中，可能會在 io.js 合入 V8 4.2 版本的時候加上去。參閱 [#952](https://github.com/iojs/io.js/pull/952) 的討論。
* **npm**：升級 npm 版本到 2.6.0。包含支援新註冊系統和為了 `npm@3` 準備的功能。參閱 [npm CHANGELOG.md](https://github.com/npm/npm/blob/master/CHANGELOG.md#v260-2015-02-12) 以了解細節。總結：
  * [#5068](https://github.com/npm/npm/issues/5068) 添加新的登出指令，並讓它對基於 bearer 和 basic 認證的客戶端有用。
  * [#6565](https://github.com/npm/npm/issues/6565) 提醒 `peerDependency` 行為改變了並添加了提醒到文件。
  * [#7171](https://github.com/npm/npm/issues/7171) 提醒 `package.json` 中的 `engineStrict` 屬性將會在下一個 npm 主版號移除 (即將到來！)
* **libuv**：升級版本到 1.4.2。參閱 [libuv 變更日誌](https://github.com/libuv/libuv/blob/v1.x/ChangeLog) 以了解修補的細節。

# ARM 提供 io.js 在 ARMv8 上的支援

ARM 已經聯繫 io.js 建置工作小組的領導者 Rod Vagg，提供他們對 io.js 專案的支援。 ARM 和他們的硬體合作夥伴已經上了軌道讓 ARMv8 成為可運作的伺服器平台，伺服器端 JavaScript 靈活的特性也讓他們完美契合地運行在新的 ARM 上面。

因為 ARMv8 已經被行動設備製造商採用，新版本的 V8 已經有很好的支援。因為 V8 在 Android 中的角色很關鍵，io.js 非常適合去追蹤它的支援情況，更甚至貢獻給 v8 會讓我們與 V8 團隊有新的關係。

從 io.js 專案開始的時候，Rod 一直倡導 ARM 對於 io.js、物聯網、愛好者和伺服器使用的角色。我們已經在每次釋出對裝置做 ARMv6 的建置，例如：Raspberry Pi。並且對許多受歡迎的裝置做 ARMv7 的建置 (包括基於 ARM 的雲端平台 Online Labs，也對 io.js 提供幫助)。ARMv8 邏輯繼承這些，但也有令人興奮的潛力來建置伺服器端應用程式，特別是它給予新的 64-bit 支援。

建置團隊被獲准使用 Linaro ARMv8 伺服器叢集，正在進行跟 io.js CI 平台的整合，這最終應該能導向正規的 ARMv8 二進位檔釋出。

# 社群更新

* [**和解提案**](https://github.com/iojs/io.js/issues/978)：io.js 著手開始進行對於 Node.js 基金會的和解草案。目前還是初期草案階段，因此來自社群的意見是非常重要的，請大家踴躍反應。
* **New internal C++ Streams API**：一個全新的 [C++ Streams API] 在這週增加到 io.js 之中，允許你可以將 TLS stream 包裝成另一個 TLS stream。
* **io.js 路徑圖**：[路徑圖](https://github.com/iojs/io.js/blob/v1.x/ROADMAP.md) 是對 io.js 未來的規劃。它描述關於穩定性策略的規劃以及列出 io.js 的當務之急。
* **路徑圖的投影片已經完成等待翻譯**：一系列之於 io.js 路徑圖的投影片已經[完成可以進行翻譯](https://github.com/iojs/roadmap/issues/18)。你覺得你可以向周遭的群體做簡報嗎？留下你的意見，我們會與你協作幫你預備好簡報！
* **Microsoft io.js How-To for Azure Websites**: 微軟 發佈一篇關於他們 Azure 平台的[入門教學](http://azure.microsoft.com/en-us/documentation/articles/web-sites-nodejs-iojs/)，描述如何在 Azure 上使用 io.js。
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
