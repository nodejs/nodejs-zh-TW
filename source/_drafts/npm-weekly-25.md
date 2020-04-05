title: "npm 週報 #25 : dist-tag, talking to Microsoft, semicolon trolling"
date: 
tags:
categories: npm 週報
---

## [npm weekly #25: dist-tag, talking to Microsoft, semicolon trolling](http://blog.npmjs.org/post/127157174356/npm-weekly-25-dist-tag-talking-to-microsoft)



[Sign up for the weekly](https://www.npmjs.com/npm-weekly?utm_campaign=newsletter20150820 "Subscribe to the weekly") and get this sent to you instead!

[![npm te ama](https://partners.npmjs.com/weekly/rio-luggage-tag.jpg "npm te ama")](https://docs.npmjs.com/cli/dist-tag?utm_campaign=newsletter20150820 "dist-tag | npm Documentation")

## let’s talk about distribution tags

You might have noticed that it’s possible to install `npm@latest`, which fetches npm 2.13.5, or `npm@beta`, which fetches npm 3.3.0\. Those tags, `latest` and `beta`, are examples of **distribution tags**, and they’re pretty great.

Tagging enables multiple streams of development — think “stable” and “canary” — in order to test out changes before they’re widely used by everyone, and lets users decide whether they want to opt in to testing new things or just want your package to work. (Consider using `latest` to mean “the newest we intend most people to use”, not just “the newest.”)

Add, remove, and enumerate distribution tags with [dist-tag](https://docs.npmjs.com/cli/dist-tag?utm_campaign=newsletter20150820 "dist-tag | npm Documentation").

(Also on the subject of versions: if you missed it, check out [last week’s explainer on semantic versioning](http://blog.npmjs.org/post/126588929320/npm-weekly-24-semver-explained-amazing-videos?utm_campaign=newsletter20150820 "npm weekly #24: semver explained, amazing videos, pizza").)

## let’s improve the Windows development experience

Over 40% of the developers who use npm’s registry are running Windows — a number which more or less held steady for a year, and now is increasing month over month — so anything that improves the process of Node development on a Windows machine has a major impact.

The good news is that we have a monthly check-in with [Microsoft’s Visual Studio team](https://channel9.msdn.com/Blogs/Seth-Juarez/Nodejs-Tools-for-Visual-Studio "Node.js Tools for Visual Studio | Seth Juarez | Channel 9") to keep an open line and make things more awesome. The also-good news is that you can help. Do you develop in Windows? What works, what hurts, and what’s on your wish list? Let us know: [tweet](https://twitter.com/intent/follow?screen_name=npmjs "npmbot (@npmjs) | Twitter"), [email](mailto:wombat-cowp@npmjs.com), or reach out through any of the other usual channels.

## let’s test npm Orgs

We have received actual fan mail about our upcoming **Orgs** support for teams and groups, and we hope you’ll love it too. Want to try this out before our release later this fall? [Sign up for the beta](http://info.npmjs.com/test-orgs?utm_campaign=newsletter20150820 "help us test npm Orgs").

## let’s help Nick with usability testing

We’re also still looking for volunteers to participate in a [30-minute usability session](https://calendly.com/npm/ux "Calendly - Nick Cawthon") to shape upcoming improvements to package discovery, registry pages, and managing npm features. This is your chance to influence a tool used over 2 billion times in the last month alone, and score [neat swag](http://shop.npmjs.com?utm_campaign=newsletter20150820 "npm swag store"). Can you lend a hand?

## let’s welcome another new human

[Angela Eichner](http://twitter.com/siliconvallygrl "SiliconVallyGrl (@SiliconVallyGrl) | Twitter") comes to us this week from Loggly to help bring npm to the largest names in technology, finance, and commerce. If you’re looking to support npm for large teams, self-host the npm registry on premise, or talk custom solutions, [get in touch](mailto:angela@npmjs.com).

## let’s make these Weeklies better

What are you working on? Who’s doing inspiring things? What projects could use a hand?

Drop us a note with your suggestions for the Weekly. Just reply to this email with your ideas.

## let’s teach the controversy: standard

[standard](https://www.npmjs.com/package/standard?utm_campaign=newsletter20150820 "standard") is a module that enforces consistent JavaScript style in your project.

[semicolons](https://www.npmjs.com/package/semicolons?utm_campaign=newsletter20150820 "semicolon") requires semicolons and will throw an exception if every line does not end with one.

We absolutely do not recommend attempting to use both of these at the same time.

#### sponsored

## let’s get you a Node job

[Hired](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent") connects Node developers with over 2,500 vetted tech companies in 13 major tech hubs, probably including yours. Developers on Hired receive an average of 5 interview requests within a week. Looking for a job? [Check them out](http://hired.com/?utm_source=npmjs&utm_medium=newsletter "Hired - Marketplace for Recruiting Startup & Tech Talent").

原文：[npm weekly, #25](http://blog.npmjs.org/post/127157174356/npm-weekly-25-dist-tag-talking-to-microsoft)，作者：[@npm](http://blog.npmjs.org/)，翻譯 [@iojs-tw](https://github.com/iojs/iojs-tw)，授權 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh_TW)
