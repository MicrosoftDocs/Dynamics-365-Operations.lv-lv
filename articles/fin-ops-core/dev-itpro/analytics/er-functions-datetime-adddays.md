---
title: ADDDAYS ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota ADDDAYS Elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 7cf2031c042ae93512cc85afe6a1b51558f6c8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858746"
---
# <a name="adddays-er-function"></a>ADDDAYS ER funkcija

[!include [banner](../includes/banner.md)]

`ADDDAYS` funkcija aprēķina *DateTime* vērtību, kas ir norādītais dienu skaits pirms vai pēc norādītā sākuma datuma.

## <a name="syntax"></a>Sintakse

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumenti

`datetime`: *DateTime*

Datuma/laika vērtība, kas apzīmē sākuma datumu.

`days`: *Vesels skaitlis*

Dienu skaits pirms vai pēc `datetime`.

## <a name="return-values"></a>Atgrieztās vērtības

*DateTime*

Iegūtā datuma/laika vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Pozitīva vērtība `days` norāda uz nākotnes datumu. Negatīva vērtība norāda uz pagātnes datumu.

## <a name="example-1"></a>1. piemērs

`ADDDAYS (NOW(), 7)` atgriež datumu un laiku septiņas dienas uz priekšu.

## <a name="example-2"></a>2. piemērs

`ADDDAYS (NOW(), -3)` atgriež datumu un laiku trīs dienas pagātnē.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]