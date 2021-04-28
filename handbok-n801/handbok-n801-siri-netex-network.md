# Håndbok N801 \(SIRI/NeTEX\) : network

## Version <a id="network-Version"></a>

Current version for **network** is:   **v1.4**   \(last changed 09 Feb 2021\) 

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591690118 {padding: 0px;}  
div.rbtoc1619591690118 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591690118 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Version](handbok-n801-siri-netex-network.md#network-Version)
* [Components](handbok-n801-siri-netex-network.md#network-Components)
  * [Network components](handbok-n801-siri-netex-network.md#network-Networkcomponents)
    * [Network](handbok-n801-siri-netex-network.md#network-Network)
    * [GroupOfLines](handbok-n801-siri-netex-network.md#network-GroupOfLines)
    * [Line](handbok-n801-siri-netex-network.md#network-Line)
      * [Presentation](handbok-n801-siri-netex-network.md#network-Presentation)
  * [Service](handbok-n801-siri-netex-network.md#network-Service)
    * [TypeOfService](handbok-n801-siri-netex-network.md#network-TypeOfService)
  * [Route](handbok-n801-siri-netex-network.md#network-Route)
    * [Route](handbok-n801-siri-netex-network.md#network-Route.1)
    * [RoutePoint](handbok-n801-siri-netex-network.md#network-RoutePoint)
    * [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint)
    * [TimingPoint](handbok-n801-siri-netex-network.md#network-TimingPoint)
    * [PointOnRoute](handbok-n801-siri-netex-network.md#network-PointOnRoute)
    * [RouteLink](handbok-n801-siri-netex-network.md#network-RouteLink)
    * [ServiceLink](handbok-n801-siri-netex-network.md#network-ServiceLink)
    * [Connection](handbok-n801-siri-netex-network.md#network-Connection)
      * [SiteConnection](handbok-n801-siri-netex-network.md#network-SiteConnection)
      * [SiteConnectionEndStructure](handbok-n801-siri-netex-network.md#network-SiteConnectionEndStructure)
    * [Stop Assignment](handbok-n801-siri-netex-network.md#network-StopAssignment)
      * [StopAssignment](handbok-n801-siri-netex-network.md#network-StopAssignment.1)
      * [PassengerStopAssignment](handbok-n801-siri-netex-network.md#network-PassengerStopAssignment)
      * [FlexibleStopAssignment](handbok-n801-siri-netex-network.md#network-FlexibleStopAssignment)
      * [TrainStopAssignment](handbok-n801-siri-netex-network.md#network-TrainStopAssignment)
  * [Journey Pattern](handbok-n801-siri-netex-network.md#network-JourneyPattern)
    * [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern.1)
      * [StopPointInJourneyPattern](handbok-n801-siri-netex-network.md#network-StopPointInJourneyPattern)
      * [BookingArrangementsStructure](handbok-n801-siri-netex-network.md#network-BookingArrangementsStructure)
      * [TimingPointInJourneyPattern](handbok-n801-siri-netex-network.md#network-TimingPointInJourneyPattern)
      * [LinkInJourneyPattern](handbok-n801-siri-netex-network.md#network-LinkInJourneyPattern)
      * [TimingLinkInJourneyPattern](handbok-n801-siri-netex-network.md#network-TimingLinkInJourneyPattern)
      * [ServiceLinkInJourneyPattern](handbok-n801-siri-netex-network.md#network-ServiceLinkInJourneyPattern)
  * [DestinationDisplay](handbok-n801-siri-netex-network.md#network-DestinationDisplay)
    * [DestinationDisplayVariant](handbok-n801-siri-netex-network.md#network-DestinationDisplayVariant)
    * [Via](handbok-n801-siri-netex-network.md#network-Via)
  * [Flexible transport](handbok-n801-siri-netex-network.md#network-Flexibletransport)
    * [FlexibleLine](handbok-n801-siri-netex-network.md#network-FlexibleLine)
    * [FlexibleStopAssignment](handbok-n801-siri-netex-network.md#network-FlexibleStopAssignment.1)
  * [Transfers](handbok-n801-siri-netex-network.md#network-Transfers)
    * [Transfer](handbok-n801-siri-netex-network.md#network-Transfer)
      * [TransferDuration](handbok-n801-siri-netex-network.md#network-TransferDuration)

  
This document is part of the Norwegian NeTEx profile and describes data elements related to **transport networks** used for public transport data exchange in the NeTEx format.

* Please note the network part of the profile describes structures, attributes, and geospatial objects, which make up the framework of the timetable data. It does not, however, describe time-related concepts, such as departure times, or operational days. All of these are described in [timetable](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable).

## Components <a id="network-Components"></a>

### Network components <a id="network-Networkcomponents"></a>

#### Network <a id="network-Network"></a>

A transport network is an "umbrella" structure for all [Lines](handbok-n801-siri-netex-network.md#network-Line) which share relevant features, such as the ownership of the lines. 

If necessary, these can be separated further as [GroupOfLines](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#GroupOfLines) \(see below\), a supplementary \(optional\) level of logical structuring within the overall Network of [Lines](handbok-n801-siri-netex-network.md#network-Line).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Network)

_Defined in ServiceFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) \(including [use of additionalNetworks](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-additionalNetworks.xml)\)

| Network &lt; [GroupOfLines](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#GroupOfLines) &lt; [GroupOfEntities]()  &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Name | [MultilingualString]() | 1: 1 | Name of the network. |
| AuthorityRef | OrganisationRefStructure | 1: 1 | [Organisation]() responsible \(for example owner\) for the network. |
| groupsOfLines | [GroupOfLines](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#GroupOfLines) | 0: \* | Lines \([Line](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Line)\) included in the network. |
| tariffZones | tariffZoneRefs | 0: \* | Tariff zones \([TariffZone](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TariffZone)\) in the network \(_when relevant_\). |

#### GroupOfLines <a id="network-GroupOfLines"></a>

Additional \(optional\) grouping of lines.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-GroupOfLines)

_Defined in ServiceFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">GroupOfLines &lt; <a href>GroupOfEntities</a> &lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Group name</td>
    </tr>
    <tr>
      <td style="text-align:left">members</td>
      <td style="text-align:left">lineRefs</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>An explicit listing of lines included in the group (if appropriate)</p>
        <p><em>Note that reference should link from</em>  <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Line"><em>Line</em></a>  <em>up to</em> 
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Network"><em>Network</em>
            </a> <em>through a RepresentedByGroupRef</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">MainLineRef</td>
      <td style="text-align:left">LineRefStructure</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to the primary line in the group.</td>
    </tr>
    <tr>
      <td style="text-align:left">TransportMode</td>
      <td style="text-align:left">AllVehicleModesOfTransportEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The transport mode of the group.</p>
        <p>See <a href>Transport Modes</a> for possible values</p>
      </td>
    </tr>
  </tbody>
</table>

#### Line <a id="network-Line"></a>

Line \(grouping of Routes\) with a name or number \(PublicCode\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Line)

_Defined in ServiceFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">Line &lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">(attr) modification</td>
      <td style="text-align:left">xs:ModificationEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Type of modification (<em>use &quot;delete&quot; when a Line is permanently discontinued</em>)</td>
    </tr>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Name of the line</td>
    </tr>
    <tr>
      <td style="text-align:left">ShortName</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Short name (e.g. short version of commonly (publicly) known name)</td>
    </tr>
    <tr>
      <td style="text-align:left">Description</td>
      <td style="text-align:left"><a href>MultilingualString</a> 
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">TransportMode</td>
      <td style="text-align:left">AllVehicleModesOfTransportEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">See <em>Mode</em> in <a href>Transport Modes</a> for valid values</td>
    </tr>
    <tr>
      <td style="text-align:left">TransportSubmode</td>
      <td style="text-align:left">TransportSubmode</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">See <em>Submodes</em> in <a href>Transport Modes</a> for valid values (<em>must be a TransportSubmode belonging to the selected TransportMode)</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Url</td>
      <td style="text-align:left">xsd:anyURI</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">URL to a website with information about the line.</td>
    </tr>
    <tr>
      <td style="text-align:left">PublicCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The publicly advertised line number, or code of the line.</p>
        <p><em>Usually a number, or a number combined with a letter (eg L2, 31, 30E etc.).</em>
        </p>
        <p><em>The Name field normally contains more information than the PublicCode, and is often the combination of PublicCode + Name.</em>
          <br
          />
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">PrivateCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Internal (non-public) identifier for the line. For example, a code used
        by transport planners.</td>
    </tr>
    <tr>
      <td style="text-align:left">ExternalLineRef</td>
      <td style="text-align:left">ExternalObjectRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference (ID) to a related Line (for example, the regular line for which
        this is a replacement).</td>
    </tr>
    <tr>
      <td style="text-align:left">OperatorRef</td>
      <td style="text-align:left">OperatorRefStructure</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to the main <a href>operator</a> (may be omitted in <em>exceptional cases, such as a different operator for every departure</em>).</td>
    </tr>
    <tr>
      <td style="text-align:left">additionalOperators</td>
      <td style="text-align:left">transportOrganisationRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Reference to additional operators of the line</td>
    </tr>
    <tr>
      <td style="text-align:left">TypeOfLineRef</td>
      <td style="text-align:left">TypeOfLineRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to the line type. Classification, (e.g. replacement line)</td>
    </tr>
    <tr>
      <td style="text-align:left">Monitored</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether real-time information normally is available for this
        line (set to <code>true</code> when real-time data exists for the line).</td>
    </tr>
    <tr>
      <td style="text-align:left">routes</td>
      <td style="text-align:left">RouteRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Reference to a listing of all routes (<a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Route.1">Route</a>)
          which are part of the line.</p>
        <p><em>The references can normally be deduced from Line references in </em>
          <a
          href="handbok-n801-siri-netex-network.md#network-Route"><em>Routes</em>
            </a><em>. Therefore this field is only relevant in exceptional cases).</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">RepresentedByGroupRef</td>
      <td style="text-align:left">GroupOfLinesRefStructure</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to the Lines&apos; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Network">Network</a> (alternatively
        a more specific reference to the <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#GroupOfLines">GroupOfLines</a>).</td>
    </tr>
    <tr>
      <td style="text-align:left">Presentation</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Presentation">Presentation</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Graphical representation information (colour, text, etc.)</td>
    </tr>
    <tr>
      <td style="text-align:left">AccessibilityAssessment</td>
      <td style="text-align:left"><a href>AccessibilityAssessment</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Universal Design - Description of the line</td>
    </tr>
  </tbody>
</table>

**Presentation**

Description of values used for presenting line information, such as fonts and colours, etc. which may be used on graphical representations of the line, such as maps or printed publications.

_It is required to fill out at least one field \(of the ones listed below\) in order to have a valid Presentation. The default values are white \(FFFFFF\) Colour with black TextColour \(000000\)._

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-Presentation.xml) 

| Presentation |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Colour | ColourValueType | 0: 1 | [Six digit hexadecimal representation of the lines' RGB colour values](https://en.wikipedia.org/wiki/Web_colors). |
| TextColour | ColourValueType | 0: 1 | [Six digit hexadecimal representation of the lines' RGB colour values](https://en.wikipedia.org/wiki/Web_colors). |
| TextFont | xsd:normalizedString | 0: 1 | Font identifier \(font\). _Normally not specified._ |

### Service <a id="network-Service"></a>

#### TypeOfService <a id="network-TypeOfService"></a>

Classification of a service. 

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TypeOfService)

_Defined in TimetableFrame_

| TypeOfService &lt; [TypeOfValue]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| TypeOfService inherits fromTypeOfValue and does not introduce new elements or attributes. |  |  |  |

### Route <a id="network-Route"></a>

#### Route <a id="network-Route.1"></a>

Description of a route, specified as a sorted list of RoutePoints.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Route)

_Defined in ServiceFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">Route &lt; <a href>LinkSequence</a> &lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">LineRef</td>
      <td style="text-align:left">LineRefStructure</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to Line (<a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Line">Line</a>)
        to which the Route belongs.</td>
    </tr>
    <tr>
      <td style="text-align:left">DirectionType</td>
      <td style="text-align:left">DirectionTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The direction of the route:</p>
        <ul>
          <li>inbound <em>(towards the city centre or transport hub)</em>
          </li>
          <li>outbound <em>(from the city centre or transport hub)</em> 
          </li>
          <li>clockwise <em>(circular route in the clockwise direction)</em>
          </li>
          <li>anticlockwise <em>(circular route in the anticlockwise direction)</em>
          </li>
        </ul>
        <p><em>To be able to identify full- or partial circular routes clockwise/anticlockwise must be specified.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">pointsInSequence</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#PointOnRoute">PointOnRoute</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">List of the routes points</td>
    </tr>
    <tr>
      <td style="text-align:left">InverseRouteRef</td>
      <td style="text-align:left">RouteRefStructure</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to any route that goes in the opposite direction</td>
    </tr>
  </tbody>
</table>

#### RoutePoint <a id="network-RoutePoint"></a>

A point that is a stop place in a route.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-RoutePoint)

_Defined in ServiceFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

| RoutePoint &lt; [Point]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| BorderCrossing | xsd:boolean | 0: 1 | Specifies whether the point is on the border between two countries. |

#### ScheduledStopPoint <a id="network-ScheduledStopPoint"></a>

Point for planned disembarking and/or boarding. Linking to [StopPlaces](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPlace)/[Quays](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Quay) is done through [StopAssignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#StopAssignment). _All ScheduledStopPoint must have such a link._

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ScheduledStopPoint)

_Defined in ServiceFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">ScheduledStopPoint &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TimingPoint">TimingPoint</a> &lt;
        <a
        href>Point</a>&lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">TimingPointStatus</td>
      <td style="text-align:left">TimingPointStatusEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of TimingPoint:</p>
        <ul>
          <li>timingPoint <em>(the ScheduledStopPoint should also explicitly be regarded as a timing point in relevant systems)</em>
          </li>
          <li>notTimingPoint <em>(the ScheduledStopPoint should <b>not</b> be regarded as a timing point)</em>
          </li>
          <li>secondaryTimingPoint <em>(for arbitrary use)</em>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">tariffZones</td>
      <td style="text-align:left">TariffZoneRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>List of TariffZones (<a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TariffZone">TariffZone</a>)
          the StopPoint belongs to</p>
        <p><em>Not recommended to use, as this may be overridden by TariffZone / FareZone geography specified in the SiteFrame.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Presentation</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Presentation">Presentation</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Graphical elements related to StopPoint</td>
    </tr>
  </tbody>
</table>

#### TimingPoint <a id="network-TimingPoint"></a>

Point for registering passing times. Usually, not a place where the vehicle stops, nor a place relevant to passengers, though it can be used to indicate places where the vehicle waits.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TimingPoint)

_Defined in ServiceFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">TimingPoint &lt; <a href>Point</a> &lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">TimingPointStatus</td>
      <td style="text-align:left">TimingPointStatusEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of TimingPoint:</p>
        <ul>
          <li>timingPoint</li>
          <li>notTimingPoint <em>(may indicate the expected passing time)</em>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">AllowedForWaitTime</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Allowed waiting time at the TimingPoint.</td>
    </tr>
  </tbody>
</table>

#### PointOnRoute <a id="network-PointOnRoute"></a>

Link between [Route](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Route) and [RoutePoint.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-RoutePoint)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-PointOnRoute)

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">PointOnRoute &lt; <a href>PointInLinkSequence</a> &lt; VersionedChild &lt;
        <a
        href>EntityInVersion</a>&lt; <a href>Entity</a> 
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">LinkSequenceRef</td>
      <td style="text-align:left">LinkSequenceRefStructure</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to <a href>LinkSequence</a> to which the point belongs.</p>
        <p><em>RouteRef should be used since </em><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Route.1"><em>Route</em></a>  <em>inherits from </em>
          <a
          href><em>LinkSequence</em>
            </a><em>.</em>
        </p>
        <p>Note that the field should <b>not</b> be used if PointOnRoute is defined
          inline in <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Route.1">Route</a>.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">projections</td>
      <td style="text-align:left"><a href>Projection</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Projection on a point (RoutePoint, TimingPoint, SchedueledStopPoint) or
        a GML-coordinate projection.</td>
    </tr>
    <tr>
      <td style="text-align:left">PointRef</td>
      <td style="text-align:left">PointRefStructure</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Reference to <a href>Point</a>
        </p>
        <p>RoutePointRef should be used to point to the corresponding <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#RoutePoint">RoutePoint</a>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### RouteLink <a id="network-RouteLink"></a>

Link \(with direction\) between two [RoutePoints.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-RoutePoint)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-RouteLink)

_Defined in ServiceFrame_

| RouteLink &lt; [Link]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| FromPointRef | RoutePointRef | 1: 1 | The start point for the RouteLink |
| ToPointRef | RoutePointRef | 1: 1 | The endpoint for the RouteLink |

#### ServiceLink <a id="network-ServiceLink"></a>

Link \(with direction\) between two [stop points](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServiceLink)

_Defined in ServiceFrame_

| ServiceLink &lt; [Link]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Distance | xsd:decimal | 0: 1 | Distance in _meters_ for ServiceLink, i.e. _driving distance_ between FromPoint and ToPoint. |
| projections | [LinkSequenceProjection]() | 0: 1 | Projection with &lt;gml:LineString&gt; indication of position. |
| FromPointRef | ScheduledStopPointRef | 1: 1 | The start point for the ServiceLink. |
| ToPointRef | ScheduledStopPointRef | 1: 1 | The endpoint for ServiceLink. |

#### Connection <a id="network-Connection"></a>

**SiteConnection**

Description of the navigation possibility between two Sites, for example between two StopPlaces, or two Quays.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-SiteConnection)

| SiteConnection &lt; [Transfer](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Transfer) &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| From | [SiteConnectionEndStructure](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteConnectionEndStructure) | 1: 1 | The starting point for SiteConnection |
| To | [SiteConnectionEndStructure](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteConnectionEndStructure) | 1: 1 | The endpoint for SiteConnection |
| navigationPaths | [NavigationPath](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#NavigationPath) | 0: \* | Possible path links between [Site](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#%5BhardBreak%5DSite)-objects |

**SiteConnectionEndStructure**

| SiteConnectionEnd |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| StopPlaceRef | StopPlaceRef | 0: 1 | Reference to the [StopPlace ](handbok-n801-siri-netex-network.md#stops-StopPlace)in question |
| QuayRef | QuayRef | 0: 1 | Reference to the [Quay ](handbok-n801-siri-netex-network.md#stops-Quay)in question |
| StopPlaceEntranceRef | StopPlaceEntranceRef | 0: 1 | Reference to the [Entrance ](handbok-n801-siri-netex-network.md#stops-Entrance)in question |

#### Stop Assignment <a id="network-StopAssignment"></a>

**StopAssignment**

Abstract class used to describe the link between [ScheduledStopPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ScheduledStopPoint) and [StopPlace.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPlace)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopAssignment)

| StopAssignment &lt; [Assignment]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| ScheduledStopPointRef | ScheduledStopPointRef | 1: 1 | Reference to [ScheduledStopPoint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ScheduledStopPoint) |

**PassengerStopAssignment**

Link between [ScheduledStopPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ScheduledStopPoint) and [StopPlace](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPlace) or [Quay](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Quay)

Examples in the [GitHub-repository](https://github.com/entur/netex-norway-examples/blob/master/examples/network/Line61A.xml)

_Defined in ServiceFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">PassengerStopAssignment &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#StopAssignment">StopAssignment</a> &lt;
        <a
        href>Assignment</a>&lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">StopPlaceRef</td>
      <td style="text-align:left">StopPlaceRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to <a href="handbok-n801-siri-netex-stops.md#stops-StopPlace">StopPlace</a> which
          is related to <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ScheduledStopPoint">ScheduledStopPoint</a>
        </p>
        <p><em>Should be included as far as possible, but the StopPlace can also be derived from the referenced Quay (QuayRef) when the StopPlaceRef is missing</em>
          <br
          />
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">QuayRef</td>
      <td style="text-align:left">QuayRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to an actual <a href="handbok-n801-siri-netex-stops.md#stops-Quay">Quay</a> on
        <a
        href="handbok-n801-siri-netex-stops.md#stops-StopPlace">StopPlace</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">trainElements</td>
      <td style="text-align:left">TrainStopAssignmentRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>References to a detailed position on platform (<a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TrainStopAssignment">TrainStopAssignment</a>)</p>
        <p><em>Used only for trains</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">attr</td>
      <td style="text-align:left">order</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>The Assignment order.</p>
        <p>The &quot;order&quot; attribute is inherited from the more generic type
          Assignment, but in the case of a PassengerStopAssignment its business meaning
          is undefined. It is however mandatory due to an XML schema validation constraint.
          <br
          />Examples of valid implementations:</p>
        <ul>
          <li>an incremented sequence number (&quot;1&quot;, &quot;2&quot;, &quot;3&quot;,
            ...)</li>
          <li>a constant value (&quot;0&quot;)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**FlexibleStopAssignment**

Link between [ScheduledStopPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ScheduledStopPoint) and [FlexibleStopPlace.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleStopPlace)

_Defined in ServiceFrame_ \(the same way as [PassengerStopAssignment](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-PassengerStopAssignment)\)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FlexibleStopAssignment &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#StopAssignment">StopAssignment</a> &lt;
        <a
        href>Assignment</a>&lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">FlexibleStopPlaceRef</td>
      <td style="text-align:left">FlexibleStopPlaceRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to <a href="handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace">FlexibleStopPlace</a> which
        is related to <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ScheduledStopPoint">ScheduledStopPoint</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) FlexibleQuayRef</td>
      <td style="text-align:left">FlexibleQuayRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to a <a href="handbok-n801-siri-netex-stops.md#stops-FlexibleQuay">FlexibleQuay.</a>
        </p>
        <p><em>Can be added in a supplementary role if a FlexibleQuay is used.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) FlexibleAreaRef</td>
      <td style="text-align:left">FlexibleAreaRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to an actual <a href="handbok-n801-siri-netex-stops.md#stops-FlexibleArea">FlexibleArea</a>
        </p>
        <p><em>Can be added in a supplementary role if a FlexibleArea is defined for the FlexibleStopPlace.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) HailAndRideAreaRef</td>
      <td style="text-align:left">HailAndRideAreaRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to an actual <a href="handbok-n801-siri-netex-stops.md#stops-HailAndRideArea">HailAndRideArea</a>
        </p>
        <p><em>Can be added in a supplementary role if a HailAndRideArea is defined for the FlexibleStopPlace.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

**TrainStopAssignment**

Link between [TrainComponent](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TrainComponent) \(train cars\) and [StopPlace](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPlace)/[Quay](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Quay)/[BoardingPosition](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-BoardingPosition).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TrainStopAssignment)

_Defined in ServiceFrame_

| TrainStopAssignment &lt; [StopAssignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#StopAssignment)  &lt; [Assignment]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| PassengerStopAssignmentRef | PassengerStopAssignmentRef | 0: 1 | Reference to [PassengerStopAssignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#PassengerStopAssignment) |
| TrainRef | TrainRef | 0: 1 | Reference to [Train.]() |
| TrainComponentRef | TrainComponentRef | 0: 1 | Reference to specific cars \([TrainComponent]()\). |
| BoardingPositionRef | BoardingPositionRef | 0: 1 | Reference to [BoardingPosition.](handbok-n801-siri-netex-stops.md#stops-BoardingPosition) |
| EntranceToVehicle | [MultilingualString]() | 0: 1 | Specifying entrances to the carriage, e.g. "front door", "rear door", etc. |

### Journey Pattern <a id="network-JourneyPattern"></a>

#### JourneyPattern <a id="network-JourneyPattern.1"></a>

Sorted list of [ScheduledStopPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ScheduledStopPoint)/[TimingPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TimingPoint) and/or [Links](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Link) for a [Route](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Route).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPattern)

_Defined in ServiceFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">JourneyPattern &lt; <a href>LinkSequence</a> &lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">PrivateCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Internal (non-public) identifier for the JourneyPattern.</td>
    </tr>
    <tr>
      <td style="text-align:left">RouteRef</td>
      <td style="text-align:left">RouteRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Route.1">Route</a> used
        in the JourneyPattern.</td>
    </tr>
    <tr>
      <td style="text-align:left">runTimes</td>
      <td style="text-align:left"><a href>JourneyPatternRunTime</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of RunTimes for the JourneyPattern.</p>
        <p><em>Only used when describing frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">waitTimes</td>
      <td style="text-align:left"><a href>JourneyPatternWaitTime</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of WaitTime for JourneyPattern</p>
        <p><em>Normally used only when describing frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">headways</td>
      <td style="text-align:left"><a href>JourneyPatternHeadway</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of JourneyHeadway for JourneyPattern</p>
        <p><em>Only used when describing frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">pointsInSequence</td>
      <td style="text-align:left">PointInJourneyPattern</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Sorted list of points in JourneyPattern. Must be <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#StopPointInJourneyPattern">StopPointInJourneyPattern</a> or
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TimingPointInJourneyPattern">TimingPointInJourneyPattern</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left">linksInSequence</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#LinkInJourneyPattern">LinkInJourneyPattern</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Sorted list of links in JourneyPattern. Must be <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ServiceLinkInJourneyPattern">ServiceLinkInJourneyPattern</a> or
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TimingLinkInJourneyPattern">TimingLinkInJourneyPattern</a>.</td>
    </tr>
  </tbody>
</table>

**StopPointInJourneyPattern**

[ScheduledStopPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ScheduledStopPoint) in a [JourneyPattern.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPattern)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPointInJourneyPattern)

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">StopPointInJourneyPattern &lt; <a href>PointInLinkSequence</a> &lt; VersionedChild
        &lt; <a href>EntityInVersion</a> &lt; <a href>Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">ScheduledStopPointRef</td>
      <td style="text-align:left">ScheduledStopPointRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ScheduledStopPoint">ScheduledStopPoint</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ForAlighting</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specifies whether alighting is allowed.</p>
        <p><em>Should be explicitly indicated (normally &quot;false&quot;) for the <b>first </b>StopPointInJourneyPattern</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ForBoarding</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specifies whether boarding is allowed.</p>
        <p><em>Should be explicitly indicated (normally &quot;false&quot;) for <b>last </b>StopPointInJourneyPattern</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DestinationDisplayRef</td>
      <td style="text-align:left">DestinationDisplayRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#DestinationDisplay">DestinationDisplay</a>
        </p>
        <p><em>The required minimum for linear routes is for <b>the first</b> StopPointInJourneyPattern to have a DestinationDisplayRef. For circular routes, the minimum is two.</em>
        </p>
        <p><em>A new DestinationDisplayRef should be set at any StopPointInJourneyPattern along the route where it is relevant to <b>update the destination text</b>. This is particularly relevant for circular routes.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">FlexiblePointProperties</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-network.md#network-FlexiblePointProperties">network#FlexiblePointProperties</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Properties of a stop point related to flexible transport.</td>
    </tr>
    <tr>
      <td style="text-align:left">RequestStop</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether passengers must signal to use this stop point.</td>
    </tr>
    <tr>
      <td style="text-align:left">RequestMethod</td>
      <td style="text-align:left">RequestMethodTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values for hailing or arranging a stop:</p>
        <ul>
          <li>handSignal</li>
          <li>phoneCall</li>
          <li>sms</li>
          <li>stopButton</li>
          <li>turnOnLight</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookingArrangements</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#BookingArrangementsStructure">BookingArrangementsStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Rules for booking.</p>
        <p><em>Please note that BookingArrangements specified at the StopPointInJourneyPattern level will <b>always override</b> equivalent specifications at the Line- or ServiceJourney level.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

**BookingArrangementsStructure**

Details for booking public transport services to a specific [StopPointInJourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-StopPointInJourneyPattern) in an otherwise non-flexible line, or when the booking details for the stop deviate from those in a [FlexibleLine](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-FlexibleLine).

<table>
  <thead>
    <tr>
      <th style="text-align:left">BookingArrangementsStructure</th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">BookingContact</td>
      <td style="text-align:left"><a href>ContactStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Contact information for booking</p>
        <p><em>Note that the field is <b>mandatory</b> if this is not already on</em> 
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#FlexibleLine"><em>FlexibleLine</em>
            </a> <em>or overridden in </em><a href="handbok-n801-siri-netex-timetable.md#timetable-FlexibleServiceProperties"><em>FlexibleServiceProperties</em></a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookingMethods</td>
      <td style="text-align:left">BookingMethodListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible ways to book (must match info found in BookingContact):</p>
        <ul>
          <li>callDriver</li>
          <li>callOffice</li>
          <li>online</li>
          <li>phoneAtStop</li>
          <li>text (text message/SMS)</li>
        </ul>
        <p><em>Note that the field is <b>mandatory</b> if this is not already on </em>
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#FlexibleLine"><em>FlexibleLine</em>
            </a> <em>or overridden in </em><a href="handbok-n801-siri-netex-timetable.md#timetable-FlexibleServiceProperties"><em>FlexibleServiceProperties</em></a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookingAccess</td>
      <td style="text-align:left">BookingAccessEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Who may place an order (book):</p>
        <ul>
          <li>public</li>
          <li>authorisedPublic (<em>eg TT-transport - special services for mobility restricted travellers </em>)</li>
          <li>staff</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookWhen</td>
      <td style="text-align:left">PurchaseWhenEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Time constraints for booking:</p>
        <ul>
          <li>timeOfTravelOnly</li>
          <li>dayOfTravelOnly</li>
          <li>untilPreviousDay</li>
          <li>advanceAndDayOfTravel</li>
        </ul>
        <p><em>Note that the field is <b>mandatory</b> if this is not already on </em>
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#FlexibleLine"><em>FlexibleLine</em>
            </a> <em>or overridden in </em><a href="handbok-n801-siri-netex-timetable.md#timetable-FlexibleServiceProperties"><em>FlexibleServiceProperties</em></a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BuyWhen</td>
      <td style="text-align:left">PurchaseMomentListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Time constraints for payment:</p>
        <ul>
          <li>onReservation</li>
          <li>beforeBoarding</li>
          <li>afterBoarding</li>
          <li>onCheckOut</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LatestBookingTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Latest possible booking time.</td>
    </tr>
    <tr>
      <td style="text-align:left">MinimumBookingPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The minimum period prior to the departure the booking has to be placed.</td>
    </tr>
    <tr>
      <td style="text-align:left">BookingNote</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Additional information about the order.</td>
    </tr>
  </tbody>
</table>

**TimingPointInJourneyPattern**

[TimingPoint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TimingPoint) in a [JourneyPattern.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPattern)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TimingPointInJourneyPattern)

| TimingPointInJourneyPattern &lt; [PointInLinkSequence]() &lt; VersionedChild &lt; [EntityInVersion]() &lt; [Entity]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Desription |
| TimingPointRef | TimingPointRef | 1: 1 | Reference to [TimingPoint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TimingPoint) |
| WaitTime | xsd:duration | 0: 1 | Wait time at the timing point |

**LinkInJourneyPattern**

An abstract type for a sorted list of timing- or service links in a JourneyPattern.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-LinkInJourneyPattern)

| LinkInJourneyPattern &lt; VersionedChild &lt; [EntityInVersion]() &lt; [Entity]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| \(choice\) TimingLinkInJourneyPattern | [TimingLinkInJourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TimingLinkInJourneyPattern) | 1: 1 | Sorted list of [TimingLinks]() |
| \(choice\) ServiceLinkInJourneyPattern | [ServiceLinkInJourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ServiceLinkInJourneyPattern) | 1: 1 | Sorted list of [ServiceLinks](handbok-n801-siri-netex-network.md#network-ServiceLink) |

**TimingLinkInJourneyPattern**

[TimingLink]() in a [JourneyPattern.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPattern)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TimingLinkInServicePattern)

| TimingLinkInJourneyPattern &lt; VersionedChild &lt; [EntityInVersion]() &lt; [Entity]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| TimingLinkRef | TimingLinkRef | 1: 1 | Reference to ServiceLink |

**ServiceLinkInJourneyPattern**

[ServiceLink](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ServiceLink) in a [JourneyPattern.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPattern)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServiceLinkInJourneyPattern)

| ServiceLinkInJourneyPattern &lt; VersionedChild &lt; [EntityInVersion]() &lt; [Entity]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| ServiceLinkRef | ServiceLinkRef | 1: 1 | Reference to ServiceLink |

### DestinationDisplay <a id="network-DestinationDisplay"></a>

The text displayed on \(or in\) a vehicle, commonly above the front window or onboard information screens, describing the vehicles final \(or intermediary\) destination.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-DestinationDisplay)

_Defined in ServiceFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-DestinationDisplay.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">DestinationDisplay &lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">SideText</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The text displayed on the side of the vehicle body.</td>
    </tr>
    <tr>
      <td style="text-align:left">FrontText</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">The text displayed on the front of the vehicle, commonly above the front
        window.</td>
    </tr>
    <tr>
      <td style="text-align:left">vias</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Via">Via</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>An intermediary destination which the vehicle will pass before reaching
          its final destination.</p>
        <p>Eg. Oslo tram line 11: <code>&quot;Majorstuen - Kjels&#xE5;s via Torshov&quot;</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">variants</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#DestinationDisplayVariant">DestinationDisplayVariant</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Variations of DestinationDisplay adapted for particular media types</p>
        <p>Note that for composite DestinationDisplay text, e.g. line number and
          destination name. The minimum requirement is to provide a DestinationDisplay
          for web sites, with a destination name.</p>
      </td>
    </tr>
  </tbody>
</table>

#### DestinationDisplayVariant <a id="network-DestinationDisplayVariant"></a>

Variations of DestinationDisplay adapted for particular media types.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-DestinationDisplayVariant)

<table>
  <thead>
    <tr>
      <th style="text-align:left">DestinationDisplayVariant &lt; <a href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">DestinationDisplayVariantMediaType</td>
      <td style="text-align:left">DeliveryVariantTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Supported media types:</p>
        <ul>
          <li>Printed</li>
          <li>TextToSpeech</li>
          <li>Web</li>
          <li>Mobile</li>
          <li>other (<em>e.g. real-time display</em>)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">FrontText</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Frontpage text for DestinationDisplay</td>
    </tr>
  </tbody>
</table>

#### Via <a id="network-Via"></a>

An intermediary destination which the vehicle will pass before reaching its final destination.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Via)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Via &lt; VersionedChild &lt; <a href>EntityInVersion</a> &lt; <a href>Entity</a> 
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">DestinationDisplayRef</td>
      <td style="text-align:left">DestinationDisplayRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to the <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#DestinationDisplay">DestinationDisplay</a> object
        describing the stop place/area the vehicle is headed towards.</td>
    </tr>
    <tr>
      <td style="text-align:left">RoutePointRef</td>
      <td style="text-align:left">RoutePointRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to <a href="handbok-n801-siri-netex-network.md#network-RoutePoint">RoutePoint.</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ViaType</td>
      <td style="text-align:left">ViaTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>stopPoint</li>
          <li>name</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Flexible transport <a id="network-Flexibletransport"></a>

#### FlexibleLine <a id="network-FlexibleLine"></a>

FlexibleLine is a concept for describing on-demand transport, with at least some non-permanent stop places and/or specific requirements for prebooking\)_._

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleLine)

_Defined in ServiceFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-316-with-interchange.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FlexibleLine &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Line">Line</a> &lt;
        <a
        href>DataManagedObject</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Nane</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">FlexibleLineType</td>
      <td style="text-align:left">FlexibleLineTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Flexible line types:</p>
        <ul>
          <li>corridorService</li>
          <li>mainRouteWithFlexibleEnds</li>
          <li>flexibleAreasOnly</li>
          <li>hailAndRideSections</li>
          <li>fixedStopAreaWide</li>
          <li>mixedFlexible</li>
          <li>mixedFlexibleAndFixed</li>
          <li>fixed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookingContact</td>
      <td style="text-align:left"><a href>ContactStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Contact information for booking.</td>
    </tr>
    <tr>
      <td style="text-align:left">BookingMethods</td>
      <td style="text-align:left">BookingMethodListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible booking methods:</p>
        <ul>
          <li>callDriver</li>
          <li>callOffice</li>
          <li>online</li>
          <li>phoneAtStop</li>
          <li>text (text message/SMS)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookingAccess</td>
      <td style="text-align:left">BookingAccessEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Who may place an order (book):</p>
        <ul>
          <li>public</li>
          <li>authorisedPublic</li>
          <li>staff</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookWhen</td>
      <td style="text-align:left">PurchaseWhenEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Time constraints for booking:</p>
        <ul>
          <li>timeOfTravelOnly</li>
          <li>dayOfTravelOnly</li>
          <li>untilPreviousDay</li>
          <li>advanceAndDayOfTravel</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BuyWhen</td>
      <td style="text-align:left">PurchaseMomentListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Time constraints for payment:</p>
        <ul>
          <li>onReservation</li>
          <li>beforeBoarding</li>
          <li>afterBoarding</li>
          <li>onCheckOut</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LatestBookingTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Latest possible booking time.</td>
    </tr>
    <tr>
      <td style="text-align:left">MinimumBookingPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The minimum period prior to the departure the booking has to be placed.</td>
    </tr>
    <tr>
      <td style="text-align:left">BookingNote</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Additional information about the order.</td>
    </tr>
  </tbody>
</table>

#### FlexibleStopAssignment <a id="network-FlexibleStopAssignment.1"></a>

Link between [ScheduledStopPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ScheduledStopPoint) and [FlexibleStopPlace.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleStopPlace)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleStopAssignment)

_Defined in ServiceFrame_

| FlexibleStopAssignment &lt; [StopAssignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#StopAssignment) &lt; [Assignment]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| FlexibleStopPlaceRef | FlexibleStopPlaceRef | 1: 1 | Reference to [FlexibleStopPlace](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace) |

### Transfers <a id="network-Transfers"></a>

#### Transfer <a id="network-Transfer"></a>

An abstract type describing physical opportunity to come from one place to another. _Not to be confused with_ [_Interchange._](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Interchange)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Transfer)

| Transfer &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Name | [MultilingualString]() | 0: 1 | Name of the transfer |
| Description | [MultilingualString]() | 0: 1 | Textual description |
| Distance | xsd:decimal | 1: 1 | Total length for transfer \(in meters\) |
| TransferDuration | [TransferDuration](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#TransferDuration) | 1: 1 | Detailed description for duration transfer |
| BothWays | xsd:boolean | 0: 1 | Specifies whether the transfer is possible in both directions |

**TransferDuration**

Specification of the duration of a transfer based on the type of traveller.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TransferDuration)

| TransferDuration |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| DefaultDuration | xsd:duration | 1: 1 | Normal duration |
| FrequentTravellerDuration | xsd:duration | 0: 1 | The time it will take a person with local knowledge to complete the transfer \(commuter\) |
| OccasionalTravellerDuration | xsd:duration | 0: 1 | The time it will take a person unfamiliar with the place to complete the transfer \(tourist etc.\) |
| MobilityRestrictedTravellerDuration | xsd:duration | 0: 1 | The time it will take a person with special needs to complete the transfer |

