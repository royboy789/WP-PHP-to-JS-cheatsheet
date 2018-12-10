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

2 main ways you'll see these 2 languages used

__PHP__  
```
<?php 
    //some PHP code 
?>
```

__JavaScript__  
In a separate `*.js` file or 
```
<script type="text/javascript">
  // Some JavaScript code 
</script>
```


For any examples below, you won't be able to just replace the PHP code with JavaScript, you'll have to tell it where to place things, and how to work with them, but we can go over that too :)

### Variables
Variables are one of the easiest and most commonly used thing as well as one of the best first things to learn for ANY language. Variables store data, so you can keep calling it.

| PHP   |      JavaScript      |
|----------|:-------------:|
| ```$someVar = 'hi Roy'``` |  ```var someVar = 'hi Roy'``` |

I can get into some of the more advanced technqiues of `let` & `const` but know that `var` is global, and should always work, so start there.

### Functions
The syntax for functions is identical. You might be familiar with such great WordPress functions like:
* `the_title()`
* `the_content()`
* `get_header()`

Functions run other code, so you are not repeating or copy & pasting code nearly as much.

| PHP   |      JavaScript      |
|----------|:-------------:|
| ```some_function()``` |  ```some_function()``` |


### Objects & Arrays
In PHP there is 1 type of "object", and its a Class, as well as 1 type of array. In JavaScript both arrays & classes are both considered objects, along with just plain Objects.

Diving deeper, in PHP when calling on something in a Class, it may depend on the permission of that function, property, etc. But that is more advanced then I want to go.   

If you want to learn more about OOP (Classes), read & follow [Carl Alexander](https://carlalexander.ca/) 

| PHP   |      JavaScript      |
|----------|:-------------:|
| Array: ```$array['key']``` <br/> Object: ```$object->key```  |  ```object.key``` |


## WordPress Hooks
[WordPress Hooks](https://codex.wordpress.org/Plugin_API/Hooks) is one of the best parts about WordPress helping making it a very extensible platform. You may be used to `add_action` or `add_filter`, and now we can do that with JavaScript.

You must be in the admin or have the `@wordpress/hooks` package. For a more detailed look at this package check out [Igor's post](https://www.ibenic.com/use-wordpress-hooks-package-javascript-apps/) on the WordPress hooks package.

For this example I'm going to assume you are in the admin and have acess to `wp.hooks` - if you are not sure, open your developer console and see if `wp.hooks` is defined by typing `wp.hooks` and hitting enter.

#### Action Hook

 | PHP   |      JavaScript      |
 |----------|:-------------:|
 | ```add_action( 'some_wp_action', 'my_callback_function', 10, 2 )``` |  ```wp.hooks.addAction( 'some_wp_action', 'namespace', callbackFunc, 10``` |
 
 
 #### Filter
 | PHP   |      JavaScript      |
  |----------|:-------------:|
  | ```add_filter( 'some_wp_action', 'my_callback_function', 10, 2 )``` |  ```wp.hooks.addFilter( 'some_filter', 'namespace', callbackFunc, 10``` |
  
To see a full list of extendability of `wp.hooks` view the [package readme](https://github.com/WordPress/gutenberg/tree/master/packages/hooks)