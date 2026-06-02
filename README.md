# 🌌 Pure CSS 3D Solar System

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![No JS](https://img.shields.io/badge/JavaScript-None-lightgrey?style=for-the-badge)

An interactive, 3D animated model of the Solar System built **100% with HTML and CSS**. No JavaScript was used. This project demonstrates advanced CSS 3D architecture, CSS state management, and complex keyframe animations.

> **[🌍 View Live Demo Here] (https://mcj5d6.csb.app/)**

*(

https://github.com/user-attachments/assets/829d40dd-ffec-4d24-90f9-e1467cad0895

)*
---

## ✨ Features

* **🚫 Zero JavaScript:** State management (Play/Pause, Speed Control) is handled entirely via CSS using hidden radio buttons, checkboxes, and the modern `:has()` pseudo-class.
* **🪐 3D Architecture:** Uses `transform-style: preserve-3d`, `rotateX`, and `translate` to create a realistic tilted orbital plane.
* **🎛️ Interactive Control Panel:** * Play/Pause the entire planetary animation globally.
  * Dynamically scale the speed of the orbits (0.5x, 1x, 2x, 3x) using CSS `calc()` and custom variables.
* **🔭 Detailed Planetary Elements:**
  * Custom gradients to mimic planetary textures (e.g., Jupiter's stripes, Mars' red hues).
  * Saturn's 3D rings and Earth's orbiting Moon.
  * Pulsing, glowing effect for the Sun.
* **ℹ️ Informational Pop-ups:** Hovering over any planet seamlessly displays its name, facts, and highlights it with a radiant text-shadow.

---

## 🛠️ Under the Hood (The CSS Magic)

This project relies heavily on modern CSS layout logic and clever styling techniques:

### 1. State Management via CSS Variables & `:has()`
Instead of using JavaScript event listeners, the UI controls use hidden HTML inputs. The CSS `:has()` selector detects which button is checked and updates global CSS variables instantly.
```css
/* Updating speed scale without JS */
body:has(#speed-2:checked) { --speed-scale: 2; }

/* Pausing all animations globally */
body:has(#pause-cb:checked) { --play-state: paused; }

```

### 2. Math & Animation Scaling

Orbit speeds are controlled via inline CSS variables (`--duration`) on the HTML elements. The actual animation speed is calculated on the fly by dividing the base duration by the user's selected speed scale.

```css
animation: spin calc(var(--duration) / var(--speed-scale)) infinite linear;

```

### 3. The Counter-Spin Technique

To prevent the planets and their text labels from spinning upside down as they orbit the sun, a `counter-spin` animation is applied to the planet wrappers. This rotates them in the exact opposite direction of the orbit, keeping them perfectly upright to the viewer.

---

## 🚀 Getting Started

Since this project uses no build tools or dependencies, running it is incredibly simple.

1. **Clone the repository:**
```bash
git clone [https://github.com/your-username/solar-system-css.git](https://github.com/your-username/solar-system-css.git)

```


2. **Navigate to the directory:**
```bash
cd solar-system-css

```


3. **Open the project:**
Simply double-click the `index.html` file to open it in your default web browser, or use an extension like VS Code Live Server.

---

## 📂 File Structure

```text
📦 solar-system-css
 ┣ 📜 index.html   # The structural layout, hidden inputs, and CSS variables
 ┣ 📜 style.css    # The 3D logic, state management, and animations
 ┗ 📜 README.md    # Project documentation

```

---

## 💡 Future Improvements

* [ ] Add mobile responsiveness (adjust `--zoom` variable based on screen width).
* [ ] Add asteroid belt using box-shadow particle generation.
* [ ] Introduce orbital inclination (different tilt angles for different planets).

---
---

