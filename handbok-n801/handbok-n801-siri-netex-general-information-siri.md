# Håndbok N801 \(SIRI/NeTEX\) : General information SIRI

Version

Current version for **Norwegian** **SIRI profile** is:   **v1.1**  \(_last changed_ 10 Nov 2020\)

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591762423 {padding: 0px;}  
div.rbtoc1619591762423 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591762423 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Preface](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Preface)
* [Introduction](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Introduction)
  * [Service Interface for Real Time Information \(SIRI\)](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-ServiceInterfaceforRealTimeInformation%28SIRI%29)
  * [SIRI high-level model](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-SIRIhigh-levelmodel)
    * [Services supported by the Norwegian SIRI-standard](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-ServicessupportedbytheNorwegianSIRI-standard)
  * [What the profile does not include](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Whattheprofiledoesnotinclude)
  * [Terminology](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Terminology)
    * [SIRI-specific objects and formats](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-SIRI-specificobjectsandformats)
    * [General requirements on data](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Generalrequirementsondata)
  * [Using ID's](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-UsingID%27s)
    * [Fixed ID's](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-FixedID%27s)
* [Exchanging data](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Exchangingdata)
  * [Asynchronous](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Asynchronous)
    * [Publish/Subscribe - Direct delivery](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Publish/Subscribe-Directdelivery)
    * [Publish/Subscribe - Fetched delivery](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Publish/Subscribe-Fetcheddelivery)
  * [Synchronous](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Synchronous)
    * [Request/response](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Request/response)
  * [General requirements](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Generalrequirements)
    * [Standard values](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Standardvalues)
    * [Data correctness](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Datacorrectness)
    * [Data completeness](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Datacompleteness)
    * [Data content](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Datacontent)
    * [Data freshness](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Datafreshness)
* [Common components](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Commoncomponents)
  * [Message objects](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Messageobjects)
    * [ServiceDelivery](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-ServiceDelivery)
  * [Data types](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-Datatypes)
    * [NaturalLanguageStringStructure](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-NaturalLanguageStringStructure)
    * [NaturalLanguagePlaceNameStructure](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-NaturalLanguagePlaceNameStructure)
    * [FramedVehicleJourneyRefStructure ](handbok-n801-siri-netex-general-information-siri.md#GeneralinformationSIRI-FramedVehicleJourneyRefStructure)

## Preface <a id="GeneralinformationSIRI-Preface"></a>

A Norwegian standard for exchanging uniform real-time data is extremely valuable for:

**Entur AS on behalf of Jernbanedirektoratet**

...in order to efficiently collect all real-time data from each data provider, ensure consistency of data, and increase data quality. This allows the creation of multimodal information systems which may be used to implement nationwide journey planning solutions and publicize business neutral information to all interested parties.

**for travellers**

...in order to present relevant, and up-to-date, high-quality journey suggestions.

**for public transport operators**

...in order to re-use the data in their own journey planning-, ticketing-, and information systems, and offer a better service to their customers.

**for third party service providers**

...in order to minimize unnecessary costs related to supporting multiple different exchange formats, and to contribute to continued growth of standardized public transport data exchange.

## Introduction <a id="GeneralinformationSIRI-Introduction"></a>

### Service Interface for Real Time Information \(SIRI\) <a id="GeneralinformationSIRI-ServiceInterfaceforRealTimeInformation(SIRI)"></a>

`Service Interface for Real Time Information (SIRI)` is a CEN-specification \(`CEN/TS 15531, prCEN/TS-OO278181`\) for exchanging real-time data for public transport and vehicles. Its development was a cooperative effort between France, Germany \(Verband Deutscher Verkehrsunternehmen, VDV\), Scandinavia and Great Britain \(`UK Real Time Interest Group, RTIG`\). The standard is based on the reference model **Transmodel** \(`CEN TC278, EN12896`\) and contains a general model for real-time data and an XML Schema for its implementation.

The SIRI format is used to update planned data with short term changes and deviations in the form of vehicle positions, estimated arrival times, and relevant textual messages.

The guidelines for using SIRI 2.0 XML Schema are specified by a local \(Norwegian\) profile of the SIRI format, which accounts for existing systems, as well as future needs. Like the [Nordic NeTEx Profile](handbok-n801-siri-netex-nordic-netex-profile.md), which defines the planned and fixed portion of public transport data, the Norwegian SIRI profile describes how- and which parts of the wider format to use. It is based on `Transmodel 5.1 (EN 12896: 2006)` which in turn is based on the standards of `NEPTUNE (AFNOR - PR NF P99-506 desember 2009)` and IFOPT \(EN 28701 - Identification of Fixed Objects in Public Transport\). The purpose of the profile is to clarify which events and data are expected to be included in a comprehensive data exchange and to make the implementation of common standards easier.

SIRI defines a standardised communication layer with procedures and mechanisms for exchanging data by means of a format which is openly described to the public and in wide use around the world. 

* Well known interface 
  * Openness
  * Scalability
  * Flexible for particular needs
* Re-useability for architecture, infrastructure and services \(cost-saving\)
  * Content independent from transfer protocols
  * Standardised publication and message handling 
    * WebService \(HTTP/SOAP with request/response\) and WS-PubSub
    * Supports common mechanisms for access control, versioning and error handling
  * Configurable updating and filtering

Links for more information about the formats

* SIRI: [https://www.vdv.de/siri.aspx](https://www.vdv.de/siri.aspx)
* Transmodel: [http://transmodel-cen.eu](http://transmodel-cen.eu/)
* NeTEx: [http://netex-cen.eu/](http://netex-cen.eu/)

### SIRI high-level model <a id="GeneralinformationSIRI-SIRIhigh-levelmodel"></a>

Overview of the functional services from the official SIRI-documentation:

![](../.gitbook/assets/637374618.jpg)

#### Services supported by the Norwegian SIRI-standard <a id="GeneralinformationSIRI-ServicessupportedbytheNorwegianSIRI-standard"></a>

Real-time information in Norway is exchanged in three formats, **SIRI-ET**, **SIRI-SX** and **SIRI-VM**:

1. **Estimated Timetable \(ET\)** for continuous updates per line, restricted to the current operational day \(may differ from calendar days\).
   1. Changes like delays, cancellations, additional departures, over-takes, or stops that are not going to be served.  
2. **Situation Exchange \(SX\)** for information on disruptions in the public transport service
   1. Information about planned deviations \(such as maintenance work on the tracks\)
   2. Information about unplanned deviations \(such as accidents, unforeseen issues with passengers, objects blocking the road, or severe weather\)  
3. **Vehicle Monitoring \(VM\)** for tracking the position of the vehicles used for public transport
   1. The actual position of vehicles as they traverse a route \(GPS data\).

SIRI also supports real-time information data types which are **not** included in the Norwegian profile:

1. **Production Timetable \(PT\)** for changes in planned time table data outside the current operational day.
2. **Stop Timetable \(ST\)** changes \(theoretic, planned, or calculated\) in arrivals and departures for stops outside the current operational day.
3. **Stop Monitoring \(SM\)** arrival- and transfer times for the same operational day.
   1. Calculated arrival time for a vehicle, usually based on GPS data.
4. **Connection Timetable \(CT\)** used to inform about guaranteed interchanges outside the current operational day.
5. **Connection Monitoring \(CM\)** for continuous updates on guaranteed interchanges.
   1. Whether the guarantee will be upheld.
   2. Unplanned interchanges \(for example, a bus will wait for a train\).
6. **General Messaging \(GM\)** for general text-based information, such as, for example, describing a widely impactful disruption.
7. **Facility Monitoring \(FM\)** for updating the status of equipment, or services.
   1. Elevators, escalators, ticket vending machines.

What the Norwegian SIRI profile includes

Based on relevant use cases as well as experience from existing real-time systems, the following features have been included:

1. Identification of reference data:
   1. Lines, Routes, and VehicleJourneys with arrival- and departure information
   2. StopPlaces, including type and Quays
   3. Connections and Transfers
   4. Data values
      * ServiceCategory
      * ProductCategory
      * VehicleFeatures
2. Specify technical data exchanges
   1. Type of data stream/subscription
   2. Categorisation of messages and data
   3. Message receipts \(when relevant\)
   4. Filtering mechanisms
   5. Consolidation and forwarding of partner-data \(including monitoring\)
   6. Meaning of functions
3. Usage of data fields
   1. Meanings
   2. Whether the field is mandatory or not
4.  The ability to describe possible expansions outside the bounds of the main SIRI profile.

### What the profile does _not_ include <a id="GeneralinformationSIRI-Whattheprofiledoesnotinclude"></a>

Technical specifications, local protocols, and their referential implementations are _not_ included in the Norwegian SIRI profile. The same is true for access privileges, the technical details for data transfers, and the administration of data sources and users.

Details regarding the methods of data transfer are however described in separate protocols, established and agreed upon between Entur, data sources and data users. This includes:

* User guides
* List of available services
* Access privileges
* Monitoring \(uptime, technical disturbances, maintenance\)

More info on utilisation of the Norwegian real-time data feeds, technical examples, real-time API documentation and a complete list of available data streams can be found at [https://developer.entur.org/pages-real-time-intro](https://developer.entur.org/pages-real-time-intro).

### Terminology <a id="GeneralinformationSIRI-Terminology"></a>

Terms and concepts for real-time data in SIRI are, just as in the case of stops- and timetable data, defined according to the NeTEx format standard, based on the European reference model "Transmodel". 

For a more detailed description of Transmodel-specific terms, see the [Norwegian NeTEx profile](handbok-n801-siri-netex-nordic-netex-profile.md).

Exchanging data in a single format means all communication systems involved need to have a unified interpretation of the terms and concepts being used. 

With Transmodel as the source for conceptual names, all objects will have English names, and any use of Norwegian terminology should be considered as guiding only since local concepts often have widely varying historical meanings and associations. For that reason, in particular, all users of the format should strive to use the unified terminology to the furthest extent possible.

It is likewise important to point out that all ID's for stop places \(StopPlace, Quay, etc.\) in the SIRI data must refer to the official stop ID's found in the national stop place registry. This is important for both data sources- as well as users.

#### SIRI-specific objects and formats <a id="GeneralinformationSIRI-SIRI-specificobjectsandformats"></a>

Definitions of Transmodel-related objects can be found in the [Norwegian NeTEx profile](handbok-n801-siri-netex-nordic-netex-profile.md). The following complementary table defines and clarifies SIRI-specific terms.

_Please note that the list is not exhaustive, and the list may be expanded on when needs arise._

<table>
  <thead>
    <tr>
      <th style="text-align:left">Data</th>
      <th style="text-align:left">Description of data type</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Encoding</td>
      <td style="text-align:left">Primarily UTF-8, but ISO-8859-1 and ASCII can also be handled.</td>
    </tr>
    <tr>
      <td style="text-align:left">Date/Time</td>
      <td style="text-align:left">
        <p>Dates and times must be in local time, according to <em><code>ISO 8601</code></em>,
          where &quot;00:00&quot; is midnight.</p>
        <p>Please note that the minimum granularity of times is in seconds, but even
          more precise timestamps can be used.</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Language</td>
      <td style="text-align:left">The language used must be defined as a <b>three-letter code</b> according
        to<code> ISO 639-3</code> (<em>recommended</em>) or as a <b>two-letter code</b> according
        to<code> ISO 639-1 / RFC 1766</code>.</td>
    </tr>
    <tr>
      <td style="text-align:left">Location</td>
      <td style="text-align:left">
        <p>Locations must always be defined according to <code>WGS84/GML</code> (normally <code>EPSG:4326</code>)</p>
        <p><em>Coordinates in other formats must be converted to WGS84 before being published in SIRI.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">StopPoint</td>
      <td style="text-align:left">In accordance with Transmodel, objects refer to a logical stop point,
        normally where passengers can board and alight. For practical reasons these
        points always have to be references to valid stops in the national stop
        place registry.</td>
    </tr>
    <tr>
      <td style="text-align:left">Destination</td>
      <td style="text-align:left">Usually, the final, or an important intermediary stop place in the route.</td>
    </tr>
    <tr>
      <td style="text-align:left">Origin</td>
      <td style="text-align:left">Usually, the first stop place in the route.</td>
    </tr>
  </tbody>
</table>

#### General requirements on data <a id="GeneralinformationSIRI-Generalrequirementsondata"></a>

For real-time data delivered in XML, the structure and content must syntactically be well-formed in accordance with SIRI 2.0 XML Schema \(XSD\), where all data fields contain meaningful information and are correctly formatted.

* Values must be trimmed \(no blanks first or last in data values\)
* Characters must be valid and in accordance with the _encoding_.

### Using ID's <a id="GeneralinformationSIRI-UsingID&apos;s"></a>

Requirements on unique ID's are described with more detail in the [Norwegian NeTEx profile](handbok-n801-siri-netex-nordic-netex-profile.md). It is important that all ID's in the SIRI- and NeTEx datasets are constants \(real-time, stops, timetables\), in order to prevent mismatches and other irregularities.

* References to **stops** must always use ID's from the national stop place registry.
* The data source is responsible for ensuring that ID's are correctly linked between timetable- and real-time data.

#### Fixed ID's <a id="GeneralinformationSIRI-FixedID&apos;s"></a>

Just as in the case of timetable data, it is strongly recommended that unchanged objects keep their ID's unchanged across datasets. This makes long term referencing, and tracking of changes easier.

## Exchanging data <a id="GeneralinformationSIRI-Exchangingdata"></a>

Communication of data must be implemented in accordance with the principles of REST-based services via HTTP.

In technical terms, the exchange of data must be identical for all types \(SIRI-ET, SIRI-SX and SIRI-VM\).

Three forms of data acquisition are allowed:

1. Publish/Subscribe - Direct delivery \(asynchronous\)
2. Publish/Subscribe - Fetched delivery \(asynchronous\)
3. Request/response \(synchronous\)

### Asynchronous <a id="GeneralinformationSIRI-Asynchronous"></a>

The service has been designed to continuously deliver data updates to all subscribed consumers.

When establishing a subscription, the data stream must be validated or reported as erroneous through the protocols of the mechanism.

All services of the publish/subscribe type **must send** [_**heartbeats**_](https://en.wikipedia.org/wiki/Heartbeat_%28computing%29) in accordance with the subscription-request \(_HeartbeatInterval_\), to ensure verification of service availability and operational status.

#### Publish/Subscribe - Direct delivery <a id="GeneralinformationSIRI-Publish/Subscribe-Directdelivery"></a>

When using _Direct Delivery_ the data is continuously streamed to all subscribers immediately after they are released into the stream. The recipient system is responsible for handling the received messages. A received message is acknowledged with a HTTP 200 "OK" success-response.

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy4919871387571942142",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=637370373&pageId=&name=PubSub-DirectDelivery&attachmentId=att637374647&pagePin=&imageAttachmentId=att637374642&border=&chrome=&html5=&size=&ceoId=&macroId=c3257a4f-1ac1-4f05-881b-75042ad9d421&spaceKey=&version=&migration=1&previewPageId=637370373&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy4919871387571942142&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJjNDViNjM0MTg3NGY2ODBlNWZlZjU5MTBmMjVkOWVjNDVlMmU1ZGIwY2EwM2Q1MDVlNDhhNDQzZjljODA4YmYxIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTk0MiwiaWF0IjoxNjE5NTkxNzYyfQ.Z4hDaKCaQBsYhs8lrwHUdZTfCsusx9dxwmXe3124poI",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiMjI5YTExOWEtZDQ3Mi00NThkLWIwN2UtNTY4MGE3OWY3Y2I1IiwiaWQiOiIyMjlhMTE5YS1kNDcyLTQ1OGQtYjA3ZS01NjgwYTc5ZjdjYjUifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxNyIsImlkIjoiNjM3MzcwMzczIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjYyLCJpYXQiOjE2MTk1OTE3NjJ9.N-6cMGL96fZoBv2wpdtdMEO5VdWDzz3zqFt6vLzhn9c",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"229a119a-d472-458d-b07e-5680a79f7cb5\",\"id\":\"229a119a-d472-458d-b07e-5680a79f7cb5\"},\"content\":{\"type\":\"page\",\"version\":\"17\",\"id\":\"637370373\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"637370373\",\"macro.hash\":\"229a119a-d472-458d-b07e-5680a79f7cb5\",\"page.type\":\"page\",\": = \| RAW \| = :\":\"imageAttachmentId=att637374642\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=c3257a4f-1ac1-4f05-881b-75042ad9d421\|migration=1\|name=PubSub-DirectDelivery\|diagramAttachmentId=att637374647\|containerId=637370373\|timestamp=1552402183238\",\"space.id\":\"637370369\",\"diagramAttachmentId\":\"att637374647\",\"containerId\":\"637370373\",\"timestamp\":\"1552402183238\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"content.version\":\"17\",\"page.title\":\"General information SIRI\",\"macro.body\":\"\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"17\",\"imageAttachmentId\":\"att637374642\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"c3257a4f-1ac1-4f05-881b-75042ad9d421\",\"content.id\":\"637370373\",\"migration\":\"1\",\"name\":\"PubSub-DirectDelivery\",\"macro.id\":\"229a119a-d472-458d-b07e-5680a79f7cb5\"}",  
    "timeZone":"Europe/Berlin",  
    "origin":"https://confluence-connect.gliffy.net",  
    "hostOrigin":"https://enturas.atlassian.net",  
    "sandbox":"allow-downloads allow-forms allow-modals allow-popups allow-scripts allow-same-origin allow-top-navigation-by-user-activation allow-storage-access-by-user-activation",    "pearApp":"true",        "apiMigrations": {  
        "gdpr": true  
    }  
}  
;  
    if\(window.AP && window.AP.subCreate\) {  
      window.\_AP.appendConnectAddon\(data\);  
    } else {  
      require\(\['ac/create'\], function\(create\){  
        create.appendConnectAddon\(data\);  
      }\);  
    }  
  }\(\)\);  


#### Publish/Subscribe - Fetched delivery <a id="GeneralinformationSIRI-Publish/Subscribe-Fetcheddelivery"></a>

When using _Fetched Delivery_ data is only sent when the receiving system has verified that it is ready to receive data from the stream. The message has to remain available with the data source until an explicit _dataSupplyRequest_ has been received, and the system has ensured data delivery in accordance with it. This delivery method allows the receiving system to hold off on data fetches until it is ready to do so. It is the responsibility of the data source to ensure that data is kept until the consumer has fully downloaded it.

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy8759968473731017022",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=637370373&pageId=&name=PubSub-FetchedDelivery&attachmentId=att637374619&pagePin=&imageAttachmentId=att637374638&border=&chrome=&html5=&size=&ceoId=&macroId=29a876fc-8bf1-4538-a0da-75d1f3ed15fe&spaceKey=&version=&migration=1&previewPageId=637370373&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy8759968473731017022&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI1ODI1ZDU0NTE4OWU0YTJiMWIxYjRkZjg0YzA2YmQxZjRlNmM2ZWU1MGQyODAzOTFiMTgyY2UxNDRmZWViNTA5IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTk0MiwiaWF0IjoxNjE5NTkxNzYyfQ.CmN-TD8HrgSrAaJxiQBD2ZVMR8HRDTiDjL3TxZZlX9w",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiOGUwY2RmYzYtZjM2ZS00MGZjLTgyNWMtN2U1MzJkYWQ2YmFiIiwiaWQiOiI4ZTBjZGZjNi1mMzZlLTQwZmMtODI1Yy03ZTUzMmRhZDZiYWIifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxNyIsImlkIjoiNjM3MzcwMzczIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjYyLCJpYXQiOjE2MTk1OTE3NjJ9.93Vk4tpsuLjL12VB7xPNHlz7cSsws7Ev2varqfbQedM",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"8e0cdfc6-f36e-40fc-825c-7e532dad6bab\",\"id\":\"8e0cdfc6-f36e-40fc-825c-7e532dad6bab\"},\"content\":{\"type\":\"page\",\"version\":\"17\",\"id\":\"637370373\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"637370373\",\"macro.hash\":\"8e0cdfc6-f36e-40fc-825c-7e532dad6bab\",\"page.type\":\"page\",\": = \| RAW \| = :\":\"imageAttachmentId=att637374638\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=29a876fc-8bf1-4538-a0da-75d1f3ed15fe\|migration=1\|name=PubSub-FetchedDelivery\|diagramAttachmentId=att637374619\|containerId=637370373\|timestamp=1552402221414\",\"space.id\":\"637370369\",\"diagramAttachmentId\":\"att637374619\",\"containerId\":\"637370373\",\"timestamp\":\"1552402221414\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"content.version\":\"17\",\"page.title\":\"General information SIRI\",\"macro.body\":\"\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"17\",\"imageAttachmentId\":\"att637374638\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"29a876fc-8bf1-4538-a0da-75d1f3ed15fe\",\"content.id\":\"637370373\",\"migration\":\"1\",\"name\":\"PubSub-FetchedDelivery\",\"macro.id\":\"8e0cdfc6-f36e-40fc-825c-7e532dad6bab\"}",  
    "timeZone":"Europe/Berlin",  
    "origin":"https://confluence-connect.gliffy.net",  
    "hostOrigin":"https://enturas.atlassian.net",  
    "sandbox":"allow-downloads allow-forms allow-modals allow-popups allow-scripts allow-same-origin allow-top-navigation-by-user-activation allow-storage-access-by-user-activation",    "pearApp":"true",        "apiMigrations": {  
        "gdpr": true  
    }  
}  
;  
    if\(window.AP && window.AP.subCreate\) {  
      window.\_AP.appendConnectAddon\(data\);  
    } else {  
      require\(\['ac/create'\], function\(create\){  
        create.appendConnectAddon\(data\);  
      }\);  
    }  
  }\(\)\);  


### Synchronous <a id="GeneralinformationSIRI-Synchronous"></a>

Explicit fetching of datasets based on service type, time, and possibly more parameters. When disruptions or other errors occur, the fetch attempt should result in predefined error messages.

#### Request/response <a id="GeneralinformationSIRI-Request/response"></a>

The service will be designed to deliver data per request, in accordance with the requestors filtering criteria \(included in the fetch request\).

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy1189091231769801769",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=637370373&pageId=&name=Request-Response&attachmentId=att637374629&pagePin=&imageAttachmentId=att637374646&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=1&previewPageId=637370373&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy1189091231769801769&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJkNmVkZjNmYjA3Mzk5Njg0NzJjNzgwMjAyNjY0NmEyYWZhMjk3MzdkMzllMjA2NGY2OTUyOTljZGE3ZGEwZDdlIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTk0MiwiaWF0IjoxNjE5NTkxNzYyfQ.qKSUFvlUGk5ohmoLQ1bWH-VOISZe14kYMW9agg\_F9s4",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiMjc1YTc4ODctZDA2MS00OWQ3LThmNDctMzgyYjQwZTFiZDQyIiwiaWQiOiIyNzVhNzg4Ny1kMDYxLTQ5ZDctOGY0Ny0zODJiNDBlMWJkNDIifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxNyIsImlkIjoiNjM3MzcwMzczIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjYyLCJpYXQiOjE2MTk1OTE3NjJ9.oadqY1BwLwpQ7ZuQaNpLB12o9eJRFdhCCEge-m5ge0I",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"275a7887-d061-49d7-8f47-382b40e1bd42\",\"id\":\"275a7887-d061-49d7-8f47-382b40e1bd42\"},\"content\":{\"type\":\"page\",\"version\":\"17\",\"id\":\"637370373\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"637370373\",\"macro.hash\":\"275a7887-d061-49d7-8f47-382b40e1bd42\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"17\",\"page.title\":\"General information SIRI\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637374646\|baseUrl=https://enturas.atlassian.net/wiki\|migration=1\|name=Request-Response\|diagramAttachmentId=att637374629\|containerId=637370373\|timestamp=1552402252751\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"17\",\"imageAttachmentId\":\"att637374646\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"637370373\",\"migration\":\"1\",\"name\":\"Request-Response\",\"macro.id\":\"275a7887-d061-49d7-8f47-382b40e1bd42\",\"diagramAttachmentId\":\"att637374629\",\"containerId\":\"637370373\",\"timestamp\":\"1552402252751\"}",  
    "timeZone":"Europe/Berlin",  
    "origin":"https://confluence-connect.gliffy.net",  
    "hostOrigin":"https://enturas.atlassian.net",  
    "sandbox":"allow-downloads allow-forms allow-modals allow-popups allow-scripts allow-same-origin allow-top-navigation-by-user-activation allow-storage-access-by-user-activation",    "pearApp":"true",        "apiMigrations": {  
        "gdpr": true  
    }  
}  
;  
    if\(window.AP && window.AP.subCreate\) {  
      window.\_AP.appendConnectAddon\(data\);  
    } else {  
      require\(\['ac/create'\], function\(create\){  
        create.appendConnectAddon\(data\);  
      }\);  
    }  
  }\(\)\);  


### General requirements <a id="GeneralinformationSIRI-Generalrequirements"></a>

It is expected that normal data deliveries will contain updates/changes since the most recent push/request. If new messages also contain previously delivered messages, mechanisms must be implemented in the exchange protocol to prevent duplication or other corrupting issues.

#### Standard values <a id="GeneralinformationSIRI-Standardvalues"></a>

All fields used when setting up a data stream, or when calling the services, are expected to have meaningful values, defaults and to be in accordance with request-parameters. For example:

* The time interval of fetched data
* Filtering
* Change-before-update

#### Data correctness <a id="GeneralinformationSIRI-Datacorrectness"></a>

Data providers must make appropriate effort to ensure that the data is correct and valid, both technically and in the sense that the content is meaningful. For example:

* Data content must comply with requirements stipulated in this profile
* Data should be semantically appropriate and interpretable by consumers
* Even in cases when technically not prohibited, e.g. due to an option between data types, empty data should still not be submitted
* Published real-time information should contain genuine updates of the message content
* Test or dummy data - or other inapplicable data such as placeholders, ficticious values, content out of scope/bounds or for other reasons being without relevant informational value - must not be published in production environments

#### Data completeness <a id="GeneralinformationSIRI-Datacompleteness"></a>

The real-time information builds upon static and planned data as described in the [Nordic NeTEx Profile](handbok-n801-siri-netex-nordic-netex-profile.md), which the SIRI data is supporting, enriching or replacing. Which is described in detail where relevant throughout this profile document.

However, the real-time data should in itself be be complete and contain all necessary information within the XML file, without depending on content from other SIRI files or external SIRI data streams to provide meaningful content.

#### Data content <a id="GeneralinformationSIRI-Datacontent"></a>

The data stream will be delivered in accordance with specified input-parameters \(i.e. filtered / reduced accordingly\). Likewise, it is expected that when no input-parameters are present, a full dataset is requested.

#### Data freshness <a id="GeneralinformationSIRI-Datafreshness"></a>

It is expected that new messages are published as soon as feasible after the source data has been changed. For example:

* Changes in stops \(EstimatedCall → RecordedCall\)
* Quay to be used has been determined or changed
* Adjustments in estimated arrivals or departures

## Common components <a id="GeneralinformationSIRI-Commoncomponents"></a>

This chapter describes the generic concept used for exchanging real-time information in accordance with the Norwegian SIRI profile. 

### Message objects <a id="GeneralinformationSIRI-Messageobjects"></a>

#### ServiceDelivery <a id="GeneralinformationSIRI-ServiceDelivery"></a>

Container for _SIRI Functional Service delivery_

Norwegian SIRI profile supports:

* [EstimatedTimetableDelivery](handbok-n801-siri-netex-siri-et.md) \(_SIRI-ET_\)
* [SituationExchangeDelivery](handbok-n801-siri-netex-siri-sx.md) \(_SIRI-SX_\)
* [VehicleMonitoringDelivery](handbok-n801-siri-netex-siri-vm.md) \(_SIRI-VM_\)

| ServiceDelivery |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | ResponseTimestamp | xsd:dateTime | 1: 1 | Time when the dataset was generated/published. |
| element | ProducerRef | xsd:NMTOKEN | 1: 1 | Codespace for dataset producer. |
| \(choice\) element | EstimatedTimetableDelivery | EstimatedTimetableDeliveryStructure | 1: 1 | Data element for Estimated Timetable \(SIRI-ET\), with changes in one or more planned  _VehicleJourneys_ within the same operating day. |
| SituationExchangeDelivery | SituationExchangeDeliveryStructure | Data element for Situation Exchange \(SIRI-SX\), with information regarding one or more situations \(or updates to previously published situations\). |  |  |
| VehicleMonitoringDelivery | VehicleMonitoringDeliveryStructure | Data element for Vehicle Monitoring \(SIRI-VM\), with monitoring information for one or more _VehicleJourneys_ \(for estimated adjustments of time table information\) |  |  |

### Data types <a id="GeneralinformationSIRI-Datatypes"></a>

#### NaturalLanguageStringStructure <a id="GeneralinformationSIRI-NaturalLanguageStringStructure"></a>

Text strings with an assigned language code.

<table>
  <thead>
    <tr>
      <th style="text-align:left">NaturalLanguageStringStructure</th>
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
      <td style="text-align:left">xml:lang</td>
      <td style="text-align:left">xsd:string</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The language used must be defined as a <b>three-letter code</b> according
          to<code> ISO 639-3</code> (<em>recommended</em>) or as a <b>two-letter code</b> according
          to<code> ISO 639-1 / RFC 1766</code>.</p>
        <p><em>Interpreted as the default &quot;NOR&quot; unless otherwise specified. This <b>must</b> be specified when the message language is other than the default.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">(element content)</td>
      <td style="text-align:left">xsd:string (<em>non-empty</em>)</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">The message text.</td>
    </tr>
  </tbody>
</table>

#### NaturalLanguagePlaceNameStructure <a id="GeneralinformationSIRI-NaturalLanguagePlaceNameStructure"></a>

Text strings with an assigned language code.

<table>
  <thead>
    <tr>
      <th style="text-align:left">NaturalLanguagePlaceNameStructure</th>
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
      <td style="text-align:left">xml:lang</td>
      <td style="text-align:left">xsd:string</td>
      <td style="text-align:left">0: 1</td>
      <td style="text-align:left">
        <p>The language used must be defined as a <b>three-letter code</b> according
          to<code> ISO 639-3</code> (<em>recommended</em>) or as a <b>two-letter code</b> according
          to<code> ISO 639-1 / RFC 1766</code>.</p>
        <p><em>Interpreted as the default &quot;NOR&quot; unless otherwise specified. This <b>must</b> be specified when the message language is other than the default.</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">element</td>
      <td style="text-align:left">(element content)</td>
      <td style="text-align:left">xsd:string (<em>non-empty</em>)</td>
      <td style="text-align:left">1: 1</td>
      <td style="text-align:left">The message text</td>
    </tr>
  </tbody>
</table>

#### FramedVehicleJourneyRefStructure  <a id="GeneralinformationSIRI-FramedVehicleJourneyRefStructure"></a>

Reference objects for _DatedVehicleJourneyRef_ with a specified _DatedFrameRef_ \(date\), in order to ensure that _VehicleJourney_ objects with the same ID can be separated based on their dates.

| FramedVehicleJourneyRefStructure |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| element | DataFrameRef | xsd:NMTOKEN | 1: 1 | Date must have the ISO-format \(YYY-MM-DD\) for the departure in question. Must be in local time. |
| element | DatedVehicleJourneyRef | xsd:NMTOKEN | 1: 1 | ID for the related _VehicleJourney_ \(must be the same as the ID of the corresponding _VehicleJourney_ in the NeTEx dataset\). |

