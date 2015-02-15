title: npm 週報 #5
date: 2015-02-15 12:00:00
tags:
categories: npm 週報
---

你希望可以[直接收到](https://www.npmjs.com/npm-weekly) npm 最新更新的消息嗎？

### CLI 有什麼更新

![](http://media.tumblr.com/5702701b335f0738fc9497aec482cb42/tumblr_inline_njqav2FNuI1t68bpr.png)

你或許有注意到從 npm@2.6.0 之後出現的警告訊息。

我們將會在 npm@3 的時候移除 `engineStrict` 這個 package.json 設定，所以你在 npm@2.6.0 之後就會看到關於這個變更的警告訊息。你仍然可以在你的 .npmrc 中設定 engine，因為在套件中設定 engine 的限制從來就沒有正常的運行，所以我們決定把它移除。

我們也會在 npm@3 改變 peerDependencies 的行為。我們將不再自動下載 peer dependency，取而代之的是，我會將會顯示警告訊息提醒你 peer dependency 沒有被安裝。所以你必須要自行處理 peerDependencies 的衝突，從長遠來看，這個改變將會減少套件相依性造成的棘手問題。

### npm@3 將會有什麼新改變

npm@3 之後，你的 node_modules 目錄將更為扁平，所有的依賴套件以及它們各自依賴的套件 (以及更上層的依賴套件) 都將置於第一層。只有他們發生衝突的時候，才會移到下一層目錄。此一改變將大大改善 Windows 使用者。

### 如何使用 npm

![](http://media.tumblr.com/b3f53c6a6a8c7d5862a95fda7a94f7de/tumblr_inline_njqazvJorm1t68bpr.png)

npm 有了一個新的互動式教學 - [how-to-npm](https://www.npmjs.com/package/how-to-npm)。學習如何發佈並更新套件到 npm，以及其他維護的工作。不需要擔心發佈到公用的套件庫之中，它只會上傳到一個運行在你電腦上假的套件庫。

### Node 基金會

Joyent 在這星期宣布他們將會籌組 Node.js 基金會。這對於支持 JavaScript 社群，吸引更多企業投資邁向了一大步。這一切尚處於早期階段，但是我們期待這個舉動對於 Node.js 專案以及 JavsScript 社群普及的影響。

原文：[npm Weekly, #5](http://blog.npmjs.org/post/110924823920/npm-weekly-5)，作者：[npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
