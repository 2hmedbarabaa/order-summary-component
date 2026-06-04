# Frontend Mentor - Order Summary Card Solution

This is a premium, pixel-perfect, and fully responsive solution to the [Order Summary Card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlUkTrNi). Frontend Mentor challenges help developers improve their professional coding workflows by building realistic digital components.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My Process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Architectural Highlights](#architectural-highlights)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the component depending on their device's screen size (from small mobile viewports up to wide desktop displays).
- See fluid hover and active states for all interactive elements (buttons, links) with smooth physics-based micro-interactions.

### Links

- Solution URL: [Add your GitHub repository URL here](https://github.com/yourusername/your-repo-name)
- Live Site URL: [Add your GitHub Pages deployment URL here](https://yourusername.github.io/your-repo-name/)

## My Process

### Built with

- **Semantic HTML5 Markup:** Using meaningful layout constructs (`<main>`, `<section>`) to enhance accessibility.
- **CSS3 Custom Properties (`:root`):** To build a unified design token engine managing theme parameters and typographic weights.
- **CSS Flexbox Layout Engine:** Used exclusively for multidirectional, fluid layout composition across core wrappers.
- **Mobile-First Responsive Strategy:** Architected code progressively, utilizing optimized global fluid properties and setting responsive breakpoints (`@media min-width: 768px`) to ensure full structural adaptation across mid-tier tablets and widescreen laptops.

### What I learned

During the optimization phase of this project, I deepened my understanding of browser rendering mechanics, the CSS box-model, and layout scalability:

1. **Fluid Box Modeling over Fixed Dimensions:** I discovered that enforcing solid constraints like `width: 350px` restricts responsiveness on microscopic displays. Switching to a `width: 100%` model paired with a bounding `max-width` restriction ensures flawless cross-device layout preservation.
   
2. **Encapsulating Flexbox Items for Dynamic Spacing:** Instead of using rigid, hardcoded padding values (`padding-right: 4rem`) to force elements apart inside a flex wrapper, I learned to group contextual sub-elements inside secondary structural containers. This leverages the browser's native `justify-content: space-between` logic to distribute whitespace dynamically.

3. **Optimizing Micro-Interactions via Smooth CSS Transitions:** I learned that declaring a `transition` directly on a state selector like `:hover` breaks the animation timeline when the mouse leaves the element. Declaring transitions directly on the base structural class ensures smooth animation interpolation in both directions.

```css
/* Optimized interactive token animation */
.f-btn {
    background: var(--Blue-700);
    box-shadow: 0px 10px 20px rgba(56, 41, 224, 0.25);
    transition: background-color 0.3s ease, box-shadow 0.3s ease;
}

.f-btn:hover {
    background: hsl(245, 75%, 65%);
    box-shadow: 0px 15px 25px rgba(56, 41, 224, 0.4);
}
### Screenshot

*(Tip: After publishing your project on GitHub Pages, take a screenshot of your live site and save it to an `images` folder, then link it below)*
