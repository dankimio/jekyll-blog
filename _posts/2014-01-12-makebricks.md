---
layout: post
title: "MakeBricks problem"
categories: blog
---
Recently, I was solving problems at [CodingBat](http://codingbat.com/) and all problems were quite straightforward and easy to solve, but there was one that made me sit down and think for a long time, it's Make Bricks.

Here's the [problem](http://codingbat.com/prob/p118406):

> We want to make a row of bricks that is goal inches long. We have a number of small bricks (1 inch each) and big bricks (5 inches each). Return True if it is possible to make the goal by choosing from the given.

Maybe it's just me who found this problem challenging, I hope you find it interesting.

Here's solution in Python (one of several possible solutions)

{% highlight python %}
def make_bricks(small, big, goal):
    if goal > small + big * 5:
        return False
    else:
        return goal % 5 <= small
{% endhighlight %}