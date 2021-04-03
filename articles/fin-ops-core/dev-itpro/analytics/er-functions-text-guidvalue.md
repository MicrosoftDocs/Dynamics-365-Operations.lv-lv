---
title: GUIDVALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota GUIDVALUE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 552c6a42dd0e189f2f8404ce5d7f7a68fec1b216
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564342"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]