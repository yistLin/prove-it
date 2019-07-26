# How to Write a Post?

Every file in this folder is going to be compiled to be a post, except the `README.md`.
To write a new post, just add a new file in this folder.
To edit a post, just edit the specific file.

## File Name

The file name should be in this format: **YYYY-MM-DD-prove-that-bla-bla-bla.md**.

For example, `2019-07-07-prove-that-god-is-love.md` is a valid file name.
But names like `2019-01-prove-that-blabla.md`, `2019-01-01.md`, or `2019-01-01-prove-that-blabla` are invalid, and these could cause some troubles to the website.

The date in the file name will be **the date of the post**.
And the rest of it will appear in the link of the post.
But it has nothing to do with the title of the post.
It's also for the others to know the content of the file when they have a glance at the file name.
So make sure you give it a short but clear name.

## Post Title and Tags

There should be YAML part at the very beginning of a file,
which specifies important information like, layout, title, subtitle and tags.
It looks like this,

~~~yaml
---
layout: post
title: "Prove that God is Love"
tags: [God, love]
---
~~~

The `layout` should always be **post**.

### Title

The **real title of a post** is the text inside two double quotes after `title:`.

Title text should be put between two double quotes.
But to put double quotes in the title text, you have to escape it with a backslash.
So this is not allowed,

~~~yaml
---
layout: post
title: "Prove that "God" is Love"
---
~~~

To make it valid, just add a **\\** before **"**.

~~~yaml
---
layout: post
title: "Prove that \"God\" is Love"
---
~~~

### Tags

Tags should be put between two square brackets.
And each tags should be separated with a comma.
So the following case would be see as only one tag **#God love**, instead of two tags, **#God** and **#love**.

~~~yaml
---
layout: post
title: "Prove that God is Love"
tags: [God love]
---
~~~

Tag name is case-sensitive, which means `God` and `god` would be considered as different tags in the tags page.
BTW, you don't need to put a # before tag names.

## Post Content

After the YAML part is the content of post.
The language we use to write the content is Markdown and will be converted by Kramdown.

~~~yaml
---
layout: post
title: "Prove that God is Love"
tags: [God, love]
---

Here is the content of the post.
And it'd be better to have one spare line after the YAML and before the content.
~~~

In the following part, I will ignore the YAML, focusing on text formatting using Markdown.
And I'll exlain how things work in code blocks.
The result would be put right after the code blocks.


### Emphasis

~~~markdown
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~
~~~

Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

### Paragraphs and Line Breaks

~~~markdown
If there's no empty line between two lines of sentences,
it will turn out to be one paragraph.
_What you write is not what you see_.

But a _spare line_ will divide sentences before and after it,
making the sentences below a new paragraph.

So it's better to write **ONE SENTENCE PER LINE**.
And always leave empty lines before and after a paragraph.

Just like this.

The same principle also applies to the following elements.
**ALWAYS LEAVE EMPTY LINES** before and after:
headers,
lists,
definition lists,
blockquotes.
~~~

If there's no empty line between two lines of sentences,
it will turn out to be one paragraph.
_What you write is not what you see_.

But a _spare line_ will divide sentences before and after it,
making the sentences below a new paragraph.

So it's better to write **ONE SENTENCE PER LINE**.
And always leave empty lines before and after a paragraph.

Just like this.

The same principle also applies to the following elements.
**ALWAYS LEAVE EMPTY LINES** before and after:
headers,
lists,
definition lists,
blockquotes.

### Headers

Putting # at the beginning of the line will make it a header.
The more # you put, the smaller the header will be.
We won't use the three biggest ones, since the title of post is using the forth biggest header.

~~~markdown
#### This is Header 4

##### And Header 5

###### Finally Header 6
~~~

#### This is Header 4

##### And Header 5

###### Finally Header 6

### Lists

~~~markdown
1. Ordered list! This is the first item
1. Actually what number is put in the front doesn't matter
1. As long as there's a number followed by a dot, it makes the whole line an ordered list item.
   1. Leaving three more spaces before the number will make the line a sub-list item

* Unordered list can use asterisks
   * The same principle of sub-list can be apply to unordered list too
- We can also use minuses
+ Or pluses
~~~

1. Ordered list! This is the first item
1. Actually what number is put in the front doesn't matter
1. As long as there's a number followed by a dot, it makes the whole line an ordered list item.
   1. Leaving three more spaces before the number will make the line a sub-list item

* Unordered list can use asterisks
   * The same principle of sub-list can be apply to unordered list too
- We can also use minuses
+ Or pluses

### Definition Lists

This is used to associate definitions with terms.
And I think it's good for showing verses.

Unfortunately, I can't show the result here because this is not supported in pure Markdown (what I use to write this document).
But it will display correctly in compiled posts.

~~~markdown
John 1:1
: In the beginning was the Word, and the Word was with God, and the Word was God.
~~~

### Blockquotes

~~~markdown
> A blockquote is started using the > marker followed by an optional space
>
> all following lines that are also started with the blockquote marker
> belong to the blockquote. 
~~~

> A blockquote is started using the > marker followed by an optional space
>
> all following lines that are also started with the blockquote marker
> belong to the blockquote.

### Links

A simple link can be created by surrounding the text with square brackets and the link URL with parentheses:

~~~markdown
This is a link to the [kramdown homepage](http://kramdown.gettalong.org).
~~~

This is a link to the [kramdown homepage](http://kramdown.gettalong.org).

### Footnotes

Footnotes can easily be used in kramdown.
Just set a footnote marker
(consists of square brackets with a caret and the footnote name inside)
in the text and somewhere else the footnote definition
(which basically looks like a reference link definition).

Unfortunately, I can't show the result either because this is not supported in pure Markdown.

~~~markdown
This is a text with a footnote[^1].

[^1]: And here is the definition.
Of course you can leave a like here, [Go to Google](www.google.com)!
~~~

### Escaping Characters

These characters need to be escaped in Markdown in order to appear as literal characters instead of performing some markdown functions:
`\`, <code>&#96;</code>, `*`, `_`, `{`, `}`, `[`, `]`, `(`, `)`, `#`, `+`, `-`, `!`

Normally, we just escape these with a backslash character, like this:

~~~
\\, \`, \*, \_, \{, \}, \[, \], \(, \), \#, \+, \-, \!
~~~

\\, \`, \*, \_, \{, \}, \[, \], \(, \), \#, \+, \-, \!

## Conclusion

Apart from what I have introduced above,
there are still many available structural elements and syntax.
For more details, please take a look at [Quick Reference - kramdown](https://kramdown.gettalong.org/quickref.html).
