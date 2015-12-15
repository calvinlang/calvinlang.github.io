--- 
published: true
title: Enumberables
layout: post
author: Calvin

---
What are enumberables? Enumerables are Ruby methods ingrained to "traverse, search, sort and manipulate collections." You may even say "iterate?" In the end, software development is creating methods to collect, modify and present information in the most efficient way possible. A large part of this is ordering between members of a collection. So of this construct we have to sometimes find max, mins, add, count, drop and so many more. So let's talk able the enumberable #cycle.

We all need loops. They are a fundamental part of programming. So what if we are in a situation we have to loop the same content several times? Well it doesn't make sense to use an each loop over and over. Sometimes .each doesn't cut it. We could just use a while loop, but if we want to refactor this into something simpler a cycle loop may be what you're looking for.

Let's say you're making an array and you want to make an array of Monday through Friday for 4 weeks. Instead of using a while loop or a .each loop we can simply use .cycle(4) for 4 weeks. Another situation is we may want to have a list of 50 rolls of a dice. Instead of creating a method that calls the loop 50 rolls, we can simply use cycle 50 for our method that will roll the dice 50 times.

For example
{% highlight ruby linenos%}
days_of_week = ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]
days_of_week.cycle(2) { |d| puts d }
{% endhighlight %}

We get:

{% highlight ruby %}
Monday
Tuesday
Wednesday
Thursday
Friday
Monday
Tuesday
Wednesday
Thursday
Friday
{% endhighlight %}

Cycle is very powerful tool that probably that has an advantage over .each and .times. in that you can easily iterate over an array as many times as you like with .cycle(). It's a terrific way to loop through elements with more functionality than a times loop.
