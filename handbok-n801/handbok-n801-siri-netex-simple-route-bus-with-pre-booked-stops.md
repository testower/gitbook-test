# Håndbok N801 \(SIRI/NeTEX\) : Simple route - Bus with pre-booked stops

**Innhold**/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591736827 {padding: 0px;}  
div.rbtoc1619591736827 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591736827 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Express bus Sørlandsekspressen](handbok-n801-siri-netex-simple-route-bus-with-pre-booked-stops.md#Simpleroute-Buswithpre-bookedstops-ExpressbusSørlandsekspressen)
  * [PublicationDelivery](handbok-n801-siri-netex-simple-route-bus-with-pre-booked-stops.md#Simpleroute-Buswithpre-bookedstops-PublicationDelivery)
  * [Service Frame](handbok-n801-siri-netex-simple-route-bus-with-pre-booked-stops.md#Simpleroute-Buswithpre-bookedstops-ServiceFrame)
    * [BookingArrangements](handbok-n801-siri-netex-simple-route-bus-with-pre-booked-stops.md#Simpleroute-Buswithpre-bookedstops-BookingArrangements)

## Express bus Sørlandsekspressen <a id="Simpleroute-Buswithpre-bookedstops-ExpressbusS&#xF8;rlandsekspressen"></a>

### PublicationDelivery <a id="Simpleroute-Buswithpre-bookedstops-PublicationDelivery"></a>

Because some data structures relevant to this example have already been covered in [Simple route - Bus \(rhythm based departures\)](handbok-n801-siri-netex-simple-rhythm-based-bus-line.md) and [Projection](handbok-n801-siri-netex-projection.md), parts of the relevant structure have been omitted, and this example covers only the [StopPointInJourneyPattern](https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/728563886/network#network-StopPointInJourneyPattern) structure.

### Service Frame <a id="Simpleroute-Buswithpre-bookedstops-ServiceFrame"></a>

#### BookingArrangements <a id="Simpleroute-Buswithpre-bookedstops-BookingArrangements"></a>

BookingArrangements provides details on the booking conditions for a specific stop when they differ from conditions defined at the line level.

In particular, the booking method and the required period for prior booking of on-demand stops can be specified. For example _per StopPointInJourneyPattern_.

```text
  <StopPointInJourneyPattern order="7" version="1" id="NBE:StopPointInJourneyPattern:1900002_1_1aNSR_Quay_101494_22">
    <ScheduledStopPointRef ref="NBE:ScheduledStopPoint:1900002_1_1aNSR_Quay_101494_22"/>
    
    <!-- The bus stops only on demand: passengers should book online or by phone, at least 10 minutes before departure -->
    <BookingArrangements>
          <BookingContact>
              <Phone>+47 407 05 070</Phone>
              <Url>https://www.nettbuss.no</Url>
          </BookingContact>
          <BookingMethods>callOffice online</BookingMethods>
          <BookingAccess>public</BookingAccess>
          <BookWhen>advanceAndDayOfTravel</BookWhen>
          <BuyWhen>onReservation</BuyWhen>
          <MinimumBookingPeriod>PT10M</MinimumBookingPeriod>
    </BookingArrangements>
  </StopPointInJourneyPattern>
```

