# Wetterblick

Weather web app (PWA) in the style of WetterOnline, built on the same public data sources:

| Feature | Source |
|---|---|
| Current weather, 48 h hourly, 14-day forecast | DWD ICON (+ ECMWF/GFS for later days) via Open-Meteo |
| Rain in the next 3 hours (15-min steps) | DWD ICON-D2 via Open-Meteo |
| Rain radar loop | RainViewer composite |
| Rain radar Germany | DWD GeoServer (Niederschlagsradar) |
| Weather warnings | DWD via Bright Sky |
| Pollen, air quality | CAMS Europe via Open-Meteo |
| Trail grip for MTB (Werksboden / Normal / Dry / Wet) | DWD station rain via Bright Sky + DWD ICON forecast and evaporation via Open-Meteo |
| Place search | Open-Meteo geocoding |

Standard location: Esslingen am Neckar.

No API keys, no account, no tracking. Favourites and the last forecast stay on the phone.

## Install on GitHub Pages
1. New repository → upload all files in this folder.
2. Settings → Pages → Deploy from branch `main`, folder `/ (root)`.
3. Open the `https://<user>.github.io/<repo>/` link on the phone → Share → *Add to Home Screen* (iPhone) or *Install app* (Android).

"Update app" and "Delete app data" are on the Pollen tab.
