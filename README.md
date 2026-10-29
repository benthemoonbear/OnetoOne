# One to One

Website for One to One, dog walking and cat sitting in Belper, Derbyshire.

It's a single static page (`index.html`) with its images, fonts and icons in `assets/`. There's no build step: upload the folder to any static host (GitHub Pages, Cloudflare Pages, Netlify) and it works.

## Folders

| Path | What's in it |
|---|---|
| `index.html` | The whole website |
| `assets/painting.jpg` | The painting behind the logo (currently a placeholder) |
| `assets/photos/` | Photos of the dogs and cats, with a soft warm grade applied |
| `assets/fonts/` | DM Serif Display and Figtree (both open licence) |
| `assets/icons/` | Favicon and home-screen icons |
| `assets/og-image.jpg` | Picture shown when the site is shared on social media or in messages |
| `logo/` | Logo files: SVG and PNG, colour, black, white, on green, with and without the subtitle |

## Swapping in the real painting

Replace `assets/painting.jpg` with a photo of the finished canvas, keeping the same file name. Use a sharp, straight-on photo in daylight, at least 2400px wide. The page shows a wide strip across the painting with the logo over the sky, so the framing may need adjusting afterwards.

## Bookings (Cal.com)

The "Request a booking" section loads Mayah's live calendar from [cal.com/mayahmoo](https://cal.com/mayahmoo). The username and event links are set near the bottom of `index.html`:

```js
const CAL_USERNAME = "mayahmoo";
```

Each service loads its own Cal.com event type, so each can have its own hours:

| Service | Cal.com link |
|---|---|
| Dog walk, half an hour (£10) | `dog-walk-30` |
| Dog walk, one hour (£15) | `dog-walk-60` |
| Night walk (price on request) | `night-walk` |
| Cat sitting visit, half an hour (£12) | `cat-sitting-30` |
| Cat sitting, longer and overnight stays (price on request) | `cat-sitting-stay` |

All event types should have **Requires confirmation** turned on, so bookings come in as requests that Mayah confirms or replies to.

## Still to do

- Replace the placeholder painting with the real canvas.
- Add the artist's name where the page says `[artist name]` (two places).
- Set prices for night walks and longer stays when decided.
- Once the site has its own domain, change `og:image` in `index.html` to the full address (e.g. `https://example.co.uk/assets/og-image.jpg`) so link previews show the picture.
- The Belper map is illustrated from memory of the area and not to scale; worth a check by someone local.
