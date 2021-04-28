# Håndbok N801 \(SIRI/NeTEX\) : General information: NeTEx

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591628994 {padding: 0px;}  
div.rbtoc1619591628994 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591628994 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Preface](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Preface)
* [Introduction](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Introduction)
  * [References](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-References)
* [Exchanging information](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-PublicationDeliveryExchanginginformation)
  * * [Each PublicationDelivery must contain the following two mandatory fields:](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-EachPublicationDeliverymustcontainthefollowingtwomandatoryfields:)
    * [Data submission in CompositeFrame](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-DatasubmissioninCompositeFrame)
    * [Data submission as single frames](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Datasubmissionassingleframes)
  * [Generalization](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Generalization)
* [Versioning](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Versioning)
  * [Version for profile](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Versionforprofile)
  * [Versions for data elements](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Versionsfordataelements)
    * [Elements that must have versions](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Elementsthatmusthaveversions)
    * [version="any"](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-version=%22any%22)
    * [Versioning in references](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Versioninginreferences)
  * [Validity for data elements](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Validityfordataelements)
    * [Data elements which can override validity \(ValidityCondition\)](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Dataelementswhichcanoverridevalidity%28ValidityCondition%29)
* [Conventions](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Conventions)
  * [Structure of ID's](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StructureofID%27s)
    * [Static ID's](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-StaticID%27s)
    * [Codespace](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Codespace)
  * [Cardinality](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Cardinality)
  * [Type description](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Typedescription)
  * [Use of Enumeration](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-UseofEnumeration)
* [Definitions](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-Definitions)

## Preface <a id="Generalinformation:NeTEx-Preface"></a>

Harmonization of exchange methodology between different systems is essential to:

**Entur AS on behalf of Jernbanedirektoratet**

...in order to efficiently collect all timetable data from each data provider, ensure consistency of data, and increase data quality. This allows the creation of multimodal information systems which may be used to implement nationwide journey planning solutions and publicize business neutral information to all interested parties.

**for travellers**

...in order to present relevant, and high-quality journey suggestions.

**for public transport operators**

...in order to re-use the data in their own journey planning-, ticketing-, and information systems, and offer a better service to their customers.

**for third-party service providers**

...in order to minimize unnecessary costs related to supporting multiple different exchange formats, and to contribute to the continued growth of standardized public transport data exchange.

## Introduction <a id="Generalinformation:NeTEx-Introduction"></a>

NeTEx \(`CEN TS 16614-1, 16614-2 og 16614-3`\) is a CEN-standard which defines the data format and description for public transport data exchanges. The standard is based on Transmodel \(`EN 12896`\), and the reference model for permanent objects required for access to public transport: IFOPT \(Identification of Fixed Objects in Public Transport, `EN 28701`\).

NeTEx supports the exchange of data necessary for stop place information, journey planning, and ticketing, and is divided into three main categories:

1. Network Topology \(`CEN TS 16614-1`\)
2. Scheduled Timetables Plan data \(`CEN TS 16614-2`\)
3. Fare Information \(`CEN TS 16614-3`\)

NeTEx was created by CEN / TC278 / WG3 / SG9 lead by France. The final part of the format was published in 2015. The format was created to support the needs of a collection of public transport data providers in Europe, among others ERA \(_European Rail Agency_\) and UIC \(_International Union of Railways_\).

NeTEx is a general-purpose XML format that facilitates the exchange of complex public transport data between distributed systems. Data in the NeTEx format should be used to effectively update various information and operational applications through both file-based services and web service architectures. The [official website](http://netex-cen.eu) contains a detailed explanation of the intention underlying the standard, data models and publicly available standard documentation. In particular, "_NeTEx White Papers_", available under the website's [Downloads](http://netex-cen.eu/?page_id=14)-section provides a good introduction to how different concepts in public transport can be modelled using NeTEx.

NeTEx is a comprehensive data format intended to describe different concepts for public transport data in various ways. In many cases, there will be parts of the specification that exceed requirements in actual implementation. Therefore, the extraction of necessary objects, which constitute a so-called NeTEx profile, should be made. Such a profile should be used to specify which parts of the NeTEx format are expected to be exchanged between systems in a given context.

This document describes NeTEx's profile Norway for the exchange of stop and timetable data between external actors and central systems provided by Entur. Moreover, this profile has been prepared with the assistance of the NeTEx working group in CEN \(_Comité européen de normalisation, the European Committee for Standardization_\).

**To reduce complexity, the profile is divided into several parts:**

* Reusable Components: [framework]()
* Information about StopPlaces: [stops](handbok-n801-siri-netex-stops.md)
* Information about Transport Network Information: [network](handbok-n801-siri-netex-network.md)
* Information about Timetable: [timetable](handbok-n801-siri-netex-timetable.md)
* Information about Fares [https://enturas.atlassian.net/wiki/spaces/ROR/pages/1638137934](https://enturas.atlassian.net/wiki/spaces/ROR/pages/1638137934)
* Information about Sales [sales](handbok-n801-siri-netex-sales.md)

Each section describes data objects that belong to a given functionality. In addition, basic objects reused across the dataset are separated into a "commons" section.  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy1639259201237446158",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563782&pageId=&name=NeTex+profil&attachmentId=att728727598&pagePin=&imageAttachmentId=att728629307&border=&chrome=&html5=&size=&ceoId=&macroId=1ba988f2-7f0f-4d9b-8a28-32028815316f&spaceKey=&version=&migration=&previewPageId=728563782&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy1639259201237446158&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI1MGU5MmRiZDhkZDc3OGQyNjAyZTBjNTYyOWE5ZWNlZGE2YjZkZmU1MTY3MDAwZmM4MjM5NzViY2Y4YmI3MjVjIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgwOSwiaWF0IjoxNjE5NTkxNjI5fQ.wv5rdDMwxEvWlf57HG\_SxJ99u8P7ShgCyF9TshXX5HE",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiOTdhNjQxNDMtYzI5NS00YWUwLTg1NGYtNjI1YzM3OGMzNDJjIiwiaWQiOiI5N2E2NDE0My1jMjk1LTRhZTAtODU0Zi02MjVjMzc4YzM0MmMifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIyMSIsImlkIjoiNzI4NTYzNzgyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTI5LCJpYXQiOjE2MTk1OTE2Mjl9.4DLeY4W6JzRolVTUGVPIMLJrE1aFuyr0Gvx\_DFVQnFU",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"97a64143-c295-4ae0-854f-625c378c342c\",\"id\":\"97a64143-c295-4ae0-854f-625c378c342c\"},\"content\":{\"type\":\"page\",\"version\":\"21\",\"id\":\"728563782\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563782\",\"macro.hash\":\"97a64143-c295-4ae0-854f-625c378c342c\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"21\",\"page.title\":\"General information: NeTEx\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728629307\|macroId=1ba988f2-7f0f-4d9b-8a28-32028815316f\|baseUrl=https://enturas.atlassian.net/wiki\|name=NeTex profil\|diagramAttachmentId=att728727598\|containerId=728563782\|timestamp=1551256319880\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"21\",\"imageAttachmentId\":\"att728629307\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"macroId\":\"1ba988f2-7f0f-4d9b-8a28-32028815316f\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728563782\",\"name\":\"NeTex profil\",\"macro.id\":\"97a64143-c295-4ae0-854f-625c378c342c\",\"diagramAttachmentId\":\"att728727598\",\"containerId\":\"728563782\",\"timestamp\":\"1551256319880\"}",  
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


### References <a id="Generalinformation:NeTEx-References"></a>

The Norwegian NeTEx profile is based on the following documents:

* `TS 16614-1, Network and Timetable Exchange (NeTEx) - Part 1: Public transport network topology exchange format`
* `TS 16614-2, Network and Timetable Exchange (NeTEx) - Part 2: Public transport scheduled timetables exchange format`
* `EN 12896, Road Transport and traffic telematics - Public transport - Reference data model (Transmodel)`
* `EN 28701, Intelligent transportation systems - Public transport - Identification of Fixed Objects in Public Transport (IFOPT)`

## Exchanging information <a id="Generalinformation:NeTEx-PublicationDeliveryExchanginginformation"></a>

Information exchanged in the NeTEx format should be XML files containing only one root tag: `PublicationDelivery`

The information should be delivered with one XML file per Line, packed as ZIP-file with a flat structure \(no subdirectories\). It is technically possible to deliver each line separately, packed in separate ZIP-files if all the data objects used by each Line are defined within its _PublicationDelivery_. However, in order to avoid issues with overwriting and ensure good data update/deletion management, it is _strongly_ recommended that only complete datasets containing all lines are exchanged. Data objects used by multiple Lines can be defined in a separate "common" XML-file \(**must** be prefixed with an underscore, e.g. "\_common.xml"\) to avoid redundancy of unique objects.

#### Each PublicationDelivery must contain the following two mandatory fields: <a id="Generalinformation:NeTEx-EachPublicationDeliverymustcontainthefollowingtwomandatoryfields:"></a>

`<PublicationTimestamp>` _\[data extraction time\]_ `</PublicationTimestamp>`  
`<ParticipantRef>` _\[codespace for data submitter\]_ `</ParticipantRef>`

Within a _PublicationDelivery_, &lt;_dataObjects_&gt;  are defined, which consist of a set of _Frames._ Each frame contains all relevant objects in a single group and specifies common validity conditions, e.g. validity and version. This mechanism supports incremental updating of individual objects in cases where the relationships between the objects are not altered and will assist in troubleshooting down to the object- or group level.

_PublicationDelivery_ allows for any number of frames, and the same frame type can be reused multiple times. It is good practice to use as few frames as possible so that the grouping within the same PublicationDelivery is appropriate \(avoid "wrapping" objects into their own frames\). Objects that naturally belong together, i.e. have the same version and validity, must be collected in the same frame.

XML example for `PublicationDelivery` can be found in the [GitHub-repository](https://github.com/entur/profile-norway-examples/blob/master/netex/frames/publicationDelivery.xml).

#### Data submission in CompositeFrame <a id="Generalinformation:NeTEx-DatasubmissioninCompositeFrame"></a>

When grouping Frames into a CompositeFrame, ValidityCondition must be the same for all its frames. That is, ValidityCondition is _not_ set per frame, but is implicitly controlled from the CompositeFrame.  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy2633347626179585102",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563782&pageId=&name=PublicationDelivery-CompositeFrame&attachmentId=att728727602&pagePin=&imageAttachmentId=att728760373&border=&chrome=&html5=&size=&ceoId=&macroId=f1cad444-fdff-43a4-9e55-34ae7fb1d25e&spaceKey=&version=&migration=&previewPageId=728563782&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy2633347626179585102&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI3MzBlMDY2ZTU1YjdkZWQzOTU4NjUzN2M1YmUzYjdkZTM4OTFmM2RjMGNkYjg1YzBlYjNkNzdiM2Y1NDBlNzQ4IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgwOSwiaWF0IjoxNjE5NTkxNjI5fQ.n6brsdGR5u42RcE9eLq2U-wPNWlPpXo1454HUYDbQ2k",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiMDA4ZmFiNzUtZDU3Mi00YTgwLTk5YTktNGQyOGIxZjg3YjMyIiwiaWQiOiIwMDhmYWI3NS1kNTcyLTRhODAtOTlhOS00ZDI4YjFmODdiMzIifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIyMSIsImlkIjoiNzI4NTYzNzgyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTI5LCJpYXQiOjE2MTk1OTE2Mjl9.9D3aoFo8W1rTHg6QLvHygjXPYDMjCe9gBjP6wkga\_8Q",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"008fab75-d572-4a80-99a9-4d28b1f87b32\",\"id\":\"008fab75-d572-4a80-99a9-4d28b1f87b32\"},\"content\":{\"type\":\"page\",\"version\":\"21\",\"id\":\"728563782\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563782\",\"macro.hash\":\"008fab75-d572-4a80-99a9-4d28b1f87b32\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"21\",\"page.title\":\"General information: NeTEx\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728760373\|macroId=f1cad444-fdff-43a4-9e55-34ae7fb1d25e\|baseUrl=https://enturas.atlassian.net/wiki\|name=PublicationDelivery-CompositeFrame\|diagramAttachmentId=att728727602\|containerId=728563782\|timestamp=1551095305482\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"21\",\"imageAttachmentId\":\"att728760373\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"macroId\":\"f1cad444-fdff-43a4-9e55-34ae7fb1d25e\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728563782\",\"name\":\"PublicationDelivery-CompositeFrame\",\"macro.id\":\"008fab75-d572-4a80-99a9-4d28b1f87b32\",\"diagramAttachmentId\":\"att728727602\",\"containerId\":\"728563782\",\"timestamp\":\"1551095305482\"}",  
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


#### Data submission as single frames <a id="Generalinformation:NeTEx-Datasubmissionassingleframes"></a>

When frames are _not_ grouped in a CompositeFrame, all relevant frames must have explicitly defined ValidityConditions.  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy1433146253653446219",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563782&pageId=&name=PublicationDelivery-separate-frames&attachmentId=att728662143&pagePin=&imageAttachmentId=att728858706&border=&chrome=&html5=&size=&ceoId=&macroId=b674be16-91aa-46b4-b46e-e022c0662111&spaceKey=&version=&migration=&previewPageId=728563782&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy1433146253653446219&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI1NzkxYWI3ZDVlN2ZhNjM5OGUyY2UyMzcyNWY4NjAwODk3YzEyMDAzN2VmNTdhM2FmMzE4NmYwNjMzZGQ1ZTEwIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTgwOSwiaWF0IjoxNjE5NTkxNjI5fQ.WSmKTFzaX6wS63vqPmyNcd1hDeCCKBjI2PsP\_a2yvZw",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYjFhOTg2NDctN2Q5Ny00NDg3LTlkNDItNjY1M2FlMDQ0Yjk2IiwiaWQiOiJiMWE5ODY0Ny03ZDk3LTQ0ODctOWQ0Mi02NjUzYWUwNDRiOTYifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIyMSIsImlkIjoiNzI4NTYzNzgyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNTI5LCJpYXQiOjE2MTk1OTE2Mjl9.FgYAjm3VssGoPNXELuBQOFkbA54l4Ik8UQ5dQXk7Sl8",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"b1a98647-7d97-4487-9d42-6653ae044b96\",\"id\":\"b1a98647-7d97-4487-9d42-6653ae044b96\"},\"content\":{\"type\":\"page\",\"version\":\"21\",\"id\":\"728563782\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563782\",\"macro.hash\":\"b1a98647-7d97-4487-9d42-6653ae044b96\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"21\",\"page.title\":\"General information: NeTEx\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728858706\|macroId=b674be16-91aa-46b4-b46e-e022c0662111\|baseUrl=https://enturas.atlassian.net/wiki\|name=PublicationDelivery-separate-frames\|diagramAttachmentId=att728662143\|containerId=728563782\|timestamp=1551095259153\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"21\",\"imageAttachmentId\":\"att728858706\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"macroId\":\"b674be16-91aa-46b4-b46e-e022c0662111\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728563782\",\"name\":\"PublicationDelivery-separate-frames\",\"macro.id\":\"b1a98647-7d97-4487-9d42-6653ae044b96\",\"diagramAttachmentId\":\"att728662143\",\"containerId\":\"728563782\",\"timestamp\":\"1551095259153\"}",  
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


### Generalization <a id="Generalinformation:NeTEx-Generalization"></a>

In NeTEx, objects can be placed at many different levels, in whichever way is most purposeful. In order to avoid redundancy, the Norwegian profile dictates that all descriptions and references should be as high up in the hierarchy as possible.

_For example,_ [_Operator_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Operator) _can be referenced from the individual_ [_ServiceJourney_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-ServiceJourney) _in_ [_Timetable_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-TimetableFrame)_, but in most cases, a Line will have only one main operator. This should, therefore, be referenced in_ [_Line_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-Line)_, and any exceptions will instead be overwritten per_ [_ServiceJourney_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-ServiceJourney) _\(with reference to "additionalOperators" in_ [_Line_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-Line)_\)._

## Versioning <a id="Generalinformation:NeTEx-Versioning"></a>

To ensure compatibility, NeTEx offers version control mechanisms which allow both sender and recipient to:

* Specify the NeTEx version used
* Ensures correct data handling when the parties in the exchange use different versions.
* Correct usage of exchanged data by the recipient.
* Notifications when using outdated elements etc.

Version control is based on the version attribute \(VersionFrame\) and should be placed on relevant objects as high up in the hierarchy as possible.

### Version for profile <a id="Generalinformation:NeTEx-Versionforprofile"></a>

When submitting NeTEx XML for stop place information, or time table data, the NeTEx version has to be specified in order to instruct the recipient of how to read the data. This is accomplished by stating the profile version of the dataset.

Profile version is defined in a version attribute for the XML's PublicationDelivery root node.

Formats for profile version:

`[NeTEx XSD-version]:[ProfileName]:[Profile-version]`

* **NeTEx xsd-version** is a numeric value specifying the NeTEx XSD \(XML Schema\) version being used \(format **X.Y**\)
* **NO-NeTEx-&lt;profilnavn&gt;** is the profile name with one of the following values:
  * **stops**
  * **networktimetable**
  * **fares**
* **Profile version** is a numeric value specifying the Norwegian NeTEx-profile version being used \(format **X.Y**\)

Examples**:**

| **Id** | **Meaning** |
| :--- | :--- |
| version="1.08:NO-NeTEx-stops:1.3" | NeTEx XSD version 1.08 with data according to Norwegian _stops_-profile version 1.3 |
| version="1.08:NO-NeTEx-networktimetable:1.3" | NeTEx XSD version 1.08 with data according to Norwegian _networktimetable_-profile version 1.3 |

When the NeTEx format or the profile is updated, it will usually be backward compatible. When backward compatibility is not possible, both active versions will be considered valid and supported, until otherwise stated.

### Versions for data elements <a id="Generalinformation:NeTEx-Versionsfordataelements"></a>

Individual elements are also versioned, and here it is up to the creator of the dataset to define a versioning system.

* The version number must be a positive whole number \(integer\).
* The version number must be increased in such a way that the latest version of the object always has the highest number.

#### Elements that must have versions <a id="Generalinformation:NeTEx-Elementsthatmusthaveversions"></a>

Most objects with an ID must also have a version \(see [Example catalogue](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370407/Eksempel-katalog+NeTEx) for more details\) to ensure all changes lead to an increase of version number.

The following changes are particularly important, and require incremental versioning:

* Changes in Network/GroupOfLines.
* Changes in Line _\(same ID, new version\)._
* Changes in organisations _\(Authority, Operator - same ID, new version\)._
* Changes in geographical data/positions for objects.
* New additional information \(such as AlternativeName\).
* Smaller corrections which impact information to the public \(such as changes of departure times\).

#### version="any" <a id="Generalinformation:NeTEx-version=&quot;any&quot;"></a>

NeTEx allows you to explicitly specify that an object is _not_ versioned by defining the version attribute as "any".

An object defined outside the submitted dataset, such as external objects from the national stop place registry will always be the "current" version.

#### Versioning in references <a id="Generalinformation:NeTEx-Versioninginreferences"></a>

A version attribute for references to a unique object defined in the same PublicationDelivery is required. This means that a reference to an element defined within the same XML-file must be versioned. References to external objects are not versioned.

Note that when referring to an object with **both id and version**, the consistency validation of the XML-file will **require** the existence of the object referred to \(with the same referred _id_ and _version_\) within the same file. This also applies when the version is defined as "any".

For the same reason, when referring to external objects \(for example an ID in the national stop place registry\), the version attribute must be **omitted** in order for the XML file to be valid.

When the version attribute is stated on a reference, this reference is validated against existing objects with the same "ID + VERSION" in the current PublicationDelivery. Because XML validation uses string comparison in Schema validation it is not possible to use _version="any"_ for references to objects with explicit version numbers. If there are several possible versions of the objects defined internally in the file, and a reference to the latest version is desired, a reference _without_ version attributes should be used \(just like when referencing external objects\).

### Validity for data elements <a id="Generalinformation:NeTEx-Validityfordataelements"></a>

All objects with a version attribute **must have a validity**. Validity can be implicitly based on inherited values, or defined explicitly on the object through ValidityConditions. ValidityConditions can be set for a single line or a set of lines.

This is done in **one** of the following ways:

* ValidityCondition set explicitly per frame in PublicationDelivery.
* ValdityCondition for a CompositeFrame, which contains all the frames in PublicationDelivery. _This defines a validity which is inherited by all objects in the dataset and applies implicitly to all subordinate frames. It is not possible to override ValidityCondition for subordinate frames within a CompositeFrame._ 

#### Data elements which can override validity \(ValidityCondition\) <a id="Generalinformation:NeTEx-Dataelementswhichcanoverridevalidity(ValidityCondition)"></a>

All subordinate data elements implicitly inherit validity defined by ValidityCondition in CompositeFrame, or in individual Frames. When it is necessary to override inherited validity on subordinate objects, they can be given their own explicit ValidityConditions:

* Overriding ValidityCondition is defined per object.
* Overriding ValidityCondition is constrained by its inherited validity. This means the overriding validity must have a **shorter** time span than the inherited value.

Overriding is supported by the following objects:

* Network
* lines
* organisations \(Authority, Operator\)
* routes
* serviceLinks
* journeyPatterns

Overriding of Timetable- and ServiceCalendar related data must be done in a complete TimetabelFrame, and ServiceCalendarFram with an unambiguous ValidityCondition for its subordinate elements.

## Conventions <a id="Generalinformation:NeTEx-Conventions"></a>

### Structure of ID's <a id="Generalinformation:NeTEx-StructureofID&apos;s"></a>

The ID attribute of NeTEx objects must follow a common pattern, and should be structured in the following way:

**`[codespace]:[type]:[identification]`**

* **codespace** Codespace _uniquely_ represents the owner, creator, or administrator of the data. \(S_ee_ [_List of current Codespaces_](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370434/List+of+current+Codespaces)_._\)
* **type**  Type should always be the name of the NeTEx data type, using exactly the same spelling as implemented in the NeTEx XSD \(for example _ResourceFrame, TransportMode, Network_, _Line_, _StopPlace_, _Quay_ etc.\)
* **identification** Identification must be a value which, in the context of the first two parts \(codespace + type\) of the ID, _uniquely_ identifies the data object. _Please note that the identification string can only use numbers \(0-9\), lowercase \(a-z\) and uppercase \(A-Z\) letters, dash \(-\) and underscore \(\_\), in any combination._

| Object | ID examples: |
| :--- | :--- |
| Line | RUT:Line:ABC |
| Route | RUT:Route:3434 |
| RoutePoint | RUT:RoutePoint:43423342-3424 |

#### Static ID's <a id="Generalinformation:NeTEx-StaticID&apos;s"></a>

When exchanging stop place information \(StopPlace, Quay etc.\) with the central database, usage of nationally defined ID's is **required**. This ensures data integrity and uniformity over time.

It is recommended that all data objects describing continual public transport services, such as Line, Route, or ServiceJourney also maintain **static ID's across datasets**, even if each dataset contains changes to them. This makes the collection and use of historical data easier, as well as linking to the dataset from other datasets \(between codespaces\).

It would then likewise be important to **not** reuse ID's when there are significant changes to Lines etc.

#### Codespace <a id="Generalinformation:NeTEx-Codespace"></a>

Just as namespace is used to identify a unique XML Schema, codespace is used in NeTEx to ensure that all elements and attributes in the XML are unique when combined with other datasets. The central agency \(Entur\) assigns each data provider a unique codespace, consisting of a three letter code, for example, "KOL" for the provider _Kolumbus_. Each dataset must have the correct codespace to pass validation.

### Cardinality <a id="Generalinformation:NeTEx-Cardinality"></a>

Cardinality is a property which describes the number of instances of XML elements per document, as well as whether the element is required or not, according to the Norwegian NeTEx profile.

* **`0: 1`** - Optional - _None, or a maximum of 1 instance allowed._
* **`0: *`** - Optional - _None, or a maximum of 1 or more instances allowed._
* **`1: 1`** ``- Required - _At least one instance is required, but no more than one._
* **`1: *`** - Required - _At least one or more instance is required._

### Type description <a id="Generalinformation:NeTEx-Typedescription"></a>

Each object is described with a table:

| &lt;Inheritance hierarchy&gt; |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
| Attribute/Element  | Name | Type | Cardinality | Description |

The inheritance hierarchy is described in the following way:

`Class < ParentClass < ParentClass < ... < ParentClass`

The first column is omitted if the table only contains elements \(it is used to separate attributes and elements\).

| DataManagedObject &lt; EntityInVersion &lt; Entity |  |  |  |  |
| :--- | :--- | :--- | :--- | :--- |
|  | Name | Type | Cardinality | Description |
| attr | responsibilitySetRef | ResponsibilitySetIdType | 1: 1 | Points to roles and responsibility areas connected to STOP PLACE, BOARDING ZONE or ACCESS ZONE |
| elem | keyList | KeyList | 0: 1 | A set of key-value pairs which describes additional properties for the relevant object \(LINE, STOP PLACE, BOARDING ZONE, PLANNED STOP POINT etc.\), and necessary for third-party systems \(eg. ticketing, journey-planning, real-time\) |
| elem | Extentions | ExtentionStructure | 0: 1 | Extension element for data not defined by NeTEx. **PLEASE NOTE:** Should only be used by approval from working group/Entur when strictly necessary \(e.g. specific need for internal data exchange\)  |
| elem | BrandingRef | BrandingRefStructure | 0: 1 | Reference to Brand \(e.g. Ruter, AtB\) |

### Use of Enumeration <a id="Generalinformation:NeTEx-UseofEnumeration"></a>

The profile documents describe the various NeTEx-objects used in Norway, with relevant fields and datatypes. Some data types are Enumeration, that is a list of predefined values allowed for the field.

There are two ways to use Enumeration:

1. Simple Enumeration  
   When the datatype is set to xxxEnumeration \(for example _FacilitySetEnumeration_\), it means only one value is allowed:

   ```text
   ...
   <facilitySet>seatingOnly</facilitySet>
   ...
   ```

2. List of Enumerations  
   When the datatype is set to xxxListOfEnumerations \(for example _MealFacilityListOfEnumerations_\), it means multiple values are allowed for the same element:

   ```text
   ...
   <mealFacilityList>breakfast dinner drinks</mealFacilityList>
   ...
   ```

## Definitions <a id="Generalinformation:NeTEx-Definitions"></a>

Description of all NeTEx terminology used in the profile:

| Term | Definition |
| :--- | :--- |
| Access | The physical \(spatial\) possibility for a passenger to access or leave the public transport system. This link may be used during a trip for:- the walking movement of a passenger from a PLACE \(origin of the trip\) to a STOP POINT \(origin of the PT TRIP\), or- the walking movement from a STOP POINT \(destination of the PT TRIP\) to a PLACE \(destination of the trip\). |
| [Access Equipment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-AccessEquipment) | Specialisation of PLACE EQUIPMENT dedicated to access \(e.g. lifts, entrances, stairs, ramps, etc.\). |
| [Access Space](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370400/stops#stops-AccessSpace) | An area within a STOP PLACE that does not give direct access to transport vehicles. Can be connected to QUAYS by PATH LINKs. |
| [Accessibility Assessment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-AccessibilityAssessment) | The accessibility characteristics of an entity used by passengers such as a STOP PLACE, or a STOP PLACE COMPONENT. Described by ACCESSIBILITY LIMITATIONs, and/or a set of SUITABILITies. |
| [Accessibility Limitation](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-AccessibilityLimitation) | A categorisation of the ACCESSIBILITY characteristics of a STOP PLACE COMPONENT such as a STOP PATH LINK, STOP PLACE or ACCESS SPACE to indicate its usability by passengers with specific needs, for example, those needing wheelchair access, step-free access or wanting to avoid confined spaces such as lifts. |
| [Actual Vehicle Equipment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-ActualVehicleEquipment) | An item of EQUIPMENT of a particular type actually available in an individual VEHICLE. |
| [Address](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Address) | The descriptive data associated with a PLACE that can be used to describe the unique geographical context of a PLACE for the purposes of identifying it. Can further be specified as either a ROAD ADDRESS, a POSTAL ADDRESS or both. |
| [Addressable Place](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370400/stops#stops-AddressablePlace) | A PLACE which may have an address. |
| [Allowed Line Direction](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-AllowedLineDirection) | A set of allowed DIRECTIONs that can be used on a given ROUTE. |
| [Alternative Name](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-AlternativeName) | An alternative name for the entity. |
| [Assignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Assignment) | A set of properties to be applied to another element. It has a name and an order. |
| [Assistance Service](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-AssistanceService) | A specialisation of LOCAL SERVICE for ASSISTANCE providing information like language, accessibility trained staff, etc. |
| [Authority](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Authority) | The organisation under which the responsibility of organising the transport service in a certain area is placed. |
| [Availability Condition](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-AvailabilityCondition) | VALIDITY CONDITION stated in terms of DAY TYPES and  PROPERTIES OF DAYs. |
| [Block](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-AvailabilityCondition) | The work of a vehicle from the time it leaves a PARKING POINT after parking until its next return to park at a PARKING POINT. Any subsequent departure from a PARKING POINT after parking marks the start of a new BLOCK. The period of a BLOCK has to be covered by DUTies. |
| [Boarding Position](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370400/stops#stops-BoardingPosition) | A location within a QUAY from which passengers may directly board, or onto which passengers may directly alight from, a VEHICLE. |
| [Branding](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Branding) | An arbitrary marketing classification. |
| [CheckConstraint](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-CheckConstraintStructure) | Characteristics of e.g. SITE COMPONENT or SERVICE JOURNEY, such as check-in, security screening, ticket control or immigration, that may potentially incur a time penalty that should be allowed for when journey planning. |
| [Common Section](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-CommonSection) | A shared set of LINKS or POINTs. A part of a public transport network where the ROUTEs of several JOURNEY PATTERNs are going in parallel and where the synchronisation of SERVICE JOURNEYs may be planned and controlled with respect to commonly used LINKs and STOP POINTs. COMMON SECTIONs are defined arbitrarily and need not cover the total lengths of topologically bundled sections. |
| [Compound Train](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-CompoundTrain) | A VEHICLE TYPE composed of a sequence of more than one vehicles of the type TRAIN. |
| [Contact Details](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-ContactDetails) | Contact details for ORGANISATION for public use. |
| [Coupled Journey](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-CoupledJourney) | A complete journey operated by a coupled train, composed of two or more VEHICLE JOURNEYs remaining coupled together all along a JOURNEY PATTERN. A COUPLED JOURNEY may be viewed as a single VEHICLE JOURNEY. |
| [Crossing Equipment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-CrossingEquipment) | A specialisation of PLACE ACCESS EQUIPMENT for CROSSING EQUIPMENTs \(zebra, pedestrian lights, acoustic device sensors, tactile guide strips, etc.\). |
| [Cycle Storage Equipment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-CycleStorageEquipment) | Specialisation of PLACE EQUIPMENT for cycle storage. |
| [Data Managed Object](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-DataManagedObject) | An ENTITY in VERSION that can be associated with a RESPONSIBILITY SET that describes who has responsibility for managing the data. |
| [Data Source](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-DataSource) | The DATA SOURCE identifies the system which has produced the data. References to a data source are useful in an interoperated computer system. |
| [Day Type](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-DayType) | A type of day characterized by one or more properties which affect public transport operation. For example "weekday in school holidays". |
| [Day Type Assignment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-DayTypeAssignment) | Associates a DAY TYPE with an OPERATING DAY within a specific Calendar. A specification of a particular DAY TYPE which will be valid during a TIME BAND on an OPERATING DAY. |
| [Dead Run](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-DeadRun) | A non-service VEHICLE JOURNEY. |
| [Default Connection](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-DefaultConnection) | The physical \(spatial\) possibility for a passenger to change from one public transport vehicle to another to continue the trip. It specifies default times to be used to change from one mode of transport to another at an area or national level as specified by a TOPOGRAPHIC PLACE, STOP AREA or SITE ELEMENT. It may be restricted to a specific MODE or OPERATOR or only apply in a particular direction of transfer, e.g. bus to rail may have a different time for rail to bus. |
| [Delivery Variant](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-DeliveryVariant) | A variant text of a NOTICE for use in a specific media or delivery channel \(voice, printed material, etc\). |
| [Destination Display](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-DestinationDisplay) | An advertised destination of a specific JOURNEY PATTERN, usually displayed on a headsign, on the front of a vehicle, or at other onboard locations. This information can be updated dynamically as the journey progresses, in particular when crossing VAI points. |
| [Destination Display Variant](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370412/network#network-DestinationDisplayVariant) | Alternative DESTINATION DISPLAY, generally aimed at specific media \(SMS, email, etc\). |
| [Direction](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Direction) | A classification for the general orientation of ROUTEs. |
| DistributionChannel | An outlet for selling a product. |
| [Entity](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Entity) | Any data instance to be managed in an operational Version Management System. When several data sources coexist \(multimodality and/or interoperability\), an ENTITY has to be related to a given DATA SOURCE in which it is defined. |
| [Entity In Version](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-EntityInVersion) | The ENTITY associated to a given VERSION. |
| [Entrance](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370400/stops#stops-Entrance) | A physical entrance or exit to/from a SITE. Can be a door, barrier, gate or another recognizable point of access. |
| [Entrance Equipment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-EquipmentTypes) | A specialisation of PLACE ACCESS EQUIPMENT for ENTRANCEs \(door, barrier, revolving door, etc.\). |
| [Equipment](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Equipment) | An item of equipment installed either fixed \(PLACE EQUIPMENT\)  or on-board vehicles \(VEHICLE EQUIPMENT\). A service \(LOCAL SERVICE such as LEFT LUGGAGE, TICKETING SERVICE\) is considered as immaterial equipment as well. |
| [Equipment Place](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370400/stops#stops-EquipmentPlace) | Designated Place within a SITE for locating EQUIPMENT. |
| [Facility Set](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-FacilitySet) | A set of FACILITIES that may be associated with an ENTITY and subject to a specific VALIDITY CONDITION.  |
| Fare Product | An immaterial marketable element \(access rights, discount rights etc\), specific to a CHARGING MOMENT. |
| [Flexible Area](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370400/stops#stops-FlexibleArea) | A specialisation of a FLEXIBLE QUAY \(which is abstract\) to identify what is the catchment area for a flexible service \(so that a stop finder can find the nearest available types of transport\). It is a named zone visited by a particular mode of transport.  It is part of the SITE data set rather than the service data set, since it can be defined, and exists independently from an actual service. |
| [Flexible Line](handbok-n801-siri-netex-network.md#network-FlexibleLine) | A specialisation of LINE for flexible service. As all the service on a LINE may not all be flexible, flexibility itself is described at JOURNEY PATTERN level \(meaning that a separate JOURNEY PATTERN is needed for each type of flexibility available for the line\). |
| [Flexible Link Properties](handbok-n801-siri-netex-network.md#network-FlexibleLinkPro) | Set of properties describing the flexible characteristics of a LINK. A composition is used with LINK in order to avoid multiple inheritances and a type explosion of link subtypes |
| [Flexible Point Properties](handbok-n801-siri-netex-network.md#network-FlexiblePointProperties) | Set of characteristics describing the possible flexibility of POINTs. A composition is used with POINT in order to avoid multiple inheritances. |
| [Flexible Quay](handbok-n801-siri-netex-stops.md#stops-FlexibleQuay) | A physical ZONE such as a section of a road where a flexible service is available on demand. The existence of the zone makes the services visible to journey planners looking for available services for an area. |
| [Flexible Route](handbok-n801-siri-netex-network.md#network-FlexibleRoute) | A specialisation of ROUTE for flexible service.  May include both point and zonal areas and ordered and unordered sections. |
| [Flexible Service Properties](handbok-n801-siri-netex-network.md#network-FlexibleServiceProperties) | Additional characteristics of a FLEXIBLE SERVICE. A service may be partly fixed, partly flexible. |
| [Flexible Stop Assignment](handbok-n801-siri-netex-network.md#network-FlexibleStopAssignment) | Assignment of a SCHEDULED STOP POINT to a FLEXIBLE STOP PLACE and quay. etc. |
| [Flexible Stop Place](handbok-n801-siri-netex-stops.md#stops-FlexibleStopPlace) | A specialisation of the STOP PLACE describing a stop of a FLEXIBLE SERVICE. It may be composed of FLEXIBLE AREAs or HAIL AND RIDE AREAs identifying the catchment areas for flexible services \(when they use areas or flexible quays\). Some FLEXIBLE SERVICE also uses regular STOP PLACEs for their stops. When assigned to a SCHEDULED STOP POINT the corresponding SCHEDULED STOP POINT is supposed to be a ZONE \(the centroid point of the ZONE being the SCHEDULED STOP POINT\). |
| [Frequency](handbok-n801-siri-netex-timetable.md#timetable-Frequency) | The frequency of Journey. \(Type for a HEADWAY INTERVAL.\) |
| [General Group Of Entities]() | A grouping of ENTITies which will be commonly referenced for a specific purpose. |
| Generic Parameter Assignment | A VALIDITY PARAMETER ASSIGNMENT specifying generic access rights for a class of products \(e.g. a time band limit - 7 to 10 a.m. - for trips made with a student pass\). |
| Group Of Distribution Channels | A grouping of DISTRIBUTION CHANNELs. |
| [Group Of Entities]() | A set of ENTITies grouped together according to a PURPOSE OF GROUPING, e.g. grouping of stops known to the public by a common name. |
| [Group Of Lines](handbok-n801-siri-netex-network.md#network-GroupOfLines) | A grouping of lines which will be commonly referenced for a specific purpose. |
| [Group Of Operators]() | A group of OPERATORs having, for instance, common schemes for fare collection or passenger information. |
| [Group of Services](handbok-n801-siri-netex-timetable.md#timetable-GroupOfServices) | A group of SERVICEs, often known to its users by a name or a number. |
| Group of Sales Offer Packages | A grouping of SALES OFFER PACKAGEs |
| [Group Of Stop Places](handbok-n801-siri-netex-stops.md#stops-GroupOfStopPlaces) | A grouping of STOP PLACEs which will be commonly referenced for a specific purpose. The term corresponds to a specialisation of standard Transmodel concept GROUP OF ENTITIES. |
| [Hail And Ride Area](handbok-n801-siri-netex-stops.md#stops-HailAndRideArea) | A section of Road between two points within which one may hail a bus to board it or alight from it or ask it to stop to alight. |
| Headway Interval | A time interval or a duration defining a headway period and characterizing HEADWAY JOURNEY GROUP \(e.g. every 10 min, every  4-6 min\). |
| [Headway Journey Group](handbok-n801-siri-netex-timetable.md#timetable-HeadwayJourneyGroup) | A group of VEHICLE JOURNEYs following the same JOURNEY PATTERN having the same HEADWAY INTERVAL between a specified start and end time \(for example, every 10 min\). This is especially useful for passenger information. |
| [Interchange](handbok-n801-siri-netex-timetable.md#timetable-Interchange) | The scheduled possibility for transfer of passengers between two SERVICE JOURNEYs at the same or different STOP POINTs. |
| [Journey](handbok-n801-siri-netex-timetable.md#timetable-Journey) | Common properties of VEHICLE JOURNEYs and SPECIAL SERVICEs, e.g. their link to accounting characteristics. |
| [Journey Frequency Group](handbok-n801-siri-netex-timetable.md#timetable-JourneyFrequencyGroup) | A group of JOURNEYs defined in order to describe special behaviour like frequency-based services or rhythmical services \(runs all xxh10, xxh25 and xxh45... for example; this is especially useful for passenger information\). |
| [Journey Headway]() | Headway interval information that is available for all the VEHICLE JOURNEYs running on the JOURNEY PATTERN  for a given TIME DEMAND TYPE,  at a given TIMING POINT.  This is a default value that can be superseded by VEHICLE JOURNEY HEADWAY. This information must be consistent with HEADWAY JOURNEY GROUP if available \(HEADWAY JOURNEY GROUP being a more detailed way of describing headway services\). |
| [Journey Layover]() | Time allowance at the end of each journey on a specified JOURNEY PATTERN, to allow for delays and for other purposes. This layover supersedes any global layover and may be superseded by a specific VEHICLE JOURNEY LAYOVER. |
| [Journey Meeting](handbok-n801-siri-netex-timetable.md#timetable-JourneyMeeting) | A time constraint for one or several SERVICE JOURNEYs fixing interchanges between them and/or an external event \(e.g. arrival or departure of a feeder line, the opening time of the theatre, etc.\). |
| [Journey Part](handbok-n801-siri-netex-timetable.md#timetable-JourneyPart) | A part of a VEHICLE JOURNEY created according to a specific functional purpose, for instance in situations when vehicle coupling or separating occurs. |
| [Journey Part Couple](handbok-n801-siri-netex-timetable.md#timetable-JourneyPartCouple) | Two JOURNEY PARTs of different VEHICLE JOURNEYs served simultaneously by a train set up by coupling their single vehicles. |
| [Journey Pattern](handbok-n801-siri-netex-network.md#network-JourneyPattern) | An ordered list of SCHEDULED STOP POINTs and TIMING POINTs on a single ROUTE, describing the pattern of working for public transport vehicles. A JOURNEY PATTERN may pass through the same POINT more than once. The first point of a JOURNEY PATTERN is the origin. The last point is the destination. |
| [Journey Pattern Run Time]() | The JOURNEY PATTERN RUN TIME is the time taken to traverse a TIMING LINK in a particular JOURNEY PATTERN, for a specified TIME DEMAND TYPE. If it exists, it will override the DEFAULT SERVICE JOURNEY RUN TIME and DEFAULT DEAD RUN RUN TIME. |
| [Journey Pattern Wait Time]() | The JOURNEY PATTERN WAIT TIME represents the time a vehicle has to wait at a specific TIMING POINT IN JOURNEY PATTERN, for a specified TIME DEMAND TYPE. This wait time can be superseded by a VEHICLE JOURNEY WAIT TIME. |
| [Journey Run Time]() | The time it takes to traverse a TIMING LINK in a particular JOURNEY PATTERN, for a specified TIME DEMAND TYPE. If it exists, it will override the DEFAULT SERVICE JOURNEY RUN TIME and DEFAULT DEAD RUN RUN TIME. |
| [Journey Timing]() | Time-related information referring to journey timing whose value depends on the time of use and so can be associated with a TIME DEMAND TYPE, TIME BAND or OPERATIONAL CONTEXT. |
| [Journey Wait Time]() | The time a vehicle has to wait at a specific TIMING POINT IN JOURNEY PATTERN, for a specified TIME DEMAND TYPE. This wait time can be superseded by a VEHICLE JOURNEY WAIT TIME. |
| [Key List]() | A list of alternative Key values for an element. |
| [Level](handbok-n801-siri-netex-stops.md#stops-Level) | An identified storey \(ground, first, basement, mezzanine, etc\) within an interchange building or SITE on which SITE COMPONENTs reside. A PATH LINK may connect components on different levels. |
| [Line](handbok-n801-siri-netex-network.md#network-Line) | A group of ROUTEs which is generally known to the public by a similar name or number. |
| [Line Network](handbok-n801-siri-netex-network.md#network-LineNetwork) | A description of the topological connectivity of a LINE as a set of LINE SECTIONs. This is sufficient to draw a route map for the whole line including branches and loops. |
| [Line Section](handbok-n801-siri-netex-network.md#network-LineSection) | A part of a NETWORK comprising an edge between two nodes. Not directional.  |
| [Link]() | An oriented spatial object of dimension 1 in view of the overall description of a network, describing a connection between two POINTs. |
| [Link In Journey Pattern](handbok-n801-siri-netex-network.md#network-LinkInJourneyPattern) | A SERVICE LINK or TIMING LINK in a JOURNEY PATTERN with its order in that JOURNEY PATTERN. |
| [Link In Link Sequence]() | The order of a LINK in a LINK SEQUENCE to which it belongs. |
| [Link Sequence]() | An ordered sequence either of POINTs or of LINKs, defining a path through the network. |
| [Location]() | The position of a POINT with a reference to a given LOCATING SYSTEM \(e. g. coordinates\). |
| [Luggage Service]() | A specialisation of CUSTOMER SERVICE for LUGGAGE SERVICE \(provides luggage service attributes like luggage trolley, free to use, etc.\). |
| [Navigation Path](handbok-n801-siri-netex-stops.md#stops-NavigationPath) | A designated path between two places. May include an ordered sequence of PATH LINKs. |
| [Network](handbok-n801-siri-netex-network.md#network-Network) | A named grouping of LINEs under which a transport network is known. |
| [Notice]() | A text for informational purposes on exceptions in a LINE, a JOURNEY PATTERN, etc. The information may be useful for passenger or driver information. |
| [Notice Assignment]() | The assignment of a NOTICE showing an exception in a JOURNEY PATTERN, a COMMON SECTION, or a VEHICLE JOURNEY, possible specifying at which POINT IN JOURNEY PATTERN the validity of the NOTICE starts and ends respectively. |
| [Operating Day]() | A day of public transport operation in a specific calendar. An OPERATING DAY may last more than 24 hours. |
| [Operating Period]() | A continuous interval of time between two OPERATING DAYs which will be used to define validities. |
| [Operator]() | A company providing public transport services. |
| [Organisation]() | A legally incorporated body associated with any aspect of the transport system. |
| [Organisation Part]() | A named subdivision of an ORGANISATION. |
| [Parking](handbok-n801-siri-netex-stops.md#stops-Parking) | A named place where Parking may be accessed. Can be a building complex \(e.g. a station\) or an on-street location. |
| [Parking Area](handbok-n801-siri-netex-stops.md#stops-ParkingArea) | An area within a PARKING. |
| [Parking Capacity](handbok-n801-siri-netex-stops.md#stops-ParkingCapacity) | The capacity of a PARKING. |
| [Parking Properties](handbok-n801-siri-netex-stops.md#stops-ParkingProperties) | PARKING specific properties other than its CAPACITY. |
| [Passenger Equipment]() | Equipment for passengers that may be in a fixed within a STOP PLACE. |
| [Passenger Stop Assignment](handbok-n801-siri-netex-network.md#network-PassengerStopAssignment) | The allocation of a SCHEDULED STOP POINT \(i.e. a SCHEDULED STOP POINT of a SERVICE PATTERN or JOURNEY PATTERN\) to a specific STOP PLACE for a SERVICE JOURNEY, and also possibly a QUAY and BOARDING POSITION. |
| [Passing Time](handbok-n801-siri-netex-timetable.md#timetable-TimetabledPassingTime) | Time data concerning public transport vehicles passing a particular POINT; e.g. arrival time, departure time, waiting time. |
| [Path Junction](handbok-n801-siri-netex-stops.md#stops-PathJunction) | A designated point, inside or outside of a STOP PLACE or POINT OF INTEREST, at which two or more PATH LINKs may connect or branch. |
| [Path Link](handbok-n801-siri-netex-stops.md#stops-PathLink) | A link between any two PLACEs \(That is STOP PLACEs, ACCESS SPACEs or QUAYs, BOARDING POSITIONs, POINTs OF INTEREST etc or PATH JUNCTIONs\) that represents a step in a possible route for pedestrians, cyclists or other out of vehicle passengers within or between a PLACE. |
| [Place]() | A geographic place of any type which may be specified as the origin or destination of a trip. A PLACE may be represented as a POINT \(dimension 0\) , a road section \(dimension 1\) or a ZONE \(dimension 2\). |
| [Place Lighting]() | A specialisation of PLACE EQUIPMENT for LIGHTING EQUIPMENT \(e.g. lamp post\). |
| [Point]() | A 0-dimensional node of the network used for the spatial description of the network. POINTs may be located by a LOCATION in a given LOCATING SYSTEM. |
| [Point In Link Sequence]() | A POINT in a LINK SEQUENCE indicating its order in that particular LINK SEQUENCE. |
| [Point Of Interest](handbok-n801-siri-netex-stops.md#stops-PointOfInterest) | A type of SITE to or through which passengers may wish to navigate as part of their journey and which is modelled in detail by journey planners. |
| [Point On Route](handbok-n801-siri-netex-network.md#network-PointOnRoute) | A ROUTE POINT used to define a ROUTE with its order on that ROUTE. |
| [Point Projection]() | An oriented correspondence from one POINT of a source layer, onto an entity in a target layer:  e.g. POINT, LINK, LINK SEQUENCE, COMPLEX FEATURE, within a defined TYPE OF PROJECTION. |
| [Postal Address]() | A specification of ADDRESS refining it by using the attributes used for conventional identification for mail. Comprises variously a building Identifier, Street name, Postcode and other descriptors. |
| Preassigned Fare Product | A FARE PRODUCT consisting of one or several VALIDABLE ELEMENTs, specific to a CHARGING MOMENT. |
| [Projection]() | An oriented correspondence - of the shape of an ENTITY on a source layer, - onto an ENTITY in a target layer: e.g. POINT, LINK, LINK SEQUENCE, COMPLEX FEATURE, - within a defined TYPE OF PROJECTION. |
| [Property Of Day]() | A property which a day may possess, such as school holiday, weekday, summer, winter etc. |
| [Quay](handbok-n801-siri-netex-stops.md#stops-Quay) | A place such as a platform, stance, or quayside where passengers have access to PT vehicles, Taxi, cars or other means of transportation. A QUAY may serve one or more VEHICLE STOPPING PLACEs and be associated with one or more STOP POINTS. A QUAY may contain other sub QUAYs. A child QUAY must be physically contained within its parent QUAY. |
| [Ramp Equipment]() | A specialisation of PLACE ACCESS EQUIPMENT for RAMPs \(provides ramp attributes like length, gradient, etc.\). |
| Refunding | Whether and how the product may be refunded. |
| [Road Address]() | A specialisation of ADDRESS refining it by using the characteristics such as road number, and name used for conventional identification of along a road. |
| [Rough Surface]() | A specialisation of PLACE EQUIPMENT for rough surfaces, giving properties of surface texture, mainly for impaired person information. |
| [Route](handbok-n801-siri-netex-network.md#network-Route) | An ordered list of located POINTs defining one single path through the road \(or rail\) network. A ROUTE may pass through the same POINT more than once. |
| [Route Link](handbok-n801-siri-netex-network.md#network-RouteLink) | An oriented link between two ROUTE POINTs allowing the definition of a unique path through the network. |
| [Route Point](handbok-n801-siri-netex-network.md#network-RoutePoint) | A POINT used to define the shape of a ROUTE through the network. |
| [Rhythmical Journey Group](handbok-n801-siri-netex-timetable.md#timetable-RhythmicalJourneyGroup) | A group of VEHICLE JOURNEYs following the same JOURNEY PATTERN having the same "rhythm" every hour \(for example, ‘runs at xxh10, xxh25 and xxh45 past the hour’\) between a specified start and end time. |
| Sales Offer Package Substitution | SALES OFFER PACKAGE that may be used to substitute base SALES OFFER PACKAGE. |
| [Sanitary Equipment]() | A SANITARY FACILITY, e.g. WC, Shower, baby change. |
| [Scheduled Stop Point](handbok-n801-siri-netex-network.md#network-ScheduledStopPoint) | A POINT where passengers can board or alight from vehicles. |
| [Schematic Map](handbok-n801-siri-netex-network.md#network-SchematicMap) | A map representing schematically the layout of the topographic structure of PLACEs \(e.g. a set of SITEs\) or the public transport network \(a set of LINEs\). It can include a pixel projection of a set of ENTITies onto a bitmap image so as to support hyperlinked interactions. |
| [Schematic Map Member](handbok-n801-siri-netex-network.md#network-SchematicMapMember) | Projection of a transport network object on a SCHEMATIC MAP. |
| [Service Calendar](handbok-n801-siri-netex-timetable.md#timetable-ServiceCalendar) | A collection of DAY TYPE ASSIGNMENTs. |
| [Service Exclusion](handbok-n801-siri-netex-network.md#network-ServiceExclusion) | A constraint on the use of a service. The service, on this specific JOURNEY PATTERN \(usually an FTS JOURNEY PATTERN\), cannot operate when another \(regular\) service operates. This may occur only on a subpart of the JOURNEY PATTERN, or only on one or some specific SCHEDULED STOP POINTs within the pattern. |
| [Service Facility Set]() | Set of FACILITies available for a SERVICE JOURNEY or a JOURNEY PART. The set may be available only for a specific VEHICLE TYPE within the SERVICE \(e.g. carriage built with a low floor\). |
| [Service Journey](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourney) | A passenger-carrying VEHICLE JOURNEY for one specified DAY TYPE. The pattern of working is in principle defined by a SERVICE JOURNEY PATTERN. |
| [Service Journey Interchange](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourneyInterchange) | The scheduled possibility for transfer of passengers between two SERVICE JOURNEYs at the same or different STOP POINTs. |
| [Service Link](handbok-n801-siri-netex-network.md#network-ServiceLink) | A LINK between an ordered pair of STOP POINTs.  Service links are directional - there will be separate links for each direction of a route. |
| [Service Link In Journey Pattern](handbok-n801-siri-netex-network.md#network-ServiceLinkInJourneyPattern) | The use of a SERVICE LINK in a specified order within a JOURNEY PATTERN or SERVICE PATTERN. |
| [Shelter Equipment]() | A specialisation of WAITING EQUIPMENT for a SHELTER. |
| [Sign Equipment]() | SIGN EQUIPMENT can define signs visible to passengers at places in a SITE, such as PLACE SIGNS, DIRECTION SIGNs, etc. these can be used to provide guidance.  |
| [Site](handbok-n801-siri-netex-stops.md#stops-Site) | A type of PLACE, such as a STOP PLACE, POINT OF INTEREST or ADDRESS, to which passengers may wish to travel. A SITE can have designated ENTRANCEs that represent the available points of access for different USER NEEDs. |
| [Site Connection](handbok-n801-siri-netex-stops.md#stops-SiteConnection) | The physical \(spatial\) possibility for a passenger to change from one public transport vehicle to another to continue the trip, determined by physical locations, such as SITEs and/or its components and/or ENTRANCEs, in particular, STOP PLACEs and/or its components. Different times may be necessary to cover the resulting distance, depending on the kind of passenger. |
| [Site Element](handbok-n801-siri-netex-stops.md#stops-SiteElement) | A type of PLACE specifying common properties of a SITE or a SITE COMPONENT  to describe it., including accessibility. |
| [Site Equipment]() | A specialisation of PLACE EQUIPMENT for SITEs \(e.g. LUGGAGE LOCKER, WAITING EQUIPMENT, TROLLEY STAND, etc.\)  |
| [Site Facility Set](handbok-n801-siri-netex-stops.md#stops-SiteFacilitySet) | Set of enumerated FACILITY values that are relevant to a SITE \(names based on TPEG classifications, augmented with UIC etc.\). |
| [Special Service](handbok-n801-siri-netex-timetable.md#timetable-SpecialService) | A passenger-carrying VEHICLE JOURNEY for one specified DAY TYPE. The pattern of working is in principle defined by a SERVICE JOURNEY PATTERN. |
| [Stop Assignment](handbok-n801-siri-netex-network.md#network-StopAssignment) | The allocation of a SCHEDULED STOP POINT \(i.e. a SCHEDULED STOP POINT of a SERVICE PATTERN or JOURNEY PATTERN\) to a specific STOP PLACE, for either a Passenger JOURNEY or VEHICLE SERVICE. |
| [Stop Place](handbok-n801-siri-netex-stops.md#stops-StopPlace) | A place comprising one or more locations where vehicles may stop and where passengers may board or leave vehicles or prepare their trip. A STOP PLACE will usually have one or more well-known names. |
| [Stop Place Space](handbok-n801-siri-netex-stops.md#stops-StopPlaceSpace) | A physical area within a STOP PLACE, for example, a QUAY, BOARDING POSITION, ACCESS SPACE or EQUIPMENT PLACE. |
| [Stop Point In Journey Pattern](handbok-n801-siri-netex-network.md#network-StopPointInJourneyPattern) | A POINT in a JOURNEY PATTERN which is a SCHEDULED STOP POINT. |
| [Suitability]() | A statement of whether a particular USER NEED can be met. It can be used to state whether a SITE can be accessed by a passenger with a particular USER NEED. |
| [Tariff Zone](handbok-n801-siri-netex-network.md#network-TariffZone) | A ZONE used to define a zonal fare structure in a zone-counting or zone-matrix system. |
| [Template Service Journey](handbok-n801-siri-netex-timetable.md#timetable-TemplateServiceJourney) | A VEHICLE JOURNEY with a set of frequencies that may be used to represent a set of similar journeys differing only by their time of departure. |
| [Template Vehicle Journey](handbok-n801-siri-netex-timetable.md#timetable-TemplateVehicleJourney) | A repeating VEHICLE JOURNEY for which a frequency has been specified, either as a HEADWAY JOURNEY GROUP \(e.g. every 20 minutes\) or a RHYTHMICAL JOURNEY GROUP \(e.g. at 15, 27 and 40 minutes past the hour\) has been specified. |
| [Ticketing Equipment]() | A specialisation of PASSENGER EQUIPMENT for TICKETING |
| [Ticket Validator Equipment]() | A specialisation of PASSENGER EQUIPMENT \(PLACE EQUIPMENT\) for TICKET VALIDATOR. |
| [Timeband]() | A period in a day, significant for some aspect of public transport, e.g. similar traffic conditions or fare category. |
| [Timetable](handbok-n801-siri-netex-timetable.md) | A set of timetable data \(VEHICLE JOURNEYs, etc.\) to which the same VALIDITY CONDITIONs have been assigned. |
| [Timetabled Passing Time](handbok-n801-siri-netex-timetable.md#timetable-TimetabledPassingTime) | Long-term planned time data concerning public transport vehicles passing a particular POINT IN JOURNEY PATTERN on a specified VEHICLE JOURNEY for a certain DAY TYPE. |
| [Timing Link]() | An ordered pair of TIMING POINTs for which run times may be recorded. |
| [Timing Link In Journey Pattern](handbok-n801-siri-netex-network.md#network-TimingLinkInJourneyPattern) | The position of a TIMING LINK in a JOURNEY PATTERN. This ENTITY is needed if a TIMING LINK is repeated in the same JOURNEY PATTERN, and separate information is to be stored about each iteration of the TIMING LINK. |
| [Timing Point](handbok-n801-siri-netex-network.md#network-TimingPoint) | A POINT against which the timing information necessary to build schedules may be recorded. |
| [Timing Point In Journey Pattern](handbok-n801-siri-netex-network.md#network-TimingPointInJourneyPattern) | A NODE in a JOURNEY PATTERN which is a TIMING POINT. |
| [Topographic Place](handbok-n801-siri-netex-stops.md#stops-TopographicPlace) | A type of PLACE providing the topographical context when searching for or presenting travel information, for example as the origin or destination of a trip. It may be of any size \(e.g. County, City, Town, Village\) and of different specificity \(e.g. Greater London, London, West End, Westminster, St James s\). A TOPOGRAPHICAL PLACE must always have an official name. |
| [Train]() | A vehicle composed of TRAIN ELEMENTs in a certain order, i.e. of wagons assembled together and propelled by a locomotive or one of the wagons. |
| [Train Component]() | A specification of the order of TRAIN ELEMENTs in a TRAIN. |
| [Train Element]() | An elementary component of a TRAIN \(e.g. wagon, locomotive\). |
| [Train In Compound Train]() | An instance of a TRAIN making up a COMPOUND TRAIN. |
| [Train Stop Assignment](handbok-n801-siri-netex-network.md#network-TrainStopAssignment) | The association of a TRAIN COMPONENT at a SCHEDULED STOP POINT with a specific STOP PLACE and also possibly a QUAY and BOARDING POSITION. |
| [Transfer](handbok-n801-siri-netex-network.md#network-Transfer) | The possibility of a passenger to transfer between two PLACEs. May have times associated with the transfer. |
| [Transfer Duration](handbok-n801-siri-netex-network.md#network-TransferDuration) | The time it takes to complete a TRANSFER. |
| [Type Of Service](handbok-n801-siri-netex-network.md#network-TypeOfService) | Classification of a Service. |
| UsageParameter | A parameter used to specify the use of a SALES OFFER PACKAGE or a FARE PRODUCT. |
| UsageParameterPrice | A set of all possible price features of a USAGE PARAMETER: discount in value or percentage etc. |
| [Valid Between]() | A simple version of a VALIDITY CONDITION. Comprises a simple period. NO UNIQUENESS CONSTRAINT. |
| [Validity Condition]() | Condition used in order to characterise a given VERSION of a VERSION FRAME. A VALIDITY CONDITION consists of a parameter \(e.g. date, triggering event, etc.\) and its type of application  \(e.g. for,  from,  until, etc.\). |
| [Validity Parameter Assignment]() | An ACCESS RIGHT PARAMETER ASSIGNMENT relating a fare collection parameter to a theoretical FARE PRODUCT \(or one of its components\) or a SALES OFFER PACKAGE. |
| [Validity Trigger]() | External event defining a VALIDITY CONDITION.  E.g exceptional flow of a river, bad weather, road closure for works. |
| [Vehicle]() | A public transport vehicle used for carrying passengers. |
| [Vehicle Journey](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourney) | The planned movement of a public transport vehicle on a DAY TYPE from the start point to the endpoint of a JOURNEY PATTERN on a specified ROUTE. |
| [Vehicle Journey Headway](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourneyHeadway) | Headway interval information that is available for a VEHICLE JOURNEY \(to be understood as the delay between the previous and the next VEHICLE JOURNEY\). This information must be consistent with HEADWAY JOURNEY GROUP if available \(HEADWAY JOURNEY GROUP being a more detailed way of describing headway services\). |
| [Vehicle Journey Layover](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourneyLayover) | A time allowance at the end of a specified VEHICLE JOURNEY. This time supersedes any global layover or JOURNEY PATTERN LAYOVER. |
| [Vehicle Journey Run Time](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourneyRunTime) | The time it takes to traverse a specified TIMING LINK IN JOURNEY PATTERN on a specified VEHICLE JOURNEY. This gives the most detailed control over times and overrides the DEFAULT SERVICE JOURNEY RUN TIME and JOURNEY PATTERN RUN TIME and the DEFAULT DEAD RUN RUN TIME. There may be different times for different TIME DEMAND TYPES. |
| [Vehicle Journey Wait Time](handbok-n801-siri-netex-timetable.md#timetable-VehicleJourneyWaitTime) | The time for a vehicle to wait at a particular TIMING POINT IN JOURNEY PATTERN on a specified VEHICLE JOURNEY. This wait time will override the JOURNEY PATTERN WAIT TIME. |
| [Vehicle Type]() | Type of VEHICLE. |
| Version | A group of operational data instances which share the same VALIDITY CONDITIONs. A version belongs to a unique VERSION FRAME and is characterized by a unique TYPE OF VERSION. |
| VersionedChild | A child ENTITY whose RESPONSIBILITY SET must be the same as its containing parent object, and which cannot exist independently of its parent in a repository, for example, a POINT IN PATTERN. Thus in practice, if the parent is deleted, so will the child be. |
| [Via](handbok-n801-siri-netex-network.md#network-Via) | A location \(e.g. a ROUTE POINT\) used to distinguish a ROUTE from another ROUTE. It may be used for DESTINATION DISPLAYs |
| [Waiting Equipment]() | A specialisation of SITE EQUIPMENT for WAITING EQUIPMENTs \(shelter, waiting room, etc.\). |
| [Zone]() | A two-dimensional PLACE within the service area of a public transport operator \(administrative zone, TARIFF ZONE, ACCESS ZONE, etc.\). |
| [Zone Projection]() | An oriented correspondence from one ZONE in a source layer,  onto a target entity: e.g.  POINT, COMPLEX FEATURE, within a defined TYPE OF PROJECTION. |

