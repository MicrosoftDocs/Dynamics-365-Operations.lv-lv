---
title: CONVERTCURRENCY ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota funkcija CONVERTCURRENCY Elektroniskie pārskati (ER).
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: ac9a1cbb1c0a4b381a4e268f563c6ab0dd9c8053
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275518"
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
