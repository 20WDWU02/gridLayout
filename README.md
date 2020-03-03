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
