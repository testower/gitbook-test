# Håndbok N801 \(SIRI/NeTEX\) : StopPlace - minimalistic

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591736710 {padding: 0px;}  
div.rbtoc1619591736710 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591736710 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Blystadlia, Rælingen](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-Blystadlia,Rælingen)
  * [A monomodal StopPlace with one Quay](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-AmonomodalStopPlacewithoneQuay)
    * [Link](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-Link)
  * [Elements](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-Elements)
    * [PublicationDelivery](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-PublicationDelivery)
    * [StopPlaces](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-StopPlaces)
    * [StopPlace](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-StopPlace)
      * [StopPlace](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-StopPlace.1)
    * [Quay](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-Quay)
      * [Quay](handbok-n801-siri-netex-stopplace-minimalistic.md#StopPlace-minimalistic-Quay.1)

## Blystadlia, Rælingen <a id="StopPlace-minimalistic-Blystadlia,R&#xE6;lingen"></a>

### A monomodal StopPlace with one Quay <a id="StopPlace-minimalistic-AmonomodalStopPlacewithoneQuay"></a>

The stop place in _Blystadlia_ is designed to allow a bus to stop at one particular location in a one-way loop. This is modelled as a [monomodal stop place](handbok-n801-siri-netex-stops.md#stops-MonomodalStopPlace) \(stop place for one transport type\), and because it is located on a one-way street in it only has one [quay](handbok-n801-siri-netex-stops.md#stops-Quay). The stop place is served exclusively by bus, similar to the example for [simple bus stop](handbok-n801-siri-netex-stopplace-simple.md).

The stop place in the example has no facilities beyond a sign showing the transport mode at the stop and is included in order to show the principles of modelling a stop place in its simplest form.

#### Link <a id="StopPlace-minimalistic-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/stops/BasicStopPlace\_example.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/BasicStopPlace_example.xml)

### Elements <a id="StopPlace-minimalistic-Elements"></a>

Below is a more detailed description of the most important elements of modelling a stop place.

Note that this is a **simplified** NeTEx XML. According to the Norwegian profile, there **must** be **several elements** for the file to be valid for data transfer to the stop place registry.

See example for [simple stop place, bus](handbok-n801-siri-netex-stopplace-simple.md) for XML containing necessary items for successful validation.

#### PublicationDelivery <a id="StopPlace-minimalistic-PublicationDelivery"></a>

All XML files according to the [Norwegian NeTEx-profile](handbok-n801-siri-netex-nordic-netex-profile.md) must be of a _PublicationDelivery_ containing relevant [Frames](). \(See [_GitHub_](https://github.com/entur/profile-norway-examples/blob/master/netex/frames/publicationDelivery.xml) for a complete example.\)

#### StopPlaces <a id="StopPlace-minimalistic-StopPlaces"></a>

Lists all StopPlaces defined in this PublicationDelivery.

#### StopPlace <a id="StopPlace-minimalistic-StopPlace"></a>

The stop place is defined with a name, transport- and stop place type, and must have defined accessibility information in order to satisfy the requirements for universal design.

**StopPlace**

```text
<StopPlace version="any" id="NSR:StopPlace:10000000">
	<Name>Blystadlia</Name>
	<!-- General accessible by wheelchair -->
	<AccessibilityAssessment version="any" id="NSR:AccessibilityAssessment:1">
		<MobilityImpairedAccess>true</MobilityImpairedAccess>
		<limitations>
			<!-- Minimum requirements to UU-information -->
			<AccessibilityLimitation>
				<WheelchairAccess>true</WheelchairAccess>
				<StepFreeAccess>true</StepFreeAccess>
			</AccessibilityLimitation>
		</limitations>
	</AccessibilityAssessment>
	<Covered>outdoors</Covered>
	<placeEquipments>
		<PassengerInformationEquipment id="NSR:PassengerInformationEquipment" version="any">
			<PassengerInformationFacilityList>passengerInformationDisplay</PassengerInformationFacilityList>
		</PassengerInformationEquipment>
		<GeneralSign id="NSR:GeneralSign:1" version="any">
			<PrivateCode>512</PrivateCode>
			<SignContentType>transportMode</SignContentType>
		</GeneralSign>
	</placeEquipments>
	<TransportMode>bus</TransportMode>
	<StopPlaceType>onstreetBus</StopPlaceType>
	<quays>
		<!--- see its own description below -->
	</quays>
</StopPlace>
```

#### Quay <a id="StopPlace-minimalistic-Quay"></a>

The individual positions for boarding/alighting are defined as quays and include descriptions of its connections \(parent stop\), as well as info about facilities tied to the specific Quay, which may be relevant to the public.

**Quay**

```text
<Quay version="any" id="NSR:Quay:11111111">
	<Centroid>
		<!-- Always WGS84 -->
		<Location srsName="WGS84">
			<Longitude>11.034508</Longitude>
			<Latitude>59.931081</Latitude>
		</Location>
	</Centroid>
	<Lighting>wellLit</Lighting>
	<PublicCode>2</PublicCode>
</Quay>
```

