# Should I Go Out? — mobile weather prototype

A functional + interface prototype of a mobile weather page, built for a design course
assignment. It pulls **live** weather data (no mocks) and answers four questions:

1. **What's the temperature right now?**
2. **Do I need a raincoat or umbrella in the next few hours?**
3. **When's the best hour to actually be outside today?** — every daylight hour is scored
   0–100 on feels-like temperature, UV index, and rain chance.
4. **How should I dress if I'm out all day?** — pick when you're heading home and it reports
   the coldest it will feel between now and then.

## Running it

No build step, no dependencies, no API keys. It's one self-contained `index.html`.

```sh
python3 -m http.server 8000
# then open http://localhost:8000
```

Serve it over `http://localhost` or HTTPS rather than opening the file directly —
`navigator.geolocation` is blocked on `file://` origins. If location access is unavailable
the page falls back to city search, so it still works either way.

## Data

- [Open-Meteo Forecast API](https://open-meteo.com/) — current conditions, hourly
  temperature / feels-like / precipitation probability / UV, daily sunrise & sunset
- [Open-Meteo Geocoding API](https://open-meteo.com/en/docs/geocoding-api) — city search
- [BigDataCloud](https://www.bigdatacloud.com/) — reverse geocoding for the location label

All are keyless and CORS-enabled, which is what lets a purely static page call them directly.
