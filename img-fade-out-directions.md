# 013 RWD / IMG Gallery Effects

## Overview

In this project, you'll learn how to:

 - create a simple responsive image gallery
 - add captions to your images
 - use the CSS `opacity` property and the CSS `:hover` pseudo-class to change the opacity of your images when you mouse over them

## Helpful Resources

 - [Setting the transparency of an image](https://www.w3schools.com/css/tryit.asp?filename=trycss_ex_images_opacity) (w3schools.com)
 - [Changing the opacity of an image on hover](https://www.w3schools.com/css/tryit.asp?filename=trycss_image_transparency2) (w3schools.com)

## Your Project Folder

> Use GitHub Desktop to create on your workstation a new project repository named `img-gallery-effects`.  Remember to publish your new repo to GitHub online by clicking the blue PUBLISH button on GitHub Desktop.

## Project HTML

+ To your page body, add a `<div>` with a class of *image-gallery*
+ Inside the `<div>`, add at least four classroom-friendly images
+ Enclose each image with a `<figure>` and `<figcaption>` tag

```html
<div class="image-gallery">
		<figure>
			<img src="desert-nm1.jpg" alt="Phrase describing Image 1">
			<figcaption>Caption 1</figcaption>
		</figure>

		<figure>
			<img src="desert-nm2.jpg" alt="Phrase describing Image 2">
			<figcaption>Caption 2</figcaption>
		</figure>


		<figure>
			<img src="desert-nm3.png" alt="Phrase describing Image 3">
			<figcaption>Caption 3</figcaption>
		</figure>

		<figure>
			<img src="desert-nm4.jpg" alt="Phrase describing Image 4">
			<figcaption>Caption 4</figcaption>
		</figure>

	</div>
```

+ To your page `<head>`, use the `<style>` tags to add an embedded style sheet to your page


## Image Gallery CSS

NOTE: We haven't worked with [CSS Flexbox](https://www.w3schools.com/css/css3_flexbox_container.asp) yet, but it's a new specification in CSS you can use to:

+ build responsive web pages
+ arrange content either horizontally OR vertically in your page (in one direction or the other, but not both)

+ First, make your `<div>` with a class of *image-gallery* a flex container:

```css
 .image-gallery {
      display: flex;
      flex-wrap: wrap;
	  justify-content: center; /* Centers gallery horizontally on the page */
    }
```

+ Next, create the hover effect for the images in your gallery:

```css
   .image-gallery img {
      width: 200px;
      height: 100%;
      margin: 10px;
      transition: opacity 0.3s ease-in-out;
    }
```

+ Then apply the hover effect to the gallery  images:

```css
   /* Add the hover effect */
    .image-gallery img:hover {
      opacity: 0.8;
    }
```

+ For spacing purposes, apply some margin to the bottom of your `<figure>` elements:

```css
figure {
		margin-bottom: 2.5rem;
	}
```

+ Then *italicize* and center the image captions:

```css
	figcaption {
		font-style: italic;
		font-size: 0.8rem;
		text-align: center;
	}
```