---
layout: post
title: How to submit posts to the Homestead Discord
date: "2018-04-28 13:30:00 -0700"
tags: [meta, docs,]
author: jpasholk
---

## How to write and submit posts

You can write regular markdown here and Jekyll will automatically convert it to a nice webpage.  <!--more-->

I strongly encourage you to [take 5 minutes to learn how to write in markdown](https://markdowntutorial.com/) - it'll teach you how to transform regular text into bold/italics/headings/tables/etc.

[Here](https://help.github.com/articles/basic-writing-and-formatting-syntax/#styling-text) is Github's guide on markdown. Since that is where we are hosting the site, it might be a good idea to read this over just to make sure you understand what it can and can't do.

## Submitting Posts

### Easy way

The easy way to submit a post is to simply send a DM to one of the project leads (for now just Jpasholk) on Discord, with a link to the markdown file in a cloud hosted solution of your choice.

### Hard way

The harder way, but more convenient for us maintainers is to clone the repository to your local machine and add the markdown file to the `_posts` directory, and then submit a pull request on the repo. This will allow us to simply merge the pull request once we have read over the post.

## Writing in Markdown

## Headings

# Here is an h1

Generally you don't want to use these in posts. Look at how weird it looks. Look at it!

## Here is an h2

### Here is an h3

#### Here is an h4

##### Here is an h5

###### Here is an h6

## Markdown

~~~
# Here is an h1 - try to avoid these.

## Here is an h2

### Here is an h3

#### Here is an h4

##### Here is an h5

###### Here is an h6
~~~

## Bold, Emphasis, and Strikethrough

**Here is some bold text**

*Here is some emphasized text*

UiKit colors emphasized text with #f0506e

~~Here is some strikethrough text~~

~~~
**Here is some bold text**

*Here is some emphasized text*

~~Here is some strikethrough text~~
~~~

## Quoting Text

You can use quotes with a `>`

> This is some quoted text!

~~~
> This is some quoted text!
~~~

## Quoting code

You can highlight code inline by using the 'back-tick' character ``(`)``, without the braces.

~~~
...by using the 'back-tick' character ``(`)``,
~~~

### Formatting a Code Block

You can put code into it's own blocks with three back-ticks or three tilde's.

#### Here's a code block

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~
#### Done like this

{% highlight html %}
~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~
{% endhighlight %}

#### Add syntax highlighting

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```
#### Done like this

{% highlight html %}
```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```
{% endhighlight %}


#### With line numbers

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

Here you have to use [Liquid](https://help.shopify.com/en/themes/liquid) Tags. Read more [here](https://jekyllrb.com/docs/templates/#code-snippet-highlighting).

{% raw %}
```liquid
{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}
```
{% endraw %}

Okay... so how did I highlight that? You'll have to look at the raw markdown of this on GitHub... ;P

## Links

Links are as easy as wrapping the alt text in square brackets `[]`, and the URL in parentheses `()`.

Something like [this](https://github.com/DIY-Homestead/Discord/tree/blog-testing).

~~~
Something like [this](https://github.com/DIY-Homestead/Discord/tree/blog-testing).
~~~

## Lists

Lists are easy. Unordered lists are made with either an asterisk `*` or a minus sign or `-` and a space. Mind the space, it is important. Ordered lists are made simply with numbers and a space.

### Unordered

* One
* Two
* Three

- Four
- Five
- Six

~~~
* One
* Two
* Three

- Four
- Five
- Six
~~~

### Ordered:

1. One
2. Two
3. Three

~~~
1. One
2. Two
3. Three
~~~

## Images

Images are very similar to links, except you need to add an exclamation point `!` before the brackets `[]`. The URL must link to the actual image as well.

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

#### Like so

~~~
![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)
~~~

## Tables

Tables are a bit tricky but once you get used to it, it's not that difficult.

### Here's a useless table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |

## More Advanced UiKit-specific Formatting

Here I'll include some more advanced formatting that is specific to the framework I'm using for this site.

### Boxes
You can add notification, warning and error boxes like this:

~~~
{: .uk-classes-here}
Text you want to modify here.
~~~

There are some limits to what classes you can add, but it's quite powerful. If you want to beef up your posts with fancy buttons, it's worth looking into.

### Notification

{: .uk-alert .uk-padding-small}
**Note:** This is a notification box.

### Success

{: .uk-alert-success .uk-padding-small}
**Note:** This is a success box.

### Primary

{: .uk-alert-primary .uk-padding-small}
**Note:** This is a primary box.

### Warning

{: .uk-alert-warning .uk-padding-small}
**Warning:** This is a warning box.

### Error

{: .uk-alert-danger .uk-padding-small}
**Error:** This is an error box.

### Width Modifier

#### Half

{: .uk-alert-primary .uk-padding-small .uk-width-1-2}
**Note:** This is a smaller primary box.

#### Third

{: .uk-alert-success .uk-padding-small .uk-width-1-3}
**Note:** This is a smaller success box.

## Buttons

{: .uk-button .uk-button-default	}
Default

{: .uk-button .uk-button-primary}
Primary

{: .uk-button .uk-button-secondary}
Secondary

{: .uk-button .uk-button-danger}
Danger

{: .uk-button .uk-button-text}
Text

{: .uk-button .uk-button-link}
Link

### Size Modifiers

{: .uk-button .uk-button-default .uk-button-small}
Small Button

{: .uk-button .uk-button-default .uk-button-large}
Large Button

{: .uk-button .uk-button-primary .uk-button-small}
Small Primary Button

{: .uk-button .uk-button-secondary .uk-button-large}
Large Secondary Button

### Width Modifiers

{: .uk-button .uk-button-default .uk-width-1-1 .uk-margin-small-bottom}
Full Width

{: .uk-button .uk-button-primary .uk-width-1-3 .uk-margin-small-bottom}
Half Width Button

### Rounded Button

{: .uk-button .uk-button-primary .uk-width-1-3 .uk-border-rounded}
Rounded Primary Button
