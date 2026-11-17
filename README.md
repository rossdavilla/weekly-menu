# Week Plan

A personal meal planner: pick the week's meals, and the app builds the shopping list and the
Sunday prep plan from them. Built to live on an iPhone home screen.

**Live:** https://rossdavilla.github.io/weekly-menu/

## What it does

- Browse the meal library — each meal has a photo, its ingredients, and its prep steps.
- Pick the meals for the week; the **shopping list** is assembled from their ingredients, combined
  and grouped so it can be worked through in one trip.
- The **Sunday prep plan** collects the prep steps of everything chosen, in the order to do them,
  with a built-in timer (`sound/iphone_timer_sound.mp3` is the alarm).

## What's in here

```
index.html                     the whole app — one self-contained file
img/<slug>.jpg                 one photo per meal, named after the meal's slug
sound/iphone_timer_sound.mp3   the prep-timer alarm
apple-touch-icon.png           home-screen icon
```

## Adding a meal

The meal data lives in arrays inside `index.html`: the ingredients feed the shopping list, the
prep steps feed the Sunday plan. Add a photo at `img/<slug>.jpg` matching the slug used in the
data, in the same change, or the card renders with a broken image.

## Running it

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

No build step and no dependencies. Selections are kept in `localStorage` on the device — there is
no backend and nothing is synced between devices.
