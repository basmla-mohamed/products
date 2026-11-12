
<div align="center">
  <img src="./images/hero.svg" width="100%" alt="Products">
</div>

<br>

<div align="center">
  <img src="https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white">
  <img src="https://img.shields.io/badge/SCSS-CF649A?style=flat-square&logo=sass&logoColor=white">
  <img src="https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white">
</div>

<br>

<div align="center">
  A responsive product catalog with an interactive shopping cart, built with Angular.
</div>

<br>

<img src="./images/overview.svg" width="100%">

## Overview

Products is an Angular shopping cart application that displays electronic products and allows users to manage their cart through a simple interface.

The application keeps product quantities, total item count, and total price synchronized through Angular's reactive state features.

---

<img src="./images/features.svg" width="100%">

## Features

| Feature | Description |
|---|---|
| Product Catalog | Displays eight electronic products with images, descriptions, and prices. |
| Add to Cart | Increases the selected product quantity. |
| Remove from Cart | Resets the selected product quantity to zero. |
| Total Items | Calculates the combined quantity of all products. |
| Total Price | Calculates the cart total using each product's current price. |
| Reactive Interface | Updates displayed values when the products state changes. |
| Responsive Layout | Uses the Bootstrap grid to adapt to different screen sizes. |

---

<img src="./images/technology.svg" width="100%">

## Technology Stack

| Technology | Usage |
|---|---|
| Angular | Application framework and component architecture |
| TypeScript | Product model and application logic |
| Angular Signals | Reactive product state |
| Computed Signals | Derived cart totals |
| HTML | Component templates |
| SCSS | Styling and layout |
| Bootstrap | Grid system and responsive utilities |

---

<img src="./images/angular-concepts.svg" width="100%">

## Angular Concepts

- **signal()** — stores the products array as reactive state.
- **computed()** — derives the total item count and total price.
- **update()** — changes the products state immutably.
- **map()** — updates the product matching a given ID.
- **reduce()** — calculates the cart summaries.
- **@for** — renders the product collection.
- **@if** — conditionally displays the Remove from Cart button.
- **Event Binding** — connects button clicks to component methods.
- **Interpolation** — displays product data and calculated values.

---

<img src="./images/project-structure.svg" width="100%">

## Project Structure

```text
my-app-module/
├── public/
├── src/
│   ├── app/
│   │   ├── components/
│   │   │   ├── home/
│   │   │   ├── navbar/
│   │   │   └── products/
│   │   │       ├── products.component.ts
│   │   │       ├── products.component.html
│   │   │       └── products.component.scss
│   │   ├── app.html
│   │   ├── app.scss
│   │   └── app.ts
│   ├── index.html
│   ├── main.ts
│   └── styles.scss
├── angular.json
├── package.json
└── README.md
```

---

<img src="./images/installation.svg" width="100%">

## Installation

### 1. Clone the repository

```bash
git clone YOUR_REPOSITORY_URL
```

### 2. Navigate to the project directory

```bash
cd my-app-module
```

### 3. Install dependencies

```bash
npm install
```

### 4. Start the development server

```bash
ng serve
```

### 5. Open the application

```text
http://localhost:4200
```

---

## Cart Calculation

### Total Items

```typescript
totalItems = computed(() =>
  this.products().reduce((total, item) => total + item.quantity, 0)
);
```

### Total Price

```typescript
totalPrice = computed(() =>
  this.products().reduce(
    (total, item) => total + item.quantity * item.newPrice,
    0
  )
);
```

Both computed values recalculate automatically when the products signal changes.

<br>

<div align="center">
  <img src="./images/footer.svg" width="100%">
</div>
