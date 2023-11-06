---
title: '👀 SASS Syntax'
date: 2022-07-20 00:00:00 +0000
categories: [STYLE, SASS]
tags: [sass]     # TAG names should always be lowercase
---

In the [previous post](https://dev.to/ak_ram/how-to-add-sass-to-your-project--32cn), we learned how to compile SCSS to CSS. Now we will learn how to write SCSS.

You should first know that you can write SASS stylesheets with two syntaxes.
1. SCSS Syntax
2. SASS Syntax

Do they differ? **_Yes_**, and the table below highlights their variants.



![SCSS vs SASS table comparison](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/y8cg7x15xzlqv2sv0uhf.jpg)



To make things more clear, check out this example, which is written twice—once with SCSS syntax and once with sass syntax.

![SCSS vs SASS code Example](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m5v7dn1icnfifujyd31m.png)

When writing SASS or SCSS, you should adhere to these two rules: 
1-Style Rules. 
2-at-Style Rules.

Again, you can take an overview look at these rules in the below screenshot.

![Style rules and at-rules list](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/79wohy6qwz9zxd2en1d9.jpg)

Fear not, we will explain each of these rules in more detail in the following sections, but for now, let's focus on the five style principles of nesting, variables, interpolation, placeholder selectors, and selector combinators.


## 1. Variables

Simple Sass variables allow you to use the name rather than the actual value by assigning a value to a name that starts with the letter $.
```
$variableName : value;
```
- variableName: any name that doesn't start with a number or a special character like @.
- value: any value (lists, strings, numbers, booleans, null, colors)


_Example:_

```
// We assign a variable
$colorOfHeading: #616165;

// then use it
h3 {
color: $colorOfHeading
}
```

Keep in mind that the variables:
- Can only be used as a property value and will throw an error if used as a property name.
- Is not available outside of its scope.

_Example:_

```
$propertyName: 'font-size';
$propertyValue: 30px;

h3{
    $propertyName: $propertyValue; // not Valid
     font-size: $propertyValue; // Valid
}
``` 

_Example:_

```
$myColor: red; // in global scope
h1{
$myColor: green; // in local scope
color: $myColor; // green
}
p{
color: $myColor; // red
}
```
The `!global` flag can be used to make local variables global.

_Example:_ 

```
$myColor: red;
h1{
$myColor: green !global;
color: $myColor; // green
}
p{
color: $myColor; // green
}
```

**_Note:_** A hyphen and an underscore are equivalent in Sass. $font-size is the same as $font_size

_Example:_

```
$font-size: 20px;
h2{
font-size: $font_size; // 20px
}
```

**_Tip:_** to fully control the sizes and widths of your styles, use variables in conjunction with expressions.

_Example:_ 

```
$full-width: 100%
.col-1 {float: left; width: $full-width / 1}
.col-2 {float: left; width: $full-width / 2}
.col-3 {float: left; width: $full-width / 3}
```
_Example:_

```
$baseFont: 10px;
$paragraphFontSize: 7px;
h3{font-size: $baseFont + $paragraphFontSize}
```
Because variables cannot be used as a property name, **[interpolation ](https://sass-lang.com/documentation/interpolation)**comes into the picture. In the following articles, interpolation will be covered in more detail.