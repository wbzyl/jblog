---
layout: post
title: Jekyll-Blog HOWTO
---

<blockquote>
<img src="../../../../images/alan-perlis.gif" alt="[Alan Perlis]" />
<p>
  Dealing with failure is easy: Work hard to improve. Success is also
  easy to handle: You've solved the wrong problem. Work hard to improve.
</p>
<p class="author">— Alan Perlis</p>
</blockquote>

# {{ page.title }}


## Markdown

Posty wpisujemy używając notacji Markdown.
Notacja jest opisana przez autora Johna Grubera 
w witrynie [Daring Fireball](http://daringfireball.net/projects/markdown/syntax).

Na stronie [Markdownr] [] można wpisywać tekst w notacji Markdown
w jednym okienku, mając w drugim — podgląd na skonwertowany na
HTMl tekst.

[markdownr]: http://markdownr.com/ "markdown online previewer"


## Kolorowanie kodu

Kod wpisujemy tak:

<pre>
&#123;% highlight ruby %&#125;
def foo
  puts 'foo'
end
&#123;% endhighlight %&#125;
</pre>

A tak to wygląda po podkolorowaniu:

{% highlight ruby %}
def foo
  puts 'foo'
end
{% endhighlight %}

Kod jest kolorowany przez narzędzie
[pygmentize](http://pygments.org/docs/cmdline/).
Wykonanie polecenia:

    pygmentize -L lexers
    ...
    * css+erb, css+ruby:
    * erb:
    * js+erb, javascript+erb, js+ruby, javascript+ruby:
    * rhtml, html+erb, html+ruby:
    * xml+erb, xml+ruby
    ...

wypisuje listę obsługiwanych języków programowania.
