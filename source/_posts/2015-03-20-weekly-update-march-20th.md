title: "io.js 週報 2015.03.20"
date: 2015-03-20 09:02:55
tags:
categories: iojs 週報
---

io.js 1.6.1, openssl 升級, 社群活動及其他事項。

這週我們釋出兩個 io.js 版本，[v1.6.1](https://iojs.org/dist/v1.6.1/) 及 [v1.6.0](https://iojs.org/dist/v1.6.0/)，完整的更新項目可以在 [Github](https://github.com/iojs/io.js/blob/v1.x/CHANGELOG.md) 上找到。

## io.js 1.6 釋出

### 1.6.1

* **path:** path.resolve()新增型別檢查 [#1153](https://github.com/iojs/io.js/pull/1153)，不包含某些特殊案例，特別是 path.dirname(undefined)。已經放鬆 path.dirname()、path.basename() 以及 path.extname() 的型別檢查（Colin Ihrig）[#1216](https://github.com/iojs/io.js/pull/1216)。
* **querystring:** 對於 querystring.parse() 以及 querystring.stringify() 所做的最佳化 [#847](https://github.com/iojs/io.js/pull/847) 妨礙了數字被 querystring.escape() 正確轉換，導致測試出現死角 [#1208](https://github.com/iojs/io.js/issues/1208)。這個臭蟲以及測試都已經被修復 (Jeremiah Senkpiel) [#1213](https://github.com/iojs/io.js/pull/1213)。

### 1.6.0

* **node:** 一個新的 -r 或 — require 命令列參數可以用來在起始階段預先載入模組 (Ali Ijaz Sheikh) [#881](https://github.com/iojs/io.js/pull/881)。
* **querystring:** parse() 及 stringify() 效能更快了 (Brian White) [#847](https://github.com/iojs/io.js/pull/847)。
* **http:** http.ClientRequest#flush() 方法已被棄置，取而代之的是 http.ClientRequest#flushHeaders()，與 Node.js v0.12 的改變相同 [joyent/node#9048](https://github.com/joyent/node/pull/9048) (Yosuke Furukawa) [#1156](https://github.com/iojs/io.js/pull/1156)。
* **net:** 允許 server.listen() 接受字串作為 port 的參數，例如 { port: “1234" } 以符合 [joyent/node#9268](https://github.com/joyent/node/pull/9268) 中 net.connect 接受相容格式的參數 (Ben Noordhuis) [#1116](https://github.com/iojs/io.js/pull/1116)。
* **tls:** 回報的記憶體洩漏問題有更進一步的處理，儘管在這問題中顯示出這是個次要問題，可在 [#1075](https://github.com/iojs/io.js/issues/1075) 追蹤問題。
* **v8:** 修補一個整數溢位的問題，當 max_old_space_size 的數值大於 4096 的時候 (Ben Noordhuis) [#1166](https://github.com/iojs/io.js/pull/1166)。
* **platforms:** io.js CI 回報已經通過 **FreeBSD** 以及 **SmartOS** (Solaris)。
* **npm:** 升級至 2.7.1，細節請參閱 [npm CHANGELOG.md](https://github.com/npm/npm/blob/master/CHANGELOG.md#v271-2015-03-05)

### 已回報問題

* 可能存在與 TLS 相關的記憶體洩漏問題，細節在 [#1075](https://github.com/iojs/io.js/issues/1075)。
* Surrogate pair in REPL can freeze terminal #690
* io.js 無法編譯成靜態函式庫 [#686](https://github.com/iojs/io.js/issues/686)
* process.send() 不是文件所建議的非同步，降級問題發生於 1.0.2 版，詳情請見 [#760](https://github.com/iojs/io.js/issues/760) 以及修正 [#774](https://github.com/iojs/io.js/issues/774)
* 當 DNS 查詢進行中的時候呼叫 dns.setServers() 將會導致程序崩潰 [#894](https://github.com/iojs/io.js/issues/894)

## 社群更新
* browserify 開始支援 io.js，可以到[這裡](https://twitter.com/yosuke_furukawa/status/577150547850969088)看到公告。
* express.js 加入對 io.js 的支援。
* 在過去的兩週，我們能夠訪問來自 Joyent 的硬件，並且引入了一個 V8 的補丁，所以可以成功構建 io.js。在那之後我們致力通過 [SmartOS](https://github.com/iojs/build/pull/64) 和 [FreeBSD](https://github.com/iojs/io.js/pull/1167) 上的測試，經過這兩天測試通過了，這要歸功於構建團隊和 [Johan Bergström](https://github.com/jbergstroem)。
* [Petka Antonov](https://github.com/petkaantonov) 提出在 io.js 中實作 workers（需要加上實驗旗標來啟用），你可以到[這裡](https://github.com/iojs/io.js/pull/1159)參與討論。
* io.js 把 openssl [升級](https://github.com/iojs/io.js/pull/1206)到 1.0.1m。

## 即將舉行的活動
* [NodeConf](http://nodeconf.com/) 的門票已經開始販售，6/8-9 於加州奧克蘭，NodeConf Adventure 則是 6/11-14 於加州沃克溪農場。
* [CascadiaJS](http://2015.cascadiajs.com/) 門票開賣，時間是 7/8~7/10 於華盛頓州。
* [NodeConf EU](http://nodeconf.eu/) 門票開賣，時間是 9/6~9/9 於愛爾蘭瓦特福。

原文：[io.js Week of March 20th](https://medium.com/node-js-javascript/io-js-1-6-release-1df38cf64e6c)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
