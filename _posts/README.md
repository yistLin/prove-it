# How to Write a Post?

Every file in this folder is going to be compiled to be a post, except the `README.md`.
To write a new post, just add a new file in this folder.
To edit a post, just edit the specific file.

## File Name

The file name should be in this format: **YYYY-MM-DD-prove-that-bla-bla-bla.md**.
For example, `2019-07-07-prove-that-god-is-love.md` is a valid file name.
But names like `2019-01-prove-that-blabla.md`, `2019-01-01.md`, or `2019-01-01-prove-that-blabla` are invalid, and these could cause some troubles to the website.

The date in the file name will be the **date of the post**.
But the other part has nothing to do with the title of the post.
It's just for the other collaborators to know the content of the file.
So make sure you give it a **short but clear** enough name.

## The Beginning of a File

There should YAML part at the very beginning of a file,
which specifies important information like, layout, title, subtitle, tags, or even categories.
It looks like this,

~~~yaml
---
layout: post
title: "Prove that God is Love"
tags: [God, love]
---
~~~

The *layout* should always be **post**.

### Title of a Post

The text inside two double quotes after `title:` is the **real title of the post**.
Title text should be put between two double quotes.
But to put double quotes **in** the title text, you have to escape it with a backslash.
So this is not allowed,

~~~yaml
---
layout: post
title: "Prove that "God" is Love"
---
~~~

To make it valid, just add a **\\** before the **"**.
Like this,

~~~yaml
---
layout: post
title: "Prove that \"God\" is Love"
---
~~~

### Tags

Tags should be put between two square brackets.
And each tags should be separated with a comma.
Tag name is case-sensitive, which means `God` and `god` would be considered as different tags in the tags page.

BTW, you don't have to add a **#** before tag names.

## Content of a File

The language we use to write the content is Markdown.
Markdown is a lightweight markup language with plain text formatting syntax.
