# Alignment

## Flexing A Row and Column

`The way of a designer is a nested one`

## A Row

* The .row class creates a flex container.
* `display: flex;` enables `flexbox` layout on the element.
* `flex-direction: row;` arranges child elements horizontally in a row.
* `flex-wrap: wrap;` changes items arrangement if the width of the row got too small {== wrapping the row so it fits the items==}

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

#### Centered content

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

#### space around Content

{%include "snippets/align/simple_row_space_around.html" %}

```css title="space-around"
.row { 
    /* the rest of the properties*/
    justify-content: space-around; 
}
```

#### content at the start of the row

{%include "snippets/align/simple_row_start.html" %}

```css title="start"
.row { 
    /* the rest of the properties*/
    justify-content: start; 
}
```

#### content at the end of the row

{%include "snippets/align/simple_row_end.html" %}

```css title="end"
.row { 
    /* the rest of the properties*/
    justify-content: end; 
}
```

### cross axis alignment

: if you have noticed all the previous examples work on the `main axis of the row` which is the horizontal axis we have also what is called a `cross axis` in the case of a row it is the vertical axis we can control it is position using the `align-items` property

```css
{
    /*rest of css properties*/
    justify-items: center;
}
```

#### [:link: align-items property reference](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)

: reference listing all possible values for align items

## Columns

!!! note
    it is recommended that the column is given 100% width by trial you will discover that it is much simpler to work with.

!!! note
    box-sizing redefines the interaction between the elements making it much more stable and predictable and less prone to encounter overflow issues

### example of a dynamic Column

#### no alignment applied

{%include "snippets/align/simple-column.html"%}

```css
.column {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    width: 100%;
}
```

#### align cross axis

{%include "snippets/align/simple-column-center.html"%}

```css
.column {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    width: 100%;
    align-items: center;
}
```

!!! note
    all alignment methods described for the Row can also be used on the Column example Above
    since it all a `Flex Box` only difference begin the `flex-direction`

!!! warning
    align properties decribed for the Row is reversed in the Column
    such as the `justify-content` being a `Cross Axis` and the `align-items` being on the `Main Axis`

## Example of Nesting ROW and COL

```html title="login.html"
    <div>
        <H1>LOGIN</H1>
        <form>
            <div>
                <input type="text">
                <input type="text">
                <div>
                    <button >Login</button>
                </div>
            </div>
        </form>
    </div>
```

: the below shows the result of the html with no alignment

{%include "snippets/align/login_no_style.html" %}

: and this is after including only a column and row class

```html
<div class="row">
        <div class="col">
            <H1>LOGIN</H1>
            <form>
                <div class="col">
                    <input class="ex" type="text">
                    <input class="ex" type="text">
                    <div class="row">
                        <button class="ex">Login</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
```

```css
.row {
        display: flex;
        flex-direction: row;
        gap: 16px;
        flex-wrap: wrap;
        margin: 0% auto;
        justify-content: center;
    }

    .col {
        display: flex;
        flex-direction: column;
        width: 100%;
        margin: 0% auto;
        box-sizing: border-box;
        align-items: center;
        gap: 1em;
    }
```

{%include "snippets/align/login_style.html" %}
