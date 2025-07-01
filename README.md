# 🚀 Redirect to Checkout on Add to Cart – WooCommerce Plugin

This lightweight plugin for **WooCommerce** automatically redirects customers to the **checkout page** after clicking the "Add to Cart" button — completely skipping the cart page.

Perfect for single-product stores, fast-purchase workflows, or mobile-first UX optimization.

---

## ✨ Features

- ✅ Skip the cart and redirect directly to **checkout**
- 🛒 Works for **all products**
- 🔧 No changes to product URLs or templates
- ⚡ Uses native WooCommerce hooks (safe and update-friendly)
- 🧩 No settings required — just install and activate!

---

## 📦 Installation

### Option 1: Upload Plugin via WordPress
1. Download the plugin ZIP file.
2. Go to `Plugins → Add New` in your WordPress dashboard.
3. Click **Upload Plugin** and upload the ZIP.
4. Click **Install Now**, then **Activate**.

### Option 2: Manual Installation
1. Upload the `redirect-to-checkout` folder to `/wp-content/plugins/` via FTP.
2. Go to `Plugins → Installed Plugins` and activate it.

---

## 🔍 How It Works

This plugin hooks into WooCommerce’s `woocommerce_add_to_cart_redirect` filter and replaces the default cart redirect with the checkout page.

```php
add_filter('woocommerce_add_to_cart_redirect', 'custom_redirect_to_checkout');

function custom_redirect_to_checkout($url) {
    return wc_get_checkout_url();
}

add_filter('woocommerce_cart_redirect_after_error', 'custom_redirect_to_checkout');
