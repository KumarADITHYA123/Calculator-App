# Calculator App

A responsive calculator app that allows users to perform basic mathematical operations and customize the theme based on their preferences.

## Table of Contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My Process](#my-process)
  - [Built With](#built-with)
  - [What I Learned](#what-i-learned)
  - [Future Improvements](#future-improvements)
  - [Resources](#resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- See the size of the elements adjust based on their device's screen size
- Perform mathematical operations like addition, subtraction, multiplication, and division
- Adjust the color theme based on their preference
- **Bonus**: Have their initial theme preference checked using `prefers-color-scheme` and have any additional changes saved in the browser

### Screenshots

![](./design/Screenshot_38.png)
![](./design/Screenshot_39.png)
![](./design/Screenshot_40.png)

### Links

- **Live Site URL**: [https://calculatorapp124.netlify.app/]

## My Process

### Built With

- Semantic HTML5
- CSS custom properties
- Flexbox and CSS Grid
- Desktop-first workflow
- JavaScript

### What I Learned

- Implemented a three-state toggle button for theme switching.
- Enhanced understanding of responsive design and browser storage for theme preferences.

````css
.radio {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 0.5rem;

  input[name="toggle"] {
    appearance: none;
    border-radius: 50%;
    opacity: 0;
    width: 15px;
    height: 15px;
  }

  input[name="toggle"]:hover {
    cursor: pointer;
  }

  #one {
    opacity: 1;
    background-color: hsl(6, 63%, 50%);
  }

  #two {
    background-color: hsl(25, 98%, 40%);
  }

  #three {
    background-color: hsl(176, 100%, 44%);
  }

  label {
    font-size: 10px;
  }

  > label {
    position: absolute;
    top: 0;
  }
}


```js
const arr = [...radioBtns];
// console.log(arr);

arr.forEach((element) => {
  element.addEventListener("click", () => {
    element.style.opacity = "1";

    arr
      .filter((item) => item != element)
      .forEach((item) => {
        item.style.opacity = "0";
      });
  });
});
````

### Continued development

I'll keep pushing myself to becoming better at programming. I really love programming, I don't ever regret the day I made the decision to join.

### Useful resources

- [CSS Tricks](https://css-tricks.com/) - Helped me understand and implement the three-state toggle button for theme switching.
- [MDN Web Docs](https://developer.mozilla.org/) - A valuable resource for understanding responsive design and browser storage.

## Author

[Author](https://kumaradithya123.netlify.app/)

```

```
