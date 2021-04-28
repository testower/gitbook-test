# Håndbok N801 \(SIRI/NeTEX\) : Profile documents

## Content <a id="Profiledocuments-Content"></a>

* [framework]()
  * [Norwegian submodes and their definitions](handbok-n801-siri-netex-norwegian-submodes-and-their-definitions.md)
* [stops](handbok-n801-siri-netex-stops.md)
* [network](handbok-n801-siri-netex-network.md)
  * [Flexible Line Types](handbok-n801-siri-netex-flexible-line-types.md)
* [timetable](handbok-n801-siri-netex-timetable.md)
* [fares](handbok-n801-siri-netex-fares.md)
* [sales](handbok-n801-siri-netex-sales.md)

## Changelog <a id="Profiledocuments-Changelog"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Date</th>
      <th style="text-align:left">Profile document</th>
      <th style="text-align:left">Change</th>
      <th style="text-align:left">Version</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">14 Apr 2021</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-netex-examples-catalogue.md">NeTEx examples catalogue</a>,
        <br
        /><a href="handbok-n801-siri-netex-general-information-netex.md">General information: NeTEx</a>,
        <br
        /><a href>framework</a>,
        <br /><a href="handbok-n801-siri-netex-stops.md">stops</a>,
        <br /><a href="https://enturas.atlassian.net/wiki/spaces/ROR/pages/637370412/network">network</a>,
        <br
        /><a href="handbok-n801-siri-netex-timetable.md">timetable</a>,
        <br /><a href="handbok-n801-siri-netex-fares.md">fares</a>,
        <br /><a href="https://enturas.atlassian.net/wiki/spaces/PUBLIC/pages/1638137934/fares+work+in+progress">sales</a>
      </td>
      <td style="text-align:left">
        <p><b>Change requests #2, 3, 4, 5, 6, 7, 8, 15, 16, 17, 18, 21, 22, 23, 24, 25, 26, 27:</b>
        </p>
        <p>Updated example for Branding of a Network and/or Line</p>
        <p>General information</p>
        <ul>
          <li>Clarify paragraph &quot;<em>Structure of ID&apos;s</em>&quot; (mainly
            requirements for the <em>identification</em> element)</li>
        </ul>
        <p>framework</p>
        <ul>
          <li>Added groupsOfTariffZones to SiteFrame</li>
          <li>Elaborated description for use of multiple DayType-properties/PropertyOfDay
            to ensure compliance with NeTEx spec and XML Schema documentation</li>
          <li>Added HolidayTypes and Seasons elements for PropertyOfDay</li>
          <li>Added abstract data objects common for fares and sales</li>
          <li>Added FareFrame and SalesTransactionFrame</li>
          <li>Minor textual additions to clarify use of conditions</li>
          <li>Added information on Part 3 addition <em>Sales Transaction Frame</em> (currently
            not in use) and changed references from &quot;Norwegian&quot; to &quot;Nordic&quot;</li>
          <li>Simplified structure for organisation data
            <ul>
              <li>Removed Organisation &#x2192; <em>parts</em> placeholder (for listing OrganisationParts),
                as this way of constructing organisation data, is neither used nor implemented
                technically</li>
              <li>Removed <em>OrganisationPart</em> data object (not in use)</li>
              <li>Removed <em>Department</em> data object (not in use)</li>
              <li>Changed cardinality for Organisation &#x2192; <em>ContactDetails </em>(previously
                mandatory, however, this data is unknown for some Operators thus will only
                be mandatory for Authority type organisations)</li>
            </ul>
          </li>
          <li>Removed <em>SchematicMap</em> container (not in use)</li>
          <li>CheckConstraints corrections/additions
            <ul>
              <li>Adding further CheckProcess types</li>
              <li>Disallowing references from CheckConstraintDelay to CheckConstraint (i.e.
                a CheckConstraint may have a delay, but not the other way around)</li>
            </ul>
          </li>
          <li>Release of the requirement to have DataManagedObject &#x2192; <em>responsibilitySetRef</em> (rarely
            used, has never been enforced)</li>
          <li>Release of the requirement to have GroupOfEntities &#x2192; <em>Name</em> (supplementary
            description added to clarify when required and when optional)</li>
          <li>Release of requirement to have Place &#x2192; <em>TypeOfPlaceRef</em> (not
            in use, current implementations use TopographicPlaceType / StopPlaceType
            instead, description is updated accordingly)</li>
          <li>Allow for use of ISO 639-2 Alpha-3 (three-letter) language codes</li>
          <li>Clarification to use of coordinates and positioning tuples (default is
            first number latitude, second number longitude)</li>
        </ul>
        <p>stops</p>
        <ul>
          <li>Extended PurposeOfGroupingRef categories</li>
          <li>Added GroupOfFareZones</li>
          <li>Added FareZone (specification of TariffZone) with mandatory AuthorityRef- <em>WiP</em>
          </li>
          <li>Added <em>members</em> (ScheduledStopPoints within) to TariffZone</li>
          <li>Added Presentation data to TariffZone</li>
          <li>Moved definition of TariffZone here (from network), as the SiteFrame included
            the containing element</li>
          <li>Added PrivateCode and PublicCode for StopPlace</li>
        </ul>
        <p>network</p>
        <ul>
          <li>Added TimingPointStatus to ScheduledStopPoint</li>
          <li>Moved SiteConnection here (from stops) and added <em>connections</em> container
            to the ServiceFrame</li>
          <li>Released on requirements for FlexibleLine (removed explicit obligation
            &quot;<del><em>FlexibleLine <b>must </b>be used if one or more </em></del>
            <a
            href="handbok-n801-siri-netex-stops.md#stops-FlexibleStopPl"><del><em>FlexibleStopPlace</em></del>
              </a><del><em>(</em></del><a href="handbok-n801-siri-netex-stops.md#stops-FlexibleArea"><del><em>FlexibleArea</em></del></a><del><em>and/or</em></del>
              <a
              href="handbok-n801-siri-netex-stops.md#stops-HailAndRideAre"><del><em>HailAndRideArea</em></del>
                </a><del><em>) are present in the Line.</em></del>&quot;) to align better
                with the practical use of BookingArrangements for non-flexible lines as
                documented in the profile</li>
        </ul>
        <p>timetable</p>
        <ul>
          <li>Clarification to the usage of arrival/departure day offset</li>
        </ul>
        <p>fares</p>
        <ul>
          <li>Added preliminary profile document for fare/product related data (v0.8
            - <em>Work In Progress</em>)</li>
        </ul>
        <p>sales</p>
        <ul>
          <li>Added preliminary profile document for sales/transactions/consumption
            related data (v0.8 - <em>Work In Progress</em>)</li>
        </ul>
      </td>
      <td style="text-align:left">v1.4</td>
    </tr>
    <tr>
      <td style="text-align:left">21 Aug 2019</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stops.md">stops</a>
      </td>
      <td style="text-align:left">
        <p><b>Change request #2: Public and private codes for StopPlaces.</b>
        </p>
        <p>stops</p>
        <ul>
          <li>Adding PrivateCode (internal code uniquely identifying the Stop Place,
            usable for e.g. inter-operating with legacy systems)</li>
          <li>PublicCode (a short and human-readable code uniquely identifying the Stop
            Place, may be used as a convenient alternative to the name or ID)</li>
        </ul>
      </td>
      <td style="text-align:left">v1.4</td>
    </tr>
    <tr>
      <td style="text-align:left">19 Jun 2019</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stops.md">stops</a>
      </td>
      <td style="text-align:left">
        <p><b>Change request #1: Parking &#x2013; payment, spaces with recharge point, spaces for disabled users.</b>
        </p>
        <p>stops</p>
        <ul>
          <li>Added ParkingPaymentProcess enumeration in Parking.</li>
          <li>Added ParkingUserType enumeration in ParkingCapacity.</li>
          <li>Added NumberOfSpacesWithRechargePoint in ParkingCapacity.</li>
          <li>Updated description of TotalCapacity and RechargingAvailable in Parking
            for consistency with ParkingCapacity.</li>
        </ul>
      </td>
      <td style="text-align:left">v1.4</td>
    </tr>
    <tr>
      <td style="text-align:left">30 Aug 2018</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-general-information-netex.md">General information: NeTEx</a>,
        <br
        /><a href>framework</a>,
        <br /><a href="handbok-n801-siri-netex-network.md">network</a>,
        <br /><a href="handbok-n801-siri-netex-stops.md">stops</a>,
        <br /><a href="handbok-n801-siri-netex-timetable.md">timetable</a>
      </td>
      <td style="text-align:left">
        <p><em><b>This revision includes moving H&#xE5;ndbok N801, all profile documents, and GitHub-examples to a new domain (Entur).</b></em>
        </p>
        <p>General information</p>
        <ul>
          <li>Version reference changed to v1.3.</li>
        </ul>
        <p>framework</p>
        <ul>
          <li>Consolidated ticketing machine-modelling into <em>TicketingEquipment</em>.
            The duplicate element <em>TicketingFacilityList</em> was removed from the
            profile.</li>
          <li>Consolidated sanitary equipment-modelling into <em>SanitaryEquipment</em>.
            The duplicate element <em>SanitaryFacilityList</em> was removed from the
            profile.</li>
          <li>Added VehichleScheduleFrame in order to specify Blocks for a vehicle.</li>
          <li>TariffZones should be handled as a part of stop places and should, therefore,
            be part of SiteFrame, rather than ServiceFrame.</li>
          <li>Added &quot;cityTram&quot; as a tram submode. To be used by &quot;Bybanen&quot;.</li>
        </ul>
        <p>stops</p>
        <ul>
          <li>Added categorisation of GroupOfStopPlaces as a pre-defined reference to
            PurposeOfGrouping.</li>
          <li>Added new StopPlaceType &quot;taxiStand&quot;</li>
        </ul>
        <p>network</p>
        <ul>
          <li>Clarification on how to structure booking information for FlexibleLines.
            Some previously mandatory elements are no longer so.</li>
          <li>Removed redundant option <em>advanceOnly</em> for BookWhen (on <em>FlexibleLine</em>, <em>BookingArrangementsStructure</em> and <em>FlexibleServiceProperties</em>)</li>
          <li>Moved FlexibleServiceProperties to Timetable (used only in <em>TimetableFrame</em>)</li>
          <li>Clarification on the usage of Line &#x2192; Presentation</li>
          <li>Changed cardinality for Line &#x2192; Monitored and Line &#x2192; AccessibilityAssessment <em>(previously mandatory elements are no longer so. The reason for this is that most data providers will not be able to provide meaningful information for it)</em>
          </li>
          <li>Changed cardinality for ServiceLink &#x2192; projections <em>(previously mandatory elements are no longer so. The reason for this is that ServiceLinks technically have geographic positionings for parts of the way)</em>
          </li>
          <li>Remove unused objects associated with flexible transport (<em>FlexibleRoute, FlexibleLinkProperties, FlexiblePointProperties</em>)
            since these should be modelled using the general objects (<em>Route, ServiceLink, ScheduledStopPoint</em>).</li>
          <li>Added optional field <em>PrivateCode</em> for JourneyPattern.</li>
        </ul>
        <p>timetable</p>
        <ul>
          <li>Specified use of Priority for Interchange (specified as weighting, not
            sequential order).</li>
          <li>Removed optional fields <em>Planned</em> and <em>Advertised</em> for <em>Interchange</em>,
            since this will be implicit for specified interchanges.</li>
          <li>Clarification on <b>required</b> attributes ID and VERSION for TimetabledPassingTime <em>(has previously not been validated due to an unhandled discrepancy of the main NeTEx XML-Schema)</em>
          </li>
          <li>Clarification that referred <em>ServiceJourney</em>  <b>has to exist</b> in
            the <em>PublicationDelivery</em>.</li>
          <li>Added possible value ServiceJourney &#x2192; ServiceAlteration &quot;replaced&quot;
            for usage in replacement transport.</li>
          <li>The concept SpecialService removed from the profile (not in use). For
            &quot;special&quot; departures, use normal ServiceJourney and add FlexibleServiceProperties
            when relevant.</li>
          <li>Added DeadRun to make the modelling of trips without passengers possible.</li>
          <li>Clarification that interchanges across datasets should <em>only</em> be
            defined for the receiving/departing Line at the interchange.</li>
        </ul>
      </td>
      <td style="text-align:left">v1.3</td>
    </tr>
    <tr>
      <td style="text-align:left">07 Mar 2018</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-general-information-netex.md">General information: NeTEx</a>,
        <br
        /><a href>framework</a>,
        <br /><a href="handbok-n801-siri-netex-network.md">network</a>,
        <br /><a href="handbok-n801-siri-netex-stops.md">stops</a>,
        <br /><a href="handbok-n801-siri-netex-timetable.md">timetable</a>
      </td>
      <td style="text-align:left"><em>Full export (appendix H&#xE5;ndbok N801)</em>
      </td>
      <td style="text-align:left">v1.2</td>
    </tr>
    <tr>
      <td style="text-align:left">06 Mar 2018</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-general-information-netex.md">General information: NeTEx</a>,
        <br
        /><a href>framework</a>, <a href="handbok-n801-siri-netex-network.md">network</a>,
        <br
        /><a href="handbok-n801-siri-netex-timetable.md">timetable</a> 
        <br />
      </td>
      <td style="text-align:left">
        <p>General information</p>
        <ul>
          <li>Updated version references (NeTEx XSD v1.08 and Norwegian profiles v1.2)</li>
        </ul>
        <p>framework</p>
        <ul>
          <li>Removed references to default values for optional fields (they are not
            optional, and should be handled explicitly).</li>
          <li>New and clearer description for fields in <em>OrganisationPart</em>.</li>
          <li>It is now <b>required</b> that ContactStructure has <b>at least</b> Email,
            Phone or Url
            <ul>
              <li>For <em>CustomerServiceContactDetails,</em> the field <em>Url</em> is now <b>required</b>.</li>
            </ul>
          </li>
          <li>Listed allowed enumerations for DayType &#x2192; PropertyOfDay &#x2192;
            DayOfWeek and DayType &#x2192; PropertyOfDay &#x2192; WeeksOfMonth</li>
          <li>It is <b>no longer required</b> to include the <em>Distance</em> field for <em>LinkSequence</em>.</li>
          <li>Added optional field <em>AlternativeTexts</em> to support translations of <em>Notice</em> texts.</li>
          <li>Added the <em>NameType</em> &quot;<b>Label</b>&quot; for <em>AlternativeName</em>.</li>
          <li>Formalised the requirement for using <em>TimeZone</em> for local time in <em>Locale</em> (was
            already the de facto standard), and removed the optional fields <em>TimeZoneOffset</em> and <em>SummerTimeZoneOffset</em> which
            won&apos;t be used.</li>
        </ul>
        <p>stops</p>
        <ul>
          <li>Updated version number.</li>
        </ul>
        <p>network</p>
        <ul>
          <li>Specified usage of <em>ForAlighting</em> and <em>ForBoarding</em> on first-
            and last stop in <em>StopPointInJourneyPattern</em>.</li>
          <li>Added optional field <em>Distance</em> for <em>ServiceLink</em> (can be used
            to monitor vehicles via in real-time).</li>
          <li>Added optional field <em>ShortName</em> for Line (can be used for alternative
            names).</li>
          <li>Changed cardinality for <em>Line </em>&#x2192; <em>PublicCode</em> (a previously
            required element is no longer required since not all lines have an actual <em>PublicCode</em>).</li>
        </ul>
        <p>timetable</p>
        <ul>
          <li>Removed references to default values for optional fields (they are not
            optional, and should be handled explicitly).</li>
          <li>Added PrivateCode as an optional field on VehicleJourney for external-
            or dataset-specific ID&apos;s (such as train- or trip numbers).</li>
        </ul>
      </td>
      <td style="text-align:left">v1.2</td>
    </tr>
    <tr>
      <td style="text-align:left">13 Sep 2017</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-general-information-netex.md">General information: NeTEx</a>,
        <br
        /><a href>framework</a>,
        <br /><a href="handbok-n801-siri-netex-network.md">network</a>,
        <br /><a href="handbok-n801-siri-netex-stops.md">stops</a>,
        <br /><a href="handbok-n801-siri-netex-timetable.md">timetable</a>
      </td>
      <td style="text-align:left"><em>Full export (appendix H&#xE5;ndbok N801)</em>
      </td>
      <td style="text-align:left">v1.1</td>
    </tr>
    <tr>
      <td style="text-align:left">12 Sep 2017</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-general-information-netex.md">General information: NeTEx</a>,
        <br
        /><a href>framework</a>,
        <br /><a href="handbok-n801-siri-netex-stops.md">stops</a>,
        <br /><a href="handbok-n801-siri-netex-network.md">network</a>,
        <br /><a href="handbok-n801-siri-netex-timetable.md">timetable</a>
      </td>
      <td style="text-align:left">
        <p>All profile documents:</p>
        <ul>
          <li>Consolidation of links.</li>
        </ul>
        <p>General information:</p>
        <ul>
          <li>Clarification regarding the use of versions.</li>
          <li>Clarification regarding ID formatting.</li>
          <li>Revised list of definitions according to changes of profile documents
            (added new-/removed outdated objects)</li>
          <li>Clarification on how a common objects file must be used.</li>
        </ul>
        <p>framework:</p>
        <ul>
          <li>Changed cardinality for <em>Point </em>&#x2192; <em>Location</em>. Previously
            required elements are no longer required when the geographic position can
            be derived from projection or links to another locational object.</li>
          <li>Changed incorrect cardinality for <em>Zone &lt; GroupOfPoints &lt; GroupOfEntities &lt; DataManagedObject</em>.
            The implementation (NeTEx-XSD) only allows 0 or 1 of <em>gml:Polygon</em> (not
            0 to many) for <em>Zone</em>.</li>
          <li>Added equipment type &quot;sign&quot;: GeneralSign &lt; SignEquipment
            &lt; PlaceEquipment &lt; Equipment &lt; DataManagedObject
            <ul>
              <li>There are explicit demands for modelling stop place signs.</li>
            </ul>
          </li>
          <li>Changed recommended modelling of walk paths to independent <em>pathLinks, </em>instead
            of <em>NavigationPaths</em> consisting of <em>pathLinks, </em>for objects
            which support this, since NavigationPath can be derived from them.</li>
          <li>Removed redundant and optional field <em>AllAreasWheelchair</em> for <em>PathLink/PathJunction</em>.
            The information can be derived from AccessibilityAssessment &#x2192; MobilityImpairedAccess
            &#x2192; <em>WheelchairAccess</em> (<em>required value</em>).</li>
          <li>Added <em>placeEquipments</em> (<em>equipmentPlaces</em> minus specified <em>Location</em>)
            for <em>Site</em>.</li>
          <li>Added <em>localServices</em> under <em>Site</em>
          </li>
          <li>Changed the abstract type <em>WaitingEquipment</em> to the correct <em>SiteEquipment</em> data
            type <em>WaitingRoomEquipment</em> (inherits from <em>WaitingEquipment</em>)</li>
          <li>Adjusted requirements of data fields for <em>Organisation</em> (specifically
            incl. <em>Authority</em>/<em>Operator</em>)</li>
          <li>Added fields for a possibly explicit <em>PrivateContactDetails</em> for <em>Organisation</em>.</li>
          <li>Adjusted <em>AlternativeName:</em>
            <ul>
              <li><em>Lang</em> and <em>NameType</em> are now <b>required</b>.</li>
              <li>NameType &quot;other&quot; no longer valid value.</li>
              <li>Removed optional fields <em>TypeOfName, ShortName, QualifierName</em> and <em>Abbreviation.</em>
              </li>
            </ul>
          </li>
          <li>Added <em>OperatingPeriodRef</em> as a possible reference in <em>DayTypeAssignment</em>.</li>
          <li>Added <em>PrivateCode</em> as an optional field for <em>Equipment</em> in
            order to handle non-public ID&apos;s/codes.</li>
          <li>Adjusted translations for <em>TransportMode &quot;</em>cableway&quot; and
            &quot;funicular&quot;.</li>
          <li>Clarification of data format for language, language code, and currency.</li>
          <li>Added the <em>TransportMode</em> &quot;coach&quot; in order to separate
            long-distance buses from local-/regional buses.</li>
          <li>Added the <em>TransportMode</em> &quot;taxi&quot; (with TaxiSubmode)</li>
          <li>Added notices and <em>noticeAssignments</em> for <em>TimetableFrame</em>.</li>
          <li>Added <em>groupsOfStopPlaces</em> for <em>SiteFrame</em>.</li>
          <li>Added <em>versionRef</em> attribute which can be used for external objects
            in a specific version.</li>
          <li>Added optional <em>additionalNetworks</em> (which allows multiple Networks
            and subsequently multiple Authorities) for <em>SiteFrame</em>.</li>
          <li>Notices
            <ul>
              <li>Removed the field <em>TypeOfNoticeRef</em>.</li>
              <li>Made the field <em>Text</em> required (notice must have content).</li>
              <li>Made <em>PublicCode</em> optional.</li>
            </ul>
          </li>
        </ul>
        <p>stops:</p>
        <ul>
          <li>Replaced optional field <em>PlaceCode</em> with optional <em>PublicCode</em> for <em>Quay</em>.</li>
          <li>Added optional element <em>TransferDuration</em> for <em>PathLink</em>.</li>
          <li>Added optional element <em>ParkingVehicleType</em> for <em>Parking</em>.</li>
          <li>Changed all previously required data fields for Parking to optional.</li>
          <li>Removed redundant value <em>covered</em> for Parking &#x2192; ParkingLayout.
            The concept is instead modelled by defining Parking &#x2192; Covered as <em>covered</em> or <em>indoors</em> (general
            value for <em>SiteElement</em>)</li>
          <li>Added optional element <em>PublicUse</em> for objects of the type <em>SiteElement</em>.</li>
          <li>Added <em>PrivateCode</em> as an optional field for <em>Quay</em>.</li>
          <li>Clarification of data format for land- and area code.</li>
          <li>Added <em>GroupOfStopPlaces</em>.</li>
          <li>Added &quot;country&quot;, &quot;region&quot;, &quot;interregion&quot;
            and &quot;municipality&quot; as allowed values for <em>TopgraphicPlaceType</em>.</li>
        </ul>
        <p>network:</p>
        <ul>
          <li>Adjusted errors in organisation references for <em>Network</em>, related
            to <em>AuthorityRef</em>.</li>
          <li>Added required connection between <em>Line</em> and <em>Authority</em>.</li>
          <li>Clarification in <em>Presentation</em>, and removed redundant fields <em>ColourName</em> and <em>TextColourName</em>.</li>
          <li>Clarification for the minimum required <em>DestinationDisplayRef</em> for
            first <em>StopPointInJourneyPattern</em>, and all subsequent stops where <em>DestinationDisplay</em> changes.</li>
          <li>Removed redundant data type <em>Connection</em>.</li>
          <li>Changed <em>Name</em> to required element for <em>Network</em> and <em>GroupOfLines</em>.</li>
          <li>Adjusted data structure for <em>Interchange</em>.
            <ul>
              <li>Removed the redundant field for transfer time.</li>
              <li>Added field for <em>Planned</em> and <em>Advertised</em>.</li>
              <li>Added field for <em>MaximumWaitTime</em>.</li>
            </ul>
          </li>
          <li>Adjusted requirements for <em>StopAssignment</em> types to reflect technical
            schema validation.</li>
          <li>Changed <em>TransportSubmode</em> to required.</li>
          <li>Removed field <em>PublicCode</em> for <em>DestinationDisplay</em>.</li>
          <li>Removed <em>noticeAssignment</em> from <em>Line, StopPointInJourneyPattern</em> and <em>TimingPointInJourneyPattern</em>.
            Should be located with notices directly in <em>ServiceFrame</em>.</li>
          <li>Added optional field <em>RequestMethod</em> for <em>StopPointInJourneyPattern</em>.</li>
          <li>Added optional dataset <em>BookingArrangements</em> for <em>StopPointInJourneyPattern</em>.</li>
          <li>Added optional field felt <em>ExternalLineRef</em> for <em>Line</em>.</li>
        </ul>
        <p>timetable:</p>
        <ul>
          <li>Added optional fields <em>ArrivalDayOffset/DepartureDayOffset</em> for <em>TimetabledPassingTime</em>.</li>
          <li>Changed time-specification for arrival/departure to required. Cardinality
            for <em>PassingTimes</em> (per <em>VehicleJourney</em>/ServiceJourney) is
            specified according to this.</li>
          <li>Changed <em>TransportMode</em> and <em>TransportSubmode</em> to required.</li>
          <li>Clarified usage of calendar objects in a <em>ServiceCalendar</em> vs. free-standing.</li>
          <li>Changed fields <em>FromDate</em> and <em>ToDate</em> to required when using <em>ServiceCalendar</em>.</li>
          <li>Removed <em>noticeAssignment</em> fra <em>Journey</em> and <em>Interchange</em>.
            as it is more relevant to place notices directly under <em>TimetableFrame</em>.</li>
          <li>Added optional field <em>ExternalVehicleJourneyRef</em> for <em>Journey</em>.</li>
        </ul>
      </td>
      <td style="text-align:left">v1.1</td>
    </tr>
    <tr>
      <td style="text-align:left">15 Apr 2020</td>
      <td style="text-align:left"><a href>framework</a>,
        <br /><a href="handbok-n801-siri-netex-stops.md">stops</a>,
        <br /><a href="handbok-n801-siri-netex-network.md">network</a>,
        <br /><a href="handbok-n801-siri-netex-timetable.md">timetable</a>
      </td>
      <td style="text-align:left"><em>Initial export (appendix H&#xE5;ndbok N801)</em>
      </td>
      <td style="text-align:left">v1.0</td>
    </tr>
  </tbody>
</table>

