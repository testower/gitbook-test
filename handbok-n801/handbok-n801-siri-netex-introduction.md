# Håndbok N801 \(SIRI/NeTEX\) : Introduction

These pages describe the formats used and the necessary considerations to take when producing public transport information for Norway. The structure of the data is defined by the two formats, NeTEx and SIRI, and the content is regulated by “Håndbok N801”, an official manual published by the Norwegian Railroad Directorate \(Jernbanedirektoratet\).

All operators of road, rail, and waterborne public transport are under law required to provide openly available public transport data through _Entur_.

Pages in this workspace

* 
Recently updated pages 

*  [Identifying systems and operators](PUBLIC/Identifying-systems-and-operators_2537914775.html) 26. Apr 2021 • contributed by [Tom Erik Støwer](PUBLIC/null/display/~5d19f8a491943f0d2ac51bcd)
*  [Internationalisation in Mobility API v2](PUBLIC/Internationalisation-in-Mobility-API-v2_2527133965.html) 23. Apr 2021 • contributed by [Tom Erik Støwer](PUBLIC/null/display/~5d19f8a491943f0d2ac51bcd)
*  [Overordnet dataflyt til Bane Nor.png](PUBLIC/null/spaces/ROR/pages/664174685/Forenklet+oversikt+togdata?preview=%2F664174685%2F1978368068%2FOverordnet+dataflyt+til+Bane+Nor.png) 20. Apr 2021 • attached by [Brede Dammen](PUBLIC/null/display/~557058%3Ae58428e0-4bec-4052-b1f8-38e56aee891a)
*  [Overordnet dataflyt til Bane Nor](PUBLIC/null/spaces/ROR/pages/664174685/Forenklet+oversikt+togdata?preview=%2F664174685%2F1978302550%2FOverordnet+dataflyt+til+Bane+Nor) 20. Apr 2021 • attached by [Brede Dammen](PUBLIC/null/display/~557058%3Ae58428e0-4bec-4052-b1f8-38e56aee891a)
*  [Overgang fra intern til ekstern DatedServiceJourney](PUBLIC/Overgang-fra-intern-til-ekstern-DatedServiceJourney_2503607289.html) 20. Apr 2021 • contributed by [Lasse Tyrihjell](PUBLIC/null/display/~557058%3A7b4c3e9a-7383-4434-8265-836b623863ff)

 [Show More](/wiki/plugins/recently-updated/changes.action?theme=concise&pageSize=5&startIndex=5&searchToken=1&spaceKeys=ROR&contentType=-mail,page,comment,blogpost,attachment,userinfo,spacedesc,personalspacedesc,space,draft,custom&cursor=_sa_WzE2MTg5MDE4MzkwMDAsIlx0MjUwMzYwNzI4OSBtJTc5cmUjI0VOVFxcaj4zLCpiMmIgY3AiXQ%3D%3D) ![Please wait](../.gitbook/assets/wait.gif)

## **På norsk** <a id="Introduction-P&#xE5;norsk"></a>

_Entur AS_ har som mandat å levere en en nasjonal, konkurransenøytral reiseplanleggertjeneste basert på følgende punkter:

1. Etablere og vedlikeholde et baksystem som skal håndtere innsamling, validering, strukturering og tilgjengeliggjøring av alle nasjonale stoppesteds-, rute- og sanntidsdata
   1. Tilgjengeliggjøre et åpent API som kan levere nasjonale reisesøk for tredjeparter
2. Etablere en sluttbrukerløsning for brukere med nasjonale reisesøk for alle modaliteter
3. Vedlikeholde Håndbok N801 i henhold til nye standarder og prosesser for innsamling av stoppesteds-, rute- og sanntidsdata

Revidert innhold for Håndbok N801 og NeTEx og SIRI-profil Norge finnes på undersider av dette arbeidsområdet.

Jernbanedirektoratet er offisiell utsteder av Håndbok N801 og nasjonale profiler for henholdsvis SIRI og NeTEx \([Jernbanedirektoratet](https://www.jernbanedirektoratet.no/no/jernbanesektoren/handboker/handboker-for-samlet-kollektiv/handbok-801-nasjonale-rutedata/)\). For alle som skal implementere disse kravene anbefales å følge dokumentasjonen på denne siden da dette er oppdatert med seneste justeringer som vil bli del av den offisielle publiseringen til Jernbanedirektoretet ved fremtidige revisjoner.

## **In English** <a id="Introduction-InEnglish"></a>

_Entur AS_ is mandated to provide a national, business-neutral journey planner service hinged on the following key points:

1. Establish and maintain a backend system to handle the collection, validation, structuring and availability of all national stop, route and real-time data
   1. Provide an open API that can deliver national travel searches for third parties
2. Establish an end-user solution for users with national travel search for all modalities
3. Maintain Manual N801 according to new standards and processes for the collection of stop, route and real-time data

Revised content for Handbook N801 and NeTEx and SIRI profile Norway can be found on subpages of this workspace.

The Railway Directorate is the official issuer of Handbook N801 and national profiles for SIRI and NeTEx \(Railway Directorate\) respectively. For anyone who is going to implement these requirements, it is recommended to follow the documentation on this page as this has been updated with the latest adjustments which will be part of the official publication to the Railway Directorate for future revisions.

For questions related to data delivery or these pages, please contact [kollektivdata@entur.org](mailto:kollektivdata@entur.org)

For questions related to the mandate of _Entur_, or _Entur_ as a business, see [www.entur.org](https://www.entur.org/)

For questions related to using _Entur’s_ systems and API’s, please visit [developer.entur.org](https://developer.entur.org/)

