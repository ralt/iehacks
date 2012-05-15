---
title: Get the target of a bubbling event
layout: post
category: events
tags: [IE6, IE7, IE8]
---

Ideal way:

{% highlight js %}
el.onclick = function( e ) {
    var target = e.target;
};
{% endhighlight %}

IE way:

{% highlight js %}
el.onclick = function( e ) {
    var evt = e || window.event,
        target = evt.target || evt.srcElement;
};
{% endhighlight %}

As shown in [this hack][1], IE must get the event through `window.event`. Also, the target is not available through `evt.target`, but through `evt.srcElement`.

[1]: http://margaine.com/iehacks/events/capture-ie-events/

