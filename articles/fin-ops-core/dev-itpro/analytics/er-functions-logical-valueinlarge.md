---
title: VALUEINLARGE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota VALUEINLARGE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705147"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE ER funkcija

[!include [banner](../includes/banner.md)]

`VALUEINLARGE` funkcija nosaka, vai norādītā *Int64* vai *Integer* tipa ievade atbilst kāda norādītā saraksta norādītā elementa vērtībai. Šī funkcija atgriež *Būla* vērtību **TRUE**, ja norādītā ievade atbilst norādītās izteiksmes palaišanas rezultātam vismaz vienam norādītā saraksta ierakstam. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**. Lai saprastu atšķirību ar `VALUEIN` funkciju, skatiet šīs tēmas [Lietojuma piezīme](#usage_note) sadaļu.

## <a name="syntax"></a>Sintakse

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumenti

`input`: *Lauks*

*Ierakstu saraksta* tipa datu avota vienības tipa derīgais ceļš. Šī elementa vērtībai tiks noteikta atbilstība.

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`list item expression`: *Izteiksme*

Derīga nosacījuma izteiksme apzīmē izteiksmi, kas norāda uz vai satur vienu norādītā saraksta lauku, kurš ir jāizmanto atbilstības noteikšanai.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name=""></a><a name="usage_note">Lietošanas piezīmes</a>

Kad norādītā ievade attēlo *Int64* vai *Integer* datu avota krājuma tipu, izsaukums, kas ir iztulkojams tiešam SQL pārskatam, norādītais saraksts tiek pārveidots uz pagaidu SQL tabulu un salīdzināšana tiek veikta datu bāzē, izpildot vienu `EXISTS JOIN` vaicājumu. Pretējā gadījumā šī funkcija darbojas kā [`VALUEIN`](er-functions-logical-valuein.md) funkcija.

Kad norādītā ievade attēlo datu avota vienumu, kas ir izveidots kā krājums, kas nav *Int64* un *Integer*, kļūda rodas noformēšanas laikā, informējot, ka `VALUEINLARGE` funkcija nav piemērojama konfigurētai ER izteiksmei.

Kad `VALUEINLARGE` funkcijas izteiksme tiek izpildīta un tiek izmantota vairāk nekā viena pagaidu tabula šīs izpildes jomā, rodas izpildlaika kļūda.

## <a name="example"></a>Paraugs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- **Tabulas ierakstu** veida datu avots *In*.
    - Šis datu avots attiecas uz **Intrastat** tabulu.
    - **Starpuzņēmumu** opcija ir iestatīta uz **Nē**.
- **Aprēķinātā lauka** veida datu avots *InMemory*.
    - Šajā datu avotā ir izteiksme `WHERE (In, In.Port <> "")`.
- **Aprēķinātā lauka** veida datu avots *InFiltered*.
    - Šajā datu avotā ir izteiksme `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Ja datu avots **InFiltered** tiek izsaukts uzņēmuma **DEMF** kontekstā, programmas datu bāzē tiek izveidota jauna pagaidu tabula, šajā tabulā tiek ievietoti uzkrātie atmiņas ierakstu identifikācijas kodi, un tiek ģenerēts šāds SQL izraksts, lai atgrieztu filtrētus ierakstus **Intrastat** tabulā.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Papildu resursi

[Loģiskās funkcijas](er-functions-category-logical.md)

[VALUEIN funkcijas](er-functions-logical-valuein.md)
