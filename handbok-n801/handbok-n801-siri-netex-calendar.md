# Håndbok N801 \(SIRI/NeTEX\) : Calendar

**Content**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591717109 {padding: 0px;}  
div.rbtoc1619591717109 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591717109 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Calendar-objects](handbok-n801-siri-netex-calendar.md#Calendar-Calendar-objects)
  * [Link](handbok-n801-siri-netex-calendar.md#Calendar-Link)
  * [Elements](handbok-n801-siri-netex-calendar.md#Calendar-Elements)
    * [PublicationDelivery](handbok-n801-siri-netex-calendar.md#Calendar-PublicationDelivery)
    * [ServiceCalendarFrame](handbok-n801-siri-netex-calendar.md#Calendar-ServiceCalendarFrame)
      * [ServiceCalendarFrame](handbok-n801-siri-netex-calendar.md#Calendar-ServiceCalendarFrame.1)
    * [dayTypes](handbok-n801-siri-netex-calendar.md#Calendar-dayTypes)
    * [timebands](handbok-n801-siri-netex-calendar.md#Calendar-timebands)
    * [operatingDays](handbok-n801-siri-netex-calendar.md#Calendar-operatingDays)
    * [operatingPeriods](handbok-n801-siri-netex-calendar.md#Calendar-operatingPeriods)
    * [dayTypeAssignments](handbok-n801-siri-netex-calendar.md#Calendar-dayTypeAssignments)

## Calendar-objects <a id="Calendar-Calendar-objects"></a>

A [Service Calendar](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/637370410/timetable#timetable-ServiceCalendar) defines days, dayType, operational periods and other calendar items, as well as the connections between them. These definitions are further used \(mainly\) in the [Timetable](handbok-n801-siri-netex-timetable.md) to specify when a Line operates.

### Link <a id="Calendar-Link"></a>

The XML example in it its entirety can be found in the GitHub repository: [https://github.com/entur/profile-norway-examples/blob/master/netex/schedule/ServiceCalendar-example.xml](https://github.com/entur/profile-norway-examples/blob/master/netex/schedule/ServiceCalendar-example.xml)

### Elements <a id="Calendar-Elements"></a>

Below is a more detailed description of the most important elements of modelling a calendar object.

Note that this is only a **simplified** example of NeTEx XML.

#### PublicationDelivery <a id="Calendar-PublicationDelivery"></a>

All XML files according to the [Norwegian NeTEx profile](handbok-n801-siri-netex-nordic-netex-profile.md) should be of type _PublicationDelivery_ containing relevant [Frames](). \(See [_GitHub_](https://github.com/entur/profile-norway-examples/blob/master/netex/frames/publicationDelivery.xml) __for a complete example.\)

Description of the _dummy_ _ServiceFrame_ and _TimetableFrame_ in the example is only included to indicate a complete _PublicationDelivery_.

#### ServiceCalendarFrame <a id="Calendar-ServiceCalendarFrame"></a>

All calendar objects are defined in a [ServiceCalendarFrame](). It _can_ be done in a [ServiceCalendar ](handbok-n801-siri-netex-timetable.md#timetable-ServiceCalendar)object, but given that most components are often reused across the dataset, it is recommended to define these directly in _ServiceCalendarFrame_.

**ServiceCalendarFrame**

```text
<ServiceCalendarFrame version="any" id="RUT:ServiceCalendarFrame:1">
	<ServiceCalendar version="any" id="RUT:ServiceCalendar">
		<Name>Weekdays</Name>
		<FromDate>2019-04-01</FromDate>
		<ToDate>2019-08-31</ToDate>
	</ServiceCalendar>
[...]
```

#### dayTypes <a id="Calendar-dayTypes"></a>

Defining day type by means of weekdays.

```text
<dayTypes>
	<DayType version="any" id="RUT:DayType:weekdays">
		<Name>Ukedager</Name>
		<properties>
			<PropertyOfDay>
				<DaysOfWeek>Monday Tuesday Wednesday Thursday Friday</DaysOfWeek>
			</PropertyOfDay>
		</properties>
	</DayType>
	[...]
</dayTypes>
```

#### timebands <a id="Calendar-timebands"></a>

Timeband shows time indication.

* StartTime and EndTime or Duration specify the period span.
* If StartTime and EndTime are equal it specifies a _specific_ time. E.g. when specifying a repeating hourly departure \(in [Rhythmical Journey](handbok-n801-siri-netex-general-information-netex.md#Generalinformation:NeTEx-RhythmicalJourneyGroup)\), this is indicated by a consistent time of "00".

```text
<timebands>
	<Timeband version="any" id="RUT:Timeband:TM15">
		<!--Name>15 minutes past the hour</Name-->
		<StartTime>00:15:00</StartTime>
		<EndTime>00:15:00</EndTime>
	</Timeband>
</timebands>
```

#### operatingDays <a id="Calendar-operatingDays"></a>

Specification of an operating day, possibly also the start and length of an operating day. Can be linked to a dayType , e.g. [Kalender\#dayTypeAssignments](https://enturas.atlassian.net/wiki/pages/resumedraft.action?draftId=637370377#Kalender-dayTypeAssignments).

```text
<operatingDays>
	<OperatingDay version="any" id="RUT:OperatingDay:default:1">
		<CalendarDate>2016-05-01</CalendarDate>
		<EarliestTime>10:10:00</EarliestTime>
		<DayLength>PT12H45M</DayLength>
	</OperatingDay>
	<OperatingDay version="any" id="RUT:od:default:2">
		<CalendarDate>2016-07-07</CalendarDate>
		<EarliestTime>11:11:00</EarliestTime>
		<DayLength>PT9H10M</DayLength>
	</OperatingDay>
</operatingDays>
```

#### operatingPeriods <a id="Calendar-operatingPeriods"></a>

Specification of an operating period, based on previously defined start and end days.

```text
<operatingPeriods>
	<OperatingPeriod version="any" id="RUT:op:default">
		<FromOperatingDayRef ref="RUT:OperatingDay:default:1"/>
		<ToOperatingDayRef ref="RUT:od:default:2"/>
	</OperatingPeriod>
</operatingPeriods>
```

#### dayTypeAssignments <a id="Calendar-dayTypeAssignments"></a>

Attaching a dayType to a specific date or pre-defined OperatingDay/Period for a given calendar, i.e. a dayType will be valid within the time period specified by the calendar object to which it is associated.

```text
<dayTypeAssignments>
	[...]
	<DayTypeAssignment version="any" order="1" id="RUT:DayTypeAssignment:period">
		<OperatingPeriodRef ref="RUT:OperatingPeriod:default"/>
		<DayTypeRef version="any" ref="RUT:DayType:weekdays"/>
	</DayTypeAssignment>
</dayTypeAssignments>
```

