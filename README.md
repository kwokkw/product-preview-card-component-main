# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). 
Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Product preview card component solution](#frontend-mentor---product-preview-card-component-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
  - [Author](#author)
  - [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- image sizing with object-fit
- buttons vs anchors
- heading order
- responsive images using the picture element 
- how to add extra info for screen reader users

### What I learned

How is the following code helping with the border-radius?

The background/content of the children overlap the parent's curved corners. So the overflow hidden is needed to crop out the bits that overflow

```css
.c-product-card {
  border-radius: var(--border-radius);
  overflow: hidden;
}
```

The “visually-hidden” class is utilizing various declarations to shrink an element into a 1px square, hiding any overflow, and absolutely positioning the element to remove any trace of it from the normal document flow.

```css

.visually-hidden:not(:focus):not(:active) {
  clip: rect(0 0 0 0); 
  clip-path: inset(50%);

  /* Shrink an element into a 1px square */
  width: 1px;
  height: 1px;

  /* Hiding any overflow */
  overflow: hidden;

  /* absolutely positioning the element to remove any trace of it from the normal document flow. */
  position: absolute;

  white-space: nowrap; 
}

```

  Letter spacing prefers `px` or `em`

### Continued development

### Useful resources

- [Scott O'Hara's Inclusively Hidden article](https://www.scottohara.me/blog/2017/04/14/inclusively-hidden.html#hiding-content-visually) - This explains how to visually hide an element. 

Why are we hiding content?
  1. Completely Hidden Content
     - CSS `display: none`
     - CSS `visibility: hidden`
     - HTML's `hidden Attribute` 

  2. Only Visually Hidden Content
    ```css

    .visually-hidden:not(:focus):not(:active) {
  clip: rect(0 0 0 0); 
  clip-path: inset(50%);
  height: 1px;
  overflow: hidden;
  position: absolute;
  white-space: nowrap; 
  width: 1px;
  }

    ```

  3. Visual-Only Content, or hiding content to assistive technologies

  ```css
  
  /* baseline rules for an off-screen class */
  .off-screen {
  left: -100vw;
  position: absolute;
  }
  
  ```

## Author
- Frontend Mentor - [@kwokkw](https://www.frontendmentor.io/profile/kwokkw)

## Acknowledgments

[How to plan your HTML (1): Product Preview Card](https://fedmentor.dev/posts/html-plan-product-preview/#series-intro) written by Grace Snow