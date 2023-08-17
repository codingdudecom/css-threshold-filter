# CSS Threshold Filter

*Original Post:* [CSS Threshold Filter](https://www.coding-dude.com/wp/css/css-threshold-filter/) on [CodingDude](https://www.coding-dude.com/wp/)

Showcasing how to create the threshold filter using CSS

## What is Thresholding in Image Processing?

![Image Thresholding](https://www.coding-dude.com/wp/wp-content/uploads/2023/08/image-thresholding.gif)

Thresholding in image processing is a fundamental technique used to segment an image into distinct regions based on pixel intensity values. It involves setting a threshold value, which serves as a boundary that divides the pixels into two groups: those that have intensity values above the threshold and those that have intensity values below it.

In simpler terms, thresholding converts a grayscale image into a binary image, where each pixel is categorized as either part of the foreground (object of interest) or the background. Pixels with intensity values above the threshold are typically assigned one value (often white), while those below the threshold are assigned another value (often black).

There are many applications that have a threshold tool including Photoshop, GIMP, etc. There are even free online applications that allow you to apply a threshold filter to an image online. For example the [stencil maker](https://www.mockofun.com/template/stencil-maker-from-photo/) from MockoFun is a cool example of a free online application. It basically applies the threshold filter to any photo and transforms it into a stencil like the famous Bansky street art designs.

[![Stencil Maker](https://www.coding-dude.com/wp/wp-content/uploads/2023/08/image-to-stencil1.jpg)](https://www.mockofun.com/template/stencil-maker-from-photo/)
[Stencil Maker](https://www.mockofun.com/template/stencil-maker-from-photo/) on [MockoFun](https://www.mockofun.com/)

## CSS Threshold Filter Code

<span>See the Pen <a href="https://codepen.io/inegoita/pen/gOQVWGK">
  CSS Threshold Filter</a> by CodingDude (<a href="https://codepen.io/inegoita">@inegoita</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
[![CSS Threshold Filter](https://www.coding-dude.com/wp/wp-content/uploads/2023/08/css-threshold-filter.jpg)](https://codepen.io/inegoita/pen/gOQVWGK)

*HTML Code*

```<img src="https://i.imgur.com/r4csVkj.jpeg" alt="CSS Stencil Filter" class="threshold">```

*CSS Code*

```:root{
--threshold:50%;
}

.threshold{
filter: brightness(calc(100% + var(--threshold))) grayscale(100%) contrast(1000%);
}```