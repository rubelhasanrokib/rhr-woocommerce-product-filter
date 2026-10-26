<div align="center">

# RHR WooCommerce Product Filter

### Free AJAX Product Filter for WooCommerce & Elementor: Search, Categories, Attributes, Price Slider and Mobile Drawer

[![Version](https://img.shields.io/badge/version-2.0.1-0b7dda.svg)](https://github.com/rubelhasanrokib/rhr-woocommerce-product-filter/releases)
[![WordPress](https://img.shields.io/badge/WordPress-6.0%2B-21759b.svg?logo=wordpress)](https://wordpress.org/)
[![WooCommerce](https://img.shields.io/badge/WooCommerce-6.0%2B-96588a.svg?logo=woocommerce)](https://woocommerce.com/)
[![Elementor](https://img.shields.io/badge/Elementor-Widget-92003b.svg?logo=elementor)](https://elementor.com/)
[![PHP](https://img.shields.io/badge/PHP-7.4%2B-777bb4.svg?logo=php)](https://www.php.net/)
[![License: GPL v2](https://img.shields.io/badge/License-GPLv2%2B-green.svg)](LICENSE)

**[⬇ Download the plugin ZIP (v2.0.1)](RHR-WooCommerce-Product-Filter-V2.0.1.zip)** · [Features](#features) · [Installation](#installation) · [Elementor setup](#elementor-pro-setup) · [FAQ](#faq) · [Changelog](CHANGELOG.md)

</div>

---

**RHR WooCommerce Product Filter** is a free, lightweight, responsive **WooCommerce product filter plugin** with **AJAX filtering**, **live product search**, **category, attribute, color swatch, price, stock, sale and rating filters**, and a smooth **mobile filter drawer**. Unlike many filter plugins, it **filters your real WooCommerce / Elementor Pro archive query**, so your existing *Archive Products* or *Loop Grid* widget refreshes in place. No second product grid and no layout breakage.

It ships with a **native Elementor widget**, a **shortcode**, and a **dashboard with one-click color palettes** so you can match any store design without writing CSS.

> Built and maintained by **[Rubel Hasan Rokib](https://rubelhasanrokib.com/)**, WooCommerce, Elementor and conversion tracking specialist. Free to use on unlimited sites.

---

## Features

### Filtering that works with your real shop query
- Filters the existing **WooCommerce shop / category archive** and the **Elementor Pro Archive Products / Loop Grid** widget
- **AJAX results**: only the product grid refreshes, with no full page reload (automatic fallback to reload if needed)
- **AJAX pagination and sorting** that keep the active filters
- Pagination is reset when filters change, so you never land on an empty `/page/2/`

### Filter types
- 🔍 **Live product search** with image, price and **SKU matching**, plus a "See all results" link
- 🗂 **Hierarchical product categories** with sub-category tree and "Show more"
- 🎨 **Any WooCommerce attribute** (Size, Color, Material…) as **chips, checkboxes or color swatches**
- 💰 **Dual-handle price range slider**, correct for **variable products** (uses the WooCommerce product lookup table)
- ✅ **In stock only** and 🏷 **On sale only** toggles
- ⭐ **Rating filter**
- **Active filter chips**, **Reset all** button and collapsible sections

### Mobile-first UX
- Smooth **off-canvas filter drawer** from the **right, left or bottom**
- **Filter button** placed above the product grid next to **Sort by**, or as a floating button
- **Tablets use the phone layout** (configurable breakpoint, default 1024px)
- "Show results" button inside the drawer
- No flash or auto-open on page load: CSS loads in `<head>` and the drawer stays hidden until tapped

### Design and control
- **Native Elementor widget "RHR Product Filter"** with a full Style tab (colors, typography, spacing)
- **One-click color palettes** plus 13 editable color controls with **live preview**
- **Every label editable**, so you can translate the filter into Bangla, Arabic, Spanish or any language
- Reset to defaults at any time; settings are kept on update
- **WooCommerce HPOS compatible** (High-Performance Order Storage)

---

## Requirements

| Requirement | Version |
|---|---|
| WordPress | 6.0 or higher |
| WooCommerce | 6.0 or higher (tested up to 10.2) |
| PHP | 7.4 or higher |
| Elementor / Elementor Pro | Optional (widget tested up to Elementor 3.32) |

---

## Installation

### Upload the ZIP in WordPress
1. Download **[RHR-WooCommerce-Product-Filter-V2.0.1.zip](RHR-WooCommerce-Product-Filter-V2.0.1.zip)**.
2. In WordPress go to **Plugins → Add New → Upload Plugin**, choose the ZIP and click **Install Now**.
3. Click **Activate**. If an older version is installed, WordPress replaces it and your settings are kept.

> ⚠️ Don't use GitHub's green **Code → Download ZIP** button for installing. Download the **RHR-WooCommerce-Product-Filter-V2.0.1.zip** file from this repository instead and upload it in WordPress.

---

## Configuration

Open **RHR Filter** in the WordPress admin menu to:
- Pick a **color palette** or set each color manually (with live preview)
- Turn individual filters on or off (search, categories, attributes, price, stock, sale, rating)
- Choose how attributes display (chips, checkboxes, color swatches)
- Set the **mobile drawer side**, **mobile/tablet breakpoint** and button style
- Rename every label for your language
- Enable **auto display on shop pages**

---

## Elementor Pro setup

1. Go to **Templates → Theme Builder → Product Archive** and create or edit your archive template.
2. Build two containers: a **sidebar container** and a **main container**.
3. Drag the **RHR Product Filter** widget into the sidebar container.
4. Drag **Archive Products** (or **Loop Grid**) into the main container.
5. Style the filter from the widget's **Style** tab, then publish.

On tablet and mobile, the sidebar becomes a **Filter** button next to *Sort by* that opens the drawer.

## Shortcode

Use the filter anywhere (classic themes, Gutenberg, page builders):

```text
[rhr_product_filter]
```

---

## FAQ

**Does it work without Elementor?**
Yes. Use the `[rhr_product_filter]` shortcode or enable **Auto display on shop pages** in the settings. It works on standard WooCommerce shop and category pages.

**Does it create a second product grid?**
No. It modifies the main WooCommerce archive query, so your theme's or Elementor's existing product grid is filtered.

**Is the price filter accurate for variable products?**
Yes. It uses the WooCommerce product lookup table, so variation prices are matched correctly.

**Can I translate it into my language?**
Yes. Every frontend label (Search, Categories, Price, Reset all, Show results…) is editable in the dashboard.

**Is it really free?**
Yes. It's released under GPLv2 or later. Use it on personal and client sites, modify it, and share it.

**Will updating delete my settings?**
No. Uploading a newer ZIP replaces the plugin files and keeps your settings.

---

## Plugin file structure (inside the ZIP)

```
rhr-woocommerce-product-filter/
├── rhr-woocommerce-product-filter.php   # Main plugin file
├── uninstall.php                        # Cleans options on uninstall
├── readme.txt                           # WordPress.org style readme
├── includes/
│   ├── class-rhr-wpf.php                # Core: settings, assets, shortcode, AJAX
│   ├── class-rhr-wpf-query.php          # Archive query filtering (tax, price, stock, rating)
│   ├── class-rhr-wpf-render.php         # Filter HTML output
│   ├── class-rhr-wpf-admin.php          # Dashboard settings page
│   ├── class-rhr-wpf-elementor.php      # Elementor integration
│   └── elementor/class-rhr-wpf-widget.php
└── assets/                              # Frontend & admin CSS/JS
```

---

## Contributing and support

Found a bug or have a feature idea? [Open an issue](../../issues). Pull requests are welcome.

If this plugin helps your store, please **⭐ star the repository**. It helps other WooCommerce store owners find it.

## Author

**Rubel Hasan Rokib**: Upwork Verified Expert in WooCommerce, Elementor, Meta Pixel / Conversion API, GA4, GTM and server-side tracking.
🌐 [rubelhasanrokib.com](https://rubelhasanrokib.com/)

## License

[GPLv2 or later](LICENSE). Copyright © Rubel Hasan Rokib.

<sub>Keywords: WooCommerce product filter, AJAX product filter, Elementor product filter, WooCommerce filter plugin free, WooCommerce attribute filter, color swatch filter, price range slider WooCommerce, mobile filter drawer, Elementor Pro archive filter, WooCommerce live search, product category filter, WordPress shop filter.</sub>
