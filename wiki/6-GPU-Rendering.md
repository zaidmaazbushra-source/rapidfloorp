# 6. GPU & Rendering

## Enable WebRender (GPU Compositing)

WebRender offloads page compositing to the GPU. Verify it’s active at `about:support` → look for **WebRender** in the Graphics section.

```
gfx.webrender.enabled → true
gfx.webrender.all → true
```

> **Note:** On some older GPUs, WebRender may cause glitches. If that happens, set `gfx.webrender.enabled` back to `false`.

---

## Hardware Acceleration

Ensure hardware acceleration is on:

1. Settings → General → Performance
2. Check **Use hardware acceleration when available**

Or via `about:config`:

```
layers.acceleration.force-enabled → true
```

---

## GPU Process

```
gfx.webrender.compositor → true
gfx.webrender.compositor.force-enabled → true
```

Check that a **GPU Process** is listed at `about:processes`.

---

## Smooth Scrolling

For buttery scroll on high-refresh monitors:

```
apz.frame_delay.enabled → false
general.smoothScroll → true
general.smoothScroll.msdPhysics.enabled → false
mousewheel.default.delta_multiplier_y → 140
```

> Setting `msdPhysics.enabled` to `false` gives a snappier, Chrome-like scroll feel.

---

## Display Refresh Rate

If you have a 120Hz+ monitor:

```
layout.frame_rate → 120  (or 144, 165, 240)
```

This allows Floorp to render at your display’s native rate instead of capping at 60 Hz.
