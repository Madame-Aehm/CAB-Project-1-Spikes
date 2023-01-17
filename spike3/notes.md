# Spike 3 notes

## CSS Grid

- **CSS Grid** divides the layout of your page into a literal grid - here's an excellent resource from [css-tricks.com](https://css-tricks.com/snippets/css/complete-guide-grid/)

- CSS Grid is yet another way to position content in an HTML document. Much like **Flexbox**, you will have a container element that holds children elements to be positioned within. The **display** property will be set to **grid** or **inline-grid** - the only difference will be how your grid container is positioned on the page, think of the difference in positioning behaviour between a **&lt;div&gt;** and a **&lt;span&gt;**.

### Grid-template-columns / grid-template-rows

- **Grid-template** with **columns** and/or **rows** is one of two ways to define the shape of your grid. The **grid-template-columns** and/or the **grid-template-rows** properties define the number and size of your rows and columns.

- The templates accept all standard HTML measurement units - **px**, **em**, **%**, etc. They will also accept **auto**, which fills remaining space, and the unique Grid unit **fr** (short for "fraction") which splits the remaining space between all **fr** columns/rows, but it can be specified how much of that space each unit will take. Example that splits into 4 fractions, with the middle column claiming 2 portions of the total:

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

- Grid **lines** are automatically assigned a number. **Positive** numbers when assigned "left -> right" and "top -> bottom", and **negative** numbers when assigned "right -> left" and "bottom -> top". You can also choose to give them your own names when you declare the template. Child items can be positioned within the grid using the lines, letting single elements span multiple grid cells. Example child item spanning 4 columns:

```css
.child-item {
  grid-column-start: 1;
  grid-column-end: 4;
}
```

- Positioning conflicts can cause some strange behaviours. Practise getting them right with the game [CSS Grid Garden](https://cssgridgarden.com/)!

### Grid-template-areas

- **Grid-template** with **areas** is the other way to define the shape of your grid. It can be used together with **grid-template-rows** and/or **grid-template-columns**, or it can be used to initialize the grid itself, however the size of the cells will be determined by the content if you don't set the row/column sizes.

- The **grid-template-areas** property accepts the **names** of the areas in each row surrounded by **quotation marks**. Each set of quotation marks represents a column. Each row needs to have the same number of cells in order to have correctly aligning columns. Example of 3 row, 4 column grid:

```css
div {
  display: grid;
  grid-template-areas:
    "header header header header"
    "main main ... sidebar"
    "footer footer footer footer";
}
```

- One or multiple (so long as there are no spaces between them) **full-stops** ( **.** or **....** ) symbol/s represent an empty cell.

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
