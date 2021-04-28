# Håndbok N801 \(SIRI/NeTEX\) : sales

This page is currently a work in progress and not yet included in the Nordic NeTEx Profile

**Version**

Current version for **fares** is:   **v0.8**   \(last changed 20 Oct 2020\) 

## Content <a id="sales-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591705944 {padding: 0px;}  
div.rbtoc1619591705944 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591705944 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Components](handbok-n801-siri-netex-sales.md#sales-Components)
  * [Customer](handbok-n801-siri-netex-sales.md#sales-Customer)
    * [Customer](handbok-n801-siri-netex-sales.md#sales-Customer.1)
    * [CustomerAccount](handbok-n801-siri-netex-sales.md#sales-CustomerAccount)
  * [Sales Transaction](handbok-n801-siri-netex-sales.md#sales-SalesTransaction)
    * [FareContract](handbok-n801-siri-netex-sales.md#sales-FareContract)
    * [FareContractEntry](handbok-n801-siri-netex-sales.md#sales-FareContractEntry)
    * [SalesTransaction](handbok-n801-siri-netex-sales.md#sales-SalesTransaction.1)
  * [Purchase](handbok-n801-siri-netex-sales.md#sales-Purchase)
    * [CustomerPurchasePackage](handbok-n801-siri-netex-sales.md#sales-CustomerPurchasePackage)
    * [CustomerPurchasePackageElement](handbok-n801-siri-netex-sales.md#sales-CustomerPurchasePackageElement)
    * [CustomerPurchasePackageElementAccess](handbok-n801-siri-netex-sales.md#sales-CustomerPurchasePackageElementAccess)
    * [CustomerPurchaseParameterAssignment](handbok-n801-siri-netex-sales.md#sales-CustomerPurchaseParameterAssignment)
  * [Prices](handbok-n801-siri-netex-sales.md#sales-Prices)
    * [CustomerPurchasePackagePrice](handbok-n801-siri-netex-sales.md#sales-CustomerPurchasePackagePrice)

This document is part of the Norwegian NeTEx Profile and describes data elements for the exchange of **customer, retail, consumption control and sales transaction information** via the NeTEx format.

Please note the [fare](https://enturas.atlassian.net/wiki/spaces/AR/pages/886898719)/sales-transaction parts of the profile describes data object for managing and exchanging fare structures, access rights, fare products, pricing, sales management/services, fare validation and consumption, as well as the presentation of fare information to the travelling public. It does not, however, describe network or time-related concepts, such as topology, date objects or departure times, as these are described in their respective profile documents [stops](handbok-n801-siri-netex-stops.md)/[network](handbok-n801-siri-netex-network.md) and [timetable](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable).

## Components <a id="sales-Components"></a>

### Customer <a id="sales-Customer"></a>

#### Customer <a id="sales-Customer.1"></a>

An identified person or organisation involved in a fare process. There may be a FARE CONTRACT between the CUSTOMER and the OPERATOR or the AUTHORITY ruling the consumption of services.

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

<table>
  <thead>
    <tr>
      <th style="text-align:left">Customer &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
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
      <td style="text-align:left">Surname</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Surname of a FARE CUSTOMER</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">FirstName</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">First name of CUSTOMER</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">DateOfBirth</td>
      <td style="text-align:left">xsd:date</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Date of birth of CUSTOMER</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>IdentityDocumentRef</del>
      </td>
      <td style="text-align:left">
        <p><del>PrivateCodeStructure (xsd:normalizedString)</del>
        </p>
        <p><del><em>Discrepancy, see </em></del><a href="https://enturas.atlassian.net/wiki/spaces/AR/pages/631144503/Known+errors+NeTEx"><del><em>Known errors NeTEx</em></del></a>
        </p>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left"><del>A document that identifies the CUSTOMER</del>
      </td>
    </tr>
  </tbody>
</table>

#### CustomerAccount <a id="sales-CustomerAccount"></a>

An identified person or organisation involved in a fare process. There may be a FARE CONTRACT between the CUSTOMERACCOUNT and the OPERATOR or the AUTHORITY ruling the consumption of services.

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

<table>
  <thead>
    <tr>
      <th style="text-align:left">CustomerAccount &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
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
      <td style="text-align:left">EndDate</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">End date of FARE CONTRACT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Status</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Status of FARE CONTRACT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">CustomerRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1637777537/sales+work+in+progress#Customer.1">CustomerRef</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to CUSTOMER that holds account</td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>TypeOfCustomerAccountRef</del>
      </td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp(forcopy/paste)-OLDEDITOR-tobedeletedwhencontentismigrated-TypeOfCustomerAccount"><del>TypeOfCustomerAccount</del></a>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left"><del>Type of CUSTOMER ACCOUNT</del>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>CustomerAccountStatusRef</del>
      </td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp(forcopy/paste)-OLDEDITOR-tobedeletedwhencontentismigrated-CustomerAccountStatus"><del>CustomerAccountStatus</del></a>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left"><del>Status of a CUSTOMER ACCOUNT</del>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">CustomerAccountStatusType</td>
      <td style="text-align:left">CustomerAccountStatusTypeEnum</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Allowed values:</p>
        <ul>
          <li>unused</li>
          <li>active</li>
          <li>dormant</li>
          <li>suspended</li>
          <li>archived</li>
          <li>closed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">customerPurchasePackages</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp(forcopy/paste)-OLDEDITOR-tobedeletedwhencontentismigrated-CustomerPurchasePackage">CustomerPurchasePackage</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">CUSTOMER PURCHASE PACKAGEs for the CUSTOMER ACCOUNT</td>
    </tr>
  </tbody>
</table>

### Sales Transaction <a id="sales-SalesTransaction"></a>

#### FareContract <a id="sales-FareContract"></a>

A contract with a particular \(but possibly anonymous\) customer, ruling the consumption of transport services \(and joint services\). A FARE CONTRACT may be designed for a fixed SALES OFFER PACKAGE \(e.g. ticket\) or to allow successive purchases of SALES OFFER PACKAGEs.

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

<table>
  <thead>
    <tr>
      <th style="text-align:left">FareContract &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
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
      <td style="text-align:left">StartDate</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Start date of FARE CONTRACT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">EndDate</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">End date of FARE CONTRACT</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Status</td>
      <td style="text-align:left">xsd:normalizedString</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Status of FARE CONTRACT</td>
    </tr>
    <tr>
      <td style="text-align:left">(choice)
        <br />element</td>
      <td style="text-align:left">CustomerRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp(forcopy/paste)-OLDEDITOR-tobedeletedwhencontentismigrated-Customer">CustomerRef</a>
      </td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Reference to the CUSTOMER for the FARE CONTRACT</td>
    </tr>
    <tr>
      <td style="text-align:left">CustomerAccountRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp(forcopy/paste)-OLDEDITOR-tobedeletedwhencontentismigrated-CustomerAccount">CustomerAccount</a>
      </td>
      <td style="text-align:left">Reference to the CUSTOMER ACCOUNT associated with the FARE CONTRACT</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><del>element</del>
      </td>
      <td style="text-align:left"><del>TypeOfFareContractRef</del>
      </td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp(forcopy/paste)-OLDEDITOR-tobedeletedwhencontentismigrated-TypeOfFareContract"><del>TypeOfFareContract</del></a>
      </td>
      <td style="text-align:left"><del>0: 1</del>
      </td>
      <td style="text-align:left"><del>Type of FARE CONTRACT</del>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">fareContractEntries</td>
      <td style="text-align:left">
        <p><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1637777537/sales+work+in+progress#SalesTransaction">FareContractEntry</a>
        </p>
        <p><em>Should maybe simplify to allow SalesTransaction(Ref) only?</em>
        </p>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">FARE CONTRACT ENTRies making up the FARE CONTRACT</td>
    </tr>
  </tbody>
</table>

#### FareContractEntry <a id="sales-FareContractEntry"></a>

An **abstract** type to record an event occurring in the life of a FARE CONTRACT: initial contracting, sales, validation entries, etc. A subset of a FARE CONTRACT ENTRY is often materialised on a TRAVEL DOCUMENT \(e.g. [SalesTransaction](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1637777537/sales+work+in+progress#SalesTransaction)\) ~~or TravelSpecification\)~~

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

| FareContractEntry &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | IsValid | xsd:boolean | 0: 1 | Whether the FARE CONTRACT ENTRY is valid or not |

#### SalesTransaction <a id="sales-SalesTransaction.1"></a>

A SALE OF a FIXED PACKAGE or a SALE OF a RELOADABLE PACKAGE

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

<table>
  <thead>
    <tr>
      <th style="text-align:left">SalesTransaction &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1637777537/sales#FareContractEntry">FareContractEntry</a> &lt;
        <a
        href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-DataManagedObject">DataManagedObject</a>&lt; <a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-EntityInVersion">EntityInVersion</a> &lt;
          <a
          href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-Entity">Entity</a>
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
      <td style="text-align:left">Date</td>
      <td style="text-align:left">xsd:dateTime</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">Date of SALES TRANSACTION</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Amount</td>
      <td style="text-align:left">CurrencyAmountType (xsd:decimal)</td>
      <td style="text-align:left"><b>1: 1</b>
      </td>
      <td style="text-align:left">Amount of SALES TRANSACTION</td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">Currency</td>
      <td style="text-align:left">CurrencyType (xsd:NMTOKEN)</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>ISO 4717 3-letter currency code</p>
        <p><em>Defaults to local currency for the sales transaction system</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">PaymentMethod</td>
      <td style="text-align:left">PaymentMethodEnumeration</td>
      <td style="text-align:left"><b>0: 1</b>
      </td>
      <td style="text-align:left">
        <p>Allowed values:</p>
        <ul>
          <li>cash</li>
          <li>cashAndCard</li>
          <li>creditCard</li>
          <li>debitCard</li>
          <li>travelCard</li>
          <li>sms</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">customerPurchasePackages</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1637777537/sales#CustomerPurchasePackage">CustomerPurchasePackage</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">CUSTOMER PURCHASE PACKAGEs bought by SALES TRANSACTION</td>
    </tr>
  </tbody>
</table>

### Purchase <a id="sales-Purchase"></a>

#### CustomerPurchasePackage <a id="sales-CustomerPurchasePackage"></a>

A purchase of a SALES OFFER PACKAGE by a CUSTOMER, giving access rights to one or several FARE PRODUCTs materialised as one or several TRAVEL DOCUMENTs.

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

| CustomerPurchasePackage &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | SalesOfferPackageRef | [SalesOfferPackage](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp%28forcopy/paste%29-OLDEDITOR-tobedeletedwhencontentismigrated-SalesOfferPackage) | **1: 1** | Reference to a SALES OFFER PACKAGE for which this is a purchase |
| \(choice\) element | CustomerRef | [CustomerRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp%28forcopy/paste%29-OLDEDITOR-tobedeletedwhencontentismigrated-Customer) | 0: 1 | Reference to the CUSTOMER associated with CUSTOMER PURCHASE PACKAGE |
| CustomerAccountRef | [CustomerAccountRef](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp%28forcopy/paste%29-OLDEDITOR-tobedeletedwhencontentismigrated-CustomerAccount) | Reference to the CUSTOMER ACCOUNT associated with CUSTOMER PURCHASE PACKAGE |  |  |
| element | customerPurchasePackageElements | [CustomerPurchasePackageElement](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp%28forcopy/paste%29-OLDEDITOR-tobedeletedwhencontentismigrated-CustomerPurchasePackageElement) | **1: \*** | CUSTOMER PURCHASE PACKAGE ELEMENTs associated with the CUSTOMER PURCHASE PACKAGE |
| \(choice\) element | prices | [CustomerPurchasePackagePrice](handbok-n801-siri-netex-sales.md#sales-CustomerPurchasePackagePrice) | 0: \* | CUSTOMER PURCHASE PACKAGE PRICEs associated with the CUSTOMER PURCHASE PACKAGE |
| [CustomerPurchasePackagePriceRef](handbok-n801-siri-netex-sales.md#sales-CustomerPurchasePackagePrice) | Reference to a CUSTOMER PURCHASE PACKAGE PRICEs associated with the CUSTOMER PURCHASE PACKAGE |  |  |  |

#### CustomerPurchasePackageElement <a id="sales-CustomerPurchasePackageElement"></a>

The assignment of a SALES OFFER PACKAGE ELEMENT, for use in a CUSTOMER SALES PACKAGE.

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

| CustomerPurchasePackageElement &lt; [PriceableObject](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#PriceableObject) &lt; [DataManagedObject](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-DataManagedObject) &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=728727624#framework-Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| element | SalesOfferPackageElementRef | [SalesOfferPackageElement](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp%28forcopy/paste%29-OLDEDITOR-tobedeletedwhencontentismigrated-SalesOfferPackageElement) | **1: 1** | Reference to a SALES OFFER PACKAGE for which this is a purchase |
| element | elementAccesses | [CustomerPurchasePackageElementAccess](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp%28forcopy/paste%29-OLDEDITOR-tobedeletedwhencontentismigrated-CustomerPurchasePackageElementAccess) | **1: \*** | CUSTOMER PURCHASE PACKAGE ELEMENT ACCESSes making up the CUSTOMER PURCHASE PACKAGE ELEMENT |
| element | validityParameterAssignments | [CustomerPurchaseParameterAssignment](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=1015382117#tmp%28forcopy/paste%29-OLDEDITOR-tobedeletedwhencontentismigrated-CustomerPurchaseParameterAssignment) | **1: \*** | ACCESS RIGHT PARAMETER ASSIGNMENTs selected for the CUSTOMER PURCHASE PACKAGE ELEMENT |
| ~~element~~ | ~~prices~~ | [~~CustomerPurchasePackageElementPrice~~](https://enturas.atlassian.net/wiki/pages/createpage.action?spaceKey=AR&title=fares&linkCreation=true&fromPageId=1637777537) | ~~**1: \***~~ | ~~CUSTOMER PURCHASE PACKAGE ELEMENT PRICEs associated with the CUSTOMER PURCHASE PACKAGE ELEMENT~~ |

#### CustomerPurchasePackageElementAccess <a id="sales-CustomerPurchasePackageElementAccess"></a>

Access to a VALIDABLE ELEMENT by a specific CUSTOMER PURCHASE PACKAGE through use of CUSTOMER PURCHASE PACKAGE.

_This is needed for validation / activation of complex SALES OFFER PACKAGEs containing tariffs structures that have FARE STRUCTURE ELEMENTs IN SEQUENCE, in such a case a given SALES PACKAGE ELEMENT may have multiple VALIDABLE ELEMENTs associated with it, each of which can be separately validated and marked._

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

<table>
  <thead>
    <tr>
      <th style="text-align:left">CustomerPurchasePackageElementAccess &lt; VersionedChild &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion">EntityInVersion</a> &lt;
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
      <td style="text-align:left">(choice) element</td>
      <td style="text-align:left">ValidableElementRef</td>
      <td style="text-align:left"><a href="https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=585105589#TEMPORARY-UnusedNeTExpart3Faresdataobjects(FareandSalesTransactionframes)-ValidableElementRef">ValidableElementRef</a>
      </td>
      <td style="text-align:left"><b>1: 1</b>
      </td>
      <td style="text-align:left">VALIDABLE ELEMENT associated with the CUSTOMER PURCHASE PACKAGE ELEMENT
        ACCESS</td>
    </tr>
    <tr>
      <td style="text-align:left">FareStructureElementRef</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-sales.md#sales-FareStructureElement">FareStructureElementRef</a>
      </td>
      <td style="text-align:left">FARE STRUCTURE ELEMENT associated with the CUSTOMER PURCHASE PACKAGE ELEMENT
        ACCESS</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">MarkedAs</td>
      <td style="text-align:left">MarkedAsEnumeration</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>Usage/marking status of CUSTOMER PURCHASE PACKAGE ELEMENT ACCESS</p>
        <p>Allowed values:</p>
        <ul>
          <li>unused</li>
          <li>activated</li>
          <li>(marked)</li>
          <li>used</li>
          <li>expired</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">validityParameterAssignments</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-sales.md#sales-CustomerPurchaseParameterAssignment">CustomerPurchaseParameterAssignment</a>
      </td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">CUSTOMER PURCHASE PARAMETER ASSIGNMENTs selected for the CUSTOMER PURCHASE
        PACKAGE ELEMENT ACCESS</td>
    </tr>
  </tbody>
</table>

#### CustomerPurchaseParameterAssignment <a id="sales-CustomerPurchaseParameterAssignment"></a>

A VALIDITY PARAMETER ASSIGNMENT specifying practical parameters chosen for a CUSTOMER PURCHASE PACKAGE within a given fare structure \(e.g. the origin or destination zone in a zone-counting system\). 

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

<table>
  <thead>
    <tr>
      <th style="text-align:left">CustomerPurchaseParameterAssignment &lt; ValidityParameterAssignment &lt;
        AccessRightParameterAssignment &lt; <a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#DataManagedObject">DataManagedObject</a> &lt;
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
        <p>Logical operator for combining USAGE PARAMETERs
          <br />elements. The default is &#x2018;AND&#x2019;.</p>
        <p><em>&#x2018;OR&#x2019; and &#x2018;XOR&#x2019; should only be used if parameters are all of the same types.</em>
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
        <p><del>Where one or more parameter is a group containing</del>
          <br /><del>multiple elements, (GROUP OF xxx), set operator for distinguishing between whole set and item interpretation of elements which are sets of elements</del>
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
      <td style="text-align:left"><a href="handbok-n801-siri-netex-sales.md#sales-UsageParameter">UsageParameter</a>
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
      <td style="text-align:left">Temporal validity parameters for the assignment (e.g. <a href="handbok-n801-siri-netex-sales.md#sales-OperatingDay">OperatingDay</a>)</td>
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
            <br />Successive elements are logically OR&apos;ed together; comparison must
            satisfy at least one specified value</li>
          <li>AND =
            <br />Successive elements are logically AND&apos;ed together; comparison must
            satisfy all specified values</li>
          <li>NOT =
            <br />Specified elements <b>must</b> be different from the given value</li>
          <li>XOR =
            <br />Successive elements are logically OR&apos;ed together; comparison must
            satisfy <b>only one</b> of the specified values</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">includes</td>
      <td style="text-align:left">GenericParameterAssignmentInContext</td>
      <td style="text-align:left">0: *</td>
      <td style="text-align:left">A list of VALIDITY PARAMETER ASSIGNMENT <em>without ID constraint used only in the given context</em> specifying
        practical parameters during a TRAVEL GenericATION, within a given fare
        structure (e.g. the origin or destination zone in a zone-counting system)</td>
    </tr>
  </tbody>
</table>

### Prices <a id="sales-Prices"></a>

#### CustomerPurchasePackagePrice <a id="sales-CustomerPurchasePackagePrice"></a>

A specialisation of FARE PRICE that defines the price of a CUSTOMER PURCHASE PACKAGE.

An example can be found in the [official GitHub-repository for Entur](https://github.com/entur/profile-examples/tree/master/netex/fares)

| CustomerPurchasePackagePrice &lt; [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) &lt; VersionedChild &lt; [EntityInVersion](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#EntityInVersion) &lt; [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#Entity) |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| XML-type | Name | Datatype | Cardinality | Description |
| CustomerPurchasePackagePrice inherits from [FarePrice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#FarePrice) without introducing new elements or attributes. |  |  |  |  |

