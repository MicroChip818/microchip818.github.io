---
layout: posts
title: Why I created this blog - and how you can do it too
date: 2025-12-24 14:00:00 -0800
last_updated: 2025-12-24 3:37:00 -0800
author: Ethan K.
categories: [Tutorial]
---

Hi! I'm Ethan. In my first blog post, I will explain why I chose to create this blog in further detail, and how you can start a blog on GitHub yourself. Let's dive in, shall we? <br>
There are 3 main reasons why I started this blog: <br>
**1. Interest in coding:** Since I was 6 years old, I have been fascinated with coding, starting with the website <a href="https://code.org/en-US" target="_blank" rel="noopener noreferrer">Code.org</a> to program simple games and later making games on <a href="https://scratch.mit.edu" target="_blank" rel="noopener noreferrer">Scratch</a>. I dug deeper into the rabbit hole of coding, learning the fundamentals of text-based coding languages (HTML and CSS) using <a href="https://www.freecodecamp.org" target="_blank" rel="noopener noreferrer">FreeCodeCamp.org.</a> After taking many breaks, another interest came to my mind: AI and machine learning. Therefore, I learned Python basics using YouTube video tutorials. <br>
**2. Addition to my portfolio:** I believe a blog would be a great addition to my coding portfolio, since I have never created any projects on as large of a scale as this. The only other text-based coding projects that I created were online quizzes that I gave up on and calculators that could be used to solve a problem with given variables. <br>
**3. To make learning about coding more accessible:** This is the most important reason for why I created this blog. Today's world is filled with online tutorials and courses that could cost people a fortune. I aim to provide tutorials, projects, and countless coding exercises that are 100% free and can be easily understandable by the average joe who doesn't know about coding. Since I am always striving to improve this blog, you can leave feedback on my GitHub repository. <br>
Before I go into detail about how you can create your own GitHub blog, it is important to know whether blogging is for you or not. Blogging is for you if: <br>
- You enjoy expressing yourself online and appreciate receiving constructive criticism.
- You intend to provide value to others whether it's by providing tutorials, promoting a product, giving insight about your life, and so on.
- You're not doing it solely for the money. If you do anything for the sole reason of making money, you're not putting real passion into your work.
Use these criteria to determine if blogging is for you. If not, don't worry! There are billions of things that programming can do for you, and many of them are lucrative, so watch out! <br>

Now, here's the fun part. Use this step-by-step guide to create a blog using GitHub pages and Jekyll. Before proceeding, make sure you have a GitHub account and a GitHub repository with the format: username.github.io in which username is your GitHub username in all lowercase. If you want a project site, feel free to use whatever repository name you like but that means changing the base URL that I will explain later. <br>
### Step 1: Create the _config.yml folder in your repository's root
The _config.yml determines the basic configuration for your blog. It is written in YAML (YAML Ain't Markup Language). Here is a default codeblock of the file:
```yaml
layout: # Name of your layout, we will get into layouts later
title: # Title of your blog
description: # Description of your blog
baseurl: "" # Leave this blank unless your repository is a project site with a custom name. If your repository is a project site, add / followed by your repository name.
url: "your-username.github.io" 
theme: null # I used no theme so I could customize it myself using CSS
markdown: kramdown # Jekyll uses Kramdown to parse Markdown code (turn it into HTML).
author: # Only add this line and an author's name if all posts will be written by the same author
```
If you want to use custom themes, go to <a href="https://github.com/topics/jekyll-theme" target="_blank" rel="noopener noreferrer">https://github.com/topics/jekyll-theme</a>
### Step 2: Create basic layouts
I recommend creating two layouts for now: a default layout for a homepage and about me page, and a layout for posts. I recommend using HTML (Hypertext Markup Language) to create them as HTML is a widely used markup language to control every webpage's structure. First, create a _layouts folder then add one HTML file per layout. From here, you can add HTML code for your layouts. Thanks to Jekyll integration, there are many commands that you can use to simplify layouts. I recommend adding the following to your layouts: <br>
- The site's metadata, found in the <head> element <br>
- The site's header, consisting of navigation links (Homepage, About Me, GitHub profile), the name of the blog and a short tagline to be displayed on all pages
- A heading for the title of the blog post or page
The following code should go into the main section of each of your webpages or the <main> element:
```html
<h1>{{ page.title }}</h1> <!-- Creates a heading with the title of your article/page -->
{{ content }} <!-- The main content of each of your webpages/posts. Can be written in HTML or Markdown. -->
```
- POSTS ONLY: Advanced features such as comments, post categories, post author/date/time (you don't need to worry about these for now)
I added a custom element in which all webpage titles end with "| Code Outside the Box" (my blog name). If you want to do something like this, copy the code into your layout's metadata:
```html
<title>{{ page.title }} | Code Outside the Box</title>
```
### Step 3: Create your blog's homepage and About Me page
You're going to have to create the 2 following files: index.html and about.html (the 2nd file could be a different name if you want to). The index.html file represents your homepage and it is necessary because it is the default file for any website, helping improve SEO (Search Engine Optimization). The about.html file represents your homepage. Write the following code into both files before the content:
```yaml
---
layout: default # Uses the default layout and saves time so you don't have to type the same HTML code in every webpage
title: About Me # The page's title and heading
---
```
You are free to use HTML or Markdown to write your content. Just change the file type to .md if you are going to use Markdown.

### Step 4: Add CSS and update your layouts with the correct CSS files
HTML represents the website's structure. However, CSS (Cascading Style Sheets) represents its styling and design. For example, let's say you have a pizza. HTML represents the dough; the pizza's base. CSS represents the toppings of the pizza. At this stage, I recommend creating a folder in your repository root called assets. This folder will store any external code and scripts, not just CSS. In this new assets folder, create a folder called css (all lowercase). From there, you can create CSS files ending in .css, so I created a file called main.css in the assets/css folder. However, to make sure the HTML code in your layouts processes the CSS, add the following line of code in your head's metadata for your layouts:
```html
<link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}"> <!-- Adjust main.css to whatever CSS file you want to use, it doesn't have to be the same CSS file for every layout but keep everything else the same -->
```
Once you're done adding this minor change, feel free to experiment with CSS! Try it on different elements and even classes, and use different properties with different values! Here is a short CSS snippet in my code:
```css
body {
  font-family: 'Lato', sans-serif; /* Displays the Lato font, otherwise displays sans-serif if the original font fails to display */
  background-color: #01163b; /* Uses this hexadecimal color code as the background */
  color: #ffffff; /* Text color throughout the entire website's content */
  padding: 2rem; /* Expands the border around the elements */
  line-height: 1.6; /* Adds some spacing between lines of text */
}
```
Note: I used a Google font for this. You have to add a special line of code to add Google fonts and items from external stylesheets.

### Step 5: Create your first post
I am at this step right now. Your first post doesn't have to be fancy or perfect - just have fun creating it! To do so, create a folder called _posts. In this folder, you can create HTML or Markdown posts. I am using Markdown since it is more convenient. Make sure you name the post file the following: <br>
YYYY-MM-DD-title-of-your-post.html (change to .md if you are using Markdown) <br>
Write the title of your post in all lowercase and separate spaces with hyphens so Jekyll recognizes the file.

### Final Thoughts
If you made it this far, you are awesome! You 100% have what it takes to create a blog of your own on GitHub! If you have any questions for me or if you just want to share your thoughts, drop a comment! I will be posting every day since I am on winter break right now. Anyways, see you next time and have fun coding!
