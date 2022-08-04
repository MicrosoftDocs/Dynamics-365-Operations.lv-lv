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
ms.openlocfilehash: 16c79a788b66830b77b2cdfb33fd2416c530f7d2
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111572"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Kļūdas kodi tabulas kartes darbspējas pārbaudei

[!include [banner](../../includes/banner.md)]



Šajā rakstā ir aprakstīti kļūdu kodi tabulas kartes veselības pārbaudei.

## <a name="error-100"></a>Kļūda 100

Kļūdas ziņojums ir "Minimālā nepieciešamā finanšu un operāciju platformas versija ir PAR KĀR 43, lai izpildītu finanšu un operāciju ieteikumus."

Funkcijai ir nepieciešami platformas atjauninājumi versijai 10.0.19 vai jaunākai finanšu un operāciju programmai.

## <a name="error-400"></a>Kļūda 400

Tiek rādīts kļūdas ziņojums: " \{Nav atrasti biznesa notikumu reģistrācijas dati elementa finanšu un operāciju UniqueEntityName\}, kas nozīmē, ka karte nav palaista, vai visu lauku kartēšana nav vienvirziena.

## <a name="error-500"></a>Kļūda 500

Kļūdas ziņojums ir " \{Projekta nosaukumam\} nav atrastas projekta konfigurācijas. Tas varētu būt neiespējots projekts, vai arī visi lauku kartējumi ir vienvirziena no debitoru saistībām uz finansēm un operācijām."

Pārbaudiet tabulas kartes kartējumus. Ja tās ir vienvirziena no debitoru piesaistes programmām finanšu un operāciju programmām, neviens trafiks netiek ģenerēts tiešai sinhronizācijai no finanšu un operāciju programmām uz Dataverse.

## <a name="error-900"></a>Kļūda 900

Kļūdas ziņojums ir "Nederīgs avota filtra \{sourceFilter formāts\} elementa finanšu un operāciju \{UniqueEntityName\}".

Avota filtrs, kas ir norādīts tabulu kartē finanšu un operāciju programmām, nav sintakses pareizs. Lai pārbaudītu filtra kritērijus, skatiet sadaļu [Tiešās sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Kļūda 1000

Kļūdas ziņojums ir " Elementa finanšu un \{operāciju vaicājums UniqueEntityName\}, kas tiek izmantots duālās rakstīšanas \{tiešajai sinhronizācijai, ir finanšu un operāciju EntityFilterQueryString.\} Ieraksti, kas atbilst vaicājuma kritērijiem, tiks izdoti tiešai sinhronizācijai."

Atgrieztais elementa vaicājums ir elementa dublēšanas SQL vaicājums. Pārbaudiet vaicājuma iekšējos savienojumus vai filtrus, kas nosaka biznesa datus, kas tiek izdoti tiešai sinhronizācijai. Iekšējie savienojumi un filtri ir obligātie nosacījumi, kas jāizpilda katram ierakstam, kas tiek izdots duālās rakstīšanas tiešajai sinhronizācijai.

## <a name="error-1300"></a>Kļūda 1300

Kļūdas ziņojums ir " \{Virtuālie lauki s.EntityFieldName\}\{elementa finanšu un operāciju EntityMetadata.EntityProperties.LogicalEntityName\} var netiģizēt dubultajai rakstīšanai."

Finanšu un operāciju tabulu virtuālie lauki nav iespējoti izsekošanai. Tieša sinhronizācija var sinhronizēt datus, bet nevarēs saņemt kolonnās veiktās izmaiņas.

## <a name="error-1500"></a>Kļūda 1500

Kļūdas ziņojums ir šāds: "Ir jābūt vismaz vienam laukam, kas ir kartēts uz meklēšanas lauku Customer Engagement, lai iespējotu izsekošanu datu avotā \{datasource.DataSourceName\}."

Elementa datu avotam nav neviena lauka, kas ir kartēts dubultai rakstīšanai. Pamattakstā veiktās izmaiņas netiks izsekotas dubultās rakstīšanas gadījumā.

## <a name="error-1600"></a>Kļūda 1600

Kļūdas ziņojums ir "Datu avots: \{datu avots. DataSourceName\} elementa finansēm \{un operācijām EntityMetadata.EntityProperties.LogicalEntityName\} ir diapazons. Tikai ieraksti, kas atbilst diapazona nosacījumam, tiek izdoti nosūtīšanai."

Elementiem finanšu un operāciju programmās var būt datu avoti, kuros ir iespējoti filtru diapazoni. Šie diapazoni nosaka ierakstus, kas ir paņemti kā daļa no tiešas sinhronizācijas. Ja daži ieraksti ir izlaisti no finanšu un operāciju programmām uz Dataverse, pārbaudiet, vai ieraksti atbilst entītijas diapazona kritērijiem. Vienkāršs veids, kā to izdarīt, ir palaist SQL vaicājumu, kas ir līdzīgs šim piemēram.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Kļūda 1700

Kļūdas ziņojums ir "Tabula: \{datasourceTable.Key.subscribedTableName\} elementam \{datasourceTable.Key.entityName\} ir izsekots elementam \{origTableToEntityMaps.EntityName\}. Tās pašas tabulas, kas tiek izsekotas vairākiem elementiem, var ietekmēt sistēmas veiktspēju tiešās sinhronizācijas transakcijās."

Ja vairākas entītijas izseko vienu un to pašu tabulu, jebkuras izmaiņas tabulā aktivizēs saistīto entītiju dubultās rakstīšanas novērtējumu. Lai arī filtra klauzulas nosūtīs tikai derīgos ierakstus, novērtējums var radīt veiktspējas problēmu, ja ir ilglaicīgi vaicājumi vai neplānoti vaicājumu plāni. No biznesa perspektīvas šis jautājums var nebūt derīgs. Tomēr, ja vairākām entītijām pastāv daudz tabulu, ieteicams vienkāršot elementu vaicājumus vai to optimizāciju.

## <a name="error-1800"></a>Kļūda 1800
Kļūdas ziņojums ir "Datu avots: elementam {} CustCustomerV3Entity ir diapazona vērtība. Ienākošo ierakstu upserts no Dataverse finansēm un operācijas var ietekmēt entītijas diapazona vērtības. Lūdzu, pārbaudiet ierakstu atjauninājumus Dataverse no finansēm un darbībām ar ierakstiem, kas neatbilst filtra kritērijiem, lai pārbaudītu jūsu iestatījumus."

Ja elementam finanšu un operāciju programmās ir norādīts diapazons, Dataverse tad ir jāpārbauda ienākošo sinhronizāciju no finanšu un operāciju programmām uz atjaunināšanas uzvedību ierakstos, kas neatbilst šī diapazona kritērijiem. Jebkurš ieraksts, kas neatbilst diapazonam, entītija tiek uzskatīta par ievietošanas operāciju. Ja pakārtotajā tabulā ir esošs ieraksts, iespraušana neizdosies. Pirms izvietošanas ražošanā ieteicams pārbaudīt šo lietošanas gadījumu visiem scenārijiem.

## <a name="error-1900"></a>Kļūda 1900
Kļūdas ziņojums ir šāds: "Elementam ir {} datu avoti, kas netiek izsekoti izejošai dubultai rakstīšanai. Tas var ietekmēt tiešsaistes sinhronizācijas vaicājuma veiktspēju. Lūdzu, remojiet elementu finansēs un operācijās, lai noņemtu neizmantotos datu avotus un tabulas vai lai ieviestu getEntityRecordIdsImpactedByTableChange, lai optimizētu izpildlaika vaicājumus."

Ja ir daudz datu avotu, kas netiek izmantoti izsekošanai faktiskajai tiešajai sinhronizācijai no finanšu un operāciju programmām, tad ir iespējamība, ka elementa veiktspēja var ietekmēt sinhronizāciju tiešsaistē. Lai optimizētu izsekotās tabulas, izmantojiet metodi getEntityRecordIdsImpactedByTableChange.

## <a name="error-5000"></a>Kļūda 5000
Kļūdas ziņojums ir "Sinhroni pārsūtīšanas darbības ir reģistrētas elementa kontu datu pārvaldības notikumiem. Tās var ietekmēt sākotnējo sinhronizāciju un tiešsaistes sinhronizācijas importa veiktspēju Dataverse. Lai nodrošinātu labāko veiktspēju, lūdzu, mainiet apstrādes formu uz asinhrono apstrādi. Reģistrēto uzņēmumu saraksts {}.

Sinhroni izpildes noteikumi elementam Dataverse var ietekmēt tiešsaistes sinhronizāciju un intial sinhronizācijas veiktspēju, pievienojot to darbību noslodzei. Ieteicamā pieeja ir vai nu izslēdz darbības, vai izveidot šos sinhronizēšanas datus par lēnu ielādes laiku sākotnējā sinhronizācijā vai tiešsaistes sinhronizāciju konkrētam elementam.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

