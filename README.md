# Frontend Mentor - News homepage solution

This is a solution to the [News homepage challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/news-homepage-H6SWTa1MFl). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page
- Toggle the mobile menu

### Screenshot

![Desktop Design](./design/desktop-design.jpg)
![Mobile Design](./design/mobile-design.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/yourusername/news-homepage)
- Live Site URL: [Live Demo](https://news-homepage-three-rouge.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- SCSS/Sass with 7-1 architecture pattern
- CSS Grid
- Flexbox
- Mobile-first workflow
- Vanilla JavaScript for mobile menu toggle
- Custom CSS mixins and variables

### What I learned

This project was an excellent opportunity to practice **CSS Grid layout** and **SCSS architecture**. I implemented a clean folder structure following the 7-1 pattern, separating concerns into:

- `abstracts/` - variables and mixins
- `base/` - reset and typography
- `components/` - buttons, navigation, header
- `layout/` - grid, hero, sidebar, trending sections

**Key learnings:**

1. **SCSS Architecture**: Organized styles into modular, reusable files making the codebase scalable and maintainable.
```scss
// Using mixins for responsive design
@mixin desktop {
@media (min-width: $breakpoint-desktop) {
@content;
}
}
```

2. **CSS Grid Mastery**: Created complex layouts with CSS Grid, especially the hero section and trending cards.
```scss
.grid {
display: grid;
@include desktop {
grid-template-columns: 1fr 1fr 1fr;
grid-template-rows: auto auto;
gap: 4.375rem 1.875rem;
}
}
```

3. **Mobile Menu Implementation**: Built a smooth sliding menu with overlay using vanilla JavaScript and CSS transitions.

```js
menuToggle.addEventListener('click', () => {
menuToggle.classList.toggle('active');
nav.classList.toggle('active');
overlay.classList.toggle('active');
});
```

4. **Responsive Images**: Implemented different images for mobile and desktop views maintaining optimal performance.

5. **Hover States**: Added smooth transitions and color changes for all interactive elements improving user experience.

### Continued development

Areas I want to continue focusing on:

- **Accessibility**: Implementing keyboard navigation and ARIA labels for better screen reader support
- **Performance optimization**: Further optimizing images and CSS delivery
- **Advanced animations**: Adding more sophisticated micro-interactions
- **Testing**: Implementing unit tests for JavaScript functionality

## Author

- Frontend Mentor - [@devbyroman](https://www.frontendmentor.io/profile/devbyroman)
- GitHub - [@devbyroman](https://github.com/devbyroman)

---

## Project Structure

news-homepage/
├── assets/
│ ├── fonts/
│ └── images/
├── styles/
│ ├── abstracts/
│ │ ├── _variables.scss
│ │ └── _mixins.scss
│ ├── base/
│ │ ├── _reset.scss
│ │ └── _typography.scss
│ ├── components/
│ │ ├── _buttons.scss
│ │ ├── _header.scss
│ │ ├── _navigation.scss
│ │ └── _overlay.scss
│ ├── layout/
│ │ ├── _container.scss
│ │ ├── _grid.scss
│ │ ├── _hero.scss
│ │ ├── _sidebar.scss
│ │ └── _trending.scss
│ └── main.scss
├── js/
│ └── script.js
├── index.html
└── README.md


## Installation

1. Clone the repository:
git clone https://github.com/devbyroman/news-homepage.git


2. Navigate to the project directory:
cd news-homepage


3. Open `index.html` in your browser or use a local server.

## Acknowledgments

- [Frontend Mentor](https://www.frontendmentor.io) for providing this challenge
- The Frontend Mentor community for inspiration and feedback
