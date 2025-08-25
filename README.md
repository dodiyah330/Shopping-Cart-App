# React Shopping Cart with Free Gift Feature

## Objective
This is a simple React application that allows users to:

- Browse a list of products.
- Add products to a shopping cart.
- Update quantities or remove products from the cart.
- Track progress toward earning a free gift when the cart subtotal reaches a defined threshold.

The application also automatically adds a free gift once the threshold is reached and removes it if the cart total falls below the threshold.

## Features

### Display Products
- Renders a list of products from the `PRODUCTS` constant.
- Each product includes:
  - Quantity selector (`+` and `-` buttons).
  - "Add to Cart" button.

### Shopping Cart
- Displays all added products with quantities and subtotal.
- Users can:
  - Update product quantities directly in the cart.
  - Remove products from the cart.
- Free gift is automatically added or removed based on cart subtotal.

### Free Gift Rule
- Threshold: `THRESHOLD = 1000`.
- Free gift: `FREE_GIFT = { id: 99, name: "Wireless Mouse", price: 0 }`.
- Progress bar shows how much more needs to be added to unlock the free gift.
- Only one free gift is added automatically.
- Free gift cannot be removed manually.

### State Management
- Uses React’s built-in `useState` and `useEffect`.
- Maintains separate states for products and cart.

### User Experience
- Smooth interactions for adding/removing items.
- Message displayed when the free gift is applied.
- Mobile responsive design following the provided UI.

## Data Constants
```javascript
const PRODUCTS = [
  { id: 1, name: "Laptop", price: 500 },
  { id: 2, name: "Smartphone", price: 300 },
  { id: 3, name: "Headphones", price: 100 },
  { id: 4, name: "Smartwatch", price: 150 },
];

const FREE_GIFT = { id: 99, name: "Wireless Mouse", price: 0 };
const THRESHOLD = 1000;
