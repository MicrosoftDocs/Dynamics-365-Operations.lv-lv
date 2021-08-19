---
title: TEXT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TEXT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 38550b8b5181b49bcb8504129932f185ea95e038e38d4581bc3e0fa076f4fb50
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762456"
---
# <a name="text-er-function"></a>TEXT ER funkcija

[!include [banner](../includes/banner.md)]

`TEXT` funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tā ir pārveidota par teksta virkni, kura ir formatēta atbilstoši pašreizējās programmas instances servera lokalizācijas iestatījumiem.

## <a name="syntax"></a>Sintakse

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumenti

`number`: *Vesels skaitlis* vai *Reāls*

Skaitlis, kas ir jāpārvērš par teksta virkni.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Vērtībām ar tipu *Reāls* šīs virknes pārveidošana ir ierobežota līdz diviem cipariem aiz komata.

## <a name="example"></a>Paraugs

Ja Microsoft Dynamics 365 Finance instances servera lokalizācija ir definēta kā **EN-US**, `TEXT (NOW ())` pašreizējo Finance sesijas datumu, 2015. gada 17. decembri, atgriež kā teksta virkni **"12/17/2015 07:59:23 AM"**. `TEXT (1/3)` atgriež **"0.33"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]