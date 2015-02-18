---
layout: post
title: Introduction to Jekyll
category: tutorial
author: steven
---

So we've recently remade this site from the ground up
to be more blogger-friendly. Our goal was to push out
content(blogs) quickly and efficiently. The old method
of creating blogs was a bit slow and messy. We didn't
want to put everything into a single html file like how
we had before. Now here's where [Jekyll](http://jekyllrb.com)
comes in.

## What is Jekyll?

Jekyll is a blogging engine popularized by [Github](https://github.com/).
They've made it integrate pretty nicely with their
[Github-pages](https://pages.github.com/) platform. Probably the biggest
advantage of using Jekyll is that it allows you to write blogposts in
[markdown](http://daringfireball.net/projects/markdown/syntax). If you don't
know what markdown is, it's essentially a different way of writing text files.
It makes a lot more sense creating documents this way as it allows you to
include links, images and more while typing naturally.

Jekyll also provides structure to project. If you're new to web development, conforming
to an organized standard is helpful in developing [good practice](http://en.wikipedia.org/wiki/Best_practice).

## First Steps: How to Install Jekyll
Since this tutorial series will be covering a lot of information, I want to keep them short by just doing baby-steps. For this first tutorial, we will just install Jekyll and launch our first site.

### Installing Ruby
If you don't have [Ruby](https://www.ruby-lang.org/en/) installed, you're probably on Windows. Mac users can skip to [this section](#install-jek).

First, go to the [rubyinstaller](http://rubyinstaller.org/downloads/) website and download the most recent one.
![ruby-installer]({{site.url}}/img/post_imgs/2015-02-17/ruby-installer.png "installer")

Run the installer. Then when you get to

`Installation Detection and Optional Tasks`

Make sure to check "Add Ruby executables to your path" so it looks like this:
![ruby-dev]({{site.url}}/img/post_imgs/2015-02-17/ruby-dev.png "ruby-dev")

Continue with the installation and it should finish pretty quickly. You now have Ruby and can access it in your `command prompt`!

Next, you need to get [ruby devkit](http://rubyinstaller.org/downloads/) It's the same page as before - just scroll down a bit. Choose `32` or `64` bit depending on what kind o system you run and download it.

Create a folder somewhere on your computer and call it something like `RubyDev`

Turn on your `command prompt` and change the directory to where ever you created your `RubyDev` folder.

As a noob, what I do is type `cd` in the `command prompt` and then drag the folder right into the `command prompt`. This gets the exact directory of where the folder is.

Then, go back to the rubydevkit you just installed and then extract it into the `RubyDev` folder.

Go to your `command prompt` and type:
`ruby dk.rb init`

Then type:
`ruby dk.rb install`

And that's it! You're set up for Windows! For reference to installing Ruby on Windows, check out [this site](http://jekyll-windows.juthilo.com/1-ruby-and-devkit/).

### Installing Jekyll<a name="install-jek"></a>
Now to install jekyll, all you need to do is type this command in your `terminal` or `command prompt`:
`gem install jekyll`

If you're on Mac and it's complaining about permissions, type `sudo gem install jekyll` instead.

And there you have it! You now have Jekyll! So now, let's make something with it.

### Creating a New Project

Change your directory to anywhere you want. Or not, if the default is fine. Then type:
`jekyll new myblog`

and then:
`cd myblog`

finally:
`jekyll serve`

Next, go to your web browser and type `http://localhost:4000` to see your new site.

Doesn't it look good?

### Conclusion

This concludes the first part of the Jekyll series. Tune in later for more tutorials that will explore the various parts of Jekyll.Hope this helps!

----
References: [Jekyllrb](http://jekyllrb.com/docs/home/), [Install ruby on windows](http://jekyll-windows.juthilo.com/1-ruby-and-devkit/)
