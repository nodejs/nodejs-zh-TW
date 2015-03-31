title: "io.js 週報 2015.03.27"
tags:
categories: iojs 週報
---
## io.js 1.6.2 release
This week we had one io.js releases v1.6.2, complete changelog can be found on GitHub.

## Notable changes

* **Windows:** The ongoing work in improving the state of Windows support has resulted in full test suite passes once again. As noted in the release notes for v1.4.2, CI system and configuration problems prevented it from properly reporting problems with the Windows tests, the problems with the CI and the codebase appear to have been fully resolved.
* **FreeBSD:** A kernel bug impacting io.js/Node.js was discovered and a patch has been introduced to prevent it causing problems for io.js (Fedor Indutny) #1218.
* **module:** you can now require(‘.’) instead of having to require(‘./’), this is considered a bugfix (Michaël Zasso) #1185.
* **v8:** updated to 4.1.0.25 including patches for — max_old_space_size values above 4096 and Solaris support, both of which are already included in io.js.

## Known issues

* Possible small memory leak(s) may still exist but have yet to be properly identified, details at #1075.
* Surrogate pair in REPL can freeze terminal #690
* Not possible to build io.js as a static library #686
* process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774
* Calling dns.setServers() while a DNS query is in progress can cause the process to crash on a failed assertion #894

## Community Updates

* Node.js Technical Governance Draft is proposed, you can check the draft here
* Microsoft Visual Studio team releases Node.js Tools 1.0 for Visual Studio, the release includes rich editor, code completions, interactive window, advanced debugging and profiling. Check the announcement.
* SPM monitor supports node.js and io.js, the monitor adds performance monitoring, alerting, and anomaly detection.

## Upcoming Events
* NodeConf tickets are on sale, June 8th and 9th at Oakland, CA and NodeConf Adventure for June 11th — 14th at Walker Creek Ranch, CA
* CascadiaJS tickets are on sale, July 8th — 10th at Washington State
* NodeConf EU tickets are on sale, September 6th — 9th at Waterford, Ireland
* nodeSchool tokyo will be held in April 12th at Tokyo, Japan

原文：[io.js Week of March 27th](https://medium.com/node-js-javascript/io-js-week-of-march-27th-9555f36bbb9a)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
