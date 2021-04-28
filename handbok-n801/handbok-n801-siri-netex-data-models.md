# Håndbok N801 \(SIRI/NeTEX\) : Data models

## Content <a id="Datamodels-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591648069 {padding: 0px;}  
div.rbtoc1619591648069 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591648069 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Content](handbok-n801-siri-netex-data-models.md#Datamodels-Content)
* [Context](handbok-n801-siri-netex-data-models.md#Datamodels-Context)
  * [Disclaimer](handbok-n801-siri-netex-data-models.md#Datamodels-Disclaimer)
* [Framework](handbok-n801-siri-netex-data-models.md#Datamodels-Framework)
  * [Location](handbok-n801-siri-netex-data-models.md#Datamodels-Location)
    * [NeTEx data model for location objects](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforlocationobjects)
  * [Organisation](handbok-n801-siri-netex-data-models.md#Datamodels-Organisation)
    * [NeTEx data model for organisation](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelfororganisation)
  * [Validity](handbok-n801-siri-netex-data-models.md#Datamodels-Validity)
    * [NeTEx data model for validity](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforvalidity)
  * [Messages/footnotes](handbok-n801-siri-netex-data-models.md#Datamodels-Messages/footnotes)
    * [NeTEx data model for messages](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelformessages)
* [Stops](handbok-n801-siri-netex-data-models.md#Datamodels-Stops)
  * [StopPlace](handbok-n801-siri-netex-data-models.md#Datamodels-StopPlace)
    * [NeTEx data model for stop place](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforstopplace)
  * [Monomodal StopPlace](handbok-n801-siri-netex-data-models.md#Datamodels-MonomodalStopPlace)
  * [Quay](handbok-n801-siri-netex-data-models.md#Datamodels-Quay)
  * [Multimodal StopPlace](handbok-n801-siri-netex-data-models.md#Datamodels-MultimodalStopPlace)
  * [Group Of StopPlaces](handbok-n801-siri-netex-data-models.md#Datamodels-GroupOfStopPlaces)
  * [FlexibleStopPlace](handbok-n801-siri-netex-data-models.md#Datamodels-FlexibleStopPlace)
    * [NeTEx data model for a flexible stop place](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforaflexiblestopplace)
* [Equipment](handbok-n801-siri-netex-data-models.md#Datamodels-Equipment)
  * [Facility](handbok-n801-siri-netex-data-models.md#Datamodels-Facility)
  * [Equipment](handbok-n801-siri-netex-data-models.md#Datamodels-Equipment.1)
* [Transport networks](handbok-n801-siri-netex-data-models.md#Datamodels-Transportnetworks)
  * [Network](handbok-n801-siri-netex-data-models.md#Datamodels-Network)
    * [NeTEx data model for network](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelfornetwork)
    * [Conceptual NeTEx model for network](handbok-n801-siri-netex-data-models.md#Datamodels-ConceptualNeTExmodelfornetwork)
  * [Route](handbok-n801-siri-netex-data-models.md#Datamodels-Route)
  * [Journey Pattern](handbok-n801-siri-netex-data-models.md#Datamodels-JourneyPattern)
    * [NeTEx data model for JourneyPattern](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforJourneyPattern)
    * [NeTEx overall conceptual model for JourneyPattern](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExoverallconceptualmodelforJourneyPattern)
    * [NeTEx detailed conceptual model for JourneyPattern](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdetailedconceptualmodelforJourneyPattern)
  * [Flexible transportation](handbok-n801-siri-netex-data-models.md#Datamodels-Flexibletransportation)
    * [NeTEx data model for flexible transport](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforflexibletransport)
  * [Transfers and Interchanges](handbok-n801-siri-netex-data-models.md#Datamodels-TransfersandInterchanges)
    * [NeTEx data model for interchange](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforinterchange)
* [NeTEx timetable data representation](handbok-n801-siri-netex-data-models.md#Datamodels-timetabledataNeTExtimetabledatarepresentation)
  * * [NeTEx data model for calendar](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforcalendar)
  * [Timetable](handbok-n801-siri-netex-data-models.md#Datamodels-Timetable)
    * [NeTEx data model for Vehicle Journey](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExdatamodelforVehicleJourney)
    * [NeTEx conceptual model for ServiceJourney](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExconceptualmodelforServiceJourney)
    * [NeTEx conceptual model for DatedServiceJourney](handbok-n801-siri-netex-data-models.md#Datamodels-NeTExconceptualmodelforDatedServiceJourney)
  * [Deviations](handbok-n801-siri-netex-data-models.md#Datamodels-Deviations)
  * [Data enrichment](handbok-n801-siri-netex-data-models.md#Datamodels-Dataenrichment)
    * [Conceptual model for enrichment of data in NeTEx](handbok-n801-siri-netex-data-models.md#Datamodels-ConceptualmodelforenrichmentofdatainNeTEx)

  
This document contains additional information for the Nordic NeTEx profile, including overall data models and conceptual descriptions of how the elements from NeTEx will be used.

## Context <a id="Datamodels-Context"></a>

Transmodel \(European Standard “Public Transport Reference Data Model”, [http://www.transmodel-cen.eu](http://www.transmodel-cen.eu)\) is the reference model and framework, used to define the Norwegian data model for exchanging public transport information, respectively, NeTEx \(Network Timetable Exchange, [http://netex-cen.eu/](http://netex-cen.eu/)\) for stop places, timetable data and SIRI \(Service Interface for Real-time information, [https://www.vdv.de/siri.aspx](https://www.vdv.de/siri.aspx)\). 

Both data models are implemented as XML and defined in respective XML Schemas \(XSD\). Further requirements for using the exchange formats are specified in Norwegian profiles for NeTEx and SIRI. 

The framework's implementations form the basis of the services offered for national public transport data in the Nordic countries:

#### Disclaimer <a id="Datamodels-Disclaimer"></a>

This document presents high-level technical views of various data models models and conceptual models utilised in the Nordic NeTEx profile. The models are intentionally created with viewpoints reflecting generic, and highly simplified, key features of the Nordic NeTEx profile as well as the NeTEx standard in general, and do neither fully comply with the UML modeling language nor take into account all aspects of the NeTEx standard.

For full feature technical models, please see the [Model documents and UML Diagrams](http://netex-cen.eu/?page_id=11) at the [CEN NeTEx website](http://netex-cen.eu/).

## Framework <a id="Datamodels-Framework"></a>

### Location <a id="Datamodels-Location"></a>

One point \([Point](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Point)\) is a node in the network with a specified location \([Location](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Location)\). It can be a stop place, Point of Interest \(POI\) or a ticket control point at a station. The point can be used to specify a larger unit - e.g. an area, using projection \([Point Projection](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-PointProjection)\). A point can also be used for the definition of a leg, e.g. to describe the actual path between two stop places. A leg can be described by using a link \([Link](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Link)\).

To define a larger area, \(e.g. Tariff Zone\) use the [Zone ](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Zone)objects, which contain different points, and can also be projected onto a map using [ZoneProjection](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-ZoneProjection).

**NeTEx data model for location objects**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy6018665574142295042",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-point-zone&attachmentId=att637372668&pagePin=&imageAttachmentId=att637372678&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy6018665574142295042&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJhYjIyOWFmYzRlNzFkODkwNjk4ZTU4YjA1OWQ4MzMxMTgyZmUzNjQwMWE4M2RmNmEzYTc2MjYxOWE3MjJjMmQyIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.nJn0DJlOeW2qQtdQ1FDxOAw5aKGAqG-o81pMHG\_62DM",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZTViOGE4YTMtOTk0Zi00ZTA2LWFhNjUtMTZmYzcxZmFjNDlkIiwiaWQiOiJlNWI4YThhMy05OTRmLTRlMDYtYWE2NS0xNmZjNzFmYWM0OWQifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.PtPSeh-aR1qOBPNCQYhuxW7kSUD9XSLy-5hwBwCXm98",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"e5b8a8a3-994f-4e06-aa65-16fc71fac49d\",\"id\":\"e5b8a8a3-994f-4e06-aa65-16fc71fac49d\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"e5b8a8a3-994f-4e06-aa65-16fc71fac49d\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372678\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-point-zone\|diagramAttachmentId=att637372668\|containerId=637370438\|timestamp=1535549536841\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372678\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-point-zone\",\"macro.id\":\"e5b8a8a3-994f-4e06-aa65-16fc71fac49d\",\"diagramAttachmentId\":\"att637372668\",\"containerId\":\"637370438\",\"timestamp\":\"1535549536841\"}",  
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


### Organisation <a id="Datamodels-Organisation"></a>

If you need to describe the organisational structure, you have a selection of several objects:

* Organisation may be either the [Authority](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Authority) entity \(responsible for providing public transport services\), or the [Operator ](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Operator)company fulfilling the physical public transport role. Operators can be further grouped into [GroupOfOperators](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-GroupOfOperators) if necessary.
* Organisations can be divided into departments \([Department](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Department)\) to better reflect their structure.
* Each organisation has contact information and postal address.
* A unique area of responsibility \([Responsibility Set](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-ResposibilitySet)\) can be assigned to an organisation to specify the parts of the dataset it represents.

**NeTEx data model for organisation**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy5448210057835097813",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-organisation&attachmentId=att637372648&pagePin=&imageAttachmentId=att637372644&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy5448210057835097813&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI5MmVlMDVlZDc0YjQzYjc0NmU3NmQyN2NkY2I3NTJjOThlMWVlZDE0NmZjZWZkNzcxYTJmZWJlOGU3NGVjNGIzIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.pBACi\_5bUigQW\_ovaER1Til2n6dEmlc5yUuibLooEAA",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiN2ZlNTk1MzgtNGJmNy00ZjNkLWI5ZTktYWRlMTI5NjhhYzNjIiwiaWQiOiI3ZmU1OTUzOC00YmY3LTRmM2QtYjllOS1hZGUxMjk2OGFjM2MifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.SFNc2QXsXBoChswwj4q\_xNfNfdxBVoKW86H-SFAO-3A",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"7fe59538-4bf7-4f3d-b9e9-ade12968ac3c\",\"id\":\"7fe59538-4bf7-4f3d-b9e9-ade12968ac3c\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"7fe59538-4bf7-4f3d-b9e9-ade12968ac3c\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372644\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-organisation\|diagramAttachmentId=att637372648\|containerId=637370438\|timestamp=1535617100578\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372644\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-organisation\",\"macro.id\":\"7fe59538-4bf7-4f3d-b9e9-ade12968ac3c\",\"diagramAttachmentId\":\"att637372648\",\"containerId\":\"637370438\",\"timestamp\":\"1535617100578\"}",  
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


### Validity <a id="Datamodels-Validity"></a>

Every single object in NeTEx can be versioned which allows changes without affecting unchanged data. A version of an object is tied to a validity description \([Validity Condition](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-ValidityCondition)\) which specifies when the definition takes effect.

Validity Condition has two specializations:

* Trigger \([Validity Trigger](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-ValidityTrigger)\) which allows long-term changes to be specified \(e.g. the stop is moved during a period of flooding, or while there is a sports event\). The trigger initiates the change.
* [AvailabilityCondition](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-AvailabilityCondition) used to describe temporary conditions with precisely specified dates.

**NeTEx data model for validity**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy7819057532865053249",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-validity&attachmentId=att637372646&pagePin=&imageAttachmentId=att637372654&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy7819057532865053249&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIyZThkZWQ4N2ZkM2U5OThjMGU1OGJiMTllOGY2ZmNlZjRkZjk3YThlZjFiZDhkNjJlMGQ5OGIzZTYyOTg4ODk1IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.ixGflUUVQR-OMoHfkZl4\_FMFPwgC29M5v7CV839BTUs",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiMWZkMDkxNTAtZDYxZS00NjU3LTkwZjQtZjY4YmI2YTE5Yzk1IiwiaWQiOiIxZmQwOTE1MC1kNjFlLTQ2NTctOTBmNC1mNjhiYjZhMTljOTUifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.tdVJHz3sqJ7g4YhqrB86t4Bcl7G3v4AMGE8BNbZWyFM",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"1fd09150-d61e-4657-90f4-f68bb6a19c95\",\"id\":\"1fd09150-d61e-4657-90f4-f68bb6a19c95\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"1fd09150-d61e-4657-90f4-f68bb6a19c95\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372654\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-validity\|diagramAttachmentId=att637372646\|containerId=637370438\|timestamp=1535617163943\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372654\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-validity\",\"macro.id\":\"1fd09150-d61e-4657-90f4-f68bb6a19c95\",\"diagramAttachmentId\":\"att637372646\",\"containerId\":\"637370438\",\"timestamp\":\"1535617163943\"}",  
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


### Messages/footnotes <a id="Datamodels-Messages/footnotes"></a>

Delivering messages to customers is essential when there are deviations or special circumstances for a service. Messages are created using [Notice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Notice) objects \(free text messages\) and assigned to different objects using a [NoticeAssignment](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-NoticeAssignment), e.g. for a single journey \([VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-VehicleJourney)\) or a route with a specific [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-JourneyPattern). Notices can be delivered in different variations depending on the media it is meant to be displayed on, e.g. a short message for the information screen at the bus stop, a longer message for mobile devices, and an expanded message for website presentation. This is handled by using [DeliveryVariant](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-DeliveryVariant).

**NeTEx data model for messages**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy4872672226036363130",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-notice&attachmentId=att637372655&pagePin=&imageAttachmentId=att637372649&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy4872672226036363130&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI2NmIxNTBmOGE4MjJmMDBmMjIwMDM3YTA1M2ZlOThlM2U3MzJiN2FmYWI2YWJhY2VmYWFkNzQzN2ZhYTRjMjdkIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.bC7tjz6fMH8-MlWvdjD6HemltFm07g9OLD1yGJ1wjOo",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiNmMyYzYwODMtZTFkZi00ODMyLWExNWQtMDEzMTBiNzJiNDAzIiwiaWQiOiI2YzJjNjA4My1lMWRmLTQ4MzItYTE1ZC0wMTMxMGI3MmI0MDMifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.iowF0NKHMYJA42rjK2P20d\_Zp8HPny11H-c3CxhVqH0",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"6c2c6083-e1df-4832-a15d-01310b72b403\",\"id\":\"6c2c6083-e1df-4832-a15d-01310b72b403\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"6c2c6083-e1df-4832-a15d-01310b72b403\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372649\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-notice\|diagramAttachmentId=att637372655\|containerId=637370438\|timestamp=1535617291366\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372649\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-notice\",\"macro.id\":\"6c2c6083-e1df-4832-a15d-01310b72b403\",\"diagramAttachmentId\":\"att637372655\",\"containerId\":\"637370438\",\"timestamp\":\"1535617291366\"}",  
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


## Stops <a id="Datamodels-Stops"></a>

### StopPlace <a id="Datamodels-StopPlace"></a>

A stop point \([StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace)\) is a special type of site \([Site](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Site)\) normally located in a [Tariff Zone](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-TariffZone). As a [Site](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx), a [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) can have multiple- [Parking](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Parking)s, [Levels](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Level) \(each one with its own [Entrance](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Entrance)\), and accessibility [Equipment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Equipment). In addition, a [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) is divided into subordinate [Quays](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Quay) \(and below the Quay, [Boarding Positions](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-BoardingPosition)\). Each [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) can also have waiting areas \([Access Space](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-AccessSpace)\) and footpaths \([NavigationPath](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-NavigationPath)\).

The structure of stop places is subject to variation. It can be anything from a simple kerb stop, to the most complex transport hubs. The following structure should be used to describe a stop place:

* A [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) always has at least one [Quay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Quay).
* A [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) may have [AccessSpaces](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-AccessSpace).
* A [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) may have a parent [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) \(maximum 1 level of nesting\).
* Two or more StopPlaces, including parent StopPlaces, can be grouped into a [GroupOfStopPlaces](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-GroupOfStopPlaces).
* A [Quay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Quay) can have [BoardingPositions](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-BoardingPositions) \(_usually only relevant to trains_\).

**NeTEx data model for stop place**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy3976807048313486368",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-stopplace&attachmentId=att637372696&pagePin=&imageAttachmentId=att637372695&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy3976807048313486368&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJjMzA1M2FkZTAwMzAyNWI4MWY4NTdlN2M5OTVlZGVkMmI2ZGQ4ODU4OTAyYThlM2VkYmE1YjQ3N2M5NWZiYTkzIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.avu5q0h9Yhphj6W4f3-djlUmHAxB5b-vUE66eLavaTQ",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZjM0N2MzYjctY2QwZi00ZDI1LWE1YWEtZjhiNjk3MjBkNDFkIiwiaWQiOiJmMzQ3YzNiNy1jZDBmLTRkMjUtYTVhYS1mOGI2OTcyMGQ0MWQifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.SnCMreLrHzQQKAaiv0GrzkxcrC7jI-evnP-pWnB1iLc",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"f347c3b7-cd0f-4d25-a5aa-f8b69720d41d\",\"id\":\"f347c3b7-cd0f-4d25-a5aa-f8b69720d41d\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"f347c3b7-cd0f-4d25-a5aa-f8b69720d41d\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372695\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-stopplace\|diagramAttachmentId=att637372696\|containerId=637370438\|timestamp=1535617507892\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372695\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-stopplace\",\"macro.id\":\"f347c3b7-cd0f-4d25-a5aa-f8b69720d41d\",\"diagramAttachmentId\":\"att637372696\",\"containerId\":\"637370438\",\"timestamp\":\"1535617507892\"}",  
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


Stop places have three distinct levels of structure:

1. StopPlace used by one transport type. This is **MonomodalStopPlace**.
2. StopPlace used by several transport types, e.g. bus and tram. This is **MultimodalStopPlace**.
3. A combination of several StopPlace in direct proximity to each other, e.g. bus and tram next to a metro station. This is **GroupOfStopPlaces**.

Note that [Quays](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Quay) on a [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) must be _monomodal_ \(only for one transport type\). If a [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) is _multimodal_ \(for multiple transport types\), this should always be modelled as a parent [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) consisting of one [StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-StopPlace) \(with monomodal [Quays](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Quay)\) per transport type, even when the transport types use the exact same position for stops. It is possible to link StopPlaces which share a common position \(one straddling the other, or exact same positions\) using AdjacentSites, which can be useful when presenting multimodal stops on a map.

Please note that it is **not** a requirement that _both_ stops belonging to a parent stop \(Multimodal StopPlace\) have different transport types.

### Monomodal StopPlace <a id="Datamodels-MonomodalStopPlace"></a>

A MonomodalStopPlace is a simple stop place consisting of one or more [Quays](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Quay). This type of stop place can only be served by one type of transport, for example bus lines.

The following rules apply to MonomodalStopPlace:

1. A monomodal StopPlace cannot have any subordinate StopPlace.
2. A monomodal StopPlace must at least have one Quay. 
3. A Quay can belong to only one monomodal stop place.
4. A monomodal StopPlace can have one parent StopPlace.

### Quay <a id="Datamodels-Quay"></a>

A [Quay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx) is an exact location where vehicles stop and travellers board, or alight. 

For train platforms, the [Quay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-Quay) can be divided into [BoardingPositions](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-BoardingPostition) if applicable. A [BoardingPosition](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-BoardingPosition) specifies exactly where on the platform a passenger should wait for the train, for example, comfort class car. 

The following rules apply to Quay:

1. A transfer is implicit within the same Quay.
2. Quay inherits the name of its parent StopPlace

### Multimodal StopPlace <a id="Datamodels-MultimodalStopPlace"></a>

A MultimodalStopPlace is a StopPlace, which serves more than one transport type. The multimodal StopPlace is the structural parent StopPlace, and it has at least two subordinate monomodal StopPlace.

Please note that it is **not** a requirement that _both_ stops belonging to a parent stop \(Multimodal StopPlace\) have different transport types.

The following rules apply to Multimodal StopPlace:

1. Has no Quays directly tied to it.
2. Has no parent StopPlaces \(only 1 level of nesting allowed\).

### Group Of StopPlaces <a id="Datamodels-GroupOfStopPlaces"></a>

[GroupOfStopPlaces](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-GroupOfStopPlaces) should be used when there is a need to group several mono- and/or multimodal stop places in order to refer to them simultaneously, usually to describe a larger and more complex StopPlace area, such as a hub or a town centre. 

### FlexibleStopPlace <a id="Datamodels-FlexibleStopPlace"></a>

An on-demand service, or flexible line, often deviates from the static bus stops, instead, a flexible stop place can be used:

A [FlexibleStopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#GenerellinformasjonNeTEx-FlexibleStopPlace), does not have a specific position, but rather a defined area, within which the flexible transport picks up, or drops off passengers depending on bookings, or other beforehand arrangements. This includes for example address to address journeys, hail and ride concepts, or combinations thereof.

**NeTEx data model for a flexible stop place**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy7695723847124335546",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-flexiblestopplace&attachmentId=att637372746&pagePin=&imageAttachmentId=att637372753&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy7695723847124335546&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIwOWRhNDE0YmY1NGYwZmQxODI2NWJlMTdhY2MzNWU0MDI1MzM4ZGJiYTg0MzljNjliNDAxMmY5YzQ3ZDk1OWU1IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.QkCORziRTNp9dsdaGMB0imoj1wwNiyUBDIdLW6OoXSk",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYjJlMmZlOTktNjYyOC00MjdmLWFmYjItNTJlMzA1MDg0NDJmIiwiaWQiOiJiMmUyZmU5OS02NjI4LTQyN2YtYWZiMi01MmUzMDUwODQ0MmYifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.JIpOIYRukT1o7n3IqPeu4\_izurKqss0UGZsxVKeSNj4",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"b2e2fe99-6628-427f-afb2-52e30508442f\",\"id\":\"b2e2fe99-6628-427f-afb2-52e30508442f\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"b2e2fe99-6628-427f-afb2-52e30508442f\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372753\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-flexiblestopplace\|diagramAttachmentId=att637372746\|containerId=637370438\|timestamp=1535617734214\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372753\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-flexiblestopplace\",\"macro.id\":\"b2e2fe99-6628-427f-afb2-52e30508442f\",\"diagramAttachmentId\":\"att637372746\",\"containerId\":\"637370438\",\"timestamp\":\"1535617734214\"}",  
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


## Equipment <a id="Datamodels-Equipment"></a>

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy5204860332869209809",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=equipment-facility&attachmentId=att637375299&pagePin=&imageAttachmentId=att637375308&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy5204860332869209809&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJkODlmYjg2OTRkYjY5ZmI4YWU5YmRmMTUzZWIzMzYxZjdmYjM2NDQzMjlmZWU5NGZkZTc3ZWIyYTZhZDVmZTBhIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.1r2ciy7WFruVFDUUN0UirMNqmAf54Y3oxXVdrWR0Kww",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiNGE2ZmYyMzYtMDJlYS00YTc0LTk5ZTEtN2IyZDhiMjAwYzcyIiwiaWQiOiI0YTZmZjIzNi0wMmVhLTRhNzQtOTllMS03YjJkOGIyMDBjNzIifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.HExUWBkj\_fYg\_2I6-5P5uuvTXoKfMspbVioVVnRYzKA",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"4a6ff236-02ea-4a74-99e1-7b2d8b200c72\",\"id\":\"4a6ff236-02ea-4a74-99e1-7b2d8b200c72\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"4a6ff236-02ea-4a74-99e1-7b2d8b200c72\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637375308\|baseUrl=https://enturas.atlassian.net/wiki\|name=equipment-facility\|diagramAttachmentId=att637375299\|containerId=637370438\|timestamp=1535617817731\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637375308\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"equipment-facility\",\"macro.id\":\"4a6ff236-02ea-4a74-99e1-7b2d8b200c72\",\"diagramAttachmentId\":\"att637375299\",\"containerId\":\"637370438\",\"timestamp\":\"1535617817731\"}",  
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


### Facility <a id="Datamodels-Facility"></a>

These are standardized lists describing available facilities which can be grouped into \(reusable\) [FacilitySets](http://framework#framework-FacilitySet). These are then used on relevant entities. 

### Equipment <a id="Datamodels-Equipment.1"></a>

In order to describe the availability and usage of the _Facilities_, use the categories [Equipment]() and [EquipmentTypes]() \(including [LocalService](http://framework#framework-LocalService)\) to describe for example the placement of the equipment.

_Equipment normally has one **or more**_ [_FacilitySets_](http://framework#framework-FacilitySet)_._

## Transport networks <a id="Datamodels-Transportnetworks"></a>

### Network <a id="Datamodels-Network"></a>

A network consists mainly of Line, Route and RoutePoints. To model them into the network, NeTEx uses the following structure:

* A [Network](http://Generell+informasjon+NeTEx#Generellinformasjon-Network) consists of several lines [Lines](http://Generell+informasjon+NeTEx#Generellinformasjon-Line). 
* Each line is operated by an [Operator](http://Generell+informasjon+NeTEx#Generellinformasjon-Operator) and has one or more [Routes](http://Generell+informasjon+NeTEx#Generellinformasjon-Route) associated with it. 
* A [Route](http://Generell+informasjon+NeTEx#Generellinformasjon-Route) shows the overall physical route of a [Network](http://Generell+informasjon+NeTEx#Generellinformasjon-Network) and consists of several [RoutePoints](http://Generell+informasjon+NeTEx#Generellinformasjon-RoutePoint).  
  * Note that a RoutePoint isn't necessarily a __[StopPlace](http://Generell+informasjon+NeTEx#Generellinformasjon-StopPlace).
* In order for it to be possible to reuse the same route points across multiple routes, [RoutePoint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-RoutePoint) objects are linked to the Route using the "intermediate object" [PointOnRoute](http://Generell+informasjon+NeTEx#Generellinformasjon-PointOnRoute) \(_see the diagram below_\).

**NeTEx data model for network**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy6719754813876193768",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-route&attachmentId=att637372734&pagePin=&imageAttachmentId=att637372733&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy6719754813876193768&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJiMWNhNDYyMTU4ZDIyNTdhNTM2ZWZiNzRiZjExYTViNmU2ZWZmNDg4Nzc2YjBkZmQyNDk0NGY1MDE4M2NkMGYwIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.EHsvD5OlIKEw7dPvsPXybnqbGAMotU\_ZkH7jJTsO\_vM",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZmVjMDUzNTEtNWRjMC00OTIyLTg0MDItNmEyNzZmN2Q5YmE5IiwiaWQiOiJmZWMwNTM1MS01ZGMwLTQ5MjItODQwMi02YTI3NmY3ZDliYTkifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.3oLB3rHRZEbDHq0cPxDXnn7DzF6mRCV7OvRE55AKiVA",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"fec05351-5dc0-4922-8402-6a276f7d9ba9\",\"id\":\"fec05351-5dc0-4922-8402-6a276f7d9ba9\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"fec05351-5dc0-4922-8402-6a276f7d9ba9\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372733\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-route\|diagramAttachmentId=att637372734\|containerId=637370438\|timestamp=1535618001884\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372733\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-route\",\"macro.id\":\"fec05351-5dc0-4922-8402-6a276f7d9ba9\",\"diagramAttachmentId\":\"att637372734\",\"containerId\":\"637370438\",\"timestamp\":\"1535618001884\"}",  
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


[Lines](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Line) are grouped into a conceptual [Network](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Network). The Lines are described as a set of [Routes](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route) with [RoutePoints](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-RoutePoint). 

**Conceptual NeTEx model for network**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy3194478758736637046",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=network-concept&attachmentId=att728563853&pagePin=&imageAttachmentId=att728596627&border=&chrome=&html5=&size=&ceoId=&macroId=a577e4f9-60cf-4540-a5c9-f6e3c57cf007&spaceKey=&version=&migration=&previewPageId=728596522&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy3194478758736637046&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIyYmZkY2ZhNDNlYTM0Y2I3YmE4MzQ1ZTc1ZGI2MDlhOTYxODgwOTI4NGQ2NzAzMmMyZjhlOGNmMjFhYmY0NjliIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.ObX3P07RWQxXvymgN5nQtsZTvhxD\_1tQ4bY-iAlJFds",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZWVmM2I3ZDUtNTE0Ny00M2Q1LWE2ZDgtMjJiYWFiYWMzNjY1IiwiaWQiOiJlZWYzYjdkNS01MTQ3LTQzZDUtYTZkOC0yMmJhYWJhYzM2NjUifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.ZG6KAomXBUJND4F-CRS9az62Im6dG-L88nWn1oC9AKE",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"eef3b7d5-5147-43d5-a6d8-22baabac3665\",\"id\":\"eef3b7d5-5147-43d5-a6d8-22baabac3665\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"eef3b7d5-5147-43d5-a6d8-22baabac3665\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728596627\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=a577e4f9-60cf-4540-a5c9-f6e3c57cf007\|name=network-concept\|diagramAttachmentId=att728563853\|containerId=728596522\|timestamp=1549869906087\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att728596627\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"a577e4f9-60cf-4540-a5c9-f6e3c57cf007\",\"content.id\":\"728596522\",\"name\":\"network-concept\",\"macro.id\":\"eef3b7d5-5147-43d5-a6d8-22baabac3665\",\"diagramAttachmentId\":\"att728563853\",\"containerId\":\"728596522\",\"timestamp\":\"1549869906087\"}",  
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


Generally speaking, a [Route](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route) represents the structure of a network, though the [RoutePoints](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-RoutePoint) do not infer _how_ the network is traversed. This however, is defined by describing a given order of [PointOnRoute](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-PointOnRoute) as a [_pointsInSequence_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-PointInJourneyPattern).

This can be illustrated by the following example: _RoutePoint vs. PointOnRoute_:  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy7912733873687328098",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=RoutePoint-vs-PointOnRoute&attachmentId=att637372736&pagePin=&imageAttachmentId=att637372735&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy7912733873687328098&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIxZThhZGI4ODEyMzQ1NGViYzg4YWJjYWRhNmE4NTYxOTQ4ODM2Y2M0MWU3OWQ2MDBjNjgzMjk5YjFjYzU0Y2E0IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.yYpRwzIb052ih6mYGGrK4wCkrakG4jmc4IQrCzwHzBQ",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYjM2ZWQxOGUtMTk2ZS00M2UwLWJiZTEtMjY4NTkzYTQ4MmYxIiwiaWQiOiJiMzZlZDE4ZS0xOTZlLTQzZTAtYmJlMS0yNjg1OTNhNDgyZjEifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.DanvUqqoK5nXHxNRYKmPEfEeWhwmGTePFNhUnEcPrHg",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"b36ed18e-196e-43e0-bbe1-268593a482f1\",\"id\":\"b36ed18e-196e-43e0-bbe1-268593a482f1\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"b36ed18e-196e-43e0-bbe1-268593a482f1\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372735\|baseUrl=https://enturas.atlassian.net/wiki\|name=RoutePoint-vs-PointOnRoute\|diagramAttachmentId=att637372736\|containerId=637370438\|timestamp=1535618309847\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372735\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"RoutePoint-vs-PointOnRoute\",\"macro.id\":\"b36ed18e-196e-43e0-bbe1-268593a482f1\",\"diagramAttachmentId\":\"att637372736\",\"containerId\":\"637370438\",\"timestamp\":\"1535618309847\"}",  
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


### Route <a id="Datamodels-Route"></a>

Thus, a [Route](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route) is defined as a list of [RoutePoints](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-RoutePoint), which are placed into the correct sequential order by [PointOnRoute](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-PointOnRoute). To further describe the specifics of the Route, such as start, stop and turn-around  points, a [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPattern), linked to the Route is used.

### Journey Pattern <a id="Datamodels-JourneyPattern"></a>

The [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPattern) is a general term which defines the "pattern of stops" \(with- or without passengers\). It consists of a sorted list of [ScheduledStopPoint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ScheduledStopPoint) \(stopping point for boarding or alighting\) and/or "check points" \(so called [TimingPoint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-TimingPoint), used for measuring vehicle progress along the pattern. The pattern references stop points \([StopPlace](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-StopPlace) objects\) using [stopAssignments](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-StopAssignment).

In addition, various time-related values can be defined if needed:

* [Headway](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Timing) - interval between two departures.
* [RunTime](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Timing) - time between two neighbouring points. 
* [WaitTime](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Timing) - TimingPoint wait time.

**NeTEx data model for JourneyPattern**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy6318739391056246234",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-journeypattern&attachmentId=att637372739&pagePin=&imageAttachmentId=att637372737&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy6318739391056246234&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJjZmM4ZWJlMmUwNDkzMjdhMjI2NGQ1NTBiOGE5NTllMTIyMzI4MTY2ZGFlNTUxY2UwZmVlZTQyMDY2YmE1ZDNhIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.9zfBdmgJOC-EXv3x-yxnIlcdaPLMEkuPISPK8ecLyxc",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiNTQ1ZDAxMzktNTc5MC00NTA2LWJhNTQtZDY0ZjEyYmI5YzIxIiwiaWQiOiI1NDVkMDEzOS01NzkwLTQ1MDYtYmE1NC1kNjRmMTJiYjljMjEifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.diNya698480f\_hHC-J0CIgZgAl0vHjy8AQjRh\_t9Cc0",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"545d0139-5790-4506-ba54-d64f12bb9c21\",\"id\":\"545d0139-5790-4506-ba54-d64f12bb9c21\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"545d0139-5790-4506-ba54-d64f12bb9c21\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372737\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-journeypattern\|diagramAttachmentId=att637372739\|containerId=637370438\|timestamp=1535618707948\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372737\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-journeypattern\",\"macro.id\":\"545d0139-5790-4506-ba54-d64f12bb9c21\",\"diagramAttachmentId\":\"att637372739\",\"containerId\":\"637370438\",\"timestamp\":\"1535618707948\"}",  
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


The pattern itself is described as a set of points in a given order, [_pointsInSequence_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-PointInJourneyPattern). This is usually the [StopPointInJourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-StopPointInJourneyPattern), but can also be the [TimingPointInJourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-TimingPointInJourneyPattern).

**NeTEx overall conceptual model for JourneyPattern**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy2789011955062076652",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=journey-concept-principal&attachmentId=att637372754&pagePin=&imageAttachmentId=att637372756&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy2789011955062076652&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI4NTFiNTYzYWI3Y2JjN2U3ZGI4NmNmYTk3MjdhNWM5ZjM1YWJmNjkwY2E4YWUwNjg3OWI5N2M5NDlmNzVlYWE5IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.KvfSssC-Yfz7nHflgqMqTBFSABX\_-KJlYbtFq1vy9\_8",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiNWQ1MDExNjItZmEyNC00MGFmLTgxYTEtOTU2NjBjZmQ0YjljIiwiaWQiOiI1ZDUwMTE2Mi1mYTI0LTQwYWYtODFhMS05NTY2MGNmZDRiOWMifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.q4HnFbRuCXRWwiMycf-JmrxYckbx4Znzaf91yRrMZUs",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"5d501162-fa24-40af-81a1-95660cfd4b9c\",\"id\":\"5d501162-fa24-40af-81a1-95660cfd4b9c\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"5d501162-fa24-40af-81a1-95660cfd4b9c\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372756\|baseUrl=https://enturas.atlassian.net/wiki\|name=journey-concept-principal\|diagramAttachmentId=att637372754\|containerId=637370438\|timestamp=1535618812696\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372756\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"journey-concept-principal\",\"macro.id\":\"5d501162-fa24-40af-81a1-95660cfd4b9c\",\"diagramAttachmentId\":\"att637372754\",\"containerId\":\"637370438\",\"timestamp\":\"1535618812696\"}",  
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


The journey pattern is further enriched by references to scheduled stops, [_ScheduledStopPoint_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ScheduledStopPoint), which again links to physical stops \([Quay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Quay)\) through a [StopAssignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-StopAssignment):

**NeTEx detailed conceptual model for JourneyPattern**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy5837362262242174331",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=journey-concept-full&attachmentId=att728563861&pagePin=&imageAttachmentId=att728858711&border=&chrome=&html5=&size=&ceoId=&macroId=db0231d4-bc2c-4bd1-a909-229bbf614a45&spaceKey=&version=&migration=&previewPageId=728596522&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy5837362262242174331&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJlYmRmNDI3YTM1OTU4OTU3ZmM3YWJhN2NiZTJjOTJmZmYwMGViZWIyZjM4NWU0YjBiZDdjZjYyZGE1ZDE0M2FlIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.vDDDJqMb73mY-GzGr34SaH9v5rAUewC7GJBJXUDJToU",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiMjViOGVhZWUtYTA0Zi00ZTdmLWE5OGQtYTA0Yjg1N2M3MGY0IiwiaWQiOiIyNWI4ZWFlZS1hMDRmLTRlN2YtYTk4ZC1hMDRiODU3YzcwZjQifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.7yGZvkVniCYLtG3siQpdyGKW23FUj79SJxuZV3CA1AE",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"25b8eaee-a04f-4e7f-a98d-a04b857c70f4\",\"id\":\"25b8eaee-a04f-4e7f-a98d-a04b857c70f4\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"25b8eaee-a04f-4e7f-a98d-a04b857c70f4\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728858711\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=db0231d4-bc2c-4bd1-a909-229bbf614a45\|name=journey-concept-full\|diagramAttachmentId=att728563861\|containerId=728596522\|timestamp=1549875263149\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att728858711\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"db0231d4-bc2c-4bd1-a909-229bbf614a45\",\"content.id\":\"728596522\",\"name\":\"journey-concept-full\",\"macro.id\":\"25b8eaee-a04f-4e7f-a98d-a04b857c70f4\",\"diagramAttachmentId\":\"att728563861\",\"containerId\":\"728596522\",\"timestamp\":\"1549875263149\"}",  
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


**Connection between Route and JourneyPattern**  
As shown in earlier example RoutePoint vs PointOnRoute a [Route](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route) is defined as a set of [RoutePoints](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-RoutePoint) in a given order, here illustrated by two routes \(red and pink respectively\):  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy8008283638162346996",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=route-journey-illustrated-route&attachmentId=att637372747&pagePin=&imageAttachmentId=att637372713&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy8008283638162346996&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI4ZGRiMjc3ZTUxNTk3N2Q0M2I0YWI4ZWZiNTkyMGEzYzA3ODcxMzZmYjYyOWQ5NzhlODdjZDRjOWQyYTQ3NTZiIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.llRqarRQ8Q5h1EF4VPea4bOVsFU1jU-8XoUMfoKR29Y",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYTM0MDFhNmYtMjdhMi00OGQ3LTg3NTctYzAxZjgyNGM0ZjFmIiwiaWQiOiJhMzQwMWE2Zi0yN2EyLTQ4ZDctODc1Ny1jMDFmODI0YzRmMWYifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.uNMaPcl5mGQf4HBx4MmcvKDHuyslbm\_4fd5CoZeXBic",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"a3401a6f-27a2-48d7-8757-c01f824c4f1f\",\"id\":\"a3401a6f-27a2-48d7-8757-c01f824c4f1f\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"a3401a6f-27a2-48d7-8757-c01f824c4f1f\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372713\|baseUrl=https://enturas.atlassian.net/wiki\|name=route-journey-illustrated-route\|diagramAttachmentId=att637372747\|containerId=637370438\|timestamp=1535618955410\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372713\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"route-journey-illustrated-route\",\"macro.id\":\"a3401a6f-27a2-48d7-8757-c01f824c4f1f\",\"diagramAttachmentId\":\"att637372747\",\"containerId\":\"637370438\",\"timestamp\":\"1535618955410\"}",  
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


How this route is operated is further defined by the [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPattern) which consists of a set of [ScheduledStopPoints](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ScheduledStopPoint) in a given order, and these again refer to each respective [Route](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route).   
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy5195677838533499941",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=route-journey-illustrated-journey&attachmentId=att637372716&pagePin=&imageAttachmentId=att637372717&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy5195677838533499941&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIyZjZmZmNlN2NkYThjNTQzZWIyY2UyYjUwZmRiNzkxYzM3MjdiMzdjMjAzNTQ1MjU5MGViNWY5Mjg4MjdiNWRhIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.\_4E8LwYHjW-b-JVia1tb-SuNUscQGOiAN3J7yUUrdTU",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZGM1MzkxYzAtNzE5MS00MmViLWI2ZDctZGFhYTA1MGExNmY5IiwiaWQiOiJkYzUzOTFjMC03MTkxLTQyZWItYjZkNy1kYWFhMDUwYTE2ZjkifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.D8YEUo76HcSbc3-iipxggY6njfzucUNceqd5ZdSgqMU",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"dc5391c0-7191-42eb-b6d7-daaa050a16f9\",\"id\":\"dc5391c0-7191-42eb-b6d7-daaa050a16f9\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"dc5391c0-7191-42eb-b6d7-daaa050a16f9\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372717\|baseUrl=https://enturas.atlassian.net/wiki\|name=route-journey-illustrated-journey\|diagramAttachmentId=att637372716\|containerId=637370438\|timestamp=1535619065570\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372717\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"route-journey-illustrated-journey\",\"macro.id\":\"dc5391c0-7191-42eb-b6d7-daaa050a16f9\",\"diagramAttachmentId\":\"att637372716\",\"containerId\":\"637370438\",\"timestamp\":\"1535619065570\"}",  
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


Each [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPattern)  follows the same overall pattern as the referenced [Route](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route), but with considerably more detail. Thus, _JourneyPattern 1_ shows in detail what _Route 1_ describes generally, _Journey Pattern 2_ shows _Route 2_ in detail, and so on_._

This forms the basis for describing the respective departures, explained in more detail in the chapter [t](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370438/Datamodeller#Datamodeller-rutetabell)[imetable data](handbok-n801-siri-netex-data-models.md#Datamodels-timetabledata).

### Flexible transportation <a id="Datamodels-Flexibletransportation"></a>

To model a flexible on demand transport, NeTEx offers "flexible" variants of Line and Route - [FlexibleLine](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-FlexibleLine) and [FlexibleRoute](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-FlexibleRoute). They have the same features as regular Line and Route, but with additional fields to describe contact- and booking information. PointOnRoute can also be expanded with [FlexiblePointProperties](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-FlexiblePointProperties) which for example describes whether the point represents an area or a point.

**NeTEx data model for flexible transport**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy1242978073219069490",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-flexibleline&attachmentId=att637372723&pagePin=&imageAttachmentId=att637372719&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy1242978073219069490&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJjNzhiODY1YmM3NzA0NTA1ZWQyMTQ2ODc0MTFmZDQ3YzhiZDVmZjkyZDAzZWIxMTVkOWFiYmUyN2ZkNDVjMzZhIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.J1We9BXj-VDjd8ATwt47ZuJrM9motXftSF6xxqG3Uog",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZDgyMmM2OWMtYmJkNS00OTU2LTgxNGYtNmNkY2U2Mjg5ZDAzIiwiaWQiOiJkODIyYzY5Yy1iYmQ1LTQ5NTYtODE0Zi02Y2RjZTYyODlkMDMifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.OT7\_-Wjye3EpSpphcoLCkJ2WjvtJ0Y-8MZMt83fuNx8",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"d822c69c-bbd5-4956-814f-6cdce6289d03\",\"id\":\"d822c69c-bbd5-4956-814f-6cdce6289d03\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"d822c69c-bbd5-4956-814f-6cdce6289d03\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372719\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-flexibleline\|diagramAttachmentId=att637372723\|containerId=637370438\|timestamp=1535623657834\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372719\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-flexibleline\",\"macro.id\":\"d822c69c-bbd5-4956-814f-6cdce6289d03\",\"diagramAttachmentId\":\"att637372723\",\"containerId\":\"637370438\",\"timestamp\":\"1535623657834\"}",  
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


### Transfers and Interchanges <a id="Datamodels-TransfersandInterchanges"></a>

Interchanges has two aspects - physical and planned. The physical action of alighting one vehicle and boarding another is represented by [Connection](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Connection), which also refers to [ConnectionEnd](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ConnectionEnd) in order to describe that the interchanges can occur between two nearby stops \(actually quays\). [Transfer](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Transfer) objects are then used to describe physical transfer between the arrival- and departure quays.

The planned transfer is represented by [Interchange](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Interchange) objects which can be linked to [Notice](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Notice) in order to provide customers relevant transfer information.

**NeTEx data model for interchange**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy6432110727917355715",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-interchange-transfer&attachmentId=att637372725&pagePin=&imageAttachmentId=att637372724&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy6432110727917355715&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIzZDliNDAwMmY3OTA2ZjZkNGI3Y2Q3OGQ1MWQ0NjM4NjZkZGVmODlkZWJmMGZmYjhjNmU4OGFkOGM2ZWEzOTU0IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.-jRiqJWyL2q57oO\_MmQ0pCuMqVDCL0YOqYBPT9cIDkk",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZDZhODA4NjktYjY5Ni00ZmQ2LThmZWEtODkwYzA2MTFiNmRhIiwiaWQiOiJkNmE4MDg2OS1iNjk2LTRmZDYtOGZlYS04OTBjMDYxMWI2ZGEifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.bXjlEdCkcc4DZ1fXnEinVLJhpde7gW1kxdUp0\_f57qg",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"d6a80869-b696-4fd6-8fea-890c0611b6da\",\"id\":\"d6a80869-b696-4fd6-8fea-890c0611b6da\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"d6a80869-b696-4fd6-8fea-890c0611b6da\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372724\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-interchange-transfer\|diagramAttachmentId=att637372725\|containerId=637370438\|timestamp=1535623866131\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372724\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-interchange-transfer\",\"macro.id\":\"d6a80869-b696-4fd6-8fea-890c0611b6da\",\"diagramAttachmentId\":\"att637372725\",\"containerId\":\"637370438\",\"timestamp\":\"1535623866131\"}",  
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


## NeTEx timetable data representation <a id="Datamodels-timetabledataNeTExtimetabledatarepresentation"></a>

A timetable consists of one or more [VehicleJourneys](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-VehicleJourney), usually modelled as [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney) \(which describes a specific departure at a specific time\) assuming the departure is a passenger carrying service. At least two stops \([PassingTime](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-TimetabledPassingTime)\) are required in a ServiceJourney. The date of the [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney) is specified as a [DayType](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-DayType), which defines a period or a date. All journeys and other relevant elements are grouped into a [TIMETABLE FRAME](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-TimetableFrame), while dates/periods are defined in a [SERVICE CALENDAR FRAME](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-ServiceCalendarFrame).

A central part of the structure is the relationship between VehicleJourney and [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPattern) which defines [StopPoints](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-StopPointInJourneyPattern) \(and perhaps [TimingPoints](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-TimingPointInJourneyPattern)\) for a [Route](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route).

Once the pattern of the route has been defined, [OperatingDay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-OperatingDay) is used to describe when, and for how long, it operates. For this a [ServiceCalendar](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceCalendar) is created to define the calendar days when the Line operates within an [OperatingPeriod](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-OperatingPeriod). It is possible to define day by day, but it is usually sensible to use [DayType](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-DayType) to define day patterns, such as "Monday-Friday". Even more detailed information, such as specific public holidays, can be defined in [PropertyOfDay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-PropertyOfDay).

[ServiceCalendar](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceCalendar) allows the linking of [OperatingDay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-OperatingDay) to [DayType](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-DayType) through [DayTypeAssignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-DayTypeAssignment).

**NeTEx data model for calendar**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy550489761422812235",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-servicecalendar&attachmentId=att637372715&pagePin=&imageAttachmentId=att637372712&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy550489761422812235&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIzMDc0ZjIzZGRmNmNkYTQ4MTQxNzdmYmE1ZjNkYWI3MmRhZGFiNzU1NjU2OGMxOTc3YWNhMWE3Njc5YzYwMTJjIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.5QucxOyHgv85s-Q18OrhKhseUL6OFO8lQvOUJAoEEyE",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiOWJjOGYyNTYtOGMzYy00ZmNhLThjNDEtYzZhOWY2MmFmMWFkIiwiaWQiOiI5YmM4ZjI1Ni04YzNjLTRmY2EtOGM0MS1jNmE5ZjYyYWYxYWQifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.gLrM97xcssvvvpRaWsiyjKvQAhODRXDLftd8zjB57\_A",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"9bc8f256-8c3c-4fca-8c41-c6a9f62af1ad\",\"id\":\"9bc8f256-8c3c-4fca-8c41-c6a9f62af1ad\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"9bc8f256-8c3c-4fca-8c41-c6a9f62af1ad\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372712\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-servicecalendar\|diagramAttachmentId=att637372715\|containerId=637370438\|timestamp=1535629560331\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372712\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-servicecalendar\",\"macro.id\":\"9bc8f256-8c3c-4fca-8c41-c6a9f62af1ad\",\"diagramAttachmentId\":\"att637372715\",\"containerId\":\"637370438\",\"timestamp\":\"1535629560331\"}",  
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


### Timetable <a id="Datamodels-Timetable"></a>

When describing a timetable \(schedule\), [TIMETABLE FRAME](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-TimetableFrame) is used with [VehicleJourneys](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-VehicleJourney) which specifies the  [ServiceJourneys](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney) \(with passengers\) for each journey. A [VehicleJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-VehicleJourney) can, if necessary be divided into several parts \([JourneyPart](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPart)\), when for example using compund trains.

It is also possible to describe rhytm based departures \(for example repeating departures every 10 minutes over whole hours\), or interval based departures \(for example departures every 15 minutes\), for a defined period of the day using [JourneyFrequencyGroup](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyFrequencyGroup) which [TemplateServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-TemplateServiceJourney) can refer to. Alternatively a list of stop places for a [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney) can be created by using [PassingTime](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-PassingTime) objects refering to stops through a [ScheduledStopPoint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ScheduledStopPoint).

**NeTEx data model for Vehicle Journey**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy8114268964184926602",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datamodel-journey&attachmentId=att637372650&pagePin=&imageAttachmentId=att637372656&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=637370438&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy8114268964184926602&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI3NTdiNDU1ZjdlNmM5Y2VkMzg4MTQ2YTgxM2QxODMzZGRhNWMzNTdjMDY3ZThiZDAyMDIwOWQ5ODQ5NjNiMTJlIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.nAbOdSELk\_AZwWgkSVxbH9yHs94c\_EU7-ap82gs-G0Y",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYmUxYWM4OGUtMzVhNi00NGZlLWEwOTItZDRjN2M2OTQxMDJiIiwiaWQiOiJiZTFhYzg4ZS0zNWE2LTQ0ZmUtYTA5Mi1kNGM3YzY5NDEwMmIifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.8hnVu\_i\_V9F\_p\_sPa7VfoQgF9OoSKuzAr7fCoax4SXE",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"be1ac88e-35a6-44fe-a092-d4c7c694102b\",\"id\":\"be1ac88e-35a6-44fe-a092-d4c7c694102b\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"be1ac88e-35a6-44fe-a092-d4c7c694102b\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att637372656\|baseUrl=https://enturas.atlassian.net/wiki\|name=datamodel-journey\|diagramAttachmentId=att637372650\|containerId=637370438\|timestamp=1535629596869\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att637372656\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datamodel-journey\",\"macro.id\":\"be1ac88e-35a6-44fe-a092-d4c7c694102b\",\"diagramAttachmentId\":\"att637372650\",\"containerId\":\"637370438\",\"timestamp\":\"1535629596869\"}",  
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


This means each departure is defined as a [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney) \(usually connected to a [Line](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Line)\), used by a [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPattern) with one or more [DayType](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-DayType) \(describing dates or periods\). The ServiceJourney describes the times of arrival and departure along the journey by use of [StopPointInJourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-StopPointInJourneyPattern) for stop, with a [PassingTime](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-TimetabledPassingTime) defining the exact times.

**NeTEx conceptual model for ServiceJourney**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy4801596079201037466",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=service-concept&attachmentId=att728596607&pagePin=&imageAttachmentId=att728858723&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=728596522&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy4801596079201037466&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI3ZDQ1ZjA4YmNhYjUzYzJkNWQ2OWU5ZjMyY2Q2YWU4MGUyZjAzMzBkMzVkYTIwMDZlYTk1ZWIyYmEyYmQ3OWJkIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.EQRkdw-NOpO9Ke7yrCeg-aJVGiO641PMm3QUT5ikOPY",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYjJhNDZjMzUtYjE2OS00ZGVhLTk4NzAtNDFlMjM1ZTYzMDdhIiwiaWQiOiJiMmE0NmMzNS1iMTY5LTRkZWEtOTg3MC00MWUyMzVlNjMwN2EifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.7AcbmwE3nVa\_BIRskjw5rwc2P7puPK\_mM9kL\_OF\_70c",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"b2a46c35-b169-4dea-9870-41e235e6307a\",\"id\":\"b2a46c35-b169-4dea-9870-41e235e6307a\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"b2a46c35-b169-4dea-9870-41e235e6307a\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728858723\|baseUrl=https://enturas.atlassian.net/wiki\|name=service-concept\|diagramAttachmentId=att728596607\|containerId=728596522\|timestamp=1549882380639\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att728858723\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"service-concept\",\"macro.id\":\"b2a46c35-b169-4dea-9870-41e235e6307a\",\"diagramAttachmentId\":\"att728596607\",\"containerId\":\"728596522\",\"timestamp\":\"1549882380639\"}",  
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


When the nature of the service requires a permanent ID per service, e.g. with tickets associated to a specific departure on a specific day, rather than having a loose coupling to a [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney) with multiple associated [DayTypes](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-DayType) these should be defined as individual **DatedServiceJourney**s with an associate [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney) specifying the nature of the service and an  [OperatingDay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-OperatingDay) defining on which date it is serviced. Should such a **DatedServiceJourney** be replanned or replaced, \(a\) new **DatedServiceJourney**\(s\) referencing the originally planned **DatedServiceJourney** should be specified.

**NeTEx conceptual model for DatedServiceJourney**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy1236051633402271420",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=datedservicejourney&attachmentId=att1900511332&pagePin=&imageAttachmentId=att1900511337&border=&chrome=&html5=&size=&ceoId=&macroId=32c5f615-21d0-474a-bdec-558e8e7865e2&spaceKey=&version=&migration=&previewPageId=728596522&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy1236051633402271420&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIxODUyMGJmNDA4YmMyMDg5ZTU0NjFiNmRiMGZjMThiZDE4M2M1OWJlODYwYjhlNGM4YjJiODE5ZGM4MDMwYWVmIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.7ddO8BDQFawk8Aowcu0NTOQd7zDsfx0CLTnPZisXWuU",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYTIwN2Q4NmQtNDE0Ny00OTAzLTg4MmItYTEwZThhM2YzYWQyIiwiaWQiOiJhMjA3ZDg2ZC00MTQ3LTQ5MDMtODgyYi1hMTBlOGEzZjNhZDIifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.bCEdiMrZ3AEQ7mXLTKgkAAa3b0MG9bKm7vgPcO9pcKo",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"a207d86d-4147-4903-882b-a10e8a3f3ad2\",\"id\":\"a207d86d-4147-4903-882b-a10e8a3f3ad2\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"a207d86d-4147-4903-882b-a10e8a3f3ad2\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att1900511337\|macroId=32c5f615-21d0-474a-bdec-558e8e7865e2\|baseUrl=https://enturas.atlassian.net/wiki\|name=datedservicejourney\|diagramAttachmentId=att1900511332\|containerId=728596522\|timestamp=1605574046913\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att1900511337\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"macroId\":\"32c5f615-21d0-474a-bdec-558e8e7865e2\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728596522\",\"name\":\"datedservicejourney\",\"macro.id\":\"a207d86d-4147-4903-882b-a10e8a3f3ad2\",\"diagramAttachmentId\":\"att1900511332\",\"containerId\":\"728596522\",\"timestamp\":\"1605574046913\"}",  
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


### Deviations <a id="Datamodels-Deviations"></a>

When describing a deviation from the common departure pattern, the [OperatingDay](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-OperatingDay), can be described in inverse by define the particular day\(s\) as _**unavailable**_.

### Data enrichment <a id="Datamodels-Dataenrichment"></a>

As mentioned above, a trip can be specified on several levels in NeTEx, ranging from the parent [Route](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-Route) via detailed [JourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-JourneyPattern) down to the individual [ServiceJourney](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370393/Generell+informasjon+NeTEx#Generellinformasjon-ServiceJourney).

The goal of the Norwegian _NeTEx profile is to place all elements as high up in the structure as possible, in order to avoid redundancies._

#### Conceptual model for enrichment of data in NeTEx <a id="Datamodels-ConceptualmodelforenrichmentofdatainNeTEx"></a>

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy7433555120361277038",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728596522&pageId=&name=data-enrichment&attachmentId=att728760378&pagePin=&imageAttachmentId=att728694871&border=&chrome=&html5=&size=&ceoId=&macroId=5fcbf3b8-2225-4f1e-8281-fb5652cc276c&spaceKey=&version=&migration=&previewPageId=728596522&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy7433555120361277038&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI4OWIwNzFkM2VmNTU2ZDlhZTAyMzFlYjEzMTUwNzYwYmEwMTFhNDlkZmU3ODYxOWFmZTRhZDIxMTY2YTgwOTQwIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgyOCwiaWF0IjoxNjE5NTkxNjQ4fQ.T9firCZY8F4Qd3AU2SRl8ea-k5t3urM\_ifoIS9w2B5w",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiNDAwYWE0NTUtYzdhZS00ZjdiLThhZjEtNmEzZWQxYmQ3ODlkIiwiaWQiOiI0MDBhYTQ1NS1jN2FlLTRmN2ItOGFmMS02YTNlZDFiZDc4OWQifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIzNyIsImlkIjoiNzI4NTk2NTIyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTQ4LCJpYXQiOjE2MTk1OTE2NDh9.LnOqUOcBSkp1rESwM7lRgKMZ9XTM2It0ONBL-dOWCP0",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"400aa455-c7ae-4f7b-8af1-6a3ed1bd789d\",\"id\":\"400aa455-c7ae-4f7b-8af1-6a3ed1bd789d\"},\"content\":{\"type\":\"page\",\"version\":\"37\",\"id\":\"728596522\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728596522\",\"macro.hash\":\"400aa455-c7ae-4f7b-8af1-6a3ed1bd789d\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"37\",\"page.title\":\"Data models\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728694871\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=5fcbf3b8-2225-4f1e-8281-fb5652cc276c\|name=data-enrichment\|diagramAttachmentId=att728760378\|containerId=728596522\|timestamp=1549885343569\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"37\",\"imageAttachmentId\":\"att728694871\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"5fcbf3b8-2225-4f1e-8281-fb5652cc276c\",\"content.id\":\"728596522\",\"name\":\"data-enrichment\",\"macro.id\":\"400aa455-c7ae-4f7b-8af1-6a3ed1bd789d\",\"diagramAttachmentId\":\"att728760378\",\"containerId\":\"728596522\",\"timestamp\":\"1549885343569\"}",  
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


