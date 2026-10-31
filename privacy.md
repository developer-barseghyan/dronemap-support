---
layout: default
title: DroneMap Privacy Policy
permalink: /privacy
dm_section: privacy
---

# Privacy Policy

App: **DroneMap: Terrain & RTH Check** for iPhone<br>
Published by: Tigran Barseghyan<br>
Effective from: 30 October 2026<br>
Questions: [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com)

This page follows each path that data can take inside DroneMap. I run no server for the app and I receive nothing from it. No personal data about you reaches me.

## Data flows at a glance

| Flow | Leaves the iPhone? | Who receives it |
|---|---|---|
| Your position | No | Nobody |
| Terrain tile downloads | Yes, tile numbers only | Amazon Web Services (AWS Open Data) |
| The map view | Yes, through iOS | Apple |
| Pro purchases | Yes, through iOS | Apple |
| Files you import | No | Nobody |
| Files you export | Only where you send them | The app or person you pick |
| Usage statistics | Not gathered | Nobody |

## 1. Your position

If you allow it, DroneMap reads your location to drop the takeoff pin where you stand and to draw a dot for you on the map. It reads location only while the app is in use. The position stays on the phone and is never sent to me or to anyone else. You can say no, or switch the permission off later in iOS Settings. Without it, you place the takeoff pin by hand and every check still works.

## 2. Terrain tile downloads

The checks need ground heights. DroneMap fetches them from the public AWS Open Data Terrain Tiles bucket (`s3.amazonaws.com/elevation-tiles-prod`). Each request names a tile by its grid numbers. A tile covers a patch of roughly 2 to 5 km, not an exact point. The request also carries a plain app User-Agent and, as with any web request, your IP address. DroneMap adds no identifier for you. Amazon's own policies decide what its servers log.

Downloaded tiles stay in the app's cache so the next check and offline use need no fresh download. You can empty that cache in DroneMap's Settings.

The two Utah sample sites ship with their terrain inside the app. Opening them makes no network request.

## 3. The map view

The base map is Apple Maps, drawn by iOS. Apple handles those map requests under its own privacy policy.

## 4. Pro purchases

Buying, renewing and restoring Pro run through Apple's StoreKit. Apple handles your payment and your Apple Account. I see no card details and no name. DroneMap only learns from iOS whether Pro is active on the device.

## 5. Files you import and export

KML, KMZ and GPX files you open in DroneMap are read on the phone. The app keeps the parts it needs with the site and copies the file nowhere else.

A PNG, PDF or KML that you export goes only where you send it with the iOS share sheet. These files hold your site's coordinates, heights and results. Share them with the same care as any location data.

## 6. What sits in the app's storage

- Saved sites: takeoff and operator points, the area or imported path, heights, margin and the chosen date.
- Downloaded terrain tiles.
- Your settings: units, height cap, margin, radio band, Sun heights and the terrain storage limit.

Removing DroneMap from the phone erases all of this. Your normal iCloud or computer backup of the iPhone may contain this storage, as it would for any app.

## 7. Measurement and tracking

DroneMap 1.0 has no analytics, no crash reporter and no ad network. It has no account or sign-in and never asks for your email address. It does not follow you across other apps or websites, so it has no reason to show the App Tracking Transparency prompt. No data is sold, rented or handed to anyone. On its App Store page, DroneMap carries the privacy category "Data Not Collected".

If a later version ever adds analytics, this page and the App Store label will both be updated before that version is released.

## 8. Young users

DroneMap is made for a general audience and does not target kids younger than 13. It gathers no personal data from anyone of any age.

## 9. Questions and requests

I hold no record about you, so I have nothing to show, fix or erase on request. Your data lives on your iPhone, and you control it there. For any privacy question, email [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com).

## 10. Revisions to this policy

A revised policy will appear at this address with a new effective date. Larger revisions will also be mentioned in the app's release notes.
