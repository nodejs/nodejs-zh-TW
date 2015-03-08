title: "io.js 週報 2015.03.06"
date: 2015-03-08 06:00:00
tags:
categories: iojs 週報
---

# io.js 3/6 週報
Buffer.indexOf()、Tessel 2 以及更多消息。

# io.js 1.5.0 釋出
On Friday, March 6th, @rvagg released io.js v1.5.0. The complete change log can be found on GitHub.
[@rvagg](https://github.com/rvagg) 在 3/6（五）釋出了 io.js [v1.5.0](https://iojs.org/dist/latest/)。完整的更新項目可以在 [Github](https://github.com/iojs/io.js/blob/v1.x/CHANGELOG.md) 上找到。

## 主要更動

* **buffer:** 提供 Buffer#indexOf() 方法，啟發自 [Array#indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)。接受 String, Buffer 以及 Number 型態. Strings 將視為 UTF8。 (Trevor Norris) [#561](https://github.com/iojs/io.js/pull/561)

* **fs:** options object properties in ‘fs’ methods no longer perform a hasOwnProperty() check, thereby allowing options objects to have prototype properties that apply. (Jonathan Ong) #635

* **tls:** A likely TLS memory leak was reported by PayPal. Some of the recent changes in stream_wrap appear to be to blame. The initial fix is in #1078, you can track the progress toward closing the leak at #1075 (Fedor Indutny).

* **npm:** npm 升級至 2.7.0，細節請參閱[更新項目](https://github.com/npm/npm/blob/master/CHANGELOG.md#v270-2015-02-26)，其中解釋了為什麼這個原本可能是主要版號升級變成了次要版號。

* **TC:** Colin Ihrig (@cjihrig) 從 TC 退出，因為他希望可以放更多心力在程式撰寫上並減少開會時間。

## 已知的 Issue 

* 可能與 TLS 相關的記憶體洩漏，細節請參閱 [#1075](https://github.com/iojs/io.js/issues/1075)。

* Windows 仍舊有使用者回報存在一些測試錯誤的情形，我們正優先追查這些問題的原因。細節請參閱 [#1005](https://github.com/iojs/io.js/issues/1005)。

* Surrogate pair in REPL can freeze terminal #690

* Not possible to build io.js as a static library #686

* process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774

# 來自社群的消息

* 聽到 io.js 與 最新版 node.js 沒有受 [FREAK Attack](https://freakattack.com/) 影響，應該鬆一口氣吧。你正使用著 io.js 或最新版的 node.js 對吧？

* Walmart is now sponsoring a build machine for the io.js Jenkins CI system. The @iojs/build team is working on creating io.js SunOS binaries (like you can get from nodejs.org). A V8 fix (iojs/io.js#1079) needs to be landed first before more progress can be made.

* We would also like to thank the following companies for contributing hardware and related technology/support/engineering for io.js builds:

* Digital Ocean (mainly Linux) Rackspace (mainly Windows) Voxer (OS X and FreeBSD) NodeSource (ARMv6 & ARMv7) Linaro (ARMv8) Walmart (SmartOS / Solaris)

* The io.js community has been hard at work on the internationalization of all of its content. There are now over 20 active languages published on iojs.org and i18n community sites. Additionally, i18n links (iojs/website#258) have been added to the website footer for easy access. Are we missing your language? Help us add it!

* Speaking of translations, the io.js roadmap presentation has been updated to link to other language versions.

* It seems that PayPal is running an experiment comparing Kappa on io.js vs node.js 0.12 vs node.js v0.10. The PayPal team identified a likely TLS memory leak. Initial fix is in #1078 and progress towards closing is in #1075

* NodeSource is now providing io.js Linux binary packages for Ubuntu/Debian as well as RHEL/Fedora distributions.

* The io.js Docker build is one of thirteen new official Docker repositories added in January and February.

* NodeBots 以及 IoT 的人們應該會很高興聽到這個剛發佈的消息 - [**Tessel2**](http://blog.technical.io/post/112787427217/tessel-2-new-hardware-for-the-tessel-ecosystem) 將[原生支援 io.js](http://blog.technical.io/post/112888410737/moving-faster-with-io-js)。

* [**@maxbeatty**](https://twitter.com/maxbeatty) 正忙於建置新版的 [jsperf.com](http://jsperf.com/) 後端，運行於 io.js 以及完全開放原始碼。歡迎貢獻者！

* 部落格: @eranhammer 寫了一篇名為 [The Node Version Dilemma](http://hueniverse.com/2015/03/02/the-node-version-dilemma/) 的文章，其中討論了許多不同版本的 node.js / io.js，建議該使用哪個版本及在何時使用。

# 對 io.js 的支援增加
* [**scrypt**](https://npmjs.com/scrypt) 已經支援 io.js，細節可以參閱這個 [Github Issue](https://github.com/barrysteyn/node-scrypt/issues/39)。
* [**proxyquire**](https://github.com/thlorenz/proxyquire) 發佈 v1.3.2 並支援 iojs。