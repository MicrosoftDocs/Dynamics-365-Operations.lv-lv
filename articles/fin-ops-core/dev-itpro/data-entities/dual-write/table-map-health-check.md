---
title: Kļūdas kodi tabulas kartes darbspējas pārbaudei
description: Šajā tēmā aprakstīti kļūdu kodi tabulas kartes darbspējas pārbaudei.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061282"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Kļūdas kodi tabulas kartes darbspējas pārbaudei

[!include [banner](../../includes/banner.md)]



Šajā tēmā aprakstīti kļūdu kodi tabulas kartes darbspējas pārbaudei.

## <a name="error-100"></a>Kļūda 100

Kļūdas ziņojums ir šāds: "Lai izpildītu Finance and Operations ieteikumus, minimālā nepieciešamā Finance and Operations platformas versija ir PU 43."

Lai izmantotu šo līdzekli, ir nepieciešami platformas atjauninājumi programmas Finance and Operations versijai 10.0.19 vai jaunākai versijai.

## <a name="error-400"></a>Kļūda 400

Kļūdas ziņojums ir šāds: "Entītijai nav atrasti biznesa notikumu reģistrācijas dati\{ Finance and Operations UniqueEntityName\} kas nozīmē, ka vai nu karte nedarbojas, vai arī visa lauka kartēšana ir vienvirziena."

## <a name="error-500"></a>Kļūda 500

Kļūdas ziņojums ir " \{Projekta nosaukumam\} nav atrastas projekta konfigurācijas. Tas var būt vai nu projekts, kas nav iespējots, vai arī visi lauka kartējumi ir vienvirziena no klientu iesaistīšanas uz Finance and Operations.

Pārbaudiet tabulas kartes kartējumus. Ja tie ir vienvirziena no klientu iesaistīšanas lietotnēm uz Finance and Operations lietotnēm, netiek ģenerēta datplūsma tiešraides sinhronizācijai no Finance and Operations lietotnēm uz Dataverse.

## <a name="error-900"></a>Kļūda 900

Kļūdas ziņojums ir “Nederīgs avota filtrs\{ avota filtrs\} entītijas formāts\{ Finance and Operations UniqueEntityName\} ”.

Avota filtrs, kas norādīts programmas Finance and Operations tabulas kartē, nav sintaktiski pareizs. Lai pārbaudītu filtra kritērijus, skatiet sadaļu [Tiešās sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Kļūda 1000

Kļūdas ziņojums ir “Entity\{ Finance and Operations UniqueEntityName\} vaicājums, ko izmanto divkāršās rakstīšanas reāllaikā sinhronizācijai\{ Finance and Operations EntityFilterQueryString \}. Ieraksti, kas atbilst vaicājuma kritērijiem, tiks izdoti tiešai sinhronizācijai."

Atgrieztais elementa vaicājums ir elementa dublēšanas SQL vaicājums. Pārbaudiet vaicājuma iekšējos savienojumus vai filtrus, kas nosaka biznesa datus, kas tiek izdoti tiešai sinhronizācijai. Iekšējie savienojumi un filtri ir obligātie nosacījumi, kas jāizpilda katram ierakstam, kas tiek izdots duālās rakstīšanas tiešajai sinhronizācijai.

## <a name="error-1300"></a>Kļūda 1300

Kļūdas ziņojums ir “Virtuālie lauki\{ s.EntityFieldName\} entītijai\{ Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} var netikt izsekots divkāršai rakstīšanai."

Virtuālie lauki no tabulām Finance and Operations nav iespējoti izsekošanai. Tieša sinhronizācija var sinhronizēt datus, bet nevarēs saņemt kolonnās veiktās izmaiņas.

## <a name="error-1500"></a>Kļūda 1500

Kļūdas ziņojums ir šāds: "Ir jābūt vismaz vienam laukam, kas ir kartēts uz meklēšanas lauku Customer Engagement, lai iespējotu izsekošanu datu avotā \{datasource.DataSourceName\}."

Elementa datu avotam nav neviena lauka, kas ir kartēts dubultai rakstīšanai. Pamattakstā veiktās izmaiņas netiks izsekotas dubultās rakstīšanas gadījumā.

## <a name="error-1600"></a>Kļūda 1600

Kļūdas ziņojums ir “Datu avots:\{ datasource.DataSourceName\} entītijai\{ Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} ir diapazons. Tikai ieraksti, kas atbilst diapazona nosacījumam, tiek izdoti nosūtīšanai."

Programmu Finance and Operations entītijām var būt datu avoti, kuros ir iespējoti filtru diapazoni. Šie diapazoni nosaka ierakstus, kas ir paņemti kā daļa no tiešas sinhronizācijas. Ja daži ieraksti tiek izlaisti no programmām Finance and Operations uz Dataverse, pārbaudiet, vai ieraksti atbilst entītijas diapazona kritērijiem. Vienkāršs veids, kā to izdarīt, ir palaist SQL vaicājumu, kas ir līdzīgs šim piemēram.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Kļūda 1700

Kļūdas ziņojums ir "Tabula: \{datasourceTable.Key.subscribedTableName\} elementam \{datasourceTable.Key.entityName\} ir izsekots elementam \{origTableToEntityMaps.EntityName\}. Tās pašas tabulas, kas tiek izsekotas vairākiem elementiem, var ietekmēt sistēmas veiktspēju tiešās sinhronizācijas transakcijās."

Ja vairākas entītijas izseko vienu un to pašu tabulu, jebkuras izmaiņas tabulā aktivizēs saistīto entītiju dubultās rakstīšanas novērtējumu. Lai arī filtra klauzulas nosūtīs tikai derīgos ierakstus, novērtējums var radīt veiktspējas problēmu, ja ir ilglaicīgi vaicājumi vai neplānoti vaicājumu plāni. No biznesa perspektīvas šis jautājums var nebūt derīgs. Tomēr, ja vairākām entītijām pastāv daudz tabulu, ieteicams vienkāršot elementu vaicājumus vai to optimizāciju.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
