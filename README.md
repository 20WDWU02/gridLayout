# Grid Layout

This project contains a 12 column css grid for making websites.
Using the example bellow, you can use rows and columns to create layouts for your websites.

```html
<!-- a row with 3 columns that have 3 different sizes -->
<div class="row">
    <div class="col col4"></div>
    <div class="col col2"></div>
    <div class="col col6"></div>
</div>

<!-- a row with 2 even columns -->
<div class="row">
    <div class="col col6"></div>
    <div class="col col6"></div>
</div>

<!-- 
  The main row has 2 columns which goes over 8 and 4 columns. 
  Inside the first (8) column, there is another row which has 2 even columns inside of that.
-->
<div class="row">
    <div class="col col8">
      <div class="row">
          <div class="col col6"></div>
          <div class="col col6"></div>
      </div>
    </div>
    <div class="col col4"></div>
</div>
```
Layout includes columns from 1 - 12.  
All of your rows should count up to 12 columns and all your columns should be included in a row.  
This should just be used for the skeleton for your website not the content itself. Because most elements are block elements, they should just stretch out to fill your columns.  

You can include more rows inside your columns if need be.  

# Responsive Design  
In this project we also start to look at responsive design.  
Responsive Design is about making your webpage look good on all devices (desktop, tablet and mobile). As a developer and ddesigner it is our job to make sure that it is responsive.

### Setting the Viewport
Before we start to make our site responsive, we need to include this meta tag in the head of your webpage. This will tell your browser the size of the viewport and the scale it needs to be.  
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
### Media Queries
w3schools has a great article on media queries [here](https://www.w3schools.com/cssref/css3_pr_mediaquery.asp)  


Media Queries are the CSS tools for making elements have different CSS properties apply to them on different **media types**.  
There are 4 different media types you can use
* all
* screen
* print
* speech

Depending on who/what your users will be doign on your webpage, you will use the appropriate media type.  
Along with the media type, you need to set the **media feature**. There is a large list of features you might use but the commmon ones are **min-width** & **max-width**. You can find a list of all the feature types on the w3schools link above.

```css
/*
@media mediatype and (mediafeature:value){

}
*/

@media screen and (min-width: 600px) {
  .box {
    display: none;
  }
}
```
In the example above, we have created a media query for when your device is at least 600px wide. If that applys, the element with the class of box will have display:none.  
When the screen is between 0 and 599px, it won't hvae display:none.

# Responsive Grid Layout
We have now expanded on our grid to make a responsive grid.  
Using media queries we created more columns that trigger on different screen sizes.  
The format for our grid is simple

* .col* - number columns on at least a small screen
* .colM* - number columns on at least a medium screen
* .colL* - number columns on at least a large screen

```html
<div class="row">
    <!-- 
        On a small screen, these two elements will go over 12 columns, 
        on a medium device 6 columns and a large device 4 columns  
    -->
    <div class="col col12 colM6 colL4"></div>
    <div class="col col12 colM6 colL4"></div>
    <!-- 
        This element is different though. 
        On a small screen it goes over 12 columns and stays that way until it gets to a large screen
        where it then changes to 4  
    -->
    <div class="col col12 colL4"></div>
</div>
```

