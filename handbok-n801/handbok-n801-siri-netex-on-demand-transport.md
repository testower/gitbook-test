# Håndbok N801 \(SIRI/NeTEX\) : On-demand transport

The concepts of flexible transportation are currently being reviewed and the examples and explanations in this document **may** become deprecated. Please contact Entur for more information.

## Content <a id="On-demandtransport-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591706270 {padding: 0px;}  
div.rbtoc1619591706270 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591706270 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Content](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Content)
* [Examples](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Examples)
  * [Line 316, Lørenskog: Flexible zones and fixed stop places](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Line316,Lørenskog:Flexiblezonesandfixedstopplaces)
    * [Description of the line](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Descriptionoftheline)
      * [Modelling](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Modelling)
      * [Link](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Link)
    * [Elements](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Elements)
      * [FlexibleStopPlace](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleStopPlace)
      * [Route](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Route)
        * [routePoints](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-routePoints)
        * [routes](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-routes)
      * [FlexibleLine](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleLine)
        * [FlexibleLine](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleLine.1)
      * [stopAssignments](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-stopAssignments)
        * [stopAssignments](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-stopAssignments.1)
        * [StopPointInJourneyPattern](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-StopPointInJourneyPattern)
      * [Timetable](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Timetable)
        * [ServiceJourney](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-ServiceJourney)
  * [On-demand transport in an area without fixed locations](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-On-demandtransportinanareawithoutfixedlocations)
    * [Description](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Description)
      * [Modelling](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Modelling.1)
      * [Link](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Link.1)
    * [Elements](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Elements.1)
      * [Route](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Route.1)
        * [routePoints](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-routePoints.1)
        * [routes](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-routes.1)
      * [stopAssignments](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-stopAssignments.2)
        * [scheduledStopPoint](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-scheduledStopPoint)
        * [stopAssignments](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-stopAssignments.3)
      * [JourneyPattern](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-JourneyPattern)
      * [Timetable](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Timetable.1)
        * [ServiceJourney](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-ServiceJourney.1)
  * [Line 517, Drøbak: Hail & Ride](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Line517,Drøbak:Hail&Ride)
    * [Description](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Description.1)
      * [Modelling](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Modelling.2)
      * [Link](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Link.2)
    * [Elements](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Elements.2)
      * [FlexibleStopPlace](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleStopPlace.1)
        * [FlexibleStopPlace](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleStopPlace.2)
      * [FlexibleLine](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleLine.2)
        * [FlexibleLine](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleLine.3)
      * [Route](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Route.2)
      * [serviceLinks](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-serviceLinks)
        * [ServiceLink](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-ServiceLink)
      * [stopAssignments](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-stopAssignments.4)
        * [PassengerStopAssignment](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-PassengerStopAssignment)
        * [FlexibleStopAssignment](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleStopAssignment)
      * [JourneyPattern](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-JourneyPattern.1)
        * [JourneyPattern](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-JourneyPattern.2)
      * [Timetable](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-Timetable.2)

On-demand transport is based on bookings, requests or hails are made by the passenger, and may operate outside the bounds of regular stop places. This may include door to door services or servicing remote stops.

According to the Norwegian NeTEx-profile, each [Line](handbok-n801-siri-netex-network.md#network-Line) must be defined in its own separate XML-file.

On-demand transport, **however**, must be sent as [FlexibleLine](handbok-n801-siri-netex-network.md#network-FlexibleLine) \(with corresponding relevant _FlexibleLineType_\).

Several variations of on-demand transport are more closely described in [Flexible Transport](handbok-n801-siri-netex-network.md#network-FlexibleTransport) and in the official whitepaper "_Representing flexible networks and multimodality in NeTEx_" \([http://netex-cen.eu/wp-content/uploads/2015/12/07.NeTEx-Flexible-Network-and-Multimodality-WhitePaper\_1.06.pdf](http://netex-cen.eu/wp-content/uploads/2015/12/07.NeTEx-Flexible-Network-and-Multimodality-WhitePaper_1.06.pdf)\)

## Examples <a id="On-demandtransport-Examples"></a>

### Line 316, Lørenskog: Flexible zones and fixed stop places <a id="On-demandtransport-Line316,L&#xF8;renskog:Flexiblezonesandfixedstopplaces"></a>

#### Description of the line <a id="On-demandtransport-Descriptionoftheline"></a>

Line 316 is an on-demand line which operates between certain pre-defined stops and an area without fixed stops on the north side of the railroad around Lørenskog; "Øvre Grønlia", "Hanaborglia, "Fridjof Nansens vei" and "Steinbekkveien". 

The line links up with \(guaranteed interchange\):

• Train at "Hanaborg station" departing for Lillestrøm and Oslo.  
• Line 100 departing for Lillestrøm and Oslo at "Lørenskog sentrum".

The journey must be booked by phone prior to 12:00 on the day _before_ the departure. The exact place of pick-up is agreed upon when booking the journey. Once the passenger has been picked up, the departure proceeds via Hanaborg station \(to link up with trains\), then continues to the bus station "Lørenskog sentrum" to connect with bus line 100, before arriving at its final destination "Triaden" \(a shopping mall\). The Line then makes a return journey, serving the same sequence of stops \(in reverse\), before again dropping passengers off at pre-booked locations inside the FlexibleArea.

**Modelling**

In NeTEx such services are usually modelled by defining a StopPlace as a [FlexibleArea](handbok-n801-siri-netex-stops.md#stops-FlexibleArea), a defined area where pick-up or drop-off is possible when a journey has been booked in advance. In this particular example, the Line picks up passengers in an area, and drops them off at a static stop places, which are always served, regardless of booking. In cases where on-demand transport is **part** of a regular Line, it is modelled just like a regular stop place in a journey pattern.  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy1609912805220670730",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563901&pageId=&name=FlexibleStopPlace-and-StopPlace&attachmentId=att642744380&pagePin=&imageAttachmentId=att642810017&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=1&previewPageId=637370387&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy1609912805220670730&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIxZWM1NDI4ODc5OWMzOWFkYjkxYjVjZjg3MDI2NGFmMWYxOTVmMzAxNDgxYzE3ZWVlMjk5NmQzYWE3ZjUwMmFmIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg4NiwiaWF0IjoxNjE5NTkxNzA2fQ.aYz3gvOnpCPMWAe3tPLf\_2BPQiDWUXyfhVsYEb5xYcg",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYjFkMGU4MTUtZmM3MC00YjhiLThhMzItNWZiZWRhZjBiZWI0IiwiaWQiOiJiMWQwZTgxNS1mYzcwLTRiOGItOGEzMi01ZmJlZGFmMGJlYjQifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxOCIsImlkIjoiNzI4NTYzOTAxIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjA2LCJpYXQiOjE2MTk1OTE3MDZ9.eBd6sGP4cFZpGxfb1WSvCILyKW7BtTBFFXQen6YjcgM",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"b1d0e815-fc70-4b8b-8a32-5fbedaf0beb4\",\"id\":\"b1d0e815-fc70-4b8b-8a32-5fbedaf0beb4\"},\"content\":{\"type\":\"page\",\"version\":\"18\",\"id\":\"728563901\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563901\",\"macro.hash\":\"b1d0e815-fc70-4b8b-8a32-5fbedaf0beb4\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"18\",\"page.title\":\"On-demand transport\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att642810017\|baseUrl=https://enturas.atlassian.net/wiki\|name=FlexibleStopPlace-and-StopPlace\|migration=1\|diagramAttachmentId=att642744380\|containerId=637370387\|timestamp=1535708161905\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"18\",\"imageAttachmentId\":\"att642810017\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728563901\",\"name\":\"FlexibleStopPlace-and-StopPlace\",\"migration\":\"1\",\"macro.id\":\"b1d0e815-fc70-4b8b-8a32-5fbedaf0beb4\",\"diagramAttachmentId\":\"att642744380\",\"containerId\":\"637370387\",\"timestamp\":\"1535708161905\"}",  
    "timeZone":"Europe/Berlin",  
    "origin":"https://confluence-connect.gliffy.net",  
    "hostOrigin":"https://enturas.atlassian.net",  
    "sandbox":"allow-downloads allow-forms allow-modals allow-popups allow-scripts allow-same-origin allow-top-navigation-by-user-activation allow-storage-access-by-user-activation",    "pearApp":"true",        "apiMigrations": {  
        "gdpr": true  
    }  
}  
;  
    if\(window.AP && window.AP.subCreate\) {  
      window.\_AP.appendConnectAddon\(data\);  
    } else {  
      require\(\['ac/create'\], function\(create\){  
        create.appendConnectAddon\(data\);  
      }\);  
    }  
  }\(\)\);  


**Link**

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-316-with-interchange.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-316-with-interchange.xml)

#### Elements <a id="On-demandtransport-Elements"></a>

Several elements of on-demand transport are more closely described in the [Simple route - Bus \(rhythm based departure\)](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md) example, and will not be repeated in this example. Because line 316 has guaranteed interchanges with trains, and buses, this example models both on-demand transport and interchanges to other Lines. A detailed description of interchange \([Connection](handbok-n801-siri-netex-network.md#network-Connection)/[Interchange](handbok-n801-siri-netex-timetable.md#timetable-Interchange)\) can be found in the [Multimodal interchange](handbok-n801-siri-netex-multimodal-interchanges.md) example.

**FlexibleStopPlace**

Please note that when sending in on-demand transport lines, [flexibleStopPlaces](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace) must be included in the Line file.

In [SiteFrame]() the pick-up area needs to be specified and described as a [FlexibleStopPlace](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace) with one [FlexibleArea](handbok-n801-siri-netex-stops.md#stops-FlexibleArea). This specifies the area where pick-up and/or drop-off is possible. The area can, for example, be used to extract a list of bookable addresses.

```text
<FlexibleStopPlace version="any" id="NHR:FlexibleStopPlace:CODE-HANABORG-NORD">
	<Name>Flexible pick-up zone for Line 316</Name>
	<Description>
		On demand service for the areas north of the rail road tracks in Lørenskog; 
		Øvre Grønlia, Hanaborglia, Fridjof Nansens vei and Steinbekkveien 
		without fixed pattern.
	</Description>
	<TransportMode>bus</TransportMode>
	<areas>
		<FlexibleArea version="any" id="NHR:FlexibleArea:CODE-HANABORG-NORD-AREA">
			<gml:Polygon srsName="wgs84" gml:id="hanaborg">
				<gml:exterior>
					<gml:LinearRing>
						<gml:pos>59.938831 10.966611</gml:pos>
						<gml:pos>59.943369 10.952606</gml:pos>
						<gml:pos>59.944642 10.962742</gml:pos>
						<gml:pos>59.950631 10.984097</gml:pos>
						<gml:pos>59.945957 10.989036</gml:pos>
						<gml:pos>59.940764 10.981718</gml:pos>
					</gml:LinearRing>
				</gml:exterior>
			</gml:Polygon>
		</FlexibleArea>
	</areas>
</FlexibleStopPlace>
```

**Route**

The Line is described by points which define the routes' pattern. The distinguishing feature of this type of line is that the flexible stop area is described with a [RoutePoint](handbok-n801-siri-netex-network.md#network-RoutePoint), where the route-"point" is a reference to a [FlexibleArea](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleStopPlace).

**routePoints**

```text
<routePoints>
	<!-- Flexible-zone Hanaborg north-->
	<RoutePoint version="any" id="RUT:RoutePoint:ID-HANABORG-NORD">
		<projections>
			<ZoneProjection version="any" id="NHR:ZoneProjection:CODE-HANABORG-NORD-ZONE">
				<ProjectedZoneRef ref="NHR:FlexibleArea:CODE-HANABORG-NORD-AREA"/>
			</ZoneProjection>
		</projections>
	</RoutePoint>
	<!-- Hanaborg stasjon -->
	<RoutePoint version="any" id="RUT:RoutePoint:ID-HANABORG">
		<projections>
			<PointProjection version="any" id="RUT:PointProjection:ID-HANABORG">
				<ProjectedPointRef version="any" ref="NHR:StopPlace:CODE-HANABORG_ST"/>
			</PointProjection>
		</projections>
	</RoutePoint>
	[...]
</routePoints>
```

Thus, the flexible area constitutes the first \(and, in opposite direction, the last\) part of the route, while the rest consists of regular stops.

**routes**

```text
<routes>
	<Route version="any" id="RUT:Route:316:TilLorenskog">
		<Name>316 to Lørenskog center</Name>
		<DirectionRef version="any" ref="NHR:Direction:TilLorenskog"/>
		<pointsInSequence>
			<PointOnRoute version="any" id="RUT:PointOnRoute:ID-HANABORG-NORD-HENTING" order="1">
				<RoutePointRef version="any" ref="RUT:RoutePoint:ID-HANABORG-NORD"/>
			</PointOnRoute>
			<PointOnRoute version="any" id="RUT:PointOnRoute:ID-HANABORG-TIL" order="2">
				<RoutePointRef version="any" ref="RUT:RoutePoint:ID-HANABORG"/>
			</PointOnRoute>
			<PointOnRoute version="any" id="RUT:PointOnRoute:ID-LORENSKOGSENTRUM-TIL" order="3">
				<RoutePointRef version="any" ref="RUT:RoutePoint:ID-LORENSKOGSENTRUM"/>
			</PointOnRoute>
			<PointOnRoute version="any" id="RUT:PointOnRoute:ID-TRIADEN-TIL" order="4">
				<RoutePointRef version="any" ref="RUT:RoutePoint:ID-TRIADEN"/>
			</PointOnRoute>
		</pointsInSequence>
		<InverseRouteRef ref="RUT:Route:316:FraLorenskog"/>
	</Route>
	[...]
</routes>
```

The opposite direction of the route is described the same way with one _InverseRouteRef_ pointing back to the route pattern in the opposite direction. 

**FlexibleLine**

The line is modelled as a [FlexibleLine](handbok-n801-siri-netex-network.md#network-FlexibleLine) with information about transport type and booking.

**FlexibleLine**

```text
<FlexibleLine version="any" id="RUT:FlexibleLine:316">
	<Name>Bestillingslinje 316: Øvre Grønlia - Hanaborg - Lørenskog center</Name>
	<TransportMode>bus</TransportMode>
	<TransportSubmode>
		<BusSubmode>shuttleBus</BusSubmode>
	</TransportSubmode>
	<PublicCode>316</PublicCode>
	<OperatorRef ref="RUT:Company:Unibuss"/>
	<routes>
		<RouteRef version="any" ref="RUT:Route:316:TilLorenskog"/>
		<RouteRef version="any" ref="RUT:Route:316:FraLorenskog"/>
	</routes>
	<FlexibleLineType>mixedFlexibleAndFixed</FlexibleLineType>
	<BookingContact>
		<Phone>04144</Phone>
	</BookingContact>
	<BookingMethods>callOffice</BookingMethods>
	<BookWhen>untilPreviousDay</BookWhen>
	<LatestBookingTime>12:00:00</LatestBookingTime>
	<BookingNote>
		How to order transport with line 316:
		Order transport by phone 04144 before 12 O'clock the former weekday.
		Taxes are as for ordinary buses, and Ruters card and tickets apply.
		If you have access to internet you can read more about order of transport at ruter.no.
	</BookingNote>
</FlexibleLine>
```

**stopAssignments**

Furthermore, the flexible stop area is linked to a [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) through a [FlexibleStopAssignment](handbok-n801-siri-netex-network.md#network-FlexibleStopAssignment). 

**stopAssignments**

```text
<stopAssignments>
	<FlexibleStopAssignment version="any" id="RUT:PassengerStopAssignment:CODE-HANABORG">
		<ScheduledStopPointRef version="any" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST-NORD"/>
		<FlexibleStopPlaceRef version="any" ref="NHR:FlexibleStopPlace:CODE-HANABORG-NORD"/>
	</FlexibleStopAssignment>
	<PassengerStopAssignment version="any" order="0" id="RUT:PassengerStopAssignment:CODE-HANABORG">
		<ScheduledStopPointRef version="any" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST"/>
		<StopPlaceRef version="any" ref="NHR:StopPlace:CODE-HANABORG_ST"/>
		<QuayRef version="any" ref="NHR:Quay:CODE-HANABORG_ST-QUAY"/>
	</PassengerStopAssignment>
	[...]
</stopAssignments>
```

This means the flexible stop area is added to the [JourneyPattern ](handbok-n801-siri-netex-network.md#network-JourneyPattern)in the same way, a normal stop place would:

**StopPointInJourneyPattern**

```text
<!-- Flexi-sone -->
<StopPointInJourneyPattern version="any" id="RUT:StopPointInJourneyPattern:ID-HANABORG-NORD:TilLorenskog" order="1">
	<ScheduledStopPointRef version="any" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST-NORD"/>
	<ForAlighting>false</ForAlighting>
	<DestinationDisplayRef ref="RUT:DestinationDisplay:Triaden"/>
</StopPointInJourneyPattern>
```

**Timetable**

The timetable must specify the earliest possible departure time \(_EarliestDepartureTime_\) and the latest possible arrival time \(_LatestArrivalTime_\), even though they may vary- or have to be estimated based on provisions for how the line is operated. 

Additional information relevant for the passenger should appear in the line's [bookingNote](handbok-n801-siri-netex-network.md#network-FlexibleLine) and/or its [notices]().

**ServiceJourney**

```text
<ServiceJourney version="any" id="RUT:ServiceJourney:0316:TilLorenskog">
	<dayTypes>
		<DayTypeRef version="any" ref="RUT:DayType:weekdays"/>
	</dayTypes>
	<JourneyPatternRef ref="RUT:JourneyPattern:316:TilLorenskog"/>
	<passingTimes>
		<TimetabledPassingTime>
			<!-- Flexible zone (time and place arranged when booking is made) -->
			<StopPointInJourneyPatternRef ref="RUT:StopPointInJourneyPattern:ID-HANABORG-NORD:TilLorenskog" version="any"/>
			<DepartureTime>10:10:00</DepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime>
			<StopPointInJourneyPatternRef ref="RUT:StopPointInJourneyPattern:ID-HANABORG_ST:TilLorenskog" version="any"/>
			<ArrivalTime>10:15:00</ArrivalTime>
		</TimetabledPassingTime>
		[...]
	</passingTimes>
</ServiceJourney>
```

###  On-demand transport in an area without fixed locations <a id="On-demandtransport-On-demandtransportinanareawithoutfixedlocations"></a>

#### Description <a id="On-demandtransport-Description"></a>

A line may also operate without fixed stop locations within a single specified area. This is usually a door to door service.

This example illustrates such transport in the Grønlia/northern Hanaborg area.

**Modelling**

NeTEx is modelled in the usual way with a [FlexibleArea](handbok-n801-siri-netex-stops.md#stops-FlexibleArea) which constitutes a [FlexibleStopPlace](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace), and the transport is modelled as a journey between two points within the flexible area.  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy2702704246967727197",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563901&pageId=&name=FlexiblePlace&attachmentId=att637372528&pagePin=&imageAttachmentId=att637372525&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370387&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy2702704246967727197&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI3ZTM3ZWE5YTkwYWQzZjgwMjMwNjg2ZjI1NGVlZmM4ODM3OGU2YzVjYzI0OTNhMmQ2Yzc1MzJiZWI2MzQzMmIzIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg4NiwiaWF0IjoxNjE5NTkxNzA2fQ.5L1p-nvoSL\_tjVXppkdDwl9tsjIpIf1LPOdPQdPbKyU",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiNzQ1NjNmYjEtYjI3MC00Mjc0LWI4MGItZWU2NTgwYzhjZmFhIiwiaWQiOiI3NDU2M2ZiMS1iMjcwLTQyNzQtYjgwYi1lZTY1ODBjOGNmYWEifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxOCIsImlkIjoiNzI4NTYzOTAxIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjA2LCJpYXQiOjE2MTk1OTE3MDZ9.kAqvURPCfZ5tVQz7\_OTI6-OgB5Kd18b1aeAp4-AZkCo",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"74563fb1-b270-4274-b80b-ee6580c8cfaa\",\"id\":\"74563fb1-b270-4274-b80b-ee6580c8cfaa\"},\"content\":{\"type\":\"page\",\"version\":\"18\",\"id\":\"728563901\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563901\",\"macro.hash\":\"74563fb1-b270-4274-b80b-ee6580c8cfaa\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"18\",\"page.title\":\"On-demand transport\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372525\|baseUrl=https://enturas.atlassian.net/wiki\|name=FlexiblePlace\|diagramAttachmentId=att637372528\|containerId=637370387\|timestamp=1535708210207\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"18\",\"imageAttachmentId\":\"att637372525\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728563901\",\"name\":\"FlexiblePlace\",\"macro.id\":\"74563fb1-b270-4274-b80b-ee6580c8cfaa\",\"diagramAttachmentId\":\"att637372528\",\"containerId\":\"637370387\",\"timestamp\":\"1535708210207\"}",  
    "timeZone":"Europe/Berlin",  
    "origin":"https://confluence-connect.gliffy.net",  
    "hostOrigin":"https://enturas.atlassian.net",  
    "sandbox":"allow-downloads allow-forms allow-modals allow-popups allow-scripts allow-same-origin allow-top-navigation-by-user-activation allow-storage-access-by-user-activation",    "pearApp":"true",        "apiMigrations": {  
        "gdpr": true  
    }  
}  
;  
    if\(window.AP && window.AP.subCreate\) {  
      window.\_AP.appendConnectAddon\(data\);  
    } else {  
      require\(\['ac/create'\], function\(create\){  
        create.appendConnectAddon\(data\);  
      }\);  
    }  
  }\(\)\);  


The area where it is possible to book transport constitutes the entire route area and has no fixed patterns.

**Link**

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-within-single-FlexibleArea.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-within-single-FlexibleArea.xml)

#### Elements <a id="On-demandtransport-Elements.1"></a>

Most elements usually included below have already been described elsewhere and will be skipped in the following examples. 

**Route**

The route consists of two points in the same area, i.e. implicitly between two arbitrary points within the same [FlexibleArea](handbok-n801-siri-netex-on-demand-transport.md#On-demandtransport-FlexibleStopPlace).

**routePoints**

```text
<routePoints>
	<!-- Flexible zone Northern Hanaborg -->
	<RoutePoint version="1" id="RUT:RoutePoint:ID-HANABORG-NORD">
		<projections>
			<PointProjection version="1" id="RUT:PointProjection:ID-HANABORG_ST-NORD">
				<ProjectToPointRef version="1" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST-NORD"/>
			</PointProjection>
		</projections>
	</RoutePoint>
</routePoints>
```

**routes**

```text
<routes>
	<Route version="1" id="RUT:Route:1-HanaborgNord">
		<Name>Northern Hanaborg</Name>
		<FlexibleLineRef ref="RUT:FlexibleLine:1" version="1"/>
		<DirectionType>inbound</DirectionType>
		<pointsInSequence>
			<PointOnRoute version="1" id="RUT:PointOnRoute:ID-HANABORG-NORD-fra" order="1">
				<RoutePointRef version="1" ref="RUT:RoutePoint:ID-HANABORG-NORD"/>
			</PointOnRoute>
			<PointOnRoute version="1" id="RUT:PointOnRoute:ID-HANABORG-NORD-til" order="2">
				<RoutePointRef version="1" ref="RUT:RoutePoint:ID-HANABORG-NORD"/>
			</PointOnRoute>
		</pointsInSequence>
	</Route>
</routes>
```

**stopAssignments**

Because the same [FlexibleArea](handbok-n801-siri-netex-stops.md#stops-FlexibleArea) is used for both start and end, only one [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) is associated with the area through a [FlexibleStopAssignment](handbok-n801-siri-netex-network.md#network-FlexibleStopAssignment).

**scheduledStopPoint**

```text
<scheduledStopPoints>
	<ScheduledStopPoint version="1" id="RUT:ScheduledStopPoint:ID-HANABORG_ST-NORD">
		<Name>Fleksi-sone Hanaborg nord</Name>
	</ScheduledStopPoint>
</scheduledStopPoints>
```

**stopAssignments**

```text
<stopAssignments>
	<FlexibleStopAssignment version="1" id="RUT:FlexibleStopAssignment:ID-HANABORG">
		<ScheduledStopPointRef version="1" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST-NORD"/>
		<FlexibleStopPlaceRef version="1" ref="RUT:FlexibleStopPlace:ID-HANABORG-NORD"/>
	</FlexibleStopAssignment>
</stopAssignments>
```

**JourneyPattern**

The above examples form a [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern), with the same [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) for start and end, so that the pattern becomes two arbitrary stops within the same flexible area. 

```text
<JourneyPattern version="1" id="RUT:JourneyPattern:1-HanaborgNord">
	<Name>Hanaborg nord</Name>
	<RouteRef version="1" ref="RUT:Route:1-HanaborgNord"/>
	<pointsInSequence>
		<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:ID-HANABORG-NORD-fra" order="1">
			<ScheduledStopPointRef version="1" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST-NORD"/>
			<ForAlighting>false</ForAlighting>
			<DestinationDisplayRef version="1" ref="RUT:DestinationDisplay:Hanaborg"/>
		</StopPointInJourneyPattern>
		<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:ID-HANABORG-NORD-til" order="2">
			<ScheduledStopPointRef version="1" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST-NORD"/>
			<ForBoarding>false</ForBoarding>
		</StopPointInJourneyPattern>
	</pointsInSequence>
</JourneyPattern>
```

Note that disembarkation is not allowed on the first stop, and boarding is not allowed on the last stop.

**Timetable**

Rules for ordering are the same as illustrated in the previous example.

The timetable specifies the earliest possible time for pick up, as well as the latest possible time for drop off:

**ServiceJourney**

```text
<ServiceJourney version="1" id="RUT:ServiceJourney:01-HanaborgNord">
	<dayTypes>
		<DayTypeRef version="1" ref="RUT:DayType:weekdays"/>
	</dayTypes>
	<JourneyPatternRef version="1" ref="RUT:JourneyPattern:1-HanaborgNord"/>
	<FlexibleLineRef version="1" ref="RUT:FlexibleLine:1"/>
	<passingTimes>
		<TimetabledPassingTime version="1" id="RUT:TimetabledPassingTime:1000">
			<!-- Flexi-sone (time and place arranged when booking is made) -->
			<StopPointInJourneyPatternRef ref="RUT:StopPointInJourneyPattern:ID-HANABORG-NORD-fra" version="1"/>
			<EarliestDepartureTime>08:00:00</EarliestDepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime version="1" id="RUT:TimetabledPassingTime:1001">
			<!-- Flexi-sone (time and place arranged when booking is made) -->
			<StopPointInJourneyPatternRef ref="RUT:StopPointInJourneyPattern:ID-HANABORG-NORD-til" version="1"/>
			<LatestArrivalTime>16:00:00</LatestArrivalTime>
		</TimetabledPassingTime>
	</passingTimes>
</ServiceJourney>
```

###  Line 517, Drøbak: Hail & Ride <a id="On-demandtransport-Line517,Dr&#xF8;bak:Hail&amp;Ride"></a>

#### Description <a id="On-demandtransport-Description.1"></a>

Line 517 is a Hail & Ride line which follows a fixed route with fixed stop times, but along specified segments of the journey pattern, the vehicle can be hailed at any location, independent of regular stops.

**Modelling**

In NeTEx this type of route is modelled by defining one or more [FlexibleStopPlacces](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace) of the type [HailAndRideArea](handbok-n801-siri-netex-stops.md#stops-HailAndRideArea) between the two [ScheduledStopPoints](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) where one may "wave down" a public transport vehicle.  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy550478572511630118",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563901&pageId=&name=HailAndRide&attachmentId=att642678866&pagePin=&imageAttachmentId=att642514997&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=1&previewPageId=637370387&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy550478572511630118&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIwODQ5NDM3NmM3MWJhOTllOTdhMDVlNjAxNTQ0NTdmYTkyMDNjMDY0MTcwMjM3ZTU4NWE3NTgwY2E2Mjk2ZmM4IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg4NiwiaWF0IjoxNjE5NTkxNzA2fQ.sGlsDxTAS0Gk0H8bFoQ9wy753g3b9uBCV4Yj5CjHIUk",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiMWU4NjFhODQtOWE4YS00ZTllLWIxYTYtNjA0MGU3MjZhM2ZmIiwiaWQiOiIxZTg2MWE4NC05YThhLTRlOWUtYjFhNi02MDQwZTcyNmEzZmYifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxOCIsImlkIjoiNzI4NTYzOTAxIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjA2LCJpYXQiOjE2MTk1OTE3MDZ9.rO40v-DaRnudjm8hZQ0nhTTbF8cstDpAsb3jk-ITFco",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"1e861a84-9a8a-4e9e-b1a6-6040e726a3ff\",\"id\":\"1e861a84-9a8a-4e9e-b1a6-6040e726a3ff\"},\"content\":{\"type\":\"page\",\"version\":\"18\",\"id\":\"728563901\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563901\",\"macro.hash\":\"1e861a84-9a8a-4e9e-b1a6-6040e726a3ff\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"18\",\"page.title\":\"On-demand transport\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att642514997\|baseUrl=https://enturas.atlassian.net/wiki\|name=HailAndRide\|migration=1\|diagramAttachmentId=att642678866\|containerId=637370387\|timestamp=1535708366019\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"18\",\"imageAttachmentId\":\"att642514997\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728563901\",\"name\":\"HailAndRide\",\"migration\":\"1\",\"macro.id\":\"1e861a84-9a8a-4e9e-b1a6-6040e726a3ff\",\"diagramAttachmentId\":\"att642678866\",\"containerId\":\"637370387\",\"timestamp\":\"1535708366019\"}",  
    "timeZone":"Europe/Berlin",  
    "origin":"https://confluence-connect.gliffy.net",  
    "hostOrigin":"https://enturas.atlassian.net",  
    "sandbox":"allow-downloads allow-forms allow-modals allow-popups allow-scripts allow-same-origin allow-top-navigation-by-user-activation allow-storage-access-by-user-activation",    "pearApp":"true",        "apiMigrations": {  
        "gdpr": true  
    }  
}  
;  
    if\(window.AP && window.AP.subCreate\) {  
      window.\_AP.appendConnectAddon\(data\);  
    } else {  
      require\(\['ac/create'\], function\(create\){  
        create.appendConnectAddon\(data\);  
      }\);  
    }  
  }\(\)\);  


Each [StopPlace](handbok-n801-siri-netex-stops.md#stops-StopPlace) is served as usual, and the segment between them is the Hail & Ride area. Please note that in the model this technically isn't a geometric _area_, but rather a geometric line traversed by the vehicle \(i.e. a road\).

**Link**

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/network/Hail-and-ride-Ruter-507.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Hail-and-ride-Ruter-507.xml)

#### Elements <a id="On-demandtransport-Elements.2"></a>

Many of the basic elements are described in more detail in the examples above, and in the example for [Simple route - Bus \(rhythm based departure\)](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md), and have been omitted from this example.

**FlexibleStopPlace**

Note that for "Order for transport" has to send in [flexibleStopPlaces](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace) in the line file.

In [SiteFrame]() areas are specified where pick-up or drop off is allowed outside normal stop places. Each "zone" is described as a [FlexibleStopPlace](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace) with one [HailAndRideArea](handbok-n801-siri-netex-stops.md#stops-HailAndRideArea) between two [ScheduledStopPoints](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint).

**FlexibleStopPlace**

```text
<FlexibleStopPlace id="RUT:FlexibleStopPlace:1" version="1">
	<Name>Between Elleveien and Vestbyveien</Name>
	<areas>
		<HailAndRideArea id="RUT:HailAndRideArea:1" version="1">
			<Name>Fleksibel påstigning mellom Elle og Ullerud</Name>
			<StartPointRef ref="RUT:ScheduledStopPoint:1" version="1"/>
			<EndPointRef ref="RUT:ScheduledStopPoint:2" version="1"/>
		</HailAndRideArea>
	</areas>
</FlexibleStopPlace>
```

**FlexibleLine**

The line must be modelled as a [FlexibleLine](handbok-n801-siri-netex-network.md#network-FlexibleLine) of type "hailAndRideSections".

**FlexibleLine**

```text
<FlexibleLine version="any" id="RUT:FlexibleLine:316">
	<Name>Bestillingslinje 316: Øvre Grønlia - Hanaborg - Lørenskog sentrum</Name>
	<TransportMode>bus</TransportMode>
	<TransportSubmode>
		<BusSubmode>shuttleBus</BusSubmode>
	</TransportSubmode>
	<PublicCode>316</PublicCode>
	<OperatorRef ref="RUT:Company:Unibuss"/>
	<routes>
		<RouteRef version="any" ref="RUT:Route:316:TilLorenskog"/>
		<RouteRef version="any" ref="RUT:Route:316:FraLorenskog"/>
	</routes>
	<FlexibleLineType>mixedFlexibleAndFixed</FlexibleLineType>
	<BookingContact>
		<Phone>04144</Phone>
	</BookingContact>
	<BookingMethods>callOffice</BookingMethods>
	<BookWhen>untilPreviousDay</BookWhen>
	<LatestBookingTime>12:00:00</LatestBookingTime>
	<BookingNote>
		Book transport by calling 04144 before 12:00 the previous weekday.
		Fares are the same as on regular bus lines. Read more on ruter.no.
	</BookingNote>
</FlexibleLine>
```

**Route**

Modelled in the usual way, with a [RoutePoint](handbok-n801-siri-netex-network.md#network-RoutePo) for prominent [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint).

**serviceLinks**

A Hail & Ride-rout requires [ServiceLinks](handbok-n801-siri-netex-network.md#network-ServiceLink) for all legs in the [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern). Furthermore, [LinkSequenceProjection]() for geographical indication of all legs where Hail & Ride is allowed is required.

**ServiceLink**

```text
<!-- Elleveien - Vestbyveien (hail&ride) -->
<ServiceLink id="RUT:ServiceLink:1" version="1">
	<Distance>1200</Distance>
	<projections>
		<LinkSequenceProjection id="RUT:LinkSequenceProjection:1" version="1">
			<gml:LineString srsName="WGS84" gml:id="Elleveien-Vestbyveien">
				<gml:pos>59.648480 10.637532</gml:pos>
				<gml:pos>59.649806 10.636470</gml:pos>
				<gml:pos>59.651631 10.636789</gml:pos>
				<gml:pos>59.652667 10.637289</gml:pos>
			</gml:LineString>
		</LinkSequenceProjection>
	</projections>
	<FromPointRef ref="RUT:ScheduledStopPoint:1" version="1"/>
	<ToPointRef ref="RUT:ScheduledStopPoint:2" version="1"/>
</ServiceLink>>
```

**stopAssignments**

A regular [StopPlace](handbok-n801-siri-netex-stops.md#stops-StopPlace) connects to [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) through a [FlexibleStopAssignment](handbok-n801-siri-netex-network.md#network-FlexibleStopAssignment). 

**PassengerStopAssignment**

```text
<!-- Elleveien -->
<PassengerStopAssignment id="RUT:PassengerStopAssignment:1" version="1" order="1">
	<ScheduledStopPointRef ref="RUT:ScheduledStopPoint:1" version="1"/>
	<StopPlaceRef ref="NSR:StopPlace:5485"/>
	<QuayRef ref="NSR:Quay:10035"/>
</PassengerStopAssignment>
```

 [HailAndRideArea](handbok-n801-siri-netex-stops.md#stops-HailAndRideArea) connects to [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) through a [FlexibleStopAssignment](handbok-n801-siri-netex-network.md#network-FlexibleStopAssignment). 

**FlexibleStopAssignment**

```text
<!-- Flexible section Elleveien - Vestbyveien -->
<FlexibleStopAssignment id="RUT:FlexibleStopAssignment:1" version="1">
	<ScheduledStopPointRef ref="RUT:ScheduledStopPoint:11" version="1"/>
	<FlexibleStopPlaceRef ref="RUT:FlexibleStopPlace:1" version="1"/>
</FlexibleStopAssignment>
```

**JourneyPattern**

[JourneyPattern](handbok-n801-siri-netex-network.md#network-Journey) is defined with [StopPointInJourneyPattern](handbok-n801-siri-netex-network.md#network-StopPointInJourneyPattern) for **all** stops that are served, i.e. both fixed stops and hail & ride areas, **and** with [ServiceLinks](handbok-n801-siri-netex-network.md#network-ServiceLink) for all legs.

Remember to specify boarding- and alighting rules.

**JourneyPattern**

```text
<JourneyPattern id="RUT:JourneyPattern:507-inbound" version="1">
	<Name>507 Elle - Dyrløkke</Name>
	<RouteRef ref="RUT:Route:507-inbound" version="1"/>
	<pointsInSequence>
		<!-- Elleveien (fixed) -->
		<StopPointInJourneyPattern id="RUT:StopPointInJourneyPattern:1" version="1" order="1">
			<ScheduledStopPointRef ref="RUT:ScheduledStopPoint:1" version="1"/>
			<ForAlighting>false</ForAlighting>
			<ForBoarding>true</ForBoarding>
			<DestinationDisplayRef ref="RUT:DestinationDisplay:1" version="1"/>
		</StopPointInJourneyPattern>
		<!-- Elleveien - Vestbyveien (hail&ride) -->
		<StopPointInJourneyPattern id="RUT:StopPointInJourneyPattern:2" version="1" order="2">
			<ScheduledStopPointRef ref="RUT:ScheduledStopPoint:11" version="1"/>
			<ForAlighting>false</ForAlighting>
			<ForBoarding>true</ForBoarding>
		</StopPointInJourneyPattern>
		[...]
	</pointsInSequence>
	<linksInSequence>
		<!-- Elleveien - Vestbyveien (hail&ride) -->
		<ServiceLinkInJourneyPattern id="RUT:ServiceLinkInJourneyPattern:1" version="1" order="1">
			<ServiceLinkRef ref="RUT:ServiceLink:1" version="1"/>
		</ServiceLinkInJourneyPattern>
		[...]
		<!-- Ullerudsletta - Dyrløkke -->
		<ServiceLinkInJourneyPattern id="RUT:ServiceLinkInJourneyPattern:5" version="1" order="5">
			<ServiceLinkRef ref="RUT:ServiceLink:5" version="1"/>
		</ServiceLinkInJourneyPattern>
	</linksInSequence>
</JourneyPattern>
```

**Timetable**

The timetable should specify the earliest possible departure time \(_EarliestDepartureTime_\) and the latest possible arrival time \(_LatestArrivalTime_\) per Hail & Ride area.

Other provisions may be specified in [FlexibleServiceProperties](handbok-n801-siri-netex-network.md#network-FlexibleServiceProperties) or [notices]().

