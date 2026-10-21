# Leyline for Android

Leyline reads World of Warcraft (TBC Anniversary) combat and chat logs and shows instance runs, boss kills,
everyone's damage and healing, deaths, loot, rolls and week-by-week history, laid out for a phone.

## Getting the app

Every time this repository changes, GitHub builds the app, installs it on an Android emulator, taps through
every screen and saves screenshots. The newest app is `Leyline.apk` on the **results** branch
(Code → switch branch to `results`), or under **Actions** → the latest run → *Artifacts*.

## Using it

1. Install `Leyline.apk` (Android asks you to allow installing apps from your browser or Files app).
2. Open Leyline and tap **Allow access**, then switch on *Allow access to manage all files*. Leyline only reads
   WoW logs and saves reports to `Documents/Leyline Reports`.
3. Copy your logs from the PC (`World of Warcraft\_anniversary_\Logs`: the `WoWCombatLog-….txt` files and
   `WoWChatLog.txt`) to the phone, for example into `Internal storage/Leyline/Logs`, then pick one in the app.

## What's in here

- `app/src/main/python/`: the log reader and all the numbers (the same code as the PC version).
- `app/src/main/assets/web/`: the screens (HTML, CSS, JavaScript).
- `app/src/main/java/app/leyline/MainActivity.java`: the Android shell (storage permission, sharing, clipboard).
- `test/`: made-up test logs (no real players or chat) and the automated emulator test.

Item data: wow-classic-items (MIT). Font: Inter (SIL Open Font License). Python on Android: Chaquopy (MIT).
The signing key `leyline-release.jks` is in the repo on purpose so every build can update the last one.
