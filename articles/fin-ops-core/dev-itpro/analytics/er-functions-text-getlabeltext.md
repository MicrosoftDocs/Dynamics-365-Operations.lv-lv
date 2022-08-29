---
title: FUNKCIJA GETLABELTEXT ER
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija GETLABELTEXT Electronic reporting (ER).
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285945"
---
# <a name="getlabeltext-er-function"></a>FUNKCIJA GETLABELTEXT ER

[!include [banner](../includes/banner.md)]

Funkcija `GETLABELTEXT` meklē noteiktu iezīmi, lai atgrieztu *[Virknes](er-formula-supported-data-types-primitive.md#string)* vērtību, kas attēlo norādītās iezīmes tulkojumu norādītajā valodā.

## <a name="syntax"></a>Sintakse

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumenti

### <a name="label-id"></a>Etiķetes kods

`label id`: *virkne vai* iezīmes *ID*

Derīgais ID vienam no šiem iezīmju tipiem:

- [Elektronisko pārskatu (ER)](general-electronic-reporting.md) etiķete
- Microsoft Dynamics 365 Finanšu etiķete

#### <a name="usage-notes"></a>Lietošanas piezīmes

Šo argumentu var definēt tikai kā konstantu, izmantojot vienu no šiem atbalstītajiem rakstiem:

- ER etiķetēm:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finanšu iezīmēm:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Ja, izmantojot norādīto iezīmes **[...](er-advanced-formula-editor.md)** ID, izstrādes laikā formulas veidotāja lapā tiek rādīts apstiprināšanas kļūdas ziņojums.

### <a name="language"></a>Valoda

`language`: *Virkne*

Virkne, kas apzīmē valodas kodu.

#### <a name="usage-notes"></a>Lietošanas piezīmes

Šo argumentu var definēt kā teksta konstanti vai kā ceļu uz datu avota lauku, kas atgriež Virknes *vērtību*.

> [!NOTE]
> Izstrādes laikā tiek parādīts apstiprināšanas kļūdas `language` ziņojums, ja valodas kodu nevar atrast, izmantojot norādīto argumentu, ja tas definēts kā teksta konstante.
>
> Izpildlaikā sistēmas valodas tulkojums `EN-US` tiek atgriezts norādītajai iezīmei, ja valodas kods nav atrasts, izmantojot norādīto `language` argumentu.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example-1-system-label"></a><a name=example-1></a> 1. piemērs: sistēmas etiķete

Izteiksmes un tiek `GETLABELTEXT (@"SYS70894", "en-us")` atgriezts programmas iezīmes tulkojums `GETLABELTEXT ("SYS70894", "en-us")` "Nav ko drukāt`@SYS70894`".

## <a name="example-2-er-label"></a><a name=example-2></a> 2. piemērs: ER etiķete

Sākat rediģēt [ER](general-electronic-reporting.md#Configuration)[...](er-quick-start2-customize-report.md#DeriveProvidedFormat)**konfigurāciju, kas atvasināta no ISO20022 kredīta pārsūtīšanas (DE)** konfigurācijas, *[...](er-calculated-field-ds-performance.md)*`GETLABELTEXT(@"GER_LABEL:VendorName", "de")` ievadiet jaunu aprēķinātā lauka tipa datu avotu un konfigurējiet izteiksmi šim datu avotam. Šajā gadījumā izpildlaikā datu avots atgriež vācu tulkojumu "Kreditorenname" `@GER_LABEL:VendorName` ER **iezīmei, kas sākotnēji tika konfigurēta bāzes ISO20022 kredīta pārskaitījuma (DE)** ER konfigurācijā.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)

[Veidot daudzvalodu pārskatus Elektroniskajos pārskatos](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
