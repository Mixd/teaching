# Layouts
Now that we've covered the basics section, you should have rudementary understanding of how Media Queries work and how you can use them, lets kick things up a notch and think about how we can use Media Queries for a Responsive Website.

## Task One
The files you'll need for this task are within the `task-1` folder. This task will introduce you to using Media Queries for layout-based changes.

### Step 1
The most common of layouts is the standard article & sidebar. Lets try creating that. If you take a look at the `index.html` file, you'll see the HTML has been already created for you. All that's left to do now is add styling once the viewport gets large enough for the sidebar to be *floated* to the right of the content. Media Query time!

**Your turn!**
- Within your `styles.css`, create a Media Query which will change the `width` and `float` of the `.content` & `.sidebar` once the viewport is at a point that warrants the change.
- Remember, when you're using floats you'll need to remember to use a clearfix, the `.clearfix` class will work fine, apply that to your `.container`.

### Step 2
Now that we have the layout structure sorted, lets apply some styling and get that designer's mind working. Think about what styling you can apply to the `.content` and `.sidebar`, whether or not the styles should be applied in a Media Query or not, and what each element would look like on a mobile.

Go on to Task Two when you feel ready.

## Task Two
The files you'll need for this task are within the `task-2` folder. This task will be an introduction to Grids within a Responsive Website.

### Step 1
Open up `index.html` and `styles.css`, you'll see I've created a really simple Grid. It'll be perfect to get your head around layouts in RWD. Lets break it down a little.
1. First of all, we have the `.container` as you've previously seen, this isn't part of the grid, its just a wrapper which in theory would wrap our entire site (assuming thats what we want to do for the design).
2. The grid actually starts by giving a block element the class of `.grid` and because this is a float-based layout, we'll need to apply the `.clearfix` too.
3. Within this, we'll add our columns/units. Percentages are used for the widths of these units and are applied by applying the second class to the `.unit` div.
4. The best is, you can add your own unit values. We'll come onto that soon.

**Your turn**
- Try adding some more *quarter* and *half* columns, looking at the `index.html` as a reference. 
- Add your own values! Think about how large you'll want your columns.
- For brownie points, think about how you could create a 12 column grid with percentages. oooo!