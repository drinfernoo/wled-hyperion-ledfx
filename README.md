# wled-hyperion-ledfx
A simple implementation of the "missing" features from the WLED integration for Home Assistant,
including overriding Hyperion and LedFx, for users of each.

## Requirements
You will need a light integrated by the WLED integration (`light.wled_tv` in these files).
This should work with segments or multiple lights, but the packages will need to be duplicated and updated for each light.

### For Hyperion support
You will need a light integrated by the Hyperion integration (`light.hyperion` in these files).
This currently works with a V4L (USB capture) device, but could possibly be updated to toggle between platform capture.

### For LedFx support
You will need an LedFx instance integrated by the LedFx ReMote integration. It can be found [here](https://github.com/YeonV/ledfxrm):, and installed via HACS.
Particularly for the Lovelace card, you'll need to make sure your LedFx entities are named as following:
 * LedFx Scene Selector -> `light.ledfx_scenes`
 * LedFx Server Status -> `binary_sensor.ledfx_status`
 * Number of Devices -> `sensor.ledfx_devices`
 * Number of Pixels -> `sensor.ledfx_pixels`
 * Number of Scenes -> `sensor.ledfx_scenes`
 * ⮑ wled -> `light.wled_ledfx`  <-- This one is for a "subdevice", and doesn't get used in these files anyways.

## Usage
 * Download all the `.yaml` files from this repository.
 * Place `hyperion.yaml` (for Hyperion support), `ledfx.yaml` (for LedFx support), and `wled.yaml` in your Home Assistant `/config` directory.
 * Copy the contents of `secrets.yaml` into your existing file (or the whole file if you don't already have them).
 * Update the paths in `secrets.yaml` to match your WLED instance.
 * Add the `package` lines from `configuration.yaml` into your existing file.
 * Restart Home Assistant.

### Lovelace
*  Copy the contents of `lovelace.yaml` into a "Manual" Lovelace card, update the address for the "peek" bar, and save the card.
