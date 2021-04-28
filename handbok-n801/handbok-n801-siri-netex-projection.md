# Håndbok N801 \(SIRI/NeTEX\) : Projection

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591717233 {padding: 0px;}  
div.rbtoc1619591717233 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591717233 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Geographical location indications \(for Line 109, Oslo\)](handbok-n801-siri-netex-projection.md#Projection-Geographicallocationindications%28forLine109,Oslo%29)
  * [JourneyPattern](handbok-n801-siri-netex-projection.md#Projection-JourneyPattern)
    * [Link](handbok-n801-siri-netex-projection.md#Projection-Link)
  * [PublicationDelivery](handbok-n801-siri-netex-projection.md#Projection-PublicationDelivery)
  * [Service Frame](handbok-n801-siri-netex-projection.md#Projection-ServiceFrame)
    * [serviceLinks](handbok-n801-siri-netex-projection.md#Projection-serviceLinks)
    * [linksInSequence](handbok-n801-siri-netex-projection.md#Projection-linksInSequence)

## Geographical location indications \(for Line 109, Oslo\) <a id="Projection-Geographicallocationindications(forLine109,Oslo)"></a>

### JourneyPattern <a id="Projection-JourneyPattern"></a>

A [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern) can be defined as [pointsInSequence](handbok-n801-siri-netex-network.md#network-PointInJourneyPattern) \(a sorted list of points, detailed in [other examples](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md#Simplerhythmbasedbusline-JourneyPattern)\) and/or [linksInSequence](handbok-n801-siri-netex-network.md#network-LinkInJourneyPattern) \(a sorted list of links between two points\).

According to [Nordic NeTEx Profile](handbok-n801-siri-netex-nordic-netex-profile.md), the actual route must be defined as at the highest possible level in the XML structure, and in most cases, it is recommended that this be done as a set of [Projeksjon\#serviceLinks](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370383#Projeksjon-serviceLinks) with [Link]() [projections]() describing the points it follows. These should unambiguously describe the path using sufficient GML coordinates \(gml:pos\) so that [the line's](handbok-n801-siri-netex-network.md#network-Line)  [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern) is correctly displayed on maps.

In some cases \(e.g. air routes\), this may be done using the line's [RoutePoints](handbok-n801-siri-netex-network.md#network-RoutePoint), since it will suffice to display the route as a straight line between these two locations.  


See also official [NeTex White Papers](http://netex-cen.eu/?page_id=14), in particular [06.NeTEx-Network-WhitePaper](http://netex-cen.eu/wp-content/uploads/2015/12/06.NeTEx-Network-WhitePaper_1.08.pdf), where this aspect is described in detail.

#### Link <a id="Projection-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/Full\_PublicationDelivery\_109\_Oslo\_morningbus\_example.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/Full_PublicationDelivery_109_Oslo_morningbus_example.xml)

### PublicationDelivery <a id="Projection-PublicationDelivery"></a>

Because other relevant data structures in the example have already been described in [Simple rhythm based bus line](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md) / [Simple bus line](handbok-n801-siri-netex-simple-bus-line.md), only the definition of [serviceLinks](handbok-n801-siri-netex-network.md#network-ServiceLink) and their use in [linksInSequence](handbok-n801-siri-netex-network.md#network-LinkInJourneyPattern) \(in [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern)\) are described in this document.

### Service Frame <a id="Projection-ServiceFrame"></a>

#### serviceLinks <a id="Projection-serviceLinks"></a>

[Projeksjon\#serviceLinks](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370383#Projeksjon-serviceLinks) with [Link]() [projections]() describes additional geographical points between [StopPoints](handbok-n801-siri-netex-network.md#network-StopPointInJourneyPattern)/[TimingPoints](handbok-n801-siri-netex-network.md#network-TimingPointInJourneyPattern) .

```text
<serviceLinks>
	<ServiceLink version="any" id="unibuss:sl:helsfyr_to_brynseng">
		<projections>
			<LinkSequenceProjection version="any" id="unibuss:lsp:109:helsfyr_to_brynseng">
				<gml:LineString srsName="WGS84" gml:id="helsfyr_to_brynseng">
					<gml:pos>59.911925 10.807198</gml:pos>
					<gml:pos>59.910395 10.813012</gml:pos>
				</gml:LineString>
			</LinkSequenceProjection>
		</projections>
		<FromPointRef version="any" ref="unibuss:ssp:helfyr_t"/>
		<ToPointRef version="any" ref="unibuss:ssp:brynseng_t"/>
	</ServiceLink>
[...]	
	<ServiceLink version="any" id="unibuss:sl:ryen_to_holtet">
		<projections>
			<LinkSequenceProjection version="any" id="unibuss:lsp:109:ryen_to_holtet">
				<gml:LineString srsName="WGS84" gml:id="ryen_to_holtet">
					<gml:pos>59.894780 10.804309</gml:pos>
					<gml:pos>59.892531 10.804000</gml:pos>
					<gml:pos>59.888996 10.805961</gml:pos>
					<gml:pos>59.887608 10.806368</gml:pos>
					<gml:pos>59.886410 10.800586</gml:pos>
					<gml:pos>59.885832 10.792943</gml:pos>
					<gml:pos>59.885392 10.788938</gml:pos>
					<gml:pos>59.885630 10.784435</gml:pos>
					<gml:pos>59.883864 10.783759</gml:pos>
					<gml:pos>59.881872 10.783770</gml:pos>
				</gml:LineString>
			</LinkSequenceProjection>
		</projections>
		<FromPointRef version="any" ref="unibuss:ssp:ryen_t"/>
		<ToPointRef version="any" ref="unibuss:ssp:holtet"/>
	</ServiceLink>
</serviceLinks>
```

#### linksInSequence <a id="Projection-linksInSequence"></a>

The links describing how to project the [line's](handbok-n801-siri-netex-network.md#network-Line) JourneyPattern are used in conjunction with the stops \(possibly timing points\) to accurately specify the line's [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern).

```text
<journeyPatterns>
	<JourneyPattern version="any" id="unibuss:jp:109">
		<RouteRef ref="unibuss:rt:109"/>
		<DestinationDisplayRef ref="unibuss:dd:holtet"/>
		<pointsInSequence>
		[...]
		</pointsInSequence>
		<linksInSequence>
			<ServiceLinkInJourneyPattern version="any" id="unibuss:slijp:helsfyr_to_brynseng" order="1">
				<ServiceLinkRef version="any" ref="unibuss:sl:helsfyr_to_brynseng"/>
			</ServiceLinkInJourneyPattern>
			<ServiceLinkInJourneyPattern version="any" id="unibuss:slijp:brynseng_to_hoyenhall" order="2">
				<ServiceLinkRef version="any" ref="unibuss:sl:brynseng_to_hoyenhall"/>
			</ServiceLinkInJourneyPattern>
			<ServiceLinkInJourneyPattern version="any" id="unibuss:slijp:hoyenhall_to_manglerud" order="3">
				<ServiceLinkRef version="any" ref="unibuss:sl:hoyenhall_to_manglerud"/>
			</ServiceLinkInJourneyPattern>
			<ServiceLinkInJourneyPattern version="any" id="unibuss:slijp:manglerud_to_ryen" order="4">
				<ServiceLinkRef version="any" ref="unibuss:sl:manglerud_to_ryen"/>
			</ServiceLinkInJourneyPattern>
			<ServiceLinkInJourneyPattern version="any" id="unibuss:slijp:ryen_to_holtet" order="5">
				<ServiceLinkRef version="any" ref="unibuss:sl:ryen_to_holtet"/>
			</ServiceLinkInJourneyPattern>
		</linksInSequence>
	</JourneyPattern>
</journeyPatterns>
```

