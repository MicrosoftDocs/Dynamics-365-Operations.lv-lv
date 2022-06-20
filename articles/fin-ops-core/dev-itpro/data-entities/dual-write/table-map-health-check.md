---
title: Kļūdas kodi tabulas kartes darbspējas pārbaudei
description: Šajā rakstā ir aprakstīti kļūdu kodi tabulas kartes veselības pārbaudei.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 3ae78077fc716311c38620b14665af3983a44c2d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884088"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Kļūdas kodi tabulas kartes darbspējas pārbaudei

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir aprakstīti kļūdu kodi tabulas kartes veselības pārbaudei.

## <a name="error-100"></a>Kļūda 100

Kļūdas ziņojums ir "Minimālā nepieciešamā finanšu un operāciju platformas versija ir PAR 43 EUR, lai izpildītu finanšu un operāciju ieteikumus."

Šis līdzeklis pieprasa platformas atjauninājumus versijā 10.0.19 vai jaunākai finanšu un operāciju programmai.

## <a name="error-400"></a>Kļūda 400

Kļūdas ziņojums ir " \{Nav atrasti biznesa notikumu reģistrācijas dati elementam Finanses un operācijas UniqueEntityName\}, kas nozīmē, ka karte nav palaista, vai visu lauku kartēšana nav vienvirziena.

## <a name="error-500"></a>Kļūda 500

Kļūdas ziņojums ir " \{Projekta nosaukumam\} nav atrastas projekta konfigurācijas. Tas, iespējams, nav iespējots projekts vai arī visi lauku kartējumi ir vienvirziena no debitoru saistībām uz Finansēm un operācijām."

Pārbaudiet tabulas kartes kartējumus. Ja tie ir vienvirziena no debitoru piesaistes programmām uz Finanšu un operāciju programmām, neviena trafika netiek ģenerēta tiešai sinhronizācijai no Finanšu un operāciju programmām uz Dataverse.

## <a name="error-900"></a>Kļūda 900

Kļūdas ziņojums ir "Nederīgs avota filtra \{sourceFilter formāts\} elementam Finanšu un \{operāciju UniqueEntityName\}."

Avota filtrs, kas ir norādīts tabulu kartē finanšu un operāciju programmām, nav sintakses pareizs. Lai pārbaudītu filtra kritērijus, skatiet sadaļu [Tiešās sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Kļūda 1000

Kļūdas ziņojums ir "Vaicājums Elementa \{finanses un operācijas UniqueEntityName\}, kas tiek izmantots duālās rakstīšanas \{tiešajai sinhronizācijai, ir Finanšu un operāciju EntityFilterQueryString \}. Ieraksti, kas atbilst vaicājuma kritērijiem, tiks izdoti tiešai sinhronizācijai."

Atgrieztais elementa vaicājums ir elementa dublēšanas SQL vaicājums. Pārbaudiet vaicājuma iekšējos savienojumus vai filtrus, kas nosaka biznesa datus, kas tiek izdoti tiešai sinhronizācijai. Iekšējie savienojumi un filtri ir obligātie nosacījumi, kas jāizpilda katram ierakstam, kas tiek izdots duālās rakstīšanas tiešajai sinhronizācijai.

## <a name="error-1300"></a>Kļūda 1300

Kļūdas ziņojums ir " \{Virtuālie lauki s.EntityFieldName\}\{elementam Finanses un operācijas EntityMetadata.EntityProperties.LogicalEntityName\} var netiģizēt dubultajai rakstīšanai."

Finanšu un operāciju tabulu virtuālie lauki nav iespējoti izsekošanai. Tieša sinhronizācija var sinhronizēt datus, bet nevarēs saņemt kolonnās veiktās izmaiņas.

## <a name="error-1500"></a>Kļūda 1500

Kļūdas ziņojums ir šāds: "Ir jābūt vismaz vienam laukam, kas ir kartēts uz meklēšanas lauku Customer Engagement, lai iespējotu izsekošanu datu avotā \{datasource.DataSourceName\}."

Elementa datu avotam nav neviena lauka, kas ir kartēts dubultai rakstīšanai. Pamattakstā veiktās izmaiņas netiks izsekotas dubultās rakstīšanas gadījumā.

## <a name="error-1600"></a>Kļūda 1600

Kļūdas ziņojums ir "Datu avots: \{datu avots. Elementa Finance un Operations \} EntityMetadata.EntityProperties.LogicalEntityName diapazons ir dataSourceName.\{\} Tikai ieraksti, kas atbilst diapazona nosacījumam, tiek izdoti nosūtīšanai."

Elementiem Finanšu un operāciju programmās var būt datu avoti, kuros ir iespējoti filtru diapazoni. Šie diapazoni nosaka ierakstus, kas ir paņemti kā daļa no tiešas sinhronizācijas. Ja daži ieraksti ir izlaisti no Finanšu un operāciju programmām uz Dataverse, pārbaudiet, vai ieraksti atbilst entītijas diapazona kritērijiem. Vienkāršs veids, kā to izdarīt, ir palaist SQL vaicājumu, kas ir līdzīgs šim piemēram.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Kļūda 1700

Kļūdas ziņojums ir "Tabula: \{datasourceTable.Key.subscribedTableName\} elementam \{datasourceTable.Key.entityName\} ir izsekots elementam \{origTableToEntityMaps.EntityName\}. Tās pašas tabulas, kas tiek izsekotas vairākiem elementiem, var ietekmēt sistēmas veiktspēju tiešās sinhronizācijas transakcijās."

Ja vairākas entītijas izseko vienu un to pašu tabulu, jebkuras izmaiņas tabulā aktivizēs saistīto entītiju dubultās rakstīšanas novērtējumu. Lai arī filtra klauzulas nosūtīs tikai derīgos ierakstus, novērtējums var radīt veiktspējas problēmu, ja ir ilglaicīgi vaicājumi vai neplānoti vaicājumu plāni. No biznesa perspektīvas šis jautājums var nebūt derīgs. Tomēr, ja vairākām entītijām pastāv daudz tabulu, ieteicams vienkāršot elementu vaicājumus vai to optimizāciju.

## <a name="error-1800"></a>Kļūda 1800
Kļūdas ziņojums ir "Datu avots: elementam {} CustCustomerV3Entity ir diapazona vērtība. Saņemšanas ieraksta upserts no Dataverse uz Finansēm un operācijām var ietekmēt entītijas diapazona vērtības. Lūdzu, pārbaudiet ieraksta atjauninājumus Dataverse no programmatūras Finanses un operācijas ar ierakstiem, kas neatbilst filtra kritērijiem, lai pārbaudītu jūsu iestatījumus."

Ja elementam finanšu un operāciju programmās ir norādīts diapazons, Dataverse tad ir jāpārbauda ienākošo sinhronizāciju no finanšu un operāciju programmām uz atjaunināšanas uzvedību ierakstos, kas neatbilst šī diapazona kritērijiem. Jebkurš ieraksts, kas neatbilst diapazonam, entītija tiek uzskatīta par ievietošanas operāciju. Ja pakārtotajā tabulā ir esošs ieraksts, iespraušana neizdosies. Pirms izvietošanas ražošanā ieteicams pārbaudīt šo lietošanas gadījumu visiem scenārijiem.

## <a name="error-1900"></a>Kļūda 1900
Kļūdas ziņojums ir šāds: "Elementam ir {} datu avoti, kas netiek izsekoti izejošai dubultai rakstīšanai. Tas var ietekmēt tiešsaistes sinhronizācijas vaicājuma veiktspēju. Lūdzu, remojiet elementu finanšu un operācijās, lai noņemtu neizmantotos datu avotus un tabulas vai lai ieviestu getEntityRecordIdsImpactedByTableChange, lai optimizētu izpildlaika vaicājumus."

Ja ir daudz datu avotu, kas netiek izmantoti izsekošanai faktiskajai tiešajai sinhronizācijai no finanšu un operāciju programmām, tad ir iespējamība, ka elementa veiktspēja var ietekmēt sinhronizāciju tiešsaistē. Lai optimizētu izsekotās tabulas, izmantojiet metodi getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Kļūda 5000
Kļūdas ziņojums ir "Sinhroni pārsūtīšanas darbības ir reģistrētas elementa kontu datu pārvaldības notikumiem. Tās var ietekmēt sākotnējo sinhronizāciju un tiešsaistes sinhronizācijas importa veiktspēju Dataverse. Lai nodrošinātu labāko veiktspēju, lūdzu, mainiet apstrādes formu uz asinhrono apstrādi. Reģistrēto uzņēmumu saraksts {}.

Sinhroni izpildes noteikumi elementam Dataverse var ietekmēt tiešsaistes sinhronizāciju un intial sinhronizācijas veiktspēju, pievienojot to darbību noslodzei. Ieteicamā pieeja ir vai nu izslēdz darbības, vai izveidot šos sinhronizēšanas datus par lēnu ielādes laiku sākotnējā sinhronizācijā vai tiešsaistes sinhronizāciju konkrētam elementam.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
