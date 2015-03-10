---
layout: post
title: Using Liquid with Jekyll
category: tutorial
author: steven
---

So now that we've got a [simple website]({%post_url 2015-02-17-intro-to-jekyll%}) up and know a bit about [markdown]({%post_url 2015-02-18-intro-markdown%}), it's time to add your own content to your page. In order to do this, you'll need to learn about the language that's used with Jekyll. In this tutorial, we will learn about [Liquid](https://github.com/Shopify/liquid/wiki) to add functionality to your blog posts.

## What is Liquid?
Liquid was created by [Shopify](http://www.shopify.com/) as a template engine. A template engine basically helps blogs quickly create all the necessary files on each post so the author only has to focus on the content.

For example, if you wanted to include the author information on a blog post for every entry, manually typing the html would be very cumbersome. This is where Liquid comes in. With Liquid, you can set that information in one spot and can pull it up quickly and elegantly.

## Add Liquid to Files
We will need to sidetrack a bit and learn about [YAML](http://yaml.org/) font matter. For the sake of this article, I won't go too deep into it. You pretty much need to add a special header to any file you want to be transformed.

To do this, all you need to do is add three dashes to the top of your page:
{% highlight yaml %}
---
---
{% endhighlight %}

That's it! You can now use Liquid in your page!

## Using Predefined Global Variables
Now that you got your YAML set up, we'll now add some basic global variables to the top of the page. Global in this scenario means that this entire page gets access to the variable.

For our first global variable, we'll be adding a `title`.

To do this, all you need to do is go up to the top and add title between your title and the title you want your page to be.

{% highlight yaml %}
---
title: My First Post
---
{% endhighlight %}

Once you do that, the page title will now be called "My First Post" which you can see on the page tab.

Now, if you want to access this page title somewhere in your code, all you need to do is reference it using these {{ }} brackets. The code ends up looking like this:
{% highlight html %}
  <html>
    <head>
    </head>
      <body>
        <h1> My page title: {{ page.title }} </h1>
      </body>
  </html>
{% endhighlight %}

To learn about the different global variables, check out [this page](http://jekyllrb.com/docs/frontmatter/).

## Creating a Collection
You may eventually want to store data that you can pull cleanly. You can do this by creating a `_data` folder in your root directly.

You then create a a file that will contain your data that is of type `.yml`. We will make a file called `books.yml`. Once you create that file, open it and then populate it with the following:

```
#book details
catinhat:
  title: The Cat in the Hat
  author: Dr. Suess

frankenstein:
  title: Frankeinstein
  author: Mary Shelley

```

So once you have that, go to the page you want to add the content. In our first page, we will then add this to the top of our page:

{% highlight yaml %}
---
title: My First Post
books: catinhat
---
{% endhighlight %}

And then, in the html we will call that information as follows:
{% highlight html %}
  <html>
    <head>
    </head>
      <body>
        <h1> My page title: {{ page.title }} </h1>
      {% raw %}    {% assign book = site.data.books[page.books] %}
          {% if book %}
          <p>{{ book.title }}</p>
          {% endif %} {% endraw %}
      </body>
  </html>
{% endhighlight %}

This may be a lot to write down for so little, but the ability to call the information without typing manually is very powerful.

## Programming in Liquid

As you may have noticed in the code above, there's an if tag in the angular brackets. This is the very heart of Liquid. You are able to use basic programming commands like if statements and for loops. Mixing this with your html will allow you to do a lot with just a little bit of code.

To make a loop that goes through all the books in your data file, all you need to do is use the for command:
{% highlight html %}
  <html>
    <head>
    </head>
      <body>
        <h1> My page title: {{ page.title }} </h1>
        {% raw %}{% for book in site.data.books %}
          <p>{{ book.title }}</p>
        {% endfor %} {% endraw %}
      </body>
  </html>
{% endhighlight %}

This will loop through each book in the `book.yml` file and output the title. Each one will be on a separate paragraph as well. As you can see, this saves a ton of time if you have a large amount of data you want to output.

## Conclusion
Liquid is one of the reasons why Jekyll is so powerful as a blog engine. Being able to use templates saves a ton of time when you want to focus on just writing posts.

----
References: [official docs](http://docs.shopify.com/themes/liquid-documentation/basics), [frontmatter](http://jekyllrb.com/docs/frontmatter/)
