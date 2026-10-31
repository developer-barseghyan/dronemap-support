---
layout: default
title: DroneMap Help
permalink: /
dm_section: help
---

# DroneMap help

**DroneMap: Terrain & RTH Check** tests a drone flight plan against the shape of the ground. You set a takeoff point, outline the area and type two heights from your drone app: the flight altitude and the Return-to-Home altitude. The app then marks each spot where that plan runs into terrain.

All the math happens on your iPhone. You do not sign up for anything, and your saved sites stay on the device.

Questions and bug reports go to [developer.barseghyan@gmail.com](mailto:developer.barseghyan@gmail.com).

## What the elevation model leaves out

> The ground data is a bare-earth model with one height sample roughly every 30 m. Its heights can be off by several meters, and by more on steep slopes.
>
> It has **no buildings, trees, towers or power lines**. A green result only says the modeled ground sits below your plan by at least your margin.
>
> You remain the pilot in command. Fly within sight, leave your drone's own warnings switched on, and obey the local rules.

## Plan a flight in four steps

1. **Try a sample site.** The Sites tab holds two samples from Utah. In **Castle Valley**, a 50 m (165 ft) RTH would hit the canyon wall on the return leg. The **Bonneville Salt Flats** sample passes every check. Neither sample needs a network connection.
2. **Set the takeoff and the area.** On the Plan tab, tap **Takeoff here** or press and hold on the map. Then tap the map to drop corners, or pick **Circle**. The card at the bottom names the next step.
3. **Type two heights.** Enter the flight altitude and the RTH altitude. Both count from takeoff, just as your controller displays them.
4. **Tap Check.** The result list opens on the most urgent item. Tap a row to show its map layer. Tap **Profile** for a cross-section.

## Takeoff height versus ground height

Your controller reports height above the takeoff point. It does not know the ground under the aircraft. Say you launch in a valley and cross a ridge that stands 100 m higher. With 120 m on the screen, only 20 m of air separates the drone from that ridge. DroneMap turns takeoff-based heights into true height over the ground across your whole area.

## The four checks

### Terrain

Red and amber cells show where the planned altitude is below the modeled ground or inside your safety margin. The default margin is 30 m. The result also names the altitude that clears the whole area. The return line appears on this layer too.

### Safe RTH

On Return-to-Home, the drone climbs to its RTH altitude and heads straight back at that height. DroneMap follows that straight path from every point in the area. It reports the lowest RTH altitude that stays above terrain on all of them. The map marks the point that sets this number and draws its return line. Use that value or a higher one in your drone app.

### Legal AGL

Rules cap the height above the ground beneath the drone: 400 ft under the FAA and 120 m under EASA. When the ground drops away, a takeoff-based altitude that started legal can go over the cap. The map shows where this happens. You also get the band of altitudes that is legal and clear everywhere. When no such band exists, the app tells you.

### Line of sight

From your standing spot plus antenna height, the app marks which parts of the area hide behind terrain at the planned altitude. It accounts for Earth curvature and for the radio Fresnel zone at 2.4 or 5.8 GHz. It also suggests a nearby spot with a wider view and says how much more of the area you would see from there.

### The large number above the list

This is the first thing to fix. When the plan hits ground, it is the lowest safe flight altitude. When only the return leg is the issue, it is the lowest safe RTH altitude. When the legal cap is the issue, it is the legal band. **SHORTFALL** tells you how far your entry sits below that minimum. **CLEARANCE** tells you how far above it you are.

### The side view

The **Profile** chart cuts along one line from takeoff. It draws the ground, your flight and RTH heights, your margin and the legal cap. By default the line runs toward the point behind the selected check. Tap **Move far point** and drag that end anywhere inside the area. Slide a finger over the chart to read ground height and clearance. The vertical scale is stretched so the terrain is easy to see, and the stretch factor sits in a corner of the chart. The profile is part of the free app.

## Editing and saving sites

- Drag a corner to move it.
- Drag the small dot halfway along an edge to insert a new corner there.
- Tap a corner, then use **Delete corner** or **Undo** on the card.
- A circle has a center and an edge handle, and you can drag both. The takeoff and operator pins move the same way.
- Tap the map to shrink the card. Tap the card or its arrow to expand it again.
- **Save** stores the plan and its latest result in the Sites tab, or overwrites the site you opened. It does not recompute. Any edit recomputes by itself.
- To refresh a stored site for today's date, swipe right on it in the Sites list.
- Removed the samples by accident? Open **Settings** and tap **Bring back the example sites**.

## Accuracy and gaps in the data

Grid and error
: Samples lie about 30 m apart. For 90% of land, the height error stays under 16 m. In open country it is usually 5 to 10 m. Narrow valleys and steep faces fare worse. That is the reason for the 30 m default margin. You can change it in Settings, but a smaller margin is your own risk.

Trees and buildings
: The model comes from a radar survey of bare earth. Thick forest and big structures show up only in part. Single trees, towers and cables are absent. Add your own buffer for them.

Cells marked "No data"
: A terrain tile failed to download for those cells. DroneMap never fills them with a guess. Run the check again once you have signal. With Pro, you can also store the site for offline use before you lose coverage.

## Units, offline use and imported files

- Switch between **m** and **ft** at the top of the Plan tab. The FAA cap always reads 400 ft and the EASA cap reads 120 m. Feet are rounded to the nearest 5. The free 2 km area limit reads 1.2 mi.
- Both samples open offline at any time. Your own sites use terrain tiles the phone has already cached.
- With Pro, **Download for offline** in the Sites tab stores every tile a site needs. iOS may purge caches when space runs low. The Sites list shows whether a site can still open offline.
- KML heights count as meters above takeoff unless the file flags them as absolute. GPX elevations are always above sea level. DroneMap converts them using the ground height at takeoff.
- Some drone apps write files with a different height convention. If imported heights look odd, type the altitude by hand.

## Drones, weather and airspace

DroneMap works with any drone because it never links to one. It plans around the takeoff-based altitude that consumer drones have in common. There is no live telemetry, no weather, and no airspace or no-fly-zone layer. Keep your usual apps for those.

## Free features and DroneMap Pro

Free for everyone: all four checks, the profile, both samples, PNG sharing and up to three saved sites.

Pro adds:

- **Sun planner.** It shows the hours when the sun sits between two heights you pick, which helps photogrammetry flights avoid long shadows. For inspections, it warns when the sun will face the camera at a facade. Pick the date at the top of the Sun sheet. The date is stored with the site, and times use the site's local time zone. The terrain checks ignore the date.
- KML, KMZ and GPX import.
- A PDF report and KML export.
- Offline site downloads.
- Areas wider than 2 km (1.2 mi).
- As many saved sites as you like.

US pricing: $4.99 per month, $29.99 per year with a free first week, or $59.99 once for lifetime access. Before you pay, the app shows the price in your local currency.

On a new phone, open **Settings** and tap **Bought Pro before?** while signed in with the Apple Account that paid. The same link sits at the foot of the DroneMap Pro screen. Subscriptions are managed in your Apple Account settings, not inside DroneMap.

## Reporting a result that seems off

Email me and attach:

1. The site as a **PDF** or **KML** export (Pro), or a screenshot showing the map and the result rows.
2. The takeoff coordinates, the two heights you typed, and your margin.
3. The result you expected and your source for it, such as a topo map, a flight log or a photo.

Three causes come up most often. The elevation data may have a gap or smoothing, so tight gorges and sharp summits can be tens of meters off. The takeoff pin may sit on a slope a few meters from where you really stood. Or an imported file may carry sea-level heights instead of takeoff-based ones.

## Data sources

Elevation: AWS Open Data Terrain Tiles, the Mapzen merge of SRTM, GMTED2010, ETOPO1, USGS NED and other public sources. Map: Apple Maps.
