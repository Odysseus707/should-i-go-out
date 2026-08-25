# Mobile Weather Prototype — Submission

**Vivek Rai** · vivekrai2949@gmail.com

---

## 1. Live webpage

**<https://odysseus707.github.io/should-i-go-out/>**

Source code: <https://github.com/Odysseus707/should-i-go-out>

Best viewed in a phone-width browser window. The page asks for location permission on first
load; if you decline, it falls back to city search and still works. It pulls live data from
the Open-Meteo API on every load — nothing on the page is mocked or hard-coded.

### The four needs it addresses

| # | Need | How the page answers it |
|---|------|------------------------|
| 1 | **Current temperature** | Large current reading with feels-like, condition, humidity, wind, and UV. |
| 2 | **Raincoat / umbrella for the next few hours?** | A yes / maybe / no verdict from the peak rain probability over the next 6 hours, with the hour rain is most likely and a bar for each hour. |
| 3 | **Best hour to be outside today** | Every remaining daylight hour is scored 0–100 on feels-like temperature, UV index, and rain chance. Shows the winning window, the three numbers behind it, and a scored bar per hour. Flips to "Go now" when the current hour is as good as the best. |
| 4 | **How to dress for a whole day out** | Pick when you're heading home (6 PM / 9 PM / 11 PM) and it reports the coldest it will *feel* between now and then, plus a layer recommendation. |

---

## 2. Writeup — the two needs I defined

> **Note to self before submitting:** rewrite this in your own words — it should be true of
> how you actually use a weather app.

Beyond temperature and rain, I added two needs of my own. The first is **knowing the single
best hour to be outside**: I'm indoors for most of the day and realistically get one window
to go for a walk or a run, so what I need isn't the whole forecast — it's a recommendation.
The page scores every daylight hour on feels-like temperature, UV index, and chance of rain
and just tells me when to go, which saves me from reading an hourly table and guessing.
The second is **dressing for a whole day out**: I leave in the morning and often don't get
home until late, and what it feels like when I walk out the door is a bad predictor of what
it'll feel like on the way back. So instead of showing today's high and low, the page asks
when I'm heading home and tells me the coldest it will feel *between now and then* — which
is the number that actually decides whether I carry a jacket.

---

## 3. Video walkthrough

**[ ▸ PASTE VIDEO LINK OR ATTACH FILE HERE ]**

<!--
  ~15 second screen recording, phone-width browser window.
  Record on macOS with Cmd+Shift+5, or QuickTime > File > New Screen Recording.
  If the file is too large to attach, upload it unlisted to Drive/YouTube and paste the link.

  Shot list — one beat per need:
    0:00-0:03  Page loads, glance at the current temperature (need 1)
    0:03-0:07  Scroll to the umbrella card, read the verdict and the 6-hour bars (need 2)
    0:07-0:11  Scroll to "Best time to be outside", scrub the hourly strip (need 3)
    0:11-0:15  Tap between the 6 PM / 9 PM / 11 PM chips, watch the coldest
               temperature and the layer recommendation change (need 4)
-->

---

## 4. Generative AI transcript

**[ ▸ PASTE TRANSCRIPT LINK OR ATTACH `TRANSCRIPT.md` / `TRANSCRIPT.pdf` HERE ]**

This prototype was built in a single Claude Code session. The full transcript covering that
session accompanies this document, per the course Gen AI policy.

---

## Technical notes

- **Data:** [Open-Meteo](https://open-meteo.com/) forecast and geocoding APIs (keyless,
  CORS-enabled), plus BigDataCloud for reverse-geocoding the location label.
- **Stack:** one self-contained `index.html` — no framework, no build step, no API keys.
- **Hosting:** GitHub Pages.
- **Prototype scope:** this is a functional and interface prototype. It genuinely fetches
  live data and its controls are real, but it is deliberately not a finished visual design
  and has not been tested with users in context.
