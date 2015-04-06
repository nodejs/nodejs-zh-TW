title: "io.js 週報 2015.04.03"
date: 2015-04-06 23:49:54
tags:
categories: iojs 週報
---

## v1.6.3 釋出

這週我們有一個新版本釋出 [v1.6.3](https://iojs.org/dist/v1.6.3/)，完整的更新日誌可以在 [Github](https://github.com/iojs/io.js/blob/v1.x/CHANGELOG.md) 找到。

## 值得注意的更動

* **fs:** 某些情況下，`fs.writeFileSync()`、`fs.writeFile()` 的附加模式以及 `fs.writeFileSync()` 會造成損毀，問題被回報在 [#1058](https://github.com/iojs/io.js/issues/1058)，修正在 [#1063](https://github.com/iojs/io.js/pull/1063)（Olov Lassus）。
* **iojs:** 一個“內部模組” API 已被導入，它允許核心代碼在 JavaScript 模組不在公開它們為一個開放API前提下，共享這個模組，這個功能只給核心使用 [#848](https://github.com/iojs/io.js/pull/848)（Vladimir Kurchatkin）。
* **timers:** 兩個次要問題已被修復：
* `Timer.close()` 現在是適當地冪等 [#1288](https://github.com/iojs/io.js/issues/1288)（Petka Antonov）。`setTimeout()` 現在在回呼中呼叫 `unref()` 只會執行一次回呼函式 [#1231](https://github.com/iojs/io.js/pull/1231)（Roman Reiss）。注意：仍然有其他未解決的顧慮，例如 [#1152](https://github.com/iojs/io.js/pull/1152)。
* **Windows:** 加入 “延遲-載入 掛鉤”，用來編譯 Windows 附加元件，這應能緩解 Windows 使用者在 io.js 上使用附加元件的某些問題 [#1251](https://github.com/iojs/io.js/pull/1251)（Bert Belder）。
* **V8:** 次要臭蟲修復，升級 V8 至 4.1.0.27。
* **npm:** 升級 npm 至 2.7.4。詳情請見 npm 的 [CHANGELOG.md](https://github.com/npm/npm/blob/master/CHANGELOG.md#v274-2015-03-20)。

## 已知問題

* 某些存在於計時器與`unref()`仍待解決。請見 [#1152](https://github.com/iojs/io.js/pull/1152)。
* REPL 的代理配對會導致終端凍結 [#690](https://github.com/iojs/io.js/issues/690)
* io.js 不可能編譯成靜態函式庫 [#686](https://github.com/iojs/io.js/issues/686)
* `process.send()` 如同文件所建議並非同步，在 1.0.2 版新增了回歸，請見 [#760](https://github.com/iojs/io.js/issues/760) 及修改 [#774](https://github.com/iojs/io.js/issues/774)
* 當某個DNS查詢正在處理中，呼叫 `dns.setServers()` 會導致程序崩潰在某個失敗的斷言 [#894](https://github.com/iojs/io.js/issues/894)

## 社群更新

* [Scaleway](https://www.scaleway.com/) 提供某些 ARM 資源給 io.js 的 測試/建置 基礎結構。
* Medium 上新發佈的文章，有關與 Node.js 的一致：[幫助我們調和 node.js 及 io.js](https://medium.com/node-js-javascript/help-us-reconcile-node-js-and-io-js-c060a9ec1bd4)
* [Reactive-Extensions/RxJS](https://travis-ci.org/Reactive-Extensions/RxJS/builds/56671837) 新增對 iojs 支援
* 合併 [joyent/nodejs-advisory-board#30](https://github.com/joyent/nodejs-advisory-board/pull/30)
* Mikeal Rogers 正在致力於調和專案生命週期及 io.js 工作小組 [joyent/nodejs-advisory-board#33](https://github.com/joyent/nodejs-advisory-board/pull/33)
* Rod Vagg 開了論壇，有關 Node.js 的一致 [iojs/io.js#1336](https://github.com/iojs/io.js/issues/1336)

## 即將舉行的活動

* [NodeConf](http://nodeconf.com/) 的門票已經開始販售，6/8-9 於加州奧克蘭，NodeConf Adventure 則是 6/11-14 於加州沃克溪農場。
* [CascadiaJS](http://2015.cascadiajs.com/) 門票開賣，時間是 7/8~7/10 於華盛頓州。
* [NodeConf EU](http://nodeconf.eu/) 門票開賣，時間是 9/6~9/9 於愛爾蘭瓦特福。
* [nodeSchool 東京](http://nodejs.connpass.com/event/13182/) 將會在 4/12 於日本東京舉辦。

原文：[io.js Week of April 3rd](https://medium.com/node-js-javascript/io-js-week-of-april-3rd-a4e1fe0c38c1)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
