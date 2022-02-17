---
title: Funkcija GETLABELTEXT ER
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota funkcija GETLABELTEXT Elektroniskā ziņošana (ER).
author: NickSelin
ms.date: 01/04/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 911567a94b80c2b762a37e83d37fc500132edb18
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075749"
---
# <a name="getlabeltext-er-function"></a>Funkcija GETLABELTEXT ER

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

The`GETLABELTEXT` funkcija meklē konkrētu etiķeti, lai atgrieztu a *[Stīga](er-formula-supported-data-types-primitive.md#string)* vērtība, kas apzīmē norādītās etiķetes tulkojumu norādītajā valodā.

## <a name="syntax"></a>Sintakse

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumenti

### <a name="label-id"></a>Etiķetes kods

`label id`:*Stīga* vai *Etiķetes ID*

Derīgs ID vienam no šiem etiķešu veidiem:

- [Elektroniskā ziņošana (ER)](general-electronic-reporting.md) etiķete
- Microsoft Dynamics 365 Finance etiķete

#### <a name="usage-notes"></a>Lietošanas piezīmes

Šo argumentu var definēt tikai kā konstanti, izmantojot vienu no šiem atbalstītajiem modeļiem:

- ER etiķetēm:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finanšu etiķetēm:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Projektēšanas laikā uz ekrāna tiek parādīts validācijas kļūdas ziņojums **[Formulas dizainers](er-advanced-formula-editor.md)** lapu, ja, izmantojot norādīto etiķetes ID, nevar atrast etiķeti.

### <a name="language"></a>Valoda

`language`: *Virkne*

Virkne, kas apzīmē valodas kodu.

#### <a name="usage-notes"></a>Lietošanas piezīmes

Šo argumentu var definēt kā teksta konstanti vai kā datu avota lauka ceļu, kas atgriež a *Stīga* vērtību.

> [!NOTE]
> Projektēšanas laikā tiek parādīts validācijas kļūdas ziņojums, ja, izmantojot piedāvāto, nevar atrast valodas kodu`language` argumentu, ja tas ir definēts kā teksta konstante.
>
> Izpildlaikā tulkojums`EN-US` sistēmas valoda tiek atgriezta noteiktai etiķetei, ja, izmantojot norādīto, nav atrasts valodas kods`language` arguments.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example-1-system-label"></a><a name=example-1></a> 1. piemērs: sistēmas etiķete

Izteicieni`GETLABELTEXT (@"SYS70894", "en-us")` un`GETLABELTEXT ("SYS70894", "en-us")` atgriezt angļu valodas tulkojumu "Nothing to print" par`@SYS70894` lietojumprogrammas etiķete.

## <a name="example-2-er-label"></a><a name=example-2></a> 2. piemērs: ER etiķete

Jūs sākat rediģēt ER [konfigurācija](general-electronic-reporting.md#Configuration) tas ir bijis [atvasināts](er-quick-start2-customize-report.md#DeriveProvidedFormat) no **ISO20022 kredīta pārvedums (DE)** konfigurāciju, ievadiet jaunu datu avotu *[Aprēķināts lauks](er-calculated-field-ds-performance.md)* ierakstiet un konfigurējiet izteiksmi`GETLABELTEXT(@"GER_LABEL:VendorName", "de")` šim datu avotam. Šajā gadījumā izpildes laikā datu avots atgriež vācu valodas tulkojumu "Kreditorenname".`@GER_LABEL:VendorName` ER etiķete, kas sākotnēji tika konfigurēta bāzē **ISO20022 kredīta pārvedums (DE)** ER konfigurācija.

## <a name="additional-resources"></a>Papildu resursi

[Teksta funkcijas](er-functions-category-text.md)

[Veidot daudzvalodu pārskatus Elektroniskajos pārskatos](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
