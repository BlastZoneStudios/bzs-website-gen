---
layout: post
title: Intro to Markdown with Jekyll
category: tutorial
author: steven
---

So in the [last tutorial]({%post_url 2015-02-17-intro-to-jekyll%}) we got a simple page up and running. That was essentially the "hello world" of Jekyll. Now, let's get to the core reason why people choose Jekyll - writing blog posts. This tutorial will cover the main language Jekyll posts are written in.

## Introduction to Markdown
Markdown is [markup's](http://en.wikipedia.org/wiki/Markup_language) more attractive sister. You're able to do most of the common things associated with markup, except in a more elegant way. [HTML](http://en.wikipedia.org/wiki/HTML) is probably the most widely known and widely used markup language. The issue with html is that it looks like this:

```html
  <html>
    <head>
      <body>
        <h1> Hello World </h1>
        <p> Check out this new site! </p>
      </body>
    </head>
  </html>
```

While it makes sense how it works programmatically, the tags can get quite repetitive after a while. This is where markdown comes in. That same snippet above can be written like this in markdown

```
# Hello World
Check out this new site!
```

See? Isn't that a lot cleaner?! Writing blogs like this is way more natural then with markup so you can just focus on the content.

### Adding headers
To add a header all you need to do is type a hashtag. The more hashtags, the smaller the headers will be. For example:

```
# Header 1
## Header 2
### Header 3
```
It ends up looking like this:
# Header 1
## Header 2
### Header 3

If you're familiar with html the hashtag count corresponds to the `<h>` tags.

### Adding links
Links are important in any blog post as it allows the reader to look up further information on the topic your post is covering.

This is the syntax for links: `[name](link)`

Say you want to link a user to a wikipedia article about cats. Here is how you do it in markdown:

`[cats](https://en.wikipedia.org/wiki/Cat)`

The result ends up looking like this: [cats](https://en.wikipedia.org/wiki/Cat)

### Adding direct images
You've just learned how to add a click link, but now how do you add an image?

The syntax is similar to linking, except with an added exclamation: `![name](link)`

So if you wanted an image of a cat you'd write it out like this:

`![cat pic](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Cat_poster_1.jpg/320px-Cat_poster_1.jpg)`

Which ends up looking like this:
![cat pic](https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/Cat_poster_1.jpg/320px-Cat_poster_1.jpg)

### Adding text blocks
You've probably noticed me including small text boxes like this: `this is a text box`

In order to do that, all you need to do is type `` `text` `` where `text` is your text

There are a couple of rules for this, but I'll only cover a<enter> few. For large blocks you should put three backticks to indicate where the comment starts and ends. For example:

````
```
var i = 5;
i += 2;
alert(i);

```
````

If you want to add a backtick to your textbox, you need to [escape](http://en.wikipedia.org/wiki/Escape_character) it by adding an extra backtick before and after it.

It looks like this: ``` `` `sup` `` ```

Escaping the example above looks like this:
```` ``` `` `sup` `` ``` ````

## What's Next?
This is pretty much the basics of markdown. You can actually get a lot done with just these few things. If you want to look more into it, here's the [official documentation](http://daringfireball.net/projects/markdown/syntax). This [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) is also really helpful!

----
References: [official docs](http://daringfireball.net/projects/markdown/syntax), [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
