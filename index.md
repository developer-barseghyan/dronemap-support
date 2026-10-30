---
layout: default
title: DroneMap Support
permalink: /
---

# Support

**DroneMap: Terrain & RTH Check** checks a drone flight against the ground before takeoff. Place your takeoff, draw the area, enter the altitude and the Return-to-Home height you will set in your drone app, and DroneMap shows where that plan hits terrain, the RTH altitude that clears every ridge on the way home, where a takeoff-relative altitude breaks the 400 ft / 120 m limit, and which parts of the area are hidden from where you stand.

There is no account and no server of mine. Every check runs on your iPhone, and your saved sites stay on it.

---

## Contact

**developer.barseghyan@gmail.com**

I usually reply within about two business days. If a result looks wrong, please read *"A result looks wrong"* below and include what it asks for.

---

## Before anything else

**DroneMap is a planning aid.** It works from a public elevation model of the bare ground with about 30 m between samples and a vertical error that can reach several meters, more on steep slopes. **Buildings, trees, masts, wires and new earthworks are not in it.** A green map means the terrain model clears your plan by your margin, nothing more. Keep your drone in sight, keep the drone app's own warnings on, and follow the rules of the place you fly in.

---

## Getting started in a minute

1. **Open an example.** The Sites tab has two ready-made example sites. **Castle Valley, Utah** shows what the app is for: an RTH of 50 m (165 ft) would fly the drone into the valley wall on the way home. **Bonneville Salt Flats, Utah** is the opposite, clear on every check. Both work offline.
2. **Make your own plan.** On the Plan tab, tap **Takeoff here** (or long-press the map), then tap the map to add the corners of your area, or choose **Circle**. The card at the bottom always says the next step.
3. **Enter your numbers.** Your flight altitude and the RTH altitude set in your drone app, both above takeoff, as your controller shows them.
4. **Tap Check.** The results open on the check that needs your attention most. Tap any row to see its layer on the map, and **Profile** for the side view.

---

## Frequently asked questions

### Why does my drone show a different altitude than the app?

Consumer drones measure altitude from the point where they took off, not from the ground beneath them. The number on your controller is "above takeoff". If you take off in a valley and fly over a ridge 100 m higher, a reading of 120 m means you are 20 m above that ridge. DroneMap converts your above-takeoff altitude into height above the real ground everywhere in your area; that is the whole point of the app.

### What do the four checks mean?

<span class="tag danger">Terrain</span> Where the planned altitude is inside the terrain model, or closer to it than your safety margin (30 m by default). The verdict also gives the altitude that clears the whole area. The map shows the RTH line on this layer too, so you see the way home over the same colors.

<span class="tag caution">Safe RTH</span> Return-to-Home climbs to the RTH altitude and flies home in a straight line at that altitude. DroneMap traces that line from every point of the area and reports the lowest RTH altitude that clears terrain on all of them, with the point that drives the number and the line drawn on the map. Set your drone's RTH altitude to that value or higher.

<span class="tag ok">Legal AGL</span> The 400 ft (FAA) or 120 m (EASA) limit is measured above the ground under the drone. Over falling ground a legal above-takeoff altitude becomes illegal. DroneMap shows where, and the band of altitudes that is both legal and clear everywhere, or tells you that no single altitude satisfies both.

<span class="tag ok">Line of sight</span> From where you stand (plus your antenna height), which parts of the area are behind terrain at the planned altitude, with Earth curvature and the radio Fresnel zone at 2.4 or 5.8 GHz. It also finds the nearby spot that would let you see more of the area, and shows how much more.

### What is the big number at the top of the results?

The one answer you need first. It is the minimum flight altitude when your plan hits terrain, the minimum RTH altitude when only the way home is the problem, or the legal altitude band when legality is. Under it, **SHORTFALL** is how far your value is below that minimum; **CLEARANCE** is how far above it you are.

### What is the Profile?

A side view along one line from your takeoff: the ground, your flight altitude, your RTH altitude, your safety margin and the legal limit. By default it follows the line to the point that drives the selected check (for example the RTH driver). Tap **Move far point** to drag it anywhere in your area, and run a finger across the chart to read the ground and your height above it at each point. The chart's height is stretched to make the terrain visible; the factor is shown in its corner. The profile is free.

### How do I change my area?

Press and drag any corner. Drag the small handle in the middle of an edge to add a corner there. Tap a corner to select it, then **Delete corner** or **Undo** in the card. For a circle, drag its center or the handle on its edge. The takeoff and operator pins can be dragged the same way. A tap on the map shrinks the card so you can see more of it; tap the card or its arrow to bring it back.

### What does Save do?

It saves the current plan and its result as a site in the Sites tab, or updates the site you opened. It does not run the check again; editing anything runs it again on its own. To re-check a saved site for today's date, swipe it right in the Sites list.

### A result looks wrong.

Please send the following and I will look at it the same week:

1. The site, exported from the results card as **PDF** or **KML** (Pro), or a screenshot of the map with the verdict rows visible.
2. The takeoff coordinates, the altitude and RTH values you entered, and your margin.
3. What you expected instead, and why (a topographic map, a drone log, a photo).

The usual reasons are: a terrain void or smoothing in the elevation model (narrow gorges and sharp peaks can be off by tens of meters), a takeoff point placed on a slope a few meters from where you actually stood, or an imported file whose altitudes are above sea level rather than above takeoff (see the import question).

### The map says "No data" in places.

Those are cells where a terrain tile could not be loaded. DroneMap never guesses: run the check again with a connection, or download the site for offline use (Pro) before leaving coverage.

### Does the app know about trees and buildings?

No. The elevation model is a bare-earth radar survey. Dense forest and large buildings are partly in it, individual trees, masts and wires are not. Treat the result as "terrain clearance" and add your own margin for obstacles.

### How accurate is the elevation data?

About 30 m between samples; absolute vertical error within 16 m for 90 % of the land, typically 5 to 10 m in open terrain and worse in narrow valleys and on steep slopes. The default 30 m safety margin exists for this reason. You can change the margin in Settings; lowering it is at your own risk.

### Meters or feet?

Tap **m** or **ft** at the top of the Plan tab. The FAA preset shows its limit as 400 ft and the EASA preset as 120 m whichever units you use. Values in feet are rounded to 5 ft. The 2 km free area limit reads 1.2 mi in feet.

### Does it work offline?

The two example sites always do. For your own sites, checks run from terrain tiles already cached on the phone. **Download for offline** (Pro) in the Sites tab fetches every terrain tile a site needs and keeps it. iOS can clear caches when storage is low; the Sites list shows whether a site is still available offline.

### I imported a KML or GPX file and the altitudes look off.

KML altitudes are treated as meters above takeoff unless the file marks them as absolute. GPX elevations are above sea level by definition and are converted using the ground height at your takeoff. If a file's altitudes come from a drone app that uses a different convention, set the plan altitude by hand instead.

### What does the Sun feature do?

Also Pro. It shows sun elevation through the day with the windows where the sun is between your chosen angles (useful for photogrammetry, which dislikes long shadows), and, for an inspection, warns when the sun will be in the camera's view of a facade. Choose the date at the top of the Sun sheet (it is saved with the site); times are in the site's local time. The four terrain checks do not depend on the date.

### Which drones does it support?

Any. DroneMap does not connect to the drone; it plans around the altitude conventions that all consumer drones share. There is no live telemetry, no weather and no airspace or no-fly-zone data in the app; use your usual apps for those.

### What is in Pro?

Areas larger than 2 km (1.2 mi) across, KML, KMZ and GPX import, PDF and KML export, unlimited saved sites, the Sun planner and offline site downloads. The four checks, the flight profile, the example sites, PNG sharing and three saved sites are free. Pro is a monthly or yearly subscription, or a one-time lifetime purchase; prices are shown in the app in your currency.

### How do I restore a purchase?

**Settings → Bought Pro before?** (or the same link at the bottom of the DroneMap Pro screen), signed in with the Apple Account that made the purchase. Subscriptions are managed in your Apple Account settings, not in the app.

### I deleted the example sites. Can I get them back?

Yes: **Settings → Bring back the example sites**.

---

## Credits

Terrain: Mapzen / AWS Open Data Terrain Tiles (SRTM, GMTED2010, ETOPO1, USGS NED and others). Maps: Apple Maps.
