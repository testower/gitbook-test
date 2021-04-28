# Håndbok N801 \(SIRI/NeTEX\) : NeTEx examples catalogue

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591706110 {padding: 0px;}  
div.rbtoc1619591706110 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591706110 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Message Format](handbok-n801-siri-netex-netex-examples-catalogue.md#NeTExexamplescatalogue-MessageFormat)
* [Examples](handbok-n801-siri-netex-netex-examples-catalogue.md#NeTExexamplescatalogue-Examples)
  * [Example-repository](handbok-n801-siri-netex-netex-examples-catalogue.md#NeTExexamplescatalogue-Example-repository)
  * [PublicationDelivery](handbok-n801-siri-netex-netex-examples-catalogue.md#NeTExexamplescatalogue-PublicationDelivery)
  * [Dataset](handbok-n801-siri-netex-netex-examples-catalogue.md#NeTExexamplescatalogue-Dataset)
  * [Creating new examples](handbok-n801-siri-netex-netex-examples-catalogue.md#NeTExexamplescatalogue-Creatingnewexamples)
    * [Tools](handbok-n801-siri-netex-netex-examples-catalogue.md#NeTExexamplescatalogue-Tools)

## Message Format <a id="NeTExexamplescatalogue-MessageFormat"></a>

All datasets should be XML files with the root node "`PublicationDelivery`" \(see [description of the exchange format](https://enturas.atlassian.net/wiki/spaces/ROR/pages/728563782/General+information+NeTEx#Generalinformation:NeTEx-Utvekslingavinformasjon)\), which is the message format defined in NeTEx to contain relevant [components]().

## Examples <a id="NeTExexamplescatalogue-Examples"></a>

The following examples are simplified snippets of semi-fictitious data to illustrate how the components and their contents should be modelled.

### Example-repository <a id="NeTExexamplescatalogue-Example-repository"></a>

Entur has an official repository at **GitHub**, which contains XML-files for all our examples below: [https://github.com/entur/profile-norway-examples/tree/master/netex](https://github.com/entur/profile-norway-examples/tree/master/netex)

The catalogue is intended to cover the most common use cases, but we welcome any ideas for creating additional examples.

### PublicationDelivery <a id="NeTExexamplescatalogue-PublicationDelivery"></a>

* **Skeleton** \(can be used as a template for datasets\)
  * \[[XML-document at GitHub](https://github.com/entur/profile-norway-examples/blob/master/netex/frames/publicationDelivery.xml)\]
* **Complete delivery** \(contains all relevant elements for datasets\)
  * \[[XML-document at GitHub](https://github.com/entur/profile-norway-examples/blob/master/netex/Full_PublicationDelivery_109_Oslo_morningbus_example.xml)\]

### Dataset <a id="NeTExexamplescatalogue-Dataset"></a>

_All the various example categories are described on individual pages with a detailed description of file structure and data content, as well as links to the corresponding XML file on GitHub._

<table>
  <thead>
    <tr>
      <th style="text-align:left">Sample</th>
      <th style="text-align:left">Profile</th>
      <th style="text-align:left">XML</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Comments</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-simple-rhythm-based-bus-line.md">Simple route - Bus with rhythm-based departures</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/network/Line61A.xml">GitHub</a>
      </td>
      <td style="text-align:left">Line 61A, Oslo:
        <br />Circular feeder route at Tveita. Operates every day except Sunday.</td>
      <td
      style="text-align:left"><em>See <b>TimetableFrame</b></em>  <em>(the file contains a full dataset for network and service)</em>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-simple-bus-line.md">Simple route - Bus with explicit ServiceJourney(s)</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/Full_PublicationDelivery_109_Oslo_morningbus_example.xml">GitHub</a>
      </td>
      <td style="text-align:left">Line 109, Oslo:
        <br />Morning bus route with three departures (times differ between weekdays,
        Saturdays and Sundays).</td>
      <td style="text-align:left"><em>See <b>TimetableFrame</b></em>  <em>(the file also contains geographical projections and a full dataset for Network, Service and Timetable.) </em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-simple-bus-line.md">Simple route - Bus</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/Full_PublicationDelivery_109_Oslo_morningbus_example.xml">GitHub</a>
      </td>
      <td style="text-align:left">Line 109, Oslo:
        <br />Morning bus route between Helsfyr T and Holtet. Operates every day except
        Sunday.</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-simple-route-bus-with-pre-booked-stops.md">Simple route - Bus with pre-booked stops</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/network/BookingArrangements.xml">GitHub</a>
      </td>
      <td style="text-align:left">Express bus S&#xF8;rlandsekspressen. Some stops are on-demand only: passengers
        must book in advance for the bus to stop.</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-on-demand-transport.md">On-demand transport</a> (FlexibleLines)</td>
      <td
      style="text-align:left"><b>network/timetable</b>
        </td>
        <td style="text-align:left">
          <ol>
            <li><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-316-with-interchange.xml">GitHub</a>
            </li>
            <li><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-within-single-FlexibleArea.xml">GitHub</a>
            </li>
            <li><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/network/Hail-and-ride-Ruter-507.xml">GitHub</a>
            </li>
          </ol>
        </td>
        <td style="text-align:left">
          <ol>
            <li>Line 316, L&#xF8;renskog: On-demand transport on weekdays.</li>
            <li>On-demand transport without a predefined journey pattern within a defined
              area.</li>
            <li>Line 507, Dr&#xF8;bak: A scheduled route which allows alighting and boarding
              outside the fixed stop places along segments of a journey (Hail &amp; Ride).</li>
          </ol>
        </td>
        <td style="text-align:left"><em>Linje 316 contains examples of Interchange</em>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-multimodal-interchanges.md">Multimodal interchange</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/network/FlexibleLine-316-with-interchange.xml">GitHub</a>
      </td>
      <td style="text-align:left">On-demand transport line which links up with train- and bus lines at a
        specific stop.</td>
      <td style="text-align:left"><em>Modelled as on-demand transport with planned interchanges for train and bus. </em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-projection.md">Projection</a> (geographical
        positions)</td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/Full_PublicationDelivery_109_Oslo_morningbus_example.xml">GitHub</a>
      </td>
      <td style="text-align:left"><a href>Projection </a>(for Line 109, Oslo):
        <br />Specification of journey pattern through positional data</td>
      <td style="text-align:left"><em>See <b>serviceLinks</b></em>  <em>in <b>ServiceFrame</b></em>  <em>(the file contains a full dataset for network and service.)</em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-calendar.md">Calendar</a> (ServiceCalendar
        with dayTypes)</td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/schedule/ServiceCalendar-example.xml">GitHub</a>
      </td>
      <td style="text-align:left">Theoretical example showing how to use different calendar types.</td>
      <td
      style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-branding.md">Branding</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-Branding.xml">GitHub</a>
      </td>
      <td style="text-align:left">Show custom company information (overriding Authority/Operator).</td>
      <td
      style="text-align:left"><em>Also, see Authorities (below)</em>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-multiple-authorities.md">Authorities</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/submodels/submodel-additionalNetworks.xml">GitHub</a>
      </td>
      <td style="text-align:left">Description of multiple Authorities in the same data set.</td>
      <td style="text-align:left"><em>Used when submitting data for a service provider different from your own (on behalf of), also see Branding. </em>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stopplace-minimalistic.md">Stop place with a minimum of required information</a>
      </td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stops.md"><b>stops</b></a>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/stops/BasicStopPlace_example.xml">GitHub</a>
      </td>
      <td style="text-align:left">Blystadlia, R&#xE6;lingen.
        <br />Monomodal stop place for bus with one Quay.</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stopplace-simple.md">Normal stop place for bus</a>
      </td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stops.md"><b>stops</b></a>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/stops/BasicStopPlace-two-quays_example.xml">GitHub</a>
      </td>
      <td style="text-align:left">&quot;Bryn skole&quot;:
        <br />Monomodal stop place for bus with one Quay in each direction.</td>
      <td
      style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stopplace-complex.md">Complex stop area </a> (multiple
        transport types)</td>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-stops.md"><b>stops</b></a>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/stops/OsloS_station_example.xml">GitHub</a>
      </td>
      <td style="text-align:left">Oslo S - Jernbanetorget:
        <br />Stop place area which with several multi- and monomodal stop places.</td>
      <td
      style="text-align:left"><em>Contains deviations from actual implementation in live solutions. The examples here will be adjusted when a revised implementation is ready for publication.</em>
        </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="handbok-n801-siri-netex-tariff-codes.md">Tariff code</a>
      </td>
      <td style="text-align:left"><b>network/timetable</b>
      </td>
      <td style="text-align:left"><a href="https://github.com/entur/profile-norway-examples/blob/master/netex/fares/tariff-code.xml">GitHub</a>
      </td>
      <td style="text-align:left">Specification of TariffZone per Line and/or departure.</td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

**fares** examples will be added at a later time.

### Creating new examples <a id="NeTExexamplescatalogue-Creatingnewexamples"></a>

If you want to expand the samples or add new ones in GitHub, eg. the need for modelling special cases not already covered follow these guidelines. 

1. Create a [_fork_](https://help.github.com/articles/fork-a-repo/) \(your local copy\) of [**the catalogue**](https://github.com/entur/profile-norway-examples).
2. Create a [_branch_](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/) \(your local branch of the code\) and make your changes to the code there.
3. Test all changes/new files. \(_XML-documents_ _**must** validate against the NeTEx official Schema, see_ [_https://github.com/NeTEx-CEN/NeTEx_](https://github.com/NeTEx-CEN/NeTEx) _for the last version of XSD's._\)
4. Make a [_pull request_](https://help.github.com/articles/creating-a-pull-request/) into the repository to "save" the changes.

Further information about the use of **pull request** in GitHub is located at [https://help.github.com/articles/using-pull-requests/](https://help.github.com/articles/using-pull-requests/).

#### Tools <a id="NeTExexamplescatalogue-Tools"></a>

It is recommended to use tools which support automatic validation of the data structure while working with XML files, eg.  [Notepad++](https://notepad-plus-plus.org/download/) with XML Tools plugin \(free, the XML-plugin could be [installed automatically in Notepad++](http://ccm.net/faq/32347-notepad-how-to-install-plugins) or downloaded [separate](https://sourceforge.net/projects/npp-plugins/files/XML%20Tools/)\) or licensed tools like [Oxygen](http://oxygenxml.com/) or [XMLspy](http://www.altova.com/xmlspy.html).

