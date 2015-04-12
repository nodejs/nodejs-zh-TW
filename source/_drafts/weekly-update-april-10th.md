title: "io.js 週報 2015.04.10"
date: 2015-04-10 09:02:55
tags:
categories: iojs 週報
---
## io.js 1.6.4 release

This week we had one io.js release v1.6.4, complete changelog can be found on GitHub.

### Notable changes

* **npm:** upgrade npm to 2.7.5. See npm CHANGELOG.md for details. Includes two important security fixes.
openssl: preliminary work has been done for an upcoming upgrade to OpenSSL 1.0.2a #1325 (Shigeki Ohtsu). See #589 for additional details.
* **timers:** a minor memory leak when timers are unreferenced was fixed, alongside some related timers issues #1330 (Fedor Indutny). This appears to have fixed the remaining leak reported in #1075.
* **android:** it is now possible to compile io.js for Android and related devices #1307 (Giovanny Andres Gongora Granada).

### Known issues

* Some problems with unreferenced timers running during beforeExit are still to be resolved. See #1264.
* Surrogate pair in REPL can freeze terminal #690
* Not possible to build io.js as a static library #686
* process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774
* Calling dns.setServers() while a DNS query is in progress can cause the process to crash on a failed assertion #894

### Community Updates

* Node Foundation dev policy draft is here
* ARMv8 / ARM64 support on io.js
* Continued work on a new dev policy for node.js/io.js
* TC call from Wednesday

### Upcoming Events

* JSConf Uruguay tickets are on sale, April 24th & 25th at Montevideo, Uruguay
* NodeConf Adventure tickets are on sale, June 11th — 14th at Walker Creek Ranch, CA
* CascadiaJS tickets are on sale, July 8th — 10th at Washington State
* NodeConf EU tickets are on sale, September 6th — 9th at Waterford, Ireland
* nodeSchool Tokyo will be held in April 12th at Tokyo, Japan

原文：[io.js Week of April 10th](https://medium.com/node-js-javascript/io-js-week-of-april-10th-cbf6cf32409)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
