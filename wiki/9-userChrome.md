# 9. Compact userChrome.css Theme

This theme makes Floorp’s UI more compact and minimal, similar to the compact theme available for Zen Browser.

## Installation

1. Go to `about:config`
2. Set `toolkit.legacyUserProfileCustomizations.stylesheets` → `true`
3. Go to `about:support`, open your Profile Directory
4. Create a `chrome/` folder if it doesn’t exist
5. Copy [`userChrome.css`](https://github.com/zaidmaazbushra-source/rapidfloorp/blob/main/userChrome.css) into the `chrome/` folder
6. Restart Floorp

> **Tip:** Floorp may already have a `chrome/` folder and a `userChrome.css`. If so, append the contents rather than replacing the file.

## What It Does

- Compact tab height (28px)
- Compact toolbar and URL bar padding
- Hides tab close button unless hovered
- Cleaner bookmarks bar
- Compact audio indicator icons
- Removes clip-path from browser area for better compatibility
- Compact Floorp workspace label

## Customizing

Feel free to edit any values. The most common adjustments:

```css
/* Change tab height */
:root { --tab-min-height: 32px !important; }  /* increase if tabs feel too small */

/* Show close button always */
.tabbrowser-tab:not(:hover) .tab-close-button { display: flex !important; }
```
