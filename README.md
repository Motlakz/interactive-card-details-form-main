# Frontend Mentor - Interactive card details form solution

This is a solution to the [Interactive card details form challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/interactive-card-details-form-XpS8cKZDWw). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

- Fill in the form and see the card details update in real-time
- Receive error messages when the form is submitted if:
- View the optimal layout depending on their device's screen size
- See hover, active, and focus states for interactive elements on the page

### Screenshot

<img width="960" alt="image" src="https://user-images.githubusercontent.com/76655996/221414254-d4e319a9-3c5f-48ed-a5c1-44ffd23f33e2.png">

### Links

- Live Site URL: [https://motlakz.github.io/interactive-card-details-form-main]

## My process

- used the box model and semantic elements to position items on the page based on their respective viewports
- adapted the mobile-first approach to style each element
- applied styling and added a couple card components with respect to the given design and viewport sizes

### Built with

- Semantic HTML5 markup
- CSS Flexbox
- CSS Grid
- Mobile-first workflow
- Pure JavaScript

### What I learned

- I learned to add different payment options using icons from FontAwesome.
- How to create a vanishing view of one side of a card.
- How to reveal form inputs on the card as you type them in.

To see how you can add code snippets, see below:

```html
<div class="icons">
  <i class="fa fa-cc-visa" style="color:navy;"></i>
  <i class="fa fa-cc-paypal" style="color:blue;"></i>
  <i class="fa fa-cc-mastercard" style="color:red;"></i>
  <i class="fa fa-cc-discover" style="color:orange;"></i>
</div>
```

```css
.container .card-container .card-back{
    position: relative;
    height: 50%;
    width: 20vw;
    top: 0;
    background:linear-gradient(45deg, rgb(115, 107, 122), rgb(160, 62, 114));
    border-radius: 8px;
    padding-top: 20px;
    margin-top: 50px;
    text-align: right;
    backface-visibility: hidden;
    box-shadow: 0 15px 25px rgba(0,0,0,.5);
    transition: ease-in .4s;
}
```

```js
document.querySelector('.cvv-input').onmouseenter = () => {
  document.querySelector('.card-front').style.transform = 'perspective(1000px) rotateY(-180deg)';
  document.querySelector('.card-back').style.transform = 'perspective(1000px) rotateY(0deg)';
};
document.querySelector('.cvv-input').onmouseleave = () => {
  document.querySelector('.card-front').style.transform = 'perspective(1000px) rotateY(0deg)';
  document.querySelector('.card-back').style.transform = 'perspective(1000px) rotateY(180deg)';
};
document.querySelector('.cvv-input').oninput = () => document.querySelector('.cvv-box').innerText = document.querySelector('.cvv-input').value;
```

### Continued development

I intend to start using CSS preprocessors such as SASS/SCSS to clean up my code and JavaScript to keep certain items selected when the page is changed. I also plan on using custom properties to avoid repetition throughout my stylesheet

### Useful resources

- [Article Piece](https://alvaromontoro.com/blog/68002/creating-a-firework-effect-with-css) - This is a wonderful article helped me add the fireworks display to the modal page that appears after the form is filled.
- [YouTube Tutorial](https://www.youtube.com/watch?v=G7_VTWnWz40) - This is the awesome tutorial created by Mr. Web Designer that 'lent' me the code for the interactive form I created.

## Author

- Frontend Mentor - [@Motlakz](https://www.frontendmentor.io/profile/Motlakz)
- Twitter - [@MotlalepulaSel6](https://www.twitter.com/MotlalepulaSel6)
