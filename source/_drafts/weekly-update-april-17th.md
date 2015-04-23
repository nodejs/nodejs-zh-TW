title: "io.js Week of April 17th"
tags:
categories: iojs 週報
---

## io.js 1.7 releases

This week we had two io.js releases v1.7.0 and v1.7.1, complete changelog can be found on GitHub.

### Notable changes

* **build:** A syntax error in the Makefile for release builds caused 1.7.0 to be DOA and unreleased. (Rod Vagg) #1421.
* **C++ API:** Fedor Indutny contributed a feature to V8 which has been backported to the V8 bundled in io.js. SealHandleScope allows a C++ add-on author to seal a HandleScope to prevent further, unintended allocations within it. Currently only enabled for debug builds of io.js. This feature helped detect the leak in #1075 and is now activated on the root HandleScope in io.js. (Fedor Indutny) #1395.
* **ARM:** This release includes significant work to improve the state of ARM support for builds and tests. The io.js CI cluster’s ARMv6, ARMv7 and ARMv8 build servers are now all (mostly) reporting passing builds and tests.
* ARMv8 64-bit (AARCH64) is now properly supported, including a backported fix in libuv that was mistakenly detecting the existence of epoll_wait(). (Ben Noordhuis) #1365. ARMv6: #1376 reported a problem with Math.exp() on ARMv6 (including Raspberry Pi). The culprit is erroneous codegen for ARMv6 when using the “fast math” feature of V8. — nofast_math has been turned on for all ARMv6 variants by default to avoid this, fast math can be turned back on with — fast_math. (Ben Noordhuis) #1398. Tests: timeouts have been tuned specifically for slower platforms, detected as ARMv6 and ARMv7. (Roman Reiss) #1366.
* **npm:** Upgrade npm to 2.7.6. See the release notes for details.

### Known issues

* Some problems with unreferenced timers running during beforeExit are still to be resolved. See #1264.
* Surrogate pair in REPL can freeze terminal #690
* process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774
* Calling dns.setServers() while a DNS query is in progress can cause the process to crash on a failed assertion #894
* readline: split escapes are processed incorrectly, see #1403

## Community Updates

* Difference between io.js and The Node Foundation iojs/io.js#1416.
* NPM launches private modules and npm inc raises.
* Thoughts of Node.js Foundation on Medium.
* io.js v1.8.0 crypto performance on io.js wiki.
* io.js mention on Oracle’s blog.
* State of the io.js Build April 2015

## Upcoming Events

* JSConf Uruguay tickets are on sale, April 24th & 25th at Montevideo, Uruguay
* NodeConf Adventure tickets are on sale, June 11th — 14th at Walker Creek Ranch, CA
* CascadiaJS tickets are on sale, July 8th — 10th at Washington State
* NodeConf EU tickets are on sale, September 6th — 9th at Waterford, Ireland

原文：[io.js Week of April 17th](https://medium.com/node-js-javascript/io-js-week-of-april-17th-e4c6f2db7659)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
