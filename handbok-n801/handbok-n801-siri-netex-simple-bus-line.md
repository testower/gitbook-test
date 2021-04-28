# Håndbok N801 \(SIRI/NeTEX\) : Simple bus line

**Innhold**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591716917 {padding: 0px;}  
div.rbtoc1619591716917 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591716917 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Line 109, Oslo](handbok-n801-siri-netex-simple-bus-line.md#Simplebusline-Line109,Oslo)
  * [Route pattern ](handbok-n801-siri-netex-simple-bus-line.md#Simplebusline-Routepattern)
    * [Link](handbok-n801-siri-netex-simple-bus-line.md#Simplebusline-Link)
  * [PublicationDelivery](handbok-n801-siri-netex-simple-bus-line.md#Simplebusline-PublicationDelivery)
  * [Service Frame](handbok-n801-siri-netex-simple-bus-line.md#Simplebusline-ServiceFrame)
    * [ServiceJourney](handbok-n801-siri-netex-simple-bus-line.md#Simplebusline-ServiceJourney)

## Line 109, Oslo <a id="Simplebusline-Line109,Oslo"></a>

According to the Norwegian NeTEx-profile, each [Line ](handbok-n801-siri-netex-network.md#network-Line)must be defined in its own separate XML-file.

### Route pattern  <a id="Simplebusline-Routepattern"></a>

Line 109 is an early morning bus service between Helsfyr and Holtet, partly as a supplement for the metro. It operates on all weekdays serving the following stops:

* Helsfyr T
* Brynseng T
* Høyenhall T
* Manglerud T
* Ryen T
* Holtet stasjon

There are three departures each morning, but times differ between weekdays and weekends. A [Line](handbok-n801-siri-netex-network.md#network-Line) with one [route](handbok-n801-siri-netex-network.md#network-Route) is modelled accordingly to the example for [Simple bus line with rhythm-based departure](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md)s, but [Timetable](handbok-n801-siri-netex-timetable.md) is modelled as an explicit [ServiceJourney](handbok-n801-siri-netex-timetable.md#timetable-timetable-ServiceJourney) for each departure.

#### Link <a id="Simplebusline-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/Full\_PublicationDelivery\_109\_Oslo\_morningbus\_example.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/Full_PublicationDelivery_109_Oslo_morningbus_example.xml)

### PublicationDelivery <a id="Simplebusline-PublicationDelivery"></a>

Because some data structures relevant to this example have already been covered in [Simple route - Bus \(rhythm based departures\)](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md) and [Projection](handbok-n801-siri-netex-projection.md), parts of the relevant structure have been omitted, and this example covers only the [ServiceJourney](handbok-n801-siri-netex-timetable.md#timetable-timetable-ServiceJourney) structure.

### Service Frame <a id="Simplebusline-ServiceFrame"></a>

#### ServiceJourney <a id="Simplebusline-ServiceJourney"></a>

Structuring of Passenger transport for a given day type is specified in this example as a set of [ServiceJourneys](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney) \(under [vehicleJourneys](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourney)\), which describe one trip each. Although the pattern could have been defined as a rhythm-based departure, ref. [Simple rhythm based bus line](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md), it may be easier to define each departure as a separate [ServiceJourney](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney). in cases where there are very few departures, or deviating journey patterns, or departure times.

The example below shows a departure operating on weekdays and Saturdays:

```text
<ServiceJourney version="any" id="UNI:sj:109:CODE-0530">
	<DepartureTime>05:30:00</DepartureTime>
	<dayTypes>
		<DayTypeRef ref="UNI:dt:weekday"/>
		<DayTypeRef ref="UNI:dt:saturday"/>
	</dayTypes>
	<JourneyPatternRef ref="UNI:JourneyPattern:109"/>
	<!-- Optional: -->
	<LineRef ref="UNI:line:109"/>
	<passingTimes>
		<TimetabledPassingTime>
			<!-- Helsfyr T -->
			<StopPointInJourneyPatternRef version="any" ref="UNI:StopPointInJourneyPattern:helfyr_t"/>
			<DepartureTime>05:30:00</DepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime>
			<!-- Brynseng T -->
			<StopPointInJourneyPatternRef version="any" ref="UNI:StopPointInJourneyPattern:brynseng_t"/>
			<DepartureTime>05:32:00</DepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime>
			<!-- Høyenhall T -->
			<StopPointInJourneyPatternRef version="any" ref="UNI:StopPointInJourneyPattern:hoyenhall_t"/>
			<DepartureTime>05:33:00</DepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime>
			<!-- Manglerud T -->
			<StopPointInJourneyPatternRef version="any" ref="UNI:StopPointInJourneyPattern:manglerud_t"/>
			<DepartureTime>05:34:00</DepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime>
			<!-- Ryen T -->
			<StopPointInJourneyPatternRef version="any" ref="UNI:StopPointInJourneyPattern:ryen_t"/>
			<DepartureTime>05:35:00</DepartureTime>
		</TimetabledPassingTime>
		<TimetabledPassingTime>
			<!-- Holtet -->
			<StopPointInJourneyPatternRef version="any" ref="UNI:StopPointInJourneyPattern:holtet"/>
			<ArrivalTime>05:40:00</ArrivalTime>
		</TimetabledPassingTime>
	</passingTimes>
</ServiceJourney>
```

