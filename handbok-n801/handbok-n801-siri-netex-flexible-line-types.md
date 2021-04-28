# Håndbok N801 \(SIRI/NeTEX\) : Flexible Line Types

This document describes the different _flexibleLineTypes_ supported in the Nordic NeTEx profile. To avoid unnessesary complexity, only the most relevant flexibleLineTypes \(1-4\) are currently described. The remaining will be described as we progress with implementation of new usecases.

## **1. fixed**  <a id="FlexibleLineTypes-1.fixed"></a>

_Currently supported in Entur’s travel search._

_Fixed route with fixed times, operating only when pre-booked._

**Definition:** 

Fixed route with fixed times, stops, and direction. Similar to regular lines, but must be pre-booked by one or more passengers for it to run.

## **2. hailAndRideSections**  <a id="FlexibleLineTypes-2.hailAndRideSections"></a>

![](../.gitbook/assets/1236730036.png)

_Given a route with fixed stops, boarding and alighting is allowed at certain sections between stops._ 

**Definition:** 

A fixed route with fixed stops, but where boarding and alighting is allowed at certain sections between stops. Operation can be requested by signalling to the driver.

## **3. flexibleAreasOnly** <a id="FlexibleLineTypes-3.flexibleAreasOnly"></a>

_Currently supported in Entur’s travel search._

![](../.gitbook/assets/1228800486.png)

_Pickup and dropoff at any point within a defined area._

**Definition:** 

Pickup and dropoff can be booked for any given location within the defined area, at any time within the given operating times. The actual route that is operated is based on the bookings.

## **4. fixedStopAreaWide**  <a id="FlexibleLineTypes-4.fixedStopAreaWide"></a>

![](../.gitbook/assets/1236631691.png)

_Flexible route defined by one or more areas, where each area can have any number of predefined stops._ 

**Definition:**

The route consists of one or more areas containing one or more fixed stops. Passing times may be defined for both the areas and the stops. The order in which the stops are operated is based on the bookings.

## **5. mainRouteWithFlexibleEnds \(to be defined\)** <a id="FlexibleLineTypes-5.mainRouteWithFlexibleEnds(tobedefined)"></a>

## **6. corridorService \(to be defined\)** <a id="FlexibleLineTypes-6.corridorService(tobedefined)"></a>

## **7. mixedFlexible \(to be defined\)** <a id="FlexibleLineTypes-7.mixedFlexible(tobedefined)"></a>

## **8. mixedFlexibleAndFixed \(to be defined\)** <a id="FlexibleLineTypes-8.mixedFlexibleAndFixed(tobedefined)"></a>

