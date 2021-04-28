# Håndbok N801 \(SIRI/NeTEX\) : Branding

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591710243 {padding: 0px;}  
div.rbtoc1619591710243 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591710243 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Additional information on Network or Line](handbok-n801-siri-netex-branding.md#Branding-AdditionalinformationonNetworkorLine)
  * [Modelling of added information](handbok-n801-siri-netex-branding.md#Branding-Modellingofaddedinformation)
    * [Link](handbok-n801-siri-netex-branding.md#Branding-Link)
  * [Elements](handbok-n801-siri-netex-branding.md#Branding-Elements)
    * [ValueSet](handbok-n801-siri-netex-branding.md#Branding-ValueSet)
    * [BrandingRef](handbok-n801-siri-netex-branding.md#Branding-BrandingRef)
      * [Branding on a Line](handbok-n801-siri-netex-branding.md#Branding-BrandingonaLine)
      * [Branding on a Network](handbok-n801-siri-netex-branding.md#Branding-BrandingonaNetwork)

## Additional information on Network or Line <a id="Branding-AdditionalinformationonNetworkorLine"></a>

Branding is a generic NeTEx element which can be applied to elements in the NeTEx structure for adding or overriding name and URL. In the Nordic profile, the usage is limited to adding additional names and URL to the Network and Line elements.

* Branding per **Network**
  * Used when certain lines in the dataset have a common denominator, i.e. Network.
  * Examples of this can be a cluster of city buses, a string of Lines which form a coherent service, or a sales related brand name.
  * The Network may have a different URL from the authority.
* Branding per **Line**
  * Used when a Line has a commonly used or publicly marketed name which a customer may relate to in addition to the Lines' `publicCode`.
  * An example of this can be e.g. "Bergensbanen" for railway service journeys between Oslo and Bergen.
  * The Line may have a different URL from the authority.

For multiple Networks in one dataset, [additionalNetwork](handbok-n801-siri-netex-multiple-authorities.md) must be used.

Note that each [additionalNetwork](handbok-n801-siri-netex-multiple-authorities.md) may have its own [Authority](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728727624/framework#framework-Authority), and must be used if necessary to have multiple Authorities within the same dataset.

### Modelling of added information <a id="Branding-Modellingofaddedinformation"></a>

The Branding elements may be added to the commons file of the dataset \(for reduced redundancy\) and is referred to from Network or Line with the use of a BrandingRef.  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy9053208264890710360",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728727682&pageId=&name=codespace-authority-branding-operator&attachmentId=att728596646&pagePin=&imageAttachmentId=att728596642&border=&chrome=&html5=&size=&ceoId=&macroId=f018d4b8-bc3b-4641-a0db-1e32be2bf385&spaceKey=&version=&migration=1&previewPageId=728727682&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy9053208264890710360&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJmMDE3NTU5YjU1NzNkMWU0NmNiOTA0NjRjMTNmOGQwOGZlOTc5Yzk2YjFmOTJlOTdiMTc4MDdiMzQwZjFlZjdkIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg5MCwiaWF0IjoxNjE5NTkxNzEwfQ.8azXg-ILBzhsJ4JxSVScgspvxKn9yNAI570dd7-0sts",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiZWU5NmY4MzMtNTlmMi00MDNiLWFhMjYtN2FjMWQ0NjFjZjQyIiwiaWQiOiJlZTk2ZjgzMy01OWYyLTQwM2ItYWEyNi03YWMxZDQ2MWNmNDIifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiIxNiIsImlkIjoiNzI4NzI3NjgyIn0sInNwYWNlIjp7ImtleSI6IlBVQkxJQyIsImlkIjoiNjM3MzcwMzY5In19fSwiZXhwIjoxNjE5NTkyNjEwLCJpYXQiOjE2MTk1OTE3MTB9.8vghkIbN38rXbv6CBfJP\_7pYl1yZZu1JSmR2KKgKxAs",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"ee96f833-59f2-403b-aa26-7ac1d461cf42\",\"id\":\"ee96f833-59f2-403b-aa26-7ac1d461cf42\"},\"content\":{\"type\":\"page\",\"version\":\"16\",\"id\":\"728727682\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728727682\",\"macro.hash\":\"ee96f833-59f2-403b-aa26-7ac1d461cf42\",\"page.type\":\"page\",\": = \| RAW \| = :\":\"imageAttachmentId=att728596642\|macroId=f018d4b8-bc3b-4641-a0db-1e32be2bf385\|baseUrl=https://enturas.atlassian.net/wiki\|name=codespace-authority-branding-operator\|migration=1\|diagramAttachmentId=att728596646\|containerId=728727682\|timestamp=1566906621697\",\"space.id\":\"637370369\",\"diagramAttachmentId\":\"att728596646\",\"containerId\":\"728727682\",\"timestamp\":\"1566906621697\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"content.version\":\"16\",\"page.title\":\"Branding\",\"macro.body\":\"\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"16\",\"imageAttachmentId\":\"att728596642\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"macroId\":\"f018d4b8-bc3b-4641-a0db-1e32be2bf385\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728727682\",\"name\":\"codespace-authority-branding-operator\",\"migration\":\"1\",\"macro.id\":\"ee96f833-59f2-403b-aa26-7ac1d461cf42\"}",  
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


_Please note that the concept of GroupOfLines is not a part of the hierarchy and does necessarily have to include the same lines as the Network._

#### Link <a id="Branding-Link"></a>

The XML sample files are located in the GitHub repository:

* [https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-Branding-Line.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-Branding-Line.xml)
* [https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-Branding-Network.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-Branding-Network.xml)

### Elements <a id="Branding-Elements"></a>

#### ValueSet <a id="Branding-ValueSet"></a>

Each instance of Branding is defined under [ResourceFrame]() \(_as a_ [_TypeOfValue_]()\), specified with **Name** value. 

```text
<typesOfValue>
	<Branding version="1" id="UNI:Branding:1">
		<Name>Lavprisekspressen</Name>
		<Url>https://lavprisekspressen.no</Url>
	</Branding>
	<Branding version="1" id="VYB:Branding:1">
		<Name>Bus4You</Name>
		<Url>https://www.vy.se</Url>
	</Branding>
</typesOfValue>
```

#### BrandingRef <a id="Branding-BrandingRef"></a>

The reference element BrandingRef must be specified for the object where a name, \(and if applicable, other fields\) is to be replaced.

**Branding on a Line**

_\(simplified example\)_

```text
<Line version="1" id="UNI:Line:1">
	<BrandingRef version="1" ref="UNI:Branding:1"/>
	<Name>Oslo-Kristiansand-Stavanger</Name>
	<TransportMode>bus</TransportMode>
	<TransportSubmode>
		<BusSubmode>localBus</BusSubmode>
	</TransportSubmode>
</Line>
```

**Branding on a Network**

_\(simplified example\)_

```text
<Network version="1" id="VYB:Network:1"> 
	<BrandingRef version="1" ref="VYB:Branding:1"/>
	<Name>Vy Buss AB</Name>
</Network>
```

