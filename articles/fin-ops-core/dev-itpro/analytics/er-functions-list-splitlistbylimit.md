---
title: SPLITLISTBYLIMIT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota SPLITLISTBYLIMIT elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 5bf13b7c1e7cab7c803b352370084421a8180dee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743440"
---
# <a name="splitlistbylimit-er-function"></a>SPLITLISTBYLIMIT ER funkcija

[!include [banner](../includes/banner.md)]

`SPLITLISTBYLIMIT` funkcija sadala norādīto sarakstu jaunā apakšsaraksta (partiju) sarakstā. Katras partijas ierakstu skaits tiek aprēķināts dinamiski. Pēc tam funkcija atgriež rezultātu kā jaunu *Ierakstu saraksta* vērtību, kas sastāv no partijām.

## <a name="syntax"></a>Sintakse

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`limit value`: *Vesels skaitlis* vai *Reāls*

Maksimālā robežvērtība, kas tiek izmantota, lai sadalītu sākotnējo sarakstu partijās.

`limit source`: *Lauks*

Derīgs ceļš laukam no veida *Vesels skaitlis* vai *Reāls* norādītajā sarakstā. Šī lauka vērtība nosaka darbību, kurā tiek palielināta kopējā summa.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Atgriezts partiju saraksts satur šādus elementus:

- **Vērtība:**: *Saraksts*

    To ierakstu saraksts, kas pieder pašreizējai partijai.

- **BatchNumber**: *Vesels skaitlis*

    Pašreizējās partijas numurs atgrieztajā sarakstā.

Ierobežojums netiek lietots atsevišķam vienumam attiecīgajā sarakstā, ja ierobežojuma avots pārsniedz definēto ierobežojumu.

## <a name="example"></a>Paraugs

Šajā attēlā ir parādīts elektronisko pārskatu (ER) formāts.

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

Nākamajā attēlā ir parādīti datu avoti, kas tiek izmantoti šim formātam.

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

Tālāk esošajā attēlā parādīts rezultāts pēc formāta palaišanas. Šajā gadījumā izvade ir nekārtots preču saraksts.

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

Nākamajos attēlos tas pats formāts ir pielāgots tā, lai preču sarakstu rādītu pa partijām, ja vienā partijā jāietver preces un nevar pārsniegt kopējā svara ierobežojumu 9.

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

Tālāk esošajā attēlā parādīts rezultāts pēc pielāgotā formāta palaišanas.

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> Ierobežojums netiek lietots pēdējam sākotnējā saraksta vienumam, jo ierobežojuma avota (**svara**) vērtība (**11**) pārsniedz noteikto ierobežojumu (**9**). Lai pārskata ģenerēšanas laikā ignorētu apakšsarakstus, izmantojiet vai nu funkciju `WHERE`, vai izteiksmi **Iespējots** no atbildstošā formāta elementa pēc jūsu nepieciešamības.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)
