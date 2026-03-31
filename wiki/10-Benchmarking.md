# 10. Benchmarking Your Results

## Recommended Benchmarks

| Benchmark | URL | What It Tests |
|---|---|---|
| Speedometer 3.1 | https://browserbench.org/Speedometer3.1/ | DOM performance, JS |
| MotionMark | https://browserbench.org/MotionMark/ | GPU rendering |
| JetStream 2 | https://browserbench.org/JetStream/ | JavaScript / WASM |
| Basemark Web 3.0 | https://web.basemark.com/ | Overall web perf |

---

## Workflow

1. **Before** — Run Speedometer 3.1 with factory Floorp settings. Write down your score.
2. **Apply** — Apply Floorp built-in Performance settings first (lowest risk).
3. **Retest** — Run Speedometer 3.1 again.
4. **Apply** — Add Fastfox user.js.
5. **Retest** — Note improvement.
6. **Apply** — Add `about:config` tweaks incrementally.
7. **Final** — Run the full suite.

---

## Tips for Clean Results

- Close all other applications
- Run each benchmark **3 times** and average the scores
- Disable extensions for pure browser performance (run in a new profile if needed)
- Run at the same time of day on the same network

---

## Sharing Results

If you’d like to share your before/after results, open a [Discussion](https://github.com/zaidmaazbushra-source/rapidfloorp/discussions) on this repo!
