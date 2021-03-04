---
title: CASE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CASE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 69b76a06bcd3ba002d9543447e60afa14d5a6ce6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687030"
---
# <a name="case-er-function"></a>CASE ER funkcija

[!include [banner](../includes/banner.md)]

`CASE` funkcija novērtē norādītās izteiksmes vērtību pret norādītajām alternatīvajām opcijām un atgriež pirmās opcijas, kas ir vienāda ar norādītās izteiksmes vērtību, rezultātu. Pretējā gadījumā tas atgriež neobligātu noklusējuma rezultātu, ja noklusējuma rezultāts ir norādīts kā pēdējās funkcijas izsauktais arguments, pirms kura neatrodas opcija. Atgrieztā vērtība var būt jebkura atbalstītā datu tipa vērtība.

## <a name="syntax"></a>Sintakse

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumenti

`expression`: *Primitīvs datu tips* (Būla, skaitlisks vai teksta)

Derīga izteiksme, kas atgriež vērtību no primitīva datu tipa.

`option 1`: *Primitīvs datu tips* (Būla, skaitlisks vai teksta)

Derīga izteiksme, kas atgriež vērtību no tā paša primitīva datu tipa kā izsauktās `expression` funkcijas argumentu. Šis arguments ir obligāts.

`result 1`: *Jebkurš no atbalstītajiem datu tipiem*

Atgrieztais rezultāts, kas atbilst iepriekšējai opcijai. Šis arguments ir obligāts.

`option N`: *Primitīvs datu tips* (Būla, skaitlisks vai teksta)

Derīga izteiksme, kas atgriež vērtību no tā paša primitīva datu tipa kā izsauktās `expression` funkcijas argumentu. ŠIs arguments nav obligāts.

`result N`: *Jebkurš no atbalstītajiem datu tipiem*

Atgrieztais rezultāts, kas atbilst iepriekšējai opcijai. ŠIs arguments nav obligāts.

`default result`: *Jebkurš no atbalstītajiem datu tipiem*

Rezultāts, kas ir jāatgriež, ja nav atbilstības. ŠIs arguments nav obligāts.

## <a name="return-values"></a>Atgrieztās vērtības

*Jebkurš no atbalstītajiem datu tipiem*

Jebkura atbalstītā datu tipa iegūtā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Izņēmums tiek rādīts izpildlaikā, ja nav atbilstības un nav definēts izvēles noklusējuma rezultāts.

Visi rezultāti ir jānorāda, izmantojot vienu datu tipu. Noformēšanas laikā tiek parādīts izņēmums, ja konfigurēto rezultātu datu tipi nesakrīt.

Ja pirmā rezultāta vērtība un *N*-tā rezultāta vērtība ir *Konteinera (ieraksta)* vai *Ierakstu saraksta* datu tipa vērtības, rezultātam ir tikai tie lauki, kas ir abās vērtībās.

## <a name="example"></a>Paraugs

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` atgriež virkni **"WINTER"**, ja pašreizējās lietojumprogrammas sesijas datums ir no oktobra līdz decembrim. Pretējā gadījumā šī izteiksme atgriež tukšu virkni.

## <a name="additional-resources"></a>Papildu resursi

[Loģiskas funkcijas](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]