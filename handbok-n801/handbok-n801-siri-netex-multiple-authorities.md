# Håndbok N801 \(SIRI/NeTEX\) : Multiple Authorities

Version requirements: NeTEx version must be 1.08 or higher in order to use **additionalNetworks**. For older versions, a temporary solution with `serviceFrame` can be used. For more information about this, [contact Entur](https://www.entur.org/kontakt/).

Content/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591713090 {padding: 0px;}  
div.rbtoc1619591713090 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591713090 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Background](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-Background)
* [Modelling multiple Networks within the same dataset](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-ModellingmultipleNetworkswithinthesamedataset)
  * [Link](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-Link)
  * [Elements](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-Elements)
    * [organizations](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-organizations)
    * [Difference between Network & additionalNetworks](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-DifferencebetweenNetwork&additionalNetworks)
      * [Network](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-Network)
      * [additionalNetworks](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-additionalNetworks)
    * [Line](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-Line)
      * [Line in the main Network](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-LineinthemainNetwork)
      * [Line in the additional Network](handbok-n801-siri-netex-multiple-authorities.md#MultipleAuthorities-LineintheadditionalNetwork)

## Background <a id="MultipleAuthorities-Background"></a>

In communication with the public, [Authority ]()is normally used to present the agency responsible for such things as travel search and ticketing. In cases where a data provider also provides route data on behalf of other service providers, the distinction of responsibility must be indicated by separation at [Network](handbok-n801-siri-netex-network.md#network-Netw) level \(and subsequently a reference to the correct [Authority]()\) to properly separate [Line](handbok-n801-siri-netex-network.md#network-Line) elements.

To override the Authority or Operator information within the same Network, use [Branding](handbok-n801-siri-netex-branding.md). 

## Modelling multiple Networks within the same dataset <a id="MultipleAuthorities-ModellingmultipleNetworkswithinthesamedataset"></a>

At least one [Network](handbok-n801-siri-netex-network.md#network-Network) is required for any dataset. If multiple Authorities are needed, add [additionalNetworks](handbok-n801-siri-netex-network.md#network-additionalNetworks) for each additional [Authority]() needed.

In the example below, the regional Authority "Opplandstrafikk" are delivering additional data on behalf of several minor private operators. "Skiblander" is a private operator, and do not operate under the Authority of Opplandstrafikk, but the two parties have reached an agreement where "Opplandstrafikk" handle the technical task of creating NeTEx data for the national database. By using _additionalNetworks_, "Opplandstrafikk" is able to separate "Skibladner" from its own routes, and Authority, within the same dataset \(Codespace\).  
  \(function\(\){  
    var data = {  
    "addon\_key":"com.gliffy.integration.confluence",  
    "uniqueKey":"com.gliffy.integration.confluence\_\_gliffy7189069908188997364",  
    "key":"gliffy",  
     "moduleType":"dynamicContentMacros",      "moduleLocation":"content",         "cp":"/wiki",  
            "general":"",  
    "w":"",  
    "h":"",  
    "url":"https://confluence-connect.gliffy.net/macro/render?space=PUBLIC&displayName=&container=728891557&pageId=&name=network-additionalNetwork&attachmentId=att728891568&pagePin=&imageAttachmentId=att728694890&border=&chrome=&html5=&size=&ceoId=&macroId=4aeba792-a987-413a-bd3c-a38b2e004ad9&spaceKey=&version=&migration=1&previewPageId=728891557&xdm\_e=https%3A%2F%2Fenturas.atlassian.net&xdm\_c=channel-com.gliffy.integration.confluence\_\_gliffy7189069908188997364&cp=%2Fwiki&xdm\_deprecated\_addon\_key\_do\_not\_use=com.gliffy.integration.confluence&lic=active&cv=1.972.0&jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJxc2giOiJhNDczMmZlNTI1MTJlMzBmZmMxZjcwNTY0MDhmNDU3YjE0OTBhYjY2MmJlZmZhZjFlNzZjYTE0N2E4MzhjZTlkIiwiaXNzIjoiQ29uZmx1ZW5jZTo2NzM5MTg5ODY1IiwiY29udGV4dCI6e30sImV4cCI6MTYxOTU5MTg5MywiaWF0IjoxNjE5NTkxNzEzfQ.pbIML6VV\_YyWRYosNRf3KP-r4EIkJdOfIA4gkbqlMWM",  
     "contextJwt": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiI1ZDE5ZjhhNDkxOTQzZjBkMmFjNTFiY2QiLCJpc3MiOiJDb25mbHVlbmNlOjY3MzkxODk4NjUiLCJjb250ZXh0Ijp7ImxpY2Vuc2UiOnsiYWN0aXZlIjp0cnVlfSwiY29uZmx1ZW5jZSI6eyJtYWNybyI6eyJvdXRwdXRUeXBlIjoiaHRtbF9leHBvcnQiLCJoYXNoIjoiYTgwMjQ1YTUtYjVkOC00MDE1LTg4NDQtZjNjNDI2MjEyOGQ3IiwiaWQiOiJhODAyNDVhNS1iNWQ4LTQwMTUtODg0NC1mM2M0MjYyMTI4ZDcifSwiY29udGVudCI6eyJ0eXBlIjoicGFnZSIsInZlcnNpb24iOiI4IiwiaWQiOiI3Mjg4OTE1NTcifSwic3BhY2UiOnsia2V5IjoiUFVCTElDIiwiaWQiOiI2MzczNzAzNjkifX19LCJleHAiOjE2MTk1OTI2MTMsImlhdCI6MTYxOTU5MTcxM30.VzD9g\_VW5RO4D2SopUkPc18RiwEkdcYGlQAsha5noFA",    "structuredContext": "{\"license\":{\"active\":true},\"confluence\":{\"macro\":{\"outputType\":\"html\_export\",\"hash\":\"a80245a5-b5d8-4015-8844-f3c4262128d7\",\"id\":\"a80245a5-b5d8-4015-8844-f3c4262128d7\"},\"content\":{\"type\":\"page\",\"version\":\"8\",\"id\":\"728891557\"},\"space\":{\"key\":\"PUBLIC\",\"id\":\"637370369\"}}}",  
    "contentClassifier":"content",  
    "productCtx":"{\"page.id\":\"728891557\",\"macro.hash\":\"a80245a5-b5d8-4015-8844-f3c4262128d7\",\"page.type\":\"page\",\": = \| RAW \| = :\":\"imageAttachmentId=att728694890\|macroId=4aeba792-a987-413a-bd3c-a38b2e004ad9\|baseUrl=https://enturas.atlassian.net/wiki\|name=network-additionalNetwork\|migration=1\|diagramAttachmentId=att728891568\|containerId=728891557\|timestamp=1550499536535\",\"space.id\":\"637370369\",\"diagramAttachmentId\":\"att728891568\",\"containerId\":\"728891557\",\"timestamp\":\"1550499536535\",\"space.key\":\"PUBLIC\",\"user.id\":\"5d19f8a491943f0d2ac51bcd\",\"content.version\":\"8\",\"page.title\":\"Multiple Authorities\",\"macro.body\":\"\",\"macro.truncated\":\"false\",\"content.type\":\"page\",\"output.type\":\"html\_export\",\"page.version\":\"8\",\"imageAttachmentId\":\"att728694890\",\"user.key\":\"8a7f808a6baf906b016bb1b5167f00d5\",\"macroId\":\"4aeba792-a987-413a-bd3c-a38b2e004ad9\",\"baseUrl\":\"https://enturas.atlassian.net/wiki\",\"content.id\":\"728891557\",\"name\":\"network-additionalNetwork\",\"migration\":\"1\",\"macro.id\":\"a80245a5-b5d8-4015-8844-f3c4262128d7\"}",  
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


### Link <a id="MultipleAuthorities-Link"></a>

The entire XML sample file is located on the project's GitHub repository [https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-additionalNetworks.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-additionalNetworks.xml)

### Elements <a id="MultipleAuthorities-Elements"></a>

#### organizations <a id="MultipleAuthorities-organizations"></a>

In the common file of the data set, one [Authority](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370398/framework#framework-Authority) is defined for each grouping of route data. 

```text
<organisations>
	<Authority version="1" id="OPP:Authority:1">
		<CompanyNumber>1</CompanyNumber>
		<Name>Opplandstrafikk</Name>
		<LegalName>Oppland fylkeskommune</LegalName>
		<ContactDetails>
			<Url>https://www.opplandstrafikk.no/</Url>
		</ContactDetails>
		<OrganisationType>authority</OrganisationType>
	</Authority>
	<Authority version="1" id="OPP:Authority:2">
		<CompanyNumber>2</CompanyNumber>
		<Name>Skibladner</Name>
		<LegalName>DS Skibladner</LegalName>
		<ContactDetails>
			<Url>https://www.skibladner.no/</Url>
		</ContactDetails>
		<OrganisationType>authority</OrganisationType>
	</Authority>
</organisations>
```

#### Difference between Network & additionalNetworks <a id="MultipleAuthorities-DifferencebetweenNetwork&amp;additionalNetworks"></a>

If the dataset does not have divisions, only one Network is defined. If the dataset is to be divided into several Authorities, these are sent as additionalNetworks.

It does not matter which Authority is in Network or additionalNetworks.

**Network**

If the dataset uniformly belongs to the same Authority, only Network is sent. 

_Simplified example:_

```text
<Network version="1" id="OPP:Network:1">
	<Name>Opplandstrafikk</Name>
	<AuthorityRef version="1" ref="OPP:Authority:1"/>
	<groupsOfLines>
		<GroupOfLines version="1" id="OPP:GroupOfLines:1">
			<Name>Fylkestrafikkerende buss</Name>
		</GroupOfLines>
	</groupsOfLines>
</Network>
```

If necessary, the lines can be grouped at the subordinate level: [GroupOfLines](handbok-n801-siri-netex-network.md#network-GroupOfLines).

**additionalNetworks**

When certain lines have to be separated from the main Authority of the dataset, these can be linked to additionalNetworks.

_Simplified example - in the example, Oppland county has provided route data on behalf of Skibladner:_

```text
<additionalNetworks>
	<Network version="1" id="OPP:Network:2">
		<Name>Skibladner</Name>
		<AuthorityRef version="1" ref="OPP:Authority:2"/>
		<groupsOfLines>
			<GroupOfLines version="1" id="OPP:GroupOfLines:2">
				<Name>Skibladner</Name>
			</GroupOfLines>
		</groupsOfLines>
	</Network>
</additionalNetworks>
```

#### Line <a id="MultipleAuthorities-Line"></a>

Data is submitted in the normal way, with one single ZIP-file containing one XML file per Line, plus a common file.

The examples below show examples for [Line](handbok-n801-siri-netex-network.md#network-Line) with two different GroupOfLines, expanding upon the above examples - subsequently referring to two separate Networks and Authorities.

**Line in the main Network**

_Simplified example:_

```text
<Line version="1" id="OPP:Line:1">
	<Name>Dokka-Fagernes</Name>
	<TransportMode>bus</TransportMode>
	<TransportSubmode>
		<BusSubmode>localBus</BusSubmode>
	</TransportSubmode>
	<PublicCode>1</PublicCode>
	<!--OperatorRef ref="[demo]"/-->
	<RepresentedByGroupRef version="1" ref="OPP:GroupOfLines:1"/>
</Line>
```

**Line in the additional Network**

_Simplified example:_

```text
<Line version="112" id="OPP:Line:5002_247">
	<Name>Eidsvoll-Lillehammer</Name>
	<TransportMode>water</TransportMode>
	<TransportSubmode>
		<WaterSubmode>localPassengerFerry</WaterSubmode>
	</TransportSubmode>
	<PublicCode>2</PublicCode>
	<!--OperatorRef ref="[demo]"/-->
	<RepresentedByGroupRef version="1" ref="OPP:GroupOfLines:2"/>
</Line>
```

