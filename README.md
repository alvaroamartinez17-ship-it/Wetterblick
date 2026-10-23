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
| Learn drying times from your own rides (ride file → rain history per place) | Open-Meteo historical DWD ICON forecasts, ERA5 before mid-2022 |
| Place search | Open-Meteo geocoding |

Standard location: Esslingen am Neckar.

No API keys, no account, no tracking. Favourites and the last forecast stay on the phone.

## Install on GitHub Pages
1. New repository → upload all files in this folder.
2. Settings → Pages → Deploy from branch `main`, folder `/ (root)`.
3. Open the `https://<user>.github.io/<repo>/` link on the phone → Share → *Add to Home Screen* (iPhone) or *Install app* (Android).

"Update app" and "Delete app data" are on the Pollen tab.

## Ride file for "Learn from my rides" (Trails tab)
CSV with one ride per row. Any of these work:

```
date,time,lat,lon
03.05.2024,16:40,48.7406,9.3108
```
```
date;place
2024-05-03;Esslingen am Neckar
2024-05-11;Bad Wildbad
```
or Strava's `activities.csv` from the account archive (only mountain bike rides are used; rides without a place count for the place shown at the top).

## Trail drying times (fitted)
Standard values come from 179 home-trail rides (Kappelberg, Korb, Schorndorf; March 2024 – September 2026) checked against hourly DWD ICON rain:
spring/summer (April–September) 1.75 days, fall/winter (October–March) 4.5 days after a heavy rain (12 mm or more), scaled by the day's actual evaporation.
