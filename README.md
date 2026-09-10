# Tool Pocket Generator V51

Clean new-version build following the approved V12.2 baseline. V51 keeps the established photo outline engine, dimensional master, editable numbered profile, Straight/Curved segments, proportional scale, clearance, geometry check, saved tools, JSON profile backup and STL workflow.

## V51 Finger Relief workflow
Finger Relief Access is part of **Draw / Edit Profile**. It is not a separate locked stage.

- Add / reposition finger relief before profile confirmation.
- Tap anywhere on the outline edge to select the nearest segment and exact position.
- FR1 and FR2 are displayed separately from normal numbered points.
- Remove the relief and place it again elsewhere as required.
- Relief changes are included in Undo.
- Confirm only when both the numbered outline and finger relief are correct.
- Close Profile & Scale remains the final profile lock.

## Undo
Undo reverses user edits newest-first. The generated/imported outline is the baseline and is never removed by Undo. Once the edit history is exhausted, further Undo does nothing.

## Repository
- index.html
- manifest.webmanifest
- sw.js
- README.md


## V51 clean new-version build
V51 is a new build following V13.0 testing. It does not amend V13.0 in place.

### V13.0 testing issues addressed
- Finger Relief Access remains part of Draw / Edit Profile.
- Finger relief can be added, repositioned or removed before final profile confirmation.
- FR1 and FR2 remain separate from normal numbered outline points.
- Finger relief edits remain part of Undo history.
- Final confirmation explicitly covers both the numbered profile and finger relief.
- After Close profile & scale, the exact completion message is: **Profile & Finger Relief completed — profile closed and scaled. Ready for Engineering Geometry Check.**
- The app automatically scrolls to Engineering Geometry Check after successful close/scale.
- JSON profile backup/import is optional and placed under **Optional: Saved Profiles**. JSON is for profile backup/reuse; STL remains the manufacturing export.

### Normal workflow
Profile editing + Finger Relief → Confirm profile & finger relief editing complete → Close profile & scale → Engineering Geometry Check → STL export.


V51 photo detection: the physical metric ruler in the uploaded photo is the authoritative scale for measuring the tool only. Detect Tool Outline leaves the entered master Length × Width unchanged and places the measured tool outline inside that rectangle. Set dimensions from physical grid deliberately replaces the master dimensions with the measured tool dimensions.
