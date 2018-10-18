# Advanced
This section will allow you to explore a more complex layout for Responsive Web Design.

In task four you handled the the sub-elements often found in a header. Whilst difficult, the header is often handled in isolation. Now you have to handle the complexities of nested grid layouts.

## Task 1
The files you'll need for this task are within the `task-1` folder.

The content section has a selection of images (aka. a gallery), and to make best use of the available space, it makes sense to stack them to a row. But...

* how many to a row? Do you do 3 then 4 then 5
* there's also a sidebar...when should it be beside the content? How does that affect the gallery?
* there's panels in the sidebar, shouldn't they be gridded making efficient use of space?

You may want to look back on `2-layouts/task-2` for inspiration, and perhaps work upon that basic grid to make something work for this layout.

## Task 2
The files you'll need for this task are within the `task-2` folder.

This task is identical to Task 1, but you've been supplied the gift of [Groot](https://github.com/lukewhitehouse/groot): a grid system Mixd use on all of our projects. Like many grid systems, Groot takes out a lot of the heavy-lifting of managing complex grids. It has preset breakpoints and a 12-piece grid system already done for you. It allows you to focus on how you want the elements to re-arrange without getting bogged down in the details of the CSS. Groot is particularly good because:

* it's easy...it's fractions. A 25% split is just `.grid__item--3-12`.
* it's versatile...you can change layouts on a per breakpoint basis, by just adding `-bp#` to the end (eg. `grid__item--3-12-bp2`).

**BUT BE WARNED:** using grid frameworks are not a replacement for actually knowing how this stuff works. It's to stop you re-inventing the wheel and writing the same gridding code (like Task 1) over and over again.

Task 2 is simple: do the same as Task 1 but using Groot.
