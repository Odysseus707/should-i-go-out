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

**<https://youtube.com/shorts/wB8YarpGf2o?feature=share>** (unlisted)

A 31-second screen recording at phone width, showing the prototype answering each of the four
needs in order: the current temperature, the umbrella verdict for the next six hours, the
scored hourly strip for the best time to be outside, and the return-time chips changing the
clothing recommendation.

---

## 4. Generative AI transcript

**PDF: <https://github.com/Odysseus707/should-i-go-out/blob/main/TRANSCRIPT.pdf>**

Markdown: <https://github.com/Odysseus707/should-i-go-out/blob/main/TRANSCRIPT.md>

This prototype was built with Claude Code (Claude Opus 5). The transcript covers the entire
session — the design discussion, the build, and the revisions — per the course Gen AI policy.
Raw tool output (file contents, API responses, browser snapshots) is omitted for length; each
assistant message still lists the tools it invoked.

---

## Technical notes

- **Data:** [Open-Meteo](https://open-meteo.com/) forecast and geocoding APIs (keyless,
  CORS-enabled), plus BigDataCloud for reverse-geocoding the location label.
- **Stack:** one self-contained `index.html` — no framework, no build step, no API keys.
- **Hosting:** GitHub Pages.
- **Prototype scope:** this is a functional and interface prototype. It genuinely fetches
  live data and its controls are real, but it is deliberately not a finished visual design
  and has not been tested with users in context.
