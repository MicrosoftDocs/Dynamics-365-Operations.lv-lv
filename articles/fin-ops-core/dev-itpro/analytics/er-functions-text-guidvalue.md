---
title: GUIDVALUE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota GUIDVALUE elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cb706a3607b4443c283a91c42c4dc1c389972e44
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285191"
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
