---
layout: default
title: DroneMap Privacy Policy
permalink: /privacy
---

# Privacy Policy

**DroneMap: Terrain & RTH Check**

Effective date: 28 October 2026<br>
Developer: Tigran Barseghyan<br>
Contact: **developer.barseghyan@gmail.com**

---

## In short

> Everything you enter stays on your iPhone. There is no account, no server of mine and no analytics.
>
> To check a plan, the app downloads public terrain tiles for the area. Those requests necessarily tell the tile server which part of the world you are looking at.
>
> Nothing is sold, and nothing is used for advertising or for tracking you across other apps.

The rest of this page explains each of these in full.

---

## What the app stores on your device

- **Sites and plans**: takeoff point, operator position, area or imported path, altitudes, margin, settings and the date you chose. Stored only in the app's own storage on your iPhone.
- **Imported files** (KML, KMZ, GPX): the parts the app uses are kept with the site; the original file is not copied anywhere else.
- **Two example sites** (Castle Valley and the Bonneville Salt Flats, Utah) with their terrain bundled inside the app, so they open without a connection. Opening them sends nothing anywhere.
- **Terrain tiles and orbital elements** downloaded for your checks, kept in the app's cache so later checks and offline use do not download them again. You can clear this cache in **Settings**.
- **Settings**: units, legal preset, margin, radio frequency, constellations, elevation mask and cache size.

Deleting the app deletes all of it. The app does not back any of it up to my servers, because there are none. Your device's normal iCloud or iTunes backup may include the app's data like any other app's.

## Location

With your permission, the app uses your location to place takeoff where you stand and to show you on the map. Location is used only while the app is open, only on the device, and is never sent to me. You can refuse or revoke the permission in iOS Settings; the app still works, with takeoff placed by hand.

## Network requests the app makes

The app has no server of mine. It talks to the following public services directly from your phone:

<div class="table-scroll" markdown="1">

| Service | What is sent | Why |
|---|---|---|
| AWS Open Data Terrain Tiles (`s3.amazonaws.com/elevation-tiles-prod`) | Map tile coordinates covering your area (and a 10 km box around takeoff for the GNSS horizon), a generic app User-Agent, your IP address as with any internet request | Elevation data for the checks |
| CelesTrak (`celestrak.org`) and the TLE mirror (`tle.ivanstanojevic.me`) | A request for the public GNSS orbital-element set; no location | Satellite positions for the GNSS window |
| Apple (App Store, StoreKit) | Handled by iOS under Apple's privacy policy | Purchases, subscriptions, restore |
| Apple Maps | Handled by iOS under Apple's privacy policy | The map |

</div>

Tile coordinates identify an area of roughly 2 to 5 km, not a precise point, and are not linked to you by me; the app has no identifier for you. These services receive your IP address the way every website does; their own policies govern what they keep.

## What the app does not do

- No analytics, crash reporting or advertising SDK of any kind in this version.
- No account, sign-in or e-mail collection.
- No tracking across apps or websites. The app does not ask for App Tracking Transparency permission because it does not track.
- No sharing or selling of data to anyone.

If a future version adds analytics, this page and the App Store privacy label will say so before that version ships.

## Sharing and export

When you share a PNG, PDF or KML from the app, you choose where it goes through the iOS share sheet. Exported files contain your site (coordinates, altitudes, results); treat them accordingly.

## Children

The app is not directed at children under 13 and collects no personal data from anyone.

## Your rights

Since I hold no data about you, there is nothing for me to access, correct or delete on request; everything is on your device and under your control. For questions, write to **developer.barseghyan@gmail.com**.

## Changes

Changes to this policy are posted on this page with a new effective date. Material changes are also noted in the app's release notes.
