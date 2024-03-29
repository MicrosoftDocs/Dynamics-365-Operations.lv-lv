---
title: NUMERALSTOTEXT ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek lietota funkcija NUMERALSTOTEXT Electronic reporting (ER).
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287994"
---
# <a name="numeralstotext-er-function"></a>NUMERALSTOTEXT ER funkcija

[!include [banner](../includes/banner.md)]

`NUMERALSTOTEXT` funkcija atgriež norādīto skaitli kā *Virknes* vērtību pēc tam, kad tas ir uzrakstīts (tas ir, konvertēts teksta virknēs) norādītajā valodā.

## <a name="syntax"></a>Sintakse

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumenti

`number`: *Vesels skaitlis* vai *Reāls*

Skaitliska vērtība, kas norāda skaitli, kas ir jāizburto.

`language`: *Virkne*

*Virknes* vērtība, kas apzīmē valodas kodu.

`currency`: *Virkne*

*Virknes* vērtība, kas apzīmē valūtas kodu.

`print currency name flag`: *Būla*

*Būla* vērtība, kas norāda, vai uzrakstam ir jāpievieno valūtas nosaukums.

`decimal points`: *Vesels skaitlis*

*Vesela skaitļa* vērtība, kas norāda ciparu aiz komata skaitu, kuram vajadzētu būt uzrakstā.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Valodas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantots izpildes konteksta valodas kods. Noklusējuma valodas kods ir **EN-US**. Valodas kods darbības kontekstam ir definēts tā elektroniskā pārskata (ER) vienumā **Mape** vai **Fails**, formātā, kas tiek izpildīts.

Valūtas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantota izpildes konteksta uzņēmuma valūta.

> [!NOTE] 
> Argumenti `print currency name flag` un `decimal points` tiek analizēti tikai šādiem valodu kodiem: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** un **RU**. Turklāt arguments `print currency name flag` tiek analizēts tikai tiem uzņēmumiem, kuru valsts vai reģiona konteksts atbalsta valūtu nosaukumu locījumus.

## <a name="example-1"></a>1. piemērs

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` atgriež **"One Thousand Two Hundred Thirty Four and 56"**.

## <a name="example-2"></a>2. piemērs

`NUMERALSTOTEXT (120, "PL", "", false, 0)` atgriež **"Sto dwadzieścia"**. 

## <a name="example-3"></a>3. piemērs

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` atgriež **"Сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
