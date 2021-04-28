# Håndbok N801 \(SIRI/NeTEX\) : SIRI-ET - Changed platform

XML

See complete examples:

* Before change:  [https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-quay-change-1.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-quay-change-1.xml)
* After change:  [https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-quay-change-2.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-quay-change-2.xml)

When any platform \(Quay\) is changed, **the entire sequence of stops must be re-confirmed in the dataset**.

## Original dataset <a id="SIRI-ET-Changedplatform-Originaldataset"></a>

In the original SIRI dataset \(or the planned data\) the **last stop** of the vehicle is `<StopPointRef>NSR:Quay:1079</StopPointRef>` \(_See the last EstimatedCall of the dataset_\). In `<ArrivalStopAssignment>` the values for `<AimedQuayRef>` and `<ExpectedQuayRef>` are equal.

```text
<EstimatedCall>
    <StopPointRef>NSR:Quay:1079</StopPointRef>
    <Order>5</Order>
    <StopPointName>Trondheim</StopPointName>
    <RequestStop>false</RequestStop>
    <AimedArrivalTime>2019-08-16T22:49:00+02:00</AimedArrivalTime>
    <ExpectedArrivalTime>2019-08-16T22:49:00+02:00</ExpectedArrivalTime>
    <ArrivalStatus>onTime</ArrivalStatus>
    <ArrivalPlatformName>2</ArrivalPlatformName>
    <ArrivalBoardingActivity>alighting</ArrivalBoardingActivity>
    <ArrivalStopAssignment>
        <AimedQuayRef>NSR:Quay:1079</AimedQuayRef>
        <ExpectedQuayRef>NSR:Quay:1079</ExpectedQuayRef>
    </ArrivalStopAssignment>
</EstimatedCall>
```

## After the platform is changed <a id="SIRI-ET-Changedplatform-Aftertheplatformischanged"></a>

The **last stop** `<StopPointRef>NSR:Quay:1079</StopPointRef>` is **replaced by** `<StopPointRef>NSR:Quay:1078</StopPointRef>` \(both are Trondheim\). Also `<ExpectedQuayRef>NSR:Quay:1079</ExpectedQuayRef>` is **replaced by** `<ExpectedQuayRef>NSR:Quay:1078</ExpectedQuayRef>` in `<ArrivalStopAssignment>.`

```text
<EstimatedCall>
    <StopPointRef>NSR:Quay:1078</StopPointRef>
    <Order>5</Order>
    <StopPointName>Trondheim</StopPointName>
    <RequestStop>false</RequestStop>
    <AimedArrivalTime>2019-08-16T22:49:00+02:00</AimedArrivalTime>
    <ExpectedArrivalTime>2019-08-16T22:49:00+02:00</ExpectedArrivalTime>
    <ArrivalStatus>onTime</ArrivalStatus>
    <ArrivalPlatformName>1</ArrivalPlatformName>
    <ArrivalBoardingActivity>alighting</ArrivalBoardingActivity>
    <ArrivalStopAssignment>
        <AimedQuayRef>NSR:Quay:1079</AimedQuayRef>
        <ExpectedQuayRef>NSR:Quay:1078</ExpectedQuayRef>
    </ArrivalStopAssignment>
</EstimatedCall>
```

