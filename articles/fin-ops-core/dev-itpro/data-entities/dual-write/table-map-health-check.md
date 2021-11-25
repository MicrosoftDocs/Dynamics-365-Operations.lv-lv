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
ms.openlocfilehash: c2d1f1e39a5ddccddf6fbbf524ff7eb0945b3c32
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782240"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Kļūdas kodi tabulas kartes darbspējas pārbaudei

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā aprakstīti kļūdu kodi tabulas kartes darbspējas pārbaudei.

## <a name="error-100"></a>Kļūda 100

Kļūdas ziņojums ir "Minimālais nepieciešamais Finance and Operations platformas versijas līmenis ir PU 43, lai palaistu Finance and Operations rekomendācijas."

Šis līdzeklis pieprasa platformas atjauninājumus versijā 10.0.19 vai jaunākā Finance and Operations programmu versijā.

## <a name="error-400"></a>Kļūda 400

Kļūdas ziņojums ir "Nav atrasti biznesa notikumu reģistrācijas dati elementam \{Finance and Operations UniqueEntityName\}, kas nozīmē, ka karte nedarbojas vai visi lauku kartējumi nav vienvirziena."

## <a name="error-500"></a>Kļūda 500

Kļūdas ziņojums ir " \{ Projekta nosaukumam\} nav atrastas projekta konfigurācijas. Tas var būt vai nu iespējots, vai visi lauku kartējumi ir vienvirziena no Customer Engagement uz Finance and Operations."

Pārbaudiet tabulas kartes kartējumus. Ja tās ir vienvirziena no Customer Engagement lietojumprogrammām uz Finance and Operations programmām, netiek ģenerēts trafiks tiešai sinhronizācijai no Finance and Operations programmām uz Dataverse.

## <a name="error-900"></a>Kļūda 900

Kļūdas ziņojums ir "Nederīgs avota filtra \{ sourceFilter\} formāts elementam \{Finance and Operations UniqueEntityName\}."

Avota filtrs, kas ir norādīts Finance and Operations programmu tabulu kartē, nav sintaktiski pareizs. Lai pārbaudītu filtra kritērijus, skatiet sadaļu [Tiešās sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Kļūda 1000

Tiek rādīts kļūdas ziņojums: "Elementa \{Finance and Operations UniqueEntityName\} vaicājums, kas tiek izmantots duālās rakstīšanas tiešajai sinhronizācijai, ir \{Finance and Operations EntityFilterQueryString\}. Ieraksti, kas atbilst vaicājuma kritērijiem, tiks izdoti tiešai sinhronizācijai."

Atgrieztais elementa vaicājums ir elementa dublēšanas SQL vaicājums. Pārbaudiet vaicājuma iekšējos savienojumus vai filtrus, kas nosaka biznesa datus, kas tiek izdoti tiešai sinhronizācijai. Iekšējie savienojumi un filtri ir obligātie nosacījumi, kas jāizpilda katram ierakstam, kas tiek izdots duālās rakstīšanas tiešajai sinhronizācijai.

## <a name="error-1300"></a>Kļūda 1300

Tiek parādīts kļūdas ziņojums: "Virtuālie lauki \{ s.EntityFieldName\} elementam \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} var netikt izsekoti duālās rakstīšanas gadījumā."

Virtuālie lauki no Finance and Operations tabulām nav iespējoti izsekošanai. Tieša sinhronizācija var sinhronizēt datus, bet nevarēs saņemt kolonnās veiktās izmaiņas.

## <a name="error-1500"></a>Kļūda 1500

Kļūdas ziņojums ir šāds: "Ir jābūt vismaz vienam laukam, kas ir kartēts uz meklēšanas lauku Customer Engagement, lai iespējotu izsekošanu datu avotā \{ datasource.DataSourceName\}."

Elementa datu avotam nav neviena lauka, kas ir kartēts dubultai rakstīšanai. Pamattakstā veiktās izmaiņas netiks izsekotas dubultās rakstīšanas gadījumā.

## <a name="error-1600"></a>Kļūda 1600

Kļūdas ziņojums ir "Datu avots: \{ datasource.DataSourceName\} elementam \{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} ir diapazons. Tikai ieraksti, kas atbilst diapazona nosacījumam, tiek izdoti nosūtīšanai."

Lietojumprogrammu Finance and Operations elementiem var būt datu avoti, kur ir iespējoti filtru diapazoni. Šie diapazoni nosaka ierakstus, kas ir paņemti kā daļa no tiešas sinhronizācijas. Ja daži ieraksti ir izlaisti no Finance and Operations programmām uz Dataverse, pārbaudiet, vai ieraksti atbilst entītijas diapazona kritērijiem. Vienkāršs veids, kā to izdarīt, ir palaist SQL vaicājumu, kas ir līdzīgs šim piemēram.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Kļūda 1700

Kļūdas ziņojums ir "Tabula: \{ datasourceTable.Key.subscribedTableName\} elementam \{ datasourceTable.Key.entityName\} ir izsekots elementam \{ origTableToEntityMaps.EntityName\}. Tās pašas tabulas, kas tiek izsekotas vairākiem elementiem, var ietekmēt sistēmas veiktspēju tiešās sinhronizācijas transakcijās."

Ja vairākas entītijas izseko vienu un to pašu tabulu, jebkuras izmaiņas tabulā aktivizēs saistīto entītiju dubultās rakstīšanas novērtējumu. Lai arī filtra klauzulas nosūtīs tikai derīgos ierakstus, novērtējums var radīt veiktspējas problēmu, ja ir ilglaicīgi vaicājumi vai neplānoti vaicājumu plāni. No biznesa perspektīvas šis jautājums var nebūt derīgs. Tomēr, ja vairākām entītijām pastāv daudz tabulu, ieteicams vienkāršot elementu vaicājumus vai to optimizāciju.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
