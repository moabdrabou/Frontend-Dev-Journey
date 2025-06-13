# CSS.md — Essential CSS Notes for Beginners

## 🔹 What is CSS?
CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of a document written in HTML. It controls the look and feel of your web pages, including colors, fonts, layout, and more.

---

## 🔹 How to Include CSS

There are three main ways to include CSS in an HTML document:

### 🔸 1. External Stylesheet (Recommended)
This is the most common and recommended method. Link an external `.css` file in the `<head>` of your HTML.

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="styles.css">
    <title>My Page</title>
  </head>
  <body>
    </body>
</html>
```

### 🔸 2. Internal Stylesheet
Embed CSS directly within the `<style>` tags in the `<head>` of your HTML document.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f4;
      }
      h1 {
        color: navy;
      }
    </style>
    <title>My Page</title>
  </head>
  <body>
    </body>
</html>
```

### 🔸 3. Inline Styles
Apply CSS directly to individual HTML elements using the `style` attribute. This method is generally discouraged for larger projects as it mixes content and presentation.

```html
<!DOCTYPE html>
<html>
  <body>
    <h1 style="color: blue; text-align: center;">Hello World</h1>
    <p style="font-size: 16px; margin-left: 20px;">This is a styled paragraph.</p>
  </body>
</html>
```

## 🔹 CSS Syntax
A CSS rule consists of a selector and a declaration block. The declaration block contains one or more declarations, each including a property and a value.

```css
selector {
  property: value;
  property: value;
}
```
Example:
```css
h1 {
  color: blue; /* Sets the text color to blue */
  font-size: 24px; /* Sets the font size to 24 pixels */
}

.my-class {
  background-color: lightgray;
  padding: 15px;
}
```

