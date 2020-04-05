title: "npm 週報 #30 : package scripts for tooling, a tutorial for front-ending, free socks for you"
date:
tags:
categories: npm 週報
---

## [npm weekly #30: package scripts for tooling, a tutorial for front-ending, free socks for you](http://blog.npmjs.org/post/129827785565/npm-weekly-30-package-scripts-for-tooling-a)

[Sign up for the Weekly](https://www.npmjs.com/npm-weekly?utm_campaign=newsletter20150924 "sign up for the npm Weekly") and get this sent to you instead!

[![](https://partners.npmjs.com/weekly/weekly30/weekly-header-30-1200x.png "npm ♥ strangeloop!")](http://www.thestrangeloop.com "Strange Loop")

## minimizing your reliance on global package installation

When you introduce a new contributor to a project — or just try to set up your new laptop — needing to run multiple global installations means plenty of opportunities for confusion or mistakes. Even the relatively straightforward process of [locally building Angular.js](https://docs.angularjs.org/misc/contribute#building-angularjs "Building AngularJS") still involves three separate shell commands and running “install” four times.

The good news is that npm scripting can help. The `scripts` section of a `package.json` can define all sorts of package-specific commands, like how to test the package and what runs after the application terminates, but as [K.Adam at Bocoup](https://bocoup.com/weblog/author/kadam-white/ "K.Adam White - Bocoup") points out,

> commands used within npm script commands have direct access to locally-installed packages: this means that modules don’t have to be globally installed in order to be exposed to the user via npm scripts.

With npm package scripts, you can provide a common façade for your tools, simplify your libraries’ workflows, and get back to building great things with the best tools for the job.

Check out K.Adam’s thorough, excellent, explanation: [A Façade for Tooling with NPM Package Scripts](https://bocoup.com/weblog/a-facade-for-tooling-with-npm-scripts/ "A Facade for Tooling with NPM Package Scripts - Bocoup").

## building a front-end workflow

We know from search and download counts in the npm registry, and the kinds of support requests we receive, that a good number of you use npm for front-end asset and dependency management — and we build our own website with npm (_delicious, delicious dog food_). Exactly how much of the workflow involved in building a website can you manage and automate with npm?

Just ask [Youssef Kababe](https://github.com/YoussefKababe "YoussefKababe (Youssef Kababe)"):

> you can literally use npm to do everything and that’s what we will do now! We’ll create a simple website by managing everything using npm!

Go follow Youssef’s step-by-step tutorial: [npm-based front-end workflow](https://moroccojs.org/tutorials/npm-based-front-end-workflow/ "npm based front-end workflow | MoroccoJS").

## rebuilding after you update Node

[Node is 4!](https://github.com/nodejs/node/blob/v4.1.1/CHANGELOG.md "node/CHANGELOG.md at v4.1.1 · nodejs/node") but among the implications that carries is the need to recompile all of your C++ addons.

[James Kyle](https://twitter.com/thejameskyle "James Kyle (@thejameskyle) | Twitter") reminds us to remind you: don’t forget about `rebuild`, which runs the `npm build` command on the folders for each package you specify.

[![NewCo Oakland Festival 2015](https://partners.npmjs.com/weekly/weekly30/newco-1100x.jpg "NewCo Oakland Festival 2015")](http://oak.newco.co/schedule-2015/ "NewCo Oakland Festival 2015")

## meeting Isaac & checking out our digs

[NewCo](http://newco.co "Home - NewCo : NewCo") is a pretty cool idea:

> Our mission is to identify, celebrate, and connect the engines of positive change in our society.

One of the unique features of their NewCo Festivals is that they introduce neat companies by literally bringing festivalgoers _to_ the companies — “get out to get in” — in a sort of business conference - _cum_ - open-studio format.

In two weeks, they’ll host the 4th Annual NewCo San Francisco and the very first NewCo Oakland Festival. We’re proud to be included. If you’re in the area, this **Thursday, October 8** at **3pm**, we hope you’ll stop by [the new place](http://blog.npmjs.org/post/128294648715/npm-weekly-27-noderedis-dependencies-and-the#oakland "oh-oh-oh-Oakland, get down"). Isaac will speak on work/life balance, you can meet the team and pet [Haggis](https://twitter.com/npmwombat "Haggis Wombat (@npmWombat) | Twitter"), and there will be swag.

Tickets are here: [NewCo Oakland](http://oak.newco.co/schedule-2015/ "2015 Schedule - NewCo Oakland : NewCo Oakland"). Use the discount code **HC30OAK** for 30% off.

[![omg npm socks](https://partners.npmjs.com/weekly/weekly30/socks-1100x.jpg "omg npm socks")](https://instagram.com/p/754Qu0gEfB/ "Jonathan Cowperthwait on Instagram: “*hyperventilates* #wombatlove”")

## finding bugs & upping your fashion game

Old and busted: [npm shirts](http://shop.npmjs.com/collections/frontpage/products/npm-t-shirt?utm_campaign=newsletter20150924 "npm t-shirt — npm swag store"), [stickers](http://shop.npmjs.com/collections/frontpage/products/npm-stickers?utm_campaign=newsletter20150924 "npm stickers — npm swag store"), and [phone chargers](http://shop.npmjs.com/collections/frontpage/products/npm-power-bank?utm_campaign=newsletter20150924 "npm Power Bank — npm swag store").

New hotness: [npm socks](https://twitter.com/cowperthwait/status/646044116606816256 "Cowperthwait on Twitter: "*hyperventilates* #wombatlove http://t.co/rwTf12eQW6 http://t.co/DJ865nMzTX"").

But there’s a catch. [Kasey](https://twitter.com/kaseybyrne "Kasey Byrne (@kaseybyrne) | Twitter") ran these off as neat gifts for [npm’s humans](https://github.com/npm/humans "npm/humans"), not for sale on the store. If you want a pair, you have to work for it.

[Sam](https://twitter.com/samccone "Sam Saccone (@samccone) | Twitter") said [he’d cry](https://twitter.com/samccone/status/646189122407698432 "Sam Saccone on Twitter: "@cowperthwait will trade copious amounts of my tears for a pair plz""), but all you have to do is help us [fix all our bugs](https://github.com/npm/npm/issues "npm/npm issues"). [James Hartig](https://twitter.com/jameshartig "James Hartig (@jameshartig) | Twitter") [already did](https://twitter.com/jameshartig/status/647248447033225216 "James Hartig on Twitter: "Woot! My @npmjs commit made it into 3.3.5: https://t.co/J8oloQV6CX""), and so can you. Submit a patch, receive a patch … of fashionable 80% cotton / 16% nylon fabric, sewn into the shape of a sock.

Seems like a fair trade to us.

#### sponsored [[?](http://info.npmjs.com/sponsorship?utm_campaign=newsletter20150924 "sponsor the Weekly")]

## getting a gig in Node

[Hired](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent") connects Node developers with over 2,500 vetted tech companies in 13 major tech hubs, probably including yours. Developers on Hired receive an average of 5 interview requests within a week. Looking for a job? [Check them out](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent").

原文：[npm weekly, #30](http://blog.npmjs.org/post/129827785565/npm-weekly-30-package-scripts-for-tooling-a)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
