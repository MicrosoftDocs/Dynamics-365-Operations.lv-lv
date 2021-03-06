---
title: DATETODATETIME ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota DATETODATETIME elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/04/2019
ms.topic: article
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
ms.openlocfilehash: bb90c58544eeba804cd39542cc70fab3b840af80
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746967"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME ER funkcija

[!include [banner](../includes/banner.md)]

`DATETODATETIME` funkcija atgriež *DateTime* vērtību, kas tiek konvertēta no konkrētā datuma vērtības uz datuma/laika vērtību pēc universālā koordinētā laika (Griničas laika \[GMT\]).

## <a name="syntax"></a>Sintakse

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a>Argumenti

`date`: *Datums*

Datuma/laika vērtība, kas apzīmē konvertējamo datumu.

## <a name="return-values"></a>Atgrieztās vērtības

*DateTime*

Iegūtā datuma/laika vērtība.

## <a name="example-1"></a>1. piemērs

`DATETODATETIME (CompInfo. 'getCurrentDate()')` atgriež pašreizējās Microsoft Dynamics 365 Finance sesijas datumu, 2015. gada 24. decembri, kā **12/24/2015 12:00:00 AM.** Šajā piemērā **CompInfo** ir elektronisko pārskatu (ER) datu avots ar veidu **Finance and Operations/Table**, un tas atsaucas uz tabulu CompanyInfo.

## <a name="example-2"></a>2. piemērs

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` atgriež datuma/laika vērtību **11/12/2019 12:00:00 AM**.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]