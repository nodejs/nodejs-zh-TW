title: "io.js Week of April 24th"
tags:
categories: iojs 週報
---

## io.js 1.8.1 release

This week we had one io.js release v1.8.1, complete changelog can be found on GitHub.

### Notable changes

* **NOTICE:** Skipped v1.8.0 due to problems with release tooling. See #1436 for details.
* **build:** Support for building io.js as a static library (Marat Abdullin) #1341
* **deps:** Upgrade openssl to 1.0.2a (Shigeki Ohtsu) #1389
* Users should see performance improvements when using the crypto API. See here for details.
* **npm:** Upgrade npm to 2.8.3. See the release notes for details. Includes improved git support.
* **src:** Allow multiple arguments to be passed to process.nextTick (Trevor Norris) #1077
* **module:** The interaction of require(‘.’) with NODE_PATH has been restored and deprecated. This functionality will be removed at a later point. (Roman Reiss) #1363

### Known issues

* Some problems with unreferenced timers running during beforeExit are still to be resolved. See #1264.
* Surrogate pair in REPL can freeze terminal #690
* process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774
* Calling dns.setServers() while a DNS query is in progress can cause the process to crash on a failed assertion #894
* url.resolve may transfer the auth portion of the url when resolving between two full hosts, see #1435.
* readline: split escapes are processed incorrectly, see #1403

## Community Updates

* Fedor Indutny opened discussion about removing TLS newSession and resumeSession event. iojs/io.js#1462
* Proposal to change the C HTTP parser JS HTTP parser here
* NPM founder talks about io.js at InfoWorld
* Proposal to add mikeal, mscdex, shigeki as new TC members. iojs/io.js#1483

## Upcoming Events

* JSConf Uruguay tickets are on sale, April 24th & 25th at Montevideo, Uruguay
* NodeConf Adventure tickets are on sale, June 11th — 14th at Walker Creek Ranch, CA
* CascadiaJS tickets are on sale, July 8th — 10th at Washington State
* NodeConf EU tickets are on sale, September 6th — 9th at Waterford, Ireland

原文：[io.js Week of April 24th](https://medium.com/node-js-javascript/io-js-week-of-april-24th-bd67dcbdfa65)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
