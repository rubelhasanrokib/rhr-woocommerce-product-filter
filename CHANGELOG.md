# Changelog

All notable changes to **RHR WooCommerce Product Filter**.

## [2.0.1]
- **New:** Tablets use the phone layout (Filter button + drawer), on by default, tablet breakpoint 1024px.
- Elementor editor: the Filter button only shows in tablet/mobile preview, not on desktop.

## [2.0.0]
- **Fix:** Mobile filter panel no longer slides in from the left and disappears on category pages (CSS loads in `<head>`, drawer hidden until tapped, transitions enabled after first paint, removed 5-second DOM polling).
- **Fix:** Search bar works: no page reload on every keystroke, suggestions no longer blocked by cached nonces, Enter / arrow button applies the search, SKU search added.
- **Fix:** Standalone shortcode grid used wrong field names (search/categories/price never applied).
- **Fix:** Price filter now correct for variable products (uses WooCommerce lookup table).
- **Fix:** Filtering from `/page/2/` no longer lands on an empty page (pagination reset).
- **Fix:** "Auto display on shop pages" setting now works.
- **Fix:** Mobile breakpoint setting is now used by the CSS too.
- **New:** AJAX archive results, AJAX pagination and sorting, Elementor widget, attributes and color swatches, category tree, active chips, rating radios, drawer side option (right / left / bottom), floating button option, one-click palettes, 13 color controls, live preview, reset to defaults, all labels editable.

## [1.7.3]
- Mobile Filter button mounted outside Elementor containers.
