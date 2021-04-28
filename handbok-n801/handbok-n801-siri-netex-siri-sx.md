# Håndbok N801 \(SIRI/NeTEX\) : SIRI-SX

**The Service Interface for Real Time Information - Situation Exchange**

Version

Current version for **SIRI-SX** is:   **v1.1**  \(_last changed_  05 Feb 2021\)

## Contents <a id="SIRI-SX-Contents"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591773293 {padding: 0px;}  
div.rbtoc1619591773293 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591773293 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Contents](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-Contents)
* [Data requirements](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-Datarequirements)
* [Components](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-Components)
  * [SituationExchangeDelivery](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-SituationExchangeDelivery)
    * [SituationExchangeDelivery](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-SituationExchangeDelivery.1)
    * [PtSituationElement](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-PtSituationElement)
    * [SituationSource](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-SituationSource)
    * [HalfOpenTimestampRangeStructure](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-HalfOpenTimestampRangeStructure)
    * [InfoLinks](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-InfoLinks)
    * [InfoLink](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-InfoLink)
    * [Affects](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-Affects)
    * [AffectedNetwork](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedNetwork)
    * [AffectedOperatorStructure](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedOperatorStructure)
    * [AffectedLineStructure](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedLineStructure)
    * [AffectedRoute](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedRoute)
    * [AffectedRouteStructure](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedRouteStructure)
    * [AffectedStopPoint](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedStopPoint)
    * [AffectedStopPlace](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedStopPlace)
    * [AccessibilityAssessment](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AccessibilityAssessment)
    * [AccessibilityLimitation](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AccessibilityLimitation)
    * [AffectedComponent](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedComponent)
    * [AffectedVehicleJourney](handbok-n801-siri-netex-siri-sx.md#SIRI-SX-AffectedVehicleJourney)

This document is part of the Norwegian SIRI Profile and describes datasets and elements used for exchanging **textual traffic situation messages** in the **SIRI Situation Exchange \(SX\)** real-time format.

SIRI-SX is used to model textual descriptions of disruptions, or deviations from the planned public transport information. The messages can be applied directly to stops, lines, vehicles etc. in the already existing public transport data by the use of ID references.

## Data requirements <a id="SIRI-SX-Datarequirements"></a>

Sending of a SIRI-SX _ServiceDelivery,_ data must be in accordance with this profile and the **entire dataset should be contained within a** _**single XML file**_.

Note that the profile does not present an exhaustive list of all real-time information technically possible to transfer via SIRI-SX, but it lays the foundation for which demands are placed on the datasets in order to meet the demands set by [Håndbok N801](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370406/H+ndbok+N801).

It is permitted for client systems to send more than one _Situations \(PtSituationElement\)_ per _SituationExchangeDelivery_, in order for real-time information to be conflated and be transferred as part of the same _ServiceDelivery_.

The [examples](handbok-n801-siri-netex-siri-examples-catalogue.md) associated with this profile are meant to show practical implementations of specific use cases, and may contain supplementary _optonal_ data fields, or lack _mandatory_ data fields, compared to a full and complete dataset. See [SIRI-SX\#Components](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-Components) for closer descriptions of the data types, specifications and requirements on the unique elements of the SIRI SX-data.

## Components <a id="SIRI-SX-Components"></a>

### SituationExchangeDelivery <a id="SIRI-SX-SituationExchangeDelivery"></a>

#### SituationExchangeDelivery <a id="SIRI-SX-SituationExchangeDelivery.1"></a>

A data type for the representation of one or more situations, or updates on previously published situations through _Situations \(PtSituationElement\)_ per _SituationExchangeDelivery_ with the status and scope of the affected services.

| SituationExchangeDelivery &lt; [ServiceDelivery](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-ServiceDelivery) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| attribute | version | xsd:NMTOKEN | 1: 1 | Version ID for SitutaionExhangeDelivery |
| element | ResponseTimestamp | xsd:dateTime | 1: 1 | Timestamp for when the dataset was created/published. |
| element | Situations | [SIRI-SX\#PtSituationElement](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-PtSituationElement) | 1: \* | Data object for a Public Transport Situation Exchange. |

#### PtSituationElement <a id="SIRI-SX-PtSituationElement"></a>

A container element for situation data.

<table>
  <thead>
    <tr>
      <th style="text-align:left">PtSituationElement</th>
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
      <td style="text-align:left">CreationTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Timestamp for when the situation was created.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ParticipantRef</td>
      <td style="text-align:left">ParticipantCode</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Codespace of the data source (see <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370434/List+of+current+Codespaces">codespace</a>).</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SituationNumber</td>
      <td style="text-align:left">xsd:anyURI</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p><b>Unique</b> situation-ID for <em>PtSituationElement.</em>
        </p>
        <p>Format:
          <br /><code>CODESPACE:SituationNumber:ID</code>
          <br /><em>e.g.:</em> ABC:SituationNumber:123</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Source</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-SituationSource">SIRI-SX#SituationSource</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Information on the source of the message.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Progress</td>
      <td style="text-align:left">WorkflowStatusEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Status of a situation message.</p>
        <p>Possible values:</p>
        <ul>
          <li>open</li>
          <li>closed (<em>the situation is over and traffic has returned to normal</em>)</li>
        </ul>
        <p><em>Please note that when Progress is set to &apos;closed&apos; the message is considered expired and should not be presented to the public.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VersionedAtTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Timestamp when the situation element was updated.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ValidityPeriod</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-HalfOpenTimestampRangeStructure">SIRI-SX#HalfOpenTimestampRangeStructure</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">
        <p>Validity period(s) set with a start time and optionally with an end time.
          When the end time of the situation is undefined the expiration of the situation
          is considered unknown until cancellation status for the situation is sent.
          If the situation has several periods, all but the last period must have
          an end date.</p>
        <p>Note that for closed (<em>Progress=closed</em>) messages, the ValidityPeriod <b>must</b> have
          an EndTime with a minimum of <b>five hours</b> into the future to ensure
          the message is properly delivered and received by all systems.</p>
        <p>Once EndTime has expired, the message will no longer be re-distributed
          in real-time data streams or services.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left"><em>UndefinedReason</em>
      </td>
      <td style="text-align:left">Reason</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p><em>Reason</em> should always be <em><b>&lt;UndefinedReason/&gt;</b></em>.</p>
        <p>The field is mandatory due to format spesification, but is not used.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Severity</td>
      <td style="text-align:left">SeverityEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>How severely the situation affects public transport services.</p>
        <p>Possible values:</p>
        <ul>
          <li>noImpact</li>
          <li>verySlight</li>
          <li>slight</li>
          <li>normal (<em>default</em>)</li>
          <li>severe</li>
          <li>verySevere</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Priority</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Number value from 1 to 10 indicating the priority (urgency) of the situation
          message.</p>
        <p><b>1</b> - First (i.e. highest) message priority. <em>Equivalent to DATEX2 urgency level &quot;extremelyUrgent&quot;</em>
          <br
          /><b>2 - 10</b> - Urgent, of various priority. <em>Equivalent to DATEX2 urgency level &quot;urgent&quot; with added priority order.</em>
        </p>
        <p>Left blank (<em>default</em>) is equivalent to DATEX2 urgency level &quot;normal
          urgency&quot;.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ReportType</td>
      <td style="text-align:left">ReportTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Type of situation report. The field is required in order to differentiate
          general information from incidents.</p>
        <p>Possible values:</p>
        <ul>
          <li>general (used for public information not impacting the actual operation
            of the PT-service. eg. &quot;No food service on this journey&quot;)</li>
          <li>incident (used for public information impacting the operation of the PT-service.
            eg. &quot;expect delays due to road construction work&quot;)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Planned</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the situation in question is due to planned events, or an unexpected
        incident.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Summary</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">
        <p>1: *</p>
        <p><em>(Can be 0 when Progress = &quot;closed&quot;)</em> 
        </p>
      </td>
      <td style="text-align:left">
        <p>The textual summary of the situation (which is not already described by
          structured data). One summary per language (if more than one, the <em>xml:lang</em> attribute <b>must</b> be
          set).</p>
        <p><b>Maximum 160 characters</b> (to keep the message readable).</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Description</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Expanded textual description (if more than one, the <em>xml:lang</em> attribute <b>must</b> be
          set) of the situation (do not repeat information from Summary, or structured
          data).</p>
        <p>Please do not add advice on how to avoid the situation, as this should
          be presented in the Advice field.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Advice</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Textual advice (if more than one, the <em>xml:lang</em> attribute <b>must</b> be
        set) on how a passenger should react/respond to the situation.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">InfoLinks</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-InfoLinks">SIRI-SX#InfoLinks</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Link to a website which has further information on the situation.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Affects</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-Affects">SIRI-SX#Affects</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>A description of what the situation affects.</p>
        <p>Only allowed to be blank (have no content) when message progress is set
          to <em>&quot;closed&quot;</em>.</p>
      </td>
    </tr>
  </tbody>
</table>

#### SituationSource <a id="SIRI-SX-SituationSource"></a>

Information on the source of the message.

<table>
  <thead>
    <tr>
      <th style="text-align:left">SituationSource</th>
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
      <td style="text-align:left">SourceType</td>
      <td style="text-align:left">SourceType</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Information type</p>
        <p>Possible values:</p>
        <ul>
          <li>directReport</li>
        </ul>
        <p><em>Required by the format spesification, but not used.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### HalfOpenTimestampRangeStructure <a id="SIRI-SX-HalfOpenTimestampRangeStructure"></a>

Period can be open- or closed-ended.

| HalfOpenTimestampRangeStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | StartTime | xsd:dateTime | 1: 1 | Start time for the period. |
| element | EndTime | xsd:dateTime | 0: 1 | End time for the period. |

#### InfoLinks <a id="SIRI-SX-InfoLinks"></a>

Collection of information links

| InfoLinks |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | InfoLink | [SIRI-SX\#InfoLink](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-InfoLink) | 1: 1 | Link to a website which has further information on the situation. |

#### InfoLink <a id="SIRI-SX-InfoLink"></a>

Link to a website which has further information on the situation.

| InfoLink |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | Uri | xsd:anyUri | 1: 1 | Link to a website which has further information on the situation. |
| element | Label | [NaturalLanguageStringStructure](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure) | 0: 1 | Label for the link. |

#### Affects <a id="SIRI-SX-Affects"></a>

Data objects for a closer description of required element affected by the situation.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Affects</th>
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
      <td style="text-align:left">(choice) element
        <br />
        <br />
        <br />
      </td>
      <td style="text-align:left">Networks</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedNetwork">SIRI-SX#AffectedNetwork</a>
      </td>
      <td style="text-align:left">
        <p>1: *</p>
        <p><em>(Can be 0 when Progress = &quot;closed&quot;)</em> 
        </p>
      </td>
      <td style="text-align:left">Network with operators and lines affected by the situation.</td>
    </tr>
    <tr>
      <td style="text-align:left">StopPlaces</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedStopPlace">SIRI-SX#AffectedStopPlace</a>
      </td>
      <td style="text-align:left">Stops affected by the situation.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">StopPoints</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedStopPoint">SIRI-SX#AffectedStopPoint</a>
      </td>
      <td style="text-align:left">Stops affected by the situation, with the possibility of specifying criteria
        of situation relevance.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">VehicleJourneys</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedVehicleJourney">SIRI-SX#AffectedVehicleJourney</a>
      </td>
      <td style="text-align:left">Trips affected by the situation.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### AffectedNetwork <a id="SIRI-SX-AffectedNetwork"></a>

References to an affected Network element\(s\).

_Please note that VehicleMode and Submode are the same as in_ [_Norwegian NeTEx profile, TransportModes_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-TransportModes)

<table>
  <thead>
    <tr>
      <th style="text-align:left">AffectedNetwork</th>
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
      <td style="text-align:left">AffectedOperator</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedOperatorStructure">SIRI-SX#AffectedOperatorStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to the affected operator.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">NetworkRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to affected Network.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">VehicleMode</td>
      <td style="text-align:left">VehicleModesOfTransportEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Affected modality.</p>
        <p>Possible values:</p>
        <ul>
          <li>all</li>
          <li>air</li>
          <li>bus</li>
          <li>coach</li>
          <li>funicular (please note: does not have a corresponding <em>submode</em>)</li>
          <li>metro</li>
          <li>rail</li>
          <li>taxi (please note: does not have a corresponding <em>submode</em>)</li>
          <li>telecabin (<em>mapped to til cableway</em>) (please note: does not have
            a corresponding <em>submode</em>)</li>
          <li>tram</li>
          <li>water</li>
          <li>selfDrive</li>
        </ul>
        <p><em>Modes must be specified together with corresponding submode (when applicable), whenever the situation does not affect all modalities in the affected planned data.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element
        <br />
        <br />
        <br />
        <br />
        <br />
        <br />
      </td>
      <td style="text-align:left">AirSubmode</td>
      <td style="text-align:left">AirSubmodesOfTransportEnumeration</td>
      <td style="text-align:left">0: 1
        <br />
        <br />
        <br />
        <br />
        <br />
        <br />
      </td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>domesticFlight</li>
          <li>helicopterService</li>
          <li>internationalFlight</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BusSubmode</td>
      <td style="text-align:left">BusSubmodesOfTransportEnumeration</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>airportLinkBus</li>
          <li>expressBus</li>
          <li>localBusService (mapped to <em>localBus</em>)</li>
          <li>nightBus</li>
          <li>railReplacementBus</li>
          <li>regionalBus</li>
          <li>schoolBus</li>
          <li>shuttleBus</li>
          <li>sightseeingBus</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Coach</td>
      <td style="text-align:left">CoachSubmodesOfTransportEnumeration</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>internationalCoachService (mapped to <em>internationalCoach</em>)</li>
          <li>nationalCoachService (mapped to <em>nationalCoach</em>)</li>
          <li>touristCoachService (mapped to <em>touristCoach</em>)</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">MetroSubmode</td>
      <td style="text-align:left">MetroSubmodesOfTransportEnumeration</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>metro</li>
          <li>urbanRailway</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">RailSubmode</td>
      <td style="text-align:left">RailSubmodesOfTransportEnumeration</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>interbational [<em>sic</em>]. <em>Please note, <b>the typo</b> is incorrectly implemented in the official standard. Mapped to &apos;international&apos;.</em>
          </li>
          <li>interRegionalRailService (mapped to <em>interregionalRail</em>)</li>
          <li>local</li>
          <li>longDistanceTrain (mapped to <em>longDistance</em>)</li>
          <li>sleeperRailService (mapped to <em>nightRail</em>)</li>
          <li>regionalRail</li>
          <li>specialTrainService (mapped to <em>airportLinkRail</em>)</li>
          <li>touristRailway</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">TramSubmode</td>
      <td style="text-align:left">TramSubmodesOfTransportEnumeration</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>localTramService (mapped to <em>localTram</em>)</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">WaterSubmode</td>
      <td style="text-align:left">WaterSubmodesOfTransportEnumeration</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>highSpeedPassengerService</li>
          <li>highSpeedVehicleService</li>
          <li>internationalCarFerryService (mapped to <em>internationalCarFerry</em>)</li>
          <li>internationalPassengerFerry</li>
          <li>localCarFerryService (mapped to <em>localCarFerry</em>)</li>
          <li>localPassengerFerry</li>
          <li>nationalCarFerryService (mapped to <em>nationalCarFerry</em>)</li>
          <li>sightseeingService</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">AffectedLine</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedLineStructure">SIRI-SX#AffectedLineStructure</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">
        <p>Reference(s) to affected line(s).</p>
        <p>Must be stated explicitly <em>AffectedLine</em> or <em>AllLines</em> due to
          technical demands on the element in the SIRI standard.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">AllLines</td>
      <td style="text-align:left">xsd:string (<em>empty</em>)</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### AffectedOperatorStructure <a id="SIRI-SX-AffectedOperatorStructure"></a>

Reference to an affected _Operator_.

| AffectedOperatorStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | OperatorRef | xsd:NMTOKEN | 1: 1 | Reference to an affected operator. |

#### AffectedLineStructure <a id="SIRI-SX-AffectedLineStructure"></a>

Information about an affected _Line_.

| AffectedLineStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | LineRef | xsd:NMTOKEN | 1: 1 | Reference to _Line_ in question \(_ID to the corresponding object in the timetable data_\). |
| element | Routes | [SIRI-SX\#AffectedRoute](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedRoute) | 1: \* | Reference to _Route\(s\)_ in question \(_ID to the corresponding object in the timetable data_\), when the situation does not apply to the entire Line. |

#### AffectedRoute <a id="SIRI-SX-AffectedRoute"></a>

Wrapper object to describe information about a Route affected by the situation.

| AffectedRouteStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | AffectedRoute | [SIRI-SX\#AffectedRouteStructure](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedRouteStructure) | 1: 1 | Reference to _Route_ in question \(_ID to the corresponding object in the timetable data_\). |

#### AffectedRouteStructure <a id="SIRI-SX-AffectedRouteStructure"></a>

Information about an affected Route

| AffectedRouteStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | RouteRef | xsd:NMTOKEN | 0: 1 | Reference to _Route_ in question \(_ID to the corresponding object in the timetable data_\). |
| element | StopPoints | [SIRI-SX\#AffectedStopPoint](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedStopPoint) | 0: \* | Reference to affected stop\(s\) in the affected Line. |

#### AffectedStopPoint <a id="SIRI-SX-AffectedStopPoint"></a>

Reference\(s\) to affected stop\(s\).

<table>
  <thead>
    <tr>
      <th style="text-align:left">AffectedStopPoint</th>
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
      <td style="text-align:left">
        <p>Reference to the Quay in question (ID corresponding to objects in the
          national stop place registry).</p>
        <p><em>If the quay is currently unknown, or the message applies to <b>all</b> quays, a reference to StopPlace may be used instead.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StopPointName</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure">NaturalLanguageStringStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Name of StopPlace (<em>Not used, but may be set to increase human readability.)</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StopCondition</td>
      <td style="text-align:left">RoutePointTypeEnumeration</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Specifies which passengers the message applies to, for example, people
          who are disembarking at an affected stop.</p>
        <p>Possible values:</p>
        <ul>
          <li>exceptionalStop (<em>for passengers expecting an interchange</em>)</li>
          <li>destination (<em>for passengers expecting to disembark, of at the last stop)</em>
          </li>
          <li>notStopping (<em>when passing a stop)</em>
          </li>
          <li>requestStop (<em>when a passenger must request the serving of a stop</em>)</li>
          <li>startPoint (<em>at departure or when passengers expect to board</em>)</li>
          <li>stop (default - <em>affects all interactions with the stop (boarding, alighting, arrival, departure, interchanges)</em>
          </li>
        </ul>
        <p>If this field is left blank or omitted the message will be interpreted
          as affecting boarding and alighting.</p>
      </td>
    </tr>
  </tbody>
</table>

#### AffectedStopPlace <a id="SIRI-SX-AffectedStopPlace"></a>

References to affected stops.

| AffectedStopPlace |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | AccessibilityAssessment | [SIRI-SX\#AccessibilityAssessment](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AccessibilityAssessment) | 0: 1 | Specifies whether the object is still available for users with special needs. |
| element | StopPlaceRef | xsd:NMTOKEN | 1: 1 | Reference to StopPlace or specific Quay \(ID corresponding to objects in the national stop place registry\). |
| element | PlaceName | [NaturalLanguageStringStructure](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-NaturalLanguageStringStructure) | 0: 1 | Name of the stop \(not used due to the reference to the national stop place registry, but _can_ be included to make the XML easier to read\). |
| element | AffectedComponents | [SIRI-SX\#AffectedComponent](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedComponent) | 0: \* | Reference\(s\) to which part\(s\) of the stop\(s\) are being affected. |

#### AccessibilityAssessment <a id="SIRI-SX-AccessibilityAssessment"></a>

Description of \(changed\) availability as a result of the situation.

| AccessibilityAssessment |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | acsb:MobilityImpairedAccess | xsd:boolean | 1: 1 | Specifies whether the object is still available for users with special needs. |
| element | acsb:Limitations | acsb:AccessibilityLimitation | 1: 1 | Specifies limitations for users with special needs. |

#### AccessibilityLimitation <a id="SIRI-SX-AccessibilityLimitation"></a>

Descriptions of limitations for users with special needs.

_Must be in accordance with **AccessibilityLimitation** for the stop, defined in accordance with the Norwegian NeTEx profile for_ [_**stops**_](handbok-n801-siri-netex-stops.md)_._

<table>
  <thead>
    <tr>
      <th style="text-align:left">AccessibilityLimitation</th>
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
      <td style="text-align:left">WheelchairAccess</td>
      <td style="text-align:left">AccessibilityEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>true</li>
          <li>false</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StepFreeAccess</td>
      <td style="text-align:left">AccessibilityEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>true</li>
          <li>false</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">EscalatorFreeAccess</td>
      <td style="text-align:left">AccessibilityEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>true</li>
          <li>false</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">LiftFreeAccess</td>
      <td style="text-align:left">AccessibilityEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>true</li>
          <li>false</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### AffectedComponent <a id="SIRI-SX-AffectedComponent"></a>

Complementary information regarding parts of a stop being affected by the situation \(for example which quay\).

<table>
  <thead>
    <tr>
      <th style="text-align:left">AffectedComponent</th>
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
      <td style="text-align:left">ComponentRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to the Quay in question (ID corresponding to objects in the
          national stop place registry).</p>
        <p><em>Used if ComponentType is &quot;quay&quot;</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ComponentType</td>
      <td style="text-align:left">ifopt:StopPlaceComponentTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>accessSpace</li>
          <li>boardingPosition (<em>only for trains</em>)</li>
          <li>entrance</li>
          <li>quay</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">AccessFeatureType</td>
      <td style="text-align:left">ifopt:AccessibilityFeatureEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>escalator</li>
          <li>lift</li>
          <li>narrowEntrance</li>
          <li>ramp</li>
          <li>stairs</li>
        </ul>
        <p><em>Used when it necessary to specify limitations for users with special mobility needs.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### AffectedVehicleJourney <a id="SIRI-SX-AffectedVehicleJourney"></a>

Reference\(s\) to affected VehicleJourney\(s\) with Route.

<table>
  <thead>
    <tr>
      <th style="text-align:left">AffectedVehicleJourney</th>
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
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">VehicleJourneyRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to affected VehicleJourney (<em>ID to the corresponding object in the timetable data</em>).</td>
    </tr>
    <tr>
      <td style="text-align:left">DatedVehicleJourneyRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">Reference to affected DatedVehicleJourney (<em>ID to the corresponding object in the timetable data</em>).</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">FramedVehicleJourneyRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370373/Generell+informasjon+SIRI#GenerellinformasjonSIRI-FramedVehicleJourneyRefStructure">FramedVehicleJourneyRefStructure</a>
      </td>
      <td style="text-align:left">Reference <b>with date</b> to affected VehicleJourney (<em>ID to the corresponding object in the timetable data</em>).</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Operator</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedOperatorStructure">SIRI-SX#AffectedOperatorStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to affected Operator (<em>ID to the corresponding object in the timetable data</em>).</p>
        <p><em>Not used, but may be set to increase human readability.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">LineRef</td>
      <td style="text-align:left">xsd:NMTOKEN</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Reference to affected Line (<em>ID to the corresponding object in the timetable data</em>).</p>
        <p><em>Not used, but may be set to increase human readability.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Route</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370605#SIRI-SX-AffectedRouteStructure">SIRI-SX#AffectedRouteStructure</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">
        <p>Reference to affected Route(s) (<em>ID to the corresponding object in the timetable data</em>).</p>
        <p><em>Mandatory field (due to format implementation), but can be blank if the situation affects <b>all</b> stops in AffectedVehicleJourney.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">OriginAimedDepartureTime</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Originally planned departure time (per time table) from the first stop
        of the departure.</td>
    </tr>
  </tbody>
</table>

