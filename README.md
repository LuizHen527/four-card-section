# Frontend Mentor - Four card feature section solution

This is a solution to the [Four card feature section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/four-card-feature-section-weK1eFYK). Frontend Mentor challenges help you improve your coding skills by building realistic projects. Status: Completed.

## Table of contents

- [Overview](#overview)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#Coded by)

## Overview

### Screenshot

![](/assets/images/page-screen-shot.png)

### Links

- Live Site URL: [Add live site URL here](https://luizhen527.github.io/four-card-section/)

## My process

### Built with

- HTML
- CSS
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- BEM

### What I learned

The challenge was to find a way to change the order of the cards between screen sizes.

- mobile layout:
  
![mobile screen](/assets/images/screen-cards-mobile.jpg)

- tablet layout:
  
![tablet screen](/assets/images/screen-cards-tablet.jpg)

- desktop layout:
  
![desktop screen](/assets/images/screen-cards-desktop.jpg)

I was studying Layout Grid on the Odin Project, so I decided to use it. And It got the job done.
With Layout Grid I could change the position of the cards to different parts of the grid. I could even change the order.
Grid its a very powerful tool.

I made the mobile screen with Flexbox and the Tablet/Desktop with Grid. This was how I made the tablet screen size:

```
    .cards-box {
        display: grid;
        grid-template: repeat(3, 250px) /  1fr 1fr 1fr 1fr;
        justify-items: center;
    }

    .card--red {
        grid-column: 2 / span 2;
    }

    .card--cyan {
        grid-column: 1 / span 2;
        grid-row: 2;
    }

    .card--yellow {
        grid-column: 3 / span 2;
    }

    .card--blue {
        grid-column: 2 / span 2;
        grid-row: 3;
    }
```

For the desktop, all I had to do was change the grid cell sizes and the position of the elements on the Grid:

```
    .cards-box {
        grid-template: 1fr 1fr 1fr 1fr / 1fr 23.6rem 1fr;
        column-gap: 0;
    }

    .card--red {
        grid-column: 2;
        grid-row: 1 / span 2;
    }

    .card--cyan {
        grid-column: 1;
        grid-row: 2 / span 2;
        margin-left: auto;
    }

    .card--yellow {
        grid-column: 2;
        grid-row: 3 / span 2;
    }

    .card--blue {
        grid-column: 3;
        grid-row: 2 / span 2;
        margin-right: auto;
    }
```

### Continued development

I want to improve:

- Use of Layout Grid.

### Useful resources

- [CSS-Tricks Grid Layout Guide](https://css-tricks.com/complete-guide-css-grid-layout/) - Very useful for quick reference. I used to check if I could do something with Grid.

## Coded by

- Linkedin - [@luizhen765](https://www.linkedin.com/in/luizhen765/)