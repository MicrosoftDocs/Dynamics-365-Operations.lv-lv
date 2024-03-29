---
title: ER funkciju saraksts saraksta kategorijā
description: Šajā rakstā ir sniegta informācija par saraksta funkcijām, kas tiek atbalstītas Elektronisko pārskatu veidošanai (ER).
author: kfend
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 6c28445f731393857cdb0c75c1244e557b5ff4a4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277698"
---
# <a name="list-of-er-functions-in-the-list-category"></a>ER funkciju saraksts saraksta kategorijā

[!include [banner](../includes/banner.md)]

Elektronisko pārskatu (ER) sarakstu funkcijas var izmantot, lai izgūtu informāciju no un veiktu operācijas ar datu avotiem no datu veidiem *Ierakstu saraksts* un *Konteiners (ieraksts)*. Šajā rakstā ir sniegts šo funkciju kopsavilkums.

## <a name="list-of-supported-functions"></a>Atbalstīto funkciju saraksts

| Funkcija | Apraksts |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | Šī funkcija darbojas kā atmiņā esoša atlase. Tā atgriež jaunu izplātu *Ierakstu saraksta* vērtību, kas sastāv no ierakstu saraksta, kas apzīmē visus vienumus, kuri atbilst norādītajam ceļam. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Šī funkcija darbojas kā apvienots SQL vaicājums. Tā atgriež jaunu izplātu *Ierakstu saraksta* vērtību, kas sastāv no ierakstu saraksta, kas apzīmē visus vienumus, kuri atbilst norādītajam ceļam. |
| [Skaits](er-functions-list-count.md)                       | Šī funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē ierakstu skaitu norādītajā sarakstā, ja saraksts nav tukšs. Ja saraksts ir tukšs, šī funkcija atgriež **0** (nulli). |
| [EmptyList](er-functions-list-emptylist.md)               | Atgriezt tukšu *Ierakstu saraksta* vērtību, šī saraksta struktūrai kā avotu izmantojot norādīto sarakstu.|
| [Uzskaitījums](er-functions-list-enumerate.md)               | Šī funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no uzskaitījumā norādītājiem saraksta ierakstiem. |
| [Filtrēt](er-functions-list-filter.md)                     | Šī funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību, kad vaicājums ir mainīts tā, ka tas filtrē norādīto nosacījumu. |
| [Pirmais](er-functions-list-first.md)                       | Šī funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis saraksts nav tukšs. Ja saraksts ir tukšs, šī funkcija rādīs izņēmumu. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Šī funkcija atgriež norādītā saraksta pirmo ierakstu kā vērtību *Konteiners (ieraksts)*, ja šis ieraksts nav tukšs. Ja ieraksts ir tukšs, šī funkcija atgriež tukšu *Konteinera (ieraksta)* vērtību. |
| [Indekss](er-functions-list-index.md)                       | Šī funkcija atgriež *Konteinera (ieraksta)* vērtību, kas ir atlasīta, izmantojot norādītajā sarakstā norādīto skaitlisko indeksu. Šī funkcija parāda izņēmumu, ja indekss neietilpst norādītajā sarakstā esošo ierakstu diapazonā. |
| [IsEmpty](er-functions-list-isempty.md)                   | Šī funkcija atgriež *Būla* vērtību **TRUE**, ja norādītajā sarakstā nav ierakstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. |
| [Saraksts](er-functions-list-list.md)                         | Šī funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv no jauna saraksta, kas ir izveidots no norādītiem argumentiem.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Šī funkcija aprēķina norādīto izteiksmi kā atlasītāju katram norādītā saraksta ierakstam. Tiek atgriezta jauna *Ierakstu saraksta* vērtība, kurā ir viens ieraksts katrai unikālajai atlasītāja vērtībai.|
| [ListJoin](er-functions-list-listjoin.md)                 | Šī funkcija atgriež *Ierakstu saraksta* vērtību, kas pārstāv jaunu savienotu sarakstu, kas ir izveidots no norādītiem argumentiem.|
| [ListOfFields](er-functions-list-listoffields.md)         | Šī funkcija atgriež *Ierakstu saraksta* vērtību, kas tiek izveidota, pamatojoties uz norādītā *Uzskaitījuma* vai *Konteinera (ieraksta)* veida argumenta struktūru. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Šī funkcija atgriež jaunu *Ierakstu saraksta* vērtību, kas sastāv vienīgi no norādītā saraksta pirmā ieraksta.|
| [OrderBy](er-functions-list-orderby.md)                   | Šī funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir sakārtots atbilstoši norādītajiem argumentiem. Šos argumentus var definēt kā izteiksmes. |
| [Atkārtot](er-functions-list-repeat.md)                     | Šī funkcija veido ierakstu, kas satur lauku, kuram ir vērtība, kas atbilst norādītajai ievadei. Tad tā atgriež jaunu *ierakstu sarakstu*, kas tiek atkārtots noteiktu reižu skaitu. |
| [Apgriezt](er-functions-list-reverse.md)                   | Šī funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību apgrieztā kārtošanas secībā. |
| [Sadalīt](er-functions-list-split.md)                       | Šī funkcija sadala norādīto ievades virkni apakšvirknēs un atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību. |
| [SplitList](er-functions-list-splitlist.md)               | Šī funkcija sadala norādīto sarakstu apakšsarakstos (jeb partijās), kuri katrs satur norādītu ierakstu skaitu. Pēc tam tā atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību, kas sastāv no partijām. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Šī funkcija sadala norādīto sarakstu jaunā apakšsaraksta (partiju) sarakstā. Katras partijas ierakstu skaits tiek aprēķināts dinamiski. Pēc tam funkcija atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību, kas sastāv no partijām. |
| [StringJoin](er-functions-list-stringjoin.md)             | Šī funkcija atgriež *Virknes* vērtību, kas sastāv no norādītā saraksta norādītā lauka savirknētajām vērtībām. Vērtības var atdalīt ar norādīto norobežotāju. |
| [Printera ports](er-functions-list-where.md)                       | Šī funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir filtrēts atbilstoši norādītajiem nosacījumam. |

## <a name="additional-resources"></a>Papildu resursi

[Elektronisko pārskatu veidošanas apskats](general-electronic-reporting.md)

[Formulu veidotājs elektronisko atskaišu veidošanā](general-electronic-reporting-formula-designer.md)

[Elektronisko atskaišu veidošanas formulas valoda](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
