# Mobile First/Responsive CSS Grid

### Defining columns in SASS
In the SASS doc you can edit the `$columns` list to define your layout.
Currently: `$columns: one, two, /* ... */ sixteen;`

```scss
$columns: one, two, three, four, five, six, seven, eight, nine, ten, eleven, twelve;
// or
$columns: one, two, three, four, five, six, seven, eight, nine, ten;
// or what ever you want..
```

### Defining the number of columns
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

### Defining column span
Adding a class of `five` doesn't mean that you have to have five columns.
You can also define how each column is split. The example below creates two columns, one at 40% width and the other at 60%.

```html
<div class="row five">
	<div class="column two"></div>
	<div class="column three"></div>
</div>
```

### Mobile first or responsive?
Setting the `$mobile-first` variable to `true` builds the media-queries to using `min-width`.
This also makes a difference in the class modifier used with the `row` class.
The class modifier for `$mobile-first: true` would be `grid-at-[break-point]`.
The class modifier for `$mobile-first: false` would be `stack-at-[break-point]`.
See Stacking columns below for more information.

### Defining breakpoints in SASS
In the SASS doc you can edit the `$break-points` list to define at which screen sizes the columns are stacked.
Currently: `$break-points: 320, 480, 640;`

```scss
$break-points: 321, 481, 641;
// or
$break-points: 769, 961, 1025;
// or, again, what ever works for your project...
```

### Stacking columns
You can add a class of `stack-at-[break-point]` to make your grid responsive or add a class of `grid-at-[break-point]` for mobile first,
where `[break-point]` is one of the defined breakpoints in SASS.
Adding this class will make the columns stack and span 100% at or under the specified `[break-point]`.
The example below will stack the columns when the screen is at or under 320px.

```html
<div class="row five stack-320">
	<div class="column two"></div>
	<div class="column three"></div>
</div>
```
