---
title: FA_BALANCE ER funkcija
description: Šajā rakstā sniegta informācija par to, FA_BALANCE tiek lietota elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: f9bb52643b60fd1b9423d798c08d731565c70f81
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285251"
---
# <a name="fa_balance-er-function"></a>FA_BALANCE ER funkcija

[!include [banner](../includes/banner.md)]

`FA_BALANCE` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas sastāv no pamatlīdzekļa bilances datiem par norādīto pamatlīdzekļa krājumu, vērtības modeļa kodu, pārskata gadu un pārskata datumu.

## <a name="syntax"></a>Sintakse

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumenti

`fixed asset code`: *Virkne*

*Virknes* vērtība, kas apzīmē pamatlīdzekļu krājuma kodu, kuram tiek aprēķināta bilance.

`value model code`: *Virkne*

*Virknes* vērtība, kas apzīmē vērtības modeļa kodu, kuram tiek aprēķināta bilance.

`reporting year`: *Uzskaitījuma vērtība*

Uzskaitījuma vērtība **AssetYear** lietojumprogrammu uzskaitījumam, kas nosaka periodu bilances aprēķinam.

`reporting date`: *Datums*

*Datuma* vērtība, kas definē bilances aprēķināšanas datumu.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners (ieraksts)*

Iegūtā ieraksta vērtība.

## <a name="example"></a>Paraugs

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` atgriež sagatavoto datu konteineru no bilancēm pamatlīdzeklim **COMP-000001** ar vērtības modeli **Pašreizējais** pašreizējā programmas sesijas datumā.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
