title: "io.js 週報 2015.04.10"
tags:
categories: iojs 週報
---
## io.js 1.6.4 release

這週我們有一個 io.js 釋出版本 [v1.6.4](https://iojs.org/dist/v1.6.4/)，完整的更新項目可以在 [GitHub](https://github.com/iojs/io.js/blob/v1.x/CHANGELOG.md) 上找到。

### 主要更新

* **npm:** npm 升級到 2.7.5，細節可以參閱 [npm CHANGELOG.md](https://github.com/npm/npm/blob/master/CHANGELOG.md#v275-2015-03-26)。這個版本包含了兩個重要的安全性更新。
* **openssl:** OpenSSL 1.0.2a [#1325](https://github.com/iojs/io.js/pull/1325) (Shigeki Ohtsu) 前期準備工作已經完成。更多細節可以參考 [#589](https://github.com/iojs/io.js/issues/589)。
* **timers:** 未被參考 timers 所造成記憶體洩漏的問題已經被修復，包含一些 timers 相關的問題 [#1330](https://github.com/iojs/io.js/pull/1330) (Fedor Indutny)。這些修復了在 [#1075](https://github.com/iojs/io.js/issues/1075) 回報的問題。
* **android:** 現在已經可以編譯讓 Android 以及相關設備使用的 io.js 版本 [#1307](https://github.com/iojs/io.js/pull/1307) (Giovanny Andres Gongora Granada)。

### 已知問題

* Some problems with unreferenced timers running during beforeExit are still to be resolved. See #1264.
* Surrogate pair in REPL can freeze terminal #690
* Not possible to build io.js as a static library #686
* process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774
* Calling dns.setServers() while a DNS query is in progress can cause the process to crash on a failed assertion #894

### 社群更新

* Node 基金會的開發策略草案在[這邊](https://github.com/jasnell/dev-policy)。
* io.js [支援](https://twitter.com/rvagg/status/586050873349939201) ARMv8 / ARM64 平台。
* 持續著 [node.js/io.js](https://github.com/jasnell/dev-policy) 新開發方針的工作。
* [星期三](https://www.youtube.com/watch?v=OjlK8k10oyo)的 TC 會議。

### 即將舉行的活動

* [JSConf 烏拉圭](http://jsconf.uy/)的門票已經開賣，時間時 4/24~4/25 於烏拉圭蒙特維多。
* [NodeConf Adventure](http://nodeconf.com/) 則是 6/11-14 於加州沃克溪農場。
* [CascadiaJS](http://2015.cascadiajs.com/) 門票開賣，時間是 7/8~7/10 於華盛頓州。
* [NodeConf EU](http://nodeconf.eu/) 門票開賣，時間是 9/6~9/9 於愛爾蘭瓦特福。
* [nodeSchool 東京](http://nodejs.connpass.com/event/13182/) 將會在 4/12 於日本東京舉辦。

原文：[io.js Week of April 10th](https://medium.com/node-js-javascript/io-js-week-of-april-10th-cbf6cf32409)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
