# Håndbok N801 \(SIRI/NeTEX\) : Simple rhythm based bus line

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591717023 {padding: 0px;}  
div.rbtoc1619591717023 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591717023 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Line 61A, Oslo](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Line61A,Oslo)
  * [Description of the line](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Descriptionoftheline)
    * [Link](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Link)
  * [PublicationDelivery](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-PublicationDelivery)
    * [Frameset](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Frameset)
  * [CompositeFrame](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-CompositeFrame)
    * [Codespace](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Codespace)
  * [ResourceFrame](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-ResourceFrame)
    * [Organisation](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Organisation)
      * [organisations](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-organisations)
    * [Site Frame](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-SiteFrame)
      * [SiteFrame](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-SiteFrame.1)
  * [Service Frame](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-ServiceFrame)
    * [General concepts](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Generalconcepts)
      * [Network](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Network)
      * [Line](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Line)
      * [Direction](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Direction)
      * [DestinationDisplay](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-DestinationDisplay)
        * [Network \| Line \| Direction \| Destination](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Network%7CLine%7CDirection%7CDestination)
    * [Route](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Route)
      * [routePoints](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-routePoints)
      * [routes](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-routes)
    * [ScheduledStopPoints](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-ScheduledStopPoints)
      * [StopAssignments](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-StopAssignments)
        * [StopAssignment](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-StopAssignment)
    * [JourneyPattern](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-JourneyPattern)
    * [Notice](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Notice)
      * [Service Calendar Frame](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-ServiceCalendarFrame)
    * [ServiceCalendar](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-ServiceCalendar)
    * [DayTypes](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-DayTypes)
    * [Timeband](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Timeband)
  * [Timetable Frame](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-TimetableFrame)
    * [Validity ](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-Validity)
      * [validityConditions](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-validityConditions)
    * [Vehicle Journeys](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-VehicleJourneys)

## Line 61A, Oslo <a id="Simplerhythmbasedbusline-Line61A,Oslo"></a>

According to the Norwegian NeTEx-profile, each [Line](handbok-n801-siri-netex-network.md#network-Line) must be defined in its own separate XML-file.

### Description of the line <a id="Simplerhythmbasedbusline-Descriptionoftheline"></a>

Line 61A is a circular bus line passing the following stops:

* Tveita T
* Tveita bedriftsområde
* Solfjellet
* Larsbråten
* Tveita bedriftsområde
* Tveita
* Tveita T

Departures are fixed to leave 15 minutes past every whole hour between 0915 and 1415, Monday through Saturday. The [Line](handbok-n801-siri-netex-network.md#network-Line) is modelled with a [Route](handbok-n801-siri-netex-network.md#network-Route), where [Timetable](handbok-n801-siri-netex-timetable.md) is modelled as [Periodical Journeys](handbok-n801-siri-netex-timetable.md#timetable-Periodicaljourneys) \(TemplateServiceJourney\) based on [RhythmicalJourneyGroup](handbok-n801-siri-netex-timetable.md#timetable-RhythmicalJourneyGroup).

#### Link <a id="Simplerhythmbasedbusline-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml)

### PublicationDelivery <a id="Simplerhythmbasedbusline-PublicationDelivery"></a>

Defines the contents of the submitted file 

**Frameset**

```text
<?xml version="1.0" encoding="UTF-8"?>
<PublicationDelivery 
    version="1.0" 
    xmlns="http://www.netex.org.uk/netex" 
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://www.netex.org.uk/netex ../../xsd/NeTEx_publication.xsd">
    [...]
    <dataObjects>
        <CompositeFrame version="1" created="2015-12-13T00:00:00Z" id="RUT:Norway:CompositeFrame:0061">
            [...]
            <frames>
                <ResourceFrame version="any" id="RUT:ResourceFrame:RF1"> 
                [...]
                </ResourceFrame>
                
                <SiteFrame version="any" id="RUT:SiteFrame:SF01">
                [...]
                </SiteFrame>
                
                <ServiceFrame version="any" id="RUT:ServiceFrame:0061">
                [...]
                </ServiceFrame>
                
                <ServiceCalendarFrame version="any" id="RUT:ServiceCalendarFrame:SCF01">
                [...]
                </ServiceCalendarFrame>
                
                <TimetableFrame version="any" id="RUT:TimetableFrame:TF02">
                [...]
                </TimetableFrame>
            </frames>
        </CompositeFrame>
    </dataObjects>
</PublicationDelivery>
```

Below is a more detailed description of the most important elements that **must** be included in the data transfer to Entur:

### CompositeFrame <a id="Simplerhythmbasedbusline-CompositeFrame"></a>

This Frame is used to group \("wrap"\) frames with data, and define ownership of the dataset in the submission's codespace. This describes the "namespace" - Xmlns - \(cf. Administration code\), which defines the submitter of the dataset.

Each operator, as well as other authorities, has its own unique namespace, allocated by Entur.

#### Codespace <a id="Simplerhythmbasedbusline-Codespace"></a>

```text
<codespaces>
    <!-- Codespace for Ruter -->
    <Codespace id="ruter">
        <Xmlns>RUT</Xmlns>
        <XmlnsUrl>http://www.ruter.no/</XmlnsUrl>
    </Codespace>
    <!-- Codespace for national stop place registry-->
    <Codespace id="nhr">
        <Xmlns>NHR</Xmlns>
        <XmlnsUrl>http://stoppested.entur.org</XmlnsUrl>
    </Codespace>
</codespaces>
```

### ResourceFrame <a id="Simplerhythmbasedbusline-ResourceFrame"></a>

#### Organisation <a id="Simplerhythmbasedbusline-Organisation"></a>

**organisations**

```text
<organisations>
	<!-- Owner of line -->
    <Authority version="1" id="RUT:Company:0">
        <CompanyNumber>991609407</CompanyNumber>
        <!-- Organisasjonsnummer -->
        <Name>Ruter</Name>
        <LegalName>RUTER AS</LegalName>
        <OrganisationType>authority</OrganisationType>
    </Authority>
    <!-- Operator of line -->
    <Operator version="1" id="RUT:Company:1">
        <CompanyNumber>985615616</CompanyNumber>
        <Name>Unibuss</Name>
        <LegalName>UNIBUSS AS</LegalName>
        <CustomerServiceContactDetails>
            <Phone>0047 177</Phone>
            <Url>http://www.ruter.no</Url>
            <FurtherDetails>Kontaktskjema på websider</FurtherDetails>
        </CustomerServiceContactDetails>
    </Operator>
</organisations>
```

#### Site Frame <a id="Simplerhythmbasedbusline-SiteFrame"></a>

Description of a stop place can be found in more detail under [Stop place - Simple](handbok-n801-siri-netex-stopplace-simple.md). Other files should only contain simplified references to the stop places with IDs from the stop place registry. 

**SiteFrame**

```text
<SiteFrame version="any" id="RUT:SiteFrame:SF01">
    <stopPlaces>
        <!-- The stops have been given ficticious ID's -->
        <StopPlace version="1" id="NHR:StopArea:03011537">
            <Name>Larsbr&#229;ten</Name>
            <quays>
                <Quay version="1" id="NHR:StopArea:0301153701"/>
            </quays>
        </StopPlace>
        <StopPlace version="1" id="NHR:StopArea:03011525">
            <Name>Tveita bedriftsomr&#229;de</Name>
            <quays>
                <Quay version="1" id="NHR:StopArea:0301152501"/>
                <Quay version="1" id="NHR:StopArea:0301152502"/>
            </quays>
        </StopPlace>
        <StopPlace version="1" id="NHR:StopArea:03011536">
            <Name>Solfjellet</Name>
            <quays>
                <Quay version="1" id="NHR:StopArea:0301153601"/>
            </quays>
        </StopPlace>
        <StopPlace version="1" id="NHR:StopArea:03011522">
            <Name>Tveita</Name>
            <quays>
                <Quay version="1" id="NHR:StopArea:0301152202"/>
            </quays>
        </StopPlace>
        <StopPlace version="1" id="NHR:StopArea:03011521">
            <Name>Tveita T</Name>
            <quays>
                <Quay version="1" id="NHR:StopArea:0301152101"/>
                <Quay version="1" id="NHR:StopArea:0301152102"/>
            </quays>
        </StopPlace>
    </stopPlaces>
</SiteFrame>
```

### Service Frame <a id="Simplerhythmbasedbusline-ServiceFrame"></a>

Defines data for a Route, such as Networks, Lines stops, etc.

#### General concepts <a id="Simplerhythmbasedbusline-Generalconcepts"></a>

**Network**

* Lines under a common "umbrella", e.g. the bus lines owned by Ruter.

**Line**

* A group of Routes known by the same marketed name, e.g. Metro Line 2.

**Direction**

* Defines the direction of a line. Line 61A is a clockwise roundtrip.

**DestinationDisplay**

* Specifies the destination information for the Line \(commonly matching the text displayed on the front of the bus\).

**Network \| Line \| Direction \| Destination**

```text
<Network version="1" changed="2015-12-13T00:00:00Z" id="RUT:GroupOfLine:RuterBuss">
    <Name>Ruter</Name>
</Network>
[...]
<Line version="any" id="RUT:Line:0061">
    <Name>Tveita Solfjellet</Name>
    <TransportMode>bus</TransportMode>
    <PublicCode>61A</PublicCode>
    <routes>
        <!-- The line has no return direction, as it is circular -->
        <RouteRef version="1" ref="RUT:Route:0061101"/>
    </routes>
</Line>
[...]
<Direction version="any" id="RUT:Route:0061101:Direction">
    <Name>Round trip</Name>
    <DirectionType>clockwise</DirectionType>
</Direction>
[...]
<destinationDisplays>
    <DestinationDisplay version="any" id="RUT:DestinationDisplay:DST_Solfjellet">
        <FrontText>Solfjellet</FrontText>
    </DestinationDisplay>
    <DestinationDisplay version="any" id="RUT:DestinationDisplay:DST_TveitaT">
        <FrontText>Tveita T</FrontText>
    </DestinationDisplay>
</destinationDisplays>
```

#### Route <a id="Simplerhythmbasedbusline-Route"></a>

**routePoints**

All route points are listed as references to StopPoints.

Even if you have multiple routes, all route points must be defined in the same routePoints block. The route points are subsequently used to define the routes. As shown in the next section, the references are specified as a sequential list of the RoutePoints used in each Route.

```text
<routePoints>
	<!-- Tveita T -->
	<RoutePoint version="1" id="RUT:RoutePoint:0061101A0A0061101001">
		<projections>
			<PointProjection version="any" id="RUT:PointProjection:0061101A0A0061101001">
				<ProjectedPointRef version="1" ref="RUT:StopPoint:0061101001"/>
			</PointProjection>
		</projections>
	</RoutePoint>
	<!-- Solfjellet -->
	<RoutePoint version="1" id="RUT:RoutePoint:0061101A2A0061101003">
		<projections>
			<PointProjection version="any" id="RUT:PointProjection:0061101A2A0061101003">
				<ProjectedPointRef version="1" ref="RUT:StopPoint:0061101003"/>
			</PointProjection>
		</projections>
	</RoutePoint>
[...]
</routePoints>
```

**routes**

Line 61A is a circular route and has no reverse pattern.

A Route always consists of a sequence of [PointOnRoute](handbok-n801-siri-netex-network.md#network-PointOnRoute), referring to the already defined [RoutePoints](handbok-n801-siri-netex-network.md#network-RoutePoint) mentioned above. 

```text
<routes>
	<Route version="1" id="RUT:Route:0061101">
		<Name>Tveita - Solfjellet - Larsbråten - Tveita</Name>
		<LineRef ref="RUT:Line:0061"/>
		<DirectionRef version="any" ref="RUT:Route:0061101:Direction"/>
		<pointsInSequence>
			<PointOnRoute version="any" id="RUT:PointOnRoute:0061101001-0">
				<RoutePointRef version="1" ref="RUT:RoutePoint:0061101A0A0061101001"/>
			</PointOnRoute>
			<PointOnRoute version="any" id="RUT:PointOnRoute:0061101003-2">
				<RoutePointRef version="1" ref="RUT:RoutePoint:0061101A2A0061101003"/>
			</PointOnRoute>
			<PointOnRoute version="any" id="RUT:PointOnRoute:0061101004-3">
				<RoutePointRef version="1" ref="RUT:RoutePoint:0061101A3A0061101004"/>
			</PointOnRoute>
			<PointOnRoute version="any" id="RUT:PointOnRoute:0061101007-6">
				<RoutePointRef version="1" ref="RUT:RoutePoint:0061101A6A0061101007"/>
			</PointOnRoute>
		</pointsInSequence>
	</Route>
</routes>
```

#### ScheduledStopPoints <a id="Simplerhythmbasedbusline-ScheduledStopPoints"></a>

Each stop served by Line 61A must be defined as a [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) in order to be used as a [StopPoint in a JourneyPattern](handbok-n801-siri-netex-network.md#network-StopPointInJourneyPattern).

```text
<scheduledStopPoints>
	<ScheduledStopPoint version="1" id="RUT:StopPoint:0061101001">
		<Name>Tveita T</Name>
	</ScheduledStopPoint>
	<ScheduledStopPoint version="1" id="RUT:StopPoint:0061101002">
		<Name>Tveita bedriftsområde</Name>
	</ScheduledStopPoint>
	<ScheduledStopPoint version="1" id="RUT:StopPoint:0061101003">
		<Name>Solfjellet</Name>
	</ScheduledStopPoint>
	<ScheduledStopPoint version="1" id="RUT:StopPoint:0061101004">
		<Name>Larsbråten</Name>
	</ScheduledStopPoint>
	<ScheduledStopPoint version="1" id="RUT:StopPoint:0061101005">
		<Name>Tveita bedriftsområde</Name>
	</ScheduledStopPoint>
	<ScheduledStopPoint version="1" id="RUT:StopPoint:0061101006">
		<Name>Tveita</Name>
	</ScheduledStopPoint>
	<ScheduledStopPoint version="1" id="RUT:StopPoint:0061101007">
		<Name>Tveita T</Name>
	</ScheduledStopPoint>
</scheduledStopPoints>
```

**StopAssignments**

Linking of a ScheduledStopPoint to a defined [StopPlace](handbok-n801-siri-netex-stops.md#stops-StopPlace)/[Quay](handbok-n801-siri-netex-stops.md#stops-Quay) is done through a PassengerStopAssignment. \(_All StopPlaces and Quays belong to the NSR codespace._\)

**StopAssignment**

```text
<stopAssignments>
	<PassengerStopAssignment version="any" order="1" id="RUT:PassengerStopAssignment:0061101001">
		<!-- Hvilket ScheduledStopPoint som mappes til ... -->
		<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101001"/>
		<!-- .. hvilket stopPlace ... og hvis mulig -->
		<StopPlaceRef version="1" ref="NSR:StopPlace:03011521"/>
		<!-- hvilken quay kjøretøyet stopper ved -->
		<QuayRef version="1" ref="NSR:Quay:0301152101"/>
	</PassengerStopAssignment>
	<PassengerStopAssignment version="any" order="2" id="RUT:PassengerStopAssignment:0061101002">
		<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101002"/>
		<StopPlaceRef version="1" ref="NSR:StopPlace:03011525"/>
		<QuayRef version="1" ref="NSR:Quay:0301152501"/>
	</PassengerStopAssignment>
	<PassengerStopAssignment version="any" order="3" id="RUT:PassengerStopAssignment:0061101003">
		<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101003"/>
		<StopPlaceRef version="1" ref="NSR:StopPlace:03011536"/>
		<QuayRef version="1" ref="NSR:Quay:0301153601"/>
	</PassengerStopAssignment>
	<PassengerStopAssignment version="any" order="4" id="RUT:PassengerStopAssignment:0061101004">
		<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101004"/>
		<StopPlaceRef version="1" ref="NSR:StopPlace:03011537"/>
		<QuayRef version="1" ref="NSR:Quay:0301153701"/>
	</PassengerStopAssignment>
	<PassengerStopAssignment version="any" order="5" id="RUT:PassengerStopAssignment:0061101005">
		<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101005"/>
		<StopPlaceRef version="1" ref="NSR:StopPlace:03011525"/>
		<QuayRef version="1" ref="NSR:Quay:0301152502"/>
	</PassengerStopAssignment>
	<PassengerStopAssignment version="any" order="6" id="RUT:PassengerStopAssignment:0061101006">
		<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101006"/>
		<StopPlaceRef version="1" ref="NSR:StopPlace:03011522"/>
		<QuayRef version="1" ref="NSR:Quay:0301152202"/>
	</PassengerStopAssignment>
	<PassengerStopAssignment version="any" order="7" id="RUT:PassengerStopAssignment:0061101007">
		<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101007"/>
		<StopPlaceRef version="1" ref="NSR:StopPlace:03011521"/>
		<QuayRef version="1" ref="NSR:Quay:0301152102"/>
	</PassengerStopAssignment>
</stopAssignments>
```

#### JourneyPattern <a id="Simplerhythmbasedbusline-JourneyPattern"></a>

The line's pattern \(unique sequence of stops\) is defined as a [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern). For the circular line 61A, there is only one pattern.

```text
<journeyPatterns>
	<JourneyPattern version="1" id="RUT:JourneyPattern:0061101">
		<Name>Tveita T</Name>
		<RouteRef version="1" ref="RUT:Route:0061101"/>
		<!-- The sequential list of stops -->
		<pointsInSequence>
			<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:0061101001" order="1">
				<!-- Referanse til hvilket ScheduledStopPoint -->
				<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101001"/>
				<ForAlighting>false</ForAlighting>
				<!-- Destinasjonstekst som vises på bussen -->
				<DestinationDisplayRef ref="RUT:DestinationDisplay:DST_Solfjellet"/>
			</StopPointInJourneyPattern>
			<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:0061101002" order="2">
				<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101002"/>
			</StopPointInJourneyPattern>
			<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:0061101003" order="3">
				<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101003"/>
				<!-- Her endrer teksten på bussen seg fra Solfjellet til Tveita T -->
				<DestinationDisplayRef ref="RUT:DestinationDisplay:DST_TveitaT"/>
			</StopPointInJourneyPattern>
			<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:0061101004" order="4">
				<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101004"/>
			</StopPointInJourneyPattern>
			<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:0061101005" order="5">
				<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101005"/>
			</StopPointInJourneyPattern>
			<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:0061101006" order="6">
				<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101006"/>
			</StopPointInJourneyPattern>
			<StopPointInJourneyPattern version="1" id="RUT:StopPointInJourneyPattern:0061101007" order="7">
				<ScheduledStopPointRef version="1" ref="RUT:StopPoint:0061101007"/>
				<ForBoarding>false</ForBoarding>
			</StopPointInJourneyPattern>
		</pointsInSequence>
	</JourneyPattern>
</journeyPatterns>
```

#### Notice <a id="Simplerhythmbasedbusline-Notice"></a>

Notices \(Free text fields, sometimes referred to as footnotes\) referring to the entire Line, are modelled in the ServiceFrame.

_Specific_ [_noticeAssignmens_]() _for a JourneyPattern is specified/referenced under PointInJourneyPattern and correspondingly for a VehicleJourney under Call._

```text
<notices>
	<Notice version="any" id="RUT:Notice:1">
		<Text>On residential roads, bus 61A can make additional stops besides the regular stops. Remember to hail the vehicle!</Text>
	</Notice>
</notices>
```

**Service Calendar Frame**

Defines data for time, days, periods, and other calendar items.

#### ServiceCalendar <a id="Simplerhythmbasedbusline-ServiceCalendar"></a>

Because line 61A follows the same departure pattern every day, an example has been created with a [ServiceCalendar](handbok-n801-siri-netex-timetable.md#timetable-ServiceCalendar), containing a relevant description of day and time. 

If more calendars are needed, the time objects can be defined externally, in the ServiceCalendarFrame itself, and be reused by referencing them in different ServiceCalendars.

#### DayTypes <a id="Simplerhythmbasedbusline-DayTypes"></a>

Description of day\(s\) with a set of properties, for example, which weekdays the dayType applies to.

```text
<dayTypes>
	<!-- Daytype indicates all weekdays and Saturday -->
	<DayType version="any" id="RUT:DayType:MonSat">
		<Name>Weekdays and Saturdays</Name>
		<properties>
			<PropertyOfDay>
				<DaysOfWeek>Monday Tuesday Wednesday Thursday Friday Saturday</DaysOfWeek>
			</PropertyOfDay>
		</properties>
	</DayType>
</dayTypes>
```

#### Timeband <a id="Simplerhythmbasedbusline-Timeband"></a>

Specifies time. In the context of a [Frequency Group](handbok-n801-siri-netex-timetable.md#timetable-JourneyFrequencyGroup) \(in the example, a [RhythmicalJourneyGroup](handbok-n801-siri-netex-timetable.md#timetable-RhythmicalJourneyGroup)\), &lt;StartTime&gt; is defined as "00" to describe how many _minutes over each full hour_ there are departures. Multiple departures within each hour are indicated by a Timeband for each departure.

```text
<Timeband version="any" id="RUT:Timeband:TM15">
	<!--Name>15 minutes past the hour</Name-->
	<StartTime>00:15:00</StartTime>
	<EndTime>00:15:00</EndTime>
</Timeband>
```

### Timetable Frame <a id="Simplerhythmbasedbusline-TimetableFrame"></a>

Defines data for scheduled departures, stops, and arrivals for a given trip \([Journey](handbok-n801-siri-netex-timetable.md#timetable-Journey)\) on a given date.

#### Validity  <a id="Simplerhythmbasedbusline-Validity"></a>

Validity period for the timetable is indicated by [AvailabilityCondition]().

**validityConditions**

```text
<validityConditions>
	<ValidBetween>
		<FromDate>2016-01-10T00:00:00</FromDate>
		<ToDate>2016-12-20T00:00:00</ToDate>
	</ValidBetween>
</validityConditions>
```

#### Vehicle Journeys <a id="Simplerhythmbasedbusline-VehicleJourneys"></a>

A specific trip with passengers for a given day type can be specified in the following ways:

* [TemplateServiceJourney ](handbok-n801-siri-netex-timetable.md#timetable-TemplateServiceJourney)describes ServiceJourneys in a recurring pattern for a given period
* A set of [ServiceJourneys, ](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney)each describing an individual trip

For a line like 61A, which has a recurring departure time \([Simple route - Bus \(rhythm based departure\)\#Timeband](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370384#Enkelrute-Buss%28rytmebasertavgang%29-Timeband)\) and follows the same route \(pattern\) every day, a TemplateServiceJourney with a [RhythmicalJourneyGroup](handbok-n801-siri-netex-timetable.md#timetable-RhythmicalJourneyGroup) describing the departure pattern can be used.

```text
<TemplateServiceJourney version="any" id="RUT:TemplateServiceJourney:0061">
	<dayTypes>
		<!-- Refers to one daytype which specifies Monday-Friday. Could also have been separate daytypes, but then all of these must be included here -->
		<DayTypeRef version="any" ref="RUT:DayType:MonSat"/>
	</dayTypes>
	<!-- Reference to the journeyPattern to be used for trips with passengers on board -->
	<JourneyPatternRef version="any" ref="RUT:JourneyPattern:0061101"/>
	<!-- Hvilken linje det gjelder (optional) -->
	<LineRef version="any" ref="RUT:Line:0061"/>
	<passingTimes>
		<TimetabledPassingTime>
			<!-- Tveita T -->
			<StopPointInJourneyPatternRef ref="RUT:StopPointInJourneyPattern:0061101001"/>
			<DepartureTime>00:15:00</DepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime>
			<!-- Tveita bedriftsområde -->
			<StopPointInJourneyPatternRef ref="RUT:StopPointInJourneyPattern:0061101002"/>
			<DepartureTime>00:17:00</DepartureTime>
		</TimetabledPassingTime>
[...]
		<TimetabledPassingTime>
			<!-- Tveita -->
			<StopPointInJourneyPatternRef ref="RUT:StopPointInJourneyPattern:0061101007"/>
			<ArrivalTime>00:31:00</ArrivalTime>
		</TimetabledPassingTime>
	</passingTimes>
	<frequencyGroups>
		<RhythmicalJourneyGroup version="any" id="RUT:RhythmicalJourneyGroup:1">
			<Name>Every hour, 15 minutes past the hour</Name>
			<!-- Første avgang er kl 09:15 -->
			<FirstDepartureTime>09:15:00</FirstDepartureTime>
			<!-- Siste avgang er kl 14:15 -->
			<LastDepartureTime>14:15:00</LastDepartureTime>
			<timebands>
				<!-- Every 15 minutes past the hour -->
				<TimebandRef version="any" ref="RUT:Timeband:TM15"/>
			</timebands>
		</RhythmicalJourneyGroup>
	</frequencyGroups>
</TemplateServiceJourney>
```

