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
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

The design has three layouts:

- **Mobile:** the five testimonials stacked in a single column.
- **Tablet:** two columns, where Daniel, Patrick and Kira span both columns, and Jonathan and Jeanette sit side by side.
- **Desktop:** four columns and two rows, where Daniel spans two columns, Kira spans both rows in the last column, and Patrick spans two columns in the second row.

### Screenshot

<p align="center">
  <img src="assets/images/screenshot.png" alt="Screenshot of the testimonials grid on desktop, showing five colored testimonial cards in a four column grid" width="600">
</p>

### Links

- GitHub repository: [YOUR-REPO-NAME](https://github.com/hossamelgendy101/Testimonials-grid-section)
- Live site: [YOUR-LIVE-SITE](https://testimonials-grid-section-psi-pied.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup (`figure`, `figcaption`, `blockquote`, `ul`, `li`)
- CSS custom properties
- CSS Grid
- Flexbox (inside each card)
- Mobile-first workflow with `min-width` media queries
- Google Fonts (Barlow Semi Condensed)

### What I learned

- **Placing items on the grid at different breakpoints:** The same five cards use three different layouts, so I wrote the base styles for mobile and added `grid-column` and `grid-row` rules in the 768px and 1200px media queries. A card can span several columns or rows, for example `grid-column: 1 / 3` or `grid-row: 1 / 3`.
- **Calculating breakpoints from the design:** I worked out the minimum width each layout needs, for example four 255px columns plus three 32px gaps equals 1116px, and then added the body padding to choose the breakpoint (1200px).
- **Separating position from appearance:** The `li` is the direct child of the grid, so it carries the position classes (such as `testimonial--daniel`), while the `figure` inside carries the shared `.card` styles and a color modifier (such as `card--purple`). This avoided repeating the same CSS for every person.
- **Color modifiers with descendant selectors:** Each card color changes several things (background, name, title, text, verification status and avatar border). I used selectors like `.card--purple .card__title` so the base `.card` styles stay shared.
- **Equal heights in a grid:** The `li` stretches to the row height but the `figure` inside it does not, so cards in the same row had different heights. Setting `height: 100%` on the card fixed this.
- **Semantic markup for testimonials:** I used `figure` with `figcaption` for the author and `blockquote` for the quote, and one visually hidden `h1` so the page has a main heading for screen readers (hidden with a `visually-hidden` class and not `display: none`).
- **Checking values instead of trusting screenshots:** My screenshots looked zoomed in because of my display scaling, which made the text look bigger than it was. I learned to compare values in the DevTools (the Computed tab) and in Figma instead of judging by eye.
- **Background image paths:** A `url()` in CSS is resolved from the CSS file's location and not from the HTML file, so the decorative quotation mark needed `../images/...`. I found this by reading the failed request in the Network tab.

```css
.testimonial--kira {
  grid-column: 4;
  grid-row: 1 / 3;
}
```

### Continued development

- Use `clamp()` for fluid typography on a project where font sizes change between screen sizes.
- Try `grid-template-areas` as a more readable way to describe layouts like this one.
- Reduce repeated CSS in the color modifiers, for example with custom properties per modifier.
- Learn Sass/SCSS after getting comfortable with plain CSS.

### AI Collaboration

During this project, I collaborated with an AI assistant (**Claude**) to enhance my workflow and problem-solving process.

- **Tools used:** Claude, as a technical consultant and reviewer.
- **How I used it:** For reviewing my HTML structure, understanding how to place items on the grid, calculating breakpoints, and finding the causes of bugs using the DevTools.
- **What worked well:** It explained concepts step by step and caught mistakes like the equal height issue and the wrong background image path.
- **What I did myself:** I wrote the HTML and CSS by hand, read the values from Figma, and tested the layouts on different screen sizes.

## Author

- GitHub - [@hossamelgendy101](https://github.com/hossamelgendy101)
- Frontend Mentor - [@hossamnabil](https://www.frontendmentor.io/profile/hossamnabil)
- Twitter - [@hossamelgendy](https://www.twitter.com/hossamelgendy)

## Acknowledgments

- Thanks to **Frontend Mentor** for this challenge.
- Thanks to the developer community and AI assistant tools for guidance and feedback.
