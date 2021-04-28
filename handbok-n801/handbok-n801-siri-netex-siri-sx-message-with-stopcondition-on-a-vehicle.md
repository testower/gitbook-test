# Håndbok N801 \(SIRI/NeTEX\) : SIRI SX - Message with stopCondition on a Vehicle

**Content**

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591774207 {padding: 0px;}  
div.rbtoc1619591774207 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591774207 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Messages depending on stopCondition](handbok-n801-siri-netex-siri-sx-message-with-stopcondition-on-a-vehicle.md#SIRISX-MessagewithstopConditiononaVehicle-MessagesdependingonstopCondition)
  * [The message is only shown when the affected stop is the target or origin of a travel search request](handbok-n801-siri-netex-siri-sx-message-with-stopcondition-on-a-vehicle.md#SIRISX-MessagewithstopConditiononaVehicle-Themessageisonlyshownwhentheaffectedstopisthetargetororiginofatravelsearchrequest)
  * [The message is only shown when boarding a specific vehicle \(departure\) on a specific stop](handbok-n801-siri-netex-siri-sx-message-with-stopcondition-on-a-vehicle.md#SIRISX-MessagewithstopConditiononaVehicle-Themessageisonlyshownwhenboardingaspecificvehicle%28departure%29onaspecificstop)
  * [The message is shown for all searches to-, from, or past the specified stops on a vehicle \(departure\)](handbok-n801-siri-netex-siri-sx-message-with-stopcondition-on-a-vehicle.md#SIRISX-MessagewithstopConditiononaVehicle-Themessageisshownforallsearchesto-,from,orpastthespecifiedstopsonavehicle%28departure%29)
  * [The message is shown when searching past a specific stop on a vehicle \(departure\)](handbok-n801-siri-netex-siri-sx-message-with-stopcondition-on-a-vehicle.md#SIRISX-MessagewithstopConditiononaVehicle-Themessageisshownwhensearchingpastaspecificstoponavehicle%28departure%29)

XML

See complete examples:

* Boarding and alighting: [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-alight-board-specific-stop-and-vehicle.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-alight-board-specific-stop-and-vehicle.xml)
* Only boarding: [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-boarding-specific-stop-and-vehicle.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-boarding-specific-stop-and-vehicle.xml)
* Passing: [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-passing-specific-stop-and-vehicle.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-passing-specific-stop-and-vehicle.xml)
* Boarding and alighting or passing: [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-alight-board-passing-stops.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-alight-board-passing-stops.xml)

## Messages depending on stopCondition <a id="SIRISX-MessagewithstopConditiononaVehicle-MessagesdependingonstopCondition"></a>

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy112521825036135528",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=637370785&pageId=&name=stopConditionExample&attachmentId=att742818141&pagePin=&imageAttachmentId=att742392170&border=&chrome=&html5=&size=&ceoId=&macroId=d255f1a7-4ec2-4218-b39e-1ba1722e483f&spaceKey=&version=&migration=&previewPageId=637370785&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy112521825036135528&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiI3MDBhNDQ1MGFmNGQyZWUwMTNkZDdkN2Q1MGFmNzQ5NTMzMDhjODQ4MTRhMTUzY2YwNTA4ZTgzMmVlYmQzODgzIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTk1NCwiaWF0IjoxNjE5NTkxNzc0fQ.L-kgse-gzOjSMSgzEb0TRCVKYFabJVjcza\_to8zlNCQ",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZDhkM2UyMTYtYjY4Zi00MGM4LTk3MzgtMGU2OWJkMzc4OTg5IiwiaWQiOiJkOGQzZTIxNi1iNjhmLTQwYzgtOTczOC0wZTY5YmQzNzg5ODkifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiI2IiwiaWQiOiI2MzczNzA3ODUifSwic3BhY2UiOnsia2V5IjoiUFVCTElDIiwiaWQiOiI2MzczNzAzNjkifX19LCJleHAiOjE2MTk1OTI2NzQsImlhdCI6MTYxOTU5MTc3NH0.1FBkfw1McYgqkL9vrkFkRuS2Uryv3dVWbY-WM-oH1Bo",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"d8d3e216-b68f-40c8-9738-0e69bd378989\",\"id\":\"d8d3e216-b68f-40c8-9738-0e69bd378989\"},\"content\":{\"type\":\"page\",\"version\":\"6\",\"id\":\"637370785\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"637370785\",\"macro.hash\":\"d8d3e216-b68f-40c8-9738-0e69bd378989\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"6\",\"page.title\":\"SIRI SX - Message with stopCondition on a Vehicle\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att742392170\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=d255f1a7-4ec2-4218-b39e-1ba1722e483f\|name=stopConditionExample\|diagramAttachmentId=att742818141\|containerId=637370785\|timestamp=1553250580683\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"6\",\"imageAttachmentId\":\"att742392170\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"d255f1a7-4ec2-4218-b39e-1ba1722e483f\",\"content.id\":\"637370785\",\"name\":\"stopConditionExample\",\"macro.id\":\"d8d3e216-b68f-40c8-9738-0e69bd378989\",\"diagramAttachmentId\":\"att742818141\",\"containerId\":\"637370785\",\"timestamp\":\"1553250580683\"}",  
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


### The message is only shown when the affected stop is the target or origin of a travel search request <a id="SIRISX-MessagewithstopConditiononaVehicle-Themessageisonlyshownwhentheaffectedstopisthetargetororiginofatravelsearchrequest"></a>

The message is displayed depending on the search request parameters, time and _StopConditions_.**stopCondition**

```text
<!---For Vehicle 1--->
<AffectedStopPoint>                          
	<StopPointRef>NSR:Quay:1067</StopPointRef> 
    <StopPointName>Dovre</StopPointName>
    <StopCondition>destination</StopCondition>
    <StopCondition>startPoint</StopCondition>
</AffectedStopPoint>
```

The message will be displayed when searching from- or to Dovre.

The following is true for the illustration:

* **Search 1** will **not** show the message
* **Search** 2 _will_ show the message
* **Search** 3 will **not** show the message
* **Search** 4 _will_ show the message due to _startPoint_ at Dovre
* **Search** 5 will **not** show the message

### The message is only shown when boarding a specific vehicle \(departure\) on a specific stop <a id="SIRISX-MessagewithstopConditiononaVehicle-Themessageisonlyshownwhenboardingaspecificvehicle(departure)onaspecificstop"></a>

The message is referenced by multiple stops on the same specific VehicleJourney \(specific departure on a specific date set with &lt;VehicleJourneyRef&gt; and &lt;OriginAimedDepartureTime&gt;\).

_stopConditions_ are set to '_startPoint_' for all stops, and the message will only be shown when searching a journey on the specific date, with the specific departure, from one of the specific stops.**stopCondition**

```text
<!---For Vehicle 1--->
<StopPoints>
	<AffectedStopPoint>
    	<StopPointRef>NSR:Quay:629</StopPointRef>
        <StopPointName>Kvam</StopPointName>
        <StopCondition>startPoint</StopCondition>
	</AffectedStopPoint>
    <AffectedStopPoint>
    	<StopPointRef>NSR:Quay:652</StopPointRef>
        <StopPointName>Dovre</StopPointName>
        <StopCondition>startPoint</StopCondition>
	</AffectedStopPoint>
    <AffectedStopPoint>
    	<StopPointRef>NSR:Quay:316</StopPointRef>
        <StopPointName>Oppdal</StopPointName>
        <StopCondition>startPoint</StopCondition>
	</AffectedStopPoint>
</StopPoints>
```

The following is true for the illustration:

* **Search 1** will **not** show the message
* **Search** 2 will **not** show the message
* **Search** 3 will **not** show the message
* **Search** 4 _will_ show the message
* **Search** 5 will **not** show the message

### The message is shown for all searches to-, from, or past the specified stops on a vehicle \(departure\) <a id="SIRISX-MessagewithstopConditiononaVehicle-Themessageisshownforallsearchesto-,from,orpastthespecifiedstopsonavehicle(departure)"></a>

The message is applied to multiple successive stops on a _VehicleJourney_, on a specific _OriginAimedDepartureTime_.

The message is shown in search responses where the particular vehicle, stop, and date appears but depends on the _stopConditions_ on the stops.**stopCondition**

```text
<!---For Vehicle 1--->
<StopPoints>
	<AffectedStopPoint>
    	<StopPointRef>NSR:Quay:4</StopPointRef>
        <StopPointName>Otta</StopPointName>
        <StopCondition>startPoint</StopCondition>
	</AffectedStopPoint>
    <AffectedStopPoint>
    	<StopPointRef>NSR:Quay:652</StopPointRef>
        <StopPointName>Dovre</StopPointName>
        <StopCondition>notStopping</StopCondition>
        <StopCondition>destination</StopCondition>
        <StopCondition>startPoint</StopCondition>
	</AffectedStopPoint>
    <AffectedStopPoint>
    	<StopPointRef>NSR:Quay:645</StopPointRef>
        <StopPointName>Dombås</StopPointName>
        <StopCondition>notStopping</StopCondition>
        <StopCondition>destination</StopCondition>
        <StopCondition>startPoint</StopCondition>
	</AffectedStopPoint>
    <AffectedStopPoint>
    	<StopPointRef>NSR:Quay:316</StopPointRef>
        <StopPointName>Oppdal</StopPointName>
        <StopCondition>destination</StopCondition>
	</AffectedStopPoint>
</StopPoints>
```

The following is true for the illustration:

* **Search 1** will **not** show the message
* **Search** 2 _will_ show the message due to Dovre being the destination
* **Search** 3 _will_ show the message twice, due to _notStopping_ at Dovre and _notStopping_ at Dombås
* **Search** 4 _will_ show the message three times, due to _startPoint_ at Dovre, _notStopping_ at Dombås and _destination_ at Oppdal
* **Search** 5 will **not** show the message

### The message is shown when searching past a specific stop on a vehicle \(departure\) <a id="SIRISX-MessagewithstopConditiononaVehicle-Themessageisshownwhensearchingpastaspecificstoponavehicle(departure)"></a>

The message is applied to multiple successive stops on a _VehicleJourney_, on a specific _OriginAimedDepartureTime_.

The message is shown in search responses where the particular vehicle- and stop.**stopCondition**

```text
<!---For Vehicle 1--->
<AffectedStopPoint>
	<StopPointRef>NSR:Quay:652</StopPointRef>
    <StopPointName>Dovre</StopPointName>
    <StopCondition>notStopping</StopCondition>
</AffectedStopPoint>
```

The following is true for the illustration:

* **Search 1** will **not** show the message
* **Search** 2 will **not** show the message
* **Search** 3 _will_ show the message
* **Search** 4 will **not** show the message
* **Search** 5 will **not** show the message

