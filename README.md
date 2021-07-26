# Overview

This is just practice for me uploading to Github and following along with a course. The idea is to update after learning something each lecture to get in the idea of committing more to the page.

# Section 1: Welcome and First Steps

## CHEATS and QUALITY of Life Codes for Coding

`COMMITTING`:

Chase says to check out the conventional commits webpage. But for general usage when committing we can write the following:

`git commit -m "prog(filename): brief description".`

So then a real life example of this in practice would look like this:

`git commit -m "prog(index.html) added basic structure of webpage"`

`COMPUTER COMMANDS for Mac`

`control + command + Q`: shortcut that will take you directly to the lock screen.

`option + z`: formats the text if it goes off page when windowed.

## The 3 languages of the Front-end

In a shared venn diagram we have `HTML, CSS, and JS` all intersecting.

## HTML the Noun

In this case `HTML` is the `NOUNS` `<p></p> means paragraph`

## CSS the adjective

`CSS` is the `adjective` `p {color: red}` means "the paragraph text is `red`".

## JS the verb

`JS` are the verbs `p.hide();` means "hide the paragraph"

## Your very first webpage!

Always call your very first page `index.html`.

`! and tab` creates the default information for your html document.

EACH AND EVERY PAGE SHOULD ONLY HAVE 1 `<h1>`..

## Ordered lists, Unordered lists and listed items

`<li>`: stands for listed item.
`<ol>`: is for ordered lists. Meaning each item will have a number next to the listed item.
`<ul>`: is for unordered list. Meaning it will just put dots instead of numbers for the items in the list.

## how to add photos to page

we use `<img />` and it needs a source attribute `src` so it knows where to gather the img from.

`<img src>` = contains the source location of the img you're trying to use

`<img alt>` = describes what the image is about if the image is not available.

`<img width="500">` we can also change the size and height of an image in HTML.

## links

we use `<a></a>` because it stands for `anchor element`.

## How to open the link in a new tab

`<a target="\_blank"></a>`

## How to add a another webpage to the main page

simply create a new webpage and add a hyperlink to the html file

`<a href="blog.html"></a>`: will point to the html we just created.

## How to make links that go nowhere (deadlink)

If you want a link that points no where we type this:

`<a target="#"></a>`: and it goes nowhere like a dead link

## Structuring our HTML

## Header

What is the `header` element? What does it do?

When we want our stuff at the top of the page to be called our webpage header

```
<header>
    <h1></h1>
    <nav>
      <a href="blog.html">Blog</a>
      <a href="#">Challenges</a>
      <a href="blog.html">Blog</a>
      <a href="blog.html">Blog</a>
    </nav>
</header>
```

## HTML entities

`&copy;`: creates the copyright symbol.

## A Note on Semantic HTML

Elements have a meaning. Not all html elements are semantic. Like before with `<b>` it didn't really have a semantic value to it like `<strong>` does.

`<strong>`: its associated as a `bold`.

`<em>`: it means to `emphasize` the word that goes in the middle of the tags.

## Element Containers (Nav, Article,Div, and Aside and their differences)

### <nav>

What does `<nav>` do?: it means `navigation` and it visually doesn't do anything but creates an invisible box that houses the links inside it.

EX:

```
    <nav>
      <a href="blog.html">Blog</a>
      <a href="#">Challenges</a>
      <a href="blog.html">Blog</a>
      <a href="blog.html">Blog</a>
    </nav>
```

### <article>

What does `<article>` element do? it represents a self-contained composition in a document, page, application, or site, which is intended to be independently distributable or reusable.

Ex. include:

forum post, magazine or newspaper article, or blog entry, a product card, a user-submitted comment, an interactive widget or gadget, or any other independent item of content.

```
<article>
  <h2> Kind of similar to div and nav, right? </h2>
</article>
```

### <div>

What does `<div>` do? it is kind of like the nav container where it doesn't do anything visually. We only use `<div>` now when we don't want to attach a certain meaning to a certain container.

```
<div>
    <h2> Kind of similar to article and nav, right?</h2>
</div>
```

### <p> element

`<p>` is semantic because it is for `paragraph`.

### <aside> element

`<aside>` tag defines some content aside from the content it is placed in. The aside content should be indirectly related to the surrounding content.

`Tip`: The `<aside>` content is often placed as a sidebar in a document.

```
<aside>
  <h2> Kind of like nav, article, and div, right? Just slightly different</h2>
</aside>
```

## img's in different file locations

We usually put images in different location than the rest of the information. Kind of like this. Create a new folder called img and store the images inside it.

`<img src="/img/test.jpg">`

# Section 2: CSS Fundamentals

## Lecture 1: Introduction to CSS

What is `CSS`? `Cascading Style Sheets`: describes the visual style and presentation of the content written in HTML.

How we select and style elements:

```

h1 {
color: blue;
text-align: center;
font-size: 20px;
}

```

`h1`: is the selector
`font-size: 20px;`: Declaration/style
`font-size`: property
`20px`: value

### What is inline-style CSS?

These should never be used. These are just to show us what they are and what they can do. An in-line CSS is when you attach a property to an element and give it a value.

`<h1 style="color:blue">`

### What is an internal CSS?

For internal CSS this is placed at the `head` element of the HTML document and we create a `style` element. Everything that goes inside this element will get styled with CSS.

```
<head>
    <style>
      h1 {
        color: blue;
      }
    </style>
</head>
```

However if we have a lot of CSS code this would load our HTML file too much. This can be used when not a lot of CSS code is needed.

### What is an external CSS file? (POG)

Create a new file. We call this external file `style.css`.

Upon reflection when we change to the external CSS compared to the other styles. Why don't we see the changes right away? It's because we need to link the external file to the main HTML file.

### How do you link an external CSS file to an HTML file?

We link it to the HTML `head` element. Using `link` element. It is not used to create hyper links lmao.
We also use `rel` attribute to say what kind of link this is.

`<link href="style.css" rel="stylesheet">`

## Lecture 2: Styling Text

In this section we will learn 6 properties to style CSS.

1. `font-size: 26px`
   1. `font-size`: is usually 16px by default until we change it.
2. `Font-family`: can specify different fonts for your text.

- The funny thing about CSS for other computers is just because you have the font-family connected to your computer, doesn't mean other people will have it on their computer. So we will need to create a link like we did for the style sheet but for fonts.

4. `text-transform: uppercase`: can turn a text uppercase and other things.

5. `font-style: italic`: can also change the font style.

`NOTE`: Just because we have an `<h1>` on the page, it doesn't mean that it also needs to be the biggest one we could have an `<h2>` with a font-size that's bigger. Being `<h1>` is only about semantics, not about what it looks like.

When we use `p` as the selector it selects all the `p's` in the html document. We can actually specify a new property so the lines don't look so mushed together. This is called `Line-height`.

6. `line-height: 1.5;`: this value means that the line height will be 1.5 times the font size. By default it is set to `1`.

7. `text-align`: can change where the text is placed.

8. `inheritance`: will come back to later.
