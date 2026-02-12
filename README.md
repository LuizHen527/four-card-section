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
- [Author](#author)

## Overview

### Screenshot

![]()

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

![mobile screen](/assets/images/screen-cards-mobile.jpg)
![tablet screen](/assets/images/screen-cards-tablet.jpg)
![desktop screen](/assets/images/screen-cards-desktop.jpg)

I was studying Layout Grid on the Odin Project, so I decided to use it. And It got the job done.
With Layout Grid I could change the position of the cards to different parts of the grid. I could even change the order.
Grid its a very powerful tool.

This was how I made the grid for the tablet screen size:

```.cards-box {
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

For the desktop, all I have to do was change the grid cell sizes and the position of the elements on it:

```.cards-box {
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

- [Example resource 1](https://www.example.com) - This helped me for XYZ reason. I really liked this pattern and will use it going forward.
- [Example resource 2](https://www.example.com) - This is an amazing article which helped me finally understand XYZ. I'd recommend it to anyone still learning this concept.

**Note: Delete this note and replace the list above with resources that helped you during the challenge. These could come in handy for anyone viewing your solution or for yourself when you look back on this project in the future.**

### AI Collaboration

Describe how you used AI tools (if any) during this project. This helps demonstrate your ability to work effectively with AI assistants.

- What tools did you use (e.g., ChatGPT, Claude, GitHub Copilot)?
- How did you use them (e.g., debugging, generating boilerplate, brainstorming solutions)?
- What worked well? What didn't?

**Note: Delete this note and the content above if you didn't use AI, or replace with your own experience.**

## Author

- Website - [Add your name here](https://www.your-site.com)
- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@yourusername](https://www.twitter.com/yourusername)

**Note: Delete this note and add/remove/edit lines above based on what links you'd like to share.**

## Acknowledgments

This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit.

**Note: Delete this note and edit this section's content as necessary. If you completed this challenge by yourself, feel free to delete this section entirely.**
