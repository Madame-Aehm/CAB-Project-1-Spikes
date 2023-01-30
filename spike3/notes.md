# Spike 3 notes

## CSS Grid

- **CSS Grid** divides the layout of your page into a literal grid - here's an excellent resource from [css-tricks.com](https://css-tricks.com/snippets/css/complete-guide-grid/)

- CSS Grid is yet another way to position content in an HTML document. Much like **Flexbox**, a "container" element holds "children" elements to be positioned within. The **display** property will be set to **grid** or **inline-grid** - the only difference will be how your grid container is positioned on the page, think of the difference in positioning behaviour between a **&lt;div&gt;** and a **&lt;span&gt;**.

### Grid-template-columns / grid-template-rows

- **Grid-template** with **columns** and/or **rows** is one of two ways to define the shape of a grid. The **grid-template-columns** and/or the **grid-template-rows** properties define the number and size of your rows and columns.

- The templates accept all standard HTML measurement units - **px**, **em**, **%**, etc. They will also accept **auto**, which fills remaining space, and the unique Grid unit **fr** (short for "fraction") which splits the remaining space between all **fr** columns/rows. Example of 3 columns split into fractions:

```css
div {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}
```

- **repeat** keyword can be used to prevent repetition. eg:

```css
div {
  display: grid;
  /* grid-template-rows: auto auto auto; */
  grid-template-rows: repeat(3, auto);
}
```

- Grid **lines** are automatically assigned a number. **Positive** numbers indicate "left -> right" and "top -> bottom", and **negative** numbers "right -> left" and "bottom -> top". You can also choose to give them your own names when you declare the template. Child items can be positioned within the grid using the lines, letting single elements span multiple grid cells. Example child item spanning 4 columns:

```css
.child-item {
  grid-column-start: 1;
  grid-column-end: 4;
}
```

- Positioning conflicts can cause some strange behaviours. Practise getting them right with the game [CSS Grid Garden](https://cssgridgarden.com/)!

### Grid-template-areas

- **Grid-template** with **areas** is the other way to define the shape of your grid. It can be used together with **grid-template-rows** / **grid-template-columns**, or it can be used to initialize the grid itself (in this case the size of the cells will be determined by the content).

- The **grid-template-areas** property accepts **names** of the areas in each row. Each set of quotation marks represents a column. Each row needs to have the same number of cells in order to have correctly aligning columns. Example of 3 row, 4 column grid:

```css
div {
  display: grid;
  grid-template-areas:
    "header header header header"
    "main main ... sidebar"
    "footer footer footer footer";
}
```

- One or multiple **full-stop** ( **.** or **....** ) symbols represent an empty cell.

- Instead of using the numbers associated with the **grid lines**, you can now use the area name to indicate the start/end positioning of your child elements, or use the **grid-area** property to position that element over the entire area. eg:

```css
.child-div {
  grid-area: header;
}
```

- Gaps between your cells can be added using the **gap** property.

- Very similar to Flexbox, CSS Grid lets you use **justify-items** and **align-items** to position the child-item inside the cell, and **justify-content** and **align-content** to position the grid inside the container. All the same values are available, but the syntax is a little bit different: **start**, **end**, **center**, **space-between**, etc. The properties **place-items** and **place-content** are shortcuts to set both justify and align values the same.

- On the child-item, **justify-self**, **align-self**, and **place-self** properties can also be used to position itself within the grid cell.

### Media Queries

- **Media Queries** can be used to conditionally apply styles based on **media type** or **media feature**. The media type, which is optional, for our use will usually be **screen**. If no media type is specified, it is assumed to be **all**. A list of media features can be found on [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries).

- The most useful media feature for our projects will be **width**, which refers to the pixel width of the viewport. I have also found **hover** to be useful to prevent some strange behaviour from hover styles on touchscreen devices. Example that shows a background change when the device screen width is less than 600px:

```css
div {
  background-color: bisque;
}

@media screen and (max-width: 600px) {
  div {
    background-color: antiquewhite;
  }
}
```
