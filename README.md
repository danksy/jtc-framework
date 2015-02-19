# Just to Confirm (JTC) Framework

Responsive front-end web framework developed using Sass.

### Licence

The MIT License (MIT)

Copyright (c) 2015 Daniel Jackson

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

### Current Version

0.1.1

### Changelog

0.1.1 / 19 February 2015

- Header
- Footer
- Border
- Center Block Elements
- Center Text
- Responsive/Fluid Images
- Full-width Banner Image
- Button - full-width when responsive
- Grid increased in size when used on the iPhone in landscape view

0.1 / 13 February 2015

- Buttons
- Border-Radius
- Vendor Prefix Mixin
- Clearfix
- Grid
- Box
- Border-Box Mixin

### Contributors

- Daniel Jackson

## Documentation

### HTML Structure

Open a text-editor and copy the HTML structure (below) into a new file.  Save the new file as `index.html` or use another file name but save using the `.html` file extension.

This example includes the JTC framework as a CSS file.

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="utf-8" />
	<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta name="HandheldFriendly" content="True">
	<meta name="MobileOptimized" content="320">
	<meta name="description" content="" />
	<meta name="author" content="" />

	<title>Page Title</title>

	<link rel="stylesheet" type="text/css" href="jtc-main.css" />
</head>
<body>
	... page content here ...
</body>
</html>
```
Any content to be added to the page must be placed between `<body>` and `</body>`.

### Installation

Once the CSS (Cascading Style Sheet) file has been downloaded, place the code (below) between the `<head>` and `</head>` tags of the page.

```
<link rel="stylesheet" type="text/css" href="jtc-main.css" />
```

Any changes to Sass files will need to be pre-compiled before being converted to CSS within your project.

### Button

A very simple button.

```
<button>Button</button>
```

The default `<button>` styling can be changed within the `utils/variables.scss` Sass file:

- `$button-color`
- `$button-color-hover`		
- `$button-color-text`		


### Button - Curved Border

A button with a curved border/border-radius

```
<button class="curved-border">Button</button>
```

Change the border-radius size within the `utils/variables.scss` Sass file:

- `$border-radius:`

### Button - Custom Buttons

Style multiple buttons using individual class names.

```
<button class="name-button">Button</button>
```
`name-button` is an example name for the documentation.  This does not currently exist within the framework.

Secondary Styled button

```
<button class="secondary-button">Button</button>
```

Alert button

```
<button class="alert-button">Button</button>
```
Success button

```
<button class="submit-button">Button</button>
```

The custom `<button>` styling can be changed within the `components/buttons.scss` Sass file:

- `@include button('secondary', #e7e7e7, #b9b9b9, #333333, 0);`
- `@include button('success', #43ac6a, #368a55, #ffffff, 0);`
- `@include button('alert', #f04124, #cf2a0e, #ffffff, 0);`

Further custom buttons can be added if required and setting the parameters as such:

- @param1 - button name
- @param2 - colour
- @param3 - hover colour
- @param4 - text colour
- @param5 - border

Example Code: 

- `@include button('mybutton', #000000, #b9b9b9, #ffffff, 0);`

- `<button class="mybutton-button">My Button</button>`

### Border

Simple Border

```
<div class="border">
...
</div>
```

The default border styling can be changed within the `utils/variables.scss` Sass file:

- `$border-width`
- `$border-type`
- `$border-color`

### Box

A box is a panel and used as a container for content on the page. 

```
<div class="box">
...
</div>
```

The default box styling can be changed within the `utils/variables.scss` Sass file:

- `$box-color`

### Images

Responsive/Fluid images. Each image will require a description within the `alt` attribute and the file path/url of the image to be used needs to be placed between the `src` attribute.

```
<img src="..." alt="image description">
```

### Header

Add a full width header to the page.

```
<header>
...
</header>
```

The `header` styling can be changed within the `utils/variables.scss` Sass file:

- `$header-color`
- `$header-height`

### Footer

Add a full width footer to the page.

```
<footer>
...
</footer>
```

The `footer` styling can be changed within the `utils/variables.scss` Sass file:

- `$footer-color`
- `$footer-height`

### Full Page Banner Image

Create a full-width banner image.

```
<section class="banner"></section>
```

The default banner styling can be changed within the `utils/variables.scss` Sass file:

- `$banner-image`
- `$banner-height`
- `$banner-position`
- `$banner-repeat`
- `$banner-background-size`

### Center Elements

Center `block` elements and non-inline elements such as: `<h1>`,`<p>`,`<div>` and `<ul>`.

```
<div class="center">
...
</div>
```

### Center Text

Center-align text.

```
<div class="center-text">
...
</div>
```

### Grid

The Framework Grid Structure.

```
<section class="wrapper">
	<div class="row">
		<div class="column-x">
			<div>
				.. content within the grid here ..
			</div>
		</div>
	</div>
</section>
```
- `x` indicates the grid size - 1 to 12. For example, to create a full-width column the class would read as: `<div class="column-12">`:

```
<section class="wrapper">
	<div class="row">
		<div class="column-12">
			<div>
				.. content within the grid here ..
			</div>
		</div>
	</div>
</section>
```

The number of columns should total no-more than `12`

```
<section class="wrapper">
	<div class="row">
		<div class="column-6">
			<div>
				.. content within the grid here ..
			</div>
		</div>
	</div>
</section>
<section class="wrapper">
	<div class="row">
		<div class="column-6">
			<div>
				.. content within the grid here ..
			</div>
		</div>
	</div>
</section>
```

The columns `(6+6) = 12`, therefore, this is fine.

### Website

[http://www.justtoconfirm.co.uk](http://www.justtoconfirm.co.uk)