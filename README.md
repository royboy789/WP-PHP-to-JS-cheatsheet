# WordPress PHP to JavaScript Cheat Sheet
This is just an open source repo to help those who are just learning JavaScript in context of WordPress. 

This is made for those who know or dabble in PHP, and are concerned with the amount of JavaScript now being used, and wil be used in the future.

There are many other great resources and classes like:
* [LinkedIn Learning](https://www.linkedin.com/learning/me)
* [JavaScripForWP.com](https://javascriptforwp.com/)
* [Gutenberg.courses](https://gutenberg.courses/)

# The Basics - Terms & Syntax
One thing I'd like to point out for those who are used to writing basic PHP in theme files, is that PHP and HTML go hand in hand. You write PHP an the server interprets & renders this as HTML for the browser.

JavaScript typically runs in a separate block (script tag) or file, and manipulates the HTML the browser sees after it has been loaded. (client side)

For any examples below, you won't be able to just replace the PHP code with JavaScript, you'll have to tell it where to place things, and how to work with them, but we can go over that too :)

## Functions
The syntax for functions is identical. You might be familiar with such great WordPress functions like:
* `the_title()`
* `the_content()`
* `get_header()`

Functions run other code, so you are not repeating or copy & pasting code nearly as much.

| PHP   |      JavaScript      |
|----------|:-------------:|
| ```some_function()``` |  ```some_function()``` |

