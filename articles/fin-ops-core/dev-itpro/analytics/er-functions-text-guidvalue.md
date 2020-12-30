---
title: GUIDVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GUIDVALUE elektroniskā pārskata (ER) funkcija.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685958"
---
# <a name="guidvalue-er-function"></a>GUIDVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`GUIDVALUE` funkcija konvertē norādīto *Virknes* veidu uz datu elementu ar datu veidu *GUID*.

## <a name="syntax"></a>Sintakse

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumenti

`input`: *Virkne*

*Virknes* tipa datu avota datu tipa derīgs ceļš.

## <a name="return-values"></a>Atgrieztās vērtības

*GUID*

Iegūtā globāli unikālā identifikatora (GUID) vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Lai veiktu konvertēšanu pretējā virzienā (tas ir, lai norādīto ievadi ar datu tipu *GUID* konvertētu uz datu elementu ar datu tipu *Virkne* ), varat izmantot funkciju [TEXT](er-functions-text-text.md).

## <a name="example"></a>Paraugs

Savā modeļa kartēšanā jūs definējat tālāk norādītos datu avotus.

- Datu avots **myID** no veida *Aprēķinātais lauks*, kas satur izteiksmi `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- **Users** datu avots no veida *Tabulas ieraksti*, kas atsaucas uz tabulu UserInfo

Pēc tam varat izmantot izteiksmi, piemēram, `FILTER (Users, Users.objectId = myID)`, lai filtrētu tabulu UserInfo pēc lauka **objectId** ar datu tipu *GUID.*

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
