# Håndbok N801 \(SIRI/NeTEX\) : SIRI-SX - Message on a stop for specific lines

XML

See complete example:

* [https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-for-stop-by-specific-lines.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-for-stop-by-specific-lines.xml)

## A message shown only when stop is served by specific lines <a id="SIRI-SX-Messageonastopforspecificlines-Amessageshownonlywhenstopisservedbyspecificlines"></a>

If the message is relevant to a specific Quay, it should be referenced directly.

If the specific Quay is unknown, or the message is relevant for all Quays at the stop, the reference is to the StopPlace.

The message is shown only when the specific lines are part of the suggested journeys \(in the absence of _stopConditions_ the message is shown for all journey suggestions to-, from-, via-, passing- or interchanging on the stop\).

  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy3045004779121911139",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=637370728&pageId=&name=illustration-message-on-stop-for-specific-line&attachmentId=att747471433&pagePin=&imageAttachmentId=att746652376&border=&chrome=&html5=&size=&ceoId=&macroId=ac60a027-dcd3-4bc2-98a1-f48dc5aa7543&spaceKey=&version=&migration=&previewPageId=637370728&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy3045004779121911139&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJkNjQxNDJlMWFiZTgzNjkwNDFiMzY5M2JlOTQ0NGVjYzllYjZmOTc5Mzc3OGI2MTNkYmUxMGExNmE4YjhhYWJiIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTk3MCwiaWF0IjoxNjE5NTkxNzkwfQ.voBiOWfI4ftfQj8Q5NthlFWC\_pV6RM9K38WcZ7\_4WAI",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZjFhNzhkNjMtN2FlMC00MzU2LTkzYzQtNWY2ZmZmYjRkMjQxIiwiaWQiOiJmMWE3OGQ2My03YWUwLTQzNTYtOTNjNC01ZjZmZmZiNGQyNDEifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiI0IiwiaWQiOiI2MzczNzA3MjgifSwic3BhY2UiOnsia2V5IjoiUFVCTElDIiwiaWQiOiI2MzczNzAzNjkifX19LCJleHAiOjE2MTk1OTI2OTAsImlhdCI6MTYxOTU5MTc5MH0.GzObtZ5GtwHRl154vvXVJIWJHO3xVpcmJsqPfHw4dL0",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"f1a78d63-7ae0-4356-93c4-5f6fffb4d241\",\"id\":\"f1a78d63-7ae0-4356-93c4-5f6fffb4d241\"},\"content\":{\"type\":\"page\",\"version\":\"4\",\"id\":\"637370728\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"637370728\",\"macro.hash\":\"f1a78d63-7ae0-4356-93c4-5f6fffb4d241\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"page.type\":\"page\",\"content.version\":\"4\",\"page.title\":\"SIRI-SX - Message on a stop for specific lines\",\"macro.body\":\"\",\": = \| RAW \| = :\":\"imageAttachmentId=att746652376\|baseUrl=https://enturas.atlassian.net/wiki\|macroId=ac60a027-dcd3-4bc2-98a1-f48dc5aa7543\|name=illustration-message-on-stop-for-specific-line\|diagramAttachmentId=att747471433\|containerId=637370728\|timestamp=1553518151647\",\"space.id\":\"637370369\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"4\",\"imageAttachmentId\":\"att746652376\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"macroId\":\"ac60a027-dcd3-4bc2-98a1-f48dc5aa7543\",\"content.id\":\"637370728\",\"name\":\"illustration-message-on-stop-for-specific-line\",\"macro.id\":\"f1a78d63-7ae0-4356-93c4-5f6fffb4d241\",\"diagramAttachmentId\":\"att747471433\",\"containerId\":\"637370728\",\"timestamp\":\"1553518151647\"}",  
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
* **Search** 2 _will_ show the message due to _destination_ at Stortorvet for line 11 and 17
* **Search** 3 _will_ show the message due to _notStopping_ at Stortorvet for line 11, 17 and 18
* **Search** 4 _will_ show the message due to _startPoint_ at Stortorvet for line 11, 17 and 18

