---
title: CONVERTCURRENCY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CONVERTCURRENCY elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: dc71ccedcdfc8a3dc9d7e087d29467bd3bbe72c3c5588872dbeaf3aa1dd35d2b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738604"
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