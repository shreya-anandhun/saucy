# 🍕 Saucy

**Saucy** is a playful food-ordering website for a pretend restaurant that sells pizza, burgers, drinks and desserts.

👉 **Live site:** https://shreya-anandhun.github.io/saucy/

You can browse the menu, add food to your order, change how many you want, and "place" the order. It's a front-end demo, so no real food gets cooked and no money changes hands 🙂

---

## ✨ What you can do on the site

| Feature | What it means |
|---|---|
| **Browse the menu** | See 12 dishes laid out as cards, each with a picture, price and short description. |
| **Filter by category** | Tap *Pizza*, *Burgers*, *Drinks* or *Desserts* to see only that kind of food. |
| **Add to order** | Click a button and the food "flies" into your cart at the top. |
| **Change amounts** | Use the **−** and **+** buttons to pick how many you want. |
| **See your bill** | Open the cart to see a paper-style receipt with the subtotal, packing fee, 5% GST and the total. |
| **Place the order** | Hit *Place order*. The receipt tears away, sprinkles burst out and you get an order number. |
| **Late-night mode** | The 🌙 button switches the site to a dark colour theme. It remembers your choice next time. |
| **Veg / non-veg marks** | A green dot means vegetarian. A brown triangle means non-vegetarian. |

It works on phones, tablets and laptops.

---

## 📁 What's in this project

The whole website lives in **one file**:

```
saucy/
├── index.html   ← the entire website (structure, looks, and behaviour)
└── README.md    ← this explanation
```

No installs and no setup. To run it on your own computer, just **double-click `index.html`** and it opens in your browser.

---

## 🧱 The three building blocks

Every website is made of three things. Think of building a house:

| Language | House comparison | What it does in Saucy |
|---|---|---|
| **HTML** | The walls and rooms | Puts things on the page: the logo, menu, buttons, cart and footer. |
| **CSS** | The paint and furniture | Decides how it looks: colours, fonts, the checked tablecloth background, rounded cards and all the animations. |
| **JavaScript** | The electricity | Makes things *happen* when you click: adding to cart, adding up the bill, switching tabs and dark mode. |

All three are inside `index.html`. The CSS sits in a `<style>` section and the JavaScript sits in a `<script>` section.

---

## 🗂️ How the code is organised

### 1. HTML: the page layout
The page is split into sections, top to bottom:

- **Nav bar** (`<header>`): the Saucy logo, a *Menu* link, the dark-mode button and the cart button.
- **Hero** (`<section class="hero">`): the big bouncy "Saucy" title with floating food stickers around it.
- **Marquee**: the red ribbon of scrolling words ("Wood-fired pizza ✺ Smash burgers ✺ ...").
- **Menu** (`<section class="menu">`): the category tabs and the grid of food cards.
- **Footer** (`<footer>`): the giant outlined "Saucy" at the bottom.
- **Cart drawer** (`<aside class="drawer">`): the panel that slides in from the right with your receipt.

### 2. CSS: the look and feel
- **Colour palette:** powder blue, cobalt (dark blue), tomato red, butter yellow, strawberry pink and pistachio green.
- **Fonts:** three free Google Fonts. *Shrikhand* for big bubbly headings, *Bricolage Grotesque* for normal text and *DM Mono* for the receipt (so it looks like a till printer).
- **Retro style:** thick outlines and solid "offset" shadows that sit slightly to the bottom-right, like a cartoon sticker.

### 3. JavaScript: the brain
The script is split into 12 numbered parts, each with a comment heading:

| # | Part | In plain words |
|---|---|---|
| 1 | **Illustrations** | Draws every food picture with code. There are no photo files. |
| 2 | **Menu data** | A list of all 12 dishes with their name, price, category, description and veg/non-veg. |
| 3 | **State** | Remembers what's in your cart and which tab you're on. |
| 4 | **Elements** | Finds the parts of the page the code needs to change. |
| 5 | **Hero** | Makes the title letters drop in and wobble, and makes the stickers follow your mouse. |
| 6 | **Category tabs** | Builds the filter tabs and slides the dark "pill" to the one you picked. |
| 7 | **Food cards** | Builds each menu card and makes it tilt in 3D when you hover. |
| 8 | **Cart logic** | Adds and removes items and works out the bill. |
| 9 | **Drawer** | Opens and closes the cart panel and handles *Place order*. |
| 10 | **Effects** | Flying food, the sprinkle burst, pop-up messages and the custom cursor ring. |
| 11 | **Late-night mode** | Switches between light and dark colours and remembers your choice. |
| 12 | **Start** | Runs everything once the page loads. |

### How the bill is worked out
```
Subtotal = price × quantity, added up for every item
Packing  = ₹25 (only if the cart isn't empty)
GST      = 5% of the subtotal, rounded
Total    = Subtotal + Packing + GST
```

---

## 📖 Glossary: tech words, simplified

### General terms
| Term | Simple meaning |
|---|---|
| **Front-end** | The part of a website you can see and click. Saucy is only front-end: there's no server or database behind it. |
| **Browser** | The app you use to visit websites (Chrome, Safari, Edge...). |
| **Responsive** | The layout adjusts itself to fit any screen, from a phone to a big monitor. |
| **Accessibility (a11y)** | Making the site usable for everyone, including people using screen readers or only a keyboard. |
| **GitHub Pages** | A free GitHub service that turns the files in this repo into a live website. |
| **Repository (repo)** | A project folder stored on GitHub that keeps the history of every change. |

### HTML terms
| Term | Simple meaning |
|---|---|
| **Tag** | A label in angle brackets, like `<button>`, that tells the browser what something is. |
| **`class`** | A name tag on an element so CSS and JavaScript can find it, like `class="card"`. |
| **`id`** | Like a class, but unique: only one element on the page can have it. |
| **`data-*` attributes** | Little notes stored on an element, e.g. `data-add="margherita"` means "this button adds a Margherita". |
| **`aria-*` attributes** | Hidden labels that tell screen readers what something is, e.g. `aria-label="Close your order"`. |
| **SVG** | A picture made from shapes described in code (circles, lines, curves). It stays sharp at any size. All the food drawings are SVG. |

### CSS terms
| Term | Simple meaning |
|---|---|
| **CSS variables** (`--tomato`) | A saved value you can reuse. Change `--tomato` once and every red on the site changes. |
| **Flexbox / Grid** | Two ways to line things up in rows and columns. The menu cards use *Grid*. |
| **`@keyframes`** | A step-by-step animation recipe, e.g. "start small, then grow big". |
| **`transition`** | Makes a change happen smoothly instead of instantly (like a button easing into its hover colour). |
| **`cubic-bezier`** | A curve that controls an animation's speed. Saucy uses a "bounce" curve so things overshoot and settle, like jelly. |
| **Media query** (`@media`) | A rule that only applies in some situations, e.g. "if the screen is narrower than 720px, hide the menu link". |
| **`prefers-color-scheme`** | Checks whether your device is in dark mode, so the site can match it. |
| **`prefers-reduced-motion`** | Checks whether you've asked your device for less animation. If so, Saucy turns its animations off. |
| **Box shadow** | A shadow behind a box. Here it's a hard, offset shadow for the sticker look. |
| **Mask** | Hides part of an element. It's how the receipt gets its zig-zag torn bottom edge. |

### JavaScript terms
| Term | Simple meaning |
|---|---|
| **Variable** (`const`, `let`) | A labelled box that holds a value. `const` can't be swapped for a new value; `let` can. |
| **Function** | A reusable set of instructions with a name, like `addItem()` or `openCart()`. |
| **Arrow function** (`=>`) | A shorter way to write a function. |
| **Array** (`[ ]`) | An ordered list, like the list of menu items. |
| **Object** (`{ }`) | A bundle of labelled info, like `{ name: 'Margherita', price: 349 }`. |
| **`Map`** | A lookup table. The cart is a Map: *dish → how many*. |
| **`$` and `$$`** | Shortcuts in this code for "find one element" and "find all matching elements" on the page. |
| **DOM** | The browser's live version of the page that JavaScript can read and change. |
| **Event listener** | Code that waits for something to happen (a click, a key press, a mouse move) and then reacts. |
| **Event delegation** | Instead of one listener per button, a single listener on the whole page checks which button was clicked. Saucy does this for all cart buttons. |
| **Template literal** (`` `...${x}...` ``) | A string with blanks you can fill in, used to build the HTML for each card. |
| **`innerHTML`** | Replaces what's inside an element with new HTML. |
| **`localStorage`** | A small notebook in your browser. Saucy writes down whether you like dark mode. |
| **`requestAnimationFrame`** | Asks the browser to run code just before it draws the next frame, which keeps the cursor ring smooth. |
| **Web Animations API** (`.animate()`) | Lets JavaScript play animations directly. Used for the flying food and sprinkles. |
| **IIFE** `(() => { ... })()` | A function that runs itself straight away. It keeps all of Saucy's code in its own bubble so it doesn't clash with anything else. |
| **`'use strict'`** | Tells JavaScript to be stricter about mistakes, so bugs get caught earlier. |

---

## 🚀 How it's hosted

This repo uses **GitHub Pages**. Every time `index.html` is updated on the `main` branch, the live site at **https://shreya-anandhun.github.io/saucy/** refreshes on its own within a minute or two.

---

Made with HTML, CSS and JavaScript. No frameworks, no libraries, just one file. 🍔🥤🍩
