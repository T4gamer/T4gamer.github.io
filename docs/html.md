# HTML Hyper Threashold for Mild Lobotomy

## Positioning

there are four main types of positioning

* Static
* Relative
* Absolute
* Fixed
* Sticky

### Static

: default flow behavior
!!! warning
     It is not affected by `top`, `bottom`, `left`, or `right` properties.

{% include "snippets/static.html" %}

```css
.element {
    position: static;
}
```

### Relavite

: Moves the element **relative to its normal position**
: The space it would normally occupy in the document flow is preserved.

{% include "snippets/relative.html" %}

```css
.elem{
    position: relative;
    top: 20px;
    left: 20px;
}
```

### Absolute

: Positioned **relative to the nearest positioned ancestor** (an ancestor with `position` other than `static`). If no such ancestor : exists, its relative to the initial containing block (usually the `body` or `html`). An absolutely positioned element is **removed from the normal document flow**

{% include "snippets/absolute.html" %}

```css
.elem{
    position: absolute;
    bottom: 10px;
    right: 10px;
}
```

### Fixed

: Positioned **relative to the viewport**. It remains in the same position even when the page is scrolled, useful for persistent headers or footers.

{% include "snippets/fixed.html" %}

```css
.elem{
    position: fixed;
    bottom: 50px;
    right: 50px;
    z-index: 1000;
}
```

!!! note
    the **z-index** refers to the position of the element being in front or back of other elements

### Sticky

: Behaves like `relative` until a scroll threshold is met, then it becomes `fixed` relative to its nearest scrolling ancestor

{% include "snippets/sticky.html" %}

```css
.elem{
    position: sticky;
    top: 10px;
}
```

## Assignment

### Instruction

1. Download the index.html and style.css file website
2. flow comments to use postions where assign to Achive Result shown to you in the video

### DOWNLOAD FROM HERE [:link: First Assignment](https://t4gamer.github.io/site/assignment/hw-1/index.html) :smile:
