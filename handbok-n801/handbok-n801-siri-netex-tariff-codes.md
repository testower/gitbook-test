# Håndbok N801 \(SIRI/NeTEX\) : Tariff codes

 **Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591736768 {padding: 0px;}  
div.rbtoc1619591736768 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591736768 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Simplified example](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-Simplifiedexample)
  * [Route pattern](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-Routepattern)
    * [Link](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-Link)
  * [PublicationDelivery](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-PublicationDelivery)
  * [Service Frame](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-ServiceFrame)
    * [Line](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-Line)
  * [Timetable Frame](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-TimetableFrame)
    * [ServiceJourney](handbok-n801-siri-netex-tariff-codes.md#Tariffcodes-ServiceJourney)

## Simplified example <a id="Tariffcodes-Simplifiedexample"></a>

This document describes a simplified example for specifying tariff codes/tariff per [Line](handbok-n801-siri-netex-network.md#network-Line) and/or [ServiceJourney](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney) using a key-value pair for tariff code.

Please note that the example, included in the XML file on GitHub \(see below\), is **only** meant to illustrate the concept and therefore lacks many data objects and references required to be a valid data submission in accordance with [Nordic NeTEx Profile](handbok-n801-siri-netex-nordic-netex-profile.md).

### Route pattern <a id="Tariffcodes-Routepattern"></a>

Same structure as in a normal submission of [Line](handbok-n801-siri-netex-network.md#network-Line), see [NeTEx examples catalogue](handbok-n801-siri-netex-netex-examples-catalogue.md).

#### Link <a id="Tariffcodes-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/fares/tariff-code.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/fares/tariff-code.xml)

### PublicationDelivery <a id="Tariffcodes-PublicationDelivery"></a>

Structured in the same way as a normal submission of [Line](handbok-n801-siri-netex-network.md#network-Line), see [NeTEx examples catalogue](handbok-n801-siri-netex-netex-examples-catalogue.md).

### Service Frame <a id="Tariffcodes-ServiceFrame"></a>

#### Line <a id="Tariffcodes-Line"></a>

To define a tariff code/tariff per [Line](handbok-n801-siri-netex-network.md#network-Line). They are defined in a **keyList** containing a **KeyValue** pair:

```text
<Line version="1" id="RUT:Line:1">
	<keyList>
		<KeyValue>
			<Key>Tariffkode</Key>
			<Value>Day_tariff</Value>
		</KeyValue>
	</keyList>
	<Name>Line-name</Name>
	<TransportMode>bus</TransportMode>
	<TransportSubmode>
		<BusSubmode>localBus</BusSubmode>
	</TransportSubmode>
	[...]
</Line>
```

### Timetable Frame <a id="Tariffcodes-TimetableFrame"></a>

#### ServiceJourney <a id="Tariffcodes-ServiceJourney"></a>

To define a tariff code/tariff per [ServiceJourney](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney) \(an individual departure\), define the codes in a **keyList** containing a **KeyValue** pair for each affected [_ServiceJourney_](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney):

```text
<ServiceJourney version="1" id="UNI:ServiceJourney:1">
	<keyList>
		<KeyValue>
			<Key>Tariffkode</Key>
			<Value>Night_tariff</Value>
		</KeyValue>
	</keyList>
	[...]
	<DepartureTime>00:00:00</DepartureTime>
	<passingTimes>
		<TimetabledPassingTime version="1" id="RUT:TimetabledPassingTime:1">
			<ArrivalTime>00:00:00</ArrivalTime>
		</TimetabledPassingTime>
	</passingTimes>
</ServiceJourney>
```

