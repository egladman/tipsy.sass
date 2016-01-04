# Tipsy.sass
An easy to use tooltip library implemented in Sass



### Changelog
- v1.1.2:
  - fixed bug where the directional pointer would be prematurely clipped when `$gravity` was either `e` or `w`
  - changed the default tooltip text/background color
  - added missing browser prefixes to transformations and transitions
  - used `em` and `ch` instead of `px`
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
Three ways:
- `bower install tipsy.sass`
- Clone `git@github.com:egladman/tipsy.sass.git`
- [Download the latest zip](https://github.com/egladman/tipsy.sass/archive/master.zip)

## Getting Started

### Import Tipsy.sass in your stylesheet

**SCSS**

```scss
@import "tipsy";
```

**SASS**

```sass
@import "tipsy"
```

### Tipsy.sass have 6 *optional* parameters

#### Tooltip & Arrow Position
  ```
  $gravity: nw | n | ne | e | se | s | sw | w`
  ```

#### Tooltip Text Color
  ```
  $color: HEX | RGB | RGBA | HSL
  ```

#### Tooltip Background Color
  ```
  $background: HEX | RGB | RGBA | HSL
  ```

#### Tooltip Arrow Size
  ```
  $border-size: px | em | rem
  ```

#### Tooltip Border Radius
  ```
  $border-radius: px | em | rem
  ```

#### Tooltip Shadow
  ```
  $box-shadow: 0px,0px,0px rgba(0,0,0,0.2)
  // same syntax as the box-shadow css property
  // https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow
  ```


### How to use

#### HTML
```html
<span data-tipsy="sample text that will be displayed in tooltip">foo bar</span>
```

#### SCSS
```scss
span {
  @include tipsy();
}

//or

span {
  @include tipsy(s, #FFF, #000, 5px, 3px);
}

//or

span {
  @include tipsy(s, #FFF, #000, 5px, 3px, 2px 2px 5px rgba(0, 0, 0, .50));
}
```

#### SASS
```sass
span
  @include tipsy()  

//or

span
  @include tipsy(s, #FFF, #000, 5px, 3px)

//or

span
  @include tipsy(s, #FFF, #000, 5px, 3px, 2px 2px 5px rgba(0, 0, 0, .50))
```

