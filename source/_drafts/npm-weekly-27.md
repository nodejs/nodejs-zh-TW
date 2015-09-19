title: "npm 週報 #27 : NodeRedis, dependencies, and the French"
date: 
tags:
categories: npm 週報
---

## [npm weekly #27: NodeRedis, dependencies, and the French](http://blog.npmjs.org/post/128294648715/npm-weekly-27-noderedis-dependencies-and-the)



[Sign up for the Weekly](https://www.npmjs.com/npm-weekly?utm_campaign=newsletter20150903 "sign up for the npm Weekly") and get this sent to you instead!

[![](https://partners.npmjs.com/weekly/weekly-header-boxes-retina.png "npm on the move")](https://www.npmjs.com/?utm_campaign=newsletter20150903)

## a story about module stewardship

![](https://partners.npmjs.com/weekly/orphan-annie-redis.jpg "how did that dog get a NodeRedis shirt?")

Today in _good news you can use_, a neat story about NodeRedis.

A while back, [Matt Ranney](https://github.com/mranney "mranney (Matt Ranney)") gave the module [redis](https://www.npmjs.com/package/redis?utm_campaign=newsletter20150903 "redis") to the community. Just this week, contributors got [the first release in a year](https://github.com/NodeRedis/node_redis/blob/master/changelog.md "node_redis/changelog.md at master · NodeRedis/node_redis") out the door.

It’s great work by the team, and also a great reminder that if you don’t have the time to maintain something anymore, the npm community is here to help.

Moving your module into a GitHub organization is a useful first step; then email your main contributors and [give them ownership on npm](https://docs.npmjs.com/cli/owner?utm_campaign=newsletter20150903 "owner | npm Documentation") and commit access on GitHub. It turns out that being given ownership in a project helps contributors feel proud to jump in and help. Win!

Have an orphan project in need of adoption? [Tell us](mailto:wombat-cowp@npmjs.com).

## _un discours sur les npm_

We didn’t get [Jon Q](https://twitter.com/itsjonq "Jon Q (@itsJonQ) | Twitter") to draw us a wombat _avec baguette_, but don’t let that stop you. If you find yourself in Toulouse next week, don’t miss [Maxime Warnier](https://github.com/maxdow/ "maxdow (Maxime Warnier)")’s talk at [Tolouse JS](http://toulousejs.francejs.org/ "Toulouse JS - L'évènement JavaScript du Sud-Ouest"): _npm: et s'il ne devait en rester qu'un_ (“npm: There Can Be Only One” — Highlander jokes transcend borders and tongues).

The talk is **Tuesday, September 8th** in Toulouse; tickets (free!) are [on Eventbrite](http://www.eventbrite.fr/e/billets-toulousejs-7-18315536262 "Billets pour ToulouseJS 7 à , Toulouse  | Eventbrite"). Send a postcard.

(And: giving a talk about npm? Don’t forget to [tell us](http://info.npmjs.com/npm-talks?utm_campaign=newsletter20150903 "giving a talk about npm?"); we’ll help spread the word.)

## a word on dependencies

You: have always wanted to know which versions of your npm package the world is using, and view npm packages and their dependencies as a graph.

[npmrank](https://github.com/anvaka/npmrank "anvaka/npmrank"): uses PageRank to identify popular or important packages. There’s a [neat online demo](http://anvaka.github.io/npmrank/online/ "npm packages sorted by pagerank") to sort packages by PageRank, and Andrei also gave us a rundown of [the top 100 packages with the most dependencies](https://github.com/anvaka/npmrank/blob/master/sample/dependencies.md#top-100-packages-with-most-dependencies) and [the top 100 packages upon which the most other packages depend](https://github.com/anvaka/npmrank/blob/master/sample/dependencies.md#top-100-most-dependent-upon-packages).

Check it out.

## a picture of dependencies

[npm2dot](https://www.npmjs.com/package/npm2dot "npm2dot") converts an npm dependency list to a dot file so you can visualize it in [Graphviz](http://www.graphviz.org/ "Graphviz | Graphviz - Graph Visualization Software"). Pretty! It’s also a neat way to see what we mean when we say that npm 3 (coming soon!) [flattens dependencies](https://github.com/npm/npm/releases/tag/v3.0.0 "Release v3.0.0 · npm/npm"):

[![](https://partners.npmjs.com/weekly/dependencies-npm-2-vs-3-550px.png "Use Case 1 : Comparison of folder structure installed separately using NPM2 and NPM3")](https://partners.npmjs.com/weekly/dependencies-npm-2-vs-3.png)

On the left, a package’s dependencies installed using npm’s current version. On the right, the same dependencies installed using npm 3: it’s easy to see a flatter structure and fewer nodes.

For a good time, try using this to compare [Express](https://www.npmjs.com/package/express "express")’ development environment and production environment:

[![](https://partners.npmjs.com/weekly/dependencies-express-dev-vs-production-550.png "Use Case 2 : Comparison of Express Production and Development environment")](https://partners.npmjs.com/weekly/dependencies-express-dev-vs-production-2000.png)

## an appeal for Private Modules users

Are you as brave as [@therockywounded](https://twitter.com/therockywounded "Rocky (@TheRockyWounded) | Twitter")? As strong as [@danmactough](https://twitter.com/@danmactough "Dan MacTough (@danmactough) | Twitter")? As noble as [@AaronMakeStuff](https://twitter.com/@AaronMakeStuff "Aaron Mendez (@AaronMakeStuff) | Twitter")? Yes. Yes, you are.

Are you _also_ a heavy user of [npm Private Modules](https://www.npmjs.com/private-modules "npm Private Modules")? Our own Nick Cawthon is working on improvements to publishing and managing private modules, and needs your help. [Sign up here](https://calendly.com/npm/ux "Calendly - Nick Cawthon") for a 30-minute usability session to influence the product and score [neat stuff](http://shop.npmjs.com?utm_campaign=newsletter20150903 "the npm swag store").

<a name="oakland" id="oakland"></a>

## oh-oh-oh-Oakland, get down

[![](https://partners.npmjs.com/weekly/office-360-retina.jpg "like Where’s Waldo, but for Rod")](https://partners.npmjs.com/weekly/office-360-3000px.jpg)

This week the Weekly is a little thin, and a little late, because we’ve been busily relocating to npm’s new world headquarters along Lake Merritt in Uptown Oakland.

The move reflects our growth to 23 humans — [and counting](https://www.npmjs.com/jobs "nice people matter: npm is hiring") — and gives us space for more classes, events, and wombat petting zoos. If you’re in the area, let’s chill.

[![](https://partners.npmjs.com/weekly/office-haggis-type-retina.jpg)](https://partners.npmjs.com/weekly/office-haggis-type-1000.jpg)[![](https://partners.npmjs.com/weekly/office-southeast-retina.jpg)](https://partners.npmjs.com/weekly/office-southeast-1000.jpg)[![](https://partners.npmjs.com/weekly/office-window-retina.jpg)](https://partners.npmjs.com/weekly/office-window-1000.jpg)

#### sponsored

## a job for you

[Hired](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent") connects Node developers with over 2,500 vetted tech companies in 13 major tech hubs, probably including yours. Developers on Hired receive an average of 5 interview requests within a week. Looking for a job? [Check them out](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent").

原文：[npm weekly, #27](http://blog.npmjs.org/post/128294648715/npm-weekly-27-noderedis-dependencies-and-the)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
