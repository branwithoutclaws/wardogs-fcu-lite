# WARDOGS FCU-LITE

Ultra-lightweight, zero-dependency second-screen ballistics computer and coordinate rangefinder designed for *WARDOGS* armor and artillery crews.

---

## Capabilities

- **Direct Sight Solutions**: Calculates Euclidean target range, azimuth bearing ($000^{\circ} - 360^{\circ}$), and gun sight elevation dial based on in-game Cartesian map coordinates ($X, Y, Z$).
- **Multi-Ordnance Presets**: Pre-configured ballistics curves for:
  - **Direct MBT (APFSDS)** (Velocity: 1,650 m/s)
  - **SPH-2 Howitzer (HE)** (High-angle indirect trajectory)
  - **L81 Mortar (81mm)** (Close-support indirect mortar table)
- **Modal Vector Radar**: Dedicated tactical scope popup displaying concentric range rings ($250\text{ m} - 2000\text{ m}$) with tap-to-plot target positioning.
- **Hardware-Friendly HUD**: True OLED black background (`#000000`), touch-optimized 4×4 tactile numpad with backspace (`⌫`), and Screen Wake Lock toggle (`AWAKE: ON/OFF`).
- **100% Offline PWA**: Zero remote assets or telemetry; fully cached locally via service worker.

---

## Repository Structure

```text
wardogs-fcu-lite/
├── index.html          # Main application (HUD, numpad, vector canvas, engine)
├── manifest.json       # Web App Manifest for mobile installation & APK packaging
├── sw.js               # Service Worker for local offline caching
├── README.md           # Documentation & instructions
└── icons/
    ├── icon-192.png    # Mobile home screen launcher icon
    └── icon-512.png    # Splash screen & store package icon
```

---

## Deployment & APK Generation

### Option 1: Instant PWA Sideload (Browser)
1. Enable **GitHub Pages** under **Settings** → **Pages** (Source: Deploy from branch `main`, root `/`).
2. Navigate to your Pages URL on your Android phone using Google Chrome.
3. Tap Chrome's menu (⋮) → **Add to Home screen** / **Install app**.

### Option 2: Build Standalone Android APK (PWABuilder)
1. Go to [PWABuilder.com](https://www.pwabuilder.com/).
2. Enter your live GitHub Pages URL (e.g., `https://branwithoutclaws.github.io/wardogs-fcu-lite/`).
3. Click **Package for Stores** → **Android** → **Generate Package (APK)**.
4. Download the generated `.apk` and install it onto your Android device.

---

## License

MIT License. Open-source for all *WARDOGS* combat crews.