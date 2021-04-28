# Håndbok N801 \(SIRI/NeTEX\) : StopPlace - complex

**Content**

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591717435 {padding: 0px;}  
div.rbtoc1619591717435 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591717435 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Complex stop place area "Oslo S - Jernbanetorget"](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-Complexstopplacearea%22OsloS-Jernbanetorget%22)
  * [Group of StopPlaces with multiple multimodal- and monomodal StopPlaces](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-GroupofStopPlaceswithmultiplemultimodal-andmonomodalStopPlaces)
  * [Link](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-Link)
  * [Modelling](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-Modelling)
    * [Model](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-Model)
    * [Illustration](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-Illustration)
  * [Elements](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-Elements)
    * [GroupOfStopPlaces](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-GroupOfStopPlaces)
    * [StopPlace](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-StopPlace)
    * [boardingPositions](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-boardingPositions)
    * [AccessSpace](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-AccessSpace)
    * [NavigationPath](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-NavigationPath)
    * [SiteFacilitySet](handbok-n801-siri-netex-stopplace-complex.md#StopPlace-complex-SiteFacilitySet)

## Complex stop place area "Oslo S - Jernbanetorget" <a id="StopPlace-complex-Complexstopplacearea&quot;OsloS-Jernbanetorget&quot;"></a>

Please note that this example doesn't represent the _actual_ modelling in the national stop place registry.

### Group of StopPlaces with multiple multimodal- and monomodal StopPlaces <a id="StopPlace-complex-GroupofStopPlaceswithmultiplemultimodal-andmonomodalStopPlaces"></a>

Jernbanetorget and Oslo S constitutes a public transport hub which can be modelled as a [Group of Stop Places](handbok-n801-siri-netex-stops.md#stops-GroupOfStopPlaces), where each part of the stop place area is modelled as a [multimodal stop place](handbok-n801-siri-netex-stops.md#stops-MultimodalStopPlace) or a [monomodal stop place](handbok-n801-siri-netex-stops.md#stops-MonomodalStopPlace).

Stop places are served by several transport modes, such as trains, metros, trams and buses, where some stop places connected to the area serve more than one transport mode. Some of the stops are indoors, or underground, while others can be found on the street level, connected to the road network. This means that the stops have different facilities depending on transport modality and location and that the area has some services that apply across the various stop places.

### Link <a id="StopPlace-complex-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/stops/OsloS\_station\_example.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/OsloS_station_example.xml)

### Modelling <a id="StopPlace-complex-Modelling"></a>

All StopPlaces for trains, buses, trams and taxis are logically linked into one stop area. In this stop area, there are 19 train tracks, two metro tracks, two tram stops, two bus stops and a taxi stop.

The model can look like this:

* Train
  * One Parent Quay for each platform with two Quays \(one for each side of the platform\) which each contain several BoardingPositions. _\(Nesting of Quays is outdated and the example will be remodelled_ in the next version of Norwegian NeTEx Profile\)
  * Parent quays are gathered in a single StopPlace representing the train station. _\(Nesting of Quays is outdated and the example will be remodelled in the next version of Norwegian NeTEx Profile\)_
* Metro
  * Two Quay objects \(one in each direction\) gathered in one StopPlace
* Bus/Tram just outside Oslo S \(bus and Tram do not share a platform\)
  * Two Quays under a StopPlace for bus
  * Two Quays under a StopPlace for the tram
  * One Parent StopPlace \(multimodal\) to above the bus and tram stop places
* Bus \(between Byporten and Oslo City\)
  * One StopPlace with two Quays
* Tram \(in front of Clarion Hotel\)
  * One StopPlace with two Quays
* One GroupOfStopPlaces to gather all the parent StopPlace objects

#### Model <a id="StopPlace-complex-Model"></a>

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy4825188674644314975",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563946&pageId=&name=Kompleks+Stoppestedsomr%C3%A5de&attachmentId=att728825982&pagePin=&imageAttachmentId=att728662202&border=&chrome=&html5=&size=&ceoId=&macroId=b0c0a5cf-6a12-4e42-bd0b-16f9d5ec9f2d&spaceKey=&version=&migration=1&previewPageId=728563946&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy4825188674644314975&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI2Y2Q3ZDYyZDEwNzQzNWMwYjEyNmM1MTcyODIxY2I2NTI2YTdmNWY2MDcwYmViNTg3MDJhMTMxMGYzNTA0MWZmIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg5NywiaWF0IjoxNjE5NTkxNzE3fQ.JDdOiFfOuVD0bUnLfVUDqXfNrxEsJKwpa8GUBnqxQzM",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiOWEyMzBhNWItOTQxNi00MWE5LThhYzktYmYxMWNlZTU4ZjNhIiwiaWQiOiI5YTIzMGE1Yi05NDE2LTQxYTktOGFjOS1iZjExY2VlNThmM2EifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxMiIsImlkIjoiNzI4NTYzOTQ2In0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjE3LCJpYXQiOjE2MTk1OTE3MTd9.vGJJVqcMdssI-A4-6ISAvrs3K3nwh6iiIdSUpBkrlqg",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"9a230a5b-9416-41a9-8ac9-bf11cee58f3a\",\"id\":\"9a230a5b-9416-41a9-8ac9-bf11cee58f3a\"},\"content\":{\"type\":\"page\",\"version\":\"12\",\"id\":\"728563946\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563946\",\"macro.hash\":\"9a230a5b-9416-41a9-8ac9-bf11cee58f3a\",\"page.type\":\"page\",\": = \| RAW \| = :\":\"imageAttachmentId=att728662202\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=b0c0a5cf-6a12-4e42-bd0b-16f9d5ec9f2d\|migration=1\|name=Kompleks Stoppestedsomr\u00e5de\|diagramAttachmentId=att728825982\|containerId=728563946\|timestamp=1550832581236\",\"space.id\":\"637370369\",\"diagramAttachmentId\":\"att728825982\",\"containerId\":\"728563946\",\"timestamp\":\"1550832581236\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"content.version\":\"12\",\"page.title\":\"StopPlace - complex\",\"macro.body\":\"\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"12\",\"imageAttachmentId\":\"att728662202\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"b0c0a5cf-6a12-4e42-bd0b-16f9d5ec9f2d\",\"content.id\":\"728563946\",\"migration\":\"1\",\"name\":\"Kompleks Stoppestedsomr\u00e5de\",\"macro.id\":\"9a230a5b-9416-41a9-8ac9-bf11cee58f3a\"}",  
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


#### Illustration <a id="StopPlace-complex-Illustration"></a>

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy5224884843923871308",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563946&pageId=&name=OsloS-Jernbanetorget-illustrasjon&attachmentId=att728891576&pagePin=&imageAttachmentId=att728760406&border=&chrome=&html5=&size=&ceoId=&macroId=a1f8aa51-3cb9-4ff8-bdd9-fe31237261f4&spaceKey=&version=&migration=&previewPageId=728563946&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy5224884843923871308&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI4YTRkNzZjZTMwZDU0OWQ5ZmM3OGQ1ODk2YTBjNTlmYTZmOWJhOTExYjk3MGJmN2E1NTlmOTllMDhjOTM1YjA3IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg5NywiaWF0IjoxNjE5NTkxNzE3fQ.qaVqjuNGOHURjvR1Jlsh8h2wgyw8UUsuP-NcqSrAvhc",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYmI0OGNkZDUtY2Q4NC00YWM3LWJhMTItNTllYjY4Zjk3Zjg0IiwiaWQiOiJiYjQ4Y2RkNS1jZDg0LTRhYzctYmExMi01OWViNjhmOTdmODQifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxMiIsImlkIjoiNzI4NTYzOTQ2In0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjE3LCJpYXQiOjE2MTk1OTE3MTd9.ZE8-co3p6AF3liEeHwpfIVPZAMkrdiFEvlY99BAuQBk",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"bb48cdd5-cd84-4ac7-ba12-59eb68f97f84\",\"id\":\"bb48cdd5-cd84-4ac7-ba12-59eb68f97f84\"},\"content\":{\"type\":\"page\",\"version\":\"12\",\"id\":\"728563946\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563946\",\"macro.hash\":\"bb48cdd5-cd84-4ac7-ba12-59eb68f97f84\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"12\",\"page.title\":\"StopPlace - complex\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728760406\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=a1f8aa51-3cb9-4ff8-bdd9-fe31237261f4\|name=OsloS-Jernbanetorget-illustrasjon\|diagramAttachmentId=att728891576\|containerId=728563946\|timestamp=1550151454493\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"12\",\"imageAttachmentId\":\"att728760406\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"a1f8aa51-3cb9-4ff8-bdd9-fe31237261f4\",\"content.id\":\"728563946\",\"name\":\"OsloS-Jernbanetorget-illustrasjon\",\"macro.id\":\"bb48cdd5-cd84-4ac7-ba12-59eb68f97f84\",\"diagramAttachmentId\":\"att728891576\",\"containerId\":\"728563946\",\"timestamp\":\"1550151454493\"}",  
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


  
**Alternativt modelleringseksempel**![](../.gitbook/assets/grey_arrow_down.png)Flyplass \(Gardermoen\)

Another example of a complex stop is an airport, in this case Oslo Airport, Gardermoen. It has several bus and taxi stop places in front of the main terminal, plus the train platforms below them. The airport consists of various airport terminals with their gates:

* Aircraft related 
  * Each gate is a Quay
  * Gates can be grouped for "Domestic", "Schengen", "Rest-of-the-world" _\(Nesting of Quays is outdated and the example will be remodeled_ in the next version of Norwegian NeTEx Profile\)
  * All Quays are collected in one StopPlace which describes the terminal.
  * A StopPlace with two Quays for Flytog _\(Dividing airport trains and regular trains into separate stop places is outdated and the example will be remodeled_ in the next version of Norwegian NeTEx Profile\)
  * A StopPlace with two Quays for regular trains _\(Dividing airport trains and regular trains into separate stop places is outdated and the example will be remodeled_ in the next version of Norwegian NeTEx Profile\)
  * a parent StopPlace for rail transport _\(Dividing airport trains and regular trains into separate stop places is outdated and the example will be remodeled_ in the next version of Norwegian NeTEx Profile\)
* Road-based 
  * Quays for each bus stop.
  * Quays for each taxi stop.
  * One StopPlace for buses and one StopPlace for taxis.
  * A parent StopPlace \(multimodal\) for bus/taxi.
* A GroupOfStopPlaces to gather all multimodal StopPlaces.

**Model**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy1415536156155592124",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563946&pageId=&name=flyplass-gardermoen-modell&attachmentId=&pagePin=&imageAttachmentId=&border=&chrome=&html5=&size=&ceoId=&macroId=&spaceKey=&version=&migration=&previewPageId=&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy1415536156155592124&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiIyNTc2YzQ5MjE4Y2FlOWJkNzQ5ZWI2YTI1MzcyYjkzZGU0ODllMzQ3NDYxM2QxMjNlYTk1ZWVkZTBiMjIyNzk2IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg5NywiaWF0IjoxNjE5NTkxNzE3fQ.vrvpmwgNu7gIY5e5vqnfDfK-FJUWgTvuTvp9ITUaqtA",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiOGUzM2M1MzktZDhlMy00YjExLTlkOWMtZjk2ZmIwMTRjYTVjIiwiaWQiOiI4ZTMzYzUzOS1kOGUzLTRiMTEtOWQ5Yy1mOTZmYjAxNGNhNWMifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxMiIsImlkIjoiNzI4NTYzOTQ2In0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjE3LCJpYXQiOjE2MTk1OTE3MTd9.eIfWYyNNpXYAKKxcNScyH6EJJ7M203kEgs2WBB2IngU",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"8e33c539-d8e3-4b11-9d9c-f96fb014ca5c\",\"id\":\"8e33c539-d8e3-4b11-9d9c-f96fb014ca5c\"},\"content\":{\"type\":\"page\",\"version\":\"12\",\"id\":\"728563946\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563946\",\"macro.hash\":\"8e33c539-d8e3-4b11-9d9c-f96fb014ca5c\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"12\",\"page.title\":\"StopPlace - complex\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"name=flyplass-gardermoen-modell\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"12\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"content.id\":\"728563946\",\"name\":\"flyplass-gardermoen-modell\",\"macro.id\":\"8e33c539-d8e3-4b11-9d9c-f96fb014ca5c\"}",  
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


**Illustration**

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy7773727812964208181",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728563946&pageId=&name=flyplass-gardermoen-illustrasjon&attachmentId=att728760410&pagePin=&imageAttachmentId=att728727693&border=&chrome=&html5=&size=&ceoId=&macroId=ab4c2afe-a03f-4b2c-af14-3cc65fc5a2a8&spaceKey=&version=&migration=&previewPageId=728563946&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy7773727812964208181&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI2NGRjOTU4ZDczMWQxOGIwODljZTJkMzk5OWEwMGUzOThmOGNmY2E5MjA4OGEwNTFhM2FkM2QwYmVhN2ZiYjk1IiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg5NywiaWF0IjoxNjE5NTkxNzE3fQ.Jn-l7zij1j-axOBMXDIGRXPhVnph3BZl0fPvhNFAHks",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZGY1NWYwMTEtOTE1OS00MGJjLWIzZjEtZGU3YjdlMDQ4Y2VmIiwiaWQiOiJkZjU1ZjAxMS05MTU5LTQwYmMtYjNmMS1kZTdiN2UwNDhjZWYifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxMiIsImlkIjoiNzI4NTYzOTQ2In0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjE3LCJpYXQiOjE2MTk1OTE3MTd9.tXrPYpLg0gbJanfGfq6T4nuLKmf9yRZT\_g14s\_VhMQ8",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"df55f011-9159-40bc-b3f1-de7b7e048cef\",\"id\":\"df55f011-9159-40bc-b3f1-de7b7e048cef\"},\"content\":{\"type\":\"page\",\"version\":\"12\",\"id\":\"728563946\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728563946\",\"macro.hash\":\"df55f011-9159-40bc-b3f1-de7b7e048cef\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"12\",\"page.title\":\"StopPlace - complex\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att728727693\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=ab4c2afe-a03f-4b2c-af14-3cc65fc5a2a8\|name=flyplass-gardermoen-illustrasjon\|diagramAttachmentId=att728760410\|containerId=728563946\|timestamp=1550832805885\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"12\",\"imageAttachmentId\":\"att728727693\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"ab4c2afe-a03f-4b2c-af14-3cc65fc5a2a8\",\"content.id\":\"728563946\",\"name\":\"flyplass-gardermoen-illustrasjon\",\"macro.id\":\"df55f011-9159-40bc-b3f1-de7b7e048cef\",\"diagramAttachmentId\":\"att728760410\",\"containerId\":\"728563946\",\"timestamp\":\"1550832805885\"}",  
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


### Elements <a id="StopPlace-complex-Elements"></a>

Many of the basic elements are described in more detail in the examples for [minimalistic stop place](handbok-n801-siri-netex-stopplace-minimalistic.md) and [single stop place](handbok-n801-siri-netex-stopplace-simple.md), and will therefore not be covered more closely in this example document. Below is an overview of \(some of\) the most important elements that should be modeled for a multimodal stop area with multiple [StopPlaces](handbok-n801-siri-netex-stops.md#stops-StopPlace):

#### GroupOfStopPlaces <a id="StopPlace-complex-GroupOfStopPlaces"></a>

No [XML](https://github.com/entur/profile-norway-examples/blob/master/netex/stops/OsloS_station_example.xml) model available. Will be described here in the next version of the handbook. Contact Entur for examples.

Please be aware, due to developments _after_ the publication of these examples, the usage of GroupOfStopPlace has been changed from a top-level StopPlace element to something more akin to an "alias" which refers to StopPlaces seen as central/important hub stops \(usually the GroupOfStopPlaces is equal to a city/town\).

#### StopPlace <a id="StopPlace-complex-StopPlace"></a>

For a larger building connected to a stop place area, it will normally be expedient to describe the stop in more detail with geographical location, its facilities, and public entrances.

In this example the railway station "Oslo S" is modelled with a higher degree of detail, \(for more examples of StopPlace modelling, see: [minimalistic stop place](handbok-n801-siri-netex-stopplace-minimalistic.md) and [single stop place](handbok-n801-siri-netex-stopplace-simple.md)\).

```text
<StopPlace id="NHR:StopPlace:8" version="any">
	<Name lang="no-NO">Oslo S</Name>
	<Centroid>
		<Location>
			<!-- Note: Generalized coordinate representing the whole station -->
			<Longitude>59.910921</Longitude>
			<Latitude>10.753284</Latitude>
		</Location>
	</Centroid>
	<placeTypes>
		<TypeOfPlaceRef ref="monomodalStopPlace"/>
	</placeTypes>
	<AccessibilityAssessment id="NHR:AccessibilityAssessment:6" version="any">
		<MobilityImpairedAccess>true</MobilityImpairedAccess>
		<limitations>
			<AccessibilityLimitation>
				<WheelchairAccess>true</WheelchairAccess>
				<StepFreeAccess>true</StepFreeAccess>
				<AudibleSignalsAvailable>true</AudibleSignalsAvailable>
			</AccessibilityLimitation>
		</limitations>
	</AccessibilityAssessment>
	<Covered>indoors</Covered>
	<Gated>openArea</Gated>
	<facilities>
		<SiteFacilitySetRef ref="sfs:1"/>
	</facilities>
	<entrances>
		<!-- Main entrance towards Jernbanetorget -->
		<StopPlaceEntrance id="NHR:Entrance:1" version="any">
			<EntranceType>automaticDoor</EntranceType>
			<Width>1.5</Width>
			<Height>2.2</Height>
		</StopPlaceEntrance>
	</entrances>
	<TransportMode>rail</TransportMode>
	<StopPlaceType>railStation</StopPlaceType>
	
	[...]
	
</StopPlace>
```

#### boardingPositions <a id="StopPlace-complex-boardingPositions"></a>

For trains, a [Quay](handbok-n801-siri-netex-stops.md#stops-Quay) can be subdivided into [BoardingPositions](handbok-n801-siri-netex-stops.md#stops-BoardingPosition), which specifies positions or zones at the along the platform. This can be used, for example, to specify where different carriage types will be relative to the length of a train, or where one may find boarding facilities for travellers with special needs.

```text
<boardingPositions>
	<BoardingPosition id="NHR:BoardingPosition:1" version="any">
		<Label>A</Label>
		<BoardingPositionType>positionOnRailPlatform</BoardingPositionType>
	</BoardingPosition>
	<BoardingPosition id="NHR:BoardingPosition:2" version="any">
		<Label>B</Label>
		<BoardingPositionType>positionOnRailPlatform</BoardingPositionType>
	</BoardingPosition>
	[...]
</boardingPositions>
```

#### AccessSpace <a id="StopPlace-complex-AccessSpace"></a>

Areas, often indoors, associated with a stop place or groups of stop places, are modelled as [AccessSpace](handbok-n801-siri-netex-stops.md#stops-AccessSpace). This includes, among other things, map position\(s\), a reference to relevant public entrances, information on general accessibility for wheelchair users and information about ticketing equipment.

For larger stop place areas, several AccessSpace can be defined, in this example, the main hall for "Oslo Central Station" \(Oslo S\) has been modelled.

```text
<AccessSpace id="NHR:AccessSpace:1" version="any">
	<gml:Polygon gml:id="OsloS">
		<!-- Perimeter of the inner public space. The main hall and the various corridors -->
		<gml:interior>
			<gml:LinearRing>
				<gml:pos>59.91160529142 10.75148462981</gml:pos>
				<gml:pos>59.91127987568 10.75117885798</gml:pos>
				<gml:pos>59.91115750777 10.75204521149</gml:pos>
				<gml:pos>59.91109699601 10.75230002135</gml:pos>
				<gml:pos>59.91093159661 10.75214177102</gml:pos>
				<gml:pos>59.91074871503 10.75290620059</gml:pos>
				<gml:pos>59.9115004057 10.75361698598</gml:pos>
				<gml:pos>59.91164966605 10.75296252698</gml:pos>
				<gml:pos>59.91131214845 10.75265407294</gml:pos>
			</gml:LinearRing>
		</gml:interior>
	</gml:Polygon>
	<PublicUse>all</PublicUse>
	<Covered>indoors</Covered>
	<Lighting>wellLit</Lighting>
	<AllAreasWheelchairAccessible>true</AllAreasWheelchairAccessible>
	<equipmentPlaces>
		<EquipmentPlace id="NHR:EquipmentPlace:1" version="any">
			<Centroid>
				<Location>
					<Longitude>59.911213</Longitude>
					<Latitude>10.752860</Latitude>
				</Location>
			</Centroid>
			<placeEquipments>
				<TicketingEquipment id="NHR:TicketingEquipment:1" version="any">
					<VehicleModes>rail bus</VehicleModes>
					<NumberOfMachines>4</NumberOfMachines>
					<TicketingFacilityList>ticketOffice mobileTicketing
						ticketMachines</TicketingFacilityList>
					<TicketingServiceFacilityList>reservations purchase</TicketingServiceFacilityList>
				</TicketingEquipment>
			</placeEquipments>
		</EquipmentPlace>
	</equipmentPlaces>
	<entrances>
		<StopPlaceEntranceRef ref="NHR:Entrance:1"/>
	</entrances>
	<AccessSpaceType>concourse</AccessSpaceType>
</AccessSpace>
```

#### NavigationPath <a id="StopPlace-complex-NavigationPath"></a>

To describe how to get from one location of a stop place area to another \(usually on foot\), for example, to indicate the expected walking time for interchanges between two transport modes within a transportation hub, a [NavigationPath](https://enturas.atlassian.net/wiki/spaces/ROR/pages/728563886#network%28Copy%29-NavigationPath) can be modelled.

```text
<!-- Path between Entrance to Oslo S and platform 1 (spor 1) -->
<NavigationPath id="np:1" version="any">
	<Distance>12.3</Distance>
	<From>
		<!-- From Entrance to Oslo S train stop (sp:osl:7) -->
		<PlaceRef ref="sp:osl:7:entr:1"/>
	</From>
	<To>
		<!-- Train platform - spor 1 -->
		<PlaceRef ref="q:sp:osl:7:spor1"/>
	</To>
	<TransferDuration>
		<DefaultDuration>PT15M0S</DefaultDuration>
		<FrequentTravellerDuration>PT4M0S</FrequentTravellerDuration>
		<OccasionalTravellerDuration>PT6M0S</OccasionalTravellerDuration>
		<MobilityRestrictedTravellerDuration>PT10M0S</MobilityRestrictedTravellerDuration>
	</TransferDuration>
	<AccessFeatureList>escalator concourse travelator</AccessFeatureList>
	<NavigationType>streetToQuay</NavigationType>
</NavigationPath>
```

#### SiteFacilitySet <a id="StopPlace-complex-SiteFacilitySet"></a>

Public facilities and services at-, or associated with a stop place, such as information boards, are described with the explicit type of [FacilitySet]() specifically defined for, and associated with a [SiteElement](handbok-n801-siri-netex-stops.md#stops-SiteElement).

```text
<SiteFacilitySet id="sfs:1" version="any">
	<AccessibilityInfoFacilityList>largePrintTimetables audioForHearingImpaired audioInformation
		displaysForVisuallyImpaired</AccessibilityInfoFacilityList>
	<PassengerInformationEquipmentList>timetablePoster</PassengerInformationEquipmentList>
	<PassengerInformationFacilityList>passengerInformationDisplay
		realTimeConnections</PassengerInformationFacilityList>
</SiteFacilitySet>
```

