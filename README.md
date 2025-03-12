# Hamburger Menus

## What is a Hamburger Menu?
A **hamburger menu** is a type of navigation menu that hides links behind a small icon consisting of three horizontal lines (**☰**). It is commonly used in **mobile and responsive web design** to save screen space while still providing access to important navigation links.

### **When and Why is a Hamburger Menu Used?**
Hamburger menus are used when:
- **Screen space is limited** (e.g., mobile screens, small devices).
- **Navigation items are secondary** (e.g., not essential to always be visible).
- **A cleaner UI is preferred** (e.g., minimalistic web design trends).
- **The focus is on content** rather than navigation (e.g., blog posts, articles, media pages).

While a hamburger menu can be useful, it is sometimes criticized for **hiding important navigation** and reducing discoverability. Some websites use alternative approaches like **sticky navigation bars** or **tabbed menus** to improve usability.

---

## Coding Examples
This repository contains three different implementations of a hamburger menu, each demonstrating a different level of complexity and animation effects.

### **1 - Basic Hamburger Menu `index.html` & `basic.css`**
This is the simplest version of a hamburger menu, built using only HTML and CSS.

**How It Works:**
- Uses a **checkbox input** and a **label** with the ☰ icon.
- When the checkbox is checked, the menu appears.
- The menu is hidden by default using CSS `display: none;`
- **No animations** are used. Just a basic toggle effect.

**Best for:** Beginners who want to understand how a pure **CSS-only menu toggle** works.

---

### **2 - Animated Hamburger Menu `animated-menu.html` & `animated-menu.css`**
This version enhances the basic menu by adding a **smooth slide-down animation** when opening and closing the menu.

**How It Works:**
- Uses a **hidden checkbox** for toggling the menu.
- Instead of `display: none;`, it uses **`max-height`** and a **CSS transition** for smooth sliding.
- The menu expands and collapses over `0.5s` for a better user experience.

**Best for:** Those who want to learn about **CSS animations** and **improving UI transitions**.

---

### **3 - Animated Icon Menu `animated-icon.html` & `animated-icon.css`**
This version animates **both the menu and the hamburger icon**, turning the ☰ icon into an **X** when clicked.

**How It Works:**
- Uses a **hidden checkbox** to control both the menu and the icon.
- The ☰ icon is built using a `<span>` element with `::before` and `::after` pseudo-elements.
- When checked:
  - The **middle line disappears** `opacity: 0;`
  - The **top line rotates down** `rotate(-45deg);`
  - The **bottom line rotates up** `rotate(45deg);`

**Best for:** Advanced learners interested in **CSS transforms, animations, and UI enhancements**.

---

## How to Use This Project
1. Open each HTML file `index.html`, `animated-menu.html`, `animated-icon.html` in a browser.
2. Resize the browser window or use **mobile view** to see the hamburger menu in action.
3. Click the ☰ icon to test the menu interactions.
4. Study each version's **CSS files** to understand how each version works. I left comments to explain what most of the style rules are doing.

Feel free to use and modify these examples in your own projects!