title: "io.js 週報 2015.03.27"
date: 2015-04-01 15:25:28
tags:
categories: iojs 週報
---


## io.js 1.6.2 釋出

這週我們有一個新版本釋出 [v1.6.2](https://iojs.org/dist/v1.6.2/)，完整的更新日誌可以在 [Github](https://github.com/iojs/io.js/blob/v1.x/CHANGELOG.md) 找到。

## 值得注意的更動

* **Windows:** 再一次，進行中改善可以在測試案例看到結果。如同 v1.4.2 更新日誌，CI 系統及設定問題阻礙了 Windows 測試正確地回報結果，這個問題及代碼似乎已經完全解決。
* **FreeBSD:** 一個影響 io.js/Node.js 的[核心臭蟲](https://lists.freebsd.org/pipermail/freebsd-current/2015-March/055043.html)已經被[發掘](https://github.com/joyent/node/issues/9326)且修補已經出爐避免io.js被影響（Fedor Indutny）[#1218](https://github.com/iojs/io.js/pull/1218)。
* **module:** 現在你可以用 `require('.')` 來取代 `require('./')`，這個考慮是個臭蟲修補（Michaël Zasso）[#1185](https://github.com/iojs/io.js/pull/1185)。
* **v8:** 更新到 4.1.0.25 包含— `max_old_space_size` 數值大於 4096 及支援 Solaris，兩者都已經包含在 io.js。

## 已知問題

* 有個微小的記憶體洩漏可能仍然存在，但是已經是適當地被識別出來，詳細請見 [#1075](https://github.com/iojs/io.js/issues/1075)。
* REPL 的代理配對會導致終端凍結 [#690](https://github.com/iojs/io.js/issues/690)
* io.js 不可能編譯成靜態函式庫 [#686](https://github.com/iojs/io.js/issues/686)
* `process.send()` 如同文件所建議並非同步，在 1.0.2 版新增了回歸，請見 [#760](https://github.com/iojs/io.js/issues/760) 及修改 [#774](https://github.com/iojs/io.js/issues/774)
* 當某個DNS查詢正在處理中，呼叫 `dns.setServers()` 會導致程序崩潰在某個失敗的斷言 [#894](https://github.com/iojs/io.js/issues/894)

## 社群更新

* Node.js 技術管理草案已經提出，可以在這裡[觀看](https://github.com/joyent/nodejs-advisory-board/pull/30)。
* Microsoft Visual Studio 團隊釋出了 Node.js Tools 1.0 for Visual Studio，這次釋出包含豐富的編輯器、代碼補完、互動視窗、進階除錯及效能評測。請見[公告](http://blogs.msdn.com/b/visualstudio/archive/2015/03/25/node-js-tools-1-0-for-visual-studio.aspx)。
* [SPM 監控支援 node.js 及 io.js](http://blog.sematext.com/2015/03/30/nodejs-iojs-monitoring/)，監控可加入效能監測、通知及異常偵測。

## 即將舉行的活動
* [NodeConf](http://nodeconf.com/) 的門票已經開始販售，6/8-9 於加州奧克蘭，NodeConf Adventure 則是 6/11-14 於加州沃克溪農場。
* [CascadiaJS](http://2015.cascadiajs.com/) 門票開賣，時間是 7/8~7/10 於華盛頓州。
* [NodeConf EU](http://nodeconf.eu/) 門票開賣，時間是 9/6~9/9 於愛爾蘭瓦特福。
* [nodeSchool 東京](http://nodejs.connpass.com/event/13182/) 將會在 4/12 於日本東京舉辦。

原文：[io.js Week of March 27th](https://medium.com/node-js-javascript/io-js-week-of-march-27th-9555f36bbb9a)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
