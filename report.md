<!-- If you want to embed images, this is how you do it:

![Image of CSS](https://cdn.pixabay.com/photo/2017/08/05/11/16/logo-2582747_960_720.png) -->
<p align="center">
  <img src="https://cdn.pixabay.com/photo/2017/08/05/11/16/logo-2582747_960_720.png" width="200" />
</p>

# SHORT-REPORT ON CSS GRID AND FLEXBOX

 Written by **`Sutirtha Dey`**

## Topics

<!--ts-->
- [CSS GRID](#CSS-GRID)
    - [What is a CSS Grid](#What-is-a-CSS-Grid)
    - [Supported Browsers](#Supported-Browsers)
    - [Grid Elements](#Grid-Elements)
    - [Display Property](#Display-Property)
    - [Adjusting Rows and Columns](#Adjusting-Rows-and-Columns)
    - [Grid template Properties](#Grid-template-Properties)

- [CSS FLEXBOX](#CSS-FLEXBOX)
    - [What is a Flexbox](#What-is-a-Flexbox)
    - [Supported Browsers](#Supported-Browsers)
    - [Flexbox Container](#Flexbox-Container)
    - [Flexbox Container Properties](#Flexbox-Container-Properties)
- [Reference](#Reference)
<!--te-->


# CSS GRID
## _What is a CSS Grid_

**`A CSS grid`** can be described as a two-dimensional figure, consisting of rows and columns. **`A CSS grid`** layout divides a webpage into different parts or regions. The grid system is flexible in terms of designing, it makes the designing of web pages easy without using position and float properties.

It allows users to arrange items into rows and columns in the same way that a table does. In comparison to tables, however, the **` CSS Grid`** makes designing layouts much easier. Using the grid-template-rows and grid-template-columns attributes, we can specify columns and rows on the grid.
## _Supported Browsers_
The **` CSS Grid`** properties are supported by all modern browsers.

- Google Chrome
- Mozilla Firefox
- Internet Explorer
- Safari
- Opera
## _Grid Elements_
A grid layout or structure is made of a parent element, which will have one or more child elements.

The grid container can be defined by setting an element's display property to grid or inline-grid.
Grid items are grid items that are placed inside rows and columns of a grid container.
```sh
<div class="container-grid">
  <div class="item-grid">one</div>
  <div class="item-grid">two</div>
  <div class="item-grid">three</div>  
  <div class="item-grid">four</div> 
</div>
```
## _Display Property_
An HTML element becomes a grid container when its display property is set to grid or inline-grid.
```sh
.container {
    display: grid;
}
```
or 
```sh
.container {
    display: inline-grid;
}
```
## _Adjusting Rows and Columns_
we can adjust gaps between rows and columns using the properties grid-column-gap and grid-row-gap
```sh
.container {
    display: grid;
    grid-column-gap: 50px;
}
```
```sh
.container {
    display: grid;
    grid-rows-gap: 50px;
}
```
There is a shorthand property called grid-gap which we can use to specify the gaps between columns and rows togather in one go.
```sh
.container {
    display: grid;
    grid-gap: 50px 100px;
}
```
This property will set the grid-row-gap to 50px and grid-column-gap to 100px.
## _Grid template Properties_
The grid-template-columns property specifies the number of columns and the width of each column in your grid layout.
The value is a space-separated list, with each value defining the width of the column it belongs to.
```sh
.container {
    display: grid;
    grid-template-columns: auto auto;
}
```
The above code will create two columns with equal width, since "auto" is set. Similarly,
```sh
.container {
    display: grid;
    grid-template-columns: 20px 30px 100px;
}
```
Here three columns of width 20px, 30px and 100px will be created as mentioned in above.
The grid-template-rows property specifies the number of rows and the width of each rows in your grid layout.
```sh
.container {
    display: grid;
    grid-template-columns: 20px 30px 100px;
}
```
Here three columns of width 20px, 30px and 100px will be created as mentioned above.

```sh
.container {
    display: grid;
    grid-template-columns: 20px 30px 100px;
}
```
Here three rows of width 20px, 30px and 100px will be created as 
mentioned above.


# CSS FLEXBOX
## _What is a Flexbox_
The Flexible Box Module, often known as flexbox, was created as a one-dimensional layout model and a way for providing space distribution and powerful alignment capabilities between elements in an interface.

There were four layout modes before the Flexbox Layout module:
- Block, for sections in a webpage
- Inline, for text
- Table, for two-dimensional table data
- Positioned, for the explicit position of an element

The Flexible Box Layout Module simplifies the creation of flexible responsive layout structures without the use of floats or positioning.
## _Supported Browser_
The **` CSS Grid`** properties are supported by all modern browsers.

- Google Chrome
- Mozilla Firefox
- Internet Explorer
- Safari
- Opera
## _Flexbox Container_
To start using the flexbox, we need to first define a flex container. We can add a flex container with several flex items as:
```sh
<div class="container-flex">
  <div class="item-flex">one</div>
  <div class="item-flex">two</div>
  <div class="item-flex">three</div>  
  <div class="item-flex">four</div> 
</div>
```
The flex container becomes flexible by setting the display property to flex:
```sh
.container-flex {
    display: flex;
}
```
## _Flexbox Container Properties_
The Flex container properties are:
- **`flex-direction**

  - flex-direction property is used to define in which direction the flex items will be stacked in the container. It has four direction options- row, row-reverse, column, and column reverse.

    - **`flex-direction: row;`** stack the flex-items from left to right.
    - **`flex-direction: row-reverse;`** stacks the flex-items from right to left, in reverse order.
    - **`flex-direction: column;`** stacks the flex item from top to bottom.
    - **`flex-direction: column-reverse;`** column-reverse will do the opposite, it will stack the flex-items from bottom to top.
- **`flex-wrap`**
  - The flex-wrap property determines whether or not the flex elements will be wrapped.
    - **`flex-wrap: nowrap;`** it doesn't wrap anything.
    - **`flex-wrap: wrap;`** wraps the overflow items into a next row or next column.
    - **`flex-wrap: wrap-reverse`** wraps the overflow items into a top row or left column.
- **`flex-flow`**
  - flex-flow combines the propeties of flex-direction and flex wrap into a single property.
```sh
   .container-flex
    {
        display: flex;
        flex-flow: row wrap;
    }
```
This property will set the **`flex-direction: row;`** and **`flex-wrap: wrap;`**
- **`justify-content**
  - justify-content property is used to align items with respect to the main axis.
    - **`justify-content: center;`** will align the items at the center of the container.
    - **`justify-content: flex-start;`** will align the items from the starting of the container.
    - **`justify-content: flex-end;`** will align the items from the end of the container.
     
- **`align-items**
  - align-items property defines how the alignment should be along the cross axis.
    - **`align-item: stretch;`** This will stretch the items for filling the entire space.
    - **`align-item: flex-start**  This property will stack the items from start.

    - **`align-item: flex-end;`** will align the items from the end of the container.
    - **`align-item: centre;`**
    This will align the items vertically in the central position of the container.

# Reference
- https://www.w3schools.com/css/css_grid.asp
- https://www.javatpoint.com/css-grid
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox
- https://www.geeksforgeeks.org/introduction-to-css-flexbox/

