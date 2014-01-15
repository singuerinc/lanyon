---
title: Day 003 - Async "waterfall" / node.js
author: singuerinc
layout: post
categories:
  - nodejs
  - async
  - javascript
---
**Waterfall** es una funci&oacute;n de la librer&iacute;a <a href="https://github.com/caolan/async" target="_blank">async.js</a> que nos permite ejecutar una serie de funciones, cada una pasa su resultado a la siguiente funci&oacute;n en el array.

{% highlight js %}
async.waterfall([
    function(callback){
    	var str = "b";
        callback(null, str);
    },
    function(arg1, callback){
    	str += "l"
        callback(null, str);
    },
    function(arg1, callback){
    	str += "o"
        callback(null, str);
    },
    function(arg1, callback){
    	str += "g"
        callback(null, str);
    },
], function (err, result) {
   console.log(result); // "blog"
});
{% endhighlight %}