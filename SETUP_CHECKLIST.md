# Setup Checklist

Before you can use this project, follow these steps:

## ☑️ Initial Setup

- [ ] Clone repository
- [ ] Download DejaVu Sans font to `fonts/dejvu-fonts/DejaVuSans.ttf`

## ☑️ Home Assistant Setup

- [ ] Install BVG/VBB integration in Home Assistant
- [ ] Find your station ID at https://www.vbb.de/fahrinfo/
- [ ] Add BVG sensor to `configuration.yaml`:
  ```yaml
  sensor:
    - platform: bvg_vbb
      stop_id: "900120003"  # Your station ID
      name: "Your Station Name"
  ```
- [ ] Enable packages in `configuration.yaml`:
  ```yaml
  homeassistant:
    packages: !include_dir_named packages
  ```
- [ ] Copy `home-assistant/packages/bvg_templates.yaml` to HA `config/packages/`
- [ ] Restart Home Assistant
- [ ] Verify template sensors exist (Developer Tools > States)

## ☑️ ESPHome Configuration

- [ ] Edit `cyd-bvg.yaml` substitutions section (lines 24-27):
  - `station_name`: Display name (e.g., "S Karlshorst")
  - `station_sensor`: HA sensor name (e.g., "s_karlshorst_berlin")
  - `temperature_sensor`: HA temp sensor (e.g., "garten_thermometer_temperature")

- [ ] Edit `home-assistant/packages/bvg_templates.yaml`:
  - Replace all `sensor.s_karlshorst_berlin` with your BVG sensor
  - Update all `unique_id: s_karlshorst_*` with your station slug
  - Adjust direction filters if needed (line 13)

## ☑️ First Flash

- [ ] Connect CYD via USB
- [ ] Run: `esphome run cyd-bvg.yaml`
- [ ] ESPHome will ask for WiFi credentials (first time only)
- [ ] Wait for compilation and upload
- [ ] Check ESPHome logs for errors
- [ ] Verify display shows data

## ☑️ Testing

- [ ] Display shows station name
- [ ] Time and temperature display correctly
- [ ] Departures show up (wait up to 5 seconds)
- [ ] Line badges have correct colors
- [ ] Delays are shown correctly
- [ ] LED pulses red when delay > 5 min (if applicable)
- [ ] Ambient light sensor works (check in HA)

## 🎉 Done!

Your BVG departure display is ready to use!

For updates via WiFi:
```bash
esphome run cyd-bvg.yaml --device cyd-bvg.local
```
