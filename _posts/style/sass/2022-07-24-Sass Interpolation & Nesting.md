---
title: '🎁 Sass: Interpolation & Nesting'
date: 2022-07-24 00:00:00 +0000
categories: [STYLE, SASS]
tags: [sass]     # TAG names should always be lowercase
---

In the prior post, we discussed the SSCS rules. We began with variables and demonstrated how they cannot be used as placeholders for property names, stating that interpolation was used in their place, so let's expand on the topic of interpolation.

# Interpolation
[sass docs](https://sass-lang.com/documentation/interpolation) said that
> Interpolation can be used almost anywhere in a Sass stylesheet to embed the result of a SassScript expression into a chunk of CSS.

It allows us to insert sass expressions into a simple SASS or CSS code by using `#{expression}`.

Interpolation Syntax:
```
#{expression}
```
Example:

![Interpolation Syntax](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/1ojaisq0tv2vo38jvqmv.png)

Keep in mind that we may use interpolation as a placeholder for both property names and values.

It can also be utilized as a placeholder for selectors.
Example: 
![Interpolation Syntax Example No. 2](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/v4zfj0xech0vhymx0vg4.png)


# Nesting rule
CSS selectors may be nested in Sass just as in HTML.

Take a look at this Sass navigation code example:


![Nesting rule](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9fuet0j06r2uncfj5bdg.png)

Notice that in Sass, the `ul`, `li`, and selectors are nested inside the `nav` selector.

While in CSS, the rules are defined one by one (not nested):

You can see that sass is more readable and cleaner than traditional CSS since it allows the nesting of properties.

## Sass Nested Properties

Numerous CSS properties, such as text-align, text-transform, and text-overflow, all begin with the same prefix.

Sass allows you to write them as nested properties:


![Sass Nested Properties Example](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2g1dtm8yqvs700m8sgd3.png)
For now, that is all there is. We will discuss nesting in further detail in the following post.

See You 🧡 

