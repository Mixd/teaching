# Basics

This is the first section of the workshop which will aim to give you a simple understanding on how to get started with Responsive Web Design and more importantly, how to implement it into your projects.

## Task One
The files you'll need for this task are within the `task-1` folder. This task will aim to show you how to get a project setup for RWD and introducing you to the syntax for Media Queries

### Step 1 - Setting up a project
The first thing we need to do in a project is to tell our Browser how it will display the viewport. By default on mobile browsers, the viewport is scaled so that you can see the whole site and *pinch-and-zoom* to see the section you want. When we're creating a Responsive website, we don't need this, as our website already caters for the reduced viewport sizing on **any** device, be that Mobile, Tablets or Smart Watch.

**Your turn!**
- Open up `index.html` and find the `<head>` tag.
- Add the following meta tag to the head – `<meta name="viewport" content="width=device-width, initial-scale=1">` – while it can go anywhere in the `<head>` of your project, try and think about grouping the different parts together.

### Step 2 - Syntax introduction
Media Queries are awesome. Without them, Responsive Web Design simply wouldn't work. They're part of CSS, and as such, you'll put them within your CSS files. Here's a basic query:

```css
@media (min-width: 800px) {
    .box {
        background: #2ecc71;
    }
}
```

What this is actually telling the browser is, when a user comes to the site with a viewport width that is *larger than 800px wide*, then we'll give our `.content` selector the CSS property of `background: #2ecc71;`.

Lets break that down. First of all, we're declaring `@media`, which says we want to create a new media query. Next, comes our 'arguments' which in this example is `(min-width: 800px)`, and finally we have the curly brackets `{}` which wrap what we want to change once the 'arguments' are true (i.e. someone is viewing the site at a minimum of 800px wide).

Now, imagine we have the following within our CSS:

```css
.box {
    background: #3498db;
}

@media screen and (min-width: 800px) {
    .box {
        background: #2ecc71;
    }
}
```

This is telling us that by default we want to use the `background` of `#3498db` on our `.box`, and then once the browser is `equal to or larger than 800px` we will change its `background` to `#2ecc71`. This in a nutshell, is how we begin to build out our Responsive Websites. Imagine for a second you have four boxes, one underneath eachother (remember, you'll be working Mobile First) and then once you get up to a certain point (when theres room for them) you change their layout to a 2x2 grid. Media Queries make that happen. This is what you might have:

```css
.column {
    /* lots of cool styles */
}

@media screen and (min-width: 768px) {
    .column {
        float: left;
        width: 50%;
    }
}
```

> You can take a look at the `media-queries.md` file within the `5-extras` folder for a list of different Media Queries you can do, why they're useful, etc.

**Your turn!**
- Open up `styles.css`
- Write your own Media Query that changes the `.box-1` selector's `background` to `#e67e22` once the width of the browser is *at least 500px*. Resize your browser to see the changes.
- Next, write another Media Query which changes the `.box-2` selectors 'background' to `#e74c3c` once the width of the browser is *at least 500px*. (Multiple selectors can be in one Media Query). Resize your browser to see the changes.
- Lets change the `.box-1` selector's background change to be *when the browser is at least 800px*. Think about how you'll organise your CSS file, remembering that browsers read CSS files top to bottom.
