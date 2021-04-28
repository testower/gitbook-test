# Håndbok N801 \(SIRI/NeTEX\) : Norwegian submodes and their definitions

  
**An appendix to the Norwegian NeTEx Profile** 

Last changed 17 Feb 2021 and **valid for Norwegian NeTEx Profile v. 1.3.**

## Preface <a id="Norwegiansubmodesandtheirdefinitions-Preface"></a>

This document is meant to provide a plain text translation of each transport mode used in the Norwegian NeTEx Profile in order to avoid misunderstandings and incorrect use of the modes when creating timetable data. For this reason, this document is bi-lingual.

## Background <a id="Norwegiansubmodesandtheirdefinitions-Background"></a>

NeTEx has a limited set of transport modes which do not always correspond directly to modes typically and historically used in Norway. This document specifies which transport types to use for each case, and which to use in cases where NeTEx is insufficiently precise. The document lists all modes grouped by their basic types and begins by specifying the NeTEx/Transmodel transport mode. A Norwegian name, a definition and an example followed by an English summary of the same follows.

The selection of modes to be used in Norway follows the mantra: "as few as possible - but everything we need". In the selection process, several potential modes were selected against because of their overly specific nature which would counter the actual use case. The specific mode for cable ferry was one such case since the ferry, while indeed being pulled by a cable, does not perform a different role from motorised ferries. In other cases, it was necessary to use the available modes from Transmodel to allow separation of the modes that Norwegian traffic required. This was the case for rail transport and the cases of Bybanen and Hurtigruten.

## List of valid submodes and their definitions <a id="Norwegiansubmodesandtheirdefinitions-Listofvalidsubmodesandtheirdefinitions"></a>

| Transmodel/NeTEx submode | Norwegian name | Norwegian definition | Norwegian example | _English summary_ | GTFS mode mapping\* |
| :--- | :--- | :--- | :--- | :--- | :--- |
|  |  |  |  |  |  |
| localBus | Lokalbuss | En buss som opererer innenfor et område tilsvarende en større kommune. Det er ikke forskjell på en lokalbuss som kjører i ett tett stoppemønster eller i en ekspresstrasé. Når/hvis cityBus blir lagt til i NeTEx-standarden må disse skilles ut fra localBus. | Bybusser, kortdistanseruter, åpne skoleruter \(hvis ikke schoolBus brukes\). | _Any short-range bus routes, city buses, or open school lines which are not distinctly marked with the school bus mode._ | 704 |
| regionalBus | Regional bussrute | En rute som knytter sammen de områder som betjenes av lokalbussene. Alternative norske betegnelser er «langruter» eller «gjennomgående ruter». Denne typen skal skilles fra kommersiell ekspressbusstrafikk \(se nationalCoach/internationalCoach\) og ekspresstjenester i lokale tilbud \(se expressBus\). |  | _Any medium range buses which are not localBus, express bus, airport link bus, or a coach._ | 701 |
| expressBus | Ekspressrute | En valgfri variant av regionsbusser \(regionalBus\) som betjener _færre_ stopp enn den vanlige regionsbussen. Skal ikke erstatte localBus. Må ikke forveksles med nationalCoach/internationalCoach. |  | _A regional bus serving fewer stops than its regionalBus counterpart \(express departure\). Not to be confused with coach services._ | 702 |
| nightBus | Nattbuss | En variant av lokalbuss, typisk en by- eller lokalbuss som kjører som dedikert nattavgang, ofte med eget rutenummer. Dette omfatter _ikke_ ruter som kjører over midnatt eller ekspressbussruter som kjører nattavgang. | N54 – Oslobuss 54 kjøres på natten som rute N54. | _A local bus operating exclusively and specifically at night \(usually midnight-5:00\)._ | 705 |
| sightseeingBus | Turistbuss | En buss rettet mot turisme og opplevelser. Har ofte lengre opphold på stoppesteder eller kjører saktere. Bør brukes kun ved spesielt behov for å identifisere dette. Inkluderer veteranbussruter. | Krøderbanen har en "buss for tog"-løsning som kjøres med veteranbuss. | _A bus focusing primarily on the experience \(tourism\) of the journey instead of efficiency and speed._ | 710 |
| shuttleBus | Shuttlebuss | En mindre bussrute som brukes i syfte å «mate» andre tilbud. Hyppige avganger eller korrespondanse er typisk. Kjørere vanligvis innen et sterkt begrenset område og få stoppesteder. | Shuttlebussens fra Torp stasjon til Sandefjord lufthavn eller shuttlebussene fra hotellene på Gardermoen til OSL. | _A local bus which acts only as a feeder route to other transports. Usually connecting to coaches, trains or airports._ | 711 |
| schoolBus | Skolerute | En valgfri variant av lokalbuss. En rute primært rettet mot skoleelever men i praksis _åpen_ _for publikum_. | Rute for skolebarn fra og til skoler som typisk ikke kjører på skolens fridager. | _A local bus specifically transporting students from their homes to their schools, but which may be used by the general public._ | 713 |
| railReplacementBus | Erstatningsbuss | En buss som midlertidig erstatter en togrute. Kan også benyttes på avvik i t-banens eller trikkens avvik. | Buss for tog. | _A temporary bus service replacing a temporarily disabled rail line._ | 714 |
| airportLinkBus | Flybuss | En bussrute knyttet til en flyplass med begrensninger for av- og påstigning som forhindrer at bussen konkurrerer med lokal-, region-, og ekspressbusser. |  | _A bus route specifically aimed at transporting passengers to and from airports. Usually with special board/alight-rules on the intermediary stops._ | 711 |
| internationalCoach | Internasjonal ekspressbuss | En ekspressbuss \(se nationalCoach\) som passerer en internasjonal grense. En reise som kan innebære grensekontroll eller regler for medført bagasje. | Rutene mellom Oslo og Göteborg eller Stockholm. | _A long-distance coach service which crosses an international border._ | 201 |
| nationalCoach | Ekspressbuss | En buss tilpasset langreiser \(f.eks. toalett, bagasje, komfort\) som kjører lengre strekninger, typisk fylkeskryssende. Har ofte regler for av- og påstigning på lokale strekninger. | NOR-WAY Bussekspress, Vy express, Lavprisekspressen | _A long-distance coach service which does not cross an international border._ | 202 |
| - | Minibuss | Rute som kjøres med minibuss. Passasjerer varsles at transporten de venter på ikke er en fullstørrelse-buss da det ofte kreves at passasjerer varlser sjåfør visuelt dersom de ønsker bli med på turen. Disse har også redusert sete- og bagasje-kapasitet. **Bruk localBus**. |  | _A distinct vehicle type. **Use localBus**._ | 704 |
| - | Maxitaxi | Rute som kjøres av en taxibil med minibuss. |  | _A distinct taxi vehicle type. **Use localBus**._ | 704 |
| - | Bybuss | Busser med lavt gulv som typisk trafikkerer sentrale deler av en by. Skilles fra lokalbussen ved gulvtype. **Bruk localBus**. |  | _Low floor buses typically used in inner-city traffic. **Use localBus**._ | 704 |
| - |  | Lokal- eller regionsbusser som krysser en internasjonal grense og kan innebære grensekontroll eller regler for medført bagasje. **Bruk localBus eller regionalBus**. | 575 Kongsvinger-Charlottenberg, 111 Halden-Svinesund-Strömstad | _A distinct mode of journey where a local- or regional route crosses an international border. **Use localBus or regionalBus**._ | 704 |
|  |  |  |  |  |  |
| localTram | Sporvogn eller Trikk | Skinnegående trafikk i bymiljø som deler veinett med andre typer kjøretøy. Unntak for Bybanen. | Trikken i Oslo og Gråkallbanen i Trondheim. | _A tram service as can be found in Oslo and Trondheim._ | 902 |
| cityTram | Bybane | Spesifikt Bybanen i Bergen. | Bybanen | _Due to the particular nature of the "Bybanen" concept in the city of Bergen this particular submode has been defined as Bybanen._ | 901 |
| metro | T-bane eller Metro | Tyngre skinnegående trafikk som ikke deler veinett med andre kjøretøy. Er ikke et tog, eller en sporvogn. | T-banen i Oslo | _A metro \(subway\) service as can be found in Oslo._ | 401 |
| _The rail modes were defined to correspond as closely as possible to the needs and usage of NSB in 2016._ |  |  |  |  |  |
| local | Lokaltog \(LT\) | Lokaltog som betjener dagpendlere i storbyregioner eller andre kortere togruter. |  | _Local train services for commuters and suburban transport._ | 109 |
| regionalRail | Regiontog \(RT\) | Togruter klassifisert mellom lokaltog og Intercity med elektrisk drift. NSB har skilt elektriske fra diesel-drevne togruter. Derfor deler vi også på dem inntil videre. |  | _Electrical trains which are not local- or intercity trains._ | 103 |
| interregionalRail | Regiontog \(DT\) | Togruter klassifisert mellom lokaltog og Intercity med dieseldrift. Disse er ofte ganske lange ruter. Derfor passer DT som interregional. |  | _Diesel-trains which are not local- or intercity trains._ | 103 |
| longDistance | Intercity \(IC\) | De lengste togrutene i Norge definert som IC fra NSB. |  | _Intercity trains._ | 102 |
| international | Internasjonalt tog | Et tog som passerer en landsgrense og kan innebære grensekontroll eller regler for medført bagasje. |  | _Trains which cross an international border._ | 100 |
| touristRailway | Museumstog | Bevarte eller restaurerte jernbanenett med utdatert teknologi og primært eksisterer som turistattraksjon. | Krøderbanen, Tertitten | _A train focusing primarily on the experience \(tourism\) of the journey instead of efficiency and speed. Usually outdated train models, sometimes on different gauge rails._ | 107 |
| nightRail | Nattog \(NT\) | Rute med spesielt fokus på overnatting under reisens gang. |  | _Train services with a particular focus on overnight journeys with sleeping compartments._ | 105 |
| airportLinkRail | Flytog | Rute med spesielle regler som bringer passasjerer til og fra flyplasser. | Flytoget | _Airport express trains._ | 108 |
|  |  |  |  |  |  |
| internationalCarFerry | Internasjonal bilferje | Bilførende fartøy som anløper utenlandske havner. | Color Line-rutene til Danmark. | _Car-carrying cruise ships between Norway and Germany/Denmark._ | 1001 |
| nationalCarFerry | Kystruten | På grunn av norske forhold innenfor bilferjetrafikken skilles kystruten ut som en egen transporttype da den uansett er en utpreget form av transport. | Hurtigruten, Havila | _Specifically assigned to the coastal route, Bergen-Kirkenes._ | 1002 |
| localCarFerry | Innenriks bilferje | Fartøy som transporterer kjøretøy mellom eller i veinett innenfor Norges grenser. Fartøyets kapasitet er uvesentlig. Inkluderer ikke hurtigbåter med bilførende kapasitet \(se highSpeedVehicleService\). |  | _Car carrying ferries, as part of road networks or disconnected locations inside Norway. Does not include high speed services._ | 1004 |
| internationalPassengerFerry | Internasjonal passasjererbåt | Båtrute uten kapasitet for biler som anløper utenlandske havner. Denne vil gjelde ytterst få ruter, men beholdes for å skille utenriks- fra innenriks-ruter. | M/S Sagasund | _Ships to international destinations which do not carry cars._ | 1005 |
| localPassengerFerry | Innenriks passasjererbåt | Båt uten kapasitet for biler, som ikke er hurtigbåt, med anløp til havner innenfor Norges grenser. | Bygdøyferga, Gripruta | _Boat services which are not: international, car carrying, or high-speed services._ | 1008 |
| sightseeingService | Turistbåtrute | Båter fremst rettede mot turisme, uansett kapasitet. | Skibladner, Fæmund, Seasight | _A boat service focusing primarily on the experience \(tourism\) of the journey instead of efficiency and speed. Usually older ships._ | 1016 |
| highSpeedVehicleService | Kombibåt eller bilførende hurtigbåt | Hurtigbåt med kapasitet for biler som anløper havner innenfor norges grenser. | Katamaraner som kan ta med biler og personer. | _A high-speed boat service with car carrying capacity. The ship type is usually a catamaran._ | 1014 |
| highSpeedPassengerService | Hurtigbåt | Hurtigbåt uten kapasitet for biler som anløper havner innenfor norges grenser. Norsk definisjon av hurtigbåt er at den er hurtig, og ikke langsom. Vanligvis katamaran. | Katamaraner som kan ta med personer, men ikke biler. | _A high-speed boat service which does not carry cars. The ship type is usually a catamaran._ | 1015 |
|  |  |  |  |  |  |
| internationalFlight | Internasjonal flyrute | Flyrute til et annet land. | Fly Oslo-London | _An aeroplane service to an international destination._ | 1102 |
| domesticFlight | Innenriks flyrute | Flyrute innenfor norges grenser. | Fly Trondheim-Bergen | _An aeroplane service to a domestic destination._ | 1103 |
| helicopterService | Helikopterrute | Flyrute som utføres med helikopter. | Mellom Værø og Bodø | _A helicopter service._ | 1110 |
|  |  |  |  |  |  |
| telecabin | Taubane | Passasjererkabin som henger fra et tau. | Ulriken | _A passenger cabin suspended on a cable._ | 1300 |
| funicular | Bergbane | Et skinnegående kjøretøy som traverserer bratte skrenter ved å dra kjøretøyet med kabler. | Fløibanen | _A passenger-carrying service which uses a pulling system to scale steep inclines._ | 1400 |

\* [TPEG-derived list of route\_type suggestions](https://groups.google.com/g/gtfs-changes/c/keT5rTPS7Y0/m/71uMz2l6ke0J?pli=1).

