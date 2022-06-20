---
title: JSONVALUE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota JSONVALUE elektronisko pārskatu (ER) funkcija.
author: NickSelin
ms.date: 10/25/2021
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
ms.openlocfilehash: 7deaed83959f033d11333efb5a2b398cbe57076d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909505"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE ER funkcija

[!include [banner](../includes/banner.md)]

`JSONVALUE` funkcija parsē datus formātā JavaScript Object Notation (JSON), kuriem piekļūst pa norādīto ceļu un izgūst skalāru vērtību, kas ir balstīta uz norādīto ID. Pēc tam tā atgriež izvērsto skalāro vērtību kā *Virknes* vērtību.

## <a name="syntax"></a>Sintakse

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenti

`input`: *Virkne*

*Virknes* tipa datu avota derīgs ceļš, kas satur JSON datus.

`path`: *Virkne*

Skalārās JSON datu vērtības identifikators. Izmantojiet slīpsvītru (/), lai atdalītu saistīto JSON zaru nosaukumus. Lai norādītu noteiktas vērtības indeksu JSON masīvā, lietojiet iekavu (\[\]) notāciju. Ņemiet vērā, ka šim indeksam tiek izmantota nulles numura numerācija.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example-1"></a>1. piemērs

Datu avotā **JsonField** ir ietverti tālāk norādītie dati JSON formātā: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. Šādā gadījumā izteiksme `JSONVALUE (JsonField, "BuildNumber")` atgriež šādu vērtību *Virknes* datu tipam: **"7.3.1234.1".**

## <a name="example-2"></a>2. piemērs

Ievadāt datu avotu **JsonField** no veida *Aprēķinātais lauks*, un tas satur šādu izteiksmi: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Šī izteiksme ir konfigurēta, lai atgrieztu [*Virknes*](er-formula-supported-data-types-primitive.md#string) vērtību, kas attēlo tālāk norādītos datus JSON formātā.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

Šādā gadījumā izteiksme `JSONVALUE(json, "workers/[1]/emails/[0]")` atgriež šādu vērtību *Virknes* datu tipam: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
