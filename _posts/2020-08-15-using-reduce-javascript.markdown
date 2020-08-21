---
layout: post
title:  "Using reduce() in javascript"
date:   2020-08-16 00:43:32 +0530
categories: javascript
---

Recently, I did find a magic function in javascript i.e reduce.

Let me explain with example.

{% highlight ruby %}
let numbers = [25,37,40,4];
let sum = numbers.reduce( (accumulatedValue, currentValue) => (accumulatedValue + currentValue));
console.log(sum);
{% endhighlight %}

`reduce` is prototype method on Array class. It takes callback function as first parameter.
Callback function will be called for each value in the array.  
Callback function will receive two parameters - accumulatedValue, currentValue. 
The return value of function will be stored in accumulatedValue. So, Let us understand by our example

First iteration before executing reduce - currentValue = 25, accumulatedValue = 0
						operation -   currentValue + accumulatedValue = 25 + 0 = 25.
						result will be stored in accumulatedValue. So, accumulatedValue is holding value 25.

Second iteration before executing reduce - currentValue = 37, accumlatedValue = 25
					after execting reduce - accumulatedValue = currentValue + accumulatedValue = 37 + 25 = 62


Third iteration before executing reduce - currentValue = 40, accumlatedValue = 62
					after execting reduce - accumulatedValue = currentValue + accumulatedValue = 40 + 62 = 102

Fourth iteration before executing reduce - currentValue = 4, accumlatedValue = 102
				after execting reduce - accumulatedValue = currentValue + accumulatedValue = 4 + 102 = 106.

Final accumulated value will returned. Here, 106 will be returned.

Check out the [MDN Docs][MDNDOCS] for more info.

[MDNDOCS]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

