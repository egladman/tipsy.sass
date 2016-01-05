# tipsy.sass
An easy to use tooltip library implemented in Sass

[DEMO](http://eli.gladman.xyz/tipsy.sass/)

### Changelog
- v1.1.2:
  - fixed bug where the directional pointer would be prematurely clipped when `$gravity` was either `e` or `w`
  - changed the default tooltip text/background color
  - added missing browser prefixes to transformations and transitions
  - use `em` and `ch` instead of `px`
- v1.1.1:
  - added bower support
- v1.1.0:
  - added default values to parameters
  - revised variable names to better reflect their associated css property
  - added text color & box-shadow parameters
  - removed support for `.scss` variant
- v1.0.5:
  - Change background variable
  - Added arrow border size of tooltip
- v1.0.4:
  - Fix reversed tipsy. Thank you [@esteinborn](https://github.com/esteinborn)



## Installation
`bower install tipsy.sass`


## Getting Started

### Import tipsy.sass in your stylesheet

**SCSS**

```scss
@import "tipsy";
```

**SASS**

```sass
@import "tipsy"
```

### tipsy has 6 *optional* parameters

1. Tooltip & Arrow Position

  `$gravity: nw | n | ne | e | se | s | sw | w`
  - `nw` = northwest
  -  `n` = north
  - `ne` = northeast
  - `se` = southeast
  -  `s` = south
  - `sw` = southwest
  -  `w` = west

2. Tooltip Text Color

  `$color: HEX | RGB | RGBA | HSL`

3. Tooltip Background Color

  `$background: HEX | RGB | RGBA | HSL`

4. Tooltip Arrow Size

  `$border-size: px | em | rem`
  *or any [unit of length](https://developer.mozilla.org/en-US/docs/Web/CSS/length)*

5. Tooltip Border Radius

  `$border-radius: px | em | rem`
  *or any [unit of length](https://developer.mozilla.org/en-US/docs/Web/CSS/length)*

6. Tooltip Shadow

  `$box-shadow: 0px,0px,0px rgba(0,0,0,0.2)`
  *same syntax as the [box-shadow css property](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)*



### How to use

##### HTML
```html
<span data-tipsy="sample text that will be displayed in tooltip">foo bar</span>
```

##### SCSS

example one
 ```scss
  span {
    @include tipsy();
  }
  ```
  
example two
  ```scss
  span {
    @include tipsy(s, #FFF, #000, 5px, 3px);
  }
  ```

example three
  ```scss
  span {
    @include tipsy(s, #FFF, #000, 5px, 3px, 2px 2px 5px rgba(0, 0, 0, .50));
  }
  ```

#### SASS

example one
```sass
span
  @include tipsy()  
```

example two
```sass
span
  @include tipsy(s, #FFF, #000, 5px, 3px)
```

example three
```sass
span
  @include tipsy(s, #FFF, #000, 5px, 3px, 2px 2px 5px rgba(0, 0, 0, .50))
```


### Contributing
Feel free to create issues, request features, or submit pull requests. 
