# C-17 Courseware — Support

C-17 Courseware is a native iPad and iPhone training app for C-17 aircrew. It plays your unit's C-17 Phase CBT packages on-device, tracks your attempts, and exports TMS-format results for the official record.

## Quick help

### How do I get a course into the app?

1. Get the course `.zip` file onto your iPad — AirDrop from another device, save from an email attachment, or copy to the **Files** app.
2. Open C-17 Courseware. Tap the **Courses** tab.
3. Tap the import button (down-arrow in the top toolbar).
4. Pick the `.zip` file. The course appears in the list with its lessons and modules within a few seconds.

### A test result didn't export to TMS — what now?

The app writes auto-export files into the **Performance** folder visible in the iPad's Files app (under "On My iPad → C-17 Courseware"). If a test is missing there:

1. **Profile → Manage Data → Snapshot row** — confirm the attempt was recorded.
2. If the attempt is there but the file is not, force-close and re-open the app, then take the test once more. The TMS export is regenerated on every pass.
3. If the problem persists, use **Profile → Submit Feedback** with logs attached and we'll triage.

### I forgot my profile name — can I get it back?

Names are stored locally on your device. If you have an **encrypted backup** (`.cbtbk` file) on another device or in iCloud Drive, restore it via **Profile → Manage Data → Restore Backup**. Otherwise, re-enter your name in the Profile tab — your attempt history persists independently of the name field.

### How do I move my progress to a new iPad?

1. On the old iPad: **Profile → Manage Data → Export Backup**. AirDrop the resulting `.cbtbk` file to the new iPad.
2. On the new iPad: install C-17 Courseware, open it, then **Profile → Manage Data → Restore Backup** and pick the `.cbtbk` file.
3. Your profile, courses, attempts, and custom courses all restore identically.

### My app keeps crashing on launch.

This is rare. Try in order:
1. Force-close the app (swipe up from home, swipe the C-17 Courseware card up).
2. Restart the iPad.
3. If the crash persists, contact support with your iPad model and iOS version.
4. As a last resort, delete and reinstall the app. Your data will be lost unless you have a backup.

### Course playback has audio glitches or stuttering.

C-17 Courseware plays the original SWF lesson modules through a bundled Ruffle WebAssembly runtime. Older lessons (especially ones with dense slide audio) can occasionally glitch. If a specific lesson is unplayable, use **Submit Feedback** with the lesson ID — we keep a known-bad list to triage.

### The app says my course `.zip` is unsupported.

The app validates course structure on import. A package needs:

- A top-level `Content/` folder.
- A `Content/courseInfo.xml`.
- One or more lesson `.xml` files under `Content/XML/`.
- The matching `.swf` modules under `Content/SWF/`.

If your `.zip` is missing one of these, re-export it from the source authoring tool and try again. The exact failure reason is logged — see **Profile → Submit Feedback → Attach Logs** to share the import log.

## Contact

For anything not covered above, email `<contact-email>` or use **Profile → Submit Feedback** inside the app (which attaches the app log automatically).

## Privacy

C-17 Courseware collects no data and makes no network requests. See the [privacy policy](privacy.html) for details.

## App Store listing

C-17 Courseware on the App Store: `<app-store-url-after-approval>`
