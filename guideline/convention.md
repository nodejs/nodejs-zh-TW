# 書籍寫作規範

## 專有名詞

有鑑於台灣名詞使用方式經常以中英文混合方式為主，為了方便所有翻譯人員，以下為技術類專有名詞，常見中英文翻譯對照列表如下。

| English | 中文翻譯 | 程式碼 |
| --- | --- | --- |
| Array | 陣列 | [] |
| CommonJS | CommonJS | - |
| ECMAScript | ECMAScript| - |
| ES6 | ES6| - |
| Framework | 框架 | - |
| Immediately-Invoked Function Expression | 立即函式 | (function () {})(); |
| - | 具名函式 | function fnName() {} |
| - | 匿名函式 | var fn = function () {}; |
| Node.js | Node.js | - |
| JavaScript | JavaScript| - |
| closure | 閉包 | - |
| export | export | - |
| io.js | io.js | - |
| npm | npm | - |
| nvm | nvm | - |
| module | 模組 | - |
| null | null | null |
| package | 套件 | - |
| undefined | undefined | undefined |

## 中英文混雜

中英文夾雜時，必須要使用『半型空白』隔開

#### 中英文混搭專有名詞範例，

  此書獻給所有 Node.js 以及對於 JavaScript 熱愛的程式開發者


## 標點符號

以中文全形標點符號為主。

  * ，、。！「」（）

遇英文段落（整句）採用一般（半形）標點符號。

中文與英文單字之間以一個空白字元隔開，標點符號與英文單字之間不需要空隔。

這是為了讓排版顯示的自動斷詞斷句可以正確運作，以及增加中英文混雜段落的閱讀舒適。

更多詳細排版規則請參考[中文文案排版指北](https://github.com/sparanoid/chinese-copywriting-guidelines)

#### 標點符號範例

Node.js 是一種適合用於 Server-side 的開發框架（Framework），相當 Nice！

## 特殊排版說明

中文同一段落為了方便編輯，可以將句子斷行；\
但行尾必須加上半形「\」倒斜線符號。\
因為在 HTML、EPUB 或 MOBI 格式中，\
換行字元會被當做空白字元處理，導致增加過多影響版面美觀的空格。

## 程式碼風格

統一使用 [idiomatic.js](https://github.com/rwaldron/idiomatic.js) (討論：[#9cf7787](https://github.com/nodejs-tw/nodejs-book-beginner-guide/commit/9cf77875a00d3f255bd1b33a3fcf60f7238d992c))

## Markdown 風格

### 章節標題設定

* 章節標頭為 H1, #
* 章節底下第一層目錄為 h2, ##
* 章節底下第二層目錄為 h3, ###

`#` 與標題間要保留 1 個空格。

### 無序清單

開頭無 whitespace

```markdown
1. item 1
2. item 2
```

### 有序清單

開頭無 whitespace

```markdown
* item 1
* item 2
```

### 程式碼區塊

只有一行、不需要 Highlight，或是一般的 command line 操作指令說明，\
使用標準 Code 寫法。

```
This is line One
This is line Two
```

使用 inline code block，並指定 language type。

```javascript
if (something) {
  alert('test');
}
```
