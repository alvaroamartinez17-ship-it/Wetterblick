# Wetterblick

Weather web app (PWA) in the style of WetterOnline, built on the same public data sources:

| Feature | Source |
|---|---|
| Current weather, 48 h hourly, 10-day forecast | DWD ICON (+ ECMWF/GFS for later days) via Open-Meteo |
| Rain in the next 3 hours (15-min steps) | DWD ICON-D2 via Open-Meteo |
| Rain radar replay: last 4 h + 2 h forecast | DWD GeoServer (Niederschlagsradar, Radar_wn-product nowcast) |
| Rain at your place, last 4 h + next 2 h | DWD radar values via Bright Sky |
| Rain radar outside Germany | RainViewer composite |
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

## Trail drying times (fitted)
Standard values come from 179 home-trail rides (Kappelberg, Korb, Schorndorf; March 2024 – September 2026) checked against hourly DWD ICON rain:
spring/summer (April–September) 1.75 days, fall/winter (October–March) 4.5 days after a heavy rain (12 mm or more), scaled by the day's actual evaporation.

## Trail states and ride ratings
Trails show four states: Wet · Werksboden · Normal · Dry (plus storm warnings).
After a ride, rate the trails in Trails → Rate your ride. Ratings stay on the phone; "Copy ratings for Claude" copies them (with what the app predicted and the rain/wind behind it) to paste into the chat for tuning.
