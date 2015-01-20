# Responsive Measurements
Difference between the different measurements in CSS and how you can use them in your Responsive Projects.

## pixel
Pixels are ultimately what the Web is made on – Pixels. While this is true, they are not a great measurement to work with when creating Responsive Websites. Personally, I'd only ever use them in Media Queries, although most of the time I'll use em's for that too.

## em
Em's (a.k.a elastic measurements) are a little different. While they still ultimately convert to Pixels, they're a measurement that it *relative* to its parent font-size. The default font-size on the web is **16px**, so this is what we will work from. Assuming we have the following with no other styling:

```html
<body>
    <h1>This is the Heading One</h1>
</body>
```

This is what different em's would equal:

Ems | Pixels | Calculation
--- | --- | ---
.5em | 8px | .5 x 16
1em | 16px | 1 x 16
1.5em | 24px | 1.5 x 16
2em | 32px | 2 x 16
2.25em | 36px | 2.25 x 16

However, where things get a little more complicated, is when you've defined a sizing on a parent. Take for example the following HTML:

```html
<body>
	<div class="box">
		<h1 class="heading"></h1>
	</div>
	
	<style type="text/css">
		.box {
			font-size: 1.5em; /* 24px */
		}
		
		.heading {
			font-size: 2em; /* 48px */
		}
	</style>
</body>
```

Confused? Don't worry. Let's break it down.

1. First of all, we start with our default font size of 16px.
2. Next, we times that by 1.5 to get the size of our `.box`, which is `24px`
3. Finally, because the `.heading` is within the `.box`, we need to times our 1.5em (which is 24px) by 2, which gives us 48px.

### Whats the benefit?
They're relative. Imagine for a second you have a user who needs to increase the font-size as they have bad eye-sight. If you're using em's, all the font-sizes will increase when they user changes their browsers default font size. Keeping everything nice and even.

### Including thoughts

All in all, em's can be confusing, but they're a great addition to a responsive website Personally, I don't use em's for font-sizing, however, I will use them for widths, paddings, margins etc (they're relative to the parent's `font-size` only remember).

## rem

Rem's (relative elastic measurements) are like Em's younger, smarter brother. It takes the things we love about em's (relativity to default size) but removes the things we don't like (relative to parent).

Where em's are relative to their parents, rem's are *only* relative to the default font-size set on the `<html>` tag.

Take the following:

```html
<body>
	<div class="box">
		<h1 class="heading"></h1>
	</div>
	
	<style type="text/css">
		.box {
			font-size: 1.5rem; /* 24px */
		}
		
		.heading {
			font-size: 2rem; /* 32px */
		}
	</style>
</body>
```

As you can see, the `.heading` is now 32px because its relative to the font-size of the `<html>` tag, which by default is 16px.

### Whats the benefit?
The exact same benefits as em's, without all the added calculations.

*As a recommendation, I'd say for you to use Rem's as your measurement of choice in font-sizing.*

## Percentages (%)
Best used on anything but font-sizing, percentages are just that, percentages of their parents. Take the following:

```html
<body>
	<div class="box">
		<h1 class="heading"></h1>
	</div>
	
	<style type="text/css">
		.box {
			width: 500px;
		}
		
		.heading {
			width: 100%; /* 500px */
		}
	</style>
</body>
```

The `.heading` will go `100%` of the width of its parent, in this case that means it'll be given the value of `500px`.

Imagine if we changed that above CSS to the following:

```css

.box {
	width: 500px;
}

.heading {
	width: 50%; /* 250px */
}
```

You'd then have to calculate what 50% of its parent is, which in this case is the following: `50% of 500px = 0.5 x 500px = 250px`. You finally get to use your math skills you learnt in high school, [can I get a hell yeah?](http://replygif.net/i/1072.gif)