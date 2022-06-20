---
title: VALUEIN ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota VALUEIN Electronic Reporting (ER) funkcija.
author: NickSelin
ms.date: 12/14/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca4bd5ad671e1c70027a2cdaa0797bfdc89cf914
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909312"
---
# <a name="valuein-er-function"></a>VALUEIN ER funkcija

[!include [banner](../includes/banner.md)]

`VALUEIN` funkcija nosaka, vai norādītā ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai. Tas atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.

## <a name="syntax"></a>Sintakse

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumenti

`input`: *Lauks*

*Ierakstu saraksta* tipa datu avota vienuma derīgs ceļš. Šī elementa vērtībai tiks noteikta atbilstība.

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`list item expression`: *Būla*

Derīga nosacījuma izteiksme apzīmē izteiksmi, kas norāda uz vai satur vienu norādītā saraksta lauku, kurš ir jāizmanto atbilstības noteikšanai.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Parasti funkcija `VALUEIN` tiek tulkota uz **OR** nosacījumu kopu. Ja **OR** nosacījumu saraksts ir liels un var tikt pārsniegts maksimālais kopējais SQL priekšraksta garums, apsveriet iespēju izmantot funkciju [`VALUEINLARGE`](er-functions-logical-valueinlarge.md).

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

Dažos gadījumos to var pārtulkot uz datu bāzes SQL paziņojumu, izmantojot `EXISTS JOIN` operatoru.

> [!NOTE]
> Funkcijai atgrieztā `VALUEIN` vērtība tiek [izmantota](er-functions-list-filter.md#usage-notes) dažādi, atkarībā no tā, vai šī funkcija tiek lietota, [`FILTER`](er-functions-list-filter.md) lai norādītu funkcijas vai funkcijas atlases [`WHERE`](er-functions-list-where.md) kritērijus.

## <a name="example-1"></a>1. piemērs

Savā modeļa kartējumā jūs definējat datu avotu: **Saraksts** ar veidu *Aprēķinātais lauks* . Šajā datu avotā ir izteiksme `SPLIT ("a,b,c", ",")`.

Ja tiek izsaukts datu avots, ja tas ir konfigurēts kā `VALUEIN ("B", List, List.Value)` izteiksme, tas atgriež **TRUE.** Šajā gadījumā `VALUEIN` funkcija tiek tulkota uz šādu nosacījumu kopu: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.

Ja tiek izsaukts datu avots, ja tas ir konfigurēts kā `VALUEIN ("B", List, LEFT(List.Value, 0))` izteiksme, tas atgriež **FALSE**. Šajā gadījumā `VALUEIN` funkcija tiek tulkota uz šādu nosacījumu: `("B" = "")`, kas nav vienāds ar **TRUE**.

Šāda nosacījuma tekstā rakstzīmju skaita augšējā robežvērtība ir 32 768 rakstzīmes. Tādēļ nevajadzētu veidot datu avotus, kas izpildlaikā varētu pārsniegt šo ierobežojumu. Ja ierobežojums tiek pārsniegts, programmas darbība tiek pārtraukta un tiek parādīts izņēmums. Piemēram, šāda situācija var rasties, ja datu avots ir konfigurēts kā `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` un sarakstā **List1** un **List2** ir daudz ierakstu.

Noteiktos gadījumos funkcija `VALUEIN` tiek tulkota uz datu bāzes priekšrakstu, izmantojot operatoru `EXISTS JOIN`. Šāda uzvedība it spēkā, kad tiek izmantota funkcija [`FILTER`](er-functions-list-filter.md) un tiek ievēroti šādi nosacījumi:

- Opcija **ASK FOR QUERY** ir izslēgta funkcijas `VALUEIN` datu avotam tādai funkcijai, kas atsaucas uz ierakstu sarakstu. Šim datu avotam izpildlaikā netiks lietoti nekādi papildu nosacījumi.
- Funkcijas `VALUEIN` datu avotam tādai funkcijai, kas atsaucas uz ierakstu sarakstu, nav konfigurētas ligzdotās izteiksmes.
- Funkcijas `VALUEIN` saraksta elements atsaucas uz kādu norādītā datu avota lauku, nevis izteiksmi vai metodi.

Apsveriet iespēju izmantot šo opciju, nevis funkciju [`WHERE`](er-functions-list-where.md), kā iepriekš aprakstīts šajā piemērā.

## <a name="example-2"></a>2. piemērs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- **Tabulas ierakstu** veida datu avots *In*. Šis datu avots attiecas uz Intrastat tabulu.
- **Tabulas ierakstu** veida datu avots *Port*. Šis datu avots attiecas uz IntrastatPort tabulu.

Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, tiek ģenerēts šāds SQL priekšraksts, lai atgrieztu filtrētos ierakstus Intrastat tabulā.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Laukiem **dataAreaId** gala SQL priekšraksts tiek ģenerēts, izmantojot operatoru `IN`.

## <a name="example-3"></a>3. piemērs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- **Aprēķinātā lauka** veida datu avots *Le*. Šajā datu avotā ir izteiksme `SPLIT ("DEMF,GBSI,USMF", ",")`.
- **Tabulas ierakstu** veida datu avots *In*. Šis datu avots attiecas uz Intrastat tabulu, un tam ir ieslēgta opcija **Starpuzņēmums**.

Kad tiek izsaukts datu avots, kas ir konfigurēts kā izteiksme `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, gala SQL priekšrakstā ir šāds nosacījums:

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Papildu resursi

[Loģiskās funkcijas](er-functions-category-logical.md)

[VALUEINLARGE funkcijas](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
