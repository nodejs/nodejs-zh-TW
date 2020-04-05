title: "io.js Week of April 17th"
tags:
categories: iojs 週報
---

## io.js 1.7 釋出

本週我們釋出了io.js v1.7.0 和 v1.7.1 兩個版本，完整的更新日誌可以到 GitHub 上面看。

### 主要更新

* **build:** A syntax error in the Makefile for release builds caused 1.7.0 to be DOA and unreleased. (Rod Vagg) #1421.
* **C++ API:** Fedor Indutny contributed a feature to V8 which has been backported to the V8 bundled in io.js. SealHandleScope allows a C++ add-on author to seal a HandleScope to prevent further, unintended allocations within it. Currently only enabled for debug builds of io.js. This feature helped detect the leak in #1075 and is now activated on the root HandleScope in io.js. (Fedor Indutny) #1395.
* **ARM:** This release includes significant work to improve the state of ARM support for builds and tests. The io.js CI cluster’s ARMv6, ARMv7 and ARMv8 build servers are now all (mostly) reporting passing builds and tests.
* ARMv8 64-bit (AARCH64) is now properly supported, including a backported fix in libuv that was mistakenly detecting the existence of epoll_wait(). (Ben Noordhuis) #1365. ARMv6: #1376 reported a problem with Math.exp() on ARMv6 (including Raspberry Pi). The culprit is erroneous codegen for ARMv6 when using the “fast math” feature of V8. — nofast_math has been turned on for all ARMv6 variants by default to avoid this, fast math can be turned back on with — fast_math. (Ben Noordhuis) #1398. Tests: timeouts have been tuned specifically for slower platforms, detected as ARMv6 and ARMv7. (Roman Reiss) #1366.
* **npm:** 升級 npm 至 2.7.6 版， 請參閱其版本資訊。

### 已知問題

* 在 beforeExit 執行未參考的 timer 仍存在一些問題需要解決 [#1264](https://github.com/iojs/io.js/issues/1264)。
* REPL 的代理配對會導致終端凍結 [#690](https://github.com/iojs/io.js/issues/690)。
* process.send() 如同文件所建議並非同步，在 1.0.2 版新增了回歸，請見 [#760](https://github.com/iojs/io.js/issues/760) 及修改 [#774](https://github.com/iojs/io.js/issues/774)。
* 當某個DNS查詢正在處理中，呼叫 dns.setServers() 會導致程序崩潰在某個失敗的斷言 [#894](https://github.com/iojs/io.js/issues/894)。
* readline 處理跳脫字元會不正確 [#1403](https://github.com/iojs/io.js/issues/1403)

## 社群更新

* Difference between io.js and The Node Foundation iojs/io.js#1416.
* NPM launches private modules and npm inc raises.
* Thoughts of Node.js Foundation on Medium.
* io.js v1.8.0 crypto performance on io.js wiki.
* io.js mention on Oracle’s blog.
* State of the io.js Build April 2015

## 即將舉行的活動

* [JSConf 烏拉圭](http://jsconf.uy/)的門票已經開賣, 時間是 4/24~4/25 於烏拉圭蒙特維多。
* [NodeConf Adventure](http://nodeconf.com/)門票開賣，時間是 6/11~14 於加州沃克溪農場。
* [CascadiaJS](http://2015.cascadiajs.com/)門票開賣，時間是 7/8~7/10 於華盛頓州。
* [NodeConf EU](http://nodeconf.eu/)門票開賣，時間是 9/6~9/9 於愛爾蘭瓦特福。

原文：[io.js Week of April 17th](https://medium.com/node-js-javascript/io-js-week-of-april-17th-e4c6f2db7659)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
