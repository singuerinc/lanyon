---
title: Day 013 - Format score
author: singuerinc
layout: post
categories:
  - javascript
---
Vamos a formatear un n&uacute;mero de forma simple con una expresi&oacute;n regular.

{% highlight js %}
function format(value){
    return value.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".");
}

format(3601234); // '3.601.234'
{% endhighlight %}

<a href="/code/day-013/index.html" target="_blank">Demo</a>