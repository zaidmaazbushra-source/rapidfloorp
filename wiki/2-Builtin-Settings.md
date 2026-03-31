# 2. Floorp Built-in Performance Settings

Floorp ships with a unique **Performance Mode** feature in its Settings. This is the fastest way to improve performance without touching `about:config`.

## Step 1: Apply a Performance Preset

1. Open `⚙️ Menu → Settings`
2. Search for **Performance** or navigate to `Advanced → Performance`
3. Choose one of these modes based on your RAM:

| Mode | Best For | Effect |
|---|---|---|
| **Best Performance** | 8GB+ RAM | Maximum speed, higher memory usage |
| **Balanced** | 4–8GB RAM | Good speed with moderate memory |
| **Minimal Memory** | 4GB or less | Lower speed, much less RAM |

## Step 2: Apply a user.js Preset

Floorp includes a built-in user.js installer:

1. In Settings, find the **user.js** section
2. Click **Apply Yokoffing Fastfox** for best performance
3. Floorp will restart automatically

Fastfox is a well-tested set of `about:config` tweaks maintained by [@yokoffing](https://github.com/yokoffing/Betterfox) that improves responsiveness and page load speed.

## Step 3: Vertical Tabs

Floorp’s vertical tab sidebar can slightly affect rendering if you’re not using it. If unused:

1. Go to Settings → Tab & Toolbar
2. Disable **Vertical Tabs** if you don’t use the sidebar tab layout

## Step 4: Disable Floorp Sidebar 2 (if unused)

Floorp’s second sidebar (web panels, etc.) uses extra processes. Disable via `about:config`:

```
floorp.browser.sidebar.enable → false
```
