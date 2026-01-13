# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-01-XX

### 🎉 Initial Release

#### Added
- Real-time BVG/VBB departure display
- Support for ESP32-3248S035C (CYD) hardware
- LVGL-based UI with 5 departure lines
- Smart filtering for S-Bahn (westbound/eastbound) and Tram/Bus
- Red pulsing LED for delays > 5 minutes
- LDR sensor for ambient light detection
- Color-coded line badges (official BVG colors)
- Cancellation warnings ("ENTFÄLLT")
- Delay information integrated with departure times
- Home Assistant integration via template sensors
- DejaVu Sans font with German umlauts support
- Easy configuration via substitutions

#### Hardware Support
- ESP32-3248S035C (Cheap Yellow Display)
- 3.5" IPS display (480x320)
- Built-in RGB LED
- Built-in LDR sensor

#### Documentation
- Complete README with setup instructions
- SETUP_CHECKLIST for step-by-step configuration
- Troubleshooting guide
- Example configurations

### Credits
- Based on [ESP32-CYD-ESPHome](https://github.com/makeitworktech/ESP32-CYD-ESPHome) by @makeitworktech
- Uses [BVG/VBB HA Integration](https://github.com/manoth-msft/home-assistant-bvg-vbb-departures) by @manoth-msft

---

## [Unreleased]

### Planned Features
- Touch screen support for station switching
- Multiple station views
- Configurable layouts (vertical, compact)
- Transport type icons
- Night mode
- More than 5 departures

### Known Issues
- None reported yet

---

[1.0.0]: https://github.com/tom71/esphome-cyd-bvg-departure-display/releases/tag/v1.0.0
