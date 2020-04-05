title: "npm 週報 #29 : npm 3 out of beta, Nick out of the country, Atom (not) out of memory"
date: 
tags:
categories: npm 週報
---

## [npm weekly #29: npm 3 out of beta, Nick out of the country, Atom (not) out of memory](http://blog.npmjs.org/post/129378362260/npm-weekly-29-npm-3-out-of-beta-nick-out-of-the)



[Sign up for the Weekly](https://www.npmjs.com/npm-weekly?utm_campaign=newsletter20150917 "sign up for the npm Weekly") and get this sent to you instead!

[![npm3 is out of beta!](https://partners.npmjs.com/weekly/weekly-header-npm3-1500x.png "npm3 is out of beta!")](https://github.com/npm/npm/releases/tag/v3.3.4 "Release v3.3.4 · npm/npm")

## npm 3 is out of beta

If you don’t [watch npm on GitHub](https://github.com/npm/npm "npm/npm") (you should!), you missed [Rebecca T.](https://github.com/iarna "iarna (Rebecca Turner)")’s [understated mic-drop](https://github.com/npm/npm/releases/tag/v3.3.4 "Release v3.3.4 · npm/npm"):

> the week of this release, v3.3.3 will become `latest` and this version (v3.3.4) will become `next`!!

To understand what this means for you, now’s a good time to revisit [our release notes from when 3 initially came out in beta](https://github.com/npm/npm/releases/tag/v3.0.0 "Release v3.0.0 · npm/npm"). Much goodness awaits, including an improved multi-stage installer, flatter dependencies, and new shrinkwrap behavior. Run, don’t walk, to get the scoop.

## what would you take to Cuba?

In [Jason Koebler](https://twitter.com/jason_koebler "Jason Koebler (@jason_koebler) | Twitter")’s fantastic _Vice_ series about the challenges of getting online in Cuba, ([part 1](http://motherboard.vice.com/read/life-offline "Life, Offline | Motherboard"), [part 2](http://motherboard.vice.com/read/the-internet-dealers-of-cuba "The Internet Dealers of Cuba | Motherboard")) he calls our attention to _los paquetes_: weekly deliveries of media and online content from the U.S. and elsewhere distributed via thumbdrive.

Our own [Nick C.](https://twitter.com/ncawthon "Nick Cawthon (@ncawthon) | Twitter") is preparing for a trip to Cuba and will be delivering _paquetes_ of his own, but…

> <div>Instead of filling these with _Mr. Bean_ videos or the latest from the land of Westeros, I’m appealing to the Node community to help me support the young developer in Cuba. Let’s provide them the open-source tools, instructions, and offers of mentorship they might need to get started with their engineering careers.</div>

He’s opened up [a GitHub repo](https://github.com/npm/Paquetes-de-Codigo-Abierto "npm/Paquetes-de-Codigo-Abierto") for collecting apps, tools, and docs to distribute to Cuban computer science students who don’t benefit from the fast, free Internet which the rest of us take for granted — and soliciting our help with the curation.

Read more about Nick’s project [on our blog](http://blog.npmjs.org/post/129317528175/los-paquetes-de-codigo-abierto?utm_campaign=newsletter20150917 "The npm Blog — Los Paquetes de Codigo Abierto"), and consider helping out.

## how we fixed a memory leak in Atom

![metaphors are a thing](https://partners.npmjs.com/weekly/Hans_Brinker_Madurodamx1100px.jpg "metaphors are a thing")

We use [Marky-Markdown](https://github.com/npm/marky-markdown "npm/marky-markdown") to parse Markdown content like readmes for display on npmjs.com. Over the course of chasing down a leak, we traced the problem to a leak in [oniguruma](https://github.com/atom/node-oniguruma/ "atom/node-oniguruma"), a regex module also used by the Atom editor.

[Our pull request with a fix](https://github.com/atom/node-oniguruma/pull/36 "Fixed bug #35: memory leak in OnigStringContext by ceejbot · Pull Request #36 · atom/node-oniguruma") was quickly accepted, which took care of our leak and helps out all of its other dependents.

Quoth [our Ryan D.](https://github.com/soldair "soldair (Ryan Day)"): “another win for small modules, and one less persistent leak waking me up at night.” Amen.

## welcome n00bs / a basic npm tutorial

You’re [probably](https://twitter.com/seldo/status/644932539635757056 "Laurie Voss on Twitter: "By npm's best estimates, 50% of node.js users started using node less than 12 months ago. We are a community of newbies."") new here, and that’s okay. Here’s a neat _InfoWorld_ writeup that provides a simple npm walk-through: [Inside npm: Building and sharing JavaScript packages](http://www.infoworld.com/article/2984358/application-development/inside-npm-building-and-sharing-javascript-packages.html "Inside NPM: Building and sharing JavaScript packages | InfoWorld") [_free registration req’d_].

Once that gets you hooked, we recommend [these docs](https://docs.npmjs.com?utm_campaign=newsletter20150917 "npm Documentation"), which will get you the rest of the way to becoming a <span style="text-decoration: line-through;">ninja</span> <span style="text-decoration: line-through;">rockstar</span> <span style="text-decoration: line-through;">unicorn</span> npm power user.

And don’t forget: at any point, if you need help, [we’re here](http://blog.npmjs.org/post/129318099330/where-to-get-help-from-npm?utm_campaign=newsletter20150917 "The npm Blog — Where to get help from npm").

## ievms: one command, many VMs for testing

[![Huguette Roe / Shutterstock.com](https://partners.npmjs.com/weekly/computergarbage-1100x.jpg "Huguette Roe / Shutterstock.com")](https://github.com/xdissent/ievms "xdissent/ievms")

40% of npm registry users use Windows, but 100% of Node developers would benefit from making cross-platform development easier. Meet [ievms](https://github.com/xdissent/ievms "xdissent/ievms"): spin up virtual machines for testing IE6 – IE11 and MSEdge with a single command. Bringing more instances of IE6 into the world in 2015 runs the risk of summoning a helldemon apocalypse: for the sake of all humanity, please use your power responsibly.

#### sponsored [[?](http://info.npmjs.com/sponsorship?utm_campaign=newsletter20150917 "sponsor the Weekly")]

[DanceJS](http://dancejs.io "DanceJS: disco inferno edition") is a unique speaker series that aims to foster a community around audio-hacking and dance music. [Early bird tickets are only $10](https://ti.to/dancejs2015/september-dance-js "September Dance.js") through 9/25.

原文：[npm weekly, #29](http://blog.npmjs.org/post/129378362260/npm-weekly-29-npm-3-out-of-beta-nick-out-of-the)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
