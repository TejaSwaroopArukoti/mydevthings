---
layout: post
title:  "Using reduce() in javascript"
date:   2020-08-16 00:43:32 +0530
categories: javascript
---

Recently, I did find a magic function in javascript i.e reduce.

Let me explain with example.

{% highlight ruby %}
let numbers = [1,2,3,5];
let sum = numbers.reduce( (a,b)=> (a+b));
console.log(sum)
{% endhighlight %}

Check out the [MDN Docs][MDNDOCS] for more info.

[MDNDOCS]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

