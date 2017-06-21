% Getty CodeCamp
% Session 3: The Web gets stylish

## What is CSS?
- **Cascading Style Sheets**
- A programming language with one job to do: Describing stylistic rules for HTML

# Core Concepts

## Separation of Concerns

- HTML for Content, CSS for Presentation
- This means that the same HTML can be totally transformed by applying a
  different stylesheet to it. See
  the [CSS Zen Garden](http://www.csszengarden.com/) for a great example of
  this.
  
## Rules and the Cascade

- CSS is organized into _rules_ that define the appearnce of one or more
  elements on the page.
- Multiple rules can apply to any given element: you can even define multiple
  stylesheets.
- CSS rules will override one another in a process of gradually increasing
  specificity. This is called _the cascade_.
  
## Where do I put it?

- CSS stylesheets can reside in the following places:
- In an external file ending in `.css` (this is the best way)
- In the `<head>` of your HTML document, inside a `<style>` tag (sometimes this
  is okay but external is better)
- Directly on an HTML element as a `style` attribute (avoid this)

---

This is also the order in which overrides are applied; CSS applied directly to
an element is very difficult to override, which is one reason we are avoiding
it.


## What can I do?
### CSS can control:

- `color`
- `background-color`
- `font-size`
- `font-family`
- `margin`
- `padding`
- `float`
- `display`

---

In 2017, CSS can also be used for **transitions**, **animations**, and
complicated grid layouts. But we won't cover these in this class.

But even without these newfangled features, the sky is the limit to what CSS can
accomplish.

# CSS Syntax

## Basic Example

```css
/* Selector */
body {
  /* property: value */
  color: #ff0000;
}
```

---

Don't forget the closing braces and the semicolons, they're mandatory!

---

A CSS Rule always starts with a **selector** (which controls what elements we
are targeting with our rule). Inside the `{}` characters, individual
**properties** are given **values**.


## Selecting multiple elements

```css
/* A rule can a single element */
h1 {
  font-size: 24px;
}

/* Or multiple elements */
h1, h2, h3, h4, h5, h6 {
  font-family: "Helvetica", "Arial", sans-serif;
}
```

## Valid targets

```css
/* Select HTML elements by name */
body {}
h1 {}
p {}
ol, ul {}

/* Select by class with the "." */
.my-header {}
.page-title {}

/* Select by ID with "#" */
#some-unique-element {}
```

# CSS Examples

## HTML Setup

Open up the `exercises/ex-3-1-basics.html` in Atom and take a look.
Open it in your browser too. Start adding some basic style rules
in the `head` of the document to see what happens.

---

### Try these examples

```css
body {
  background-color: #ff0000;
}

h1 {
  font-size: 36px;
}

body {
  font-family: "Comic Sans MS";
}


```


## Typography

Open up the `exercises/ex-3-2-typography.html` file and follow along.

---

### Font Family

One of the first things you probably want to know is how to get rid of the
dreaded _Times New Roman_, right?

---

```css

h1, h2, h3, h4, h5, h6 {
  font-family: "Helvetica", "Arial", sans-serif;
}

```

---

Any font installed on your machine will work _locally_, but if you want to make
sure that everyone sees the same thing you need to chose fonts carefully.


```css
/* Try this - do you see anything change? */

h1, h2, h3, h4, h5, h6 {
  font-family: "Futura", "Helvetica", "Arial", sans-serif;
}

```

---

This is why it's often a good idea to define a series of fonts to act as
_fallbacks_ when you declare `font-family` properties. `serif` and `sans-serif`
are special keywords that will use whatever the system default is on the user's
machine -- good to add this one last, as a last resort.

---

### Font Style

You can also specify whether text should be bold, italic, normal, or underlined.

```css

h1, h2, h3, h4, h5, h6 {
  font-family: "Helvetica", "Arial", sans-serif;
  font-weight: bold; /* try italic, normal too */
  text-decoration: underline;
}

```

---

### Text Alignment

Just like in Word, you can control whether text should be left, center, or
right-aligned. You can also justify text (though it looks bad without
hyphenation.)

```css
/* possible values: left, right, center, justify */
.body-text p {
  text-align: left;
}

```

---

### Text spacing

You can control both `line-height` and `letter-spacing` in CSS:

```css
/* Small changes go a long way here! */
.body-text p {
  line-height: 1.6;
  letter-spacing: 1px;
}

```

---

### Font Sizes

The `font-size` property accepts several different units of measurement, including:
`px`, `in`, `cm`, and `pt`. But most of the time you will want to use `em` or `px`.

Hard-coding specific sizes as `px` values is probably the easiest method, but
using `em` (a relative measurement) can be quite useful.

---

A common pattern looks like this:

```css
/* Assign a px value to the root element as a baseline */
body {
  font-size: 16px;
}

/* Then set relative values for different parts of the page */
.headings {
  font-size: 0.75em; 
}

.body-text {
  font-size: 1.25em;
}

```

---

The `em` value of these elements will act as a multiplier for the text inside.
So we just made all the text in the `.heading` section 25% smaller, and the
`.body-text` 25% larger, while preserving the relative values of elements to one
another.

---

### Colors

- text: `aliceblue`, `tomato`
- hexadecimal strings (need to start with #): `#ff0000`, `#333333`
- RGB values like `rgb(255, 255, 255)`.

You can find a complete list of predefined color values [here](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)

---

Try writing some rules that change the `color` of text elements, or the
`background-color` of `body`, `.body-text`, or `section`

---

### Lists

You can control lists too. `ol` and `ul` elements can accept many different
values for the `list-style-type` property:

```css
ol {
  list-style-type: lower-roman;
}

ul {
  list-style-type: square
}

/* what happens when you set a value of 'none' ? */

```



