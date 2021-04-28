# Håndbok N801 \(SIRI/NeTEX\) : StopPlace - simple

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591717298 {padding: 0px;}  
div.rbtoc1619591717298 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591717298 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Bryn skole, Oslo](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-Brynskole,Oslo)
  * [Monomodal StopPlace with two Quays](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-MonomodalStopPlacewithtwoQuays)
    * [Link](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-Link)
  * [Elements](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-Elements)
    * [PublicationDelivery](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-PublicationDelivery)
    * [Validity](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-Validity)
      * [ValidityConditions](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-ValidityConditions)
    * [Organization](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-Organization)
      * [Codespace](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-Codespace)
    * [Site Frame](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-SiteFrame)
      * [Stop Place](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-StopPlace)
      * [Quay](handbok-n801-siri-netex-stopplace-simple.md#StopPlace-simple-Quay)

## Bryn skole, Oslo <a id="StopPlace-simple-Brynskole,Oslo"></a>

### Monomodal StopPlace with two Quays <a id="StopPlace-simple-MonomodalStopPlacewithtwoQuays"></a>

Bryn skole \(at Ole Deviks vei\) is modelled as a [monomodal stop place](handbok-n801-siri-netex-stops.md#stops-MonomodalStopPlace) \(a stop place for one single type of transport\) with two [quays](handbok-n801-siri-netex-stops.md#stops-Quay), and serves as an example of a stop place which is served only by bus. All stop places that are served by only one type of transport, such as tram, metro, train or boat, are modelled in this manner.

The stop place for Bryn skole has no facilities beyond a sign showing that there is a bus stop, with information board for the bus route, with a timetable.

#### Link <a id="StopPlace-simple-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/stops/BasicStopPlace-two-quays\_example.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/BasicStopPlace-two-quays_example.xml)

### Elements <a id="StopPlace-simple-Elements"></a>

The following is a more detailed description of the most important elements that must be included in the data transfer to the stop place registry:

#### PublicationDelivery <a id="StopPlace-simple-PublicationDelivery"></a>

All XML files according to the [Norwegian NeTEx-profile](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370405/NeTEx+profil+Norge) should be of type PublicationDelivery containing relevant [Frames](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework). \(See [_GitHub_](https://github.com/entur/profile-norway-examples/blob/master/netex/frames/publicationDelivery.xml) __for a complete example.\)

#### Validity <a id="StopPlace-simple-Validity"></a>

Describes the validity criteria for the dataset. In this example, an open-ended validity period, from a specific date, without an end date.

**ValidityConditions**

```text
<validityConditions>
	<AvailabilityCondition version="any" id="NSR:AvailabilityCondition:1">
		<FromDate>2017-03-08T12:12:00.0Z</FromDate>
	</AvailabilityCondition>
</validityConditions>
```

#### Organization <a id="StopPlace-simple-Organization"></a>

Each operator, as well as other authorities, has its own "namespace" - Xmlns - \(cf. Administration Code\) which guarantees the uniqueness of the contents of the dataset.

In Norway, these codes are set by the national stop place registry.

**Codespace**

```text
<codespaces>
	<Codespace id="NRS">
		<Xmlns>NSR</Xmlns>
		<XmlnsUrl>http://www.entur.org/ns/nsr</XmlnsUrl>
	</Codespace>
</codespaces>
```

#### Site Frame <a id="StopPlace-simple-SiteFrame"></a>

This block contains the information relevant for describing "physical" objects, including StopPlace, Quay and Facilities/Equipment found on them.

```text
<SiteFrame version="any" id="NSR:SiteFrame:1">
	<!-- ===StopPlaces=== -->
	<!-- Details for StopPlace and Quay can be found further down in the example -->
	<stopPlaces>
		<StopPlace>
			[...]
			<quays>
				<Quay>[...]</Quay>
			</quays>
		</StopPlace>
	</stopPlaces>
	
	<siteFacilitySets>
		<SiteFacilitySet id="NSR:SiteFacilitySet:timetablePoster" version="any">
			<PassengerInformationEquipmentList>timetablePoster</PassengerInformationEquipmentList>
		</SiteFacilitySet>
		<SiteFacilitySet id="NSR:SiteFacilitySet:lineNetworkPlan" version="any">
			<PassengerInformationEquipmentList>lineNetworkPlan</PassengerInformationEquipmentList>
		</SiteFacilitySet>
		<SiteFacilitySet id="NSR:SiteFacilitySet:fareInformation" version="any">
			<PassengerInformationEquipmentList>fareInformation</PassengerInformationEquipmentList>
		</SiteFacilitySet>
	</siteFacilitySets>
</SiteFrame>
```

**Stop Place**

The stop place is generally described with name, transport mode, and location, and should have accessibility information defined to satisfy universal design requirements. \(Accessibility can also be modelled as [NavigationPaths](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-NavigationPath) if relevant.\)

```text
<!-- Note: StopPlace-ID must be generated by the stop place registry -->
<StopPlace version="any" id="NSR:StopPlace:12345678">
	<Centroid>
		<Location srsName="WGS84" id="NSR:Location:1">
			<Longitude>10.824609</Longitude>
			<Latitude>59.913915</Latitude>
		</Location>
	</Centroid>
	<AccessibilityAssessment version="any" id="NSR:AccessibilityAssessment:1">
		<MobilityImpairedAccess>true</MobilityImpairedAccess>
		<limitations>
			<AccessibilityLimitation>
				<WheelchairAccess>true</WheelchairAccess>
				<StepFreeAccess>true</StepFreeAccess>
			</AccessibilityLimitation>
		</limitations>
	</AccessibilityAssessment>

	<placeEquipments>
		<GeneralSign id="NSR:GeneralSign:1" version="any">
			<PrivateCode>512</PrivateCode>
			<SignContentType>transportMode</SignContentType>
		</GeneralSign>
	</placeEquipments>

	<TransportMode>bus</TransportMode>
	<StopPlaceType>onstreetBus</StopPlaceType>

	<quays>
		[...]
	</quays>
</StopPlace>
```

**Quay**

An individual \(and exact\) position for boarding/alighting is defined as a Quay. It can have references to nearby roads, facilities, compass bearing etc. Its most prominent features are coordinate and PublicCode \(platform identifier\). The Quay always inherits name from its parent StopPlace.

```text
<Quay version="any" id="NSR:Quay:12345679">
	<Centroid>
		<Location>
			<Longitude>59.9139819</Longitude>
			<Latitude>10.8247039</Latitude>
		</Location>
	</Centroid>
	<Lighting>poorlyLit</Lighting>
	<facilities>
		<SiteFacilitySetRef ref="NSR:SiteFacilitySet:timetablePoster"/>
		<SiteFacilitySetRef ref="NSR:SiteFacilitySet:fareInformation"/>
	</facilities>
	<PublicCode>A</PublicCode>
	<CompassBearing>200</CompassBearing>
</Quay>
```

