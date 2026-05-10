# 🐾 Pawday — Dog Day Route Planner

A dog-friendly outing planner for Toronto, centred on Sherbourne Station. Built as a single-file web app — no build step, no server, just open in a browser.

## Features

- 🗺 Interactive Google Map centred on Sherbourne Station
- ☕ Filter by coffee shops, dog parks, on-leash parks, and pet stores
- 🧭 Auto-build a route or manually pick your stops
- 📏 Live walking distance and estimated time (via Google Directions)
- 🌤 Real-time Toronto weather (no API key needed — uses Open-Meteo)
- 📱 Mobile-friendly
- 💌 Share button to send the link to your gf

---

## Setup (5 minutes)

### Step 1 — Get a free Google Maps API key

1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. Create a project (or use an existing one)
3. Go to **APIs & Services → Enable APIs** and enable:
   - **Maps JavaScript API**
   - **Directions API**
4. Go to **APIs & Services → Credentials → Create API Key**
5. Copy the key

> **Free tier**: Google gives you $200/month credit free — more than enough for personal use.

### Step 2 — Add your key to index.html

Open `index.html` and find this line near the bottom:

```html
src="https://maps.googleapis.com/maps/api/js?key=YOUR_GOOGLE_MAPS_API_KEY&callback=initMap
```

Replace `YOUR_GOOGLE_MAPS_API_KEY` with your actual key.

### Step 3 — Host on GitHub Pages

1. Create a new repo on GitHub (e.g. `pawday`)
2. Upload `index.html` to the root of the repo
3. Go to **Settings → Pages → Source: Deploy from branch → main → / (root)**
4. Wait ~1 min, then your app is live at:

```
https://YOUR_USERNAME.github.io/pawday/
```

Share that URL with your gf — she can open it on her phone with no app install needed.

---

## Restrict your API key (recommended)

After testing, lock down your key so it only works on your GitHub Pages domain:

1. Go to your key in Google Cloud Console
2. Under **Application restrictions** → select **HTTP referrers**
3. Add: `https://YOUR_USERNAME.github.io/*`

This prevents anyone else from using your key if they find it in the source.

---

## Spots included

All spots are within walking distance of Sherbourne Station:

| Place | Type | Rating |
|-------|------|--------|
| Roozamoon Cafe | ☕ Coffee | ★ 4.9 |
| Buvette Pacey | ☕ Coffee | ★ 4.9 |
| Bisou Toronto | ☕ Coffee | ★ 4.7 |
| Mutual Street Perks | ☕ Coffee | ★ 4.7 |
| Bevy | ☕ Coffee | ★ 4.7 |
| Craigleigh Gardens Dog Park | 🏃 Dog park | ★ 4.7 |
| Allan Gardens Dog Park | 🏃 Dog park | ★ 3.9 |
| Barbara Hall Dog Park | 🏃 Dog park | ★ 3.9 |
| Brick Works Dog Park | 🏃 Dog park | ★ 3.8 |
| Milkman's Lane Trail | 🌿 On-leash | ★ 4.8 |
| Riverdale Park East | 🌿 On-leash | ★ 4.8 |
| Riverdale Park West | 🌿 On-leash | ★ 4.7 |
| Rosedale Ravine Park | 🌿 On-leash | ★ 4.5 |
| Don Valley Brick Works Park | 🌿 On-leash | ★ 4.7 |
| HappyPets Pantry | 🛍 Pet store | ★ 4.9 |
| The Beastiary | 🛍 Pet store | ★ 4.8 |
| Pet Cuisine & Accessories | 🛍 Pet store | ★ 4.8 |

---

## Future ideas (when you want to grow it)

- [ ] Add more cities (Vancouver, Montreal, NYC)
- [ ] Let users submit new spots
- [ ] User accounts / saved routes
- [ ] Business listings / "verified" badges (monetization)
- [ ] Seasonal route suggestions
- [ ] Dog size filter (small / large)

---

Built with ❤️ for Tobi the mini schnauzer 🐕
