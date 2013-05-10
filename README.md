autogrow.js
===========

[![endorse](https://api.coderwall.com/ultimatedelman/endorsecount.png)](https://coderwall.com/ultimatedelman)

**autogrow.js** is a jQuery plugin that, like most plug-ins, was built out of frustration for lack of support for a much-needed feature, namely the ability for a `textarea` to automatically grow and shrink dynamically with its content. I received a head-start from [this post](http://stackoverflow.com/a/10080841/7173), but decided I needed more functionality. It handles the `paste` event and 'ctrl+x', or cutting.

Basic usage ([Interactive Demo](http://jsfiddle.net/edelman/HrnHb/)):

    $('textarea').autogrow(); //or some selector that will grab textareas

**autogrow.js** has some options that you can set:

 - `context`: defaults to `$(document)`. The parent element events will be delegated to. If you want to simply use defaults but want to pass in a context, you can just do that like this: `$('textarea').autogrow($('.myContext'));`
 - `animate`: defaults to `true`. Set to `false` if you don't want the resizing of the box to be animated.
 - `speed`: defaults to 200. Speed of the resize animation.
 - `fixMinHeight`: defaults to `true`. Set to `false` if you don't want the box to stop shrinking when it hits its initial size.
 - `cloneClass`: defaults to `'autogrowclone'`. Helper CSS class for the clone used for measuring sizes. Use this if you need to apply special rules for a textbox that is right next to the one you're autogrowing, but not exactly it so that they are identical.

Example: 

    var opts = {
        context: $('li')
        , animate: false
        , cloneClass: 'faketextarea'
    };
    $('.mytextareas').autogrow(opts);
