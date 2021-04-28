# Håndbok N801 \(SIRI/NeTEX\) : SIRI-ET - Partial cancellation \(first leg\)

**Content**

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591773681 {padding: 0px;}  
div.rbtoc1619591773681 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591773681 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [The first part of the journey has been cancelled](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md#SIRI-ET-Partialcancellation%28firstleg%29-Thefirstpartofthejourneyhasbeencancelled)
  * [Before departure](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md#SIRI-ET-Partialcancellation%28firstleg%29-Beforedeparture)
    * [RecordedCall](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md#SIRI-ET-Partialcancellation%28firstleg%29-RecordedCall)
    * [EstimatedCall](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md#SIRI-ET-Partialcancellation%28firstleg%29-EstimatedCall)
  * [Etter avgang](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md#SIRI-ET-Partialcancellation%28firstleg%29-Etteravgang)
    * [RecordedCall](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md#SIRI-ET-Partialcancellation%28firstleg%29-RecordedCall.1)
    * [EstimatedCall](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md#SIRI-ET-Partialcancellation%28firstleg%29-EstimatedCall.1)

XML

See complete example:

* [https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-first-stops.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-first-stops.xml)

## The first part of the journey has been cancelled <a id="SIRI-ET-Partialcancellation(firstleg)-Thefirstpartofthejourneyhasbeencancelled"></a>

The vehicle has a planned cancellation of the **Vinstra to Dovre** leg but plans to execute the **Dovre to Trondheim** leg.

Since the cancellation includes stops from the very beginning of the route, which must always be described fully \(all stops in the journey listed\), _RecordedCalls_ for the cancelled leg must be submitted.

_EstimatedCalls_ \(before passing\)/_RecordedCalls_ \(after passing\) are submitted as usual for the operational leg.

### Before departure <a id="SIRI-ET-Partialcancellation(firstleg)-Beforedeparture"></a>

#### RecordedCall <a id="SIRI-ET-Partialcancellation(firstleg)-RecordedCall"></a>

For cancelled stops.

  
**RecordedCall**

```text
<RecordedCall>
	<StopPointRef>NSR:Quay:709</StopPointRef>
	<Order>1</Order>
	<StopPointName>Vinstra</StopPointName>
	<Cancellation>true</Cancellation>
	<AimedDepartureTime>2018-04-18T13:05:00</AimedDepartureTime>
</RecordedCall>
```

#### EstimatedCall <a id="SIRI-ET-Partialcancellation(firstleg)-EstimatedCall"></a>

For stops which will be served.

_Please note that this RecordedCall is **not** included in the complete XML example, as the example describes data submitted **after** the stop was served \(see_ [_RecordedCall_](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370798#SIRI-ET-Partialcancellation%28firstleg%29-RecordedCall.1)_\)._**RecordedCall**

```text
<RecordedCall>
	<StopPointRef>NSR:Quay:1067</StopPointRef>
	<Order>4</Order>
	<StopPointName>Dovre</StopPointName>
	<AimedArrivalTime>2018-04-18T13:51:50</AimedArrivalTime>
	<ExpectedDepartureTime>2018-04-18T13:52:00</ExpectedDepartureTime>
	<ActualDepartureTime>2018-04-18T13:52:00</ActualDepartureTime>
</RecordedCall>
```

### Etter avgang <a id="SIRI-ET-Partialcancellation(firstleg)-Etteravgang"></a>

#### RecordedCall <a id="SIRI-ET-Partialcancellation(firstleg)-RecordedCall.1"></a>

For already served stops.

  
**RecordedCall**

```text
<RecordedCall>
	<StopPointRef>NSR:Quay:1067</StopPointRef>
	<Order>4</Order>
	<StopPointName>Dovre</StopPointName>
	<AimedArrivalTime>2018-04-18T13:51:50</AimedArrivalTime>
	<ExpectedDepartureTime>2018-04-18T13:52:00</ExpectedDepartureTime>
	<ActualDepartureTime>2018-04-18T13:52:00</ActualDepartureTime>
</RecordedCall>
```

#### EstimatedCall <a id="SIRI-ET-Partialcancellation(firstleg)-EstimatedCall.1"></a>

For upcoming stops \(re-estimated continuously\).**RecordedCall**

```text
<EstimatedCall>
	<StopPointRef>NSR:Quay:519</StopPointRef>
	<Order>6</Order>
	<StopPointName>Oppdal</StopPointName>
	<RequestStop>false</RequestStop>
	<AimedArrivalTime>2018-04-18T14:59:00</AimedArrivalTime>
	<ExpectedArrivalTime>2018-04-18T15:03:00</ExpectedArrivalTime>
	<ArrivalStatus>onTime</ArrivalStatus>
	<ArrivalBoardingActivity>alighting</ArrivalBoardingActivity>
	<AimedDepartureTime>2018-04-18T15:02:00</AimedDepartureTime>
	<ExpectedDepartureTime>2018-04-18T15:05:00</ExpectedDepartureTime>
	<DepartureStatus>onTime</DepartureStatus>
	<DepartureBoardingActivity>boarding</DepartureBoardingActivity>
</EstimatedCall>
```

