# Hamburger Menu Examples

This project explores how **hamburger menus** work and shows two different versions of the same basic idea:

1. **Hamburger Menu** – the main example and the version we will focus on for class
2. **Animated Icon** – a more advanced version where the icon itself animates into an “X”

The project also includes an **overview page** that explains what a hamburger menu is, why websites use them, and some of the pros and cons of this navigation pattern.

---

## What is a hamburger menu?

A **hamburger menu** is a navigation pattern that hides links behind a small icon. That icon usually looks like **three horizontal lines**. When the user clicks or taps the icon, the menu opens.

Hamburger menus are especially common on **phones and tablets** because smaller screens do not leave much room for a full horizontal navigation bar.

---

## Why do websites use hamburger menus?

Hamburger menus can be useful because they:

- save space on smaller screens
- help keep layouts cleaner
- allow navigation to stay available without always taking up room on the page

But they also have tradeoffs:

- navigation is hidden until the user clicks
- some users may not notice the icon right away
- important links can become less visible

Like many web design choices, a hamburger menu is not always right or wrong. It depends on the layout, audience, and goals of the website.

---

## What this project includes

### `index.html`
This is the **overview page**. It explains the concept of a hamburger menu and links to the two example pages.

### `hamburger-menu.html`
This is the **main example** and the one most important for class. It uses a hidden checkbox and a label to open and close a dropdown navigation menu on smaller screens.

### `hamburger-menu.css`
This stylesheet contains the menu-specific styles for the main hamburger menu example.

### `animated-icon.html`
This is a more advanced variation. It uses the same basic idea, but the hamburger icon itself also animates.

### `animated-icon.css`
This stylesheet contains the menu-specific styles for the animated icon example.

### `overview.css`
This stylesheet controls the layout and design of the overview page.

### `shared.css`
This stylesheet contains the general page styles shared by both menu example pages, such as page background, content area styling, footer styling, and color themes.

### `reset.css`
This reset file removes browser default styling so the pages behave more consistently.

---

## How the main hamburger menu works

The main hamburger menu uses a simple HTML and CSS technique:

- A hidden **checkbox** stores whether the menu is open or closed
- A **label** acts as the visible hamburger button
- When the label is clicked, it toggles the checkbox
- CSS uses the `:checked` state of the checkbox to reveal the menu

In the main example, the menu is hidden by default on smaller screens using:

- `max-height: 0;`
- `overflow: hidden;`

When the checkbox is checked, the menu expands using a larger `max-height`.

Because `max-height` can be animated, this creates a smoother opening effect than simply using `display: none;`.

---

## How the animated icon version is different

The animated icon version uses the same general idea, but adds more CSS so the icon itself changes shape when the menu opens.

In that version:

- the icon is built with three `<span>` elements
- each span forms one line of the hamburger icon
- CSS transforms rotate and move the lines
- the middle line fades out
- the icon changes from three lines into an “X”

This creates a more polished effect, but it also requires more code.

---

## Why the CSS is split across multiple files

This project separates the CSS by purpose:

- **`shared.css`** handles the general page styling
- **`hamburger-menu.css`** handles only the main menu behavior
- **`animated-icon.css`** handles only the advanced animated icon version

This makes the code easier to understand and reuse.

For example, if you want to copy just the menu behavior into one of your own projects later, it is easier to identify which CSS rules are responsible for the menu itself.

---

## Tips for learning from this project

As you explore the files, pay close attention to these ideas:

- how the `label` and `input` work together
- why the checkbox is hidden but still important
- why the checkbox appears **before** the `<ul>` in the HTML
- how `#menu:checked + ul` works in the main example
- how `#menu-toggle:checked ~ ul` works in the animated icon example
- why `max-height` is used instead of `display: none`
- how CSS transitions improve the user experience

---

## Good customization ideas

If you want to experiment with the code, try changing:

- the header colors
- the dropdown menu background color
- the link hover color
- the size of the hamburger icon
- the spacing inside the menu
- the width of the dropdown
- the animation speed

The CSS comments in the example files explain what many of these values control.

---

## How to move this code into your own project

If you want to reuse one of these hamburger menus in your own website, move the code carefully so the HTML and CSS still match each other.

### 1. Copy the correct HTML structure

Start by copying the menu code from either:

- `hamburger-menu.html`
- `animated-icon.html`

Be careful not to leave out important parts like:

- the hidden `input`
- the `label`
- the `ul` of links
- the `span` elements inside the animated icon version

These parts work together. If one is missing, the menu may stop working.

### 2. Keep the HTML in the same order

The order of the elements matters.

For example, in the main hamburger menu version, the CSS uses:

`#menu:checked + ul`

That means the `ul` must come **immediately after** the checkbox in the HTML.

In the animated icon version, the CSS uses:

`#menu-toggle:checked ~ ul`  
`#menu-toggle:checked + label`

That means the checkbox, label, and menu must stay in the correct order for the selectors to work.

If you rearrange the HTML, the menu may stop opening or animating.

### 3. Copy the correct CSS file too

Do not copy only the HTML.

You also need to copy the matching CSS from:

- `hamburger-menu.css` for the main example
- `animated-icon.css` for the advanced example

You may also want to copy some supporting styles from `shared.css`, especially if you want the page to look similar.

### 4. Check your class names and IDs

Make sure these still match between the HTML and CSS:

- `id="menu"`
- `id="menu-toggle"`
- `class="menu-icon"`

If you change an ID or class name in the HTML, you must also change it in the CSS.

### 5. Watch out for color and layout dependencies

Some colors and page styles come from `shared.css`.

If you copy only the menu CSS into your own project, the menu will still work, but it may not look exactly the same unless you also copy or recreate:

- header background colors
- text colors
- spacing
- dropdown background styles

### 6. Test the menu at small screen sizes

A hamburger menu usually only appears at smaller screen widths because of the media query.

After moving the code into your own project:

- resize the browser window
- test the menu on a narrow screen
- click the icon to make sure it opens and closes correctly

If the menu seems to “disappear,” it may simply still be in desktop mode.

### 7. Customize it after it works

First, make sure the copied version works.

Then you can start customizing things like:

- colors
- icon size
- spacing
- hover styles
- animation speed
- dropdown width

It is usually better to get the menu working first and then make visual changes one step at a time.

## Quick checklist

Before you finish moving the menu into your own site, make sure:

- the HTML structure is complete
- the elements are in the correct order
- the CSS file is copied too
- the IDs and classes still match
- the media query is still present
- the menu works on a small screen

---

## Suggested order for exploring the project

1. Open **`index.html`** and read the overview
2. Open **`hamburger-menu.html`** and study the main example
3. Resize the browser window and test the menu
4. Look through **`hamburger-menu.css`**
5. Open **`animated-icon.html`** and compare it to the main example
6. Study **`animated-icon.css`** to see how the icon animation works

  ---

This project was created for learning, experimentation, and discussion in Web Design 2.

You are welcome to use and adapt this code in your own projects.
