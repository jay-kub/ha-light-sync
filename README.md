# ha-light-sync
A blueprint for Home Assistant to sync the state and brightness of one light to another light(s)

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fjay-kub%2Fha-light-sync%2Fblob%2Fmain%2Fha-light-sync.yaml)

The following recommended settings will help make the transitions more fluid:

  - Transitions from on to off should be set to 0 for all devices
  - Initial On Level should match for all devices
  - The device settings for the Control Light should not have a minimum brigtness
  - Slow down the dimming speed on the Control Light to account for lag

Please note, the Control Light brightness must be able to scale between 1-100. When Minimum Brightness is > 1, the script will ensure the Target Light never falls below that value, with an adjusted linear scale between the minimum value and 100%. Because of this, the brightness value for each light will appear different.
