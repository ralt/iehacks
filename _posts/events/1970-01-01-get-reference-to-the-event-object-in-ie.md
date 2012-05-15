---
layout: post
title: Get reference to the event object in IE
category: events
tags: [IE6, IE7, IE8]
---

Ideal way:

{% highlight js %}
el.onclick = function( e ) {
    // Handle the event "e"
};
{% endhighlight %}

IE way:

{% highlight js %}
el.onclick = function( e ) {
    var evt = e || window.event;
    // Handle the event "evt"
}
{% endhighlight %}

