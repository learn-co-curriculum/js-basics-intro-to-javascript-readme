# Intro to JavaScript

## Problem Statement

If we want to create modern, fully-equipped websites and web apps, we need to
use JavaScript. This programming language has its own uses, history, tools and
practices, and becoming familiar with them will let us leverage JavaScript's
power to improve all of our web experiences.

## Objectives

1. Describe the JavaScript language and its uses
2. Outline the history of JavaScript
3. Write JavaScript in the Chrome Dev Tools console
4. Identify JavaScript syntax and best practices
5. Establish good JavaScript learning habits

## Describe the JavaScript language and Its Uses

_JavaScript_, commonly abbreviated as _JS_, is the programming language of the web.
Along with HTML and CSS, it's used to create virtually all the web pages and
apps you interact with, from Google to Facebook to Wikipedia to Amazon to
Netflix.

Each of these three main web technologies plays a role in creating the content you
see on a website:

- **HyperText Markup Language (HTML)** provides structure to the content, arranging it in a nested, tree-like way, and allows us to mark up the content with attributes like `id` and `class`.
- **Cascading Style Sheets (CSS)** adds styling to the page, letting us customize the look of the content, often using `id` and `class` attributes, in addition to the semantic elements, to target the elements we want to style.
- **JavaScript** does pretty much everything else and handles most of the dynamic behavior of a website. For example: reacting to user events (like clicking a button), changing the page's content without reloading, and executing network requests in the background. Like CSS, the joining of HTML elements and changes that happen when they're interacted with (clicked on, moused over, etc.) often happens by targeting elements by their `id` or `class` attribute.

When you hover your mouse over a button and it wiggles in anticipation, or when
you see new notification alerts on Twitter without refreshing the page, or when
new content progressively appears at the bottom of the page as you scroll down
your Facebook news feed—that's all JavaScript. At this point, JavaScript is a
fundamental aspect of most users' web experience.

JavaScript is one of the most popular languages in the world, and it shows no
signs of slowing up. It's still the only programming language that can run in
every major browser (HTML is a _markup language_ and CSS is a _style sheet
language_).

A language of many talents, JavaScript allows us to create incredibly diverse
applications that run in the browser, on the back-end as NodeJS, on the desktop, and on
mobile devices. It's a flexible language, allowing us to program in many
different styles — [functional][fn] and [object-oriented][oo], in particular — mixing and
matching concepts to adapt to our needs. It's powerful, scalable, and has a
robust community of developers churning out new code and advancing the language.
And, finally, it's a great first or second language to learn.

## Outline the History of JavaScript

The first version of JavaScript was built incredibly quickly in 1995. There were
a few other competitors vying to become the language of the web, but they never
gained enough traction to knock off JavaScript. And then... not much happened.
There were incremental improvements and adjustments, but JavaScript development
around 2000 very much resembled JavaScript development in the mid-1990s.

### The Emergence of Asynchronous JavaScript

Around the turn of the century, Microsoft wanted to give its customers a way to
access their email via a web browser, so they added a new JavaScript feature to
Internet Explorer that allowed an already-loaded web page to fire off a request
for additional data. It was a huge improvement over existing webmail services
that required the whole page to be reloaded in order to check for new email. The
process of making requests for additional data became known as _Asynchronous
JavaScript and XML_, or _AJAX_. (We'll take a long look at AJAX and asynchronous
code execution later on in the JavaScript material.) By 2004, when Gmail came
along with a heavy dependence on AJAX, JavaScript was in the early stages of a
rise in popularity and usefulness that has continued to the present day.

### Standardization and Modernization

Even though AJAX provided a lot of useful functionality to the language,
JavaScript was still difficult to program. Different browsers implemented
different features in different ways. There were a few competing camps which all
had different ideas about what the language should be. In early 2009, everyone
came together to agree on standardization. The fifth version of JavaScript was
released in late 2009. It's known as _ES5_ ('ES' for _ECMAScript_, the official
name of the JavaScript specification) or _Harmony_ (because it harmonized
competing implementations of the ECMAScript specification). (Note: We still
refer to the language as JavaScript, and use the particular version titles only
when we need to point to particular version features.)

Harmonization was great, but the language was still lacking modern language
features common to most standard programming languages like PHP, Java, C, Python
and Ruby. JavaScript began to address those concerns in 2015 with the unveiling
of _ES6_ or _ES2015_, the sixth version of JavaScript. Since then, they have
released updates every year, including _ES2016_ and _ES2017_, both of which have
brought additional modern features into the language. 

## Compilation and JavaScript

The name _JavaScript_ was chosen as a marketing ploy: the _Java_ language was
all the rage in 1995. The two languages share very little in common. Some JS
syntax is borrowed from Java (to make it more familiar for those early
developers coming over from the world of Java), but that's about it.

Unlike Java, JavaScript code doesn't need to be compiled. The code that you
write in a JavaScript file is the exact same code that the web browser parses
and runs. In a compiled language like Java, you write some code in a human-
readable format, and then the compiler takes that code and essentially
translates it into machine-readable code. That means that it's very difficult to
open up the source code for an application written in a compiled language and
poke around in it to understand what's going on.

Because JavaScript doesn't get compiled, that is exactly what we can do with
JavaScript code. Towards the end of this JavaScript curriculum, you'll find
yourself able to go to a website you like, open up the source code using your
browser's developer tools, and look directly at all of the JavaScript code used
on that site. This is a powerful feature of the language and an incredible tool
for learning by example.

## Write JavaScript in the Chrome Dev Tools Console

Every major browser comes with a built-in set of developer tools that you can
use to inspect, modify, and debug the content of a web page.

***NOTE:*** To ensure that instructions and screenshots match up with your
experience, use [Google Chrome](https://www.google.com/chrome/index.html) browser.

To [open the dev tools in Chrome](https://developers.google.com/web/tools/chrome-devtools/console/#open_as_panel
), press `Ctrl+Shift+J` (Windows / Linux) or `Cmd+Opt+J` (Mac). Chrome ships with a whole suite of useful dev tools, but the only one we care about for now is the JavaScript console.

The console is an environment in the browser where we can type and run arbitrary
JavaScript code in the context of the current browser window. The console is
_sandboxed_, meaning the only resources it has access to are those loaded on the
current page. Once we start declaring variables and functions in separate
JavaScript files, we'll be able to access and play around with them in the
console. The console is the single best tool for debugging JavaScript in the
browser, so start familiarizing yourself with it now.

The `Ctrl+Shift+J` / `Cmd+Opt+J` command should open up straight into the
console. If, for whatever reason, it doesn't, you can always click on `Console`
in the dropdown (when the dev tools are collapsed) or in the list of tabs:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/opening_the_console.gif" alt="Opening the console">
</picture>

To access the Chrome dev tools settings — for example, to change the theme from
light to dark — click the three vertical dots:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/changing_the_theme.gif" alt="Changing the theme">
</picture>

If at any point the console becomes cluttered with errors, warnings, or anything
else, click the `Clear console` button:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/clearing_the_console.gif" alt="Clearing the console">
</picture>

Okay, okay, enough background and setup. Let's write some code!

### Coding

We'll start off with some simple math. In the console, type `1 + 1` and press
enter. You should see the number `2` appear.

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/math_in_console.gif" alt="Math in the console">
</picture>

You just wrote and ran your first line of JavaScript code!

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/celebration.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/celebration.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/celebration.gif" alt="Celebration time!">
</picture>

The code you wrote, `1 + 1` is an _expression_. In JavaScript, an expression is **[a valid unit of code that returns a value](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators#Expressions)**. The value that it returned, `2`, is aptly referred to as the **return value** of the expression. Try out some more mathematical expressions and see what they return!

Next up, let's write some text. To make sure the JavaScript engine knows that we're trying to write some literal text, we need to wrap it in quotation marks, like so:

```js
"This is some literal text in JavaScript!"
```

Go ahead and type that classic phrase, `"Hello, world!"`, into the console and
press enter. It returned `"Hello, world!"` right back to us. Try typing some
more literal text into the console, such as your name. Don't forget the
quotation marks!

<img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/text_in_console_300.gif" alt="Text in the console">


### Debugging

JavaScript comes with a number of built-in features that can help us build and
debug our applications. One of the simplest is the `alert()` function, which
creates a simple alert in the browser window:

<picture>
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/alerting_in_console.webp" type="image/webp">
  <source srcset="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/alerting_in_console.gif" type="image/gif">
  <img src="https://curriculum-content.s3.amazonaws.com/web-development/js/basics/intro-to-javascript/alerting_in_console.gif" alt="Alerting in the console">
</picture>

Try it out yourself! Put some numbers, text, or maybe even a mathematical
equation between `alert()`'s parentheses and see what happens.

This is just a quick demonstration of one of the many features JavaScript makes
available to you in the browser. In the lessons to come, we'll learn a lot more
about the built-in magic JavaScript provides for us.

## Identify JavaScript Syntax and Best Practices

### Using Semicolons

In JavaScript, ending each statement with a semicolon is optional. When you run
some JavaScript code in the browser, the JavaScript engine actually makes
multiple passes over the same code. The first pass is to parse the syntax of
your code. The second pass is to initialize variables and functions and store
them in memory. And the third pass is to actually execute the code line-by-line.
We'll learn more about the second and third phases in an upcoming lesson.

During the first pass as it's parsing the syntax of your JavaScript file, the
engine undertakes a process called _automatic semicolon insertion_. The name
says it all, and this is why statement-ending semicolons are optional — the
JavaScript engine will automatically insert them for us. There's one main gotcha
that we'll talk about in the lesson introducing functions, but it generally
works as expected. That being said, semicolons _are_ part of the JavaScript
syntax, whether you insert them or the engine does. It's not a bad idea to
practice putting them at the end of your statements, at least until you become
more comfortable with the overall syntax of the language. Many of the examples
in upcoming lessons will include semicolons to show you where they go, and we
recommend you follow the same patterns.

### Referencing Functions, Keywords, and Variables

Throughout the JavaScript curriculum on Learn.co, we'll often refer to pieces of
code in these READMEs. If the piece of code is a function, we'll include a pair
of trailing parentheses to mark it as such, e.g., `myFunction()` or the already
introduced `alert()`. If the piece of code is a keyword in the language or a
variable that we're referencing, there'll be no parentheses: `myVariable`,
`debugger`, `if...else`, etc.

## Establish Good JavaScript Learning Habits

It's impossible to overstate how important practice is when you're learning a
new programming language. You can read the READMEs and watch the videos, but the
true education is in writing code — _lots_ of it.

As you move through the JavaScript curriculum, you should almost always have a
browser console open, either on the lesson page or in a separate window. Code
along with every example. Get used to the syntax and familiarize yourself with
the errors that arise when you mistype something. Clear the console or simply
refresh the page whenever you need a clean slate. Code, code, **code**,
**code**, ***code***.

## Resources

- [W3C — A Short History of JavaScript](https://www.w3.org/community/webed/wiki/A_Short_History_of_JavaScript)
- [Wikipedia — ECMAScript: Versions](https://en.wikipedia.org/wiki/ECMAScript#Versions)
- [MDN — Getting started with the Web](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web)

## Conclusion

JavaScript is popular and powerful programming language for the web. It works with HTML and CSS to provide many of the web experiences users now interact with daily. Its history shows that its evolution has been complicated, but improvements are happening now on a regular, yearly basis. We can use the console in Chrome Dev Tools to run JavaScript code and there are best practices to use when it comes to syntax and referencing functions, keywords and variables. The most effective way to understand JavaScript code is to practice writing it frequently.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-basics-intro-to-javascript-readme' title='Intro to JavaScript'>Intro to JavaScript</a> on Learn.co and start learning to code for free.</p>

[fn]: https://hackernoon.com/functional-programming-what-language-should-you-be-talking-313dd8bc379b
[oo]: https://en.wikipedia.org/wiki/Object-oriented_programming
