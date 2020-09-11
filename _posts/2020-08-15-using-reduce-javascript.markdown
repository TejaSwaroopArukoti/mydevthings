---
layout: post
title:  "Using reduce() in javascript"
date:   2020-08-16 00:43:32 +0530
categories: javascript
---

Recently, I found a magic function in javascript i.e reduce().

 Let me explain with an example

{% highlight ruby %}
let numbers = [25,37,40,4];
let sum = numbers.reduce( (accumulatedValue, currentValue) => (accumulatedValue + currentValue));
console.log(sum);
{% endhighlight %}

`reduce()` is prototype method on Array class.   
It takes callback function as first parameter.   
Callback function will be called for each value in the array.  
Callback function will receive two parameters - `accumulatedValue`, `currentValue`. 
The return value of function will be stored in `accumulatedValue`. 

#### First iteration 
Before executing reduce - `currentValue` = 25, `accumulatedValue` = 0       
Operation -   `currentValue` + `accumulatedValue` = 25 + 0 = 25  
The result will be stored in `accumulatedValue`. So, `accumulatedValue` is holding value 25.    

#### Second iteration     
Before executing reduce - `currentValue` = 37, `accumulatedValue` = 25         
After executing reduce - `accumulatedValue` = `currentValue` + `accumulatedValue` = 37 + 25 = 62   


#### Third iteration    
Before executing reduce - `currentValue` = 40, `accumulatedValue` = 62    
After executing reduce - `accumulatedValue` = `currentValue` + `accumulatedValue` = 40 + 62 = 102    

#### Fourth iteration    
Before executing reduce - `currentValue` = 4, `accumulatedValue` = 102    
After executing reduce - `accumulatedValue` = `currentValue` + `accumulatedValue` = 4 + 102 = 106.    

Final accumulated value will be returned. Here, 106 will be returned.

Check out the [MDN Docs][MDNDOCS] for more info.

[MDNDOCS]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/reduce

