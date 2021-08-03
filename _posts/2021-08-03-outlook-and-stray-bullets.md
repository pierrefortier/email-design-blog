---
layout: post
title: Outlook and stray bullets
date:   2021-08-03 16:00:00 -0400
tags:   email, outlook
---

An annoying bug that crops up in certain versions of Outlook is a stray, or extra, empty bullet point at the end of a list. 

The solution is simple but requires adding in some code. After the list, add the following `div`:

{% highlight html %}
    <div style="display:none;">&nbsp;</div> 
{% endhighlight %}

This inserts a non-breaking space after the list, which is set to `display: none;` so it doesn't affect your layout. For reasons that I can't fathom, when Outlook parses this it doesn't terminate the list with an empty element anymore. 
