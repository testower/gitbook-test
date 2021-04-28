# Håndbok N801 \(SIRI/NeTEX\) : SIRI-ET

**The Service Interface for Real Time Information - Estimated Timetable**

Version

Current version for **SIRI-ET** is:   **v1.1**  \(_last changed_ 01 Dec 2020 \)

## Content <a id="SIRI-ET-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591773172 {padding: 0px;}  
div.rbtoc1619591773172 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591773172 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Content](handbok-n801-siri-netex-siri-et.md#SIRI-ET-Content)
* [Data requirements](handbok-n801-siri-netex-siri-et.md#SIRI-ET-Datarequirements)
* [Components](handbok-n801-siri-netex-siri-et.md#SIRI-ET-Components)
  * [EstimatedTimetableDelivery](handbok-n801-siri-netex-siri-et.md#SIRI-ET-EstimatedTimetableDelivery)
    * [EstimatedTimetableDelivery](handbok-n801-siri-netex-siri-et.md#SIRI-ET-EstimatedTimetableDelivery.1)
    * [EstimatedJourneyVersionFrame](handbok-n801-siri-netex-siri-et.md#SIRI-ET-EstimatedJourneyVersionFrame)
    * [EstimatedVehicleJourney](handbok-n801-siri-netex-siri-et.md#SIRI-ET-EstimatedVehicleJourney)
    * [SimpleContactStructure](handbok-n801-siri-netex-siri-et.md#SIRI-ET-SimpleContactStructure)
    * [SituationRefStructure](handbok-n801-siri-netex-siri-et.md#SIRI-ET-SituationRefStructure)
    * [RecordedCall](handbok-n801-siri-netex-siri-et.md#SIRI-ET-RecordedCall)
    * [RecordedCallStructure](handbok-n801-siri-netex-siri-et.md#SIRI-ET-RecordedCallStructure)
    * [EstimatedCall](handbok-n801-siri-netex-siri-et.md#SIRI-ET-EstimatedCall)
    * [EstimatedCallStructure](handbok-n801-siri-netex-siri-et.md#SIRI-ET-EstimatedCallStructure)
    * [StopAssignmentStructure](handbok-n801-siri-netex-siri-et.md#SIRI-ET-StopAssignmentStructure)

This document is part of the Norwegian SIRI Profile and describes datasets and elements used for exchanging **continuous changes to planned data within the same calendar day** in the **SIRI Estimated Timetable \(ET\)** real-time format.

SIRI-ET is used to model the status of existing VehicleJourneys and to ensure that deviations from the planned data \(within the same operational day\) such as cancellations, additional departures, delays, detours and changes in stops, can be published on short notice. The data is linked to objects in the planned data by use of ID's, which ensures data quality.

## Data requirements <a id="SIRI-ET-Datarequirements"></a>

Sending a _ServiceDelivery_ of SIRI-ET data must be in accordance with this profile and the **entire dataset should be contained within a** _**single XML file**_.

When sending _Estimated Timetable_ data, information should **always contain all stops**, that is **all served** _EstimatedCalls_ when relevant _RecordedCalls_ \(and _IsCompleteStopSequence_ = 'true'\)

It is permitted for client systems to send more than one _EstimatedVehicleJourney_ per _EstimatedTimetableDelivery_, in order for real-time information to be conflated and be transferred as part of the same _ServiceDelivery_. Note that the profile does not present an exhaustive list of all real-time information technically possible to transfer via SIRI-ET, but it lays the foundation for which demands are placed on the datasets in order to meet the demands set by [Håndbok N801](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370406/H+ndbok+N801).

The [examples](handbok-n801-siri-netex-siri-examples-catalogue.md) associated with this profile are meant to show practical implementations of specific use cases, and can contain supplementary, lack certain data fields, or contain optional data, compared to a full and complete dataset. See [SIRI-ET\#Components](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-Components) for closer descriptions of the data types, specifications and requirements on the unique elements of the SIRI-ET-data.

## Components <a id="SIRI-ET-Components"></a>

### EstimatedTimetableDelivery <a id="SIRI-ET-EstimatedTimetableDelivery"></a>

#### EstimatedTimetableDelivery <a id="SIRI-ET-EstimatedTimetableDelivery.1"></a>

A data type for representing information about time table changes for one or more VehicleJourneys within the same operational day.

| EstimatedTimetableDelivery &lt; [ServiceDelivery](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-ServiceDelivery) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| attribute | version | xsd:NMTOKEN | 1: 1 | Version ID for EstimatedTimetableDelivery. |
| element | ResponseTimestamp | xsd:dateTime | 1: 1 | Timestamp for when the dataset was created/published. |
| element | EstimatedJourneyVersionFrame | [SIRI-ET\#EstimatedJourneyVersionFrame](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-EstimatedJourneyVersionFrame) | 1: \* | A container element for sending one or more _Estimated Timetable_ with a timestamp. |

#### EstimatedJourneyVersionFrame <a id="SIRI-ET-EstimatedJourneyVersionFrame"></a>

Container-element for returning an _Estimated Timetable_ comprised of one or more _EstimatedVehicleJourney._

| EstimatedJourneyVersionFrame |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | RecordedAtTime | xsd:dateTime | 1: 1 | The time when the data object was created/published. |
| element | EstimatedVehicleJourney | [SIRI-ET\#EstimatedVehicleJourney](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-EstimatedVehicleJourney) | 1: \* | Object for _Estimated Timetable_ dataset. |

#### EstimatedVehicleJourney <a id="SIRI-ET-EstimatedVehicleJourney"></a>

Continuously updated timetable data with changes in the current operating day for a VehicleJourney \(may also include a reference to a Vehicle\), and its estimated arrival times at stops.

<table>
  <thead>
    <tr>
      <th style="text-align:left">EstimatedVehicleJourney</th>
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
      <td style="text-align:left">RecordedAtTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">The time when this individual journey was recorded.</td>
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
      <td style="text-align:left">DirectionRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Direction reference.</p>
        <p><em>Please note that the field is implemented as mandatory, but is not used as a free standing data type in the Norwegian SIRI profile. If it is not used, this value can be set to 0 (zero).</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">FramedVehicleJourneyRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-FramedVehicleJourneyRefStructure">FramedVehicleJourneyRefStructure</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference with date to VehicleJourney in question (<em>ID to the corresponding object in the timetable data</em>).</td>
    </tr>
    <tr>
      <td style="text-align:left">EstimatedVehicleJourneyCode</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">
        <p>Un-affected replacement departures must be given a new codespace-unique
          ID.</p>
        <p>For example: <code>RUT:ServiceJourney:51-108833-11872056-00</code>
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">ExtraJourney</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The VehicleJourney in question is a replacement departure.</p>
        <p><em>Must be &apos;true&apos; if it is a replacement departure.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Cancellation</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">
        <p>Used when the VehicleJourney in question is cancelled.</p>
        <p><em>Set to &apos;true&apos; only if the whole VehicleJourney is cancelled. When only parts of the VehicleJourney is cancelled: use</em>  <em>RecordedCall and/or EstimatedCall.</em>
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">JourneyPatternRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to JourneyPattern in question (<em>ID to the corresponding object in the timetable data</em>).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleMode</td>
      <td style="text-align:left">VehicleModesEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Transport type.</p>
        <p><em>Must be defined for replacement departures!</em>
        </p>
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
      <td style="text-align:left">RouteRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to Route in question (<em>ID to the corresponding object in the timetable data</em>).</p>
        <p><em>Must be defined for replacement departures!</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PublishedLineName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Public number or name of the line.</p>
        <p>Is only used when <em>replacement departures</em> reference a new LineRef
          that is not already defined in timetable data. It will then be used to
          represent the added Line.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">GroupOfLinesRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to Network/GroupOfLines in question (<em>ID to the corresponding object in the timetable data</em>).</p>
        <p><em>Must be defined for replacement departures!</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExternalLineRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to Line in question (<em>ID to the corresponding object in the timetable data</em>)
          that the departure replaces. If not provided, the value from LineRef will
          be used.</p>
        <p><em>Must be defined for replacement departures!</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">OriginName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Name of the first stop of the departure (not used due to the reference
        to the national stop place registry, however <em>can</em> be included to
        make the XML easier to read).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DestinationName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Name of the last stop of the departure (not used due to the reference
        to the national stop place registry, however <em>can</em> be included to
        make the XML easier to read).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">OperatorRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to Operator in question (ID to the corresponding company in
          the timetable data)</p>
        <p><em>Must be defined for replacement departures where the operator has been changed!</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PublicContact</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-SimpleContactStructure">SIRI-ET#SimpleContactStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Contact point for the public (if different from original timetable information).</p>
        <p><em>At least one field must be filled out.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">OperationsContact</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-SimpleContactStructure">SIRI-ET#SimpleContactStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Administrative contact details (if different from original timetable information).</p>
        <p><em>At least one field must be filled out.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SituationRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-SituationRefStructure">SIRI-ET#SituationRefStructure</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Unique reference to one or more <em>SituationNumber</em> which link to earlier
        published Situation elements (SIRI-SX) when these provide <em>supplementary information</em> for
        the current EstimatedVehicleJourney.</td>
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
      <td style="text-align:left">PredictionInaccurate</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the VehicleJourney is affected by traffic jams or other circumstances
        which lead to uncertainty around the time estimates.</td>
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
      <td style="text-align:left">BlockRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to block (<em>trip pattern</em>)</p>
        <p><em>Internal (non-public) information.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleJourneyRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to the VehicleJourney being replaced (<em>ID to the corresponding object in the timetable data</em>).</p>
        <p>Please note: Use only for unplanned replacement departures. In other cases,
          use FramedVehicleJourneyRef.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">AdditionalVehicleJourneyRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Reference to other affected VehicleJourneys.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RecordedCalls</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-RecordedCall">SIRI-ET#RecordedCall</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The full sequence of already served stops in the order they were served
          by the VehicleJourney.</p>
        <p><em>Please note that all stops in the sequence must be in chronological order. (Except if the recording of a call is missed, then this call may be kept in the sequence as a correspondingly labeled EstimatedCall even after passed.)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">EstimatedCalls</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-EstimatedCall">SIRI-ET#EstimatedCall</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The full sequence of affected stops in the order they <b>will be</b> served
          by the VehicleJourney.</p>
        <p><em>Please note that all stops in the sequence must be in chronological order.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IsCompleteStopSequence</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Should always be &apos;true&apos; as a confirmation that the sequence
        of RecordedCalls/EstimatedCalls is complete (contains all the stops) for
        the current EstimatedVehicleJourney.</td>
    </tr>
  </tbody>
</table>

#### SimpleContactStructure <a id="SIRI-ET-SimpleContactStructure"></a>

Contact details to be presented to the public in cases where the information stated in the planned time table data is no longer true.

| SimpleContactStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | PhoneNumber | xsd:string | 0: 1 | Phone number |
| element | Url | xsd:anyURI | 0: 1 | Url |

#### SituationRefStructure <a id="SIRI-ET-SituationRefStructure"></a>

Reference to a related [Situation Element](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370605/SIRI-SX#SIRI-SX-PtSituationElement) in an existing [SIRI-SX](handbok-n801-siri-netex-siri-sx.md) message.

| SituationRefStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | SituationSimpleRef | xsd:string | 1: 1 | Unique referance to _SituationNumber_ for previously published [Situation Element](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370605/SIRI-SX#SIRI-SX-PtSituationElement) \([SIRI-SX](handbok-n801-siri-netex-siri-sx.md)\) |

#### RecordedCall <a id="SIRI-ET-RecordedCall"></a>

Wrapper object to describe information regarding already served stops in a VehicleJourney.

_Specified RecordedCalls must, together with EstimadeCalls, define **all** stops of a complete EstimatedVehicleJourney \(that is, IsCompleteStopSequence should always be 'true'\)._

| RecordedCall |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | RecordedCall | [SIRI-ET\#RecordedCallStructure](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-RecordedCallStructure) | 1: 1 | Description |

#### RecordedCallStructure <a id="SIRI-ET-RecordedCallStructure"></a>

Data structure with information regarding already served stops.

<table>
  <thead>
    <tr>
      <th style="text-align:left">RecordedCall</th>
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
      <td style="text-align:left">Reference to actually served Quay. (ID to the corresponding Quay in the
        timetable data and national stop place registry).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Order</td>
      <td style="text-align:left">xsd:positiveInteger</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Which number in the sequence of served stops this <em>RecordedCall</em> is
          describing.</p>
        <p><em>Please not that the sequence must contain <b>all</b> described stops (Call), that is Order must be a continuous sequence from registered RecordedCall to upcoming EstimatedCall.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StopPointName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Name (one per language).</td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">ExtraCall</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the served stop is in addition to the planned stop sequence.</td>
    </tr>
    <tr>
      <td style="text-align:left">Cancellation</td>
      <td style="text-align:left">
        <p>Whether this is a cancellation of a planned stop.</p>
        <p><em>Only used when the stop was not served, either for boarding or alighting.</em>
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
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
      <td style="text-align:left">AimedArrivalTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Originally planned arrival time. Required, except for the first stop.</td>
    </tr>
    <tr>
      <td style="text-align:left">element
        <br />(choice)</td>
      <td style="text-align:left">ActualArrivalTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Actual arrival time. Required, except for the first stop.</td>
    </tr>
    <tr>
      <td style="text-align:left">ExpectedArrivalTime</td>
      <td style="text-align:left">
        <p>Estimated arrival time.</p>
        <p><em>Only to be used if the corresponding </em><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-EstimatedCall"><em>SIRI-ET#EstimatedCall</em></a><em> was recorded with ArrivalStatus &quot;missed&quot; and/or the ActualArrivalTime of this RecordedCall is unknown/void, due to the Call not being served despite planned or arrival data for the served Call was not recorded.<br /><b>NB: </b>As the</em> ArrivalStatus<em> field is currently <b>not</b> available in the RecordedCall data object (will be added in the SIRI v2.1 update, expected Q2/Q3 2020), maintaining the ExpectedArrivalTime in a RecordedCall implicitly states that the ActualArrivalTime is unavailable and that the arrival can be handled as if &quot;missed&quot;.</em>
          <br
          />
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">AimedDepartureTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Originally planned departure time. Required, except for the last stop.</td>
    </tr>
    <tr>
      <td style="text-align:left">element
        <br />(choice)</td>
      <td style="text-align:left">ActualDepartureTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Actual departure time. Required, except for the last stop.<em><br /></em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ExpectedDepartureTime</td>
      <td style="text-align:left">
        <p>Estimated departure time.</p>
        <p><em>Only to be used if the corresponding </em><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-EstimatedCall"><em>SIRI-ET#EstimatedCall</em></a><em> was recorded with DepartureStatus &quot;missed&quot; and/or the ActualDepartureTime of this RecordedCall is unknown/void, due to the Call not being served despite planned or departure data for the served Call was not recorded.<br /><b>NB: </b>As the</em> DepartureStatus<em> field is currently <b>not</b> available in the RecordedCall data object (will be added in the SIRI v2.1 update, expected Q2/Q3 2020), maintaining the ExpectedDepartureTime in a RecordedCall implicitly states that the ActualDepartureTime is unavailable and that the departure can be handled as if &quot;missed&quot;.</em>
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### EstimatedCall <a id="SIRI-ET-EstimatedCall"></a>

Wrapper object for describing a stop which will be served in a VehicleJourney.

_Specified EstimatedCalls_ _must, together with RecordedCalls_, define **all** stops of a complete _EstimatedVehicleJourney \(that is, IsCompleteStopSequence should always be 'true'\)._

| EstimatedCall |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | EstimatedCall | [SIRI-ET\#EstimatedCallStructure](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-EstimatedCallStructure) | 1: 1 | Description  |

#### EstimatedCallStructure <a id="SIRI-ET-EstimatedCallStructure"></a>

Data structure information about stops which will be served, in chronological sequence.

<table>
  <thead>
    <tr>
      <th style="text-align:left">EstimatedCall</th>
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
      <td style="text-align:left">Reference to the StopPlace in question (ID corresponding to objects in
        the national stop place registry).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Order</td>
      <td style="text-align:left">xsd:positiveInteger</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Which number in the sequence of served stops this <em>EstimatedCall </em>is
        describing.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StopPointName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Name (one per language).</td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">ExtraCall</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the served stop is in addition to the planned stop sequence.</td>
    </tr>
    <tr>
      <td style="text-align:left">Cancellation</td>
      <td style="text-align:left">
        <p>Whether this is a cancellation of a planned stop.</p>
        <p><em>Only used when the stop was not served, either for boarding or alighting.</em>
        </p>
        <p><em>When partially cancelled departures the last stop before the cancellation part is defined with DepartureStatus &apos;cancelled&apos;, while the first stop in the cancellation part is defined with ArrivalStatus &apos;cancelled&apos;. The remaining non-served stops (the partial cancellation) are defined with</em>  <em>Cancellation &apos;true&apos;.</em>
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PredictionInaccurate</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the VehicleJourney is affected by traffic jams or other circumstances
        which lead to uncertainty around the time estimates <em>for this call</em>.
        When the whole VehicleJourney is uncertain, this should instead be set
        on EstimatedVehicleJourney.</td>
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
      <td style="text-align:left">RequestStop</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the passenger must signal the vehicle for the stop to be served.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DestinationDisplay</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>The (destination) text displayed on the vehicle when arriving at a stop.</p>
        <p><em>If this is <b>not</b> defined the original text of the departure will be used.</em>
        </p>
        <p>Please note that the text field <b>must</b> be defined in cases of ExtraJourney
          or when overriding a destination text from the planned timetable data.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SituationRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-SituationRefStructure">SIRI-ET#SituationRefStructure</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">One or more <em>SituationNumber</em> linking to already published SIRI-SX
        messages for the Call in question.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">AimedArrivalTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Originally planned arrival time. Required, except for the first stop.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExpectedArrivalTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Estimated arrival time. Required, except for the first stop.</p>
        <p><em>When the estimated ArrivalStatus is &quot;missed&quot;, the ExpectedArrivalTime can be empty.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ArrivalStatus</td>
      <td style="text-align:left">CallStatusEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Status for arrival</p>
        <p>Possible values:</p>
        <ul>
          <li>arrived</li>
          <li>cancelled</li>
          <li>delayed</li>
          <li>early</li>
          <li>missed</li>
          <li>onTime</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ArrivalBoardingActivity</td>
      <td style="text-align:left">ArrivalBoardingActivityEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Used when there are changes in the boarding restrictions (must be in accordance
          with ArrivalStatus).</p>
        <p>Possible values:</p>
        <ul>
          <li>alighting</li>
          <li>noAlighting</li>
          <li>passThru</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ArrivalStopAssignment</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-StopAssignmentStructure">SIRI-ET#StopAssignmentStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Assigned arrival place (Quay).</p>
        <p><em>When necessary <b>either</b> the ArrivalStopAssignment <b>or</b> DepartureStopAssignment, are defined, but never both</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">AimedDepartureTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Originally planned departure time. Required, except for the last stop.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExpectedDepartureTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Estimated departure time. Required, except for the last stop.</p>
        <p><em>When the estimated DepartureStatus is &quot;missed&quot;, the ExpectedDepartureTime can be empty.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DepartureStatus</td>
      <td style="text-align:left">CallStatusEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Status for departure.</p>
        <p>Possible values:</p>
        <ul>
          <li>cancelled</li>
          <li>delayed</li>
          <li>missed</li>
          <li>onTime</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DepartureBoardingActivity</td>
      <td style="text-align:left">DepartureBoardingActivityEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Used when there are changes in the boarding restrictions (assuming this
          is not the final stop. Must be in accordance with ArrivalStatus).</p>
        <p>Possible values:</p>
        <ul>
          <li>boarding</li>
          <li>noBoarding</li>
          <li>passThru</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DepartureStopAssignment</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370392#SIRI-ET-StopAssignmentStructure">SIRI-ET#StopAssignmentStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Assigned departure place (Quay).</p>
        <p><em>When necessary <b>either</b> the ArrivalStopAssignment <b>or</b> DepartureStopAssignment, is defined, but never both</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### StopAssignmentStructure <a id="SIRI-ET-StopAssignmentStructure"></a>

Assignment of stop place \(Quay\).

| StopAssignmentStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | AimedQuayRef | xsd:NMTOKEN | 1: 1 | Reference to originally planned Quay \(ID corresponding to objects in the national stop place registry\). |
| element | ExpectedQuayRef | xsd:NMTOKEN | 0: 1 | Reference to expected/current Quay \(ID corresponding to objects in the national stop place registry\), when there are changes. |

