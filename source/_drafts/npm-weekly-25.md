title: "npm 週報 #24 : dist-tag, talking to Microsoft, semicolon trolling"
date: 
tags:
categories: npm 週報
---

[加入週報](https://www.npmjs.com/npm-weekly?utm_campaign=newsletter20150820 "訂閱週報")將會寄送這個給你！

[![npm te ama](https://partners.npmjs.com/weekly/rio-luggage-tag.jpg "npm te ama")](https://docs.npmjs.com/cli/dist-tag?utm_campaign=newsletter20150820 "dist-tag | npm 文件")

## 話說散佈標籤

你或許已經知道安裝 `npm@latest` 會取得 npm 2.13.5 或者安裝 `npm@beta` 會取得 npm 3.3.0。`latest` 及 `beta` 這些標籤是很棒的 **散佈標籤** 示範。

標籤開啟了多個開發流（streams）— 試想 "穩定" 及 "金絲雀（canary）" - 為了能夠在被使用者廣泛地採用之前進行測試，並且讓使用者測試新功能或試試看你的模組是否正常運作。（把 `latest` 視為”我們希望大多數使用者所使用的最新版本“，而非單純的”最新版“）

新增、修改或列舉散步標籤請使用 [dist-tag](https://docs.npmjs.com/cli/dist-tag?utm_campaign=newsletter20150820 "dist-tag | npm 文件").

(Also on the subject of versions: if you missed it, check out [last week’s explainer on semantic versioning](http://blog.npmjs.org/post/126588929320/npm-weekly-24-semver-explained-amazing-videos?utm_campaign=newsletter20150820 "npm weekly #24: semver explained, amazing videos, pizza").)

（以及有關版號主題：如果你錯過了，請見[上週的語意版號解釋一文](http://blog.npmjs.org/post/126588929320/npm-weekly-24-semver-explained-amazing-videos?utm_campaign=newsletter20150820 "npm 週報 #24: semver 說明、驚艷影片、比薩")）

## 提升 Windows 開發體驗

使用 npm registry 的開發者中，超過 40% 的開發者使用 Windows - 這數字已保持將近一年，現在逐月的成長中 - 所以任何提升 Windows 平台的 Node 開發程序有重大影響。

好消息是我們與 [Microsoft’s Visual Studio  團隊](https://channel9.msdn.com/Blogs/Seth-Juarez/Nodejs-Tools-for-Visual-Studio "Node.js Tools for Visual Studio | Seth Juarez | Channel 9")有每月 check-in，以保持溝通暢通並且讓事情做得更棒。同樣的好消息是你也可以協助。你是否也在 Windows 平台上進行開發呢？什麼可以運作？什麼不行？或者你有個希望清單？讓我們知道：[tweet](https://twitter.com/intent/follow?screen_name=npmjs "npmbot (@npmjs) | Twitter") 或 [email](mailto:wombat-cowp@npmjs.com) 或任何其他經常聯絡的到我們的管道皆可。

## 測試 npm 組織

我們收到真實狂熱粉絲的信件，有關我們即將推出的 **組織（Orgs）** 支援，我們希望你也會喜歡。想要在正式推出前試試嗎？[按此加入 beta 測試](http://info.npmjs.com/test-orgs?utm_campaign=newsletter20150820 "幫助我們測試 npm 組織")。

## 協助 Nick 可用性測試

我們仍在持續徵求自願者參與一個 [30 分鐘可用性會期](https://calendly.com/npm/ux "Calendly - Nick Cawthon")，為了形成接下來對模組探索、registry頁面以及npm管理功能的提升。這是一個機會可以影響一個工具，這個工具過去一個月被單獨使用超過20億次，另外也請給 [neat swag](http://shop.npmjs.com?utm_campaign=newsletter20150820 "npm swag store") 評分。你可以幫忙嗎？

## 歡迎另一位新人

來自 Loggly 的 [Angela Eichner](http://twitter.com/siliconvallygrl "SiliconVallyGrl (@SiliconVallyGrl) | Twitter") 在這週加入我們，協助 npm 成為科技、財務及商業界中名號最響亮的名字。如果你也想要協助 npm 成為更大的團隊、有意的自主持有 npm registry 或談論客製解決方案，請[與我們聯絡](mailto:angela@npmjs.com)。

## 讓週報更好

你正在做什麼？誰正在做些啟發世人的事？哪些專案需要幫忙？

告訴我們你對週報有什麼建議。直接回覆這封信件告訴我們你的想法。

## 講授論點：standard

[standard](https://www.npmjs.com/package/standard?utm_campaign=newsletter20150820 "standard") 是一個模組，用來強迫專案有一致的 JavaScript 風格。

[semicolons](https://www.npmjs.com/package/semicolons?utm_campaign=newsletter20150820 "semicolon") 要求分號並且丟出例外，如果每一行結尾沒有分號。

我們絕對不建議一次使用上述兩個風格。

#### 贊助

## 獲得 Node 工作

[Hired](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent") 連接超過 2,500 個審查過的科技企業，13 個主要科技樞紐的 Node 開發者，可能也包含你的科技樞紐。Hired 的開發者平均一週內收到 5 個面試邀請。正在找工作？[試試 Hired](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent").

原文：[npm weekly, #25](http://blog.npmjs.org/post/127157174356/npm-weekly-25-dist-tag-talking-to-microsoft)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
