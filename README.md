# Obsidian Roast — Volcanic Single-Origin Coffee

An ultra-luxury, high-performance scroll-driven narrative website built to showcase **Obsidian Roast**, a premium single-origin coffee cultivated in the mineral-rich volcanic ash of Mount Agung, Bali.

---

## Key Features

1. **Memory-Cached Video Preloader**:
   * Utilizes a custom Javascript `fetch` stream reader (`ReadableStream`) to download `coffee.mp4` fully in the background.
   * Displays an elegant gold loading progress percentage.
   * Converts the finished stream into an in-memory `Blob` object URL, preventing video buffering stutters and lag during high-speed scrubbing.

2. **GSAP Scroll-Scrubbing Engine**:
   * Uses GSAP and `ScrollTrigger` to bind the background video's playhead (`currentTime`) directly to the page scroll progress.
   * Configured with custom inertia (`scrub: 1.2`) for smooth frame transition seeking.

3. **Lenis Smooth Scroll**:
   * Integrates the **Lenis Smooth Scroll** library for inertial scrolling physics, making the scroll-driven animations feel exceptionally seamless.

4. **Atmospheric Lighting Shifts**:
   * Soft radial background glows (`#ambient-glow-roast` and `#ambient-glow-elixir`) trigger as you cross specific narrative milestones, shifting the atmosphere of the page dynamically from volcanic amber to roasted gold.

5. **Procedural Topographic Canvases**:
   * Product cards feature HTML5 `<canvas>` elements rendering topographic elevation lines.
   * Features dynamic hover interactions: when you hover over a card, the terrain waves ripple faster and glow with an ambient box-shadow matching the roast profile.

6. **Cinematic Text Overlays & Parallax**:
   * Individual section titles and copy slide up and fade in as they enter the screen, dwell in the center viewport, and fade away as the next chapter begins.
   * A floating side navigation dot system keeps track of current sections.

---

## File Structure

```bash
├── index.html       # Combined structure, custom Tailwind settings, styles, and animation logic
├── coffee.mp4       # Raw background video asset (45MB, 30s)
├── final.mp4        # Symbolic link pointing to coffee.mp4
└── README.md        # Documentation
```

---

## How to Run Locally

Since the preloader uses the `fetch` API to download the video, the file must be served over an HTTP server to avoid CORS issues.

1. **Start a local HTTP server**:
   If you have Node.js installed, you can launch a quick static server:
   ```bash
   npx -y http-server -p 3000
   ```
   Or if you prefer Python:
   ```bash
   python3 -m http.server 3000
   ```

2. **Open the browser**:
   Navigate to:
   👉 **[http://localhost:3000/index.html](http://localhost:3000/index.html)**
# coffee-cinematic-antigravity
