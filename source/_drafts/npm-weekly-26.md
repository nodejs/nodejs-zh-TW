title: "npm 週報 #26 : git tags simplified, run scripts explained, React rendered on bread"
date: 
tags:
categories: npm 週報
---

## [npm weekly #26: git tags simplified, run scripts explained, React rendered on bread](http://blog.npmjs.org/post/127718263610/npm-weekly-26-git-tags-simplified-run-scripts)



[Sign up for the Weekly](https://www.npmjs.com/npm-weekly?utm_campaign=newsletter20150827 "sign up for the npm Weekly") and get this sent to you instead!

[![](https://partners.npmjs.com/weekly/wombat-heart-git.jpg "(no, this is not a real shirt)")](https://partners.npmjs.com/weekly/wombat-heart-git.jpg)

## keep tabs on tags

Here’s a tidy little thing that was added to git a while back: `git config push.followTags true`

Once you set this config in git, any tags that you create with `npm version` will automatically be grabbed and included when you make a regular push to GitHub, or wherever your repos are. No more needing to remember to specially handle your tags!

This has been available for a few versions of git, but its (re‑) discovery within the npm office was met with joy.

“Whoaaaaaa!” <span style="text-decoration: italic;">—an npm, Inc. developer</span>

“Suddenly tags aren’t a massive pain in the ass!” <span style="text-decoration: italic;">—another npm, Inc. developer</span>

Give it a shot.

## guest post: testing and deploying with ordered npm run scripts

Also on the topic of simplifying your workload…

If there’s a `package.json` file in your project, you have the opportunity to include time-saving scripts for your development process. `npm test` is the most common — in fact, it’s included by default when you initialize a new `package.json` — but there’s much more you can script to cover both testing and what code gets run after the application is terminated.

Learn more in [this guest post from Kenneth Ormandy of Surge](http://blog.npmjs.org/post/127671403050/testing-and-deploying-with-ordered-npm-run-scripts?utm_campaign=newsletter20150827 "The npm Blog — Testing and deploying with ordered npm run scripts").

## 40 npm modules Croissant can’t live without

[Dave](https://twitter.com/daveometer "Dave Idell (@daveometer) | Twitter") from [Croissant](https://www.getcroissant.com/ "Croissant | Get access to workspaces in NYC with one monthly membership for $99") took the time to list out (and _alphabetize_) the 40 (!) npm modules their team can’t live without: [Sharing is caring](https://medium.com/startup-study-group/40-npm-modules-we-can-t-live-without-36e29e352e3a "40 NPM Modules We Can’t Live Without — Startup Study Group — Medium").

40 covered, [178,221](https://www.npmjs.com/?utm_campaign=newsletter20150827 "npm") to go. Want to tell us about your favorites?

## npm ama Brasil

[![](https://partners.npmjs.com/weekly/nodo-paraca-malhor.png "(we’re not sure if this is real Portuguese)")](http://slides.com/seldo/npm-past-present-and-future?token=xYgn8LKj#/)

If you weren’t able to attend [BrazilJS](http://braziljs.com.br/ "BrazilJS"), you missed not only [a collectible npm USB charger](https://twitter.com/seldo/status/634462665994301440 "Laurie Voss on Twitter: Hey #BrazilJS, if you would like a nifty external USB charger, come find me after my talk on Saturday! http://t.co/VgY1HHjKxe"), but a fine keynote from our own [Laurie Voss](https://twitter.com/seldo "Laurie Voss (@seldo) | Twitter").

You’re on your own for the chargers — your battery’ll last longer if you just turn down the screen brightness… — but if you want Laurie’s slides, you’re in luck: [npm past, present & future](http://slides.com/seldo/npm-past-present-and-future?token=xYgn8LKj#/ "npm past, present and future by seldo").

## join the npm usability testing hall of fame

Each week, we ask for volunteers to [help our Nick Cawthon](https://calendly.com/npm/ux "Calendly - Nick Cawthon") review upcoming improvements to package discovery, registry pages, and managing npm features; and share your feedback. This can bring not only [lucre and fineries](http://shop.npmjs.com?utm_campaign=newsletter20150827 "npm swag store") but the immortality of fame. Just ask these heroes:

*   [@boennemann](https://twitter.com/boennemann "Stephan Bönnemann (@boennemann) | Twitter")
*   [@netaisllc](https://twitter.com/netaisllc "Kevin McGee (@netaisllc) | Twitter")
*   [@roymath](https://twitter.com/roymath "Roy Mathew (@roymath) | Twitter")
*   [@beaugunderson](https://twitter.com/beaugunderson "menacing earthworks (@beaugunderson) | Twitter")
*   [@GuilfordHunter](https://twitter.com/GuilfordHunter "Hunter Lester (@GuilfordHunter) | Twitter")
*   [@beardfury](https://twitter.com/beardfury "Mike Engel (@beardfury) | Twitter")
*   [@chrisjob012](https://twitter.com/chrisjob012 "chris job (@chrisjob012) | Twitter")

[Sign up here](https://calendly.com/npm/ux "Calendly - Nick Cawthon") for a 30-minute UX session.

## up next: a React custom renderer for my toaster

[![react-blessed](https://partners.npmjs.com/weekly/react-blessed-550x.gif "(yes, this is real)")](https://www.npmjs.com/package/react-blessed/?utm_campaign=newsletter20150827 "react-blessed")

It’s so exciting that React’s core and renderer are now separated! This allows custom renderers for any browser! Even things that aren’t browsers! Like… the command line. We don’t know why you’d want to do that, but you can!

Behold: [react-blessed](https://www.npmjs.com/package/react-blessed/ "react-blessed"), a React custom renderer for [blessed](https://github.com/chjj/blessed "chjj/blessed").

#### sponsored

## a Node working hero is something to be

[Hired](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent") connects Node developers with over 2,500 vetted tech companies in 13 major tech hubs, probably including yours. Developers on Hired receive an average of 5 interview requests within a week. Looking for a job? [Check them out](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent").

原文：[npm weekly, #26](http://blog.npmjs.org/post/127718263610/npm-weekly-26-git-tags-simplified-run-scripts)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
