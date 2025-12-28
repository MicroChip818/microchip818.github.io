---
layout: posts
title: 10 Essential HTML Tags
date: 2025-12-27 13:29:00 -0800
author: Ethan K.
categories: [Overview]
---

HTML has over 100 unique tags used to define the structure of websites, with new tags added and old tags removed during each update. Despite HTML's expansive customization, websites are not required to use every single HTML tag. There are still many tags that every website needs to function. Here are 10 essential tags for every HTML website.
### 1. &lt;!DOCTYPE html&gt; (no closing tag)
The tag above declares that the website is displayed using the HTML5 markup language.

### 2. &lt;html&gt;
The html tag serves as the webpage's root. It is also used to tell the browser what language to display the website in. For example, if an attribute named 'lang' is added with a value of 'en', the website will be displayed in English.
```html
<html lang="en">
```

### 3. &lt;head&gt;
The head of an HTML webpage contains important metadata to determine how the website is displayed.

### 4. &lt;meta&gt; (no closing tag)
Metadata is internal data that describes the website. A webpage's metadata includes the character encoding system, its title, etc. Here are some important metadata (note that not all metadata uses the &lt;meta&gt; tag):
```html
<meta charset="UTF-8"> <!-- Character encoding system UTF-8 -->
<meta name="description" content="Learning programming the fun and interactive way with coding projects, exercises, and quick tips."> <!-- Webpage description that displays on the search bar -->
<meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Scales the website to fit all devices -->
```

### 5. &lt;title&gt;
Every webpage needs a title that displays on the browser tab.

### 6. &lt;link&gt; (no closing tag)
This element is a piece of metadata that allows for linking to an external stylesheet to add CSS.
```html
<link rel="stylesheet" href="/assets/css/main.css"> <!-- change the href value to whatever your CSS file is named and include all folders before that -->
```

### 7. &lt;body&gt;
The body represents all of the webpage's visible content.

### 8. &lt;h1&gt;
Use this tag wisely. It is recommended to have one h1 tag, because it represents the main heading of the page.

### 9. &lt;a&gt;
If your website has multiple webpages or if you want to create a link to an external website, you must include the anchor tag. The syntax for opening the page in a new tab looks like this:
```html
<a href="https://microchip818.github.io/index.html" target="_blank">Homepage</a> <!-- Make sure to include the target attribute with a value of blank to open in a new tab! -->
```

### 10. &lt;main&gt;
Although not strictly required to have a functional website, having the main tag is strongly recommended to improve Search Engine Optimization (SEO).

### Final Thoughts
Many HTML tags aren't required to have a working site, but they are recommended due to the following improvements: <br>
1. Search Engine Optimization (SEO): SEO-friendly websites appear higher on search results, so more people come across them.
2. User accessibility: Websites with certain tags are more accessible as sections are distinct from each other.<br>
If you are creating a website, make sure it uses all 10 of these tags (except for the &lt;a&gt; tag if you intend to have 1 page only). Happy coding!
