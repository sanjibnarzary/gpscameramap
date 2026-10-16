# Narzary GPS Camera Map

A professional, high-performance Android GPS camera application engineered for field verification, engineering surveys, civil inspections, social welfare beneficiary audits, and geotagged documentation.

---

## 🌟 Key Features

### 1. High-Resolution Geotagged Photography & Video
- **Crisp High-Definition Output:** Captures photos and records videos in 4:3 Full HD (1440×1080) by default in landscape mode and 3:4 Full HD (1080×1440) in portrait mode, with support for 16:9 Full HD (1920×1080) up to 4K/8K.
- **Landscape Video Orientation Alignment:** In landscape mode, the left side of the camera view (where the live location HUD, mini-map, address info, and mode controls reside) is precisely mapped to the **bottom of the frame** in the recorded video, ensuring consistent orientation with the on-screen survey layout.
- **Synchronized Audio & Export:** Records hardware-encoded AAC audio synchronized with H.264 video at real-time normal speed (1.0x default, with selectable 0.5x, 1.5x, 2.0x speeds available in settings). Saved and exported videos include the mixed audio track.
- **In-Camera Audio & HUD Toggles (Above HUD on Right Side):** Dedicated interactive control buttons placed directly above the HUD card on the right side:
  - **Audio On/Off Toggle (Top):** Instant sound toggle (🔊 Audio ON / 🔇 Muted) to enable or disable microphone recording before and during video capture.
  - **HUD On/Off Toggle (Just Below Audio):** Instant toggle (🗺️ HUD ON / 🚫 HUD OFF) to enable or disable the minimap and location address overlay. When ON (default), minimap, address HUD, video, and audio are all recorded and saved together. When OFF, only clean video and audio (or clean photo) are saved without the HUD overlay.
- **Camera Controls & Zoom:** Supports pinch-to-zoom hand gestures on the viewfinder and preset zoom pills (`0.5`, `1x`, `2`) floating cleanly at the top of the camera view, fully responsive during both preview and active recording.
- **Settings-Gated Video Feature:** Video recording is disabled by default in settings. When disabled, the video mode button and controls are completely hidden from the viewfinder.
- **Smooth Live HUD Video Recording:** Live location mini-map, reverse-geocoded address, digital compass, GPS coordinates, and real-time telemetry are stamped dynamically onto every video frame at 25–30 FPS.
- **Long-Duration Memory-Bounded Recording:** Zero heap allocation per frame, high-performance NV12 hardware encoding, and native buffer reuse allow continuous video recording for as long as needed without memory leaks or OOM crashes.
- **Non-Intrusive Photo Capture Flow:** Capturing a photo saves it immediately with full geotags without force-opening the viewer, keeping the camera ready for continuous survey documentation.
- **Interactive Full-Screen Photo Viewer:** Dedicated Photo Detail screen allows tapping the photo area to open a full-screen viewer with pinch-to-zoom, double-tap zoom, smooth panning across all areas, and floating zoom controls.

### 2. Global Pro Upgrade, Factory Reset & Sister Projects
- **Automatic Regional Pricing Detection:** Automatically detects country location (India: **₹499 / 499 Rupees**; Outside India: **USD $4.99**) and displays only the relevant pricing without requiring manual country selection. Permanently unlocks the Watermark Copyright toggle and custom watermark text.
- **Reset All Settings to Default:** One-tap restore to reset all camera, video speed, HUD, and watermark preferences back to initial defaults with a safe confirmation dialog.
- **Developer Social Links:** Direct social links to connect with developer Dr. Sanjib Narzary on [𝕏 (x.com/SanjibNarzary)](https://x.com/SanjibNarzary) and [Facebook (facebook.com/SanjibNarzary)](https://facebook.com/SanjibNarzary).
- **Featured Sister Projects:** Integrated links in Settings to:
  - **Echo Search:** [https://echo.narzary.com](https://echo.narzary.com) — Fast, privacy-centric AI search engine.
  - **Alayaran News:** [https://www.alayaran.com](https://www.alayaran.com) — Digital news & media portal.
  - **SeekGPT:** [https://www.seekgpt.org](https://www.seekgpt.org) — Next-gen AI research platform with social channels on [𝕏 (x.com/seekgpt)](https://x.com/seekgpt), [Facebook (facebook.com/seekgpt)](https://facebook.com/seekgpt), and [LinkedIn (linkedin.com/company/seekgpt)](https://linkedin.com/company/seekgpt).

### 3. Live Mini-Map & Google Maps API Integration
- **Real-Time Mini-Map:** Real Google Maps static vector/satellite/hybrid rendering embedded directly in the camera viewfinder, stamped onto photos, and rendered frame-by-frame onto exported videos.
- **Protected Default Maps API Key:** The built-in Google Maps API key is fully protected and hidden (`●●●●●●`). Users can supply their own custom Google Maps API key via Settings without revealing the default system key.
- **Offline Map Cache:** Automatic offline tile caching ensures uninterrupted mapping even in remote areas without cellular reception.

### 4. Adaptive Landscape & Portrait Camera Viewfinder
- **Smart Landscape Mode Architecture:** In landscape orientation, the mini-map, address info, telemetry, and photo/video mode switcher are neatly organized on the **LEFT** side; the shutter button, lens toggle, and gallery thumbnail are ergonomically centered at the **BOTTOM**; and the custom survey note badge is pinned to the **RIGHT EDGE** for unobstructed camera framing.
- **Physical Orientation Sensing:** Hardware accelerometer/gyroscope integration smoothly detects device orientation changes (0°, 90°, 180°, 270°) and animates control icons in place.

### 5. Telemetry & Streamlined Address Plus Code
- **Streamlined HUD:** Google Plus Codes are automatically incorporated into the reverse-geocoded address line, eliminating redundant separate Plus Code badges from the HUD overlay card.
- **Comprehensive Geolocation Data:** Latitude, Longitude (DMS or Decimal), Altitude, Accuracy, Speed, Street Name, District, and State.
- **Digital Compass Display:** 360° rotating azimuth compass showing live cardinal heading.
- **Department Emblems & Custom Badges:** Pre-configured with government and institutional department insignias (Social Welfare, Revenue, Engineering, Forest & Environment, Police) with custom logo upload support.

### 6. Gallery & Universal Multi-Media Sharing
- **Multi-Selection Photo & Video Sharing:** Seamlessly share multiple photos, videos, or mixed media to any installed app (WhatsApp, Telegram, Google Photos, Gmail, Drive, Messages).
- **Universal ClipData & Security Propagation:** Automatically provisions `ClipData` containing all media URIs with `FLAG_GRANT_READ_URI_PERMISSION` across Chooser activities and grants explicit URI read access to all recipient apps.

### 7. Dual Gallery Storage & Cloud Sync
- **Dual Gallery Storage:** Captured photos and videos are stored in Room SQLite database and automatically mirrored to the device's public `Pictures/NarzaryGPSMapCamera` and `Movies/NarzaryGPSMapCamera` directories.
- **Auto Cloud Sync:** Background synchronization queue for enterprise data consolidation.

---

## 📜 Legal & Compliance

- **[LICENSE](LICENSE):** Open-source under the Apache License 2.0.
- **[Terms of Service](TERMS_OF_SERVICE.md):** Complete terms including zero ads guarantee, voluntary Pro Upgrade pricing ($4.99 USD international / ₹499 India), local device storage, sensor accuracy disclaimer, and user privacy.

---

## ⚙️ Configuration & Settings

| Setting | Options / Defaults | Description |
|---|---|---|
| **Google Maps API Key** | Protected Default / User Custom | Override with personal Maps API key; default key remains masked. |
| **Razorpay API Key** | Default Test / User Custom | Key ID for processing donations via UPI and Indian cards. |
| **Map Style** | `HYBRID`, `SATELLITE`, `ROADMAP`, `TERRAIN` | Switch visual satellite/vector map basemaps. |
| **Video Framerate** | `25 FPS`, `30 FPS`, `60 FPS` | Ensures smooth, cinematic inspection video recording. |
| **Coordinate Format** | `DMS` (Degrees/Minutes/Seconds), `DECIMAL` | Format for displayed and stamped coordinates. |
| **Copyright Watermark** | Always Enabled (Locked) | Tamper-proof watermark protection for official surveys. |

---

## 🛠️ Tech Stack & Architecture

- **Language:** Kotlin 100%
- **UI Framework:** Jetpack Compose (Material Design 3)
- **Camera Pipeline:** CameraX (Preview, ImageCapture, VideoCapture, Recorder)
- **Payment Gateway:** Razorpay Android SDK & REST API (UPI Intent, GPay, PhonePe, Paytm, BHIM, Cards, NetBanking)
- **Local Persistence:** Room Database + SharedPreferences
- **Graphics Pipeline:** Hardware Canvas, Bitmap Stamping, AndroidX ExifInterface
- **Mapping:** Google Maps Android SDK + Google Maps Static API + Offline Tile Cache

---

## 📱 Permissions

- `CAMERA`: Viewfinder and optical sensor capture.
- `ACCESS_FINE_LOCATION` & `ACCESS_COARSE_LOCATION`: High-precision GPS coordinates.
- `RECORD_AUDIO`: Audio recording for video inspections.
- `INTERNET` & `ACCESS_NETWORK_STATE`: Map tiles, cloud sync, and Razorpay UPI checkout.
- `POST_NOTIFICATIONS`: Video export and background processing notifications.
