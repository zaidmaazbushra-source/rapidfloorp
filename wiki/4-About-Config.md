# 4. about:config Tweaks

Open `about:config` in Floorp and search for each key. Apply tweaks appropriate for your system.

---

## 🚀 Performance & Responsiveness

| Preference | Value | Notes |
|---|---|---|
| `nglayout.initialpaint.delay` | `0` | Paint page immediately |
| `nglayout.initialpaint.delay_in_oopif` | `0` | Same for iframes |
| `content.notify.interval` | `100000` | Faster reflow notifications |
| `dom.enable_web_task_scheduling` | `true` | Better task prioritization |
| `browser.startup.preXulSkeletonUI` | `false` | Skip skeleton UI on startup |
| `toolkit.cosmeticAnimations.enabled` | `false` | Disable fullscreen/minimize animations |

---

## 🧠 Memory Management

| Preference | Value | Notes |
|---|---|---|
| `dom.ipc.processCount` | `4` (4GB) / `8` (8GB) / `16` (16GB+) | Content process limit |
| `browser.tabs.unloadOnLowMemory` | `true` | Auto-unload background tabs on low RAM |
| `browser.low_memory_notification_interval_ms` | `10000` | Check memory every 10s |
| `javascript.options.mem.gc_incremental_slice_ms` | `10` | Smaller GC pauses |
| `javascript.options.mem.gc_high_frequency_time_limit_ms` | `1000` | Control GC frequency |

---

## 💾 Disk Cache

| Preference | Value (4GB) | Value (8GB+) | Notes |
|---|---|---|---|
| `browser.cache.disk.enable` | `false` | `true` | Disk cache |
| `browser.cache.disk.capacity` | `0` | `2000000` | Cache size in KB |
| `browser.cache.memory.enable` | `true` | `true` | Keep memory cache on |
| `browser.cache.memory.capacity` | `65536` | `262144` | Memory cache in KB |

---

## 🌐 Network

| Preference | Value | Notes |
|---|---|---|
| `network.http.max-connections` | `1800` | More parallel connections |
| `network.http.max-persistent-connections-per-server` | `10` | More per-server connections |
| `network.ssl_tokens_cache_capacity` | `32768` | Larger TLS session cache |
| `network.prefetch-next` | `false` | Disable link prefetching |
| `network.predictor.enabled` | `false` | Disable network predictor |
| `network.http.speculative-parallel-limit` | `0` | Disable speculative connections |

---

## 🎮 GPU & Rendering

See [GPU & Rendering](./6-GPU-Rendering.md) for the full list.

---

## 🔇 Floorp-Specific

| Preference | Value | Notes |
|---|---|---|
| `floorp.browser.sidebar.enable` | `false` | Disable Sidebar 2 if unused |
| `floorp.browser.sidebar2.enable` | `false` | Same for secondary sidebar |

---

> **Tip:** After editing `about:config`, you don’t need to restart for most changes. Some preferences (GPU, IPC counts) require a restart.
