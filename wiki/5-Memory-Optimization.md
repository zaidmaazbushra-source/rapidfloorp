# 5. Memory Optimization

## The RAM Problem

Floorp, like Firefox, can grow in memory usage over long sessions. Here’s a tiered approach:

---

## 🟥 4 GB RAM

**Goal: Keep Floorp under 600 MB baseline.**

1. Use **Minimal Memory** performance mode (Settings → Performance)
2. Set `dom.ipc.processCount` → `2`
3. Disable disk cache: `browser.cache.disk.enable` → `false`
4. Limit memory cache: `browser.cache.memory.capacity` → `32768` (32 MB)
5. Enable tab unloading: `browser.tabs.unloadOnLowMemory` → `true`
6. Disable Floorp sidebar if unused: `floorp.browser.sidebar.enable` → `false`
7. Use [Auto Tab Discard](https://addons.mozilla.org/en-US/firefox/addon/auto-tab-discard/) extension

---

## 🟡 8 GB RAM

**Goal: Balance speed and memory, stay under 1.5 GB with 10+ tabs.**

1. Use **Balanced** performance mode
2. Set `dom.ipc.processCount` → `4–8`
3. Enable disk cache: `browser.cache.disk.capacity` → `1000000` (1 GB)
4. Memory cache: `browser.cache.memory.capacity` → `131072` (128 MB)
5. Apply Fastfox user.js preset

---

## 🟢 16 GB+ RAM

**Goal: Maximum performance, let Floorp use what it needs.**

1. Use **Best Performance** mode
2. Set `dom.ipc.processCount` → `16` (or leave at default)
3. Enable large disk cache: `browser.cache.disk.capacity` → `2000000` (2 GB)
4. Memory cache: `browser.cache.memory.capacity` → `524288` (512 MB)
5. Apply Fastfox user.js preset

---

## Manual Memory Free

At any time, open the browser console (Shift+F2 or DevTools) and run:

```
window.QueryInterface(Ci.nsIInterfaceRequestor).getInterface(Ci.nsIDOMWindowUtils).garbageCollect();
```

Or simply navigate to a new tab and back — Floorp’s GC will release unused memory.
