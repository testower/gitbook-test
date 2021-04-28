# Håndbok N801 \(SIRI/NeTEX\) : SIRI-VM

**The Service Interface for Real Time Information - Vehicle Monitoring**

Version

Current version for **SIRI-VM** is:   **v1.1**  \(_last changed_ 07 Oct 2020 \)

## Content <a id="SIRI-VM-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591773404 {padding: 0px;}  
div.rbtoc1619591773404 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591773404 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Content](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-Content)
* [Data requirements](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-Datarequirements)
* [Components](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-Components)
  * [VehicleMonitoringDelivery](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-VehicleMonitoringDelivery)
    * [VehicleMonitoringDelivery](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-VehicleMonitoringDelivery.1)
    * [VehicleActivity](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-VehicleActivity)
    * [ProgressBetweenStops](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-ProgressBetweenStops)
    * [MonitoredVehicleJourney](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-MonitoredVehicleJourney)
    * [Location](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-Location)
    * [MonitoredCallStructure](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-MonitoredCallStructure)

This document is part of the Norwegian SIRI Profile and describes datasets and elements used for exchanging **updates on position and status, as well as estimated delays** in the **SIRI Vehicle Monitoring \(VM\)** real-time format.

SIRI-VM is used to model vehicle-movements and their progress compared to a planned timetable. The data is linked to objects in the planned data by use of ID's, which ensures data quality.

## Data requirements <a id="SIRI-VM-Datarequirements"></a>

Sending a _ServiceDelivery_ of SIRI-VM data must be in accordance with this profile and the **entire dataset should be contained within a** _**single XML file**_.

When sending _Vehicle Monitoring_ data, information should be limited to **contain only** the _MonitoredCall_, that is the previous or current stop \(and _IsCompleteStopSequence_ = 'false'\)

Note that the profile does not present an exhaustive list of all real-time information technically possible to transfer via SIRI-VM, but it lays the foundation for which demands are placed on the datasets in order to meet the demands set by [Håndbok N801](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370406/H+ndbok+N801).

It is permitted for client systems to send more than one _VehicleActivity_ per _VehicleMonitoringDelivery_, in order for real-time information to be conflated and be transferred as part of the same _ServiceDelivery_.

The [examples](handbok-n801-siri-netex-siri-examples-catalogue.md) associated with this profile are meant to show practical implementations of specific use cases, and can contain supplementary, lack certain data fields, or contain optional data, compared to a full and complete dataset. See [Components](handbok-n801-siri-netex-siri-vm.md#SIRI-VM-Components)  for closer descriptions of the data types, specifications and requirements on the unique elements of the SIRI VM-data.

It is a fundamental requirement that valid timetable data \(as NeTEx or SIRI-ET-data\) is delivered **before** sending in position- and status information as SIRI-VM.

## Components <a id="SIRI-VM-Components"></a>

### VehicleMonitoringDelivery <a id="SIRI-VM-VehicleMonitoringDelivery"></a>

#### VehicleMonitoringDelivery <a id="SIRI-VM-VehicleMonitoringDelivery.1"></a>

A data type for representing vehicle monitoring \(for estimated adjustment of times\) for one or more _VehicleJourneys_.

| VehicleMonitoringDelivery &lt; [ServiceDelivery](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-ServiceDelivery) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| attribute | version | xsd:NMTOKEN | 1: 1 | Version ID for EstimatedTimetableDelivery |
| element | ResponseTimestamp | xsd:dateTime | 1: 1 | Timestamp for when the dataset was created/published. |
| element | VehicleActivity | [SIRI-VM\#VehicleActivity](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370425#SIRI-VM-VehicleActivity) | 1: \* | A container element for sending one or more _VehicleActivity_ with a timestamp. |

#### VehicleActivity <a id="SIRI-VM-VehicleActivity"></a>

Container-element for  returning one or more _VehicleActivity._

| VehicleActivity |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | RecordedAtTime | xsd:dateTime | 1: 1 | Timestamp for when the dataset was created/published. |
| element | ValidUntilTime | xsd:dateTime | 1: 1 | Validity-expiration date and time of the dataset. |
| element | ProgressBetweenStops | [ SIRI-VM\#ProgressBetweenStops](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370425#SIRI-VM-ProgressBetweenStops) | 0: 1 | Information on the progress of the vehicle between stops. |
| element | MonitoredVehicleJourney | [SIRI-VM\#MonitoredVehicleJourney](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370425#SIRI-VM-MonitoredVehicleJourney) | 1: 1 | Data object for a real-time monitored _VehicleJourney_.  |

#### ProgressBetweenStops <a id="SIRI-VM-ProgressBetweenStops"></a>

Information on the progress of the vehicle along the current _ServiceLink_, i.e. between the previous and the next _ScheduledStopPoint_. 

<table>
  <thead>
    <tr>
      <th style="text-align:left">ProgressBetweenStops</th>
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
      <td style="text-align:left">element</td>
      <td style="text-align:left">Percentage</td>
      <td style="text-align:left">xsd:decimal</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">How much of the total distance (percentage) that has been traversed at
        the time of the message.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">LinkDistance</td>
      <td style="text-align:left">xsd:decimal</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Distance in meters between the previous stop (or <em>current</em>, if located
          at stop) and the next stop.</p>
        <p><em>Corresponds to Distance for current ServiceLink, when available.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### MonitoredVehicleJourney <a id="SIRI-VM-MonitoredVehicleJourney"></a>

Data objects with elements to describe a real-time monitored VehicleJourney, including supplementary locational information, and data about the previous/current stop.

_Used to enrich existing timetable data._

<table>
  <thead>
    <tr>
      <th style="text-align:left">MonitoredVehicleJourney</th>
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
      <td style="text-align:left">element</td>
      <td style="text-align:left">LineRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to the Line in question (<em>ID to the corresponding object in the timetable data</em>)</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">FramedVehicleJourneyRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/General+information+SIRI#GeneralinformationSIRI-FramedVehicleJourneyRefStructure">FramedVehicleJourneyRefStructure</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to VehicleJourney in question. Has a date.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleMode</td>
      <td style="text-align:left">VehicleModesEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Transport types</p>
        <p>Possible values:</p>
        <ul>
          <li>air</li>
          <li>bus</li>
          <li>coach</li>
          <li>ferry (<em>mapped to &quot;water&quot;</em>)</li>
          <li>metro</li>
          <li>rail</li>
          <li>tram</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">OperatorRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to Operator in question (ID to the corresponding company in
        the timetable data)</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">OriginRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to origin Quay in question (ID to the corresponding Quay in
        the timetable data and national stop place registry)</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">OriginName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/General+information+SIRI#GeneralinformationSIRI-NaturalLanguagePlaceNameStructure">NaturalLanguagePlaceNameStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Name describing the origin of the departure.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DestinationRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to destination Quay in question (ID to the corresponding Quay
        in the timetable data and national stop place registry)</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DestinationName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/General+information+SIRI#GeneralinformationSIRI-NaturalLanguagePlaceNameStructure">NaturalLanguagePlaceNameStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Name describing the destination of the departure.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Monitored</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the vehicle is currently reporting real-time data or not (for
        example set to <em>true</em> when the driver of the vehicle logs on to the
        system before departing).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DataSource</td>
      <td style="text-align:left">xsd:string</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Codespace of the data source (see <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370434/List+of+current+Codespaces">codespace</a>).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleLocation</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370425#SIRI-VM-Location">SIRI-VM#Location</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">The position of a vehicle as a geospatial point.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Bearing</td>
      <td style="text-align:left">xsd:float</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Current compass bearing (direction of VehicleJourney)</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Occupancy</td>
      <td style="text-align:left">OccupancyEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Open seats-status.</p>
        <p>Possible values:</p>
        <ul>
          <li>unknown</li>
          <li>manySeatsAvailable (<em>more than ~50% of seats available</em>)</li>
          <li>seatsAvailable (<em>less than ~50% of seats available</em>)</li>
          <li>standingAvailable (<em>less than ~10% of seats available</em>)</li>
          <li>full (<em>close to or at full capacity</em>)</li>
          <li>notAcceptingPassengers (<em>if vehicle/carriage is not in use / unavailable, or passengers are only allowed to alight due to e.g. crowding</em>)</li>
        </ul>
        <p><em>This status should reflect the allowed occupancy level, not necessarily physical spacing available.</em>
        </p>
        <p><em>If the operator runs with reduced capacity, e.g. in order to maintain a certain service level, social distancing etc., the occupancy status must be set in accordance with current limitation i.e. &quot;full&quot; when all seats assigned for use are occupied (regardless of disallowed seating/standing still being physically available).</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Delay</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Delay-time.</p>
        <p><em>Defined as &quot;PT0S&quot; (0 seconds) when there are no delays.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">InCongestion</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the vehicle is affected by traffic jams or other circumstances
        which may lead to further delays.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleStatus</td>
      <td style="text-align:left">VehicleStatusEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Vehicle status.</p>
        <p>Possible values:</p>
        <ul>
          <li>assigned (<em>a vehicle has been assigned, but not yet deployed</em>)</li>
          <li>atOrigin (<em>VehicleJourney has not begun, the vehicle is still at the first stop</em>)</li>
          <li>cancelled</li>
          <li>completed (<em>verification that the VehicleJourney has been completed</em>)</li>
          <li>inProgress</li>
          <li>offRoute (<em>VehicleJourney is taking a detour</em>)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to the vehicle in question (ID to the corresponding vehicle
        in the timetable data).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MonitoredCall</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370425#SIRI-VM-MonitoredCallStructure">SIRI-VM#MonitoredCallStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Information on the most recent (if en route) or current (if stopped) call
        made at a stop for a <em>VehicleJourney</em>.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IsCompleteStopSequence</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left"><b>Always</b> set to &apos;false&apos; when the submitted data only contains
        MonitoredCall.</td>
    </tr>
  </tbody>
</table>

#### Location <a id="SIRI-VM-Location"></a>

Specifies location of something.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Location</th>
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
      <td style="text-align:left">attribute</td>
      <td style="text-align:left">srsName</td>
      <td style="text-align:left">xsd:string</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The reference system for longitude and latitude. If stated, use <code>WGS84</code> or
        if necessary a valid coordinate-reference to the standard used (for example
        &quot;<code>EPSG:4326</code>&quot;).</td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">
        <p>Longitude</p>
        <p>Latitude</p>
      </td>
      <td style="text-align:left">
        <p>xsd:decimal</p>
        <p>xsd:decimal</p>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Longitude (-180 to 180)</p>
        <p>Latitude (-90 to 90)</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Coordinates</td>
      <td style="text-align:left">xsd:NMTOKENS</td>
      <td style="text-align:left">
        <p>Location coordinates.</p>
        <p>For example: <code>&lt;gml: pos srsName=&quot;urn:ogc:def:crs:EPSG::4326&quot;&gt; -59.123 -45.1254 &lt;/gml:pos&gt;</code>
        </p>
        <p><em>Note! The stop place registry only accepts WGS84-coordinates.</em>
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### MonitoredCallStructure <a id="SIRI-VM-MonitoredCallStructure"></a>

Information regarding the current stop for VehicleJourney \(the stop the vehicle is headed to or has stopped at.

<table>
  <thead>
    <tr>
      <th style="text-align:left">MonitoredCallStructure</th>
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
      <td style="text-align:left">element</td>
      <td style="text-align:left">StopPointRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to the Quay in question (ID corresponding to objects in the
        national stop place registry).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StopPointName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/General+information+SIRI#GeneralinformationSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Name of the stop (not used due to the reference to the national stop place
        registry, but <em>can</em> be included to make the XML easier to read).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleAtStop</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the vehicle is at the stop.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleLocationAtStop</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370425#SIRI-VM-Location">SIRI-VM#Location</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Where the vehicle is at the stop.</p>
        <p>Used for significant deviations from planned and published information.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DestinationDisplay</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/General+information+SIRI#GeneralinformationSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Destination text (information only, not to be used for override but <em>can</em> be
        included to make the XML easier to read).</td>
    </tr>
  </tbody>
</table>

