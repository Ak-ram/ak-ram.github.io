---
title: '🤔 How to add SASS to your project ?'
date: 2022-07-14 00:00:00 +0000
categories: [STYLE, SASS]
tags: [sass]     # TAG names should always be lowercase
---

#### I added the course road map.
[![Course Roadmap](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9ro0ca8b5z7t169f1o5w.jpg)](https://miro.com/app/board/uXjVPXQ4nvk=/?share_link_id=333319943899)

---




The [previous post](https://dev.to/akram_ak/sass-the-style-you-want-the-code-you-need-5188) explained what SASS is and why it's preferable to use it rather than CSS. **Right now**, we are about to learn how to include it in our project.

Browsers won't understand sass files since, as we all know, they only understand HTML, CSS, and JS. Therefore, in order to make it simple for browsers to grasp, we need to compile Sass scripts into CSS files.

![Sass files should be compiled to CSS ones.](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/63m1yhszew26x5d9npv0.png)

In the next few lines, we will discuss 3 methods to compile Sass to Css

## #1. Command Line
![Git illustrate how to install sass](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2t214g7ucgcn69az3bb5.gif)

One of the simplest ways to compile Sass into CSS is by using the [sass](https://www.npmjs.com/package/sass) package.

sass can be installed on Windows, Mac OS X, Linux, and Unix operating systems. It can also be installed through the Node Package Manager (NPM). The installation process for both methods is quite simple.

To install sass using NPM, we need to install [node.js](https://nodejs.org/en/) first on our machine, then open the node terminal and follow these steps:

**1-Run** `node --version` to confirm that the node has been set up properly.
```node
node --version
> Expected: v16.16.0 or any other version
```

**2-Install sass**
```scss
npm install -g sass
```
This will download the package from npm's repository and install it globally on your system.

**3-Watching sass file**

```scss
sass -w style.sass style.css
```
This will automatically compile style.sass file to style.css file

Congratulate 🎉 you have setup sass successfully.

Now, if you copy & paste this Scss code in your local Scss file 
```scss
$socails : facebook twitter youtube;
@each $item in $socails {
    .#{$item}-img{
        background: url('../images/image-#{$item}.png');
    }
}

```
it will be compiled to 

```css
.facebook-img {
  background: url("../images/image-facebook.png");
}

.twitter-img {
  background: url("../images/image-twitter.png");
}

.youtube-img {
  background: url("../images/image-youtube.png");
}
```
---

## #2 VS Code Extensions

[live-sass](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass) is one of the most efficient VS code extensions that is used in sass compilation.


![live sass vs code extension](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5ym2rv1gufpz1q5xl4rf.gif)

---

## #3 Online Compilers
There are some online tools, such as [sassMeister](https://www.sassmeister.com/) that compile Sass without any installs.


![sassMeister online compilers](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/04mn1n7patpapv7gffhb.png)

Now, it's time to go deeper with sass. In the next article, we will learn more about sass syntax.





 



