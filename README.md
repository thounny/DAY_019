# DAY_019 |  Fullscreen Responsive Overlay Menu with Image Parallax Effect

## Project Overview

This project is part of my daily code challenge series, **DAY_019**, where I focused on building a fullscreen responsive overlay menu with an **image parallax effect** using **HTML**, **CSS**, **JavaScript**, and **GSAP**. The design is inspired by an element from **Arock** on **Awwwards**.

[Visit the incredible website by Arock!](https://arocksworld.com/)

---

## Preview

![DAY_019 Preview](./assets/DAY_019_1.gif)

## Inspiration

![Arock](./assets/DAY_019_2.gif)

---

## Key Features

- **Fullscreen Responsive Overlay Menu**: The menu slides in smoothly and adapts to various screen sizes, providing an engaging user experience.
- **Image Parallax Effect**: As users move their cursor, the images shift, creating a dynamic 3D effect.
- **GSAP Animations**: Transitions and parallax effects are powered by **GSAP** for professional-grade, smooth animations.
- **Responsive Design**: The layout and interactions are optimized for both desktop and mobile users.

---

## GSAP in Action

**GSAP (GreenSock Animation Platform)** powers the responsive overlay menu, ensuring fluid and interactive animations. Below are some key snippets of the animation and parallax effect setup:

### Menu Opening and Closing Animations

```javascript
const openMenu = () => {
  gsap.to(".menu", {
    clipPath: "polygon(0% 100%, 100% 100%, 100% 0%, 0% 0%)",
    pointerEvents: "all",
    duration: 1.25,
    ease: "power4.inOut",
  });
  gsap.to(".hero", {
    top: "-50%",
    opacity: 0,
    duration: 1.25,
    ease: "power4.inOut",
  });
};
```

**Explanation**:

- **Opening Animation**: The menu expands using `clipPath`, transitioning from an invisible state to a fullscreen overlay.
- **Smooth Transition**: GSAP’s `ease` options ensure that the transitions are smooth and visually appealing.

---

### Image Parallax Effect

```javascript
const updateParallax = (mouse) => {
  let dx = mouse.x - window.innerWidth / 2;
  let dy = mouse.y - window.innerHeight / 2;
  gsap.to(".menu-img", {
    duration: 2,
    transform: `rotate3d(${dy / 20}, ${dx / 20}, 0, 15deg)`,
    ease: "power3.out",
  });
};
```

**Explanation**

- **Parallax Movement**: The images in the menu react to the user's mouse movement, shifting and rotating to create a 3D effect.
- **Depth and Interaction**: This effect gives the menu a more immersive feel, enhancing user engagement.

---

## How to Run

1. **Clone the repository**:

   ```bash
   git clone https://github.com/thounny/DAY_019.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd DAY_019
   ```

3. **Open the `index.html` file** in your browser, or use a local development server like **Live Server** in VSCode.

---

## Project Structure

```bash
DAY_019/
│
├── assets/
├── css/
│   └── styles.css
├── fonts/
├── js/
│   └── menu.js
│   └── tilt.js
├── index.html
```

---

## Features

- **Fullscreen Overlay Menu**: A stylish menu that appears smoothly and provides a dynamic user experience.
- **Image Parallax**: Interactive images with a 3D parallax effect, reacting to cursor movement.
- **GSAP-Powered Animations**: High-performance animations controlled by GSAP.
- **Responsive Design**: Ensuring compatibility across all device sizes.

---

## Technologies Used

- **HTML5**: For the structure and layout.
- **CSS3**: Custom styling and responsiveness.
- **JavaScript (ES6)**: Handles the interactivity and animations.
- **GSAP (GreenSock Animation Platform)**: Powers the animations and parallax effects.

---

## Author

![Logo](./assets/thounny_logo.png)

**Thounny Keo**  
Creative Developer & Designer
Frontend Development Student | Year Up United

---

![Miku](./assets/miku.gif)