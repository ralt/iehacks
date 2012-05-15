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

'q' n'est pas reconnu en tant que commande interne
ou externe, un programme excutable ou un fichier de commandes.

