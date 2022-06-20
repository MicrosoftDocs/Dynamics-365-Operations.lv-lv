---
title: DAYS ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija DIENAS elektroniskie pārskati (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 41a324ca93497f8b297c8c944f622b7829f1ceff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881230"
---
# <a name="days-er-function"></a>DAYS ER funkcija

[!include [banner](../includes/banner.md)]

`DAYS` funkcija atgriež *Vesela skaitļa* vērtību, kas reprezentē dienu skaitu no viena norādītā datuma līdz otram norādītajam datumam.

## <a name="syntax"></a>Sintakse

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumenti

`date 1`: *Datums*

Datuma vērtība, kas apzīmē sākuma datumu, kas jāizmanto, aprēķinot dienu skaitu.

`date 2`: *Datums*

Datuma vērtība, kas apzīmē beigu datumu, kas jāizmanto, aprēķinot dienu skaitu.

## <a name="return-values"></a>Atgrieztās vērtības

*Vesels skaitlis*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

`DAYS` funkcija atgriež pozitīvu vērtību, ja pirmais datums ir vēlāks par otro datumu; tiek atgriezta **0** (nulle), ja pirmais datums ir vienāds ar otro; vai tiek atgriezta negatīva vērtība, ja pirmais datums ir agrāks par otro datumu.

## <a name="example"></a>Paraugs

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` atgriež **-1**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]