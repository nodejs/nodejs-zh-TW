title: "npm 週報 #21 : npm 3 更新 + react.js 元件工具"
tags:
categories: npm 週報
---

[訂閱](https://www.npmjs.com/npm-weekly) npm 週報

## npm 3 beta 測試者們

如果你是位 npm@3 beta 測試者，在此通知：下載 npm@3 最新及預備版（next versions）的標籤已經更改。現在請改用 `npm@3.x-next` 及 `npm@3.x-latest`。詳細請見 [CHANGELOG](https://github.com/npm/npm/blob/master/CHANGELOG.md)。同樣地，感謝各位給予我們的協助消滅各種臭蟲！

當 [Forrest](https://twitter.com/othiym23) 離開，[Kat](https://twitter.com/maybekatz) 加入許多東西到 npm@2，詳細請見 [CHANGELOG](https://github.com/npm/npm/blob/master/CHANGELOG.md#v2130-2015-07-02)。

## npm 3 beta 給 windows 用戶帶來好消息

[Rebecca](https://twitter.com/ReBeccaOrg) [告訴 InfoQ](http://www.infoq.com/news/2015/06/npm) 有關 npm@3，特別是安裝程序的改變將會幫助 Windows 用戶。

## 私有模組的驗屍

我們已經透過 email 警示私有模組的用戶們，萬一你沒有收到，再次通知，上週有個私有模組的安全性議題。私有模組的 Metadata 洩漏，但不包括整包內容以及私人用戶訊息。詳細請見[驗屍](http://status.npmjs.org/incidents/6r2jr0dd9kd5)一文。

##  react podcast 廣播有關 webpack 對上 browserify

如果你正在使用 React.js 元件，你可能會想聽 React Podcast 廣播 [Webpack 對上 Browserify](http://reactpodcast.com/2015/06/webpack-vs-browserify/)，用來管理前端模組相依的工具。長度大約 7 分鐘。

相同主題，[Lin](https://twitter.com/linclark) 在上個月 jQuerySF 上說明了[如何在 npm 使用 Browserify（及 Babel）](https://youtu.be/Tjwm9yPzBGg?t=6913)來管理前端模組，並且將會在八月的 [React Rally](http://www.reactrally.com/) 演講有關 Webpack。

## npm 現在是我的片段資料庫

[Sindre Sorhus](https://twitter.com/sindresorhus) 在他的 AMA（問我任何事）說明了他如何使用 npm 作為一種用來[捕獲（capture）他的程式碼片段](https://github.com/sindresorhus/ama/issues/10#issuecomment-117766328)的方式。

說明了當你可以 require 它的時後，為何要複製貼上，以及有個清楚意圖的益處。當你在片段中修正一個臭蟲，你只需要更新一個模組，而不是手動修正所有用到片段的地方。

原文：[npm Weekly, #21](http://blog.npmjs.org/post/123564120105/npm-weekly-21-npm-3-updates-react-js)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
