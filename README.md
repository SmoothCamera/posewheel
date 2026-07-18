========================================
  POSE WHEEL - START HERE
========================================

Read this first. It's short. It will save you a lot of confusion.


----------------------------------------
  THE ONE RULE THAT MATTERS MOST
----------------------------------------

Install the app to your iPad home screen ONE time (steps below).
After that, ALWAYS open it from that home screen icon.

Do NOT double-click index.html to use it day-to-day.
Do NOT use it in a Safari tab.

Here's why this matters:

Every place you open this app has its own SEPARATE saved data.
They look identical but they don't share anything.

  - The file you double-click        = one separate copy of your data
  - The home screen app              = a DIFFERENT separate copy
  - A Safari tab                     = yet ANOTHER separate copy

If you edit your poses in one place, then open a different place,
your edits will seem to have "disappeared." They didn't. They're
still in the first place. You're just looking at a different copy.

THE SOLUTION: Pick the home screen app. Use only that. Always.
Then there is only ONE copy of your data and nothing gets lost.


----------------------------------------
  HOW SAVING WORKS (READ THIS ONCE)
----------------------------------------

You do NOT need to press save. The app saves automatically as you
edit, to whatever place you currently have open.

EXPORT = download a backup file to keep or move to another device.
IMPORT = REPLACE everything currently in the app with a backup file.

  *** IMPORT ERASES what's there and replaces it. ***

So the golden habit is:

  1. Do your editing (in the home screen app).
  2. The moment you finish, tap Settings > Export backup.
  3. That's your safety copy. Done.

Do NOT import a file after editing unless you WANT to throw your
edits away and go back to that file. Import is for restoring or
moving to a new device, not for saving.


----------------------------------------
  INSTALL IT (ONE TIME, ~5 MINUTES)
----------------------------------------

You need a free GitHub account to host the app so your iPad can
install it. This is the one-time annoying part. After this it just
works forever, offline, from your home screen.

STEP 1 - Make a GitHub repository
  1. Go to github.com, sign in (or make a free account)
  2. Click the + (top right), then "New repository"
  3. Name it: posewheel
  4. Choose Public
  5. Click "Create repository"

STEP 2 - Upload the app files
  1. Click "uploading an existing file"
  2. Drag in ONLY these 6 files:
        index.html
        sw.js
        manifest.webmanifest
        icon-180.png
        icon-192.png
        icon-512.png
  3. Do NOT upload this README or the Glitter Poses file.
  4. Click "Commit changes"

STEP 3 - Turn on hosting
  1. In the repo, click Settings, then Pages (left menu)
  2. Source: "Deploy from a branch"
  3. Branch: main    Folder: / (root)
  4. Click Save, wait 1-2 minutes

  Your app is now live at:
        https://YOUR-USERNAME.github.io/posewheel/

STEP 4 - Add to home screen
  1. Open that link in Safari on your iPad
  2. Tap the Share button, then "Add to Home Screen"
  3. Tap Add
  4. CLOSE Safari. From now on only use the home screen icon.
  5. Open it once from the icon while online (this makes it work
     offline forever after).


----------------------------------------
  LOAD YOUR POSES
----------------------------------------

  1. Put the "Glitter Poses" .json file somewhere your iPad can
     reach it (iCloud Drive, or email it to yourself, or AirDrop).
  2. Open the app FROM THE HOME SCREEN ICON.
  3. Tap Settings > Import backup.
  4. Pick the .json file.
  5. Done. Your poses, photos, and tags are all loaded.


----------------------------------------
  DAY-TO-DAY: ADDING OR EDITING POSES
----------------------------------------

  - Poses tab: tap "+ Add" for one pose, or "Bulk" to add many
    photos at once (each photo becomes a pose).
  - Tap any pose card to open its editor.
  - Tap the title to rename it. Tap a tag (Solo/Pair/Group) to
    toggle it. Tap the box icon to archive.
  - ARCHIVE = hide a pose from the wheel without deleting it.
    Good for poses that don't have a photo yet. Find archived
    poses with the "Archived" filter at the top of the Poses tab.

  WHEN YOU'RE DONE EDITING: Settings > Export backup. Every time.
  Name it with today's date so you know which is newest.


----------------------------------------
  RUNNING IT AT THE PARTY
----------------------------------------

  - Pick Solo, Pair, or Group at the top. Toggle the male symbol
    if you want only poses that need it.
  - Flick the wheel with your finger (harder = longer spin), or
    tap the SPIN button.
  - When it lands: the title shows first, then the photo, then
    the how-to text.
  - "Present" (top right) goes fullscreen and keeps the screen
    awake. Use AirPlay screen mirroring to put it on a TV.


----------------------------------------
  MOVING WORK BETWEEN iPAD AND MAC
----------------------------------------

Editing lots of text is much easier on the Mac. Here is exactly
how to move your work back and forth. Follow every step.

USE "IMPORT & MERGE" FOR THIS. Not Replace. Merge adds and updates
without deleting anything, so you can't lose work by going the
wrong direction.


=== PART 1: GET YOUR WORK OFF THE iPAD ===

  1. On the iPad, open Pose Wheel from the home screen icon.
  2. Tap "Settings" in the top right.
  3. Scroll down to the box labeled "Backup".
  4. Tap the blue "Export backup" button.
  5. A box appears asking where to save. Tap "Save to Files".
  6. Choose a place you'll remember. "iCloud Drive" is best
     because the Mac can see it too. Tap "Save" (top right).
  7. The file is named something like:
        Glitter Poses 2026-07-14 1728 35photos.json
     The date, time, and photo count are in the name so you can
     always tell which file is newest.


=== PART 2: GET THE FILE ONTO THE MAC ===

  Pick ONE of these two methods.

  METHOD A - iCloud Drive (automatic, no clicking)
  ------------------------------------------------
  If you saved to iCloud Drive in Part 1:
  1. On the Mac, open Finder.
  2. In the left sidebar, click "iCloud Drive".
  3. Your file is there. It may take a minute to appear.
     If you see a little cloud icon on it, click the file once
     to download it fully.

  METHOD B - AirDrop (fast, manual)
  ----------------------------------
  1. On the iPad, open the "Files" app.
  2. Find the file you just saved (check "Recents" at the bottom).
  3. Press and HOLD your finger on the file until a menu appears.
  4. Tap "Share".
  5. Tap "AirDrop".
  6. Your Mac's name appears as a circle. Tap it.
  7. On the Mac, click "Accept" if it asks.
  8. The file lands in your Mac's "Downloads" folder.


=== PART 3: OPEN THE APP ON THE MAC AND LOAD THE FILE ===

  1. On the Mac, open the app.
     - If you installed it on GitHub, go to your link:
           https://YOUR-USERNAME.github.io/posewheel/
     - Bookmark this link. Use the SAME bookmark every time.
  2. Click "Settings" in the top right.
  3. Scroll to the "Backup" box.
  4. Click "Import & Merge" (NOT "Import & Replace").
  5. A file picker window opens. Find the file from Part 2
     (look in Downloads or iCloud Drive). Click it, then "Open".
  6. A message tells you how many poses will be added or updated.
     Click "OK".
  7. Wait for the progress bar. Your iPad work is now on the Mac.


=== PART 4: DO YOUR EDITING ON THE MAC ===

  Now you have a real keyboard. Copy and paste all you want.
  - Click "Poses" at the top.
  - Click any pose card to open it and edit the text.
  - Add photos, change descriptions, fix tags.


=== PART 5: SEND IT BACK TO THE iPAD ===

  1. On the Mac, click "Settings".
  2. Click the blue "Export backup" button.
  3. The file goes to your Mac's "Downloads" folder automatically.
     (Look for the newest file starting with "Glitter Poses".)

  Now move it to the iPad. Pick ONE:

  METHOD A - AirDrop (fastest)
  -----------------------------
  1. Open Finder, go to "Downloads".
  2. Right-click the new "Glitter Poses" file.
  3. Choose "Share", then "AirDrop".
  4. Click your iPad when it appears.
  5. On the iPad, tap "Accept".
  6. It asks which app to open it with. Tap "Save to Files"
     and put it in iCloud Drive or On My iPad.

  METHOD B - iCloud Drive
  ------------------------
  1. Open Finder, go to "Downloads".
  2. Drag the file into "iCloud Drive" in the sidebar.
  3. Wait a minute for it to sync.

  Then on the iPad:
  1. Open Pose Wheel FROM THE HOME SCREEN ICON.
  2. Tap "Settings".
  3. Tap "Import & Merge".
  4. Find and pick the file you just moved over.
  5. Confirm. Done. Your Mac edits are now on the iPad.


=== THE SHORT VERSION (once you've done it once) ===

  iPad  -> Settings -> Export -> Save to Files (iCloud Drive)
  Mac   -> Settings -> Import & Merge -> pick that file
  Mac   -> edit everything with a real keyboard
  Mac   -> Settings -> Export (goes to Downloads)
  AirDrop that file to the iPad
  iPad  -> Settings -> Import & Merge -> pick it

  Always MERGE. Always export right after editing.


=== IF SOMETHING LOOKS WRONG ===

  "I don't see my new poses after merging"
     Check you picked the newest file. The date and time are in
     the filename. Newest = most recent date/time.

  "It says nothing new in that file"
     That file is identical to what's already there. You probably
     picked an older export by mistake.

  "I accidentally clicked Replace instead of Merge"
     Import your most recent export to get back. This is why you
     export often. Every export is a restore point.


----------------------------------------
  WHAT EACH FILE IN THIS FOLDER IS
----------------------------------------

  index.html ............ the actual app
  sw.js ................. makes it work offline
  manifest.webmanifest .. lets it install to home screen
  icon-*.png ............ the app icons
  Glitter Poses ....json  your poses + photos (import this)
  README ................ this file


----------------------------------------
  IF SOMETHING BREAKS
----------------------------------------

  "My edits disappeared!"
     You're looking at a different copy. Use the home screen app
     only. Import your last export to restore.

  "The wheel looks wrong / broken after I opened the folder"
     Double-clicking the file is unreliable. Install to the home
     screen and use that instead.

  "I imported and lost my new work"
     Import replaces everything. Only import to restore or move
     devices. Export (don't import) to save.

  When in doubt: Export a backup. It can't hurt. It's just a copy.
