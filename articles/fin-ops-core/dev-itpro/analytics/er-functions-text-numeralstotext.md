---
title: NUMERALSTOTEXT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NUMERALSTOTEXT elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31fd4076d04ce7d849555bc8301c4d23ad8e1a7e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041015"
---
# <a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER funkcija</a>

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

Valodas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantots izpildes konteksta valodas kods. Noklusējuma valodas kods ir **EN-US**. Valodas kods darbības kontekstam ir definēts tā elektroniskā pārskata (ER) vienumā  **Mape** vai **Fails**, formātā, kas tiek izpildīts.

Valūtas kods nav obligāts. Ja tas ir definēts kā tukša virkne, tiek izmantota izpildes konteksta uzņēmuma valūta.

> [!NOTE] 
> Argumenti `print currency name flag` un `decimal points` tiek analizēti tikai šādiem valodu kodiem:  **CS**, **ET**, **HU**, **LT**, **LV**, **PL** un **RU**. Turklāt arguments `print currency name flag` tiek analizēts tikai tiem uzņēmumiem, kuru valsts vai reģiona konteksts atbalsta valūtu nosaukumu locījumus.

## <a name="example-1"></a>1. piemērs

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)`atgriež **"One Thousand Two Hundred Thirty Four and 56"**.

## <a name="example-2"></a>2. piemērs

`NUMERALSTOTEXT (120, "PL", "", false, 0)`atgriež **"Sto dwadzieścia"**. 

## <a name="example-3"></a>3. piemērs

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)`atgriež **"Сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)
