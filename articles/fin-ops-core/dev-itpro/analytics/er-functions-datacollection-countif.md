---
title: COUNTIF ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija COUNTIF Elektroniskie pārskati (ER).
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 60a17d6a5e089cc6006a5fb3493654963de1b392
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906863"
---
# <a name="countif-er-function"></a>COUNTIF ER funkcija

[!include [banner](../includes/banner.md)]

`COUNTIF` funkcija atgriež *Vesela skaitļa* vērtību, kas apzīmē to formātu elementu skaitu, kuri tika savākti, kad formāta elementi tika izmantoti, lai ģenerētu izejošo dokumentu formāta izpildes laikā un kas atbilst norādītajam nosacījumam. Nosacījums sastāv no atslēgu diapazona un atslēgas vērtības.

## <a name="syntax"></a>Sintakse

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Argumenti

`condition range`: *Virkne*

Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta elektronisko pārskatu (ER) formāta komponenta rekvizītā **Ievāktais datu atslēgas nosaukums**.

`condition value`: *Virkne*

Vērtība, ko atgriež izteiksme, kura ir konfigurēta komponenta ER formāta komponenta rekvizītā **Ievāktā datu atslēgas vērtība**.

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Rekvizītus **Ievāktās datu atslēgas nosaukums** un **Ievāktā datu atslēgas vērtība** var konfigurēt vainu komponentā **Secība** vai komponentā **XML elements** ER formātā, kas atrodas zem komponenta **Vispārīgi\\Fails**, kur ir ieslēgta opcija **Ievākt detalizētu informāciju par izvadi**.

Šī funkcija atgriež **0** (nulles) vērtību, ja pašreizējā komponenta **Vispārīgi\\Fails** opcija **Apkopot izvades informāciju** ir izslēgta.

`condition range` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.

`condition value` argumentā aizstājējzīmi **"\*"** var izmantot, lai attēlotu jebkādas vairākas rakstzīmes.

## <a name="example"></a>Paraugs

Lai uzzinātu vairāk par šīs funkcijas lietojumu, skatiet uzdevuma ceļvedi [ER Lietot formāta izvades datus uzskaitei un summēšanai](tasks/er-format-counting-summing-1.md), kas ir daļa no biznesa procesa **Iegūt/izstrādāt IT pakalpojumu/risinājuma komponentus**.

## <a name="additional-resources"></a>Papildu resursi

[Datu apkopošanas funkcijas](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]