# Håndbok N801 \(SIRI/NeTEX\) : SIRI Examples Catalogue

This page contains examples and descriptions of best-practice for how to structure data in the SIRI format in accordance with the [Norwegian SIRI profile](handbok-n801-siri-netex-norwegian-siri-profile.md). The catalogue is openly available and is meant to cover the most common use cases. Suggestions for additional examples to the catalogue are welcome.

## Content <a id="SIRIExamplesCatalogue-Content"></a>

/\*&lt;!\[CDATA\[\*/  
div.rbtoc1619591773586 {padding: 0px;}  
div.rbtoc1619591773586 ul {list-style: disc;margin-left: 0px;}  
div.rbtoc1619591773586 li {margin-left: 0px;padding-left: 0px;}  
  
/\*\]\]&gt;\*/

* [Content](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-Content)
* [Message format](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-Messageformat)
  * [GitHub repository](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-GitHubrepository)
  * [Service Delivery](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-ServiceDelivery)
  * [Dataset](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-Dataset)
    * [SIRI-ET](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-SIRI-ET)
    * [SIRI-SX](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-SIRI-SX)
    * [SIRI-VM](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-SIRI-VM)
  * [Creating new examples](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-Creatingnewexamples)
    * [Tools](handbok-n801-siri-netex-siri-examples-catalogue.md#SIRIExamplesCatalogue-Tools)

## Message format <a id="SIRIExamplesCatalogue-Messageformat"></a>

All real-time datasets must be in one of the three supported formats \([SIRI-ET](handbok-n801-siri-netex-siri-et.md), [SIRI-SX](handbok-n801-siri-netex-siri-sx.md), [SIRI-VM](handbok-n801-siri-netex-siri-vm.md)\), and sent as a single XML-file \(per format\) with the root node "`ServiceDelivery`". 

### GitHub repository <a id="SIRIExamplesCatalogue-GitHubrepository"></a>

The XML examples can all be found on GitHub at [https://github.com/entur/profile-norway-examples/tree/master/siri](https://github.com/entur/profile-norway-examples/tree/master/siri)

### Service Delivery <a id="SIRIExamplesCatalogue-ServiceDelivery"></a>

* **Skeleton** \(can be used as a starting point to generate the XML data\)
  * [Estimated Timetable \(SIRI-ET\)](https://github.com/entur/profile-norway-examples/blob/master/siri/delivery/siri-et-outline.xml)
  * [Situation Exchange \(SIRI-SX\)](https://github.com/entur/profile-norway-examples/blob/master/siri/delivery/siri-sx-outline.xml)
  * [Vehicle Monitoring \(SIRI-VM\)](https://github.com/entur/profile-norway-examples/blob/master/siri/delivery/siri-vm-outline.xml)
* **Complete dataset** \(contains all relevant elements for a complete dataset\)
  * \[_Not yet available_\]

### Dataset <a id="SIRIExamplesCatalogue-Dataset"></a>

_All examples are linked to XML-files in GitHub. Some examples have been more extensively described on a separate page._

#### SIRI-ET <a id="SIRIExamplesCatalogue-SIRI-ET"></a>

| Eksempel | XML | Beskrivelse | Kommentar |
| :--- | :--- | :--- | :--- |
| Vehicle before departure | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-vehicle-before-departure.xml) | Real-time data for a departure. |  |
| Partial cancellation \(last leg\) | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-last-stops.xml) \(_before departure_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-last-stops-after-departure.xml) \(_underway_\) | [_See own document_](handbok-n801-siri-netex-siri-et-cancelled-before-departure.md) | Examples of real-time data **before departure**, and real-time data **underway**. |
| Partial cancellation \(first leg\) | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-partial-cancellation-first-stops.xml) | [_See own document_](handbok-n801-siri-netex-siri-et-partial-cancellation-first-leg.md) | Example of cancellation **after** departing. |
| Cancelled in the middle of the route before departure | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-cancellation-of-stop-before-departure.xml) | [_See own document_](handbok-n801-siri-netex-siri-et-cancelled-in-the-middle-of-the-route-before-departure.md) |  |
| Cancelled before departure | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-cancellation-before-departure.xml) | Real-time data for a cancelled departure |  |
| Replacement departure | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-extra-journey-1.xml) \(_before departure_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-extra-journey-2.xml) \(_underway_\) |  | Examples of real-time data **before departure**, and real-time data **underway**. |
| Changed platform | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-quay-change-1.xml) \(_before change_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/estimated-timetable/siri-et-quay-change-2.xml) \(_after change_\) | [_See own document_](handbok-n801-siri-netex-siri-et-changed-platform.md) |  |

#### SIRI-SX <a id="SIRIExamplesCatalogue-SIRI-SX"></a>

| Eksempel | XML | Beskrivelse | Kommentar |
| :--- | :--- | :--- | :--- |
| Message on a Line | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-for-line.xml) | [_See own document_](handbok-n801-siri-netex-siri-sx-message-on-a-line.md) |  |
| Message on a leg for multiple Vehicles | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-multiple-vehicles.xml) | [_See own document_](handbok-n801-siri-netex-siri-sx-message-on-a-leg-melding-pa-en-strekning-for-flere-kjoretoy.md) |  |
| Message on a Network | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-for-network.xml) | Applies to all departures \(Vehicles\) in a Network |  |
| Message on a Stop | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-for-stop.xml) | [_See own document_](handbok-n801-siri-netex-siri-sx-message-on-a-single-stop.md) |  |
| Message on a Stop for specific Lines | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-for-stop-by-specific-lines.xml) | [_See own document_](handbok-n801-siri-netex-siri-sx-message-on-a-stop-for-specific-lines.md) |  |
| Message with stopCondition on a Vehicle | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-alight-board-specific-stop-and-vehicle.xml) \(_boarding/alighting_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-boarding-specific-stop-and-vehicle.xml) \(_boarding_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-passing-specific-stop-and-vehicle.xml) \(_passing_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-alight-board-passing-stops.xml) \(_board./alight./pass._\) | [_See own document_](handbok-n801-siri-netex-siri-sx-message-with-stopcondition-on-a-vehicle.md) |  |
| Message on a Vehicle | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-one-vehicle-1.xml) \(_alternative 1_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-one-vehicle-2.xml) \(_alternative 2_\) | [_See own document_](handbok-n801-siri-netex-siri-sx-message-on-a-vehicle.md) |  |
| Message on multiple Vehicles and multiple Dates | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-multiple-vehicles-multiple-dates.xml) | [_See own document_](handbok-n801-siri-netex-siri-sx-message-on-multiple-vehicles-on-multiple-dates.md) |  |
| Validity of a message | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-timebound.xml) \(_set validity time_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-open-ended.xml) \(_open_\) [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/situation-exchange/siri-sx-close.xml) \(_closing_\) | [_See own document_](handbok-n801-siri-netex-siri-sx-validity-of-a-message.md) |  |

#### SIRI-VM <a id="SIRIExamplesCatalogue-SIRI-VM"></a>

| Eksempel | XML | Beskrivelse | Kommentar |
| :--- | :--- | :--- | :--- |
| Message on a Vehicle before arriving the next Stop | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/vehicle-monitoring/siri-vm-before-stop.xml) | A vehicle underway to monitored stop |  |
| Message on a Vehicle while serving a Stop | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/vehicle-monitoring/siri-vm-at-stop.xml) | A vehicle which has stopped at a monitored stop |  |
| Message with the coordinates of a Vehicle | [GitHub](https://github.com/entur/profile-norway-examples/blob/master/siri/vehicle-monitoring/siri-vm-minimum.xml) |  | Minimum-example with position, but does not indicate the progress of the trip |

### Creating new examples <a id="SIRIExamplesCatalogue-Creatingnewexamples"></a>

If you want to expand the samples or add new ones in GitHub, eg. the need for modelling special cases not already covered follow these guidelines. 

1. Create a [_fork_](https://help.github.com/articles/fork-a-repo/) \(your local copy\) of [**the catalogue**](https://github.com/entur/profile-norway-examples).
2. Create a [_branch_](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/) \(your local branch of the code\) and make your changes to the code there.
3. Test all changes/new files. \(_XML-documents **must** validate against the NeTEx official Schema, see_ [_https://www.vdv.de/siri.aspx_](https://www.vdv.de/siri.aspx) for the last version of XSD's.\)
4. Make a [_pull request_](https://help.github.com/articles/creating-a-pull-request/) into the repository to "save" the changes.

Further information about the use of **pull request** in GitHub is located at [https://help.github.com/articles/using-pull-requests/](https://help.github.com/articles/using-pull-requests/).

#### Tools <a id="SIRIExamplesCatalogue-Tools"></a>

It is recommended to use tools which support automatic validation of the data structure while working with XML files, eg.  [Notepad++](https://notepad-plus-plus.org/download/) with XML Tools plugin \(free, the XML-plugin could be [installed automatically in Notepad++](http://ccm.net/faq/32347-notepad-how-to-install-plugins) or downloaded [separate](https://sourceforge.net/projects/npp-plugins/files/XML%20Tools/)\) or licensed tools like [Oxygen](http://oxygenxml.com/) or [XMLspy](http://www.altova.com/xmlspy.html).

