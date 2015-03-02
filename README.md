# Simple CSS Grid Layout

## Defining the number of columns
-------------------------------
Class `row` or `row one` makes all child elements of class `column` span full width.
Add class `two` through `sixteen` to define the number of columns. This will set the width of each column equally.
The markup below adds five columns each at 20% width.

```html
<div class="row five">
	<div class="column"></div>
	<div class="column"></div>
	<div class="column"></div>
	<div class="column"></div>
	<div class="column"></div>
</div>
```

## Defining column span
-------------------------------
Adding a class of `five` doesn't mean that you have to have five columns.
You can also define how each column is split. The example below creates two columns, one at 40% width and the other at 60%.

```html
<div class="row five">
	<div class="column two"></div>
	<div class="column three"></div>
</div>
```