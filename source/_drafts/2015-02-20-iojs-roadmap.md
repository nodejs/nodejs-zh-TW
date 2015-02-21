# io.js Roadmap

<!-- ***This is a living document, it describes the policy and priorities as they exist today but can evolve over time.*** -->
***這是進行中的文件，描述現階段的方針以及重點，但是會隨著時間而修改。***

<!-- ## Stability Policy -->
## 穩定性方針

<!-- The most important consideration in every code change is the impact it will have, positive or negative, on the ecosystem (modules and applications). -->
當所有程式碼修改時最優先考量的是其對於生態圈 (模組以及應用程式) 的影響，無論是好或壞。

<!-- io.js does not remove stdlib JS API. -->
io.js 不會移除 stdlib JS API。

Shipping with current and well supported dependencies is the best way to ensure long term stability of the platform. When those dependencies are no longer maintained io.js will take on their continued maintenance as part of our [Long Term Support policy](#long-term-support).

io.js will continue to adopt new V8 releases.
* When V8 ships a breaking change to their C++ API that can be handled by [`nan`](https://github.com/rvagg/nan)
the *minor* version of io.js will be increased.
* When V8 ships a breaking change to their C++ API that can NOT be handled by [`nan`](https://github.com/rvagg/nan)
the *major* version of io.js will be increased.
* When new features in the JavaScript language are introduced by V8 the
*minor* version number will be increased. TC39 has stated clearly that no
backwards incompatible changes will be made to the language so it is
appropriate to increase the minor rather than major.

No new API will be added in *patch* releases.

Any API addition will cause an increase in the *minor* version.

<!-- ### Long Term Support -->
### 長期支援

<!-- io.js supports old versions for as long as community members are fixing bugs in them. -->
只要社群成員有持續的修復臭蟲，io.js 就會持續支援舊版本。

<!-- As long as there is a community back porting bug fixes we will push patch releases for those versions of io.js. -->
只要社群移植修正到舊版本，我們就會釋出修正版本。 

<!-- When old versions of dependencies like V8 are no longer supported by their project io.js will take on the responsibility of maintenance to ensure continued long term support in io.js patch releases. -->
一旦依賴套件的版本，譬如 V8，已經不再於該專案中維護，io.js 將會接手維護並釋出修正版本以確保長期支援。

<!-- ## Channels -->
## 頻道

<!-- * Release - Stable production ready builds. Unique version numbers following semver. -->
* Relase - 穩定、適用於線上環境的版本。版本號將依循 semver。
<!-- * Canary - Nightly builds w/ V8 version in Chrome Canary + changes landing to io.js. No version designation. -->
* Canary - 基於 Chrome Canary V8 的測試版本以及 io.js 專案的改動，將不會有版本號。
<!-- * NG - "Next Generation." No version designation. -->
* NG - 「次世代」，同樣不會有版本號。

<!-- ## NG (Next Generation) -->
## NG (次世代)

<!-- In order for io.js to stay competitive we need to work on the next generation of the platform that can more accurately integrate and reflect the advancements in the language and the ecosystem. -->
為了維持 io.js 的競爭力，我們必須開始著手下一代平台，能夠更精確的整合並將進展反映在程式語言以及生態系統之上。

<!-- While this constitutes a great leap forward for the platform we will be making this leap without breaking backwards compatibility with the existing ecosystem of modules. -->
雖然對於 io.js 來說這無疑是向前邁進了一大步，但是我們將努力使這步伐不會影響到現有生態系統的相容性。

<!-- NG will use ES6 modules and will be implementing a new platform and standard library available only to modules using this native new style. Modules written prior to NG using the old CommonJS module syntax will continue to operate against the old API. This is what will allow us to make improvements to the platform without breaking compatibility and still letting future NG based applications benefit from all the modules built today. -->
NG 將會使用 ES6 中的模組功能，並且將會實作一個新的平台以標準函式庫，只相容於那些使用新規範的模組。在 NG 之前的那些使用 CommonJS 語法的模組將會相容於舊 API。這樣我們將可以在不影響相容性的情形之下對平台進行改良，而且又能夠讓未來相容於 NG 規範的應用程式能夠使用現存的模組。

<!-- # Immediate Priorities -->
# 燃眉之急

<!-- ## Debugging and Tracing -->
## 除錯及追蹤

<!-- Debugging is one of the first things from everyone's mouth, both developer and enterprise, when describing trouble they've had with node.js/io.js. -->
無論開發者或是企業用戶，當他們提到什麼是使用 node.js/io.js 最令人挫折的，除錯經常是第一個被提到的。

<!-- The goal of io.js' effort is to build a healthy debugging and tracing ecosystem and not to try and build any "silver bullet" features for core (like the domains debacle). -->
io.js 的目標是建立一個健康的除錯以及追蹤生態系統，而非將任何「銀彈」放進核心功能之中 (譬如之前 domain 的災難)。

<!-- The [Tracing WG](https://github.com/iojs/tracing-wg) is driving this effort: -->
[Tracing WG](https://github.com/iojs/tracing-wg) 將試著改善下列幾項：

<!-- * AsyncWrap improvements - basically just iterations based on feedback from people using it. -->
* AsyncWrap 的改良 - 基本上將基於從使用者得到的反饋。
* async-listener - userland module that will dogfood AsyncWrap as well as provide many often requested debugging features.

<!--* Tracing -->
* 追蹤
  <!-- * Add tracing support for more platforms (LTTng, etc). -->
  * 在更多平台上支援追蹤的功能 (LTTng .. 等等)。
    * [Unify the Tracing endpoint](https://github.com/iojs/io.js/issues/729)。
      <!-- * New Chrome Debugger - Google is working on a version of Chrome's debugger that is without Chrome and can be used with io.js. -->
      * 新 Chrome 除錯器 - Google 正在撰寫一個不需要 Chrome 並且相容於 io.js 的 Chrome 除錯器。

<!-- ## Ecosystem Automation -->
## 生態系統的自動化

In order to maintain a good release cadence without harming compatibility we must do a better job of understanding exactly what impact a particular change or release will have on the ecosystem. This requires new automation.

The initial goals for this automation are relatively simple but will create a baseline toolchain we can continue to improve upon.

* Produce a list of modules that no longer build between two release versions.
* Produce a list of modules that use a particular core API.
* Produce detailed code coverage data for the tests in core.

<!-- ## Improve Installation and Upgrades -->
## 改良安裝及升級

<!-- * Host and maintain registry endpoints (Homebrew, apt, etc). -->
* 建立並維護註冊端點 (Homebrew, apt .. 等等)
<!-- * Document installation and upgrade procedures with an emphasis on using nvm or nave for development and our registry endpoints for traditional package managers and production. -->
* 撰寫關於安裝及升級的步驟，關於使用 nvm 或 nave 進行開發、傳統套件管理器的註冊端點以及線上環境。

## Streams

<!-- * Fix all existing compatibility issues. -->
* 修復所有現存相容性的問題。
<!-- * Simplify stream creation to avoid user error. -->
* 簡化建立 stream 以避免使用上的錯誤。
<!-- * Explore and identify compatibility issues with [WHATWG Streams](https://github.com/whatwg/streams). -->
* 與 [WHATWG Streams](https://github.com/whatwg/streams) 一起研究相容性的問題。
<!-- * Improve stream performance. -->
* 改善 stream 的效能。

<!-- ## Internationalization / Localization -->
## 國際化 / 本地化

<!-- * Build documentation tooling with localization support built in. -->
* 建立包含本地化支援的文件工具。
<!-- * Reduce size of ICU and ship with it by default. -->
* 縮減 ICU 的大小並且使之成為預設。
<!-- * Continue growth of our i18n community. -->
* i18n 社群的持續成長。
