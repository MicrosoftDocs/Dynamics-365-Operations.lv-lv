---
title: CONVERTCURRENCY ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota funkcija CONVERTCURRENCY Elektroniskie pārskati (ER).
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: e51086d977652e4be4c19390a824d4f4507b60d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898467"
---
# <a name="convertcurrency-er-function"></a>CONVERTCURRENCY ER funkcija

[!include [banner](../includes/banner.md)]

`CONVERTCURRENCY` funkcija atgriež *Reālu* vērtību, kas apzīmē rezultātu norādītas naudas summas konvertēšanai no norādītās avota valūtas norādītajā mērķa valodā, izmantojot norādītā uzņēmuma iestatījumus norādītajā datumā.

## <a name="syntax"></a>Sintakse

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumenti

`amount`: *Vesels skaitlis* vai *Reāls*

Skaitliska vērtība, kas apzīmē naudas summu, kura ir jākonvertē.

`source currency`: *Virkne*

Avota valūtas kods.

`target currency`: *Virkne*

Mērķa valūtas kods.

`date`: *Datums*

*Datuma* vērtība, kas apzīmē datumu, kas tiek izmantots, lai noteiktu konversijas valūtas kursu.

`company`: *Virkne*

*Virknes* vērtība, kas apzīmē tā uzņēmuma kodu, kurš nodrošina konversijai izmantotos iestatījumus.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="example"></a>Paraugs

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` atgriež viena eiro ekvivalentu ASV dolāros pašreizējās sesijas datumā, balstoties uz uzņēmuma **DEMF** iestatījumiem.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]