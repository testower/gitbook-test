# Håndbok N801 \(SIRI/NeTEX\) : SIRI Profile Documents

* [SIRI-ET](handbok-n801-siri-netex-siri-et.md)
* [SIRI-SX](handbok-n801-siri-netex-siri-sx.md)
* [SIRI-VM](handbok-n801-siri-netex-siri-vm.md)

## Changelog <a id="SIRIProfileDocuments-Changelog"></a>

<table>
  <thead>
    <tr>
      <th style="text-align:left">Date of change</th>
      <th style="text-align:left">Profile document</th>
      <th style="text-align:left">Description of change</th>
      <th style="text-align:left">Version</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">03 Feb 2021</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-general-information-siri.md">General information SIRI</a>,
        <br
        /><a href="handbok-n801-siri-netex-siri-et.md">SIRI-ET</a>,
        <br /><a href="handbok-n801-siri-netex-siri-sx.md">SIRI-SX</a>,
        <br /><a href="handbok-n801-siri-netex-siri-vm.md">SIRI-VM</a>
      </td>
      <td style="text-align:left">
        <p>General information:</p>
        <ul>
          <li>Allow three-letter ISO 639-3 language codes</li>
          <li>General requirements:
            <ul>
              <li>Minor restructuring and clarification</li>
              <li>Added paragraphs &quot;Data correctness&quot; and &quot;Data completeness&quot;
                with (further) examples on irrelevant data not to be published in production
                ET/SX/VM</li>
            </ul>
          </li>
        </ul>
        <p>SIRI-ET</p>
        <ul>
          <li>Added optional element PublishedLineName in EstimatedVehicleJourney</li>
          <li>Added optional element Occupancy in EstimatedCall</li>
          <li>Added Occupancy enumerations &quot;unknown&quot;, &quot;manySeatsAvailable&quot;
            and &quot;notAcceptingPassengers&quot; with usage guidance (per EstimatedVehicleJourney
            and per EstimatedCall)</li>
          <li>Added ArrivalStatus / DepartureStatus &quot;missed&quot; for calls missing
            arrival/departure time</li>
          <li>Made ActualArrivalTime / ActualDepartureTime non-mandatory for calls missing
            arrival/departure time</li>
          <li>Added ExpectedArrivalTime / ExpectedDepartureTime for RecordedCall when
            ActualArrivalTime / ActualDepartureTime is missing</li>
        </ul>
        <p>SIRI-SX</p>
        <ul>
          <li>Added Severity (of incident) enumerations &quot;verySlight&quot; and &quot;verySevere&quot;
            as allowed values</li>
          <li>Affects must have minimum <em>one</em> object (unless Progress=&quot;closed&quot;)</li>
          <li>Allowed for no Summary element (0: *) <em>when the situation no longer affect public transport</em> (Progress=&quot;closed&quot;)</li>
          <li>Specify Priority as a number between 1 (highest priority) and 10 (lowest
            priority) for messages where urgency is relevant</li>
          <li>Added DatedVehicleJourneyRef as optional AffectedVehicleJourney element</li>
        </ul>
        <p>SIRI-VM</p>
        <ul>
          <li>Aligning descriptions of ProgressBetweenStops, MonitoredCall and MonitoredCallStructure
            with the SIRI spec and usage consensus</li>
          <li>Added Occupancy enumerations &quot;unknown&quot;, &quot;manySeatsAvailable&quot;
            and &quot;notAcceptingPassengers&quot; with usage guidance</li>
          <li>Added VehicleRef as required element for the MonitoredVehicleJourney</li>
        </ul>
      </td>
      <td style="text-align:left">v. 1.1</td>
    </tr>
    <tr>
      <td style="text-align:left">01 May 2019</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-siri-et.md">SIRI-ET</a>
        <br /><a href="handbok-n801-siri-netex-siri-sx.md">SIRI-SX</a>
        <br /><a href="handbok-n801-siri-netex-siri-vm.md">SIRI-VM</a>
      </td>
      <td style="text-align:left">The profile is now official and version is changed 1.0 without any changes
        to the content.</td>
      <td style="text-align:left">v. 1.0</td>
    </tr>
    <tr>
      <td style="text-align:left">22 Aug 2018</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-siri-et.md">SIRI-ET</a>
        <br /><a href="handbok-n801-siri-netex-siri-sx.md">SIRI-SX</a>
        <br /><a href="handbok-n801-siri-netex-siri-vm.md">SIRI-VM</a>
      </td>
      <td style="text-align:left">Corrections and clarifications of data structure and message contents.</td>
      <td
      style="text-align:left">v. 0.9.2
        <br />v. 0.9.2
        <br />v. 0.9.2</td>
    </tr>
    <tr>
      <td style="text-align:left">02 Mar 2018</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-general-information-siri.md">General information SIRI</a>,
        <br
        /><a href="handbok-n801-siri-netex-siri-et.md">SIRI-ET</a>,
        <br /><a href="handbok-n801-siri-netex-siri-sx.md">SIRI-SX</a>,
        <br /><a href="handbok-n801-siri-netex-siri-vm.md">SIRI-VM</a>
      </td>
      <td style="text-align:left"><em>Initial publication of Norwegian SIRI profile.</em>
      </td>
      <td style="text-align:left">v. 0.9</td>
    </tr>
  </tbody>
</table>

