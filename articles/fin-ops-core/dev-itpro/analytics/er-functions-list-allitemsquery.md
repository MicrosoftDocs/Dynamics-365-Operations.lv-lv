---
title: ALLITEMSQUERY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ALLITEMSQUERY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37546fccf804a4522638147d39206997e8c0c24c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745373"
---
# <a name="allitemsquery-er-function"></a>ALLITEMSQUERY ER funkcija

[!include [banner](../includes/banner.md)]

`ALLITEMSQUERY` funkcija darbojas kā apvienots SQL vaicājums. Tā atgriež jaunu izplātu *Ierakstu saraksta* vērtību, kas sastāv no ierakstu saraksta, kas apzīmē visus vienumus, kuri atbilst norādītajam ceļam.

## <a name="syntax"></a>Sintakse

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumenti

`path`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš. Tam jāsatur vismaz viena relācija.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Norādītais ceļš ir jādefinē kā derīgs datu avota ceļš datu avota elementam ar *Ierakstu saraksta* datu tipu. Tam arī jāsatur vismaz viena relācija. Tādiem datu elementiem kā *Virkne* un *Datums* elektronisko pārskatu (ER) izteiksmju veidotājā veidošanas laikā ir jāizraisa kļūda.

Ja šī funkcija tiek lietota datu tipa *Ierakstu saraksta* datu avotiem, kas attiecas uz programmas objektu, kuru var tieši izsaukt, izmantojot SQL (piemēram, tabulu, entītiju vai vaicājumu), tā darbojas kā savienots SQL vaicājums. Pretējā gadījumā tas darbojas atmiņā kā [ALLITEMS](er-functions-list-allitems.md) funkcija.

## <a name="example"></a>Paraugs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- **CustInv** datu avots no veida *Tabulas ieraksti*, kas atsaucas uz tabulu CustInvoiceTable
- Datu avots **Filteredinv** no veida *Aprēķinātais lauks*, kas satur izteiksmi `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- Datu avots **JourLines** no veida *Aprēķinātais lauks*, kas satur izteiksmi `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Kad palaižat modeļa kartēšanu, lai izsauktu datu avotu **JourLines**, tiek izpildīts tālāk norādītais SQL priekšraksts.

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)
