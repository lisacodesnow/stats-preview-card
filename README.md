# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

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


**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./images/screenshot.png)


### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: (https://lisacodesnow.github.io/stats-preview-card/)

## My process

Work big to small. Out to in.
1. Break down the mobile design comp into containers
2. Decide what system to use between Flexbox and CSS Grid
  I used flexbox for mobile and Grid and Flexbox for desktop
3. Write html from top to bottom
  Figure out what elements to wrap in what
4. Write CSS starting with the top again, work inside of the container to layout the elements, and then keep working down
5. Lastly, add the tiny details (color, font, line-height, padding, margin)


### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow


### What I learned

1. I learned how to put a color over top of an image.
  That took a long time and alot of trial and error, but I figured it out.
  Had to wrap the image in another div.
  ```html
  <div class=photo>
    <img src="#">
  </div>
  ```
  Then I was able to add a color to the photo div, lower the opacity on the image and the color showed up

2. I had a gap between the photo and information in my mobile design
  I fixed it by making the photo div flex. And it made the image flush with the business card info
   ```css
   .photo{
    display: flex;
   }
   ```

3. In order to stop my photo and information card from getting too large when expanding the screen I set a max-width for the containers.

4. My information card and photo didn't have the same height. My photo was shorter than the card and wouldn't evenly line up, even with height and width 100%.
  I used grid for the outer container and set the photo and business card inside
  ```css
  .containter{
		display: grid;
		grid-template-columns: 1fr 1fr;
		width: 90%;
		max-width: 1200px;
	}
	.photo{
		grid-column: 2 / 3;
		grid-row: 1 /2;
		height: 100%;
	}
  #desktop-picture{
		opacity: .50;
		display: inline;
		width: 100%;
	}
	
	.business-info{
		width: 100%;
		grid-column: 1 / 2;
		height: 100%;
		display: flex;
		justify-content: center;
		align-content: center;
		
	}
  ```
  Doing this allowed my photo to reach the same height as the card


### Continued development

1. Continue to use flexbox and grid together.
2. Use grid for bigger containers and flex for smaller ones


## Author

- Website - [Lisa Thompson](https://lisacodesnow.github.io/stats-preview-card/)
- Frontend Mentor - [@lisacodesnow](https://www.frontendmentor.io/profile/lisacodesnow)




