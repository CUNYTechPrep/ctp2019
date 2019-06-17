# JavaScript Guide

## About JavaScript (ECMAScript, abbreviated ES)

JavaScript (JS) is a rapidly evolving language and today's web applications depend on it. JavaScript is the only programming language supported across all modern web browsers, making it a critical technology for any web application. But since the release of Node.js, it has also gained wide adoption as a general and server-side language. JavaScript has also become the scripting language of choice for various non-web platforms, like the MongoDB database and [many more platforms](https://en.wikipedia.org/wiki/JavaScript#Uses_outside_Web_pages).

The "JavaScript" name is trademarked by the Oracle Corporation. When you work with JavaScript you will also often read and hear the term "ECMAScript" or ES. ECMAScript refers to the languages standardized specification set by the [ECMA-International](http://www.ecma-international.org/) group. The ES abbreviation is commonly used to denote which version of the JavaScript language we are using.

## Some terms and acronyms to know

- **ES5**
    + is the version of JavaScript that was published in 2009. It is currently *FULLY* supported by all major web browsers, and most books and resources written before 2015 use this version of JavaScript code.
    + For programmers, it is still important to understand how ES5 works since so much code in ES5 already exists, and it can be used simultaneously with the new ES6 syntax, which can often be confusing.
- **ES6 (ES2015)**
    + is the modern version of JavaScript published in 2015. ES6 was a _major_ update to the JavaScript language, it not only substantially changed the syntax of the language, but it also changed the behavior of various features, and has led to a new set of best practices and conventions for programming in JavaScript.
    + ES6 (as of mid 2017) is almost fully supported in modern browsers and Node.js. There are some features (module loading) which are not yet fully supported.
    + For programmers it is best practice to use ES6 as it will ensure applications will be maintainable going forward. But for businesses, it is crucial to support as many browsers as possible, to reach as many customers/users as possible. For this reason, the community has developed compilers (really transpilers that convert code) that convert ES6 to valid ES5 that can run in all currently supported browsers. The most popular ES6 compiler is [*Babel.js*](https://babeljs.io/).
- **ES7/8/Next (ES2016/2017)**
    + Since the publication of ES6, and its massive adoption, new features are being proposed and finalized at a faster pace. The changes in these new versions are much smaller than the ES5 to ES6 update, and often are already available in new browser and Node.js versions.
- **_"Vanilla JavaScript"_ or Core JavaScript**
    + refers to the syntax, expressions, statements, control flow, loops, the data types, and typing system for computing. This includes how to define objects and functions and their use.  It does not refer to any API's or host environments for accessing inputs and producing outputs. The host environments determines which inputs a JS program is allowed to receive, and what outputs it is allowed. The two primary JS host environments we will work with are the Web Browser (on the client-side) and in Node.js (on the server-side).
- **Client-Side JavaScript**
    + refers to JS programs that run within a Web Browser window. In this mode, the browser only provides API's for the language to access the document within the window (through the **DOM**: Document Object Model) and resources related to the document such as cookies. It does not allow programs to access other browser windows or any hardware resources on the computer.
- **Server-Side JavaScript**
    + refers to JS programs that run within a runtime that provides programs API's to access hardware and file resources on the computer such as the filesystem, networking sockets, keyboard, sound, cameras, etc. For this reason, runtime's like Node.js have become very popular for Web Application development as well as development on IoT devices and microprocessors such as Arduino's.
- **[Node.js](https://nodejs.org/en/)**
    + is the most popular runtime for running JavaScript on the server.
- **V8 (JavaScript) Engine**
    + an open source JavaScript engine developed by Google to speed up JS performance, by compiling JS code into native machine code. It is used by various JS runtimes (such as the Chrome Browser, Node.js, MongoDB, etc.). The runtimes are responsible for adding the environment API's that JS programs are given access to.
- **NPM: Node Package Manager**
    + `npm` is the node command line tool used to create projects and to download 3rd party packages available on https://www.npmjs.com/.


## Resources and Documentation


### Language Documentation

- MDN (Mozilla Developer Network) Web Docs 
    + https://developer.mozilla.org/en-US/docs/Web/JavaScript
    + Documentation for the Core Language and Client-side (Web Browser) API's.
    + DOM API:
        * https://developer.mozilla.org/en-US/docs/Web/API/Document
    + _Hint:_ When searching google prefix your search with "mdn javascript", such as "mdn javascript array"
- Node Documentation (Server-Side Node.js API's)
    + https://nodejs.org/en/docs/
    

### Books

- [Eloquent JavaScript, 3rd Edition](https://eloquentjavascript.net/index.html)
    + An easy to read book for new JavaScript programmers, but also contains great descriptions of more advanced topics
    + Core JavaScript: Chapters: 1-6, and 6-11
    + Optional/Advanced sections:
        * Chapter 6 is important, but you can skim: Symbols, The Iterator Interface, Inheritance
        * Chapter 8
        * Chapter 9
- [You Don't Know JS - Book Series](https://github.com/getify/You-Dont-Know-JS)
    + Various free books on specific JS topics
- For advanced books on JavaScript I recommend [Dr. Axel Rauschmayer's Books](http://exploringjs.com/)
    + For ES6: http://exploringjs.com/es6.html

## Resources for Learning ES6 when you already know ES5

### Video Courses

- [ES2015 Crash Course](https://laracasts.com/series/es6-cliffsnotes)
    + Only watch Episodes 3-10, 13-15, 17
    + This video course does a great job at comparing ES5 vs ES6 features and syntax.
    + **Note:** The videos sometimes reference _PHP, Laravel, Vue, and other technologies_ which you may not be familiar with. For those parts, focus on how the ES6 syntax works and ignore the details of those specific technologies since we won't be using them.


### Quick Listings of ES6 changes

- [ES6: New Features and Comparisons](http://es6-features.org/#Constants)
    + Provides Code Samples for quick reference of ES5 to ES6 changes
- [Learn ES2015 (from Babel.js website)](https://babeljs.io/learn-es2015/)
    + A brief overview of major changes and code samples
    + Try the Online REPL: https://babeljs.io/repl/


### Checking ES6 Compatibility

- ES6 Browser Support Table
    + https://kangax.github.io/compat-table/es6/
- ES6 Node Support
    + http://node.green/
    
