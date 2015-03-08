title: "io.js 週報 2015.02.27"
tags:
categories: iojs 週報
---

Buffer.indexOf()、Tessel 2 以及更多消息。

# io.js 1.5.0 釋出

[@rvagg](https://github.com/rvagg) 在 3/6（五）釋出了 io.js [v1.5.0](https://iojs.org/dist/latest/)。可以在 [Github](https://github.com/iojs/io.js/blob/v1.x/CHANGELOG.md) 上找到完整的變更日誌。

## 主要更動

* **buffer:** 提供 Buffer#indexOf() 方法，啟發自 [Array#indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)。接受 String、Buffer 以及 Number 型態。Strings 將視為 UTF8。 (Trevor Norris) [#561](https://github.com/iojs/io.js/pull/561)

* **fs:** 「fs」 的方法不再對 options 物件屬性執行 hasOwnProperty() 檢查，以允許 options 物件擁有 apply prototype 的屬性。 (Jonathan Ong) #635

* **tls:** 一個由 PayPal 回報，可能是 TLS 記憶體洩漏的問題。近期對於 **stream_wrap** 的更動可能造成問題。問題回報於 [#1078](https://github.com/iojs/io.js/pull/1078)，你可以在 [#1075](https://github.com/iojs/io.js/issues/1075) 得知目前的進展。(Fedor Indutny)

* **npm:** npm 升級至 2.7.0，細節請參閱[更新項目](https://github.com/npm/npm/blob/master/CHANGELOG.md#v270-2015-02-26)，其中解釋了為什麼這個原本可能是主要版號升級變成了次要版號。

* **TC:** Colin Ihrig (@cjihrig) 從 TC 退出，因為他希望可以放更多心力在程式撰寫上並減少開會時間。

## 已知的問題

* 可能與 TLS 相關的記憶體洩漏，細節請參閱 [#1075](https://github.com/iojs/io.js/issues/1075)。

* Windows 仍舊有使用者回報存在一些測試錯誤的情形，我們正優先追查這些問題的原因。細節請參閱 [#1005](https://github.com/iojs/io.js/issues/1005)。

* 在 REPL 中代理對 (Surrogate pair) 會凍結終端 [#690](https://github.com/iojs/io.js/issues/690)

* 不能編譯 io.js 為靜態函式庫 [#686](https://github.com/iojs/io.js/issues/686)

* 1.0.2 重新加入的 process.send() 不如文件上所說為同步地，參閱 [#760](https://github.com/iojs/io.js/issues/760)  和 [#774](https://github.com/iojs/io.js/issues/774) 的修補

# 社群消息

* 聽到 io.js 與 最新版 node.js 沒有受 [FREAK Attack](https://freakattack.com/) 影響，應該鬆一口氣吧。你正使用著 io.js 或最新版的 node.js 對吧？

* Walmart 贊助了建構的機器來運行 io.js Jenkins 持續整合系統。[@iojs/build](https://github.com/orgs/iojs/teams/build) 團隊開始著手進行 SunOS 版本（正如你可以從 node.js 取得的一樣）。不過在此之前，有一個 V8 的臭蟲（[iojs/io.js#1079](https://github.com/iojs/io.js/pull/1079)）必須要先修復。

* 此外，我們也在此感謝以下的企業，對於 io.js 提供硬體以及相關的技術/支援/工程師的協助：

* Digital Ocean (主要是 Linux) Rackspace (主要是 Windows) Voxer (OS X 和 FreeBSD) NodeSource (ARMv6 & ARMv7) Linaro (ARMv8) Walmart (SmartOS / Solaris)

* io.js 社群很努力的進行本地化的工作。目前有超過 20 種語系內容發佈到 [io.js.org](http://iojs.org/) 以及 i18n 社群網站上。此外，i18n 的連結也已經加到網站的頁面底部便與使用。你懷念自己的語系嗎？[來協助我們吧！](https://github.com/iojs/website/blob/master/TRANSLATION.md)

* 既然提到翻譯，io.js [路徑圖的簡報](http://roadmap.iojs.org/)已經更新並加上其中語系的連結。

* PayPal 做了一個實驗來比較 [Kappa](https://www.npmjs.com/package/kappa) 運行在 io.js、node.js 0.12，以及 node.js 0.10。PayPal 團隊也發現了可能造成記憶體洩漏的問題。一開始的問題回報在 [#1078](https://github.com/iojs/io.js/pull/1078)，後續的處理在 [#1075](https://github.com/iojs/io.js/issues/1075)。

* [**NodeSource**](http://nodesource.com/) 開始提供 Ubuntu/Debian 的[程式包](https://nodesource.com/blog/nodejs-v012-iojs-and-the-nodesource-linux-repositories)，正如給 RHEL/Fedora 一樣。

* io.js [Docker版本](https://registry.hub.docker.com/u/library/iojs/)，是一、二月中，十三個新加入的 [Docker 官方容器](http://blog.docker.com/2015/03/thirteen-new-official-repositories-added-in-january-and-february/)的其中之一。

* NodeBots 以及 IoT 的人們應該會很高興聽到這個剛發佈的消息 - [**Tessel2**](http://blog.technical.io/post/112787427217/tessel-2-new-hardware-for-the-tessel-ecosystem) 將[原生支援 io.js](http://blog.technical.io/post/112888410737/moving-faster-with-io-js)。

* [**@maxbeatty**](https://twitter.com/maxbeatty) 正忙於建置新版的 [jsperf.com](http://jsperf.com/) 後端，運行於 io.js 以及完全開放原始碼。歡迎貢獻者！

* 部落格: @eranhammer 寫了一篇名為 [The Node Version Dilemma](http://hueniverse.com/2015/03/02/the-node-version-dilemma/) 的文章，其中討論了許多不同版本的 node.js / io.js，建議該使用哪個版本及在何時使用。

# 對 io.js 的支援增加

* [**scrypt**](https://npmjs.com/scrypt) 已經支援 io.js，細節可以參閱這個 [Github Issue](https://github.com/barrysteyn/node-scrypt/issues/39)。
* [**proxyquire**](https://github.com/thlorenz/proxyquire) 發佈 v1.3.2 並支援 iojs。

原文：[io.js Week of March 6th](https://medium.com/node-js-javascript/io-js-week-of-march-6th-2f9344688277)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
