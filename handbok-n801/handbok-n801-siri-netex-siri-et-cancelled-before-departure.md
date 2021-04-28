# Håndbok N801 \(SIRI/NeTEX\) : SIRI-ET - Cancelled before departure

XML

See complete examples:

* Before departure:  [https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-last-stops.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-last-stops.xml)
* After departure:  [https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-last-stops-after-departure.xml](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-last-stops-after-departure.xml)

## Example: Train is cancelled between Dombås and Trondheim <a id="SIRI-ET-Cancelledbeforedeparture-Example:TrainiscancelledbetweenDomb&#xE5;sandTrondheim"></a>

### Published data _before_ departure <a id="SIRI-ET-Cancelledbeforedeparture-Publisheddatabeforedeparture"></a>

#### Last served stop: <a id="SIRI-ET-Cancelledbeforedeparture-Lastservedstop:"></a>

Dombås status has **not** been set to `<Cancellation>true</Cancellation>`, **but** `<DepartureStatus>cancelled</DepartureStatus>`.

#### Cancelled stops <a id="SIRI-ET-Cancelledbeforedeparture-Cancelledstops"></a>

The successive stops are cancelled **by setting** `<Cancellation>true</Cancellation>` **in addition to** `<ArrivalStatus>cancelled</ArrivalStatus>` **and** `<DepartureStatus>cancelled</DepartureStatus>`.

The **exception** is the final stops, Trondheim, which **does not have** departure information and subsequently **cannot have** `<DepartureStatus>cancelled</DepartureStatus>`.

### Published data _after_ departure <a id="SIRI-ET-Cancelledbeforedeparture-Publisheddataafterdeparture"></a>

If a vehicle becomes partially cancelled after it has begun its journey, the changes are sent as _EstimatedCalls_ in the same way as when cancelling before departure.

The example _"after departure"_ shows the vehicle has passed Otta and been partially cancelled from Dombås and onward. The vehicles final stop is now Dombås.

