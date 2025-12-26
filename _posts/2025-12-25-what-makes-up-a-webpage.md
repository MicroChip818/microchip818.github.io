---
layout: posts
title: What makes up a webpage?
date: 2025-12-25 17:30:00 -0800
author: Ethan K.
categories: [Overview]
---
In my last post, I explained how you could create a blog step-by-step. There is one important point: most of the blog's systems and code are automated by GitHub Pages and Jekyll. For example, you don't have to type the same HTML code into every webpage with layouts. I will go over all of the internal components of a webpage, specifically <a href="https://microchip818.github.io/tutorial/2025/12/24/why-i-created-this-blog-and-how-you-can-do-it-too.html" target="_blank" rel="noopener noreferrer">my last post</a>.<br>
Before I talk about the webpage's code, here are some things to keep in mind:
- An element is represented by an opening tag <> followed by a closing tag </> with content inside.
- An element may or may not have attributes followed by values. The syntax for an element like such is:
- Element classes are special attributes. I use classes on specific elements to simplify styling for those elements.

```html
<element attribute="value">content</element>
```
- In CSS, properties are traits given to elements, classes, or IDs. A property must have a value. For example, a CSS element with a font-size property and a value of 18px sets the element's font size to 18 pixels.
- For non-zero values, the value's unit needs to be specified (px, %, etc.). If a value is equal to 0, you don't need a unit.
- Some attributes don't have values. They are called boolean values; they could either be enabled or disabled from the element.
A webpage's source code contains HTML as well as different links, including the CSS file. To view a page's source code on desktop, use the keyboard shortcut Ctrl + U. If you're on a mobile device, copy the webpage's link (make sure it starts with https://), then go into the search bar and type view-source: followed by the link you copied. To view the CSS file, click on the link that ends with .css. In this source code overview, I will explain every major element in detail.

### The &lt;!DOCTYPE html&gt; declaration
This element declares that the webpage is run in the HTML5 markup language. It is a must for every HTML page.
### The &lt;html&gt; element
This element is the root of the webpage. I also added a **lang** attribute with a value of **en** to tell the browser to display the website in English.
### The &lt;head&gt; element
The head element contains all of the webpage's important metadata, some of which are represented by &lt;meta&gt; tags. Note that these tags don't require closing tags. Here is a list of the important metadata components in the webpage:
- This element tells the browser to use the UTF-8 character encoding system, encoding Unicode characters. Unicode is the world's largest character set consisting of about 160,000 characters.

```html
<meta charset="UTF-8">
```
- This element provides a description when the webpage appears in search results.

```html
<meta name="description" content="Learning programming the fun and interactive way with coding projects, exercises, and quick tips.">
```
- This element scales the webpage to optimize for all device types.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- This element provides the webpage title that the tab displays in the browser.

```html
<title>Why I created this blog - and how you can do it too | Code Outside the Box</title>
```
- Optional; this element creates an external link to Google Fonts with the font name Lato. Only use an external link for fonts if the font you want to use isn't supported by the default stylesheet.

```html
<link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&display=swap" rel="stylesheet">
```
- The link between the HTML file and the CSS file with a reference to the default stylesheet.

```html
<link rel="stylesheet" href="/assets/css/main.css">
```

### The &lt;body&gt; element
The body contains the webpage's visible content. It consists of 3 distinct sections, each of which I will cover.

#### The &lt;header&gt; element
The header is the top part of a webpage. Using my layout for posts and default links (About Me and Homepage), I made the header display the same thing throughout the website.
- This element represents the website's navigation links.

```html
<nav>
  <a href="https://microchip818.github.io/index.html" class="nav_links">Homepage</a>
  <a href="https://microchip818.github.io/about.html" class="nav_links">About Me</a>
  <a href="https://github.com/microchip818" class="nav_links">GitHub</a>
</nav>
```
- I added a few paragraph elements on top with classes after that, represented by &lt;p&gt;.
After the header, I added a short &lt;hr&gt; element to split the header and the main content with a horizontal line while improving long-term site accessibility. I also added a &lt;div&gt; element to create an object containing the main content of the element along with a class, making it much easier to style in CSS.

#### The &lt;main&gt; element
This is self-explanatory; the main content of a webpage. Here are some of the key elements I included in this portion of the site:
- **&lt;article&gt;** tells the browser the content inside the article of the webpage, this helps improve Search Engine Optimization (SEO), making the site better to display on search engines
- **&lt;h1&gt;** the main heading of the webpage; only use this once per page
- **&lt;ul&gt;** creates a list in which the order of the items isn't displayed, use &lt;ol&gt; for an ordered list instead
- **&lt;li&gt;** creates a list item
- **The id attribute** gives an element a unique identification; an ID can only be used to identify one element
These are just a few of the many elements used in the main section of my post. There are additional scripts in the page that you don't need to worry about now; I had to look them up myself. I will make a post about these scripts one day. After all, we all have a lot of new things to learn and explore!

#### The &lt;footer&gt; element
The footer is an optional part of a website, but it is recommended to store information about the author, including copyright info. This is also where my &lt;div&gt; element ends, remember?<p>
Before we finish up, I need to go over the CSS file named /assets/css.main.css. I will demonstrate the correct syntax for basic CSS selectors that are used to customize element types, classes, and IDs.<br>

```css
element {
  property: value;
}
```
You can add multiple properties. Besides that, if you want to apply the same set of properties for multiple items, add a comma for the next item. If you want to use a class instead, add a . before every class. For IDs, add a # before every ID.<br>
- **font-family** property: Sets the font of the given item. I recommend applying this property to the &lt;body&gt; element to keep the same font throughout the webpage. To add fallback fonts (fonts that show up in case the original font fails to load), add a comma followed by each fallback font.
- **background-color** and **color** properties: Sets the background color of the item and the color of all of the content itself in the item. There are 5 ways to represent colors in CSS, but for simplicity, I use the hexadecimal method. This method consists of 6 numbers in base 16 (ranging from 0 to F), going from #000000 (black) to #FFFFFF (white). The first 2 numbers represent red, the second 2 represent green, and the last 2 represent blue, similar to the RGB system.
- **margin** property: Adds space on all 4 sides of the element with a value in pixels (px). You can also specify the side (left, right, top, bottom) with properties such as margin-left. Setting the margin of a specific side to auto creates the largest margin on that side possible. For example, if I set margin-left to auto, the text shifts to the right, creating the largest left margin possible.
- **padding** property: Expands the border of the element. The "rem" value, or root em, represents a default multiple of 16 pixels (the font size of the &lt;html&gt; root).
- **max-width** property: Sets the max width of an element. This property is useful for making sure the main text of my posts doesn't extend the whole page.
- **text-align** property: Sets the alignment of the given element. This only works for text, and the values are left, right, center, and justify (the text takes up the whole width of the element).
- **font-size** property: Sets the size of the font with a value in pixels (px).

### Final Thoughts
I hope you enjoyed learning the structure of my last post's webpage and had fun during the process! As always, please provide feedback and share your thoughts by dropping a comment! Your support is greatly appreciated! With that being said, MERRY CHRISTMAS EVERYONE!!!!
