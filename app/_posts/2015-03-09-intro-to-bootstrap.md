---
layout: post
title: Introduction to Bootstrap
category: tutorial
author: steven
---

Ever notice when you go on the same website on your desktop and mobile device, the website looks different? A lot of the time, web developers use a technique known as [responsive web design](http://en.wikipedia.org/wiki/Responsive_web_design) to make their sites optimally formatted based on the device that's accessing it. In this lesson, we'll be learning about [Bootstrap](http://getbootstrap.com/); a popular framework that incorporates these techniques and then some.

## What is Bootstrap?

Twitter Bootstrap was originally created as a side project by a couple employees of [Twitter](https://twitter.com/). Their goal was to create a unified framework for front-end development. Over the years, the Bootstrap project developed a mobile-first approach, so that websites first start out in smaller devices, then build up from there.

As mentioned above, the mobile-first, responsive design that's ingrained into the Bootstrap framework is one of it's best features. When building a site, if you take this approach, you only have to code the site once and it'll great on many devices.

In essence, Bootstrap provides tools to make your website look pretty.

## Getting Started
For this first tutorial, we will just cover installing bootstrap. There are several ways to do this, but I'll be only covering the CDN method.

For those that don't know, CDNs are [content delivery networks](http://en.wikipedia.org/wiki/Content_delivery_network). The reason I choose this method over the others is because with a CDN, Bootstrap content is served to your users through the CDN's servers and not your own. This results in faster load times for your users and puts less strain on your own server. Also it's easier to install.

So to add Bootstrap to your project, first open up your `index.html`

Then, add this code to your file:
{% highlight html %}
<html>
  <head>
  <!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css">
  </head>
    <body>
    <!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/js/bootstrap.min.js"></script>
    </body>
</html>
{% endhighlight %}

And that's it!

You now have Bootstrap installed on your website. In the next posts, we will go through how to get stuff done in Bootstrap. Thanks for reading!

----
References: [official site](http://getbootstrap.com/getting-started/)
