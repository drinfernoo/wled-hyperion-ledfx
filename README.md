# ha-wled-hyperion
A simple implementation of the "missing" features from the WLED integration for Home Assistant,
including overriding Hyperion for users of both.

Requires a light integrated by the WLED integration.

### Usage
 * Download all the `.yaml` files from this repository.
 * Place `hyperion.yaml` (for Hyperion support), `ledfx.yaml` (for LedFx support), and `wled.yaml` in your Home Assistant `/config` directory.
 * Copy the contents of `secrets.yaml` into your existing file (or the whole file if you don't already have them).
 * Update the paths in `secrets.yaml` to match your WLED instance.
 * Add the `package` lines from `configuration.yaml` into your existing file.
 * Restart Home Assistant.

### Lovelace
* Copy the contents of `lovelace.yaml` into a "Manual" Lovelace card, update the address for the "peek" bar, and save the card.