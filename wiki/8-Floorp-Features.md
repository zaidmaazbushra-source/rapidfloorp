# 8. Floorp-Specific Features

Floorp has unique features not found in vanilla Firefox. Here’s how to configure each for performance.

---

## Workspaces

Floorp’s Workspaces separate tabs into groups — great for keeping background tabs isolated.

- Use workspaces to confine heavy tabs (video, web apps) to separate groups
- Switching workspaces unloads inactive ones from active rendering

---

## Sidebar 2 (Web Panels)

The secondary sidebar (Sidebar 2) can host web pages as panels. Each panel is a separate process.

- **Tip:** Only enable panels you actively use
- Disable if unused: `floorp.browser.sidebar.enable → false`

---

## Progressive Web Apps (PWA)

Floorp supports installing PWAs. PWAs run in separate windows with reduced UI overhead, which can be faster than a full browser tab for certain apps (like Notion, Discord).

---

## Lepton Theme

Floorp’s default Lepton theme is clean and well-optimized. Avoid heavy custom themes as they can introduce CSS layout overhead.

---

## Vertical Tabs

Floorp’s built-in vertical tab sidebar is more efficient than extensions like Tree Style Tab (no extension overhead). Use the built-in if you want vertical tabs.

---

## Auto Tab Discard

Floorp can automatically discard inactive tabs. Configure via Settings → Tab → Tab Sleep / Tab Discard settings.

This is especially useful on 4–8 GB RAM systems.

---

## Firefox Sync

Floorp supports Firefox Sync. If you use Sync, it runs a background process. Disable it in Settings if you don’t need it to save a small amount of CPU/memory.
