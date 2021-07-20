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
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Desktop](./screenshots/desktop.png)
![Mobile](./screenshots/mobile.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process
- I will solve this challenge by doing mobile-first approach. Reason I do this is I find it easier creating the structure of the HTML and setting up CSS by creating the mobile design first. As making it responsive to larger screens is an easier process in my opinion. But I also see many developers recommending using this approach.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

**Note: These are just examples. Delete this note and replace the list above with your own choices**

### What I learned

#### Using CSS variables
I never used this much, but have also known about them. I noticed especially when doing only HTML and CSS I find the CSS variables quite useful. If I were to create this in React id probably not use CSS variables, as id use `Styled Components` to store colors, pixels ...

#### Adding border radius to specific corners
A problem I stumbleded upon in this project, was too achieve border-radius on the photo aswell. I thought since the image is a child of the main container `card-wrapper` it would also get the border-radius if I assigned border-radius to that CSS class. But seems that did not work! There might be a work around or better solution, but I ended up defining border-radius for specific corner of the image, depenedent on the size of the browser (Desktop has border-radius on top-right and bottom-right. While mobile is top-left, top-right).

I was happy to see, it follows same logic as `padding` and `margin` with it being: 
```css {
  border-radius: top, right, bottom, left
}
```

#### Adding background color to image
I never have used `url(<imgUrl>)` before. As I found this a bit confusing, regarding accessibility I am not sure if this is a good way of using a photo, but it might be possible to provide an `alt` tag in CSS also. I searched the web to find a simple way to achieve purple color on the photo. And stumbled across a method which only needs two lines:

```css 
.purple-background-on-image {
  background: url(`./images/image-header-desktop.jpg), var(--accent);
  background-blend-mode: multiply;
}
```
How this works, is that when you use `background-blend-mode: multiply` it will blend the color which you define AFTER the backgorund image, and the color will be applied onto the photo!
I liked this solution as it is only two lines, and were not dependent on `linear-gradient` as many solutions I found were based on using that property.
**Note: Only concern is the photo color is not exactly the same as the preview photo showed...**

#### Background-size cover
I did not understand why the photo did not want to take the full space it had, but then later realised that it is `background-size: cover` which does the magic for that! 

### Continued development

Use this section to outline areas that you want to continue focusing on in future projects. These could be concepts you're still not completely comfortable with or techniques you found useful that you want to refine and perfect.

There are certain things I want to improve which are:
`Better naming`
  - I usually end up stopping for a second, as I never seem to find a name I find most desriptive. (E.G `flexin` is not a descriptive CSS selector name in my opinion, but I understand what it means, haha).

`Background with image in CSS`
  - I always use `<img>` HTML tag when using pictures, but this session helped me realize how this can be used only in CSS! (Ill have to check how accessibility friendly it is though).

`Write more readable and structured CSS code`
  - Using CSS variables surely helped making it easier using more of the same values and keeping it a bit more structured. But I feel that I maybe use to many CSS selectors, or could have done thing differently... but I think the solution is OK (I am quite the perfectionist... it can be a bad habit of never being satisfied 😂).

`Create this using a framework like React`
  - I mostly work with Angular (only because of my job), but really want to try this in React! I usually tend to only solve it in vanilla way, since I am most comfortable with that, and libraries are not needed... which I prefer, since I am lazy....

### Useful resources

- [W3Schools](www.w3schools.com) - This helped me with understanding the different properties `background` has to offer
- [Stack Overflow - Add overlay to background image](https://stackoverflow.com/questions/36679649/how-to-add-a-color-overlay-to-a-background-image/36679903) - The answer in this post surely introduced me to a fast and easy way to add a single color overlay to a image! 
- [MDN - background-blend-mode](https://developer.mozilla.org/en-US/docs/Web/CSS/background-blend-mode) - My favorite documentation website when needing to check how different properties and attributes work!

## Author

- Frontend Mentor - [@yourusername](https://www.frontendmentor.io/profile/gleative)
- Twitter - [@yourusername](https://www.twitter.com/gleative)