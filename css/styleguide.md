# TMG's Frontenders CSS and SCSS Styleguide {

## Table of Contents

1. [General Style](#general-style) 

## General Style

- Use tabs for indentation.

- Avoid the use of `!important` as much as _absolutely_ possible.

- If the value of a property is `0`, do not specify units.

   ```css
   // good
   padding-top: 0;
   
   // bad
   padding-left: 0px;
   ```
   
- Unless there is a really good reason to, _avoid_ using IDs for CSS styling.

- When using colors, always use a `$variable`. Either creating a new one if it's a new color, or reusing the existing ones. Use of the `darken()` and `lighten()` Sass functions is encouraged.

	```css
	// good
	$white: #fafafa;
	$header-background: $white;
	
	.tag-page-header {
		background-color: $header-background;
	}
	
	.tag-page-title {
		color: darken($white, 50%);
	}
	```

**[⬆ back to top](#table-of-contents)**

#}