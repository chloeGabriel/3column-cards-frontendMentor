# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process
Looking at the design, I started first to divide the components of the 3 cards, to make my code
tidy and clean. Like atomic design.
In a <main>, I put a <div class="containter"> to put inside the 3 cards.
I divide each card in 3 parts : 
 - card-header that contains the icon and the title, 
 - card-body for the text content
 - and card-footer for the button
 
For the CSS part, I started to code the general settings properties of the challenge.
Next step, I coded the main properties by using the flex box and fixed the size of the tag.

The following step were to code the properties of the container class and the cards.
I also wanted to create 3 classes for the different colors used in this challenge as well.

Then I wrote the properties for the cards elements, such as .card-header, .card-body, .card-footer and the button inside
the card-footer. For the button, I add a transparent border. It's important to use it for the hovering properties. 
Without it, looks like the button is moving.


### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow


### What I learned

1) I've learned the deeper use of @media for the responsive properties. Specially for the flex box attributes
to change it from rox to column whenever the screen size is changing.

2) Using the <main> could be useful, especially to create a content properly.

```html
<main>
	<div class="container">
		<!-- Card Sedans -->
		<div class="card bg-first">
			<div class="card-header">
				<img src="images/icon-sedans.svg">
				<h1>Sedans</h1>
			</div>
			<div class="card-body">
				<p>Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city
					or on your next road trip.</p>
			</div>
			<div class="card-footer">
				<button class="first">Learn More</button>
			</div>
		</div>
    </div>
</main>
```
```css
@media only screen and (min-width: 300px) and (max-width: 989px) {
    main {
        height: 180vh;
    }
    .container {
        flex-direction: column;
        max-width: 350px;
    }
    .bg-first {
        border-radius: 10px 10px 0 0;
    }
    .bg-third {
        border-radius: 0 0 10px 10px;
    }

    .card-header, .card-body, .card-footer {
        margin: 10px 0 5px 0;
    }
    button {
        margin-top: 5px;
    }

    .attribution {
        position: relative;
        margin: 20px auto;
    }
}

@media only screen and (min-width: 990px) and (max-width: 1100px) {
    .card {
        padding: 40px;
    }
}
```

### Continued development

It's interesting to improve the responsive design skill through this kind of exercices.
These type of challenge is what I'm looking form to improve my CSS responsive skills.
It's an important knowledge I'd like to strengthen more.

## Author

- Frontend Mentor - [@chloeGabriel](https://www.frontendmentor.io/profile/chloeGabriel)
