# 3. user.js Presets (Betterfox / Fastfox)

A `user.js` file applies `about:config` preferences automatically on startup. It overrides defaults without permanently changing `prefs.js`.

## Option A: Use Floorp’s Built-in Installer (Recommended)

Floorp has a one-click user.js installer in its Settings. Use **Yokoffing Fastfox** for performance.

## Option B: Manual Betterfox Install

1. Download [Betterfox user.js](https://github.com/yokoffing/Betterfox)
2. Choose one profile:
   - `Fastfox` — maximum performance
   - `Securefox` — privacy focus
   - `Peskyfox` — annoyance removal
   - `Smoothfox` — smooth scrolling focus
3. Place the file as `user.js` in your profile folder
4. Restart Floorp

## Key Fastfox Entries

```js
user_pref("nglayout.initialpaint.delay", 0);
user_pref("nglayout.initialpaint.delay_in_oopif", 0);
user_pref("content.notify.interval", 100000);
user_pref("browser.startup.preXulSkeletonUI", false);
user_pref("layout.css.grid-template-masonry-value.enabled", true);
user_pref("dom.enable_web_task_scheduling", true);
```

## RAM-Targeted Presets

| RAM | Recommended | Notes |
|---|---|---|
| 4 GB | Fastfox + Minimal Memory mode | Lower `dom.ipc.processCount` to 2–4 |
| 8 GB | Fastfox + Balanced mode | Default `dom.ipc.processCount` (8) is fine |
| 16 GB+ | Fastfox + Best Performance | Increase process count, enable disk cache |
