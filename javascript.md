## **Javascript/jQuery**

jQuery is very commonly used with Javascript so I've decided to combine the two guides.
Especially since there is always the possibility of accidentally mixing up Javascript and
 jQuery syntax.

### '_' is not a function

If you're using a built-in function, make sure that you're using the proper notation/function
 name for either Javascript or jQuery. For example, `html()` is a jQuery function that
 will return the HTML contents of the selected element. But it will not work if you did
 not select your element with the jQuery selector syntax `$('#id'/'.class')`.
 
If you're using a function that you have defined yourself, make sure you've spelled
the function name correctly and the that the function exists in the scope of your
function call. This error may come up if you're calling a function that's not in the right
Javascript file or if you're calling a function that hasn't been defined for the entire
script.

### Nothing gets selected when I try selecting an element

There are two ways that I select elements. You can either use the
[document object](https://developer.mozilla.org/en-US/docs/Web/API/Document), 
or you can use [jQuery](https://learn.jquery.com/using-jquery-core/selecting-elements/).

If you are using the document interface, you will need to make sure that you are using
the [proper function](http://www.w3schools.com/js/js_htmldom_document.asp) and that you
are NOT including the ID/class selector in your text. 
(`document.getElementById("the_id")` NOT `document.getElementById("#the_id")`)

If you are using jQuery, you will need to inclde the ID/class select and you will
need to make sure that you are calling it with jQuery syntax. e.g. `$("#the_id")`.