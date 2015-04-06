title: "io.js 週報 2015.04.03"
date: 2015-04-03 09:02:55
tags:
categories: iojs 週報
---
## v1.6.3 Release
This week we had one io.js release v1.6.3, complete changelog can be found on GitHub.

## Notable changes

* **fs:** corruption can be caused by fs.writeFileSync() and append-mode fs.writeFile() and fs.writeFileSync() under certain circumstances, reported in #1058, fixed in #1063 (Olov Lassus).
* **iojs:** an “internal modules” API has been introduced to allow core code to share JavaScript modules internally only without having to expose them as a public API, this feature is for core-only #848 (Vladimir Kurchatkin).
* **timers:** two minor problems with timers have been fixed:
Timer.close() is now properly idempotent #1288 (Petka Antonov). setTimeout() will only run the callback once now after an unref() during the callback #1231 (Roman Reiss). NOTE: there are still other unresolved concerns with the timers code, such as #1152.
* **Windows:** a “delay-load hook” has been added for compiled add-ons on Windows that should alleviate some of the problems that Windows users may be experiencing with add-ons in io.js #1251 (Bert Belder).
* **V8:** minor bug-fix upgrade for V8 to 4.1.0.27.
* **npm:** upgrade npm to 2.7.4. See npm CHANGELOG.md for details.

## Known issues

* Some problems exist with timers and unref() still to be resolved. See #1152.
* Possible small memory leak(s) may still exist but have yet to be properly identified, details at #1075.
* Surrogate pair in REPL can freeze terminal #690
* Not possible to build io.js as a static library #686
* process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774
* Calling dns.setServers() while a DNS query is in progress can cause the process to crash on a failed assertion #894

## Community Updates

* Scaleway provides some ARM resources for the iojs test/build infrastructure.
* New post on Medium about Node.js reconciliation: Help us reconcile node.js and io.js
* Added support for iojs in Reactive-Extensions/RxJS
* joyent/nodejs-advisory-board#30 merged
* Mikeal Rogers is working on reconciling Project Lifecycle and io.js WGs joyent/nodejs-advisory-board#33
* Rod Vagg opened the discussion forum about Node.js reconciliation in iojs/io.js#1336

## Upcoming Events

* NodeConf tickets are on sale, June 8th and 9th at Oakland, CA and NodeConf Adventure for June 11th — 14th at Walker Creek Ranch, CA
* CascadiaJS tickets are on sale, July 8th — 10th at Washington State
* NodeConf EU tickets are on sale, September 6th — 9th at Waterford, Ireland
* nodeSchool tokyo will be held in April 12th at Tokyo, Japan

原文：[io.js Week of April 3rd](https://medium.com/node-js-javascript/io-js-week-of-april-3rd-a4e1fe0c38c1)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
