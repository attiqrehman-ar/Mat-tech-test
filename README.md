# Shopify Developer Test Task – Custom Product Page Template (Dawn Theme)

## Overview
This project customizes the Dawn theme to provide a unique product page experience, as per the test requirements. It features a split layout with synchronized product/image sliders, custom fonts, variant selection, AJAX add-to-cart, drawer cart updates, and automatic free shipping logic.

---

## Features

### 1. Theme Setup
- Based on a fresh copy of the latest Dawn theme.

### 2. Font Customization
- **Headings:** Uses "Dancing Script" font.
- **Body Text:** Uses "Oswald" font.
- Fonts are loaded via Google Fonts and applied in the theme's CSS.

### 3. Custom Product Page Template & Section
- **Template:** A new product template is created and assigned to products as needed.
- **Section:** Implements a split layout:
  - **Left:** Image carousel/slider (5 images, placeholder or product images).
  - **Right:** Product slider (5 dummy or real products), each with:
    - Product image, title, price
    - Color and Size variant dropdowns (3 options each)
    - Add to Cart button (requires variant selection)
- **Synchronized Sliders:** Hovering/selecting a product on the right updates the left image carousel.
- **AJAX Add to Cart:** Adds selected variant to cart without page reload and updates the cart drawer.

### 4. Free Shipping Logic
- **Automatic Free Shipping:**
  - Orders over $50 (5000 cents) show a congratulatory message.
  - Orders below $50 show how much more is needed for free shipping.
  - Message appears both after AJAX add-to-cart and on the cart page (in the footer).
  - Actual free shipping is handled by Shopify's shipping settings at checkout.

### 5. Responsiveness
- Fully responsive layout for desktop and mobile.

### 6. No Third-Party Apps
- All logic is implemented using Liquid, JavaScript, and CSS only.

---

## How to Use

1. **Fonts:**
   - Ensure the following Google Fonts are loaded in your theme (add to `theme.liquid` or main CSS):
     ```html
     <link href="https://fonts.googleapis.com/css?family=Dancing+Script:700&display=swap" rel="stylesheet">
     <link href="https://fonts.googleapis.com/css?family=Oswald:400,500,700&display=swap" rel="stylesheet">
     ```
   - In your CSS:
     ```css
     h1, h2, h3, h4, h5, h6 { font-family: 'Dancing Script', cursive; }
     body, p, span, div, a, li, input, select, button { font-family: 'Oswald', sans-serif; }
     ```

2. **Assign the Custom Product Template:**
   - In Shopify admin, go to Products > select a product > Theme template > choose your new custom template (e.g., `product.custom-split`).

3. **Dummy Data:**
   - The section uses either dummy products or a specific collection. Adjust as needed in the section code.

4. **Free Shipping:**
   - Set up a free shipping rate for orders over $50 in Shopify Admin > Settings > Shipping and delivery.
   - The theme displays a message, but the actual discount is applied at checkout by Shopify.

5. **Cart Drawer:**
   - AJAX add-to-cart automatically opens/updates the cart drawer.

---

## Files Modified or Added
- `sections/custom-product-split.liquid` (main custom section)
- `sections/main-cart-footer.liquid` (free shipping message in cart)
- CSS for font customization (see above)

---

## Notes
- No third-party apps or libraries are used.
- All code is clean, commented, and follows Shopify best practices.
- For any questions, refer to code comments or contact the developer.

---

**End of README**
