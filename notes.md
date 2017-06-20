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

  
