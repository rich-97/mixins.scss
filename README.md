# mixins.scss 

scss **mixins** syntax of `sass`

## Installation

via `bower`
```shell
bower install mixins.scss --save
```
## Usage

-   [`font-face`](#font-face)
-   [`trans`](#trans)
-   [`trans-bezier`](#trans-bezier)
-   [`border`](#border)
-   [`bgc`](#bgc)
-   [`media`](#media)
-   [`clearfix`](#clearfix)
-   [`text-overflow`](#text-overflow)
-   [`overflow-x`](#overflow-x)
-   [`unstyled-list`](#unstyled-list)
-   [`inline-list`](#inline-list)
-   [`unstyled-link`](#unstyled-link)
-   [`hidden`](#hidden)
-   [`heading`](#heading)
-   [`center-block`](#center-block)

### font-face

```scss
/*
 * @param $fontname name of font
 * @param $path the path of font
 * @apram $weight this is optional param default: normal
 */

// font-weight: normal
@include font-face('yourfontname', '/path/font');

// or include font-weight
@include font-face('yourfontname', '/path/font', 600);
```

### trans

```scss
/*
 * @param $args is optional default: all .5s ease, or use the following list for use the prefix (all .5s):
 * 1. linear
 * 2. ease-in
 * 3. ease-in-out
 * 4. ease-out
 */

.foo {
  @include trans;
}

// Use the name of animation
.foo {
  @include trans(linear);
}

// also ..
.foo {
  @include trans(border-radius .2s ease-in-out);
}
```

### trans-bezier

```scss
/*
 * @params $n, $m, $l, $p betwen 0 and 1
 */

.foo {
  @include trans-bezier(0.25, 0.25, 0.5, 0.1);
}
```

### border

```scss
/*
 * @param $width border width the param not have unity
 * @param $color is optional default: #0b0b0b
 * @param $style is optional default: solid
 */

  .foo {
    @include border(1, $color);
  }

  // or include style
  .foo {
    @include border(5, $color, dotted);
  }
```

### bgc

`background-color`

```scss
/*
 * @param $color this param has 3 option:
 * 1. hex color e.p #009288
 * 2. rgba color e.p (1, 22, 31, .8)
 * 3. rgb color e.p (22, 14, 21)
 */

// hex color
@include bgc(#009688);

// rgb color
@include bgc((22, 35, 88));

// rgba coor
@include bgc((34, 123, 1, .8));
```

### media

```scss
/*
 * @param $media options:
 * - xs : 360px
 * - sm : 767px
 * - md : 1023px
 * - lg : 1360px
 */

.foo {
  @include media(xs) {
    width: 50%;
  }
}

// or

@include media(xs) {
  .foo {
    width: 50%;
  }
}
```

### clearfix

```scss
@include clearfix;
```

### text-overflow

```scss
@include text-overflow;
```

### overflow-x

```scss
@include overflow-x;
```

### unstyled-list

```scss
@include unstyled-list;
```

### inline-list

```scss
@include inline-list;
```

### unstyled-link

```scss
/*
 * @param $color is optional default: #000
 */

a {
  @include unstyled-link;
}

// or adding color
a {
  @include unstyled-link(#0b0b0b);
}
```

### hidden

```scss
/*
 * @param $what options:
 * - invisible or hide.
 */

.foo {
  @include hidden('invisible');
}
```

### heading

```scss
// Styles for heading h1, h2... h6.

@include heading {
    font-family: 'Ubuntu';
    color: #ccc;
}
```
### center-block

```scss
/*
 * @param $width the width of element only on percentage (unity relative)
 * @param $margin is optional default: 0 auto  or (margin-top and margin-bottom) unity: pixels
 */

foo {
  // equivalent to width: 70%; and margin: 20px auto;
  @include center-block(70, 20);
}
```

