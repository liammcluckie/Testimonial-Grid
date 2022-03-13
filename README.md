# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

-   [Overview](#overview)
    -   [The challenge](#the-challenge)
    -   [Screenshot](#screenshot)
    -   [Links](#links)
-   [My process](#my-process)
    -   [Built with](#built-with)
    -   [What I learned](#what-i-learned)
    -   [Continued development](#continued-development)
    -   [Useful resources](#useful-resources)
-   [Author](#author)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

-   View the optimal layout for the site depending on their device's screen size

### Screenshot

![Completed Project](assets/images/completed-screenshot.png)

### Links

-   [Solution URL](https://github.com/liammcluckie/Testimonial-Grid)
-   [Live Site URL](https://liammcluckie.github.io/Testimonial-Grid/)

## My process

### Built with

-   Semantic HTML5 markup
-   SASS
    -   Mixins
    -   Functions
    -   Variables
-   CSS Grid
-   Mobile-first workflow

### What I learned

Using this challenge I practiced using CSS grid for easy responsive changes and layout switches. Alongside this I also further enhanced my learning of SASS functions.

```SASS Media Query Mixin
@mixin response($breakpoint) {
    @if ($breakpoint == md) {
        @media (min-width: 800px) {
            @content;
        }
    }

    @if ($breakpoint == lg) {
        @media (min-width: 1440px) {
            @content;
        }
    }
}
```

```Simple use of CSS grid to achieve the required layout
.testimonial-grid {
    display: grid;
    margin-inline: auto;
    width: 85%;
    max-width: 1440px;
    grid-gap: margin(xxl);
    grid-auto-columns: 1fr;
    grid-template-areas:
        "one"
        "two"
        "three"
        "four"
        "five";

    @include response(md) {
        grid-template-areas:
            "one one"
            "two three"
            "five five"
            "four four";
    }

    @include response(lg) {
        grid-template-areas:
            "one one two five"
            "three four four five";
        margin: margin(xxl) auto;
    }
}
```

### Continued development

The SASS used in this project was useful and aided in consistency as well as clean code. I plan to bring these and as well as CSS grid into future projects.

### Useful resources

-   [Kevin Powell - Learn CSS grid](https://www.youtube.com/watch?v=rg7Fvvl3taU) - This helped me understand the key properties of CSS grid.

## Author

-   Linkedin - [Liam Mcluckie](https://www.linkedin.com/in/liam-mcluckie-441b43148/)
-   Frontend Mentor - [@liammcluckie](https://www.frontendmentor.io/profile/liammcluckie)
