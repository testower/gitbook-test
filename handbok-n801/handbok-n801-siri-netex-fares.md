# Håndbok N801 \(SIRI/NeTEX\) : fares

This page is currently a work in progress and not yet included in the Nordic NeTEx Profile

**Version**

Current version for **fares** is:   **v0.8**   \(last changed 20 Oct 2020\) 

## Content <a id="fares-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591705732 {padding: 0px;}  
div.rbtoc1619591705732 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591705732 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Components](handbok-n801-siri-netex-fares.md#fares-Components)
  * [Fare components](handbok-n801-siri-netex-fares.md#fares-Farecomponents)
    * [GeographicalUnit](handbok-n801-siri-netex-fares.md#fares-GeographicalUnit)
    * [GeographicalInterval](handbok-n801-siri-netex-fares.md#fares-GeographicalInterval)
    * [GeographicalStructureFactor](handbok-n801-siri-netex-fares.md#fares-GeographicalStructureFactor)
    * [TimeInterval](handbok-n801-siri-netex-fares.md#fares-TimeInterval)
  * [Controllable elements](handbok-n801-siri-netex-fares.md#fares-Controllableelements)
    * [FareStructureElement](handbok-n801-siri-netex-fares.md#fares-FareStructureElement)
    * [FareStructureElementInSequence](handbok-n801-siri-netex-fares.md#fares-FareStructureElementInSequence)
    * [GenericParameterAssignment](handbok-n801-siri-netex-fares.md#fares-GenericParameterAssignment)
    * [ValidableElement](handbok-n801-siri-netex-fares.md#fares-ValidableElement)
  * [Usage Parameters](handbok-n801-siri-netex-fares.md#fares-UsageParameters)
    * [UsageParameter](handbok-n801-siri-netex-fares.md#fares-UsageParameter)
    * [UserProfile](handbok-n801-siri-netex-fares.md#fares-UserProfile)
    * [UsageValidityPeriod](handbok-n801-siri-netex-fares.md#fares-UsageValidityPeriod)
    * [Suspending](handbok-n801-siri-netex-fares.md#fares-Suspending)
    * [RoundTrip](handbok-n801-siri-netex-fares.md#fares-RoundTrip)
    * [FrequencyOfUse](handbok-n801-siri-netex-fares.md#fares-FrequencyOfUse)
    * [Interchanging](handbok-n801-siri-netex-fares.md#fares-Interchanging)
    * [LuggageAllowance](handbok-n801-siri-netex-fares.md#fares-LuggageAllowance)
    * [PurchaseWindow](handbok-n801-siri-netex-fares.md#fares-PurchaseWindow)
    * [Reserving](handbok-n801-siri-netex-fares.md#fares-Reserving)
    * [Cancelling](handbok-n801-siri-netex-fares.md#fares-Cancelling)
    * [ChargingPolicy ](handbok-n801-siri-netex-fares.md#fares-ChargingPolicy)
    * [PenaltyPolicy ](handbok-n801-siri-netex-fares.md#fares-PenaltyPolicy)
    * [Subscribing ](handbok-n801-siri-netex-fares.md#fares-Subscribing)
    * [GroupTicket](handbok-n801-siri-netex-fares.md#fares-GroupTicket)
    * [CompanionProfile](handbok-n801-siri-netex-fares.md#fares-CompanionProfile)
    * [CommercialProfile](handbok-n801-siri-netex-fares.md#fares-CommercialProfile)
    * [Transferability](handbok-n801-siri-netex-fares.md#fares-Transferability)
    * [Reselling](handbok-n801-siri-netex-fares.md#fares-Reselling)
    * [Refunding](handbok-n801-siri-netex-fares.md#fares-Refunding)
    * [Exchanging](handbok-n801-siri-netex-fares.md#fares-Exchanging)
    * [Replacing](handbok-n801-siri-netex-fares.md#fares-Replacing)
  * [Fare Product](handbok-n801-siri-netex-fares.md#fares-FareProduct)
    * [ServiceAccessRight](handbok-n801-siri-netex-fares.md#fares-ServiceAccessRight)
    * [FareProduct](handbok-n801-siri-netex-fares.md#fares-FareProduct.1)
    * [PreassignedFareProduct](handbok-n801-siri-netex-fares.md#fares-PreassignedFareProduct)
    * [AccessRightInProduct](handbok-n801-siri-netex-fares.md#fares-AccessRightInProduct)
    * [SupplementProduct](handbok-n801-siri-netex-fares.md#fares-SupplementProduct)
    * [ThirdPartyProduct](handbok-n801-siri-netex-fares.md#fares-ThirdPartyProduct)
    * [SaleDiscountRight](handbok-n801-siri-netex-fares.md#fares-SaleDiscountRight)
    * [CappedDiscountRight](handbok-n801-siri-netex-fares.md#fares-CappedDiscountRight)
    * [CappingRule](handbok-n801-siri-netex-fares.md#fares-CappingRule)
  * [Pricing](handbok-n801-siri-netex-fares.md#fares-Pricing)
    * [GeographicalUnitPrice](handbok-n801-siri-netex-fares.md#fares-GeographicalUnitPrice)
    * [GeographicalIntervalPrice](handbok-n801-siri-netex-fares.md#fares-GeographicalIntervalPrice)
    * [FareStructureElementPrice](handbok-n801-siri-netex-fares.md#fares-FareStructureElementPrice)
    * [UsageParameterPrice](handbok-n801-siri-netex-fares.md#fares-UsageParameterPrice)
    * [FareProductPrice](handbok-n801-siri-netex-fares.md#fares-FareProductPrice)
    * [FulfilmentMethodPrice](handbok-n801-siri-netex-fares.md#fares-FulfilmentMethodPrice)
    * [SalesOfferPackagePrice](handbok-n801-siri-netex-fares.md#fares-SalesOfferPackagePrice)
    * [PriceGroup](handbok-n801-siri-netex-fares.md#fares-PriceGroup)
    * [FareTable](handbok-n801-siri-netex-fares.md#fares-FareTable)
    * [Cell](handbok-n801-siri-netex-fares.md#fares-Cell)
  * [Ticketing](handbok-n801-siri-netex-fares.md#fares-Ticketing)
    * [DistributionChannel](handbok-n801-siri-netex-fares.md#fares-DistributionChannel)
    * [GroupOfDistributionChannels](handbok-n801-siri-netex-fares.md#fares-GroupOfDistributionChannels)
    * [FulfilmentMethod](handbok-n801-siri-netex-fares.md#fares-FulfilmentMethod)
    * [TypeOfTravelDocument](handbok-n801-siri-netex-fares.md#fares-TypeOfTravelDocument)
    * [SalesOfferPackage](handbok-n801-siri-netex-fares.md#fares-SalesOfferPackage)
    * [GroupOfSalesOfferPackages](handbok-n801-siri-netex-fares.md#fares-GroupOfSalesOfferPackages)
    * [SalesOfferPackageElement](handbok-n801-siri-netex-fares.md#fares-SalesOfferPackageElement)
    * [SalesOfferPackageSubstitution](handbok-n801-siri-netex-fares.md#fares-SalesOfferPackageSubstitution)
    * [DistributionAssignment](handbok-n801-siri-netex-fares.md#fares-DistributionAssignment)
    * [GroupOfDistributionAssignments](handbok-n801-siri-netex-fares.md#fares-GroupOfDistributionAssignments)

This document is part of the Norwegian NeTEx Profile and describes data elements for the exchange of **product and fare related information** via the NeTEx format.

Please note the fare/[sales-transaction](https://enturas.atlassian.net/wiki/spaces/AR/pages/1015382117) parts of the profile describes data object for managing and exchanging fare structures, access rights, fare products, pricing, sales management/services, fare validation and consumption, as well as presentation of fare information to the traveling public. It does not, however, describe network or time-related concepts, such as topology, date objects or departure times, as these are described in their respective profile documents [stops](handbok-n801-siri-netex-stops.md)/[network](handbok-n801-siri-netex-network.md) and [timetable](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable).

## Components <a id="fares-Components"></a>

### Fare components <a id="fares-Farecomponents"></a>

#### GeographicalUnit <a id="fares-GeographicalUnit"></a>

A geographical interval specifying access rights for the FARE STRUCTURE ELEMENTs within the range of this interval: “20-5 km”, “4-6 zones”, etc.

| GeographicalUnit &lt; FareUnit &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | Distance | xsd:nonNegativeIntegerpric | 0: 1 | If distance based unit, length of unit |
| element | prices | [GeographicalUnitPriceRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-GeographicalUnitPrice) | 0: \* | Prices associated with GEOGRAPHICALUNIT |

#### GeographicalInterval <a id="fares-GeographicalInterval"></a>

A geographical interval specifying access rights for the FARE STRUCTURE ELEMENTs within the range of this interval: “20-5 km”, “4-6 zones”, etc.

<table>
  <thead>
    <tr>
      <th style="text-align:left">GeographicalInterval &lt; FareStructureFactor &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StartGeographicalValue</td>
      <td style="text-align:left">xsd:decimal</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Start value for GEOGRAPHICAL INTERVAL</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">EndGeographicalValue</td>
      <td style="text-align:left">xsd:decimal</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">End value for GEOGRAPHICAL INTERVAL</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">NumberOfUnits</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Quantity of units in GEOGRAPHICAL INTERVAL</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IntervalType</td>
      <td style="text-align:left">IntervalTypeEnum</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of interval type</p>
        <p>Allowed values:</p>
        <ul>
          <li>coupon</li>
          <li>distance</li>
          <li>section</li>
          <li>stop</li>
          <li>tariffZone</li>
          <li><em>tariffUnit</em> ( mangler for &quot;takstenhet&quot;, dvs ville v&#xE6;rt
            hensiktsmessig med egen type for &#xE5; modellere TEN/FEN )</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">prices</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-GeographicalIntervalPrice">GeographicalIntervalPriceRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Prices for GEOGRAPHICAL INTERVAL</td>
    </tr>
  </tbody>
</table>

**TODO**

Assess the use / necessity of GeographicalStructureFactor, given Fares profile v.1 will have pre-calculated fares

#### GeographicalStructureFactor <a id="fares-GeographicalStructureFactor"></a>

The value of a GEOGRAPHICAL INTERVAL or a DISTANCE MATRIX ELEMENT expressed by a GEOGRAPHICAL UNIT.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| GeographicalStructureFactor &lt; FareStructureFactor &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | DistanceMatrixElementRef | [DistanceMatrixElementRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-DistanceMatrixElement) | 0: 1 | Reference to a DISTANCE MATRIX ELEMENT |
| element | GeographicalIntervalRef | [GeographicalIntervalRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-GeographicalIntervalRef) | 0: 1 | Reference to a GEOGRAPHICAL INTERVAL |
| element | GeographicalUnitRef | [GeographicalUnitRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-GeographicalUnit) | 0: 1 | Reference to GEOGRAPHICAL UNIT |
| element | NumberOfUnits | xsd:integer | 0: 1 | Quantity of units. |
| element | AmountFactor | xsd:decimal | 0: 1 | Arbitrary amount factor associated with Factor |

#### TimeInterval <a id="fares-TimeInterval"></a>

A time-based interval specifying access rights for the FARE STRUCTURE ELEMENTs within the range of this interval: “0-1 hours,” “1-3 days”, etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| TimeInterval &lt; FareInterval &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | StartTime | xsd:time | 0: 1 | Start time of interval |
| element | EndTime | xsd:time | 0: 1 | End time of interval |
| element | Duration | xsd:duration | 1: 1 | Duration for the TimeInterval |

### Controllable elements <a id="fares-Controllableelements"></a>

#### FareStructureElement <a id="fares-FareStructureElement"></a>

A sequence or set of CONTROLLABLE ELEMENTs to which rules for limitation of access rights and calculation of prices \(fare structure\) are applied.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FareStructureElement &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">TariffBasis</td>
      <td style="text-align:left">TariffBasisEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>TARIFF BASIS to be used for the element</p>
        <p>Allowed values:</p>
        <ul>
          <li>flat</li>
          <li>distance</li>
          <li>route</li>
          <li>zone</li>
          <li>period</li>
          <li>tour</li>
          <li>group</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">validityParameterAssignments</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-GenericParameterAssignment">GenericParameterAssignment</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">VALIDITY (i.e. GENERIC) PARAMETER ASSIGNMENTs for an element</td>
    </tr>
    <tr>
      <td style="text-align:left">fareStructureElementsInSequence</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-FareStructureElementInSequence">FareStructureElementInSequence</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">Use of FARESTRUCTURE ELEMENTs in a particular sequence</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">prices</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-FareStructureElementPriceRe">FareStructureElementPriceRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">A set of all possible price features of a FARE STRUCTURE ELEMENT: default
        total price, discount in value or percentage etc.</td>
    </tr>
  </tbody>
</table>

#### FareStructureElementInSequence <a id="fares-FareStructureElementInSequence"></a>

A FARE STRUCTURE ELEMENT as a part of a VALIDABLE ELEMENT, including its possible order in the sequence of FARE STRUCTURE ELEMENTs forming that VALIDABLE ELEMENT, and its possible quantitative limitation.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FareStructureElementInSequence &lt; FareElementInSequence &lt; VersionedChild
        &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">FareStructureElementRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-FareStructureElementRef">FareStructureElementRef</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to a FARE STRUCTURE ELEMENT</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>ValidableElementRef</del>
      </td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-ValidableElementRef"><del>FareStructureElementRef</del></a>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left">
        <p><del>Reference to a VALIDABLE ELEMENT</del>
        </p>
        <p><em>We do currently not want to allow &quot;backwards&quot; referencing</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>validityParameterAssignments</del>
      </td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-ValidityParameterAssignment"><del>ValidityParameterAssignment</del></a>
      </td>
      <td style="text-align:left"><del>0: *</del>
      </td>
      <td style="text-align:left">
        <p><del>VALIDITY PARAMETER ASSIGNMENTs associated with the ELEMENT IN SEQUENCE</del>
        </p>
        <p><em>Should be assigned in the referred GenericParameterAssignment(s), NOT contained as part of the sequence</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### GenericParameterAssignment <a id="fares-GenericParameterAssignment"></a>

A VALIDITY PARAMETER ASSIGNMENT specifying generic access rights for a class of products. May include alternatives from which a purchaser selects.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">GenericParameterAssignment &lt; ValidityParameterAssignment &lt; AccessRightParameterAssignment
        &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">LimitationGroupingType</td>
      <td style="text-align:left">BooleanOperatorEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Logical operator for combining USAGE PARAMETERs elements. The default
          is &#x2018;AND&#x2019;.</p>
        <p><em>&#x2018;OR&#x2019; and &#x2018;XOR&#x2019; should only be used if parameters are all of the same type</em>
        </p>
        <p>Allowed values:</p>
        <ul>
          <li>AND (<em>default, i.e. interpreted as such if not stated</em>) =
            <br />Successive elements are logically ANDed together; comparison must satisfy
            all specified values</li>
          <li>OR =
            <br />Successive elements are logically ORed together; comparison must satisfy
            at least one specified value</li>
          <li>NOT =
            <br />Specified elements <b>must</b> be different from the given value</li>
          <li>XOR =
            <br />Successive elements are logically ORed together; comparison must satisfy <b>only one</b> of
            the specified values</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>LimitationSetSelectionType</del>
      </td>
      <td style="text-align:left"><del>SetOperatorEnumeration</del>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left">
        <p><del>Where one or more parameter is a group containing multiple elements, (GROUP OF xxx), set operator for distinguishing between whole set and item interpretation of elements which are sets of elements</del>
        </p>
        <p><del><em>I.e. only to be used in relation to GroupOf&#x2026; parameters,</em> <em><b>not</b></em> <em>to evaluate combinations of singular parameters</em></del>
        </p>
        <p><del>Allowed values:</del>
        </p>
        <ul>
          <li><del>oneOfAnyOneSet</del>
            <br /><del>(only one item from all  referenced GROUPs OF ENTITies of a given type may be selected/has been selected)</del>
          </li>
          <li><del>oneOfEachSet</del>
            <br /><del>(one item from each specified referenced GROUP OF ENTITies of a given type shall be selected/has been selected)</del>
          </li>
          <li><del>someOfAnySet</del>
            <br /><del>(multiple items from any referenced GROUP OF ENTITies of a given type may be selected/have been selected)</del>
          </li>
          <li><del>allOfOneSet</del>
            <br /><del>(all items from one specified  referenced GROUP OF ENTITies of a given type may be selected/have been selected)</del>
          </li>
          <li><del>allOfAllSets</del>
            <br /><del>(all items from all  referenced GROUPs OF ENTITies of a given type may be selected/have been selected)</del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">limitations</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">UsageParameter</a>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">Limitations (i.e. <em>limitation</em> of use) for the assignment</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ValidityParameterAssignmentType</td>
      <td style="text-align:left">RelativeOperatorEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Comparison operator for matching validity parameter values</p>
        <p>Allowed values:</p>
        <ul>
          <li>EQ (<em>default</em>) =
            <br />Equal (parameter value must have the same identity, or have a value equal
            to a quantitative value associated with the specified item)</li>
          <li>NE =
            <br />Not Equal (parameter value must not have the same identity, or have a
            value different from a quantitative value associated with the specified
            item)</li>
          <li>GT =
            <br />Greater than (parameter value must be greater than a quantitative value
            associated with the specified item)</li>
          <li>GE =
            <br />Greater than or equal (parameter value must be greater than or equal to
            a quantitative value associated with the specified item)</li>
          <li>LT =
            <br />Less than (parameter value must be less than a quantitative value associated
            with the specified item)</li>
          <li>LE =
            <br />Less than or equal (parameter value must be less than or equal to a quantitative
            value associated with the specified item)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ValidityParameterGroupingType</td>
      <td style="text-align:left">BooleanOperatorEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Logical operator for combining network validity parameters, e.g. &#x2018;AND&#x2019;
          / &#x2018;OR&#x2019; / &#x2018;NOT&#x2019; / &#x2018;XOR&#x2019;</p>
        <p>Allowed values:</p>
        <ul>
          <li>AND (<em>default, i.e. interpreted as such if not stated</em>) =
            <br />Successive elements are logically ANDed together; comparison must satisfy <b>all</b> specified
            values</li>
          <li>OR =
            <br />Successive elements are logically ORed together; comparison must satisfy <b>at least one</b> specified
            value</li>
          <li>NOT =
            <br />Specified elements must be <b>different</b> from the given value</li>
          <li>XOR =
            <br />Successive elements are logically ORed together; comparison must satisfy <b>only one</b> of
            the specified values</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ValidityParameterSetSelectionType</td>
      <td style="text-align:left">SetOperatorEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Where one or more parameter is a group containing multiple elements, (GROUP
          OF xxx), set operator for distinguishing between whole set and item interpretation
          of elements which are sets of elements</p>
        <p><em>I.e. only to be used in relation to GroupOf&#x2026; parameters,</em>  <em><b>not</b></em>  <em>to evaluate combinations of singular parameters</em>
        </p>
        <p>Allowed values:</p>
        <ul>
          <li>oneOfAnyOneSet
            <br />(only one item from all referenced GROUPs OF ENTITies of a given type
            may be selected/has been selected)</li>
          <li>oneOfEachSet
            <br />(one item from each specified referenced GROUP OF ENTITies of a given
            type shall be selected/has been selected)</li>
          <li>someOfAnySet
            <br />(multiple items from any referenced GROUP OF ENTITies of a given type
            may be selected/have been selected)</li>
          <li>allOfOneSet
            <br />(all items from one specified referenced GROUP OF ENTITies of a given
            type may be selected/have been selected)</li>
          <li>allOfAllSets
            <br />(all items from all referenced GROUPs OF ENTITies of a given type may
            be selected/have been selected)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">temporalValidityParameters</td>
      <td style="text-align:left">
        <p>TemporalValidityParameter</p>
        <p><em>Not yet defined allowed <b>validity parameters</b></em>
        </p>
        <p><em>See proposal (</em><a href="https://enturas.atlassian.net/wiki/spaces/AR/pages/585105589"><em>TEMPORARY - Unused NeTEx Fares (Fare and SalesTransaction frames) data objects</em></a><em>) and NeTEx part 3 part &quot;7.6.1.2 Validity Parameters&quot; (page 200-&gt;)</em>
        </p>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">Temporal validity parameters for the assignment (e.g. <a href="handbok-n801-siri-netex-fares.md#fares-OperatingDay">OperatingDay</a>)</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">validityParameters</td>
      <td style="text-align:left">
        <p>ValidityParameter</p>
        <p><em>Not yet defined allowed <b>validity parameters</b></em>
        </p>
        <p><em>See proposal (</em><a href="https://enturas.atlassian.net/wiki/spaces/AR/pages/585105589"><em>TEMPORARY - Unused NeTEx Fares (Fare and SalesTransaction frames) data objects</em></a><em>) and NeTEx part 3 part &quot;7.6.1.2 Validity Parameters&quot; (page 200-&gt;)</em>
        </p>
      </td>
      <td style="text-align:left">1: *</td>
      <td style="text-align:left">Validity parameters for the assignment (e.g. <a href>ServiceFacilities</a>)</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">TimeIntervalRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-TimeIntervalRef">TimeIntervalRef</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">References to TIME INTERVALS pertaining to FARE STRUCTURE ELEMENT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">GeographicalIntervalRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-GeographicalIntervalRef">GeographicalIntervalRef</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">References to GEOGRAPHICAL INTERVALS pertaining to FARE STRUCTURE ELEMENT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">QualityStructureFactorRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-QualityStructureFactorRef">QualityStructureFactorRef</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">References to QUALITY STRUCTURE FACTORs pertaining to FARE STRUCTURE ELEMENT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IncludesGroupingType</td>
      <td style="text-align:left">BooleanOperatorEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Logical operator for combining included elements, i.e. nesting of GenericParameterAssignment.
          The default is &#x2018;OR&#x2019;.</p>
        <p>Allowed values:</p>
        <ul>
          <li>OR (<em>default, i.e. interpreted as such if not stated</em>) =
            <br />Successive elements are logically ORed together; comparison must satisfy
            at least one specified value</li>
          <li>AND =
            <br />Successive elements are logically ANDed together; comparison must satisfy
            all specified values</li>
          <li>NOT =
            <br />Specified elements <b>must</b> be different from the given value</li>
          <li>XOR =
            <br />Successive elements are logically ORed together; comparison must satisfy <b>only one</b> of
            the specified values</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">includes</td>
      <td style="text-align:left">GenericParameterAssignmentInContext</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">A list of VALIDITY PARAMETER ASSIGNMENT <em>without ID constraing used only in the given context</em> specifying
        practical parameters during a TRAVEL GenericATION, within a given fare
        structure (e.g. the origin or destination zone in a zone-counting system)</td>
    </tr>
  </tbody>
</table>

#### ValidableElement <a id="fares-ValidableElement"></a>

A sequence or set of FARE STRUCTURE ELEMENTs, grouped together to be **validated** in one go.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| ValidableElement &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | fareStructureElements | [FareStructureElement](handbok-n801-siri-netex-fares.md#fares-FareStructureElementRef) | 1: \* | FARE STRUCTURE ELEMENTs making up VALIDABLE ELEMENT. |
| element | prices | [FareStructureElementPriceRef](handbok-n801-siri-netex-fares.md#fares-FareStructureElementPrice) | 0: \* | A set of all possible price features of a FARE STRUCTURE ELEMENT: default total price, discount in value or percentage etc. |

### Usage Parameters <a id="fares-UsageParameters"></a>

#### UsageParameter <a id="fares-UsageParameter"></a>

Abstract parameter type specifying the use of a SALES OFFER PACKAGE or a FARE PRODUCT.

[See definition in General information](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=Generell%20informasjon%20NeTEx&linkCreation=true&fromPageId=1638137934)

| UsageParameter &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | prices | UsageParameterPriceRef | 0: \* | Prices associated with USAGE PARAMETER |

#### UserProfile <a id="fares-UserProfile"></a>

The social profile of a passenger, based on age group, education, profession, social status, sex etc., often used for allowing discounts: 18-40 years old, graduates, drivers, unemployed, women etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">UserProfile &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>TypeOfConcessionRef</del>
      </td>
      <td style="text-align:left"><del>TypeOfConcessionRef</del>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left">
        <p><del>Classification by type of concession (eligibility for discount)</del>
        </p>
        <p><em>TypeOfConcession defineres som et ValueSet (i ResourceFrame) for &#xE5; gruppere/kategorisere passasjerer som kvalifiserer til rabatt, men datatypen inneholder i praksis kun fritekst-beskrivelser og er lite egnet for kategorisering. Gir upresis klassifisering av data og anbefales derfor ikke &#xE5; bruke.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">UserType</td>
      <td style="text-align:left">UserTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>User types</p>
        <p>Allowed values:</p>
        <ul>
          <li>adult (normally equal to &quot;anyone&quot;)</li>
          <li>animal</li>
          <li>anyone (normally equal to &quot;adult&quot;)</li>
          <li>child</li>
          <li>disabled</li>
          <li>disabledCompanion</li>
          <li>employee</li>
          <li>infant</li>
          <li><del>jobSeeker</del>
          </li>
          <li>military</li>
          <li>schoolPupil</li>
          <li>senior</li>
          <li>student</li>
          <li><del>youngPerson</del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MinimumAge</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Minimum age to be eligible for profile</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumAge</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum age to be eligible for profile</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ProofRequired</td>
      <td style="text-align:left">ProofOfIdentityEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of proof required</p>
        <p>Allowed values:</p>
        <ul>
          <li>noneRequired</li>
          <li>creditCard</li>
          <li>passport</li>
          <li>drivingLicence</li>
          <li>membershipCard</li>
          <li>identityDocument</li>
          <li>medicalDocument</li>
          <li>studentCard</li>
          <li>letterWIthAddress</li>
          <li><del>measurement</del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DiscountBasis</td>
      <td style="text-align:left">DiscountBasisEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Discount for this profile.</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>free</li>
          <li>discount</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">CompanionProfileRef</td>
      <td style="text-align:left">CompanionProfileRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">COMPANION PROFILEs describing users who may travel with user</td>
    </tr>
  </tbody>
</table>

#### UsageValidityPeriod <a id="fares-UsageValidityPeriod"></a>

A time limitation for validity of a FARE PRODUCT or a SALES OFFER PACKAGE. It may be composed of a standard duration \(e.g. 3 days, 1 month\) and/or fixed start/end dates and times.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">UsageValidityPeriod &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">
        <p><del>UsageValidityType</del>
          <br /><del>ValidityType</del>
        </p>
        <p>ValidityPeriodType</p>
      </td>
      <td style="text-align:left">UsageValidity<b>Type</b>Enumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of usage validity Period</p>
        <p>Allowed values (<em>NB: XSD does</em>  <em><b>not</b></em>  <em>match spec, hence this list complies to XSD</em>):</p>
        <ul>
          <li>singleRide</li>
          <li>singleTrip</li>
          <li>returnTrip</li>
          <li>carnet (<em>a fixed number of individual trips</em>)</li>
          <li>dayPass</li>
          <li>weeklyPass</li>
          <li>weekendPass</li>
          <li>monthlyPass</li>
          <li>annualPass</li>
          <li>seasonTicket</li>
          <li>profileMembership</li>
          <li>openEnded</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">UsageTrigger</td>
      <td style="text-align:left">UsageTriggerEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Trigger event that starts validity period</p>
        <p>Allowed values:</p>
        <ul>
          <li>startOfPeriod</li>
          <li>startOutboundRide</li>
          <li>endOutboundRide</li>
          <li>startReturnRide</li>
          <li>purchase</li>
          <li>specifiedStartDate</li>
          <li>fulfilment</li>
          <li>dayOffsetBeforeCalendarPeriod</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">UsageEnd</td>
      <td style="text-align:left">UsageEndEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of when the end of the Usage validity period occurs. May
          be a specified period (Standard Duration) or an event, e.g. end of trip</p>
        <p>Allowed values:</p>
        <ul>
          <li>standardDuration</li>
          <li>endOfCalendarPeriod</li>
          <li>endOfRide</li>
          <li>endOfTrip</li>
          <li>endOfFareDay</li>
          <li>endOfFarePeriod</li>
          <li>productExpiry</li>
          <li>profileExpiry</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">StandardDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration of VALIDITY PERIOD after departure. or validation</td>
    </tr>
  </tbody>
</table>

#### Suspending <a id="fares-Suspending"></a>

Conditions governing temporary suspension of a FARE PRODUCT, \(i.e. period pass or subscription\).

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Suspending &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SuspensionPolicy</td>
      <td style="text-align:left">SuspensionPolicyListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Policies for suspending term of product</p>
        <p>Allowed values (<em>multiple can be used simultaneously</em>):</p>
        <ul>
          <li>forCertifiedIllness</li>
          <li>forParentalLeave</li>
          <li>forHoliday</li>
          <li>forAnyReason</li>
          <li><em>necessary to add further?</em>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">QualificationPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Minimum duration that shall have occurred before a suspension is allowed</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MinimumSuspensionPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Minimum duration allowed for a suspension</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumSuspensionPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum duration allowed for a suspension</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumNumberOfSuspensionsPerTerm</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum number of suspensions for the related term</td>
    </tr>
  </tbody>
</table>

#### RoundTrip <a id="fares-RoundTrip"></a>

Properties relating to single or return trip use of an access right.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">RoundTrip &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">TripType</td>
      <td style="text-align:left">RoundTripTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of trip</p>
        <p>Allowed values:</p>
        <ul>
          <li>single (default)</li>
          <li>return (<em>outbound and return</em>)</li>
          <li>returnOut (<em>outbond part</em>)</li>
          <li>returnBack (<em>return part</em>)</li>
          <li>multiple</li>
          <li><del>returnOnly</del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DoubleSingleFare</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether fare for return trip is simply double the single fare</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IsRequired</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether return trip is required</td>
    </tr>
  </tbody>
</table>

#### FrequencyOfUse <a id="fares-FrequencyOfUse"></a>

The limits of usage frequency for a FARE PRODUCT \(or one of its components\) or a SALES OFFER PACKAGE during a specific VALIDITY PERIOD. There may be different tariffs depending on how often the right is consumed during the period.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FrequencyOfUse &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">FrequencyOfUseType</td>
      <td style="text-align:left">FrequencyOfUseTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of Frequency of Use</p>
        <p>Allowed values:</p>
        <ul>
          <li>single (default)</li>
          <li>none (<em>i.e. no interchange allowed</em>)</li>
          <li>limited</li>
          <li>unlimited</li>
          <li>twiceADay</li>
          <li><del>twiceADay</del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MinimalFrequency</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximalFrequency</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration of VALIDITY PERIOD after departure. or validation</td>
    </tr>
  </tbody>
</table>

#### Interchanging <a id="fares-Interchanging"></a>

Limitations on making changes within a trip.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| Interchanging &lt; [UsageParameter](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | CanInterchange | xsd:boolean | 0: 1 | Whether an interchange can be made |
| element | CanBreakJourney | xsd:boolean | 0: 1 | Whether the journey can be broken at an interchange point |

#### LuggageAllowance <a id="fares-LuggageAllowance"></a>

Period in which the product can be purchased.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">LuggageAllowance &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">BaggageUseType</td>
      <td style="text-align:left">BaggageUseTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of Baggage use</p>
        <p>Allowed values:</p>
        <ul>
          <li>carryOn</li>
          <li>checkIn</li>
          <li>oversizeCheckIn</li>
          <li>baggageCompartment</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">BaggageType</td>
      <td style="text-align:left">BaggageTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of Baggage described by allowance</p>
        <p>Allowed values:</p>
        <ul>
          <li>animal</li>
          <li>bicycle</li>
          <li>game</li>
          <li>handbag</li>
          <li>handLuggage</li>
          <li>largeMotorizedWheelchair</li>
          <li>motorcycle</li>
          <li>motorizedWheelchair</li>
          <li>musicalnstrument</li>
          <li>oversizeItem</li>
          <li>pushChair</li>
          <li>skis</li>
          <li>smallAnimal</li>
          <li>smallSuitcase</li>
          <li>sportingEquipment</li>
          <li>suitcase</li>
          <li>trunk</li>
          <li>wheelchair</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">LuggageAllowanceType</td>
      <td style="text-align:left">LuggageAllowanceTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of allowance type</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>limited</li>
          <li>singleBag</li>
          <li>unlimited</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumNumberItems</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Number of items allowed for this allowance</td>
    </tr>
    <tr>
      <td style="text-align:left">element (x4, possibly)</td>
      <td style="text-align:left">
        <p><em>Relevant to add?</em>
        </p>
        <ul>
          <li><em>MaximumBagHeight</em>
          </li>
          <li><em>MaximumBagWidth</em>
          </li>
          <li><em>MaximumBagDepth</em>
          </li>
          <li><em>MaximumBagWeight</em>
          </li>
        </ul>
      </td>
      <td style="text-align:left">type</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum bag ...</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">TotalWeight</td>
      <td style="text-align:left">xsd:decimal</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Total maximum weight limit (in kilograms) for this allowance</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">LuggageChargingBasis</td>
      <td style="text-align:left">LuggageChargingBasisEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Basis on which luggage is charged</p>
        <p>Allowed values:</p>
        <ul>
          <li>free</li>
          <li>chargedByItem (<em>per colli</em>)</li>
          <li>chargedByWeight (<em>total weight</em>)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### PurchaseWindow <a id="fares-PurchaseWindow"></a>

Period in which the product can be purchased.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">PurchaseWindow &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PurchaseAction</td>
      <td style="text-align:left">PurchaseActionEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Action governed by Purchase Window</p>
        <p>Allowed values:</p>
        <ul>
          <li>purchase (default)</li>
          <li>reserve</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PurchaseWhen</td>
      <td style="text-align:left">PurchaseWhenEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>When purchase may be made</p>
        <p>Allowed values:</p>
        <ul>
          <li>advanceAndDayOfTravel (default)</li>
          <li>advanceOnly</li>
          <li>dayOfTravelOnly</li>
          <li>timeOfTravelOnly</li>
          <li>untilPreviousDay</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">LatestTime</td>
      <td style="text-align:left">xsd:time</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Latest time on specified last day when ticket can be purchased</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MinimumPeriodBeforeDeparture</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Minimum duration before departure that ticket may be purchased</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumPeriodBeforeDeparture</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum duration before departure that ticket may be purchased</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PurchaseMoment</td>
      <td style="text-align:left">PurchaseMomentListOfEnumerations</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Permitted moments of purchase</p>
        <p>Allowed values (<em>multiple can be used simultaneously</em>):</p>
        <ul>
          <li>inAdvance</li>
          <li>beforeBoarding</li>
          <li>afterBoarding</li>
          <li>onCheckIn</li>
          <li>onReservation</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Reserving <a id="fares-Reserving"></a>

Indicating whether the access right requires reservation and any limitations on making and changing reservations.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| Reserving &lt; [UsageParameter](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | BookingArrangements | [BookingArrangementsStructure](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=network&linkCreation=true&fromPageId=1638137934) | 0: 1 | Booking Arrangements for cancellations |
| _See NeTEx part 3 chapter 7.6.1.3.9.2 Reserving – Model Element / Table 189 – Reserving – Element if further elements e.g. related to reservation fees are relevant_ |  |  |  |  |

#### Cancelling <a id="fares-Cancelling"></a>

Requirements for cancelling a booking.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| Cancelling &lt; [UsageParameter](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | BookingArrangements | [BookingArrangementsStructure](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=network&linkCreation=true&fromPageId=1638137934) | 0: 1 | Booking Arrangements for cancellations |

#### ChargingPolicy  <a id="fares-ChargingPolicy"></a>

Policy regarding different aspects of charging such as credit limits.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">ChargingPolicy &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">CreditPolicy</td>
      <td style="text-align:left">TravelCreditPolicyEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Policy for traveling on credit</p>
        <p>Allowed values:</p>
        <ul>
          <li>allowTravel</li>
          <li>blockPayAsYouGoTravel</li>
          <li>blockAllTravel</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">BillingPolicy</td>
      <td style="text-align:left">TravelBillingPolicyEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Policy for billing frequency</p>
        <p>Allowed values:</p>
        <ul>
          <li>billAsYouGo</li>
          <li>billOnThreshold</li>
          <li>billAtFareDayEnd</li>
          <li>billAtPeriodEnd</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### PenaltyPolicy  <a id="fares-PenaltyPolicy"></a>

Policy regarding different aspects of penalty charges, for example repeated entry at the same station, no ticket etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">PenaltyPolicy &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PenaltyPolicyType</td>
      <td style="text-align:left">PenaltyPolicyTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of Penalty Policy</p>
        <p>Allowed values:</p>
        <ul>
          <li>noTicket</li>
          <li>noValidation</li>
          <li><del>noCheckin</del>
          </li>
          <li><del>noCheckout</del>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">
        <p>PenaltyAction</p>
        <p><em>(forslag til NeTEx utvidelse)</em>
        </p>
      </td>
      <td style="text-align:left">
        <p>PenaltyActionEnumeration</p>
        <p><em>(forslag til NeTEx utvidelse, dvs inkl ny enumeration)</em>
        </p>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Classification of Penalty Action</p>
        <p>Allowed values:</p>
        <ul>
          <li>fine</li>
          <li>...??? <em>(m&#xE5; revideres)</em>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">
        <p>PaymentMethod</p>
        <p><em>(forslag til NeTEx utvidelse, b&#xF8;r implementeres som liste slik at det fungerer &#xE5; legge inn flere betalingsalternativer per policy)</em>
        </p>
      </td>
      <td style="text-align:left">PaymentMethodListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Available penalty payment methods</p>
        <p>Allowed values (<em>forl&#xF8;pig listet opp alle som eksisterer for objektet</em>):</p>
        <ul>
          <li><del>cash</del>
          </li>
          <li><del>cashAndCard</del>
          </li>
          <li><del>coin</del>
          </li>
          <li><del>banknote</del>
          </li>
          <li><del>cheque</del>
          </li>
          <li><del>travellersCheque</del>
          </li>
          <li><del>postalOrder</del>
          </li>
          <li><del>companyCheque</del>
          </li>
          <li>creditCard</li>
          <li>debitCard</li>
          <li>cardsOnly</li>
          <li>travelCard</li>
          <li><del>contactlessPaymentCard</del>
          </li>
          <li><del>contactlessTravelCard</del>
          </li>
          <li><del>directDebit</del>
          </li>
          <li>bankTransfer</li>
          <li>sms</li>
          <li>mobilePhone</li>
          <li>voucher</li>
          <li><del>token</del>
          </li>
          <li><del>warrant</del>
          </li>
          <li><del>mileagePoints</del>
          </li>
          <li>...??? <em>(m&#xE5; revideres)</em>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Subscribing  <a id="fares-Subscribing"></a>

Parameters governing subscription to a product allowing payment at regular intervals.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Subscribing &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SubscriptionTermType</td>
      <td style="text-align:left">SubscriptionTermTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Types of subscription term allowed</p>
        <p>Allowed values:</p>
        <ul>
          <li>fixed</li>
          <li>openEnded</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MinimumSubscriptionPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Minimum duration allowed for a subscription</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumSubscriptionPeriod</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum duration allowed for a subscription</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SubscriptionRenewalPolicy</td>
      <td style="text-align:left">SubscriptionRenewalPolicyEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Policy on renewing subscription</p>
        <p>Allowed values:</p>
        <ul>
          <li>automatic</li>
          <li>manual</li>
          <li>none (<em>for termination of subscription type</em>)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">possibleInstallmentIntervals</td>
      <td style="text-align:left">TimeIntervalRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Allowed billing Intervals for payment in instalment</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">InstallmentPaymentMethods</td>
      <td style="text-align:left">PaymentMethodListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Allowed means of payment of installations as standard value</p>
        <p>Allowed values (<em>multiple can be used simultaneously</em>):</p>
        <ul>
          <li>bankTransfer</li>
          <li>creditCard</li>
          <li>debitCard</li>
          <li>travelCard</li>
          <li>sms</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### GroupTicket <a id="fares-GroupTicket"></a>

The number and characteristics of persons entitled to travel in addition to the holder of an access right.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">GroupTicket &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MinimumNumberOfPersons</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Minimum number of persons overall allowed on ticket</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumNumberOfPersons</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum number of persons overall allowed on ticket</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">companionProfiles</td>
      <td style="text-align:left">CompanionProfileRef</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">The number and characteristics of a category of users allowed on the ticket</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PricingBasis</td>
      <td style="text-align:left">PricingBasisEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Discount for this profile.</p>
        <p>Allowed values:</p>
        <ul>
          <li>perOffer</li>
          <li>perPerson</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">JointCheckIn</td>
      <td style="text-align:left">GroupCheckInEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Whether the group must check in together</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>required</li>
          <li>allowed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">GroupBookingFacility</td>
      <td style="text-align:left">GroupBookingEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of GROUP FACILITY type (TPEG pti23)</p>
        <p>Allowed values:</p>
        <ul>
          <li>groupsAllowed</li>
          <li>groupsNotAllowed</li>
          <li>groupsAllowedWithReservation</li>
          <li>groupBookingsRestricted</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### CompanionProfile <a id="fares-CompanionProfile"></a>

The COMPANION PROFILE specifies the number and characteristics of persons entitled to travel in addition to the holder of an access right, for example children, wheelchair carer, etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">CompanionProfile &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">CompanionRelationshipType</td>
      <td style="text-align:left">CompanionRelationshipEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Required Relationship of companion to eligible user</p>
        <p>Allowed values:</p>
        <ul>
          <li>anyone</li>
          <li>carer</li>
          <li>child</li>
          <li>dependent</li>
          <li>family</li>
          <li>partner</li>
          <li>teacher</li>
          <li>pupil</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MinimumNumberOfPersons</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Minimum number of persons overall allowed of this type</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumNumberOfPersons</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Maximum number of persons overall allowed of this type</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DiscountBasis</td>
      <td style="text-align:left">DiscountBasisEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Nature of discount for this type of user</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>free</li>
          <li>discount</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### CommercialProfile <a id="fares-CommercialProfile"></a>

A category of users depending on their commercial relations with the operator \(frequency of use, amount of purchase etc.\), often used for allowing discounts.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| CommercialProfile &lt; [UsageParameter](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| CommercialProfile inherits from [UsageParameter](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter) without introducing new elements or attributes. |  |  |  |  |

#### Transferability <a id="fares-Transferability"></a>

The number and characteristics of persons entitled to use the public transport service instead of the original customer.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Transferability &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">CanTransfer</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether ticket can be transferred to someone else</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MaximumNumberOfNamedTransferees</td>
      <td style="text-align:left">xsd:nonNegativeInteger</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Where a product can be used by a limited number of named users, maximum
        number of users allowed.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">HasTransferFee</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether there is a fee for a refund or exchange</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SharedUsage</td>
      <td style="text-align:left">ResellWhenEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Indicates the nature of the permitted sharing, if any, of products that
          can be shared, e.g. Trips from a multi-trip carnet</p>
        <p>Allowed values:</p>
        <ul>
          <li>singleUser</li>
          <li>concurrentUsers (<em>multiple users at the same time</em>)</li>
          <li>concurrentDesignatedUsers (<em>multiple users at the same time, but only designated companions</em>)</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Reselling <a id="fares-Reselling"></a>

Common resale conditions \(i.e. for exchange or refund\) attaching to the product.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Reselling &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Allowed</td>
      <td style="text-align:left">ResellTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Whether exchange or refund is allowed</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>partial</li>
          <li>full</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">UnusedTicketsOnly</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether it is possible to exchange partially used tickets</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">HasFee</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether there is a fee for a refund or exchange</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExchangeableFromDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration to start of period before (negative) or after (positive) the
        trigger point (i.e. either Start Of Validity or First Use) or that ticket
        may be exchanged or refunded</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExchangeableUntilDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration to end of period before (negative) or after (positive) the trigger
        point (i.e. either Start Of Validity or First Use) that ticket may be exchanged
        or refunded</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ResellWhen</td>
      <td style="text-align:left">ResellWhenEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Event marking when the exchangeable status of the ticket changes</p>
        <p>Allowed values (<em>NB: XSD does</em>  <em><b>not</b></em>  <em>match spec, hence this list complies to XSD</em>):</p>
        <ul>
          <li>never</li>
          <li>beforeFirstUse</li>
          <li>afterFirstUse</li>
          <li>beforeStartOfValidity</li>
          <li>afterStartOfValidity</li>
          <li>afterEndOfValidity</li>
          <li>beforeValidation</li>
          <li>afterValidation</li>
          <li>anyTime</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Refunding <a id="fares-Refunding"></a>

Whether and how the product may be refunded.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Refunding &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares+work+in+progress#Reselling">Reselling</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
            <a
            href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Allowed</td>
      <td style="text-align:left">ResellTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Whether exchange or refund is allowed</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>partial</li>
          <li>full</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">CanChangeClass</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether user can change class</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">UnusedTicketsOnly</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether it is possible to exchange partially used tickets</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ResellWhen</td>
      <td style="text-align:left">ResellWhenEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Event marking when the is exchangable status of the ticket changes</p>
        <p>Allowed values:</p>
        <ul>
          <li>never</li>
          <li>beforeStartOfValidity</li>
          <li>afterStartOfValidity</li>
          <li>afterEndOfValidity</li>
          <li>beforeFirstUse</li>
          <li>afterFirstUse</li>
          <li>beforeValidation</li>
          <li>afterValidation</li>
          <li>anyTime</li>
          <li>afterSale (tillegg)</li>
        </ul>
        <p><em>M&#xE5; revideres - NB: &quot;afterSale&quot; finnes (forel&#xF8;pig) ikke i enum&apos;en</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExchangableFromDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration to start of period before (negative) or after (positive) the
        trigger point (i.e. either Start of Validity or First Use ) or that ticket</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExchangableUntilDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration to end of period before (negative) or after (positive) the trigger
        point (i.e. either Start of Validity or First Use ) or that ticket</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">HasFee</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether there is a feed for reselling</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RefundBasis</td>
      <td style="text-align:left">PerBasisEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Basis for which refund is given</p>
        <p>AllowedValues:</p>
        <ul>
          <li>perOffer</li>
          <li>perPerson</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RefundType</td>
      <td style="text-align:left">RefundTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of Refund</p>
        <p>Allowed values:</p>
        <ul>
          <li>unused</li>
          <li>delay</li>
          <li>cancellation</li>
          <li>partialJourney</li>
        </ul>
        <p><em>NB: Kun mulig &#xE5; angi &#xE9;n (mulig workaround &#xE5; definere redundante Refund-objekter)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PaymentMethod</td>
      <td style="text-align:left">PaymentMethodListOfEnumerations</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Payment methods allowed to make refund</p>
        <p>Allowed values:</p>
        <ul>
          <li>cash</li>
          <li>cashAndCard</li>
          <li>coin</li>
          <li>banknote</li>
          <li>cheque</li>
          <li>travellersCheque</li>
          <li>postalOrder</li>
          <li>companyCheque</li>
          <li>creditCard</li>
          <li>debitCard</li>
          <li>cardsOnly</li>
          <li>travelCard</li>
          <li>contactlessPaymentCard</li>
          <li>contactlessTravelCard</li>
          <li>sms</li>
          <li>mobilePhone</li>
          <li>voucher</li>
          <li>token</li>
          <li>warrant</li>
        </ul>
        <p><em>M&#xE5; revideres! NB: Kun mulig &#xE5; angi &#xE9;n (noen dekker riktignok flere case... mulig workaround &#xE5; definere redundante Refund-objekter)</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### Exchanging <a id="fares-Exchanging"></a>

Whether and how access rights may be exchanged for other access rights.

Example can be found in the [official GitHub-repository for Ent](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Exchanging &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares+work+in+progress#Reselling">Reselling</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
            <a
            href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Allowed</td>
      <td style="text-align:left">ResellTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Whether exchange or refund is allowed</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>partial</li>
          <li>full</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">UnusedTicketsOnly</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether it is possible to exchange partially used tickets</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">HasFee</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether there is a fee for a refund or exchange</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExchangeableFromDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration to start of period before (negative) or after (positive) the
        trigger point (i.e. either Start Of Validity or First Use) or that ticket
        may be exchanged or refunded</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExchangeableUntilDuration</td>
      <td style="text-align:left">xsd:duration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Duration to end of period before (negative) or after (positive) the trigger
        point (i.e. either Start Of Validity or First Use) that ticket may be exchanged
        or refunded</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ResellWhen</td>
      <td style="text-align:left">ResellWhenEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Event marking when the exchangeable status of the ticket changes</p>
        <p>Allowed values (<em>NB: XSD does</em>  <em><b>not</b></em>  <em>match spec, hence this list complies to XSD</em>):</p>
        <ul>
          <li>never</li>
          <li>beforeFirstUse</li>
          <li>afterFirstUse</li>
          <li>beforeStartOfValidity</li>
          <li>afterStartOfValidity</li>
          <li>afterEndOfValidity</li>
          <li>beforeValidation</li>
          <li>afterValidation</li>
          <li>anyTime</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">NumberOfExchangesAllowed</td>
      <td style="text-align:left">xsd:integer</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether it is possible to exchange partially used tickets</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ToFareClass</td>
      <td style="text-align:left">FareClassEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Fare class to which can be exchanged.</p>
        <p>Allowed values:</p>
        <ul>
          <li>any</li>
          <li>businessClass</li>
          <li>economyClass</li>
          <li>firstClass</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ExchangeableTo</td>
      <td style="text-align:left">ExchangableToEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of exchange allowed. <em>The default is &#x2018;anyProduct&#x2019;, i.e. to any other fare.</em>
        </p>
        <p>Allowed values:</p>
        <ul>
          <li>anyProduct</li>
          <li>sameProductSameDay</li>
          <li>sameProductAnyDay</li>
          <li>upgradeToStandardFare</li>
          <li>upgradeToSpecifiedFare</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### Replacing <a id="fares-Replacing"></a>

Whether and how access rights may be replaced if lost or stolen.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Replacing &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares+work+in+progress#Reselling">Reselling</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#UsageParameter">UsageParameter</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
            <a
            href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Allowed</td>
      <td style="text-align:left">ResellTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Whether exchange or refund is allowed</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>partial</li>
          <li>full</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">UnusedTicketsOnly</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether it is possible to exchange partially used tickets</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">HasFee</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether there is a fee for a refund or exchange</td>
    </tr>
  </tbody>
</table>

### Fare Product <a id="fares-FareProduct"></a>

#### ServiceAccessRight <a id="fares-ServiceAccessRight"></a>

Abstract type describing an immaterial marketable element \(access rights, discount rights etc\).

[See definition in General information](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=Generell+informasjon+NeTEx&linkCreation=true&fromPageId=916554300)

| ServiceAccessRight &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Type | Cardinality | Description |
| element | PrivateCode | xsd:normalizedString | 0: 1 | Identifier of SERVICE ACCESS RIGHT |
| element | InfoUrl | xsd:anyURI | 0: 1 | Link for product information |

#### FareProduct <a id="fares-FareProduct.1"></a>

Abstract type describing an immaterial marketable element \(access rights, discount rights etc\), specific to a CHARGING MOMENT.

[See definition in General information](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=Generell+informasjon+NeTEx&linkCreation=true&fromPageId=916554300)

| FareProduct &lt; [ServiceAccessRight](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#ServiceAccessRight) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Type | Cardinality | Description |
| element | ChargingMomentRef | FareProductRef | 0: 1 | Reference to a CHARGING MOMENT for product |
| ~~element~~ | ~~TypeOfFareProductRef~~ | ~~TypeOfFareProductRef~~ | ~~0: 1~~ | ~~Reference to a type of FARE PRODUCT~~ |
| element | ConditionSummary | [ConditionSummary](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#DEPRECATED-faresdataobjects-ConditionSummary) | 0: 1 | Summary description of conditions on FARE PRODUCT |
| element | OperatorRef | OperatorRef | 0: 1 | Reference to OPERATOR to which ACCESS RIGHT PARAMETER is assigned |
| element | FareProductRef | FareProductRef | 0: 1 | Another FARE PRODUCT which this product extends. Will assume all properties of base product unless specifically overridden. |
| element | validityParameterAssignments | [ValidityParameterAssignment](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#DEPRECATED-faresdataobjects-ValidityParameterAssignment) | 0: 1 | Type for a list of VALIDITY PARAMETER ASSIGNMENT. |
|  | _se_ _**ValidityParameterAssignment**_ _\(må ta stilling til om objektene i denne også skal være internt i objektet, eller kun wrappet\)_ |  |  |  |

#### PreassignedFareProduct <a id="fares-PreassignedFareProduct"></a>

A FARE PRODUCT consisting of one or several VALIDABLE ELEMENTs, specific to a CHARGING MOMENT.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| PreassignedFareProduct &lt; [FareProduct](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#FareProduct) &lt; [ServiceAccessRight](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#ServiceAccessRight) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | SupplementProductRef | [SupplementProductRef](handbok-n801-siri-netex-fares.md#fares-SupplementProduct) | 1: 1 | Reference to a SUPPLEMENT PRODUCT |
| element | accessRightsInProduct | [AccessRightInProduct](handbok-n801-siri-netex-fares.md#fares-AccessRightInProduct) | 0: \* | List ACCESS RIGHT IN PRODUCT for this FARE PRODUCT |
| element | prices | [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) | 0: \* | PRICEs for this FARE PRODUCT |

#### AccessRightInProduct <a id="fares-AccessRightInProduct"></a>

A VALIDABLE ELEMENT as a part of a PRE-ASSIGNED FARE PRODUCT, including its possible order in the set of all VALIDABLE ELEMENTs grouped together to define the access right assigned to that PREASSIGNED FARE PRODUCT.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">AccessRightInProduct &lt; FareElementInSequence &lt; VersionedChild &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ValidableElementRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-ValidableElementRef">ValidableElementRef</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to a VALIDABLE ELEMENT for which access rights are specified</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SupplementProductRef</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-SupplementProduct">SupplementProductRef</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Reference to a SUPPLEMENT PRODUCT</p>
        <p><em>Preferably not used as an AccessRight, but rather as a SUPPLEMENT PRODUCT to the FARE PRODUCT itself.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### SupplementProduct <a id="fares-SupplementProduct"></a>

An additional FARE PRODUCT that may be used to describe additional purchases entitled by another product. A SUPPLEMENT PRODUCT is usually constrained by some or all of the parameters of the supplemented product, e.g. same service, same route, etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">SupplementProduct &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#PreassignedFareProduct">PreassignedFareProduct</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#FareProduct">FareProduct</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#ServiceAccessRight">ServiceAccessRight</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
            <a
            href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PreassignedFareProductRef</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-PreassignedFareProduct">PreassignedFareProductRef</a>
      </td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Reference to base PRE ASSIGNED FARE PRODUCT OFFER for which this is a
          supplement</p>
        <p><em>G&#xE5;r kun an &#xE5; referere <b>ett</b></em>  <em>FareProduct (dvs enten <b>ett</b></em>  <em>SupplementaryProduct eller <b>en</b></em>  <em>SalesDiscountRight).</em>
        </p>
        <p> <em>Se FareProductRelationGroup (netex_fareProduct_version.xsd)</em>
        </p>
        <p><em>Det m&#xE5; ENTEN fikses, ellers m&#xE5; referansen g&#xE5; tilbake for akkurat dette datasettet. (Hvilket umuliggj&#xF8;r gjenbruk.)</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">SupplementProductType</td>
      <td style="text-align:left">SupplementProductEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Classification of SUPPLEMENT PRODUCT</p>
        <p>Allowed values:</p>
        <ul>
          <li>animal</li>
          <li>bicycle</li>
          <li>dog</li>
          <li>eventAddOn</li>
          <li>extraLuggage</li>
          <li>journeyAddOn</li>
          <li>journeyExtension</li>
          <li>meal</li>
          <li>parking</li>
          <li>penalty</li>
          <li>seatReservation</li>
          <li>upgrade</li>
          <li>wifi</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### ThirdPartyProduct <a id="fares-ThirdPartyProduct"></a>

A FARE PRODUCT that is marketed together with a Public Transport Fare Product.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| ThirdPartyProduct &lt; [FareProduct](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#FareProduct) &lt; [ServiceAccessRight](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#ServiceAccessRight) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | prices | [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) | 0: \* | Capping FARE PRICEs for this rule |
| _Må ta stilling til hva dette objektet skal inneholde_ | _name_ | _type_ | _0: x_ | _description_ |

#### SaleDiscountRight <a id="fares-SaleDiscountRight"></a>

A FARE PRODUCT allowing a customer to benefit from discounts when purchasing SALES OFFER PACKAGEs.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">SaleDiscountRight &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#FareProduct">FareProduct</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#ServiceAccessRight">ServiceAccessRight</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
            <a
            href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">ProductType</td>
      <td style="text-align:left">SaleDiscountRightEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>SaleDiscountRightEnumeration</p>
        <p>Allowed values:</p>
        <ul>
          <li>payAsYouGoRight</li>
          <li>statutoryRight (<em>per regulatory approval</em>)</li>
          <li>travelCard</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

**Under utarbeidelse \(uke 43-44\), avklare hvilke use-case som skal støttes i første leveranse**

#### CappedDiscountRight <a id="fares-CappedDiscountRight"></a>

A specialisation of SALE DISCOUNT RIGHT where the discount is expressed as a capping limit for a given  
time interval. For example, the London Oyster card fare, which charges for each journey at a reduced price until travel equivalent to a day pass has been consumed.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| CappedDiscountRight &lt; [SaleDiscountRight](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#SaleDiscountRight) &lt; [FareProduct](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#FareProduct) &lt; [ServiceAccessRight](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#ServiceAccessRight) &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | cappingRules | [CappingRule](handbok-n801-siri-netex-fares.md#fares-CappingRule) | 1: 1 | List of parameters setting a price cap on a product. |

#### CappingRule <a id="fares-CappingRule"></a>

A capping limit for a given time interval, where the capping is expressed by another product. For example, the London Oyster card fare, which charges for each journey at a reduced price until travel equivalent to a  
day pass for the mode of travel has been consumed. A CAPPING RULE is a PRICEABLE OBJECT and may have USAGE PARAMETERS such as a USAGE VALIDITY PERIOD to specify how long the capping period is and a CHARGING POLICY to specify rules about travelling under credit.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| CappingRule &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | prices | [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) | 0: \* | Capping FARE PRICEs for this rule |

### Pricing <a id="fares-Pricing"></a>

#### GeographicalUnitPrice <a id="fares-GeographicalUnitPrice"></a>

A unit for calculating geographical graduated fares

| GeographicalUnitPrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| GeographicalUnitPrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

#### GeographicalIntervalPrice <a id="fares-GeographicalIntervalPrice"></a>

A set of all possible price features of a QUALITY STRUCTURE FACTOR , e.g. default total price etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| GeographicalIntervalPrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| GeographicalIntervalPrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

#### FareStructureElementPrice <a id="fares-FareStructureElementPrice"></a>

A set of all possible price features of a FARE STRUCTURE ELEMENT: default total price, discount in value or percentage etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| FareStructureElementPrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| FareStructureElementPrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

#### UsageParameterPrice <a id="fares-UsageParameterPrice"></a>

A set of all possible price features of a USAGE PARAMETER: discount in value or percentage etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| UsageParameterPrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| UsageParameterPrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

#### FareProductPrice <a id="fares-FareProductPrice"></a>

A set of all possible price features of a FARE PRODUCT: default total price, discount in value or percentage etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| FareProductPrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| FareProductPrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

#### FulfilmentMethodPrice <a id="fares-FulfilmentMethodPrice"></a>

A set of all possible price features of a FULFILMENT METHOD, default total price etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| FulfilmentMethodPrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| FulfilmentMethodPrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

#### SalesOfferPackagePrice <a id="fares-SalesOfferPackagePrice"></a>

A set of all possible price features of a SALES OFFER PACKAGE: default total price etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| SalesOfferPackagePrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| SalesOfferPackagePrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

#### ~~PriceGroup~~ <a id="fares-PriceGroup"></a>

~~A grouping of prices, allowing the grouping of numerous possible consumption elements into a limited number of price references, or to apply grouped increases, in value or percentage.~~

~~Example can be found in the~~ [~~official GitHub-repository for Entur~~](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| ~~PriceGroup &lt;~~ [~~GroupOfEntities~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-GroupOfEntities) ~~&lt;~~ [~~DataManagedObject~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-DataManagedObject) ~~&lt;~~ [~~EntityInVersion~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) ~~&lt;~~ [~~Entity~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| ~~XML-type~~ | ~~Name~~ | ~~Datatype~~ | ~~Cardinality~~ | ~~Description~~ |
| ~~element~~ | ~~Amount~~ | ~~xsd:decimal~~ | ~~0: 1~~ | ~~Price in a specified currency~~ |
| ~~element~~ | ~~Currency~~ | ~~xsd:NMTOKEN \(_3 letters_\)~~ | ~~0: 1~~ | ~~ISO 4717 type currency code \(optimization to allow PRICE UNITs to be omitted\)~~ |
| ~~element~~ | ~~PricingRuleRef~~ | [~~PricingRuleRef~~](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-PricingRuleRef) | ~~0: 1~~ | ~~Reference to a PRICING RULE used in calculation step to derive price~~ |

#### FareTable <a id="fares-FareTable"></a>

A grouping of prices that may be associated with various combinations fare elements such as the DISTANCE MATRIX ELEMENT, FARE STRUCTURE ELEMENT, GEOGRAPHICAL INTERVAL, TIME INTERVAL, USAGE PARAMETER, etc.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| FareTable &lt; [_PriceGroup_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#PriceGroup) &lt; [GroupOfEntities](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-GroupOfEntities) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) _\(NB: Ikke implementert slik, i XSD arver FareTable direkte fra GroupOfEntities\)_ |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| ~~element~~ | ~~StartDate~~ | ~~xsd:date~~ | ~~0: 1~~ | ~~Start date for PRICE validity~~ |
| ~~element~~ | ~~EndDate~~ | ~~xsd:date~~ | ~~0: 1~~ | ~~End date for PRICE validity.~~ _Gyldighet bør heller angis med ValidityCondition for objektet_ |
| ~~element~~ | ~~RoundingRef~~ | ~~RoundingRef~~ | ~~0: 1~~ | ~~Reference to a ROUNDING to use on calculation~~ |
| element | pricesFor | [PriceableObjectRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-PriceableObject) | 0: \* | Combination of Elements for which this table provides PRICEs |
| \(choice\) element   | usedIn | TariffRef | 0: \* | Elements that use FARE TABLE that are not PRICEABLE OBJECTs |
| GroupOfDistanceMatrixElementsRef |  |  |  |  |
| GroupOfSalesOfferPackagesRef |  |  |  |  |
| element | OrganisationRef | [OrganisationRef](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=framework&linkCreation=true&fromPageId=1638137934) | 0: \* | Reference to a ORGANISATION for which this table applies |
| element | limitations | [UsageParameterRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-UsageParameterRef) | 0: \* | Usage parameters common to all cells in table |
| element | prices | [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) | 0: \* | Simple FARE PRICE cells \(optimised, without additional associations\) |

#### ~~Cell~~ <a id="fares-Cell"></a>

Foreløpig ikke anbefalt brukt, trolig bedre å angi priser og pristyper direkte \(så lenge det er dekkende\) fremfor å utveksle formatert / cellestrukturert tabell.

~~An unique individual combination of features within a FARE TABLE, used to associate a FARE PRICE with a fare element.~~

~~Example can be found in the~~ [~~official GitHub-repository for Entur~~](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| ~~Cell &lt; VersionedChild &lt;~~ [~~EntityInVersion~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) ~~&lt;~~ [~~Entity~~](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| ~~XML-type~~ | ~~Name~~ | ~~Datatype~~ | ~~Cardinality~~ | ~~Description~~ |
| ~~attribute~~ | ~~order~~ | ~~xsd:integer~~ | ~~1: 1~~ | ~~&gt;Order in which cell is to appear~~ |
| ~~element~~ | ~~FareStructureElementPriceRef~~ | [~~FareStructureElementPriceRef~~](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-FareStructureElementPrice) | ~~0: \*~~ | ~~Reference to a FARE STRUCTURE ELEMENT PRICE~~ |

### Ticketing <a id="fares-Ticketing"></a>

#### DistributionChannel <a id="fares-DistributionChannel"></a>

A type of outlet for selling a product.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">DistributionChannel &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">alternativeNames</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&amp;title=framework&amp;linkCreation=true&amp;fromPageId=1638137934">AlternativeName</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List for alternative name(s) for Distribution Channel</td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">DistributionChannelType</td>
      <td style="text-align:left">DistributionChannelTypeEnumeration</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">
        <p>Classification of DISTRIBUTION CHANNEL</p>
        <p>Allowed values:</p>
        <ul>
          <li>atStop</li>
          <li>onBoard</li>
          <li>online</li>
          <li>telephone</li>
          <li>electronicPass</li>
          <li>postal</li>
          <li>mobileDevice</li>
          <li>agency</li>
          <li>tourOperator</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">AllDistributionChannelsRef</td>
      <td style="text-align:left">AllDistributionChannelsRefStructureElement</td>
      <td style="text-align:left"><em>Always &quot;All&quot;</em>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IsObligatory</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether use of the channel is obligatory</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RequiresEmailAddress</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether use of the channel requries the pruchaser to have an email address</td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">ContactDetails</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&amp;title=framework&amp;linkCreation=true&amp;fromPageId=1638137934">ContactStructure</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Contact details for distribution channel</td>
    </tr>
    <tr>
      <td style="text-align:left">OrganisationRef</td>
      <td style="text-align:left">OrganisationRef</td>
      <td style="text-align:left">Reference to Organisation responsible for Distribution Channel</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PaymentMethods</td>
      <td style="text-align:left">PaymentMethodEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Available payment methods</p>
        <p>Allowed values:</p>
        <ul>
          <li>cash</li>
          <li>cashAndCard</li>
          <li>coin</li>
          <li>banknote</li>
          <li>cheque</li>
          <li>travellersCheque</li>
          <li>postalOrder</li>
          <li>companyCheque</li>
          <li>creditCard</li>
          <li>debitCard</li>
          <li>cardsOnly</li>
          <li>travelCard</li>
          <li>contactlessPaymentCard</li>
          <li>contactlessTravelCard</li>
          <li>sms</li>
          <li>mobilePhone</li>
          <li>voucher</li>
          <li>token</li>
          <li>warrant</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DistributionRights</td>
      <td style="text-align:left">DistributionRightsEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Channels DISTRIBUTION RIGHTs</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>sell</li>
          <li>exchange</li>
          <li>refund</li>
          <li>inform</li>
          <li>private</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">distributionPoints</td>
      <td style="text-align:left">PointRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">List of references to a POINT (e.g. for info on geolocation)</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>DistributionGroupRef</del>
      </td>
      <td style="text-align:left"><del>DistributionGroupRef</del>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left">
        <p><del>Prefined Group of specified points to which distribution is restricted, if any.</del>
        </p>
        <p><em>Guppering gj&#xF8;res gjennom GroupOfDistributionChannels, ikke motsatt vei.</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### GroupOfDistributionChannels <a id="fares-GroupOfDistributionChannels"></a>

Type for a collection of one or more references to a DISTRIBUTION CHANNEL.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| GroupOfDistributionChannels &lt; [GroupOfEntities](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-GroupOfEntities) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | members | DistributionChannelRefs | 1: 1 | List containing _minimum two or more_ DistributionChannelRef for group |

#### FulfilmentMethod <a id="fares-FulfilmentMethod"></a>

The means by which the ticket is delivered to the Customer.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FulfilmentMethod &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">FulfilmentMethodType</td>
      <td style="text-align:left">FulfilmentMethodTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Type of FULFILMENT METHOD</p>
        <p>Allowed values:</p>
        <ul>
          <li>ticketOffice</li>
          <li>ticketMachine</li>
          <li>conductor</li>
          <li>agent</li>
          <li>post</li>
          <li>selfprint</li>
          <li>sms</li>
          <li>email</li>
          <li>topUpDevice</li>
          <li>validator</li>
          <li>mobileApp</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RequiresCard</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether use of of the method requires a credit or debit card</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RequiresBookingReference</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether use of of the method requires a booking reference</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">typesOfTravelDocument</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-TypeOfTravelDocument">TypeOfTravelDocumentRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of TYPES OF TRAVEL DOCUMENT associated with method</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">canIssueTypesOfTravelDocument</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-TypeOfTravelDocument">TypeOfTravelDocumentRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of TYPES OF TRAVEL DOCUMENT that can be ISSUED with method</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">canReuseTypesOfTravelDocument</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-TypeOfTravelDocument">TypeOfTravelDocumentRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">TYPES OF TRAVEL DOCUMENT that can be REUSED with method</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">prices</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-FulfilmentMethodPrice">FulfilmentMethodPriceRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">Reference to a FULFILMENT METHOD PRICE</td>
    </tr>
  </tbody>
</table>

#### TypeOfTravelDocument <a id="fares-TypeOfTravelDocument"></a>

A classification of TRAVEL DOCUMENTs expressing their general function and local functional characteristics specific to the operator

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">TypeOfTravelDocument &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#TypeOfValue">TypeOfValue</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IsCard</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the TRAVEL DOCUMENT is materialised as a card</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">IsSmart</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the TRAVEL DOCUMENT is materialized on a smart card or mobile
        device</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">HasPhoto</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether the TRAVEL DOCUMENT has a photo</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MediaType</td>
      <td style="text-align:left">MediaTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of the TRAVEL DOCUMENT by Media Type</p>
        <p>Allowed values:</p>
        <ul>
          <li>paperTicket</li>
          <li>paperTicketWithCoupons</li>
          <li>coupon</li>
          <li>selfPrintPaperTicket</li>
          <li>smartCard</li>
          <li>mobileApp</li>
          <li>card</li>
          <li>mms</li>
          <li>sms</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MachineReadable</td>
      <td style="text-align:left">MachineReadableEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of the TRAVEL DOCUMENT by Machine Readable mechanism</p>
        <p>Allowed values:</p>
        <ul>
          <li>magneticStrip</li>
          <li>chip</li>
          <li>ocr</li>
          <li>barCode</li>
          <li><em>shotCode (NB: Only as temporary replacement for</em>  <em><b>QRcode</b>)</em>
          </li>
          <li><b>QRcode</b> (currently missing in NeTEx)</li>
          <li>nfc</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### SalesOfferPackage <a id="fares-SalesOfferPackage"></a>

A package to be sold as a whole, consisting of one or several FARE PRODUCTs materialised thanks to one or several TRAVEL DOCUMENTs. The FARE PRODUCTs may be either directly attached to the TRAVEL DOCUMENTs, or may be reloadable on the TRAVEL DOCUMENTs.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">SalesOfferPackage &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PrivateCode</td>
      <td style="text-align:left">PrivateCodeType</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Alternative identifier of an entity. can be used to associate with legacy
        systems.</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <img src="../.gitbook/assets/help_16.png" alt="(question)" /><em> Mer ryddig &#xE5; definere RoundingRef, prices, PrincingService(Ref), PricingRule(Ref), priceGroups og fareTables utenfor (evt i FareProduct)? (</em>
        <img
        src="../.gitbook/assets/warning.png" alt="(warning)" /> <em>F.eks. kun i</em>  <a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-SalesOfferPackageElement"><em>SalesOfferPackageElement</em></a><em>)</em>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">
        <img src="../.gitbook/assets/warning.png" alt="(warning)" />validityParameterAssignments</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-GenericParameterAssignment">GenericParameterAssignment</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of VALIDITY PARAMETER ASSIGNMENTs for SALES OFFER PACKAGE</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">distributionAssignments</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-DistributionAssignment">DistributionAssignment</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>List of DISTRIBUTION ASSIGNMENTs for SALES OFFER PACKAGE</p>
        <p><em>Can be defined as separate object and referred, but may be more consistent to have embedded</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RoundingRef</td>
      <td style="text-align:left">RoundingRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to a ROUNDING</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">prices</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-SalesOfferPackagePrice">SalesOfferPackagePrice</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of SALES OFFER PACKAGE PRICEs associated with the SALES OFFER PACKAGE
        ELEMENT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">salesOfferPackageElements</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-SalesOfferPackageElement">SalesOfferPackageElement</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">List of SALES OFFER PACKAGE ELEMENTs</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>SalesOfferPackageSubstitutions</del>
      </td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-SalesOfferPackageSubstitution"><del>SalesOfferPackageSubstitution</del></a>
      </td>
      <td style="text-align:left"><del>1: *</del>
      </td>
      <td style="text-align:left"><del>List of SALES OFFER PACKAGE SUBSTITUTIONs</del>
      </td>
    </tr>
  </tbody>
</table>

#### GroupOfSalesOfferPackages <a id="fares-GroupOfSalesOfferPackages"></a>

A grouping of SALES OFFER PACKAGEs

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| GroupOfSalesOfferPackages &lt; [GroupOfEntities](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-GroupOfEntities) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | alternativeNames | [AlternativeName](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=framework&linkCreation=true&fromPageId=1638137934) | 0: \* | ALTERNATIVE NAMEs for GROUP of SALES OFFER PACKAGEs |
| element | PricingServiceRef | PricingServiceRef | 0: \* | PRICING SERVICE to use to fetch prices dynamically |
| element | PricingRuleRef | [PricingRuleRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects%28FareandSalesTransactionframes%29-PricingRuleRef) | 0: \* | Default PRICING RULE to use to derive prices from this element |
| element | priceGroups | PriceGroupRef | 0: \* | PRICE GROUPs associated with this element |
| \(choice\) element | fareTables | StandardFareTableRef | 0: \* | List of FARE TABLEs associated with this element |
| FareTableRef |  |  |  |  |
| element | SalesOfferPackageElements | SalesOfferPackageElement | 0: 1 | Common properties of SALES OFFER PACKAGE and GROUP OF SALES OFFER PACKAGES |
| element | members | SalesOfferPackageRef | 1: \* | References to members of GROUP of SALES OFFER PACKAGEs |

#### SalesOfferPackageElement <a id="fares-SalesOfferPackageElement"></a>

The assignment of a FARE PRODUCT to a TYPE OF TRAVEL DOCUMENT in order to define a SALES OFFER PACKAGE, realised as a fixed assignment \(printing, magnetic storage etc.\) or by the possibility for the FARE PRODUCT to be reloaded on the TYPE OF TRAVEL DOCUMENT.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left">SalesOfferPackageElement &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject">PriceableObject</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RequiresValidation</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether element requires validation before it can be used</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>ConditionSummary</del>
      </td>
      <td style="text-align:left"><del>ConditionSummary</del>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left"><del>Summary description of SALES OFFER PACKAGE properties</del>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>SalesOfferPackageRef</del>
      </td>
      <td style="text-align:left"><del>SalesOfferPackageRef</del>
      </td>
      <td style="text-align:left"><del>1: 1 (ikke implementert som mandatory)</del>
      </td>
      <td style="text-align:left">
        <p><del>Reference to a SALES OFFER PACKAGE of which this is part. If not given by containing context must be specified.</del>
        </p>
        <p>Sannsynligvis bedre med embedding enn referanse, dvs SalesOfferPackage
          inkluderer sine elements?</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">TypeOfTravelDocumenRef</td>
      <td style="text-align:left">TypeOfTravelDocumenRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to a TYPE OF TRAVEL DOCUMENT.</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">FareProductRef</td>
      <td style="text-align:left">FareProductRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">FARE PRODUCT associated with this SALES OFFER PACKAGE</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">validityParameterAssignments</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares#GenericParameterAssignment">GenericParameterAssignment</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">GENERIC PARAMETER ASSIGNMENTs associated with the SALES OFFER PACKAGE
        ELEMENT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">prices</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-SalesOfferPackagePrice">SalesOfferPackagePriceRef</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">SALES OFFER PACKAGE PRICEs associated with the SALES OFFER PACKAGE ELEMENT</td>
    </tr>
  </tbody>
</table>

#### ~~SalesOfferPackageSubstitution~~ <a id="fares-SalesOfferPackageSubstitution"></a>

~~Information on the preferred substitution of packages with other package if quota restricted product is no longer available. The relative priority is specified using the order attribute inherited from ASSIGNMENT.~~

~~Example can be found in the~~ [~~official GitHub-repository for Entur~~](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

<table>
  <thead>
    <tr>
      <th style="text-align:left"><del>SalesOfferPackageSubstitution &lt; </del><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Assignment"><del>Assignment</del></a><del> &lt; </del>
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject"><del>DataManagedObject</del>
          </a><del> &lt; </del><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion"><del>EntityInVersion</del></a><del> &lt; </del>
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity"><del>Entity</del>
            </a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><del>XML-type</del>
      </td>
      <td style="text-align:left"><del>Name</del>
      </td>
      <td style="text-align:left"><del>Datatype</del>
      </td>
      <td style="text-align:left"><del>Cardinality</del>
      </td>
      <td style="text-align:left"><del>Description</del>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>SalesOfferPackageRef</del>
      </td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-fares.md#fares-SalesOfferPackage">SalesOfferPackage</a>
      </td>
      <td style="text-align:left"><del>0: *</del>
      </td>
      <td style="text-align:left">
        <p><del>text</del>
        </p>
        <p><del>Anbefaler som del av objektet fremfor eksternt definert (i FareFrame) med referanse, siden dette (sannsynligvis) vil v&#xE6;re unikt per SalesOfferPackage</del>
        </p>
      </td>
    </tr>
  </tbody>
</table>

#### DistributionAssignment <a id="fares-DistributionAssignment"></a>

An assignment of the COUNTRY and/or DISTRIBUTION CHANNEL through which a product may or may not be distributed

[See definition in General information](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=Generell%20informasjon%20NeTEx&linkCreation=true&fromPageId=1638137934)

<table>
  <thead>
    <tr>
      <th style="text-align:left">DistributionAssignment &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Assignment">Assignment</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity">Entity</a>
      </th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">XML-type</td>
      <td style="text-align:left">Name</td>
      <td style="text-align:left">Datatype</td>
      <td style="text-align:left">Cardinality</td>
      <td style="text-align:left">Description</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>ServiceAccessRightRef</del>
      </td>
      <td style="text-align:left"><del>ServiceAccessRightRef</del>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left">
        <p><del>Reference to a SERVICE ACCESS RIGHT</del>
        </p>
        <p><em>Rather referenced through PreassignedFareProduct of SalesOfferPackageElement</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">SalesOfferPackageRef</td>
      <td style="text-align:left">SalesOfferPackageRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to a SALES OFFER PACKAGE</td>
    </tr>
    <tr>
      <td style="text-align:left">GroupOfSalesOfferPackagesRef</td>
      <td style="text-align:left">GroupOfSalesOfferPackagesRef</td>
      <td style="text-align:left">Reference to a GROUP OF SALES OFFER PACKAGEs</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DistributionRights</td>
      <td style="text-align:left">DistributionRightsEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>List of values for DISTRIBUTION RIGHTs</p>
        <p>Allowed values:</p>
        <ul>
          <li>none</li>
          <li>sell</li>
          <li>exchange</li>
          <li>refund</li>
          <li>inform</li>
          <li>private</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DistributionChannelType</td>
      <td style="text-align:left">DistributionChannelTypeEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Classification of DISTRIBUTION CHANNEL</p>
        <p>Allowed values:</p>
        <ul>
          <li>atStop</li>
          <li>onBoard</li>
          <li>online</li>
          <li>telephone</li>
          <li>electronicPass</li>
          <li>postal</li>
          <li>mobileDevice</li>
          <li>agency</li>
          <li>tourOperator</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">AllowedInChannel</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether distribution is allowed or forbidden for given channel</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RestrictedToChannel</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether distribution is restricted to a given <del>country and / or</del> channel</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MandatoryProduct</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether product is mandatory, i.e. must be provided</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">TicketingServiceFacilityList</td>
      <td style="text-align:left">TicketingServiceFacilityEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>List of TICKETING SERVICE FACILITies</p>
        <p>Allowed values:</p>
        <ul>
          <li>purchase</li>
          <li>collection</li>
          <li>cardTopUp</li>
          <li>reservations</li>
          <li>exchange</li>
          <li>refund</li>
          <li>renewal</li>
          <li>excessFares</li>
          <li>all</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PaymentMethods</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Payment methods</p>
        <p>Allowed values:</p>
        <ul>
          <li>cash</li>
          <li>cashAndCard</li>
          <li>coin</li>
          <li>banknote</li>
          <li>cheque</li>
          <li>travellersCheque</li>
          <li>postalOrder</li>
          <li>companyCheque</li>
          <li>creditCard</li>
          <li>debitCard</li>
          <li>cardsOnly</li>
          <li>travelCard</li>
          <li>contactlessPaymentCard</li>
          <li>contactlessTravelCard</li>
          <li>sms</li>
          <li>mobilePhone</li>
          <li>voucher</li>
          <li>token</li>
          <li>warrant</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">RequiresRegistration</td>
      <td style="text-align:left">xsd:boolean</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Whether distribution requires registered user</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">FulfilmentMethodRef</td>
      <td style="text-align:left">FulfilmentMethodRef</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to a FULFILMENT METHOD</td>
    </tr>
  </tbody>
</table>

**Currently missing in NeTEx**

Vurdere PR for utvidelse med **GroupOfDistributionAssignments** som peker på "standardgrupper" av vanlige konfigurasjoner, for å slippe å assigne _alle_ SalesOfferPackage til _alle_ aktuelle DistributionAssignments?

#### GroupOfDistributionAssignments <a id="fares-GroupOfDistributionAssignments"></a>

Type for a collection of one or more references to a DISTRIBUTION CHANNEL.

Example can be found in the [official GitHub-repository for Entur](https://github.com/rutebanken/profile-norway-examples/blob/master/netex/network/Line61A.xml)

| GroupOfDistributionAssignments &lt; [GroupOfEntities](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-GroupOfEntities) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | members | DistributionAssignmentRefs | 1: 1 | List containing _minimum two or more_ DistributionAssignmentRef for group |

