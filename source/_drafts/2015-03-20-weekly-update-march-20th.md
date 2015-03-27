title: "io.js 週報 2015.03.20"
date: 2015-03-20 09:02:55
tags:
categories: iojs 週報
---
io.js 1.6.1, openssl upgrade, community events and many more.

This week we had a two io.js releases v1.6.1 and v1.6.0, complete changelog can be found on GitHub.

## io.js 1.6 Release

### 1.6.1

path: New type-checking on path.resolve() #1153 uncovered some edge-cases being relied upon in the wild, most notably path.dirname(undefined). Type-checking has been loosened for path.dirname(), path.basename(), and path.extname() (Colin Ihrig) #1216.
querystring: Internal optimizations in querystring.parse() and querystring.stringify() #847 prevented Number literals from being properly converted via querystring.escape() #1208, exposing a blind-spot in the test suite. The bug and the tests have now been fixed (Jeremiah Senkpiel) #1213.

### 1.6.0

node: a new -r or — require command-line option can be used to pre-load modules at start-up (Ali Ijaz Sheikh) #881.
querystring: parse() and stringify() are now faster (Brian White) #847.
http: the http.ClientRequest#flush() method has been deprecated and replaced with http.ClientRequest#flushHeaders() to match the same change now in Node.js v0.12 as per joyent/node#9048 (Yosuke Furukawa) #1156.
net: allow server.listen() to accept a String option for port, e.g. { port: “1234" }, to match the same option being accepted in net.connect() as of joyent/node#9268 (Ben Noordhuis) #1116.
tls: further work on the reported memory leak although there appears to be a minor leak remaining for the use-case in question, track progress at #1075.
v8: backport a fix for an integer overflow when — max_old_space_size values above 4096 are used (Ben Noordhuis) #1166.
platforms: the io.js CI system now reports passes on FreeBSD and SmartOS (Solaris).
npm: upgrade npm to 2.7.1. See npm CHANGELOG.md for details.

### Known Issues

Possible remaining TLS-related memory leak(s), details at #1075.
Surrogate pair in REPL can freeze terminal #690
Not possible to build io.js as a static library #686
process.send() is not synchronous as the docs suggest, a regression introduced in 1.0.2, see #760 and fix in #774
Calling dns.setServers() while a DNS query is in progress can cause the process to crash on a failed assertion #894

## Community Updates
browserify supports io.js, you can check the announcement here
express.js added support to io.js
Over the last two weeks we got access to hardware from Joyent and upstreamed a patch to V8 so we got io.js building. After that we worked on passing tests for both SmartOS and FreeBSD which as of two days ago now pass, this was thanks to the amazing work of the build team and Johan Bergström
Petka Antonov is proposing a workers implementation in io.js under an experimental flag, you can join the discussion here
io.js upgraded openssl to 1.0.1m

## Upcoming Events
NodeConf tickets are on sale, June 8th and 9th at Oakland, CA and NodeConf Adventure for June 11th — 14th at Walker Creek Ranch, CA
CascadiaJS tickets are on sale, July 8th — 10th at Washington State
NodeConf EU tickets are on sale, September 6th — 9th at Waterford, Ireland

原文：[io.js Week of March 20th](https://medium.com/node-js-javascript/io-js-1-6-release-1df38cf64e6c)，作者：[@iojs](https://medium.com/@iojs)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
