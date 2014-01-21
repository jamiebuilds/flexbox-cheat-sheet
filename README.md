Flexbox Cheat Sheet
===================

Quick references for everything you need to know about using flexbox

---

**YO! THIS DOCUMENT IS A WORK IN PROGRESS. PROCEED WITH CAUTION**

---

### Resources

- [W3C: Editor's Draft CSS Flexible Box Layout Module](http://dev.w3.org/csswg/css-flexbox/)
- [W3C: 2012 CSS Flexible Box Layout Module](http://www.w3.org/TR/2012/WD-css3-flexbox-20120322/)
- [W3C: 2011 CSS Flexible Box Layout Module](http://www.w3.org/TR/2011/WD-css3-flexbox-20111129/)
- [W3C: 2009 CSS Flexible Box Layout Module](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/)
- [Bourbon Source](https://github.com/thoughtbot/bourbon/blob/master/app/assets/stylesheets/css3/_flex-box.scss)
- [Bourbon (New Flex Box) Source](https://github.com/thoughtbot/bourbon/blob/new-flex-box/app/assets/stylesheets/css3/_flex-box.scss)
- [Compass Docs](http://compass-style.org/reference/compass/css3/box/)
- [Compass Source](https://github.com/chriseppstein/compass/blob/stable/frameworks/compass/stylesheets/compass/css3/_box.scss)
- [Nib Source](https://github.com/visionmedia/nib/blob/master/lib/nib/flex.styl)
- [Less Hat Docs](https://github.com/csshat/lesshat/blob/master/README.md)
- [CSS Flexbox 2009/2011 Spec Syntax Property Mapping](http://wiki.csswg.org/spec/flexbox-2009-2011-spec-property-mapping)
- [A Guide to Flexbox (CSS Tricks)](http://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [“Old” Flexbox and “New” Flexbox (CSS Tricks)](http://css-tricks.com/old-flexbox-and-new-flexbox/)
- [Quick hits with the Flexible Box Model (HTML5 Rocks)](http://www.html5rocks.com/en/tutorials/flexbox/quick/)
- [Flexible box ("Flexbox") layout (MSDN)](http://msdn.microsoft.com/en-us/library/ie/hh673531.aspx)

---

### 2009 Spec
Deprecated (See: [2012 Spec](#2012-spec))

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/) 

```css
display:                   box;
display:            inline-box;
box-align:             stretch; /* start | end | center | baseline | stretch */
box-direction:          normal; /* normal | reverse | inherit */
box-flex:                  0.0; /* <number> */
box-flex-group:              1; /* <integer> */
box-lines:              single; /* single | multiple */
box-ordinal-group:           1; /* <integer> */
box-orient:        inline-axis; /* horizontal | vertical | inline-axis | block-axis | inherit */
box-pack:                start; /* start | end | center | justify */
```

### 2011 Spec
Deprecated (See: [2012 Spec](#2012-spec))

[W3C Reference](http://www.w3.org/TR/2011/WD-css3-flexbox-20111129/) 

```css
display:               flexbox;
display:        inline-flexbox;
flex-align:            stretch; /* start | end | center | baseline | stretch */
flex-flow:                 row; /* [ row | row-reverse | column | column-reverse ] [ wrap | wrap-reverse ]? */
flex-line-pack:          start; /* start | end | center | justify */
flex-order:                  0; /* <number> */
flex-pack:               start; /* start | end | center | justify */

/* Flex Function
 *   flex( [ <pos-flex> <neg-flex>? ]? || <preferred-size>? )
 */
```

### 2012 Spec

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/) 

```css
display:               flex;
display:        inline-flex;
align-content:      stretch; /* flex-start | flex-end | center | space-between | space-around | stretch */
align-items:        stretch; /* flex-start | flex-end | center | baseline | stretch */
align-self:            auto; /* auto | flex-start | flex-end | center | baseline | stretch */
flex:              0 1 auto; /* none | [ <flex-grow> <flex-shrink>? || <flex-basis> ] */
flex-basis:            auto; /* <width> */
flex-direction:         row; /* row | row-reverse | column | column-reverse */
flex-flow:       row nowrap; /* <flex-direction> || <flex-wrap> */
flex-grow:                0; /* <number> */
flex-shrink:              0; /* <number> */
flex-wrap:           nowrap; /* nowrap | wrap | wrap-reverse */
justify-content: flex-start; /* flex-start | flex-end | center | space-between | space-around */
order:                    0; /* <integer> */
```

---

### Display Box
Deprecated (See: [Display Flex](#display-flex))

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#overview) 

```css
display:  -webkit-box;
display:     -moz-box;
display:          box;

/* Bourbon */
@include display-box;

/* Compass */
@include display-box;
```

### Display Inline Box
Deprecated (See: [Display Inline Flex](#display-inline-flex))

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#overview) 

```css
display: inline-box;
```

### Display Flexbox
Deprecated (See: [Display Flex](#display-flex))

[W3C Reference](http://www.w3.org/TR/2011/WD-css3-flexbox-20111129/#display-flexbox) 

```css
display: -ms-flexbox;
```

### Display Flexbox
Deprecated (See: [Display Inline Flex](#display-inline-flex))

[W3C Reference](http://www.w3.org/TR/2011/WD-css3-flexbox-20111129/#display-flexbox) 

```css
display: -ms-inline-flexbox;
```

### Display Flex

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#flex-containers) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

```css
display: -webkit-flex;
display:    -moz-flex;
display:         flex;

/* Bourbon: New Flex Box */
@include display(flex);

/* Nib */
display flex

/* Less Hat */
.display(flex);
```

### Display Inline Flex

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#flex-containers) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/display)

```css
display: -webkit-inline-flex;
display:    -moz-inline-flex;
display:         inline-flex;

/* Bourbon: New Flex Box */
@include display(inline-flex);

/* Nib */
display inline-flex

/* Less Hat */
.display(inline-flex);
```

### Box Flex
Deprecated (See: [Flex](#flex))

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#propdef-box-flex) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-flex)

```css
-webkit-box-flex: <number>;
   -moz-box-flex: <number>;
        box-flex: <number>;

/* Bourbon */
@include box-flex(<number>);

/* Compass */
$default-box-flex: 0;
@include box-flex(<number>);
```

### Flex

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#propdef-flex) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/flex)

```css
-webkit-flex: [ none | [ <flex-grow> <flex-shrink>? || <flex-basis> ] ];
   -moz-flex: [ none | [ <flex-grow> <flex-shrink>? || <flex-basis> ] ];
        flex: [ none | [ <flex-grow> <flex-shrink>? || <flex-basis> ] ];

/* Bourbon: New Flex Box */
@include flex( [ none | [ <flex-grow> <flex-shrink>? || <flex-basis> ] ] );

/* Nib */
flex [ none | [ <flex-grow> <flex-shrink>? || <flex-basis> ] ]

/* Less Hat */
.flex( [ none | [ <flex-grow> <flex-shrink>? || <flex-basis> ] ] )
```

### Box Ordinal Group
Deprecated (See: [Order](#order))

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#propdef-box-ordinal-group) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-ordinal-group)

```css
-webkit-box-ordinal-group: <integer>;
   -moz-box-ordinal-group: <integer>;
        box-ordinal-group: <integer>;

/* Bourbon */
@include ordinal-group(<integer>);

/* Compass */
$default-box-ordinal-group: 1;
@include box-ordinal-group(<integer>);
```

### Order

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#propdef-order) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/order)

```css
-webkit-order: <integer>;
   -moz-order: <integer>;
        order: <integer>;

/* Bourbon: New Flex Box */
@include order(<integer>);

/* Nib */
order <integer>

/* Less Hat */
.order(<integer>);
```

### Box Orient

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#propdef-box-orient) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-orient)

```css
-webkit-box-orient: [ horizontal | vertical | inline-axis | block-axis | inherit ];
   -moz-box-orient: [ horizontal | vertical | inline-axis | block-axis | inherit ];
        box-orient: [ horizontal | vertical | inline-axis | block-axis | inherit ];

/* Bourbon */
@include box-orient([ horizontal | vertical | inline-axis | block-axis | inherit ]);

/* Compass */
$default-box-orient: horizontal;
@include box-orient([ horizontal | vertical | inline-axis | block-axis | inherit ]);
```

### Box Pack

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#propdef-box-pack) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-pack)

```css
-webkit-box-pack: [ start | end | center | justify ];
   -moz-box-pack: [ start | end | center | justify ];
        box-pack: [ start | end | center | justify ];

/* Bourbon */
@include box-pack([ start | end | center | justify ]);

/* Compass */
$default-box-pack: start;
@include box-direction([ start | end | center | justify ]);
```

### Box Align
Deprecated (See: [Align Self](#align-self))

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#propdef-box-align) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-align)

```css
-webkit-box-align: [start | end | center | baseline | stretch];
   -moz-box-align: [start | end | center | baseline | stretch];
        box-align: [start | end | center | baseline | stretch];

/* Bourbon */
@include box-align([ start | end | center | justify ]);

/* Compass */
$default-box-align: stretch;
@include box-align([ start | end | center | justify ]);
```

### Align Self

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#align-items-property) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self)

```css
-webkit-align-self: [ auto | flex-start | flex-end | center | baseline | stretch ];
   -moz-align-self: [ auto | flex-start | flex-end | center | baseline | stretch ];
        align-self: [ auto | flex-start | flex-end | center | baseline | stretch ];

/* Bourbon: New Flex Box */
@include align-self([ auto | flex-start | flex-end | center | baseline | stretch ]);

/* Nib */
align-self [ auto | flex-start | flex-end | center | baseline | stretch ]

/* Less Hat */
.align-self([ auto | flex-start | flex-end | center | baseline | stretch ]);
```

### Box Direction
Deprecated (See: [Flex Direction](#flex-direction))

[W3C Reference](http://www.w3.org/TR/2009/WD-css3-flexbox-20090723/#propdef-box-direction) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/box-direction)

```css
-webkit-box-direction: [ normal | reverse | inherit ];
   -moz-box-direction: [ normal | reverse | inherit ];
        box-direction: [ normal | reverse | inherit ];

/* Bourbon */
@include box-direction([ normal | reverse | inherit ]);

/* Compass */
$default-box-direction: normal;
@include box-direction([ normal | reverse | inherit ]);
```

### Flex Direction

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#flex-direction-property) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction) · [CSS Tricks Almanac](http://css-tricks.com/almanac/properties/f/flex-direction/)

```css
-webkit-flex-direction: [ row | row-reverse | column | column-reverse ];
   -moz-flex-direction: [ row | row-reverse | column | column-reverse ];
        flex-direction: [ row | row-reverse | column | column-reverse ];

/* Bourbon: New Flex Box */
@include flex-direction($value: row);

/* Nib */
flex-direction [ row | row-reverse | column | column-reverse ]

/* Less Hat */
.flex-direction([ row | row-reverse | column | column-reverse ]);
```

### Align Content

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#align-content-property) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content) · [CSS Tricks Almanac](http://css-tricks.com/almanac/properties/a/align-content/)

```css
-webkit-align-content: [ flex-start | flex-end | center | space-between | space-around | stretch ];
   -moz-align-content: [ flex-start | flex-end | center | space-between | space-around | stretch ];
        align-content: [ flex-start | flex-end | center | space-between | space-around | stretch ];

/* Bourbon: New Flex Box */
@include align-content([ flex-start | flex-end | center | space-between | space-around | stretch ]);

/* Nib */
align-content [ flex-start | flex-end | center | space-between | space-around | stretch ]

/* Less Hat */
.align-content([ flex-start | flex-end | center | space-between | space-around | stretch ])
```

### Justify Content

[W3C Reference](http://dev.w3.org/csswg/css-flexbox/#justify-content-property) · [MDN Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) · [CSS Tricks Almanac](http://css-tricks.com/almanac/properties/j/justify-content/)

```css
-webkit-justify-content: [ flex-start | flex-end | center | space-between | space-around ];
   -moz-justify-content: [ flex-start | flex-end | center | space-between | space-around ];
        justify-content: [ flex-start | flex-end | center | space-between | space-around ];

/* Bourbon: New Flex Box */
@include justify-content([ flex-start | flex-end | center | space-between | space-around ]);

/* Nib */
justify-content [ flex-start | flex-end | center | space-between | space-around ]

/* Less Hat */
.justify-content([ flex-start | flex-end | center | space-between | space-around ]);
```

## Support

Have a question or need help? Tweet [@thejameskyle](https://twitter.com/thejameskyle).

## Contributing

As an open-source project, contributions are more than welcome, they're extremely helpful and actively encouraged. If you see any room for improvement, open an [issue](https://github.com/thejameskyle/bootcamp/issues) or submit a [pull request](https://github.com/thejameskyle/bootcamp/pulls). Also make sure to take a look at the [contributing doc](CONTRIBUTING.md).

## License

This project is provided under the terms of the [MIT License](LICENSE.md).

---

Authored by **James Kyle** · [Github](https://github.com/thejameskyle) · [Twitter](https://twitter.com/thejameskyle) · [CodePen](https://codepen.com/thejameskyle)

[Built Equal](http://www.hrc.org/donate) · [Made in Boston](http://bostonbuilt.org/)
