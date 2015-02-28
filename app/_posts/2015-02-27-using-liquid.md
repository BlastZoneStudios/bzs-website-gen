---
layout: post
title: Using Liquid with Jekyll
category: tutorial
author: steven
---

So now that we've got a [simple website]({%post_url 2015-02-17-intro-to-jekyll%}) up and know a bit about [markdown]({%post_url 2015-02-18-intro-markdown%}), it's time to add your own content to your page. In order to do this, you'll need to learn about the language that's used with Jekyll. In this tutorial, we will learn about Liquid Template Language, or [Liquid](https://github.com/Shopify/liquid/wiki), to add functionality to your blog posts.

## What is Liquid?
Liquid was created by [Shopify](http://www.shopify.com/) as a template engine. A template engine basically helps blogs quickly create all the necessary files on each post so the author only has to focus on the content.

For example, if you wanted to include the author information on a blog post for every entry, manually typing the html would be very cumbersome. This is where Liquid comes in. With Liquid, you can set that information in one spot and can pull it up quickly and elegantly.
