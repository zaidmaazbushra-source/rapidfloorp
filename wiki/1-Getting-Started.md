# 1. Getting Started

## Prerequisites

- Download [Floorp Browser](https://floorp.app/) (latest stable)
- Know your system RAM: 4GB, 8GB, or 16GB (guide adapts to each)
- Have a baseline Speedometer 3.1 score before applying any changes

## Where to Apply Changes

| Method | How to Open |
|---|---|
| `about:config` | Type in address bar, press Enter, accept warning |
| `user.js` | Place in your Floorp profile folder (see below) |
| `userChrome.css` | Place in `chrome/` folder inside profile (see below) |
| Floorp Settings | `⚙️ Menu → Settings` |

## Finding Your Profile Folder

1. Type `about:support` in the address bar
2. Click **Open Directory** next to “Profile Directory”
3. This is where `user.js` and the `chrome/` folder go

## Enabling userChrome.css

1. Go to `about:config`
2. Search for `toolkit.legacyUserProfileCustomizations.stylesheets`
3. Set it to `true`
4. Create a `chrome/` folder in your profile if it doesn’t exist
5. Place `userChrome.css` inside it
6. Restart Floorp

> **Tip:** Floorp may already have a `chrome/` folder — check before creating one.
