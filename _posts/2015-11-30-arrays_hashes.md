--- 
published: true
title: Ruby Arrays and Hashes
layout: post
author: Calvin

---
Have you ever met someone who learned the piano and musical theory growing up? They just seem to have this magical sense of music. They hear so much more, and it's because they have so much background in the subject. If you hand someone like this a new instrument like a trumpet or a flute, and they can perhaps start playing a scale in about an hour. Whereas someone with no musical experience will take a few days to have be able to get to that point.

The point I'm trying to make is that experience within a genre is incredibly translatable. This week we had the assignment of learning Javascript as people who have already studied Ruby. I will make the analogy that learning Javascript knowing Ruby is like learning the Ukulele when you already play the guitar.

Essentially the process of learning Javascript has been made far simpler through knowing Ruby due to the translatability of them. They are both object oriented programming languages and the underlying principles are the same. You can have strings, integers, floats and arrays. Ruby methods are called functions in Javascript with a few differences in what those mean, but for our purposes we have just seen a difference in syntax. Ruby hashes are called objects in Javascript, and that's what we'll talk about today.

First of all, the lingo:

  *Ruby "hashes" are Javascript objects*

  *Ruby hash "keys" are Javascript object "variables"*

The differences in syntax are written as below:
{% highlight ruby linenos%}
Ruby:
  hash = { key: value, key2: value2 }

Javascript:
  var object = { property: value, property2: value }
{% endhighlight %}
To call values:
{% highlight ruby linenos%}
Ruby
  hash[:key]    ===> value

Javascript
  object.property  ===> value
{% endhighlight %}

Notice how similar they are in syntax? Keep in mind, there are some differences to take into account, they are different languages after all, but in syntax we can see a lot of similarities between Ruby hashes and Javascript objects.

One important thing to keep in mind though is the aspect of using the dot notation for Ruby. We can create hashes in Ruby with this syntax as well as how it is called:

{% highlight ruby linenos%}
hash = { key => value, key2 => value2 }
hash[key] ===> value
{% endhighlight %}

Let's look back at the syntax we used earlier:

{% highlight ruby linenos%}
hash = { key: value, key2: value2 }
hash[:key]    ===> value
{% endhighlight %}

Notice how with the : we call the key with the : in front? With this syntax the :key is not a string, it is a symbol. This makes it the best format if it's a symbol you're going to use many times.
