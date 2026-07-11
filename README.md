[README.md](https://github.com/user-attachments/files/29931289/README.md)
# Pose Wheel

A self-contained photo shoot pose spinner built as a single-page web app. Designed for live events where participants spin a wheel and get a random pose prompt with an optional full-screen reference photo.

Works offline. No account required. All data stays on your device.

---

## What's in the box

| File | Purpose |
|---|---|
| `index.html` | The entire app (HTML + CSS + JS, one file) |
| `sw.js` | Service worker that caches everything for offline use |
| `manifest.webmanifest` | Tells the browser this is an installable app |
| `icon-180.png` | Apple touch icon (iPad/iPhone home screen) |
| `icon-192.png` | Android/PWA icon |
| `icon-512.png` | High-res icon for splash screens |

Optional:

| File | Purpose |
|---|---|
| `glittercamp-import.json` | Example backup file with 34 sample poses and a pre-built wheel |

---

## Install on iPad (recommended)

The app installs as a home screen icon that launches fullscreen, stays cached offline, and keeps your data safe from Safari's automatic storage cleanup.

**You need a free static host.** GitHub Pages is the easiest option and costs nothing.

### Step 1: Create a GitHub repository

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click the **+** button (top right), then **New repository**
3. Name it `posewheel` (or whatever you want)
4. Set it to **Public**
5. Click **Create repository**

### Step 2: Upload the app files

1. On the new repo page, click **"uploading an existing file"**
2. Drag all **6 files** onto the upload area: `index.html`, `sw.js`, `manifest.webmanifest`, `icon-180.png`, `icon-192.png`, `icon-512.png`
3. Do NOT upload the zip or the folder. Just the 6 loose files.
4. Click **Commit changes**

### Step 3: Enable GitHub Pages

1. Go to your repo's **Settings** tab
2. In the left sidebar, click **Pages**
3. Under "Source," select **Deploy from a branch**
4. Branch: **main**, folder: **/ (root)**
5. Click **Save**
6. Wait 1 to 2 minutes for the deploy to finish

Your app is now live at:
```
https://YOUR-USERNAME.github.io/posewheel/
```

### Step 4: Add to Home Screen

1. Open that URL in **Safari** on your iPad
2. Tap the **Share** button (square with arrow)
3. Tap **Add to Home Screen**
4. Name it "Pose Wheel" (or anything), tap **Add**
5. **Close the Safari tab.** From now on, always launch from the home screen icon.
6. Open the app from the icon once while still online. This triggers the service worker to cache everything.
7. Test: turn on Airplane Mode, open the app. It should load normally.

### Why the home screen icon matters

Safari automatically deletes website data after 7 days of inactivity. Home screen web apps are exempt from this. If you only use the Safari tab, your poses and photos will vanish between events.

**Important:** The Safari tab and the home screen app have separate storage. If you import data in Safari, it will not appear in the home screen app. Always do everything (importing, adding poses, spinning) inside the home screen app.

---

## Install on other devices

The same GitHub Pages URL works on any device with a modern browser.

- **iPhone:** Same as iPad. Safari, Share, Add to Home Screen.
- **Android:** Open in Chrome, tap the three-dot menu, "Add to Home Screen" or "Install app."
- **Desktop (Mac/Windows):** Open in Chrome or Edge. Click the install icon in the address bar, or just bookmark it. Desktop browsers don't aggressively purge storage, so a bookmark is fine.

---

## Importing a backup file

Backup files (like `glittercamp-import.json`) contain all poses, photos, wheels, tags, and settings in one JSON file.

1. **Launch the app from the home screen icon** (not a Safari tab)
2. Go to the **Settings** tab (gear icon)
3. Tap **Import backup**
4. Pick the `.json` file from Files, iCloud Drive, or wherever you saved it
5. Confirm when prompted. Import replaces all current data.
6. The app will show a progress indicator as it loads each pose

After importing, go to the Play tab and verify your wheel and poses are there.

### Where to put the backup file on iPad

The easiest options:

- **iCloud Drive:** Save the JSON file to iCloud Drive on any device. The iPad's file picker can browse iCloud directly.
- **AirDrop:** Send the file from a Mac or another Apple device.
- **Email/Messages:** Send it to yourself, tap the attachment, tap Share, "Save to Files."

---

## Adding poses manually

1. Go to the **Poses** tab
2. Tap **+ Add**
3. Type the prompt text
4. Tag it: **Solo**, **Pair**, **Group 3+** (pick all that apply)
5. Tap **Choose photo** to attach a reference image (optional)
6. If you added a photo, adjust the wheel crop with the zoom slider and drag. This only affects how the photo looks on the wheel wedge. The landing page always shows the full original.
7. Tap **Save**

---

## Managing wheels

A wheel is a named selection from your master pose library. One pose can belong to multiple wheels.

- Go to the **Wheels** tab
- Type a name and tap **+ Add** to create a new wheel
- Expand a wheel to check/uncheck which poses it includes
- On the Play tab, tap the wheel name (top of screen) to switch between wheels

If you only need one wheel, skip this entirely. The default "All poses" view shows everything.

---

## Filtering by group size

On the Play tab, tap the filter chips above the wheel:

- **All** = every pose on the current wheel
- **Solo** = poses tagged for one person
- **Pair** = poses tagged for two people
- **Group** = poses tagged for three or more

The wheel rebuilds instantly when you switch filters. Fair mode tracks progress per filter, so switching from Solo to Pair starts a fresh cycle.

---

## Fair mode

When enabled (Settings tab), every pose plays exactly once before any repeats. A counter below the wheel shows "12 poses, 8 left." When the pool empties, it reshuffles and toasts a notice.

The winner is pre-selected from the remaining pool, then the wheel animates to land on it. Your flick controls the speed and direction (the feel), not the outcome. This is how every fair-mode wheel app works.

---

## Presenting on a TV

1. Connect the iPad to an Apple TV via AirPlay (Control Center, Screen Mirroring)
2. Tap the **Present** button (bottom of the Play tab)
3. The app goes fullscreen, hides all controls, and keeps the screen awake
4. Tap the **X** button (top corner) or swipe to exit Present mode

This is screen mirroring, not native AirPlay video. The TV shows exactly what the iPad shows.

---

## Exporting a backup

1. Settings tab, tap **Export backup**
2. A `.json` file downloads containing every pose (with embedded photos), every wheel, all settings
3. Save it somewhere safe: iCloud Drive, a Mac, email it to yourself

Photos are embedded as base64 inside the JSON, so backup files can be large (tens of MB if you have many high-res photos). This is intentional: the backup is fully self-contained and works without internet.

**Back up before every event.** If anything goes wrong, you can import the backup and be running in 30 seconds.

---

## Updating the app

If you receive a new version of `index.html`:

1. Go to your GitHub repo
2. Click on `index.html`, then the pencil (edit) icon, or delete and re-upload
3. Also update `sw.js`: open it, change `posewheel-v1` to `posewheel-v2` (or increment the number). This tells the service worker to re-cache.
4. Commit the changes
5. Wait 1 to 2 minutes for GitHub Pages to redeploy
6. Open the app from the home screen while online. The service worker will pull the new version.

Your saved data (poses, photos, wheels) is untouched by app updates. Data lives in IndexedDB, code lives in the cache. They're separate.

---

## Troubleshooting

**App won't load offline:**
Launch it once while online after installing to the home screen. The service worker needs that first load to cache the files.

**Poses disappeared:**
You probably imported data in the Safari tab instead of the home screen app (or vice versa). They have separate storage. Import again inside the correct one.

**Photos look different on the wheel vs the landing page:**
This is intentional. The wheel wedge shows a cropped/zoomed slice of the photo (adjustable per pose). The landing page always shows the full original image. This was a deliberate fix: the old app degraded landing photos when you adjusted the wheel crop.

**"Import backup" doesn't see my file:**
Make sure the file has a `.json` extension. The file picker filters by type. If you renamed it or it downloaded as `.txt`, rename it back to `.json`.

**Wheel shows "Add some poses":**
Either no poses exist yet, or your current wheel/filter combination has zero matching poses. Try switching the filter to "All" or the wheel to "All poses."

---

## Technical notes

- Single self-contained HTML file, no external dependencies, no build step
- Storage: IndexedDB when running standalone, with an in-memory fallback
- Photos are auto-downscaled to max 2000px on import to stay within storage limits. Originals remain in your Photos library.
- Audio (tick sounds, landing chime) is generated with the Web Audio API. No sound files needed.
- The service worker uses a cache-first strategy: it serves from cache and only hits the network for uncached resources.

---

## Privacy

- **Nothing leaves the device.** No analytics, no tracking, no server calls after the initial page load.
- The GitHub Pages host serves the static files only. It has no access to your poses, photos, or usage.
- Backup files contain your photos as base64 data. Treat them like you'd treat the photos themselves.
