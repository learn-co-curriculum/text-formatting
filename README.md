# Text Formatting

## Objectives

1. Practice using bread-and-butter HTML tags (`<br>`, `<h1> - <h6>`, `<p>`)
2. Create browser ready HTML text content

### Getting Started

**Remember to use `httpserver` to live test your webpage**

 This lesson is all about formatting text in HTML. Let's start off by adding
`Hello, World!` inside the `<body>` tags of our `index.html`. Start up
`httpserver` and check out your website. You should see the new text displayed
on the page (if you don't, make sure to hit 'refresh').

Cool, we've got text on the page! Go back to your editor, and add two blank lines below `Hello, World!`. Following, add: `Hello, Moon!`. Your HTML should look something like this:

```HTML
...
<body>
  Hello, World!


  Hello, Moon!
</body>
...
```

Take a look at how this HTML is being presented in your browser. You will notice that the whitespace in our HTML file is not represented the same in our browser. Stack Overflow has an [excellent explanation][pro-so-answer] for HTML --> Browser whitespace behavior. At this juncture, your time should not be spent memorizing the various rules and history behind HTML whitespace parsing and rendering. Instead, the important takeaway is this: **if you are unsure, load the page in the browser and check!**

Assuming we do want two lines between them in the browser, let's actually address this issue now. Our solution brings us to our first tag!

---

#### `<br>`

Commonly referred to as the 'break element' or 'break tag', `<br>` provides a line break (aka carriage return) where provided. It does not need to be on its own line. For example, the following produces a visual representation closer to the html spacing we created above:

```HTML
  ...
  Hello, World!<br><br><br>Hello, Moon!
  ...
```


---

#### `<p>`

Instead of wonky spacing via the line break tags, let's wrap it all in a `<p>`
tag. Right before, and on the same line as, `Hello, World!` open the tag with
`<p>` and close it after `Hello, Moon!` with `</p>`.

You will notice a change in how whitespace is handled within. The `<p>` stands
for _paragraph_, and is used to wrap text with some built in formatting rules.

**Note:** Always make sure to close your tags - if you've left a tag open, subsequent tags
may be interpreted by the browser as _nested_ within the first tag.

---

#### `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, and `<h6>`

Aside from paragraphs, it would be nice to be able to indicate headings and
subheadings in our page. The way we do this is by using _heading_ tags, written
from largest to smallest as `<h1>` down to `<h6>`. Headings are useful for more
than just aesthetics. They aid in search engine optimization, with the largest
heading, `<h1>`, carrying the highest importance.

Above our `<p>` tags, inside `<body>`, write `Exceptional` within opening and
closing `<h1>` tags, and then, on the next line, a smaller subheading that says
`Realty Group` using `<h2>`. If we save and look at the HTML in our browser,
refreshing the page, we can see that 'Exceptional' is much larger as an `<h1>`
heading.

---

## Putting It Together

With `index.js` as our homepage, we want to include some text introducing the
Exceptional Realty Group. For now, we can put in filler text to help visualize
the look of the page:
```HTML
<body>
  <h1>Exceptional</h1>
  <h2>Realty Group</h2>

  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
  </p>
  <p>
    Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </p>
</body>
```

## Creating `real-estate-listings.html`

The second HTML page we will make requires a lot of the same basic structure as
`index.html`, and enough that developers will often use built-in text editor
snippets or copy and paste from previously written pages. We can go ahead and
copy the structure of our `index.html` file directly into
`real-estate-listings.html`. The only parts we need to change will be the
visible content inside `<body>` and our `<title>` content.

Let's append 'Listings' to our `<title>` content, and use the same two headings
we wrote in `index.html`. This time, instead of paragraph tags, let's add an
`<h3>` with 'Property Archive' as the heading content, and below we'll add in an
`<h4>` tag for 2014. Our page should look like:

```HTML
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Exceptional Realty Group - Luxury Homes - Listings</title>
  </head>
  <body>
    <h1>Exceptional</h1>
    <h2>Realty Group</h2>

    <h3>Property Archives</h3>
    <h4>2014</h4>

  </body>
</html>
```

## Going Forward

We introduced some of the basic tags needed to present text on screen. In the
next lesson, we will jump into using list tags.  

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/text-formatting' title='Text Formatting'>Text Formatting</a> on Learn.co and start learning to code for free.</p>

[pro-so-answer]: https://stackoverflow.com/questions/12863588/when-does-whitespace-matter-in-html
