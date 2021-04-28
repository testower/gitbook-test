# Håndbok N801 \(SIRI/NeTEX\) : Multimodal interchanges

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591717163 {padding: 0px;}  
div.rbtoc1619591717163 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591717163 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [An interchange between "on-demand transport" and a bus or train](handbok-n801-siri-netex-multimodal-interchanges.md#Multimodalinterchanges-Aninterchangebetween%22on-demandtransport%22andabusortrain)
  * [JopurneyPattern](handbok-n801-siri-netex-multimodal-interchanges.md#Multimodalinterchanges-JopurneyPattern)
    * [Modelling](handbok-n801-siri-netex-multimodal-interchanges.md#Multimodalinterchanges-Modelling)
    * [Link](handbok-n801-siri-netex-multimodal-interchanges.md#Multimodalinterchanges-Link)
  * [Elements](handbok-n801-siri-netex-multimodal-interchanges.md#Multimodalinterchanges-Elements)
    * [journeyInterchanges](handbok-n801-siri-netex-multimodal-interchanges.md#Multimodalinterchanges-journeyInterchanges)

## An interchange between "on-demand transport" and a bus or train <a id="Multimodalinterchanges-Aninterchangebetween&quot;on-demandtransport&quot;andabusortrain"></a>

According to the Norwegian NeTEx-profile, each [Line](handbok-n801-siri-netex-network.md#network-Line) must be defined in its own separate XML-file.

### JopurneyPattern <a id="Multimodalinterchanges-JopurneyPattern"></a>

On-demand line 316, both directions link up with:

• Train L1 towards Lillestrøm/Oslo \(at "Hanaborg stasjon"\)  
• Bus 100 towards Lillestrøm/Oslo \(at "Lørenskog sentrum"\)

#### Modelling <a id="Multimodalinterchanges-Modelling"></a>

Interchanges are modelled in NeTEx by defining [journeyInterchanges](handbok-n801-siri-netex-timetable.md#timetable-Interchange) \(in [TimetableFrame]()\) specifying which terms apply for interchange between the respective lines.

#### Link <a id="Multimodalinterchanges-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-316-with-interchange.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-316-with-interchange.xml)

### Elements <a id="Multimodalinterchanges-Elements"></a>

Many of the basic elements of a line are described in more detail in the [Simple rhythm based bus line](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md) example, and will not be detailed in this document.

Line 316 is an on-demand line which is covered more closely in the [On-demand transport](handbok-n801-siri-netex-on-demand-transport.md) example. Therefore many elements relevant to this type of transport are omitted here, instead focusing on only the most important elements of multimodal interchanges.

#### journeyInterchanges <a id="Multimodalinterchanges-journeyInterchanges"></a>

Specified in the timetable with a [ServiceJourneyInterchange](handbok-n801-siri-netex-timetable.md#timetable-ServiceJourneyInterchange).

```text
<ServiceJourneyInterchange version="any" id="RUT:ServiceJourneyInterchange:ID-HANABORG_ST-316-to-L1-A">
	<Description>2Ø Tog mot Lillestrøm 1019</Description>
	<Priority>1</Priority>
	<StaySeated>false</StaySeated>
	<Planned>true</Planned>
	<Guaranteed>false</Guaranteed>
	<Advertised>true</Advertised>
	<MaximumWaitTime>PT0M</MaximumWaitTime>
	<FromPointRef version="any" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST"/>
	<ToPointRef version="any" ref="RUT:ScheduledStopPoint:ID-HANABORG_ST"/>
	<FromJourneyRef version="any" ref="RUT:ServiceJourney:0316-TilLorenskog"/>
	<ToJourneyRef ref="NSB:ServiceJourney:L1-Spikkestad-1-ExternalRef"/>
</ServiceJourneyInterchange>
[...]
<ServiceJourneyInterchange version="any" id="RUT:ServiceJourneyInterchange:ID-LORENSKOG-316-to-100-A">
	<Description>2Ø Buss 100 mot Oslo 1022</Description>
	<Priority>1</Priority>
	<StaySeated>false</StaySeated>
	<Planned>true</Planned>
	<Guaranteed>false</Guaranteed>
	<Advertised>true</Advertised>
	<MaximumWaitTime>PT0M</MaximumWaitTime>
	<FromPointRef version="any" ref="RUT:ScheduledStopPoint:ID-LORENSKOG"/>
	<ToPointRef version="any" ref="RUT:ScheduledStopPoint:ID-LORENSKOG"/>
	<FromJourneyRef version="any" ref="RUT:ServiceJourney:0316-TilLorenskog"/>
	<ToJourneyRef ref="RUT:ServiceJourney:100-Oslo-1-ExtenalRef"/>
</ServiceJourneyInterchange>
```

