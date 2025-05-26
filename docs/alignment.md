# Alignment

## Flexing A Row and Column

`The way of a designer is a nested one`

## A Row

* The .row class creates a flex container.
* `display: flex;` enables flexbox layout on the element.
* `flex-direction: row;` arranges child elements horizontally in a row.
* `flex-wrap: wrap;` changes items arrangement if the width of the row got too small {==wraping the row so it fits the items==}

```css
.row {
    display: flex;
    flex-direction: row;
    border: 2px dashed var(--border-color);
    flex-wrap: wrap;
    gap : 10px;
    padding: 10px;
}
```

: result with some Items to  give it a height

{%include "snippets/align/simple_row.html" %}

### Align da Row

!!! note
    the main axis of a Row is `the Vertical Axis`, the arrangement of the content can be change with justify-content style

{%include "snippets/align/simple_row_align_cont.html" %}

```css title="Center content of div" hl_lines="8 9"
.row { 
    display: flex;
    flex-direction: row;
    border: 2px dashed var(--border-color);
    flex-wrap: wrap;
    gap : 10px;
    padding: 10px;
    /* the justify content affecting the main axis of a Row*/
    justify-content: center; 
}
```

!!! note
    the gap property is used to give a space between the content inside the Row

### other values of justify content

* space-between
* space-around
* space-evenly

: example around

{%include "snippets/align/simple_row_space_around.html" %}

```css title="space-around"
.row { 
    /* the rest of the properties*/
    justify-content: space-around; 
}
```

: example start

{%include "snippets/align/simple_row_start.html" %}

```css title="start"
.row { 
    /* the rest of the properties*/
    justify-content: start; 
}
```

: example end

{%include "snippets/align/simple_row_end.html" %}

```css title="end"
.row { 
    /* the rest of the properties*/
    justify-content: end; 
}
```

## Columns

: good example of a dynamic Column
!!! note
    it is recommended that the column is given 100% width by trial you will discover that it is much simpler to work with the column with this

!!! note
    box-sizing redfines the interaction between the elemments making it much more stable and predictable and less prone to face issues with overflow
{%include "snippets/align/simple-column.html"%}

```css
.column {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    width: 100%;
}
```
