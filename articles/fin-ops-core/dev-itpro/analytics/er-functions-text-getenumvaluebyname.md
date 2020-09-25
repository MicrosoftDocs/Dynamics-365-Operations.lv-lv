---
title: GETENUMVALUEBYNAME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GETENUMVALUEBYNAME elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743859"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER funkcija

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` funkcija meklē konkrētu *Enum* vērtību norādītajā uzskaitījuma datu avotā, izmantojot uzskaitījuma nosaukumu, kas ir norādīts kā *Virknes* vērtība. Ja tiek tiek atrasta *Enum* vērtība, funkcija to atgriež. Pretējā gadījumā funkcija atgriež uzskaitījuma vērtību **null**.

## <a name="syntax"></a>Sintakse

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Argumenti

`enumeration data source path`: *Uzskaitījums*

Derīgs datu avota atsauces ceļš vienam no šādiem uzskaitījumu tipiem:

- Elektronisko pārskatu (ER) modeļu uzskaitījums
- ER formāta uzskaitījums
- Microsoft Dynamics 365 Finance uzskaitījums

`enumeration value text`: *Virkne*

Virknes vērtība, kas apzīmē vienas uzskaitījuma vērtības nosaukumu.

## <a name="return-values"></a>Atgrieztās vērtības

Nullējama *Enum*

Iegūtā uzskaitījuma vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Netiek rādīts izņēmums, ja *Enum* vērtība nav atrasta, izmantojot uzskaitījuma vērtības nosaukumu, kas ir norādīts kā *Virknes* vērtība.

## <a name="example"></a>Paraugs

Tālāk esošajā attēlā ir parādīts datu modelī ieviests uzskaitījums **ReportDirection**. Ņemiet vērā, ka etiķetes ir definētas uzskaitījumu vērtībām.

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

Tālāk esošajā attēlā parādīta tālāk uzskaitītā informācija.

- **$Direction** datu avots ir konfigurēts ER pārskatā. Šis datu avots ir konfigurēts, pamatojoties uz modeļa uzskaitījumu **ReportDirection**.
- Izteiksme `$IsArrivals` ir izveidota ar mērķi lietot modeļa uzskaitījumā bāzētu datu avotu **$Direction** kā šīs funkcijas parametru.
- Šīs salīdzinājuma izteiksmes vērtība ir **TRUE**.

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
