# Week Plan (`weekly-menu`)

Ross's personal meal planner: pick the week's meals, and the app builds the shopping list and the
Sunday prep plan from them. Live at <https://rossdavilla.github.io/weekly-menu/>.

## Layout

```
index.html                     the whole app — one self-contained file (~1,500 lines)
img/<slug>.jpg                 one photo per meal, named after the meal's slug
                               (e.g. chickpeacurry.jpg, saagpaneer.jpg)
sound/iphone_timer_sound.mp3   the prep-timer alarm
apple-touch-icon.png           home-screen icon (it is used from an iPhone home screen)
```

HTML, CSS and JS are inline in `index.html`; no build step and no dependencies beyond Google
Fonts. Selections and state are kept in `localStorage` on the phone — there is no backend and
nothing is synced.

## Adding or changing a meal

The meal data lives in the arrays inside `index.html`. A meal needs its ingredients (which feed
the shopping list), its prep steps (which feed the Sunday plan), and a photo at
`img/<slug>.jpg` matching the slug used in the data. Add the image in the same change as the
data, or the card renders with a broken photo.

Ross edits these often and in small ways (halving a quantity, rewording a prep step). Match the
voice of the entries already there: prep steps are short bullet-style imperatives.

## Publishing

GitHub Pages serves `main` from the repository root, so a push to `main` is the deploy. It is
installed to an iPhone home screen, so check the layout at phone width.

This app is already in `data/sites.json` in the
[`rossdavilla.github.io`](https://github.com/rossdavilla/rossdavilla.github.io) repo under the
`personal` tag.
