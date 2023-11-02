# Beginner Project - Clock Challenge

This is a solution to the Clock Challenger. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)



## Overview
  The objective is to create a real-time clock that accurately reads time from a provided image interface. This clock boasts a sleek and minimalist design, featuring hands for seconds, minutes, and hours, along with a digital display interface.

### The challenge
Users should be able to:

- Design the interface so that the hands can rotate around the clock's face. 
- use Date method to get the current time for the Clock


## My process
I initiated the process by creating the clock face and positioning each hand at the center of the clock. To determine the current time, I employed the JavaScript Date method.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Desktop-first workflow

### What I learned
I learnt about how Javascript Date Method functions. 
Additionally, this code snippet demonstrates how to synchronize the movement of the clock hands with the current time.

function setDate(){

    const now = new Date();
    const seconds = now.getSeconds();
    const secondsDegree = Math.round(((seconds / 60) * 360) + 90);
    secondHand.style.transform = `rotate(${secondsDegree}deg)`;
    const mins = now.getMinutes();
    const minsDegree = ((mins / 60) * 360) + 90;
    minHand.style.transform = `rotate(${minsDegree}deg)`;
    const hours = now.getHours();
    const hoursDegree = ((hours / 12) * 360) + 90;
    hourHand.style.transform = `rotate(${hoursDegree}deg)`;


    let time = `${hours}:${mins}`;
    console.log(digitalTime);

    digitalTime.innerHTML  = time;
    
}

### Continued development
- Ongoing development will include the addition of functionalities like the ability to change the watch face.

## Author
Name : Shavii