---
title: How to add blog post on Jekyll
categories: blog
---


It's very easy to add post on `kordinglab.github.io`. All the posts are located in `_posts` folder located in [KordingLab.github.io](https://github.com/KordingLab/KordingLab.github.io). Post arrangement is based on date. Each posts can be written in markdown format (also in `html` too, like `<br>` means new line). File name of each post is in `year-month-date-post-name.md` format such as `2016-02-05-how-to-add-blog.md` or `2016-01-22-bayesian-theory.md`. On top of each post, you just have to state 2 main things in markdown, `title` and `categories` as follows

{% highlight markdown %}
---
title: Summer School in Computational Sensory-Motor Neuroscience (CoSMo)
categories: scientists
---
{% endhighlight %}

where `categories` can be only 4 choices: `scientists`, `students`, `discussion`, `blog`. It will automatically put that blog post on the page depending on categories you put.

There are multiple ways for someone to add posts:

- First way is going directly to [KordingLab.github.io](https://github.com/KordingLab/KordingLab.github.io) then go to `_post` folder and directly add markdown file. Github allows you to see preview of the markdown too so you can check before you submit any file.
- Second way is to clone the repository and add post in your local computer then push to the repository. This way you can install `Jekyll` and test to see your post on local computer by running `jekyll serve` on terminal (after you follow [instruction](http://jekyllrb.com/)) and go to `localhost:4000`. For example, this post has `blog` categories, I can see preview of my blog on `localhost:4000/blog` before I push to [KordingLab.github.io](https://github.com/KordingLab/KordingLab.github.io).

<hr>

#### Add math equation

No problem, Jekyll allows you to add math equation!

To add inline math, we don't use `$` like in LaTeX since it can be conflicted with a lot of actual dollar sign so we have to use `\\(` and `\\)` as opening and closing bracket instead i.e. <br> `\\(\mathbf{y} = A \mathbf{x}\\)` will render as \\(\mathbf{y} = A \mathbf{x}\\)

For one-line equation, we can use the same as LaTeX that is <br>`$$\cfrac{d}{dt}\cfrac{\partial L}{\partial \dot{q}} = \cfrac{\partial L}{\partial q}$$`. It will render as

$$\cfrac{d}{dt}\cfrac{\partial L}{\partial \dot{q}} = \cfrac{\partial L}{\partial q}$$


#### Add code snippet

For inline code, it's the same format as simple markdown. However, if you want to add multiple line, see [jekyllrb.com/docs/templates/](http://jekyllrb.com/docs/templates/). Bacially we will use `highlight <programming language>` and `endhighlight` as beginning and end tag for code snippet.


#### Add images link or Youtube video

For images link, we can add `html` as follows

{% highlight html %}
<figure><center>
  <img width="300" src="http://explainxkcd.com/wiki/images/4/4d/git.png"/>
</center></figure>
{% endhighlight %}

<figure><center>
  <img width="300" src="http://explainxkcd.com/wiki/images/4/4d/git.png"/>
</center></figure>


For Youtube, you can just copy embed link from Youtube (`share` > `embed`). For example,

{% highlight html %}
<center>
<iframe width="420" height="315" src="https://www.youtube.com/embed/pF5xBtaL3YI" frameborder="0" allowfullscreen></iframe>
</center>
{% endhighlight %}

<center>
<iframe width="420" height="315" src="https://www.youtube.com/embed/pF5xBtaL3YI" frameborder="0" allowfullscreen></iframe>
</center>