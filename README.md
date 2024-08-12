# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Screenshot

|  Mobile designed at 375px:   |  Desktop designed at 1440px:  |
| :--------------------------: | :---------------------------: |
| ![](./screenshot-mobile.png) | ![](./screenshot-desktop.png) |

### Links

- Solution URL: [https://github.com/elisilk/testimonials-grid-section-main](https://github.com/elisilk/testimonials-grid-section-main)
- Live Site URL: [https://elisilk.github.io/testimonials-grid-section-main/](https://elisilk.github.io/testimonials-grid-section-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- [Grid layouts](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout) - This felt like the essence of the challenge, and was definitely the most fun part. It was cool to get the cards to span multiple rows or columns and still maintain the original ordering of the mobile design. To help with getting the heights of the cards pixel perfect, I ended up setting the `align-items` property to `start`, even though it's probably better to keep it set as `stretch` so that the cards fill up the fill height of the row as the viewport size changes.
- [Box shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) - I don't have a great eye for this yet. I feel like the desktop design did have a box shadow on each of the cards, but it was hard to tell for sure. And them it was hard to implement it in a subtle way that was true to the design. So I probably need to work on this a bit more.
- [Background position](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position) - For the one card, there is a background image, so I needed to clarify how to get it positioned correctly, at the top of the container and most of the way toward the right manipulating the [`background-position-x` property](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position-x) (approximately 90%). Of course, I still want to have a background color and I don't want the image to repeat so have to put those in the [background shorthand](https://developer.mozilla.org/en-US/docs/Web/CSS/background) as well.
- Fonts - It was a little unclear to me how to specify the [importing of the font faces](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face) properly, and so I did a little looking into that. [Specifying each of the font faces separately](https://www.456bereastreet.com/archive/201012/font-face_tip_define_font-weight_and_font-style_to_keep_your_css_simple/) turned out to be the cleanest method that had a working result, so I like this solution.
- [BEM](https://getbem.com/introduction/) - Definitely used BEM more in this challenge than the previous ones, since the colored cards seem very much like modifiers of a more general class of cards. So hoping I implemented the BEM principles reasonably well, even though I am using [child](https://developer.mozilla.org/en-US/docs/Web/CSS/Child_combinator) and [descendent](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_combinator) selectors on occasion in this solution.
- [Card components](https://developer.mozilla.org/en-US/docs/Web/CSS/Layout_cookbook/Card) - I based the HTML on a card component. I chose to put them in a list, because ther are [advantages to assistive technology users' experience](https://inclusive-components.design/cards/), as screen readers provide shortcuts to lists and between list items and screen readers enumerate the items so users know how many are available.
- [Applying opacity to a CSS color variable](https://stackoverflow.com/questions/40010597/how-do-i-apply-opacity-to-a-css-color-variable) - A great explanation and example of how CSS vars can be used to combine an RGB with an alpha value. "The magic lies in the fact that the values of custom properties are substituted as is when replacing var() references in a property value, before that property's value is computed."
- [HSL to RGB color conversion](https://www.rapidtables.com/convert/color/hsl-to-rgb.html) - I used this tool to conver the HSL values given in the design to RGB values. This was a bit confusing as the Figma design value gave separate RGB values rather than specifying a smaller set of RGB values some of which were an opacity of another. I looked into equivalent [RGBA to RGB converter](https://borderleft.com/toolbox/rgba/), but didn't get all that far with that.
- [ems/rems](https://www.joshwcomeau.com/css/surprising-truth-about-pixels-and-accessibility/) - Still learning more about how to use more `rem` (and less `px`) in my CSS code. Trying to chase pixel perfection is much easier when at least starting with `px` values, but I definitely understand the value of relative units in many situations.
- [Box sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) - For the avatars, it looked like they had a border (at least in some of the cards) that was outside the content box in which the avatar, the name, and the verified status were positioned. So I spent some time playing with box sizing, although did end up moving back to the idea of `content-box` as the best option for this case.
- [Line height](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) - I got a little frustrated with line heights in this challenge, especially with the header box. In trying to match the box heights for the header and the other text, I played with those a bit, essentially removing the line heights from the header text and increasing it in the actual testimonial text. Not sure I matched exactly how the design intended and in a way that works for all screen sizes, so this is something I will continue to think and learn about.

### Continued development

Hmm 🤔, so much to think about, but not sure what to focus on specifically. I definitely want to improve my eye for `box-shadow` and use more `rem` (and `em`, and less `px`). And I also want to just get more efficient in implementing a full solution, without getting caught up in the pixel perfection of line heights and paddings that seem to take up the majority of the time I devote to each challenge.

### Useful resources

- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web) - Of course, as always. So useful.

## Author

- Website - [Eli Silk](https://github.com/elisilk)
- Frontend Mentor - [@elisilk](https://www.frontendmentor.io/profile/elisilk)
