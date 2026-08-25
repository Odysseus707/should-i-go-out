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

So besides the two prerequisite features that were in the project description already, I came
up with two specific other functionalities that I would find interesting to have in such a
weather app. one of them being the feature of telling me the kinda clothing I need to wear.
Usually, the thing is that I find it difficult for me to actually understand the Fahrenheit
system too much since I have been living in a Celcius system throughout my life. I wanted to
get a better idea of how cold certain temperatures are in Fahrenheit so I could get used to
the weather forecasts I see in the news. So this tells me if I need To wear a shirt outside or
maybe a light jacket or a heavy jacket or stay completely padded up or even wear rainy day
clothes. In a similar vein, I would say the other feature that I wanted to implement was the
when should I go out feature. This essentially tells me the best time during the day to
actually go out for a walk because I'm a big fan of walks, and sometimes I feel like I go
outside and the temperature is a bit too cold or it's a bit too dreary. So these feature both
tie into the act of me deciding when to go for a walk.

---

## 3. Video walkthrough

**[ PASTE VIDEO LINK OR ATTACH FILE HERE ]**

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

**[ PASTE TRANSCRIPT LINK OR ATTACH `TRANSCRIPT.md` / `TRANSCRIPT.pdf` HERE ]**

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
