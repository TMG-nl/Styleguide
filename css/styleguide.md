# TMG's Frontenders CSS and SCSS Styleguide {

## Table of Contents

1. [General Style](#general-style)
2. [External Links](#external-links)

## General Style

- Use tabs for indentation.

- For strings, use `"double quotes"`.

- Avoid the use of `!important` as much as _absolutely_ possible.

- If the value of a property is `0`, do not specify units.

   ```css
   // good
   padding-top: 0;
   
   // bad
   padding-left: 0px;
   ```
   
- **Avoid** using IDs for CSS styling, unless there is a really good reason to.

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
- When grouping selectors, use one line per selector.

- Add one space between the end of the selector and `{

- Add one space after the `:` in properties.

- One line per declaration.

- End all declarations with `;`.

  ```css
  // good
  .main-header,
  .footer-text,
  .banner {
      color: $light-blue;
      line-height: 1.2em;
      text-shadow: 0 1px 1px rgba(0, 0, 0, .5);
  }
  
  // bad
  .main-header, .footer-text, .banner{
      text-shadow: 0 1px 1px rgba(0,0,0,.5); line-height: 1.2em;      
      color:$light-blue
  }
  ```

- Hex values for colors in lowercases. `#fafafa` instead of `#FAFAFA`.
- Hex values for colors in shorthand, if possible. `#bbb` instead of `#bbbbbb`.

**[⬆ back to top](#table-of-contents)**

## External Links
* [CSS Vocabulary](http://pumpula.net/p/apps/css-vocabulary/).

**[⬆ back to top](#table-of-contents)**


#}