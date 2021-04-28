# Håndbok N801 \(SIRI/NeTEX\) : timetable

## Version <a id="timetable-Version"></a>

Current version for **timetable** is:   **v1.3**   \(last changed 29 Aug 2018\) 

## Content <a id="timetable-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591705394 {padding: 0px;}  
div.rbtoc1619591705394 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591705394 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Version](handbok-n801-siri-netex-timetable.md#timetable-Version)
* [Components](handbok-n801-siri-netex-timetable.md#timetable-Components)
  * [Journey](handbok-n801-siri-netex-timetable.md#timetable-Journey)
    * [Journey](handbok-n801-siri-netex-timetable.md#timetable-Journey.1)
    * [JourneyEndpointStructure](handbok-n801-siri-netex-timetable.md#timetable-JourneyEndpointStructure)
  * [Types of journey](handbok-n801-siri-netex-timetable.md#timetable-Typesofjourney)
    * [VehicleJourney](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourney)
      * [JourneyPart](handbok-n801-siri-netex-timetable.md#timetable-JourneyPart)
      * [Frequency](handbok-n801-siri-netex-timetable.md#timetable-Frequency)
      * [VehicleJourneyWaitTime](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourneyWaitTime)
      * [VehicleJourneyRunTime](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourneyRunTime)
      * [VehicleJourneyHeadway](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourneyHeadway)
      * [TimetabledPassingTime](handbok-n801-siri-netex-timetable.md#timetable-TimetabledPassingTime)
    * [ServiceJourney](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney)
      * [FlexibleServiceProperties](handbok-n801-siri-netex-timetable.md#timetable-FlexibleServiceProperties)
    * [DeadRun](handbok-n801-siri-netex-timetable.md#timetable-DeadRun)
    * [Periodical journeys](handbok-n801-siri-netex-timetable.md#timetable-Periodicaljourneys)
      * [TemplateVehicleJourney](handbok-n801-siri-netex-timetable.md#timetable-TemplateVehicleJourney)
      * [TemplateServiceJourney](handbok-n801-siri-netex-timetable.md#timetable-TemplateServiceJourney)
      * [JourneyFrequencyGroup](handbok-n801-siri-netex-timetable.md#timetable-JourneyFrequencyGroup)
      * [RhythmicalJourneyGroup](handbok-n801-siri-netex-timetable.md#timetable-RhythmicalJourneyGroup)
      * [HeadwayJourneyGroup](handbok-n801-siri-netex-timetable.md#timetable-HeadwayJourneyGroup)
    * [Coupled journeys](handbok-n801-siri-netex-timetable.md#timetable-Coupledjourneys)
      * [CoupledJourney](handbok-n801-siri-netex-timetable.md#timetable-CoupledJourney)
      * [JourneyPartCouple](handbok-n801-siri-netex-timetable.md#timetable-JourneyPartCouple)
  * [ServiceCalendar](handbok-n801-siri-netex-timetable.md#timetable-ServiceCalendar)
  * [Interchange](handbok-n801-siri-netex-timetable.md#timetable-Interchange)
    * [Interchange across datasets](handbok-n801-siri-netex-timetable.md#timetable-Interchangeacrossdatasets)
    * [Interchange](handbok-n801-siri-netex-timetable.md#timetable-Interchange.1)
    * [ServiceJourneyInterchange](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourneyInterchange)

This document is part of NeTEx Norwegian Profile and describes data elements used for **calendar data** and **planned timetables** data exchange in the NeTEx format.

Note that the timetable-part of the profile describes elements for constructing time plans or time tables \(dates, times, frequencies etc.\) to be used in exchanging data between different systems, and representation of this information to travellers, based on the superordinate concept from the [network](handbok-n801-siri-netex-network.md)-profile document.

## Components <a id="timetable-Components"></a>

### Journey <a id="timetable-Journey"></a>

#### Journey <a id="timetable-Journey.1"></a>

An abstract type which describes a departure/journey.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Journey)

Examples in the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) \(_replacement transport_\)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Journey &lt; <a href>LinkSequence</a> &lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">Description</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Description of the departure</td>
    </tr>
    <tr>
      <td style="text-align:left">TransportMode</td>
      <td style="text-align:left">AllVehicleModesOfTransportEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Transport mode, see Mode in <a href>Transport Modes</a> for possible values
          (with accompanying submodes).</p>
        <p><em>Note that when overriding the mode for a Journey, <b>both</b> TransportMode and TransportSubmode must be specified.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">TransportSubmode</td>
      <td style="text-align:left">TransportSubmode</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Transport submode</p>
        <p>See <em>Submode</em> in <a href>Transport Modes</a> for possible values (<em>must be a submode of specified TransportMode</em>)</p>
        <p><em>Note that when overriding the mode for a Journey, <b>both</b> TransportMode and TransportSubmode must be specified.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ExternalVehicleJourneyRef</td>
      <td style="text-align:left">ExternalObjectRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference (ID) to original <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourney">ServiceJourney</a> when
          specifying replacement traffic.</p>
        <p><em>Note that replaced ServiceJourneys (if ID is referred to by ExternalVehicleJourneyRef) must also be part of the dataset (even in cases of partial delivery) to ensure the validity of the reference.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Monitored</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether real-time information is available for the departure.</td>
    </tr>
  </tbody>
</table>

#### JourneyEndpointStructure <a id="timetable-JourneyEndpointStructure"></a>

Description of the beginning,- or the destination of a [VehicleJourney](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney)

| JourneyEndpointStructure |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Name | [MultilingualString]()   | 0: 1 | Name |
| ScheduledStopPointRef | ScheduledStopPointRef | 0: 1 | Reference to [ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) |
| DestinationDisplayRef | DestinationDisplayRef | 0: 1 | Reference to [DestinationDisplay](handbok-n801-siri-netex-network.md#network-DestinationDisplay) |

### Types of journey <a id="timetable-Typesofjourney"></a>

#### VehicleJourney <a id="timetable-VehicleJourney"></a>

A planned journey from starting point to a destination, according to a [JourneyPattern](handbok-n801-siri-netex-network.md#network-JourneyPattern).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney)

<table>
  <thead>
    <tr>
      <th style="text-align:left">VehicleJourney &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Journey.1">Journey</a> &lt;
        <a
        href>LinkSequence</a>&lt; <a href>DataManagedObject</a> 
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
      <td style="text-align:left">Internal code (<em>non-public identifier</em>) for the journey (e.g. train-
        or trip number from the planners&apos; tool)</td>
    </tr>
    <tr>
      <td style="text-align:left">DepartureTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Time of departure for the journey.</td>
    </tr>
    <tr>
      <td style="text-align:left">Frequency</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Frequency">Frequency</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Frequency or interval for departures.</p>
        <p><em>Used <b>only</b> for frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">JourneyDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The total duration of the journey.</td>
    </tr>
    <tr>
      <td style="text-align:left">RouteRef</td>
      <td style="text-align:left">RouteRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to Route (<em>not mandatory for ServiceJourney, as this can be derived from JourneyPatternRef</em>)</td>
    </tr>
    <tr>
      <td style="text-align:left">PublicCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Public code or identifier for the journey</p>
        <p><em>Used only when for example the line number is changed per trip or has extraordinary overrides.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">waitTimes</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourneyWaitTime">VehicleJourneyWaitTime</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of wait times at <a href="handbok-n801-siri-netex-network.md#network-TimingPoint">TimingPoints</a>
        </p>
        <p><em>Normally used only when describing frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">runTimes</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourneyWaitTime">VehicleJourneyRunTime</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of run times between <a href="handbok-n801-siri-netex-network.md#network-TimingPoint">TimingPoints</a>
        </p>
        <p><em>Normally used only when describing frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">passingTimes</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#TimetabledPassingTime">TimetabledPassingTime</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">Description of planned passing times at <a href="handbok-n801-siri-netex-network.md#network-StopPoint">StopPoints</a> or
        <a
        href="handbok-n801-siri-netex-network.md#network-TimingPoint">TimingPoints</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">parts</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#JourneyPart">JourneyPart</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of the parts of the journey. Used in special cases such as combined
        journeys.</td>
    </tr>
  </tbody>
</table>

**JourneyPart**

A part of a journey, used for example when creating compound train journeys. 

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPart)

| JourneyPart &lt; [DataManagedObject]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Description | [MultilingualString]()   | 0: 1 | Description |
| MainPartRef | JourneyPartCoupleRef | 1: 1 | Reference to the main part of the journey |
| JourneyPartCoupleRef | JourneyPartCoupleRef | 0: 1 | Reference to [CoupledJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#CoupledJourney) to which this journey part belongs. |
| FromStopPointRef | ScheduledStopPointRef | 0: 1 | The starting point for the journey part \([ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint)\) |
| ToStopPointRef | ScheduledStopPointRef | 0: 1 | The destination for the journey part \([ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint)\) |
| StartTime | xsd:time | 1: 1 | Start-time |
| EndTime | xsd:time | 1: 1 | End-time |

**Frequency**

The frequency for a journey, i.e. the time interval between each departure in _frequency based_ traffic.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Frequency)

| Frequency &lt; [DataManagedObject]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| ScheduledHeadwayInterval | xsd:duration | 1: 1 | Planned departure interval |
| MinimumHeadwayInterval | xsd:duration | 0: 1 | Minimum departure interval |
| MaximumHeadwayInterval | xsd:duration | 0: 1 | Maximum departure interval |
| Description | [MultilingualString]()   | 0: 1 | Description, for example, "every 15 minutes" |

**VehicleJourneyWaitTime**

Waiting time at [TimingPoint](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TimingPoint) for a [VehicleJourney.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourneyWaitTime)

| VehicleJourneyWaitTime &lt; JourneyWaitTime &lt; [JourneyTiming]() &lt; VersionedChild  &lt; [EntityInVersion]()  &lt; [Entity]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| VehicleJourneyRef | VehicleJourneyRef | 0: 1 | Reference to [VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney) |

**VehicleJourneyRunTime**

Run time between [TimingPoints](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TimingPoint) for a [VehicleJourney.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourneyRunTime)

| VehicleJourneyRunTime &lt; JourneyRuntime &lt; [JourneyTiming]()  &lt; VersionedChild  &lt; [EntityInVersion]()  &lt; [Entity]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| VehicleJourneyRef | VehicleJourneyRef | 0: 1 | Reference to [VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney) |

**VehicleJourneyHeadway**

The interval between two [VehicleJourneys.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney)

_Used for frequency-based traffic._

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourneyHeadway)

| VehicleJourneyHeadway &lt; JourneyHeadway &lt; [JourneyTiming]()  &lt; VersionedChild  &lt; [EntityInVersion]()  &lt; [Entity]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| VehicleJourneyRef | VehicleJourneyRef | 0: 1 | Reference to [VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney) |

**TimetabledPassingTime**

Planned passing time at a [PointInJourneyPattern](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-PointInJourneyPattern) \([ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) or [TimingPoint](handbok-n801-siri-netex-network.md#network-TimingPoint)\) for a [VehicleJourney.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TimetabledPassingTime)

Examples in the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml)

**ALTERNATIVE 1: Ordinary timetable for planned journeys**

<table>
  <thead>
    <tr>
      <th style="text-align:left">TimetabledPassingTime &lt; PassingTime &lt; VersionedChild &lt; <a href>EntityInVersion</a> &lt;
        <a
        href>Entity</a>
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
      <td style="text-align:left">attr</td>
      <td style="text-align:left">id</td>
      <td style="text-align:left">ObjectIdType</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Unique id for the object</p>
        <p><em>Mandatory attribute</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">attr</td>
      <td style="text-align:left">version</td>
      <td style="text-align:left">VersionIdType</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Version number</p>
        <p><em>Mandatory attribute</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">PointInJourneyPatternRef</td>
      <td style="text-align:left">PointInJourneyPatternRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to <a href="handbok-n801-siri-netex-network.md#network-PointInJourneyPattern">PointInJourneyPattern</a> (the
        point being served/passed by the vehicle)</td>
    </tr>
    <tr>
      <td style="text-align:left">elem (choice)</td>
      <td style="text-align:left">
        <p>ArrivalTime</p>
        <p>ArrivalDayOffset</p>
      </td>
      <td style="text-align:left">
        <p>xsd:time</p>
        <p>DayOffsetType (xsd:integer)</p>
      </td>
      <td style="text-align:left">
        <p>1: 1</p>
        <p>0: 1</p>
      </td>
      <td style="text-align:left">
        <p>Planned arrival time (<em>if relevant, both ArrivalTime and DepartureTime <b>may</b> be specified</em>)</p>
        <p><em>ArrivalOffset relative to the</em>  <a href><em>OperatingDay</em></a>  <em>/</em> 
          <a
          href><em>Date</em>
            </a> <em>for the affected </em><a href="handbok-n801-siri-netex-timetable.md#timetable-VehicleJourney"><em>VehicleJourney(s)</em></a><em>, e.g. &quot;-1&quot; (previous day) or &quot;1&quot; (next day)</em>
            <br
            />
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>DepartureTime</p>
        <p>DepartureDayOffset</p>
      </td>
      <td style="text-align:left">
        <p>xsd:time</p>
        <p>DayOffsetType (xsd:integer)</p>
      </td>
      <td style="text-align:left">
        <p>1: 1</p>
        <p>0: 1</p>
      </td>
      <td style="text-align:left">
        <p>Planned departure time (<em>if relevant, both ArrivalTime and DepartureTime <b>may</b> be specified</em>)</p>
        <p><em>DepartureOffset relative to the</em>  <a href><em>OperatingDay</em></a>  <em>/</em> 
          <a
          href><em>Date</em>
            </a> <em>for the affected </em><a href="handbok-n801-siri-netex-timetable.md#timetable-VehicleJourney"><em>VehicleJourney(s)</em></a><em>, e.g. &quot;-1&quot; (previous day) or &quot;1&quot; (next day)</em>
        </p>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">WaitingTime</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Planned waiting time at a <a href>Point</a>
      </td>
    </tr>
  </tbody>
</table>

**ALTERNATIVE 2: On demand transport/FlexibleLines including hail and ride**

<table>
  <thead>
    <tr>
      <th style="text-align:left">TimetabledPassingTime &lt; PassingTime &lt; VersionedChild &lt; <a href>EntityInVersion</a> &lt;
        <a
        href>Entity</a>
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
      <td style="text-align:left">attr</td>
      <td style="text-align:left">id</td>
      <td style="text-align:left">ObjectIdType</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Unique id for the object</p>
        <p><em>Mandatory attribute</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">attr</td>
      <td style="text-align:left">version</td>
      <td style="text-align:left">VersionIdType</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Version number</p>
        <p><em>Mandatory attribute</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">PointInJourneyPatternRef</td>
      <td style="text-align:left">PointInJourneyPatternRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to <a href="handbok-n801-siri-netex-network.md#network-PointInJourneyPattern">PointInJourneyPattern</a> (the
        point being served/passed by the vehicle)</td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">WaitingTime</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Planned waiting time at a <a href>Point</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">LatestArrivalTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Latest possible (planned) arrival time (<em>if relevant, both LatestArrivalTime and EarliestDepartureTime <b>may</b> be specified</em>)</td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">LatestArrivalDayOffset</td>
      <td style="text-align:left">DayOffsetType (xsd:integer)</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Number of days of arrival relative to the journey start day <em>(only used when journey spans more than one calendar day)</em>
        </p>
        <p><em>ArrivalOffset relative to the</em>  <a href><em>OperatingDay</em></a><em>/</em>
          <a
          href><em>Date</em>
            </a> <em>for the affected </em><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney"><em>VehicleJourney(s)</em></a><em>, e.g. &quot;-1&quot; (previous day) or &quot;1&quot; (next day)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">EarliestDepartureTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Earliest possible departure time (<em>if relevant, both LatestArrivalTime and EarliestDepartureTime <b>may</b> be specified</em>)</td>
    </tr>
    <tr>
      <td style="text-align:left">elem</td>
      <td style="text-align:left">EarliestDepartureDayOffset</td>
      <td style="text-align:left">DayOffsetType (xsd:integer)</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Number of days of arrival relative to the journey start day <em>(only used when journey spans more than one calendar day)</em>
        </p>
        <p><em>DepartureOffset relative to the</em>  <a href><em>OperatingDay</em></a><em>/</em>
          <a
          href><em>Date</em>
            </a> <em>for the affected </em><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney"><em>VehicleJourney(s)</em></a><em>, e.g. &quot;-1&quot; (previous day) or &quot;1&quot; (next day)</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### ServiceJourney <a id="timetable-ServiceJourney"></a>

[VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney) with passengers. This is usually an ordinary departure according to the planned time table.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServiceJourney)

_Defined in TimetableFrame_

Examples in the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine863-with-interchange.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">ServiceJourney &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney">VehicleJourney</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Journey.1">Journey</a>&lt; <a href>LinkSequence</a> &lt; <a href>DataManagedObject</a> 
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
      <td style="text-align:left">ServiceAlteration</td>
      <td style="text-align:left">ServiceAlterationEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Journey type:</p>
        <ul>
          <li>extraJourney</li>
          <li>cancellation</li>
          <li>planned</li>
          <li>replaced (<em>by another new ServiceJourneys</em>)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DepartureTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Departure time</td>
    </tr>
    <tr>
      <td style="text-align:left">Frequency</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Frequency">Frequency</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Frequency or interval for departures.</p>
        <p><em>Used <b>only</b> for frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">JourneyDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration of the journey</td>
    </tr>
    <tr>
      <td style="text-align:left">dayTypes</td>
      <td style="text-align:left">DayTypeRef</td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">References to <a href>DayTypes</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">JourneyPatternRef</td>
      <td style="text-align:left">JourneyPatternRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">References to <a href="handbok-n801-siri-netex-network.md#network-JourneyPattern">JourneyPattern</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">JourneyFrequencyGroupRef</td>
      <td style="text-align:left">JourneyFrequencyGroupRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">References to <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#JourneyFrequencyGroup">JourneyFrequencyGroup</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">VehicleTypeRef</td>
      <td style="text-align:left">VehicleTypeRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">References to <a href>VehicleType</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">OperatorRef</td>
      <td style="text-align:left">OperatorRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">References to <a href>Operator</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">passingTimes</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#TimetabledPassingTime">TimetabledPassingTime</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">Planned passing times</td>
    </tr>
    <tr>
      <td style="text-align:left">parts</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#JourneyPart">JourneyPart</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>List of parts of the journey (used in special cases, such as combined
          journeys)</p>
        <p><em>To make re-use of journey parts possible, these must be defined separately (as independent objects, referred to from here).</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">checkConstraints</td>
      <td style="text-align:left"><a href>CheckConstraint</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Information about security checks, barriers etc. which may cause delays.</td>
    </tr>
    <tr>
      <td style="text-align:left">TrainSize</td>
      <td style="text-align:left"><a href>TrainSize</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Information about the size and structure of a train</td>
    </tr>
    <tr>
      <td style="text-align:left">FlexibleServiceProperties</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-network.md#network-FlexibleServiceProperties">FlexibleServiceProperties</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Properties for flexible (on demand) transport.</p>
        <p><em>It is possible to define properties here if they deviate from the flexible service properties set at the </em>
          <a
          href="handbok-n801-siri-netex-network.md#network-Line"><em>Line</em>
            </a><em>-level.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

**FlexibleServiceProperties**

Description of properties for flexible transport \(used from [ServiceJourney](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServiceJourney)\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleServiceProperties)

_Defined in TimetableFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Flexx-809.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FlexibleServiceProperties &lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">FlexibleServiceType</td>
      <td style="text-align:left">FlexibleServiceTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of flexible transport:</p>
        <ul>
          <li>dynamicPassingTimes</li>
          <li>fixedHeadwayFrequency</li>
          <li>fixedPassingTimes</li>
          <li>notFlexible</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">CancellationPossible</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether a service may be cancelled by the operator</td>
    </tr>
    <tr>
      <td style="text-align:left">ChangeOfTimePossible</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether times may be changed by the operator</td>
    </tr>
    <tr>
      <td style="text-align:left">BookingContact</td>
      <td style="text-align:left"><a href>ContactStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Contact information to book the on-demand service.</td>
    </tr>
    <tr>
      <td style="text-align:left">BookingMethods</td>
      <td style="text-align:left">BookingMethodListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible methods for booking the on-demand service.</p>
        <ul>
          <li>callDriver</li>
          <li>callOffice</li>
          <li>online</li>
          <li>other</li>
          <li>phoneAtStop</li>
          <li>text</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookingAccess</td>
      <td style="text-align:left">BookingAccessEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Access categories for who may place the order for the on-demand service.</p>
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
        <p>A time when the booking must be completed:</p>
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
        <p>A time when payment must be completed:</p>
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
      <td style="text-align:left">Latest possible time for booking</td>
    </tr>
    <tr>
      <td style="text-align:left">MinimumBookingPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The minimum time ahead of journey departure the booking must be completed</td>
    </tr>
    <tr>
      <td style="text-align:left">BookingNote</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Additional information about booking</td>
    </tr>
  </tbody>
</table>

#### DeadRun <a id="timetable-DeadRun"></a>

[VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney) without passengers.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-DeadRun)

_Defined in TimetableFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">DeadRun &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney">VehicleJourney</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Journey.1">Journey</a>&lt; <a href>LinkSequence</a> &lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">Frequency</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Frequency">Frequency</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Frequency/interval for departures</p>
        <p><em>Used <b>only</b> for frequency-based departures.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">dayTypes</td>
      <td style="text-align:left">DayTypeRef</td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">References to <a href>DayTypes</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">JourneyPatternRef</td>
      <td style="text-align:left">JourneyPatternRef</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>References to <a href="handbok-n801-siri-netex-network.md#network-JourneyPattern">JourneyPattern</a>
        </p>
        <p><em>Note, that for JourneyPatterns used exclusively by DeadRuns, it is permitted to define </em>
          <a
          href="handbok-n801-siri-netex-network.md#network-ScheduledStopPoint"><em>ScheduledStopPoints</em>
            </a> <em>which are not linked to a </em><a href="handbok-n801-siri-netex-stops.md#stops-Place"><em>Place</em></a>  <em>(i.e.</em> 
            <a
            href="handbok-n801-siri-netex-network.md#network-StopAssignment"><em>StopAssignment</em>
              </a><em> is not defined), when these ScheduledStopPoints do not exist in the stop place registry (e.g. vehicle garages, workshops, rest areas)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">JourneyFrequencyGroupRef</td>
      <td style="text-align:left">JourneyFrequencyGroupRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#JourneyFrequencyGroup">JourneyFrequencyGroup</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">VehicleTypeRef</td>
      <td style="text-align:left">VehicleTypeRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to <a href>VehicleType</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">passingTimes</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#TimetabledPassingTime">TimetabledPassingTime</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Planned passing times</td>
    </tr>
    <tr>
      <td style="text-align:left">OperatorRef</td>
      <td style="text-align:left">OperatorRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to <a href>Operator</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">DeadRunType</td>
      <td style="text-align:left">DeadRunTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of DeadRun <em>(if relevant)</em>:</p>
        <ul>
          <li>garageRunOut</li>
          <li>garageRunIn</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Periodical journeys <a id="timetable-Periodicaljourneys"></a>

**TemplateVehicleJourney**

Template to describe recurring [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourney), used together with [HeadwayJourneyGroup ](handbok-n801-siri-netex-timetable.md#timetable-HeadwayJourneyGroup)\(to describe frequency-based departures\) or with [RhythmicalJourneyGroup](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#RhythmicalJourneyGroup) \(to describe departures at the same time of day in a set period\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TemplateVehicleJourney)

_Defined in TimetableFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">TemplateServiceJourney &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#TemplateVehicleJourney">TemplateVehicleJourney</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourney">ServiceJourney</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Journey.1">Journey</a> &lt;
          <a
          href>LinkSequence</a>&lt; <a href>DataManagedObject</a> 
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
      <td style="text-align:left">frequencyGroups</td>
      <td style="text-align:left">
        <p>(choice) <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#RhythmicalJourneyGroup">RhytmicalJourneyGroup</a>
        </p>
        <p>(choice) <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#HeadwayJourneyGroup">HeadwayJourneyGroup</a>
        </p>
        <p>(choice) RhytmicalJourneyGroupRef</p>
        <p>(choice) HeadwayJourneyGroupRef</p>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#RhythmicalJourneyGroup">RhythmicalJourneyGroup</a> or
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#HeadwayJourneyGroup">HeadwayJourneyGroup</a>, or reference to a template which applies to this
          pattern.</td>
    </tr>
  </tbody>
</table>

**TemplateServiceJourney**

Template to describe recurring [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourney), used either with [HeadwayJourneyGroup ](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#HeadwayJourneyGroup)\(to describe frequency-based departures\) or with [RhytmicalJourneyGroup](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#RhythmicalJourneyGroup) \(to describe departures at the same time of day in a set period\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TemplateServiceJourney)

_Defined in TimetableFrame_

Examples in the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

| TemplateServiceJourney &lt; [TemplateVehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#TemplateVehicleJourney) &lt; [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourney) &lt; [Journey](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Journey.1)  &lt; [LinkSequence]() &lt; [DataManagedObject]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| TemplateServiceJourney inherits from [TemplateVehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#TemplateVehicleJourney) and does not introduce new elements or attributes. |  |  |  |

**JourneyFrequencyGroup**

Abstract type which describes recurring \(for example: "departures at xx05, xx15, xx25, xx35, xx45, xx55"\) or frequency based departures \("departures with X minutes spacing"\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyFrequencyGroup)

<table>
  <thead>
    <tr>
      <th style="text-align:left">JourneyFrequencyGroup &lt; <a href>GroupOfEntities</a> &lt; <a href>DataManagedObject</a> 
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
      <td style="text-align:left">FirstDepartureTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Departure time for the first stop in the first departure in the frequency
        group.</td>
    </tr>
    <tr>
      <td style="text-align:left">LastDepartureTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Departure time for the first stop in the last departure in the frequency
        group.</td>
    </tr>
    <tr>
      <td style="text-align:left">DayOffset</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Number of days from the starting point <em>(when service period spans more than one calendar day)</em>
        </p>
        <p><em>Offset is relative to the</em>  <a href><em>OperatingDay</em></a>  <em>/</em> 
          <a
          href><em>Date</em>
            </a> <em>for the affected </em><a href="handbok-n801-siri-netex-timetable.md#timetable-VehicleJourney"><em>VehicleJourney(s)</em></a><em>, e.g. &quot;-1&quot; (previous day) or &quot;1&quot; (next day)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">journeys</td>
      <td style="text-align:left">VehicleJourneyRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>List of journeys in a JourneyFrequencyGroup.</p>
        <p><em>Lists <b>only</b> ServiceJourneyRef objects.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

**RhythmicalJourneyGroup**

Description of service where departure\(s\) start at the same time \(minutes over a whole hour\) in a set period.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-RhythmicalJourneyGroup)

_Defined in TimetableFrame_

Examples in the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">RhythmicalJourneyGroup &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#RhythmicalJourneyGroup">JourneyFrequencyGroup</a> &lt;
        <a
        href>GroupOfEntities</a>&lt; <a href>DataManagedObject</a> 
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
      <td style="text-align:left">timebands</td>
      <td style="text-align:left"><a href>TimebandRef</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">
        <p>Reference to a <a href>Timeband</a>-object which describes the departure
          time for <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourney">ServiceJourney</a> as
          minutes over a full hour.</p>
        <p><em>In the context of RhythmicalJourneyGroup, </em><a href><em>Timeband</em></a>  <em>must have identical StartTime and EndTime and show the departure time as minutes over a full hour. Use &quot;00:...&quot; for generic time representation.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

**HeadwayJourneyGroup**

Description of service which has the same time interval between departures _\(frequency-based departures\)._

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-HeadwayJourneyGroup)

_Defined in TimetableFrame_

| HeadwayJourneyGroup &lt; [JourneyFrequencyGroup](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#JourneyFrequencyGroup) &lt; [GroupOfEntities]()   &lt; [DataManagedObject]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| ScheduledHeadwayInterval | xsd:duration | 1: 1 | The planned interval between departures |
| MinimumHeadwayInterval | xsd:duration | 0: 1 | The minimum interval between departures |
| MaximumHeadwayInterval | xsd:duration | 0: 1 | The maximum interval between departures |
| Description | [MultilingualString]() | 0: 1 | Description \(for example: "every 15 minutes"\) |

#### Coupled journeys <a id="timetable-Coupledjourneys"></a>

**CoupledJourney**

A combined/coupled journey comprised of different [VehicleJourneys](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney), where the operating vehicle is a combination of two or more single vehicles _\(normally used for linking trains\)_.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-CoupledJourney)

_Defined in TimetableFrame_

| CoupledJourney &lt; [DataManagedObject]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Description | [MultilingualString]() | 0: 1 | Description |
| journeys | VehicleJourneyRef | 0: \* | List of [VehicleJourneys](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourney) in the coupled journey. |

**JourneyPartCouple**

Two or more [JourneyParts](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPart) from different [VehicleJourneys](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-VehicleJourney) which are operating together \(coupled\) \(_normally used for linking trains_\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-JourneyPartCouple)

_Defined in TimetableFrame_

| JourneyPartCouple &lt; [DataManagedObject]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Description | [MultilingualString]() | 0: 1 | Description of a coupled journey |
| StartTime | xsd:time | 1: 1 | Starting time for a coupled journey |
| EndTime | xsd:time | 1: 1 | The end time for a coupled journey |
| FromStopPointRef | ScheduledStopPointRef | 1: 1 | The planned first stop for a coupled journey \([ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint)\) |
| ToStopPointRef | ScheduledStopPointRef | 1: 1 | Planned last stop for the coupled journey \([ScheduledStopPoint](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint)\) |
| MainPartRef | JourneyPartRef | 1: 1 | The main part of a coupled journey \(relevant for travel information to the public\) |
| journeyParts | JourneyPartRef | 0: 1 | Remaining parts of a coupled journey \(excl. MainPartRef\) |

### ServiceCalendar <a id="timetable-ServiceCalendar"></a>

A logical container for a grouping of calendar-related elements with identical validity criteria, and/or identical start-end dates.

_Please note that unlinked calendar objects with validity criteria identical to the current_ [_ServiceCalendarFrame_]() _should be added directly below it, rather than unnecessarily grouping it in a ServiceCalendar._

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServiceCalendar)

_Defined in ServiceCalendarFrame_

Examples in the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/schedule/ServiceCalendar-example.xml).

<table>
  <thead>
    <tr>
      <th style="text-align:left">ServiceCalendar &lt; <a href>DataManagedObject</a> 
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
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Name of calendar</td>
    </tr>
    <tr>
      <td style="text-align:left">FromDate</td>
      <td style="text-align:left">xsd:date</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Calendar start date</td>
    </tr>
    <tr>
      <td style="text-align:left">ToDate</td>
      <td style="text-align:left">xsd:date</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Calendar end date</td>
    </tr>
    <tr>
      <td style="text-align:left">EarliestTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Start time for the day can be defined in cases where it differs from the
        normal 00:00:00.</td>
    </tr>
    <tr>
      <td style="text-align:left">DayLength</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Length of the day can be defined in cases where it differs from the normal
        24 hours.</td>
    </tr>
    <tr>
      <td style="text-align:left">dayTypes</td>
      <td style="text-align:left"><a href>DayType</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>DayTypes used in a calendar</p>
        <p><em>May be defined directly in</em>  <a href><em>ServiceCalendarFrame</em></a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">timebands</td>
      <td style="text-align:left"><a href>Timeband</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Timebands used in a calendar</p>
        <p><em>May be defined directly in </em><a href><em>ServiceCalendarFrame</em></a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">operatingDays</td>
      <td style="text-align:left"><a href>OperatingDay</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>OperatingDays used in a calendar</p>
        <p><em>May be defined directly in </em><a href><em>ServiceCalendarFrame</em></a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">operatingPeriods</td>
      <td style="text-align:left"><a href>OperatingPeriod</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>OperatingPeriods used in a calendar</p>
        <p><em>May be defined directly in </em><a href><em>ServiceCalendarFrame</em></a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">dayTypeAssignments</td>
      <td style="text-align:left"><a href>DayTypeAssignment</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Linking of <a href>DayTypes</a> to <a href>OperatingDays</a>
        </p>
        <p><em>May be defined directly in </em><a href><em>ServiceCalendarFrame</em></a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

### Interchange <a id="timetable-Interchange"></a>

#### Interchange across datasets <a id="timetable-Interchangeacrossdatasets"></a>

Please note that when creating **interchanges between different datasets** \(across codespaces\), the agency delivering the _receiving_ [Line](handbok-n801-siri-netex-network.md#network-Line) is responsible for creating, maintaining and delivering potential interchanges. This is because it normally is the connecting \(waiting\) transport which defines/controls the interchange rules for each case.

This means such interchanges are only ever defined on the receiving side, in the appropriate Line-file containing the [ServiceJourneyInterchange](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourneyInterchange) to which the interchange is linked \(where [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#ServiceJourney) for ToJourneyRef is defined\). To re-iterate, interchanges should not be defined by the arriving transport.

#### Interchange <a id="timetable-Interchange.1"></a>

An abstract type which describes planned possibilities for passengers to transfer between[ServiceJourneys](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServiceJourney) on the same or \(usually\) nearby stops, with a description of when/if a vehicle will wait for another arriving vehicle.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Interchange)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Interchange &lt; <a href>DataManagedObject</a> 
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
      <td style="text-align:left">Priority</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Weighted prioritization of transfers, e.g. when there are multiple possible
          interchange locations along a journey, or when there is a need to mark
          a location as inappropriate for interchanges:</p>
        <ul>
          <li>-1 (interchanges not allowed. Corresponds to: <em>noInterchange</em>)</li>
          <li>0 (<em>null</em>, standard interchange value. Corresponds to: <em>interchangeAllowed</em>)</li>
          <li>1 (recommended interchange location to be weighted higher in the journey
            planner. [<em>timed</em> according to stated MaximumWaitTime]. Corresponds
            to: <em>recommendedInterchange</em>)</li>
          <li>2 (preferred interchange to be weighted with maximum preference by the
            journey planner. Corresponds to: <em>preferredInterchange</em>)</li>
        </ul>
        <p><em>Corresponds to Weighting (InterchangeWeightingEnumeration) for </em>
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370400/stops#stops-StopPlace"><em>StopPlace</em>
            </a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">StaySeated</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specifies that the traveller can remain seated in the vehicle, as it will
          be re-used for the next part of the journey.</p>
        <p><em>Useful when describing Lines that operate in a circular pattern (prevents fictitious interchanges)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Guaranteed</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether the interchange is guaranteed <em>(the passenger is guaranteed the transfer between the two journeys)</em>.</td>
    </tr>
    <tr>
      <td style="text-align:left">MaximumWaitTime</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum time (after normal departure time) the connecting transport allows
        for delays.</td>
    </tr>
  </tbody>
</table>

#### ServiceJourneyInterchange <a id="timetable-ServiceJourneyInterchange"></a>

Specialization of [Interchange](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Interchange) for [ServiceJourney.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServieJourney)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ServiceJourneyInterchange)

_Defined in TimetableFrame_

Examples in the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine863-with-interchange.xml) 

| ServiceJourneyInterchange &lt; [Interchange](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#Interchange.1) &lt; [DataManagedObject]()  |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| FromPointRef | ScheduledStopPointRef | 1: 1 | Reference to stop place where passenger begins transfer/interchange \(arriving vehicle location\) |
| ToPointRef | ScheduledStopPointRef | 1: 1 | Reference to stop place where passenger continues the journey from \(departing vehicle location\) |
| FromJourneyRef | VehicleJourneyRef | 1: 1 | Reference to the journey the passenger transfers from \([VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney)\) |
| ToJourneyRef | VehicleJourneyRef | 1: 1 | Reference to the journey the passenger transfers to \([VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728760393/timetable#VehicleJourney)\) |

