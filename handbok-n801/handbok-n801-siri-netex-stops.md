# Håndbok N801 \(SIRI/NeTEX\) : stops

## Version <a id="stops-Version"></a>

Current version for **stops** is:   **v1.4**   \(last changed 14 Apr 2021\) 

## Content <a id="stops-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591689790 {padding: 0px;}  
div.rbtoc1619591689790 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591689790 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Version](handbok-n801-siri-netex-stops.md#stops-Version)
* [Components](handbok-n801-siri-netex-stops.md#stops-Components)
  * [Place](handbok-n801-siri-netex-stops.md#stops-Place)
    * [TopographicPlace](handbok-n801-siri-netex-stops.md#stops-TopographicPlace)
    * [AddressablePlace](handbok-n801-siri-netex-stops.md#stops-AddressablePlace)
    * [SiteElement](handbok-n801-siri-netex-stops.md#stops-SiteElement)
    * [Site](handbok-n801-siri-netex-stops.md#stops-Site)
      * [Level](handbok-n801-siri-netex-stops.md#stops-Level)
      * [Entrance](handbok-n801-siri-netex-stops.md#stops-Entrance)
  * [Group of Stop Places](handbok-n801-siri-netex-stops.md#stops-GroupofStopPlaces)
    * [GroupOfStopPlaces](handbok-n801-siri-netex-stops.md#stops-GroupOfStopPlaces)
  * [StopPlace](handbok-n801-siri-netex-stops.md#stops-StopPlace)
    * [StopPlace](handbok-n801-siri-netex-stops.md#stops-StopPlace.1)
    * [StopPlaceSpace](handbok-n801-siri-netex-stops.md#stops-StopPlaceSpace)
    * [Quay](handbok-n801-siri-netex-stops.md#stops-Quay)
    * [BoardingPosition](handbok-n801-siri-netex-stops.md#stops-BoardingPosition)
    * [Inner Objects](handbok-n801-siri-netex-stops.md#stops-InnerObjects)
      * [AccessSpace](handbok-n801-siri-netex-stops.md#stops-AccessSpace)
      * [PathLink](handbok-n801-siri-netex-stops.md#stops-PathLink)
      * [PathJunction](handbok-n801-siri-netex-stops.md#stops-PathJunction)
      * [EquipmentPlace](handbok-n801-siri-netex-stops.md#stops-EquipmentPlace)
      * [SiteFacilitySet](handbok-n801-siri-netex-stops.md#stops-SiteFacilitySet)
  * [Flexible Stop Place](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace)
    * [FlexibleStopPlace](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace.1)
    * [FlexibleQuay](handbok-n801-siri-netex-stops.md#stops-FlexibleQuay)
    * [FlexibleArea](handbok-n801-siri-netex-stops.md#stops-FlexibleArea)
    * [HailAndRideArea](handbok-n801-siri-netex-stops.md#stops-HailAndRideArea)
  * [Point of Interest](handbok-n801-siri-netex-stops.md#stops-PointofInterest)
    * [PointOfInterest](handbok-n801-siri-netex-stops.md#stops-PointOfInterest)
  * [Parking](handbok-n801-siri-netex-stops.md#stops-Parking)
    * [Parking](handbok-n801-siri-netex-stops.md#stops-Parking.1)
    * [ParkingArea](handbok-n801-siri-netex-stops.md#stops-ParkingArea)
    * [ParkingProperties](handbok-n801-siri-netex-stops.md#stops-ParkingProperties)
    * [ParkingCapacity](handbok-n801-siri-netex-stops.md#stops-ParkingCapacity)
  * [Navigation](handbok-n801-siri-netex-stops.md#stops-Navigation)
    * [NavigationPath](handbok-n801-siri-netex-stops.md#stops-NavigationPath)
      * [PathLinkEndStructure](handbok-n801-siri-netex-stops.md#stops-PathLinkEndStructure)
  * [Zonal](handbok-n801-siri-netex-stops.md#stops-Zonal)
    * [TariffZone](handbok-n801-siri-netex-stops.md#stops-TariffZone)
    * [FareZone](handbok-n801-siri-netex-stops.md#stops-FareZone)
    * [GroupOfTariffZones](handbok-n801-siri-netex-stops.md#stops-GroupOfTariffZones)

This document is part of the Norwegian NeTEx Profile and describes data elements for the exchange of **place-, and stop place related information** via the NeTEx format.

## Components <a id="stops-Components"></a>

### Place <a id="stops-Place"></a>

#### TopographicPlace <a id="stops-TopographicPlace"></a>

An abstract data type for geospatial settlement or inhabited areas, such as city, rural area or suburb.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-TopographicPlace)

_Defined in SiteFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">TopographicPlace &lt; <a href>Place</a> &lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt;
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
      <td style="text-align:left">IsoCode</td>
      <td style="text-align:left">SubdivisionIdType</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p><em>ISO 3166-2</em> code to identify region county/territory</p>
        <p>For example <b>[LK]-[OK]</b>
          <br />LK = two letter country code [LK] according to <code>ISO 3166-1 alfa-2</code>
        </p>
        <p>OK = two letter area code [OK] according to <code>ISO 3166-2:NO</code>
        </p>
        <p>Examples:</p>
        <ul>
          <li>NO-02 &#x2013; Akershus</li>
          <li>NO-09 &#x2013; Vest Agder</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">TopographicPlaceType</td>
      <td style="text-align:left">TopographicPlaceTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of areas:</p>
        <ul>
          <li>country (<em>nationstate)</em>
          </li>
          <li>county (<em>first level subdivision of country</em>)</li>
          <li>city (<em>city</em>)</li>
          <li>interregion (<em>region spanning several other regions</em>)</li>
          <li>municipality (<em>second level subdivision of country</em>)</li>
          <li>placeOfInterest (sometimes known as pointOfInterest, or POI)</li>
          <li>region (<em>area/region</em>)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">CountryRef</td>
      <td style="text-align:left">CountryPrincipalityCodeType</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Two letter country code [LK] according to <code>ISO 3166-1 alfa-2</code>
        </p>
        <p><em>Only mandatory for TopographicPlaceType &quot;county&quot;</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParentTopographicPlaceRef</td>
      <td style="text-align:left">TopographicPlaceRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to parent area for an area. For example: a municipality is typically
        a subdivision of a parent county-region.</td>
    </tr>
  </tbody>
</table>

#### AddressablePlace <a id="stops-AddressablePlace"></a>

A place which can have address information

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-AddressablePlace)

<table>
  <thead>
    <tr>
      <th style="text-align:left">AddressablePlace &lt; <a href>Place</a> &lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt;
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
      <td style="text-align:left">Url</td>
      <td style="text-align:left">xsd:anyURI</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">URL related to the place</td>
    </tr>
    <tr>
      <td style="text-align:left">PostalAddress</td>
      <td style="text-align:left"><a href>PostalAddress</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Postal address for the place</td>
    </tr>
    <tr>
      <td style="text-align:left">RoadAddress</td>
      <td style="text-align:left"><a href>RoadAddress</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Road/street address for the place</p>
        <p><em>Mandatory for objects which should be linked to road networks, e.g. </em>
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#Entrance"><em>Entrance</em>
            </a> <em>and </em><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#StopPlace.1"><em>StopPlace</em></a><em>/</em>
            <a
            href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#Quay"><em>Quay</em>
              </a>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### SiteElement <a id="stops-SiteElement"></a>

An abstract type which describes a superordinate place.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-SiteElement)

<table>
  <thead>
    <tr>
      <th style="text-align:left">SiteElement &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a> &lt;
        <a
        href>Place</a>&lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">AccessibilityAssessment</td>
      <td style="text-align:left"><a href>AccessibilityAssessment</a>
      </td>
      <td style="text-align:left">1: 1 for StopPlace</td>
      <td style="text-align:left">Universal Design - description, see <a href="handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-AccessibilityAssessment">Accessibility Assessment definition</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">alternativeNames</td>
      <td style="text-align:left"><a href>AlternativeName</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of alternative names for Site</td>
    </tr>
    <tr>
      <td style="text-align:left">PublicUse</td>
      <td style="text-align:left">PublicUseEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specify for whom the place is available:</p>
        <ul>
          <li>all</li>
          <li>publicOnly</li>
          <li>authorisedPublicOnly</li>
          <li>disabledPublicOnly</li>
          <li>staffOnly</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Covered</td>
      <td style="text-align:left">CoveredEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specify whether the place has a roof (is covered and protects people from
          e.g. rain or snow):</p>
        <ul>
          <li>covered (<em>just a roof</em>)</li>
          <li>indoors (<em>roof and walls</em>)</li>
          <li>outdoors (<em>no roof or walls</em>)</li>
          <li>mixed (<em>partially roofed/indoor</em>)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Gated</td>
      <td style="text-align:left">GatedEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specify whether the place/area is open or gated:</p>
        <ul>
          <li>openArea</li>
          <li>gatedArea</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Lighting</td>
      <td style="text-align:left">LightingEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specify the lighting situation of the place:</p>
        <ul>
          <li>wellLit</li>
          <li>poorLit</li>
          <li>unlit</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">facilities</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteFacilitySet">SiteFacilitySet</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of available facilities</td>
    </tr>
  </tbody>
</table>

#### Site <a id="stops-Site"></a>

An abstract type describing a place.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Site)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Site &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement">SiteElement</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a>&lt; <a href>Place</a> &lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt;
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
      <td style="text-align:left">TopographicPlaceRef</td>
      <td style="text-align:left">TopographicPlaceRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to parent area (<a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#TopographicPlace">TopographicPlace</a>).</td>
    </tr>
    <tr>
      <td style="text-align:left">Locale</td>
      <td style="text-align:left"><a href>Locale</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Information about Locale.</td>
    </tr>
    <tr>
      <td style="text-align:left">OrganisationRef</td>
      <td style="text-align:left">OrganisationRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to governing or operating <a href>organisation</a> for the place.</td>
    </tr>
    <tr>
      <td style="text-align:left">ParentSiteRef</td>
      <td style="text-align:left">ParentSiteRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to parent SITE which contains this SITE
        <br /><em>Value dependent on context.</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">levels</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#Level">Level</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of levels (floors) for SITE</td>
    </tr>
    <tr>
      <td style="text-align:left">entrances</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#Entrance">Entrance</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Description of entrance objects <em>(mandatory if Site is a building).</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">equipmentPlaces</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#%5BhardBreak%5DEquipmentPlace">EquipmentPlace</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of equipment.</p>
        <p><em>Used to set </em><a href><em>Location</em></a>  <em>for PlaceEquipment/LocalService if relevant.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">placeEquipments</td>
      <td style="text-align:left"><a href>Equipment</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Description of available <a href>installed equipment</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left">localServices</td>
      <td style="text-align:left"><a href>Equipment</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Description of available <a href>LocalServices</a>.</td>
    </tr>
  </tbody>
</table>

**Level**

Description of levels \(floors in a building\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Level)

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/StopPlace-with-equipment-and-parking_example.xml)

| Level &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Name | [MultilingualString]() | 1: 1 | Name of level, e.g. "1", "A", "first floor" |
| Description | [MultilingualString]() | 0: 1 | Description |
| PublicUse | xsd:boolean | 0: 1 | Specifies if the floor is accessible to the public, or if access permission is required |
| AccessibilityAssessment | [AccessibilityAssessment]() | 0: 1 | Description of Universal Design accessibility. |

**Entrance**

Description of entrances.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Entrance)

Examples in the the[ GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/StopPlace-with-equipment-and-parking_example.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">Entrance &lt; SiteComponent &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement">SiteElement</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a>&lt; <a href>Place</a> &lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt;
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
      <td style="text-align:left">LevelRef</td>
      <td style="text-align:left">LevelRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to a <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#Level">Level</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left">checkConstraints</td>
      <td style="text-align:left"><a href>CheckConstraint</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Description of security checkpoints, barriers or other potentially delaying
        factors.</td>
    </tr>
    <tr>
      <td style="text-align:left">equipmentPlaces</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#%5BhardBreak%5DEquipmentPlace">EquipmentPlace</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Description of available equipment.</td>
    </tr>
    <tr>
      <td style="text-align:left">placeEquipments</td>
      <td style="text-align:left">InstalledEquipment</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Description of permanently installed equipment. See <a href>Equipment Types</a> for
        more information regarding which objects may be used here.</td>
    </tr>
    <tr>
      <td style="text-align:left">EntranceType</td>
      <td style="text-align:left">EntranceEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of entrance:</p>
        <ul>
          <li>opening</li>
          <li>openDoor</li>
          <li>door</li>
          <li>swingDoor</li>
          <li>revolvingDoor</li>
          <li>automaticDoor</li>
          <li>ticketBarrier</li>
          <li>gate</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">isEntry</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether an object is an entrance.</td>
    </tr>
    <tr>
      <td style="text-align:left">isExit</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies if an object is an exit.</td>
    </tr>
    <tr>
      <td style="text-align:left">Width</td>
      <td style="text-align:left">xsd:decimal</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The width of an entrance (in meters).</td>
    </tr>
    <tr>
      <td style="text-align:left">Height</td>
      <td style="text-align:left">xsd:decimal</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Height (clearance) of an entrance (in meters).</td>
    </tr>
  </tbody>
</table>

### Group of Stop Places <a id="stops-GroupofStopPlaces"></a>

#### GroupOfStopPlaces <a id="stops-GroupOfStopPlaces"></a>

A grouping normally used to tie together stop places in close proximity to each other. This can be used to link several major stop places into a "hub". _Not to be confused with_ [_parentStopPlace \(multimodal StopPlace\)_](handbok-n801-siri-netex-stopplace-complex.md).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-GroupOfStopPlaces)

_Defined in SiteFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/StopPlace-with-equipment-and-parking_example.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">GroupOfStopPlaces &lt; <a href>GroupOfEntities</a> &lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">PurposeOfGroupingRef</td>
      <td style="text-align:left">
        <p>xsd:normalizedString</p>
        <p><em>predefined values, see Description</em>
        </p>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Categorization for the grouping, defined by referencing predefined PurposeOfGrouping:</p>
        <ul>
          <li>generalization (<em>grouping of prominent stop places with a superordinate Place, for example, a town, or city centre</em>)</li>
          <li>cluster (<em>stop places in proximity to each other which have a natural geospatial- or public transport-related relationship</em>)</li>
          <li>railStationAssociatedStops (<em>stop places associated with rail public transport, including its feeder/distributor and replacement services</em>)</li>
        </ul>
        <p>Example:
          <br /><code>&lt;PurposeOfGroupingRef ref=&quot;NSR:PurposeOfGrouping:generalization&quot;/&gt;</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">members</td>
      <td style="text-align:left">StopPlaceRef</td>
      <td style="text-align:left">2: *</td>
      <td style="text-align:left">List of references (<em>StopPlace ID from national stop place registry</em>)
        to stop places included in the group</td>
    </tr>
    <tr>
      <td style="text-align:left">alternativeNames</td>
      <td style="text-align:left"><a href>AlternativeName</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of alternative names for the grouping</td>
    </tr>
  </tbody>
</table>

### StopPlace <a id="stops-StopPlace"></a>

#### StopPlace <a id="stops-StopPlace.1"></a>

Description of stop place.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPlace)

_Defined in SiteFrame_

Examples in the GitHub-repository 

<table>
  <thead>
    <tr>
      <th style="text-align:left">StopPlace &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#%5BhardBreak%5DSite">Site</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement">SiteElement</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a> &lt;
          <a
          href>Place</a>&lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">(attr) modification</td>
      <td style="text-align:left">ModificationEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Type of change (audit action). For example, <code>delete</code> when deleting
        a stop place.</td>
    </tr>
    <tr>
      <td style="text-align:left">Description</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Description. Used to supplement stop place name. Usage of this field is
        closely tied to which fields are made public in the end.</td>
    </tr>
    <tr>
      <td style="text-align:left">PrivateCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">An internal code that uniquely identifies the Stop Place. May be used
        for interoperating with legacy systems.</td>
    </tr>
    <tr>
      <td style="text-align:left">PublicCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">A short, human-readable, public code that uniquely identifies the Stop
        Place. The public code may be used for interacting with passengers when
        it provides a convenient alternative to the (longer) Stop Place name or
        NeTEx ID.</td>
    </tr>
    <tr>
      <td style="text-align:left">TransportMode</td>
      <td style="text-align:left">VehicleModeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Main transport type for the stop place.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) AirSubmode</td>
      <td style="text-align:left">AirSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for air.</p>
        <p>See <a href>Transport Modes</a> for possible values</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) BusSubmode</td>
      <td style="text-align:left">BusSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for bus.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) FunicularSubmode</td>
      <td style="text-align:left">FunicularSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for funicular.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) MetroSubmode</td>
      <td style="text-align:left">MetroSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for metro.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) TramSubmode</td>
      <td style="text-align:left">TramSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for tram.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) TelecabinSubmode</td>
      <td style="text-align:left">TelecabinSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for telecabin.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) RailSubmode</td>
      <td style="text-align:left">RailSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for rail.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) WaterSubmode</td>
      <td style="text-align:left">WaterSubmodeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Submodes for waterborne transport types.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">OtherTransportModes</td>
      <td style="text-align:left">VehicleModeListOfEnumerations
        <br />(<em>tilsvarer VehicleModeEnumeration</em>)</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>List of other available transport types <em>(valid values are the same as for transport type).</em>
        </p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">tariffZones</td>
      <td style="text-align:left">TariffZoneRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Reference to <a href="handbok-n801-siri-netex-network.md#network-TariffZone">TariffZone</a> associated
        with the stop place.</td>
    </tr>
    <tr>
      <td style="text-align:left">StopPlaceType</td>
      <td style="text-align:left">StopTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Classification of stop place:</p>
        <ul>
          <li>onstreetBus (bus stops)</li>
          <li>onstreetTram (tram stops)</li>
          <li>taxiStand (taxi stations)</li>
          <li>airport (airports)</li>
          <li>railStation (railway stations)</li>
          <li>metroStation (metro or subway stations)</li>
          <li>busStation (bus terminals (different from regular bus stops))</li>
          <li>harbourPort (ports where cars may board or disembark a ship)</li>
          <li>ferryStop (ports where people can board or disembark a ship)</li>
          <li>liftStation (station for a cable borne vehicle)</li>
        </ul>
        <p><em>Mandatory when StopPlace has one or more subordinate Quay.</em>
          <br
          /><em>Not mandatory if the StopPlace is a parentStop.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BorderCrossing</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies if the stop is an international border crossing.</td>
    </tr>
    <tr>
      <td style="text-align:left">Weighting</td>
      <td style="text-align:left">InterchangeWeightingEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Relative weighting for interchanges at the stop.</p>
        <ul>
          <li>preferredInterchange</li>
          <li>recommendedInterchange</li>
          <li>interchangeAllowed</li>
          <li>noInterchange</li>
        </ul>
        <p><em>Corresponds to Priority for</em>  <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-Interchange"><em>Interchange</em></a><em> </em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">quays</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#Quay">Quay</a>
      </td>
      <td style="text-align:left">
        <p>1: * (<em>for leaf StopPlace</em>)</p>
        <p>0 (<em>for parent StopPlace or unknown Quay</em>)</p>
      </td>
      <td style="text-align:left">
        <p>List of Quays at the StopPlace</p>
        <ul>
          <li><em>One or more for normal StopPlaces. Specifies exact boarding position.</em>
          </li>
          <li><em>Must be <b>none if the StopPlace is a parentStop</b> with subordinate StopPlaces.</em>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">accessSpaces</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AccessSpace">AccessSpace</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of access spaces at the StopPlace</td>
    </tr>
    <tr>
      <td style="text-align:left">pathLinks</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathLink">PathLink</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Elements describing part of a path link (walking link)</td>
    </tr>
    <tr>
      <td style="text-align:left">pathJunctions</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathJunction">PathJunction</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Part of a path link which describes a point where one or many <a href="handbok-n801-siri-netex-stops.md#stops-PathLink">PathLinks</a> connect
        to each other.</td>
    </tr>
    <tr>
      <td style="text-align:left">navigationPaths</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#NavigationPath">NavigationPath</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of path links at- or associated with the StopPlace.</p>
        <p><em>Used only when path links should be overridden, or if it is not relevant to define pathLinks for the StopPlace.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### StopPlaceSpace <a id="stops-StopPlaceSpace"></a>

An abstract class describing details for an area within a [StopPlace.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPlace)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StopPlaceSpace)

| StopPlaceSpace &lt; [SiteElement](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement)  &lt; [AddressablePlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace) &lt; [Place]() &lt; [Zone]() &lt; [GroupOfPoints]()  &lt; [GroupOfEntities]()  &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| entrances | [Entrance](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#Entrance) | 0: \* | Description of entrances |

#### Quay <a id="stops-Quay"></a>

A part of [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#StopPlace.1) where passengers can board or disembark a vehicle. For example tactile paving position at a bus stop, the midpoint of a railway platform, a gate at an airport.

[See definition under General information.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Quay)

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/BasicStopPlace_example.xml).

_Please note:_

* _Quays do **not** have their own names. This information is inherited from the parent StopPlace._
* _QuayType is **not** to be specified. This information is inherited from TransportMode on the parent StopPlace. The Norwegian NeTEx profile does not allow "multimodal" Quays._

| Quay &lt; [StopPlaceSpace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#StopPlaceSpace) &lt; [SiteElement](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement)  &lt; [AddressablePlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace) &lt; [Place]() &lt; [Zone]() &lt; [GroupOfPoints]()  &lt; [GroupOfEntities]()  &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| PrivateCode | xsd:normalizedString | 0: 1 | Internal code or information not to be presented to the public. |
| PublicCode | xsd:normalizedString | 0: 1 | A public code for a Quay, usually linked to a physical sign with a letter or number for the platform/track. |
| \(attr\) modification | xs:ModificationEnumeration | 0: 1 | Type of change \(audit action\). For example, `delete` when deleting a Quay. |
| CompassBearing | AbsoluteBearingType | 0: 1 | The compass bearing \(direction\) of the Quay, i.e. which direction will vehicles leaving the Quay travel. Set in degrees. |
| boardingPositions | [BoardingPosition](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#BoardingPosition) | 0: \* | List of boarding positions along a Quay, typically used for railway platforms. |

#### BoardingPosition <a id="stops-BoardingPosition"></a>

Description of a boarding position. Currently defined to be used only for rail.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-BoardingPosition)

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/OsloS_station_example.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">BoardingPosition &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#StopPlaceSpace">StopPlaceSpace</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement">SiteElement</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a> &lt;
          <a
          href>Place</a>&lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">Label</td>
      <td style="text-align:left">MultilingualString</td>
      <td style="text-align:left">1:1</td>
      <td style="text-align:left">A code usually linked to a physical sign with a letter or number for the
        platform/track.</td>
    </tr>
    <tr>
      <td style="text-align:left">BoardingPositionType</td>
      <td style="text-align:left">BoardingPositionTypeEnumeration</td>
      <td style="text-align:left">1:1</td>
      <td style="text-align:left">
        <p>Classification for BoardingPosition:</p>
        <ul>
          <li>positionOnRailPlatform</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Inner Objects <a id="stops-InnerObjects"></a>

**AccessSpace**

Description of waiting areas on a [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#StopPlace.1)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-AccessSpace)

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/OsloS_station_example.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">AccessSpace &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#StopPlaceSpace">StopPlaceSpace</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement">SiteElement</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a> &lt;
          <a
          href>Place</a>&lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">AccessSpaceType</td>
      <td style="text-align:left">AccessSpaceTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Classification of AccessSpace:</p>
        <ul>
          <li>concourse (<em>for example the main hall of a central train station or an airport terminal</em>)</li>
          <li>underpass</li>
          <li>overpass</li>
          <li>passage</li>
          <li>lift</li>
          <li>waitingRoom</li>
          <li>staircase</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**PathLink**

A link between two [Place]()-objects which describe a \(possible\) path link between them.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-PathLink)

<table>
  <thead>
    <tr>
      <th style="text-align:left">PathLink &lt; <a href>Link</a>&lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">From</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathLinkEndStructure">PathLinkEndStructure</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Starting position for the PathLink</td>
    </tr>
    <tr>
      <td style="text-align:left">To</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathLinkEndStructure">PathLinkEndStructure</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">End position for the PathLink</td>
    </tr>
    <tr>
      <td style="text-align:left">Description</td>
      <td style="text-align:left"><a href>MultilingualString</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">AccessibilityAssessment</td>
      <td style="text-align:left"><a href>AccessibilityAssessment</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Universal Design - description of the path link</p>
        <p><em>Only used when AccessibilityAssessment for</em>  <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#NavigationPath"><em>NavigationPath</em></a>  <em>of which the PathLink is a part, needs to be specified in further detail.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Covered</td>
      <td style="text-align:left">CoveredEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>indoors</li>
          <li>outdoors</li>
          <li>mixed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Gated</td>
      <td style="text-align:left">GatedEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>gatedArea</li>
          <li>openArea</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Lighting</td>
      <td style="text-align:left">LightingEnumeraion</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>wellLit</li>
          <li>poorlyLit</li>
          <li>unlit</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">AllowedUse</td>
      <td style="text-align:left">DirectionOfUseEnum</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>up</li>
          <li>down</li>
          <li>both</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Transition</td>
      <td style="text-align:left">TransitionEnum</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>up</li>
          <li>down</li>
          <li>level</li>
          <li>upAndDown</li>
          <li>downAndUp</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">AccessFeatureType</td>
      <td style="text-align:left">AccessFeatureEnum</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>lift</li>
          <li>escalator</li>
          <li>travelator</li>
          <li>ramp</li>
          <li>stairs</li>
          <li>crossing</li>
          <li>barrier</li>
          <li>narrowEntrance</li>
          <li>concourse</li>
          <li>queueManagement</li>
          <li>street</li>
          <li>pavement</li>
          <li>footpath</li>
          <li>passage</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">PassageType</td>
      <td style="text-align:left">PassageTypeEnum</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>pathway</li>
          <li>corridor</li>
          <li>overpass</li>
          <li>underpass</li>
          <li>tunnel</li>
          <li>none</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">TransferDuration</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-network.md#network-TransferDuration">TransferDuration</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration of time needed to traverse the path link</td>
    </tr>
    <tr>
      <td style="text-align:left">checks</td>
      <td style="text-align:left"><a href>CheckConstraint</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Processes or constraints which may cause queues or delays.</td>
    </tr>
  </tbody>
</table>

**PathJunction**

A junction within-, or connected to a [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#StopPlace.1) or [PointOfInterest](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PointOfInterest), where path links meet or split.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-PathJunction)

<table>
  <thead>
    <tr>
      <th style="text-align:left">PathJunction &lt; <a href>Point</a> &lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">Covered</td>
      <td style="text-align:left">CoveredEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>indoors</li>
          <li>outdoors</li>
          <li>covered</li>
          <li>mixed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Gated</td>
      <td style="text-align:left">GatedEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>gatedArea</li>
          <li>openArea</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Lighting</td>
      <td style="text-align:left">LightingEnumeraion</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>wellLit</li>
          <li>poorlyLit</li>
          <li>unlit</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**EquipmentPlace**

Available equipment at a [Site.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Site)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-EquipmentPlace)

| EquipmentPlace &lt; [Place]() &lt; [Zone]() &lt; [GroupOfPoints]()  &lt; [GroupOfEntities]()  &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| placeEquipments | [Equipment]() | 0: \* | Description of available equipment. Use the classes which inherit from Equipment. For more details, see [EquipmentTypes](). |

**SiteFacilitySet**

Description of services available for a [Site.](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Site)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-SiteFacilitySet)

_Defined in SiteFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/StopPlace-with-equipment-and-parking_example.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">SiteFacilitySet &lt; <a href>FacilitySet</a> &lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">LuggageLockerFacilityList</td>
      <td style="text-align:left">LuggageLockerFacilityLisfOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>lockers</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">LuggageServiceFacilityList</td>
      <td style="text-align:left">LuggageServiceFacilityLisfOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>leftLuggage</li>
          <li>baggageChekInCheckOut</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingFacilityList</td>
      <td style="text-align:left">ParkingFacilityLisfOfEnumerations</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>carPark</li>
          <li>parkAndRidePark</li>
          <li>motorcyclePark</li>
          <li>cyclePark</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Flexible Stop Place <a id="stops-FlexibleStopPlace"></a>

#### FlexibleStopPlace <a id="stops-FlexibleStopPlace.1"></a>

Description of a stop place area for on-demand transport \(FlexibleLines\).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleStopPlace)

_Defined in SiteFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">FlexibleStopPlace &lt; <a href>Place</a> &lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt;
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
      <td style="text-align:left">TransportMode</td>
      <td style="text-align:left">VehicleModeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Main transport mode for the stop place.</p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">areas</td>
      <td style="text-align:left">(choice) <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#FlexibleArea">FlexibleArea</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Zones where on-demand transport is available.</td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#HailAndRideArea">HailAndRideArea</a>
      </td>
      <td style="text-align:left">Road sections/segments where the transporting vehicle may be hailed.</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

#### FlexibleQuay <a id="stops-FlexibleQuay"></a>

Description of a specific area where on-demand transport is possible.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleQuay)

_Defined in SiteFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">FlexibleQuay &lt; <a href>Place</a> &lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt;
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
      <td style="text-align:left">TransportMode</td>
      <td style="text-align:left">VehicleModeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Transport type for the flexible Quay (used to override transport type
          defined in superordinate <a href="handbok-n801-siri-netex-stops.md#stops-FlexibleStop">FlexibleStop)</a>
        </p>
        <p>See <a href>Transport Modes</a> for possible values.</p>
      </td>
    </tr>
  </tbody>
</table>

#### FlexibleArea <a id="stops-FlexibleArea"></a>

Description of an area for on-demand transport, in practice, a [FlexibleQuay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#FlexibleQuay).

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-FlexibleArea)

| FlexibleArea &lt; [FlexibleQuay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#FlexibleQuay) &lt;  [Place]() &lt; [Zone]() &lt; [GroupOfPoints]()  &lt; [GroupOfEntities]()  &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Name | normalizedString | 0: 1 | Name of the area \(_if necessary for override/detail_\). |
| Description | normalizedString | 0: 1 | Description of area \(_if necessary for override/detail_\). |
| destinations | DestinationDisplayRef | 0: \* | References to [DestinationDisplay](handbok-n801-siri-netex-network.md#network-DestinationDisplay) objects. |

#### HailAndRideArea <a id="stops-HailAndRideArea"></a>

Description of an area where it is possible to hail a vehicle.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-HailAndRideArea)

| HailAndRideArea &lt; [FlexibleQuay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#FlexibleQuay)  &lt;  [Place]() &lt; [Zone]() &lt; [GroupOfPoints]()  &lt; [GroupOfEntities]()  &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| destinations | DestinationDisplayRef | 0: \* | References to [DestinationDisplay](handbok-n801-siri-netex-network.md#network-DestinationDisplay) objects |
| StartPointRef | PointRef | 1: 1 | Start of section |
| EndPointRef | PointRef | 1: 1 | End of section |

### Point of Interest <a id="stops-PointofInterest"></a>

#### PointOfInterest <a id="stops-PointOfInterest"></a>

A location \(POI\) which may be of interest to people utilizing public transport, for example, museums, stadiums or monuments.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-POI)

_Defined in SiteFrame_

<table>
  <thead>
    <tr>
      <th style="text-align:left">PointOfInterest &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#%5BhardBreak%5DSite">Site</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement">SiteElement</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a> &lt;
          <a
          href>Place</a>&lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">nearTopographicPlaces</td>
      <td style="text-align:left">TopographicPlaceRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">References to nearby <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#TopographicPlace">TopographicPlace</a>-objects</td>
    </tr>
    <tr>
      <td style="text-align:left">pathLinks</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathLink">PathLink</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">An element which describes a part of a path link.</td>
    </tr>
    <tr>
      <td style="text-align:left">pathJunctions</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathJunction">PathJunction</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Part of a path link which describes where one or more <a href="handbok-n801-siri-netex-stops.md#stops-PathLink">PathLinks</a> are
        connected.</td>
    </tr>
    <tr>
      <td style="text-align:left">navigationPaths</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#NavigationPath">NavigationPath</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Description of a path to or from a POI.</p>
        <p><em>Used <b>only</b> when overriding a pathLink, or as a piece of stand-alone information if it is not relevant to define pathLinks for the StopPlace.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

### Parking <a id="stops-Parking"></a>

#### Parking <a id="stops-Parking.1"></a>

A place to park private road vehicles.

_Please note that a parking location always needs to refer to a StopPlace by means of Site/parentSiteRef._

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Parking)

_Defined in SiteFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/StopPlace-with-equipment-and-parking_example.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">Parking &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#%5BhardBreak%5DSite">Site</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement">SiteElement</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace">AddressablePlace</a> &lt;
          <a
          href>Place</a>&lt; <a href>Zone</a> &lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">pathLinks</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathLink">PathLink</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">An element which describes part of a path link</td>
    </tr>
    <tr>
      <td style="text-align:left">pathJunctions</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathJunction">PathJunction</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Part of a path link which describes a point where one or more <a href="handbok-n801-siri-netex-stops.md#stops-PathLink">PathLinks</a> are
        connected.</td>
    </tr>
    <tr>
      <td style="text-align:left">navigationPaths</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#NavigationPath">NavigationPath</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Navigation description to and from a parking location.</p>
        <p><em>Used <b>only</b> when overriding a pathLink, or as stand-alone information if it is not relevant to define pathLinks for the StopPlace.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingType</td>
      <td style="text-align:left">ParkingTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of parking:</p>
        <ul>
          <li>parkAndRide</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingVehicleType</td>
      <td style="text-align:left">ParkingVehicleEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible vehicle types:</p>
        <ul>
          <li>car</li>
          <li>motorcycle</li>
          <li>pedalCycle</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingLayout</td>
      <td style="text-align:left">ParkingLayoutEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type/layout of parking values:</p>
        <ul>
          <li>openSpace</li>
          <li>multistorey</li>
          <li>underground</li>
          <li>roadside</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingPaymentProcess</td>
      <td style="text-align:left">ParkingPaymentProcessEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>A space-separated list of available payment processes.
          <br />Possible values:</p>
        <ul>
          <li>free: No payment required at any time for any user category.</li>
          <li>payAndDisplay: Payment by purchasing a ticket on the spot.</li>
          <li>payByPrepaidToken: Payment through a registration process, prior to using
            the parking. The proof of registration can be a transponder token, a parking
            permit card, &#x2026;</li>
          <li>payByMobileDevice: Payment by mobile phone application or SMS.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">PrincipalCapacity</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Available public parking spaces (reservable spaces excluded)</td>
    </tr>
    <tr>
      <td style="text-align:left">TotalCapacity</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Total number of parking spaces (reservable spaces included)</p>
        <p><em>When the number of reservable spaces is unknown, only specify TotalCapacity.</em>
        </p>
        <p><em>The TotalCapacity should be equal to the sum of spaces defined in the ParkingCapacity sub-elements.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">OvernightParkingPermitted</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies if overnight parking is allowed</td>
    </tr>
    <tr>
      <td style="text-align:left">RechargingAvailable</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Specifies if the parking area has charging stations for electrical vehicles.</p>
        <p>Must be set to true if NumberOfSpacesWithRechargePoint is specified in
          a ParkingCapacity element.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Secure</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies if the parking area is guarded by some form of security service.</td>
    </tr>
    <tr>
      <td style="text-align:left">RealTimeOccupancyAvailable</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether the parking area has real-time information regarding
        occupancy.</td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingReservation</td>
      <td style="text-align:left">ParkingReservationEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Parking reservation values:</p>
        <ul>
          <li>noReservations</li>
          <li>registrationRequired</li>
          <li>reservationRequired</li>
          <li>reservationAllowed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">BookingUrl</td>
      <td style="text-align:left">xsd:anyURI</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">URL for reserving a parking space</td>
    </tr>
    <tr>
      <td style="text-align:left">FreeParkingOutOfHours</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies whether parking at the area is free outside &quot;office hours&quot;.</td>
    </tr>
    <tr>
      <td style="text-align:left">parkingProperties</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#ParkingProperties">ParkingProperties</a>
      </td>
      <td style="text-align:left">0:*</td>
      <td style="text-align:left">Additional properties for the parking area</td>
    </tr>
    <tr>
      <td style="text-align:left">parkingAreas</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#ParkingCapacity">ParkingArea</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Description of individual areas inside the parking.</td>
    </tr>
  </tbody>
</table>

#### ParkingArea <a id="stops-ParkingArea"></a>

A subsection of a parking area.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ParkingArea)

| ParkingArea &lt; ParkingComponent &lt; SiteComponent &lt; [SiteElement](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#SiteElement)  &lt; [AddressablePlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#AddressablePlace) &lt; [Place]() &lt; [Zone]() &lt; [GroupOfPoints]()  &lt; [GroupOfEntities]()  &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| Label | [MultilingualString]() | 0: 1 | Label or identifier for the subsection presented to the public |
| TotalCapacity | xsd:nonNegativeInteger | 0: 1 | Total capacity for the specific subsection |
| ParkingProperties | [ParkingProperties](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#ParkingProperties) | 0: 1 | Additional properties for the parking subsection |

#### ParkingProperties <a id="stops-ParkingProperties"></a>

Additional properties for a parking.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ParkingProperties)

<table>
  <thead>
    <tr>
      <th style="text-align:left">ParkingProperties &lt; VersionedChild &lt; <a href>EntityInVersion</a> &lt;
        <a
        href>Entity</a>
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
      <td style="text-align:left">ParkingUserTypes</td>
      <td style="text-align:left">ParkingUserListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>User classification:</p>
        <ul>
          <li>all</li>
          <li>registered</li>
          <li>registeredDisabled</li>
          <li>residentsWithPermits</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">MaximumStay</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum allowed time to stay parked</td>
    </tr>
    <tr>
      <td style="text-align:left">spaces</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#ParkingCapacity">ParkingCapacity</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">A detailed description of the parking capacity</td>
    </tr>
  </tbody>
</table>

#### ParkingCapacity <a id="stops-ParkingCapacity"></a>

A detailed description of the parking capacity.

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ParkingCapacity)

<table>
  <thead>
    <tr>
      <th style="text-align:left">ParkingCapacity &lt; VersionedChild &lt; <a href>EntityInVersion</a> &lt;
        <a
        href>Entity</a>
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
      <td style="text-align:left">ParkingVehicleType</td>
      <td style="text-align:left">ParkingVehicleEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Vehicle types:</p>
        <ul>
          <li>car</li>
          <li>motorcycle</li>
          <li>pedalCycle</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingUserType</td>
      <td style="text-align:left">ParkingUserEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>User types:</p>
        <ul>
          <li>allUsers: the spaces are available for all user types.</li>
          <li>registeredDisabled: the spaces are available only for disabled users.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ParkingStayType</td>
      <td style="text-align:left">ParkingStayEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Parking duration values:</p>
        <ul>
          <li>shortStay</li>
          <li>longTerm</li>
          <li>dropoff</li>
          <li>unlimited</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">NumberOfSpaces</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Number of parking spaces</td>
    </tr>
    <tr>
      <td style="text-align:left">NumberOfSpacesWithRechargePoint</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Number of spaces with a recharge point.</p>
        <p>This property should be set in a ParkingCapacity element where the property
          ParkingUserType is equal to &#x201C;allUsers&#x201D;.</p>
      </td>
    </tr>
  </tbody>
</table>

### Navigation <a id="stops-Navigation"></a>

#### NavigationPath <a id="stops-NavigationPath"></a>

A detailed description of the path between two places \(_can usually be derived automatically from_ [_PathLinks_](handbok-n801-siri-netex-stops.md#stops-PathLink)\)

[See definition under General information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-NavigationPath)

_Defined in SiteFrame_

Examples in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/StopPlace-with-equipment-and-parking_example.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">NavigationPath &lt; <a href>LinkSequence</a> &lt; <a href>DataManagedObject</a>
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
      <td style="text-align:left">From</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathLinkEndStructure">PathLinkEndStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The starting point for the path link</td>
    </tr>
    <tr>
      <td style="text-align:left">To</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#PathLinkEndStructure">PathLinkEndStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">The endpoint for the path link</td>
    </tr>
    <tr>
      <td style="text-align:left">AccessibilityAssessment</td>
      <td style="text-align:left"><a href>AccessibilityAssessment</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Universal Design - Description of the path link</td>
    </tr>
    <tr>
      <td style="text-align:left">TransferDuration</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-network.md#network-TransferDuration">TransferDuration</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Specifies the duration of the transfer</td>
    </tr>
    <tr>
      <td style="text-align:left">Covered</td>
      <td style="text-align:left">CoveredEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>indoors</li>
          <li>outdoors</li>
          <li>covered</li>
          <li>mixed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Gated</td>
      <td style="text-align:left">GatedEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>gatedArea</li>
          <li>openArea</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Lighting</td>
      <td style="text-align:left">LightingEnumeraion</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Possible values:</p>
        <ul>
          <li>wellLit</li>
          <li>poorlyLit</li>
          <li>unlit</li>
          <li>unknown</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">NavigationType</td>
      <td style="text-align:left">NavigationTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Path link types:</p>
        <ul>
          <li>hallToQuay</li>
          <li>hallToStreet</li>
          <li>quayToHall</li>
          <li>quayToStreet</li>
          <li>streetToHall</li>
          <li>streetToQuay</li>
          <li>streetToSpace</li>
          <li>streetTostreet</li>
          <li>spaceToHall</li>
          <li>hallToSpace</li>
          <li>spaceToSpace</li>
          <li>other</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">pathLinksInSequence</td>
      <td style="text-align:left">PathLinkInSequence</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Sequential list of <a href="handbok-n801-siri-netex-stops.md#stops-PathLink">PathLinks</a>,
        that describe each part of the total walk path.</td>
    </tr>
  </tbody>
</table>

**PathLinkEndStructure**

| PathLinkEndSturcture |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| PlaceRef | PlaceRef | 0: 1 | Reference to [Place]() |

### Zonal <a id="stops-Zonal"></a>

#### TariffZone <a id="stops-TariffZone"></a>

A ZONE used to define a zonal fare structure in a zone-counting or zone-matrix system.

Example found [in GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/site/submodel-StationWithEquipment.xml) 

| TariffZone &lt; [Zone]() &lt; [GroupOfPoints]() &lt; [GroupOfEntities]() &lt; [DataManagedObject]() |  |  |  |
| :--- | :--- | :--- | :--- |
| Name | Type | Cardinality | Description |
| ~~members~~ | [~~PointRef~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Point) | ~~0: \*~~ | ~~List of~~ [~~ScheduledStopPoints~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ScheduledStopPoint) ~~within TARIFF ZONE~~ |
| Presentation | [Presentation](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#Presentation) | 0: 1 | Presentation features associated with TARIFF ZONE |

#### FareZone <a id="stops-FareZone"></a>

Under development

A specialization of TARIFF ZONE to include fare related zonal information.

Example found [in GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/site/submodel-StationWithEquipment.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">FareZone &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#TariffZone">TariffZone</a> &lt;
        <a
        href>Zone</a>&lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">PrivateCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">An internal code that uniquely identifies the FareZone, e.g. for use with
        technical data management</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>PublicCode</del>
      </td>
      <td style="text-align:left"><del>xsd:normalizedString</del>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left">
        <p><del>A short, human-readable, public code that uniquely identifies the Fare Zone.</del>
        </p>
        <p><del>This public code may e.g. be used for passenger information as publicized alternative to the FareZone ID or Name.</del>
        </p>
        <p><em>Not yet included in NeTEx</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">members</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Point">PointRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>List of <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ScheduledStopPoint">ScheduledStopPoints</a> within
          the FARE ZONE</p>
        <p><em>Only to be used in conjunction with ScopingMethod &#x201C;explicitStops&#x201D;</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ZoneTopology</td>
      <td style="text-align:left">ZoneTopologyEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Topology of FARE ZONE with regard to other zones.</p>
        <p>Allowed values:</p>
        <ul>
          <li><code>tiled</code>  <em>(arbitrary shapes, adjacent but may not overlap)</em>
          </li>
          <li><code>sequence</code> Zones <em>(arranged as adjacent tiles in sequence that touch at either or both ends. They do not overlap.)</em>
          </li>
          <li><code>overlapping</code>  <em>(arbitrary shapes that may overlap)</em>
          </li>
          <li><code>nested</code>  <em>(zones fully contained and automatically included if outer zone is selected, may also overlap with neighbour zones)</em>
          </li>
          <li><del>honeycomb</del>  <del><em>(specialization of tiled; regular polygons e.g. Hexagons, squares etc. that do not overlap)</em></del>
          </li>
          <li><del>annular</del>  <del><em>(Zones are arranged in tiled hollow rings. The area of any immediately nested zone is excluded from the containing outer zone)</em></del>
          </li>
          <li><del>overlappingSequence</del>  <del><em>(Zones are arranged as adjacent tiles in sequence that touch at either or both ends. They may partially overlap such that some stops are in both zones)</em></del>
          </li>
          <li><del>ring</del>  <del><em>(nested inner zones are included in any containing outer zones)</em></del>
          </li>
          <li><del>other</del>  <del><em>(Zone has other or unspecified topology)</em></del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ScopingMethod</td>
      <td style="text-align:left">ScopingMethodEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Indication of how member stops of a FARE ZONE are specified</p>
        <p>Allowed values:</p>
        <ul>
          <li><code>explicitStops</code>  <em>(stated members of the zone)</em>
          </li>
          <li><code>implicitSpatialProjection</code>  <em>(if spatially contained then regarded as member of the zone)</em>
          </li>
        </ul>
        <p><em>If ScopingMethod is &#x201C;explicit&#x201D;, all</em>  <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#ScheduledStopPoint"><em>ScheduledStopPoints</em></a>  <em>within the FareZone must be referred in its list of &lt;members&gt;</em>
        </p>
        <ul>
          <li><del>explicitPeripheryStops</del>  <del><em>(The extent of the zone is indicated by a set of stops marking the border points</em></del>
            <br
            /><del><em>on the periphery of the FARE ZONE. Any stop that is spatially contained within the indicated extent is assumed to be a member)</em></del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">AuthorityRef</td>
      <td style="text-align:left">OrganisationRefStructure</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">Reference to AUTHORITY of FARE ZONE</td>
    </tr>
    <tr>
      <td style="text-align:left">neighbours</td>
      <td style="text-align:left">FareZoneRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">
        <p>Adjacent FARE ZONEs</p>
        <p><em>Used to define adjacent Zones in context of fare calculation/management, i.e. explicitly treated as an allowed Zone traversal adding <b>one</b> new zone to the count. If <b>not</b> defined as neighbours, the Zone traversal should by systems using this parameter, be assessed as <b>not allowed</b> (in relation to calculation of Zone travelsals) regardless of physical proximity.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### GroupOfTariffZones <a id="stops-GroupOfTariffZones"></a>

Under development

A grouping of TARIFF ZONEs which will be commonly referenced for a specific purpose.

Example found [in GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/site/submodel-StationWithEquipment.xml) 

<table>
  <thead>
    <tr>
      <th style="text-align:left">FareZone &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#TariffZone">TariffZone</a> &lt;
        <a
        href>Zone</a>&lt; <a href>GroupOfPoints</a> &lt; <a href>GroupOfEntities</a> &lt;
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
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Type</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">PurposeOfGroupingRef</td>
      <td style="text-align:left">
        <p>xsd:normalizedString</p>
        <p><em>predefined values, see Description</em>
        </p>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Categorization for the grouping, defined by referencing predefined PurposeOfGrouping:</p>
        <ul>
          <li>TO BE DECIDED</li>
        </ul>
        <p>Example:
          <br /><code>&lt;PurposeOfGroupingRef ref=&quot;NSR:PurposeOfGrouping:generalization&quot;/&gt;</code>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">PrivateCode</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">An internal code that uniquely identifies the GroupOfTariffZone, e.g.
        for use with technical data management</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>PublicCode</del>
      </td>
      <td style="text-align:left"><del>xsd:normalizedString</del>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left">
        <p><del>A short, human-readable, public code that uniquely identifies the Fare Zone.</del>
        </p>
        <p><del>This public code may e.g. be used for passenger information as publicized alternative to the FareZone ID or Name.</del>
        </p>
        <p><em>Not yet included in NeTEx. RELEVANT FOR THIS GROUPING?</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">members</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727661/stops#TariffZone">TariffZoneRef</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">List of TariffZones (or more specifically FareZones) within the GROUP
        OF TARIFF ZONEs</td>
    </tr>
  </tbody>
</table>

