# Håndbok N801 \(SIRI/NeTEX\) : SIRI-SX - Message on a leg Melding på en strekning for flere kjøretøy

XML

See complete example:

* [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-multiple-vehicles.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-multiple-vehicles.xml)

## A message which affects multiple departures/vehicles on a certain leg <a id="SIRI-SX-MessageonalegMeldingp&#xE5;enstrekningforflerekj&#xF8;ret&#xF8;y-Amessagewhichaffectsmultipledepartures/vehiclesonacertainleg"></a>

The message is applied to each vehicle passing the stops in question.

The message is shown in search results returning the vehicles in question, depending on _stopConditions_ and stops.

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy5061292228732933555",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=637370746&pageId=&name=illustration&attachmentId=att746848808&pagePin=&imageAttachmentId=att750649429&border=&chrome=&html5=&size=&ceoId=&macroId=c7bdf472-edcd-4948-bd89-95f766e1b7d9&spaceKey=&version=&migration=&previewPageId=637370746&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy5061292228732933555&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJjZDAwNzI5NGFlODdiOTA3OWE0MTQyMTczYzg0YzUyYWI3MWNhZGM5MjBjNDk5ZDgwNzU0NWEwMTJjOWJjYzhmIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTk2NiwiaWF0IjoxNjE5NTkxNzg2fQ.KOq9EndKPlhRpH3vNsZMaSWD\_6uOHEmiUbMVxmVeONU",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZWMxZWVhZDctYWI0Yi00YjlmLTg0NjUtODBkODRlNWQ3MzlmIiwiaWQiOiJlYzFlZWFkNy1hYjRiLTRiOWYtODQ2NS04MGQ4NGU1ZDczOWYifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiI1IiwiaWQiOiI2MzczNzA3NDYifSwic3BhY2UiOnsia2V5IjoiUFVCTElDIiwiaWQiOiI2MzczNzAzNjkifX19LCJleHAiOjE2MTk1OTI2ODYsImlhdCI6MTYxOTU5MTc4Nn0.dX-1uC3ZL3dy2-bSNHqf7VnnvgOr08U8DvfSvndkSZQ",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"ec1eead7-ab4b-4b9f-8465-80d84e5d739f\",\"id\":\"ec1eead7-ab4b-4b9f-8465-80d84e5d739f\"},\"content\":{\"type\":\"page\",\"version\":\"5\",\"id\":\"637370746\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"637370746\",\"macro.hash\":\"ec1eead7-ab4b-4b9f-8465-80d84e5d739f\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"5\",\"page.title\":\"SIRI-SX - Message on a leg Melding p\u00e5 en strekning for flere kj\u00f8ret\u00f8y\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att750649429\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=c7bdf472-edcd-4948-bd89-95f766e1b7d9\|name=illustration\|diagramAttachmentId=att746848808\|containerId=637370746\|timestamp=1553515654802\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"5\",\"imageAttachmentId\":\"att750649429\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"c7bdf472-edcd-4948-bd89-95f766e1b7d9\",\"content.id\":\"637370746\",\"name\":\"illustration\",\"macro.id\":\"ec1eead7-ab4b-4b9f-8465-80d84e5d739f\",\"diagramAttachmentId\":\"att746848808\",\"containerId\":\"637370746\",\"timestamp\":\"1553515654802\"}",  
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


The following is true for the illustration:

* **Search 1** will **not** show the message
* **Search** 2 will **not** show the message
* **Search** 3 _will_ show the message, due to _notStopping_ at Oppedal for vehicle 1
* **Search** 4 _will_ show the message, due to _destination_ at Oppedal for vehicle 1
* **Search** 5 _will_ show the message, due to _notStopping_ at Oppedal, and _destination_ at Støren for vehicle 2
* **Search 6** will **not** show the message

Searching Otta to Dombås will not show the message since the message at Dombås is only for _stopCondition_ "startPoint".

