---
title: FA_SUM ER funkcija
description: Šajā rakstā ir sniegta informācija par FA_SUM funkciju Elektroniskie pārskati (ER).
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
ms.openlocfilehash: bcedbc3df835b219b8df6d05f1db6b331f1e9254
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278923"
---
# <a name="fa_sum-er-function"></a>FA_SUM ER funkcija

[!include [banner](../includes/banner.md)]

`FA_SUM` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas sastāv no pamatlīdzekļa summu datiem par norādīto pamatlīdzekļa krājumu, vērtības modeļa kodu, pārskata gadu un datumu periodu.

## <a name="syntax"></a>Sintakse

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumenti

`fixed asset code`: *Virkne*

*Virknes* vērtība, kas apzīmē pamatlīdzekļu krājuma kodu, kuram tiek aprēķināta bilance.

`value model code`: *Virkne*

*Virknes* vērtība, kas apzīmē vērtības modeļa kodu, kuram tiek aprēķināta bilance.

`start date`: *Datums*

*Datuma* vērtība, kas apzīmē sākuma datumu periodam, kuram tiek aprēķinātas pamatlīdzekļu summas.

`end date`: *Datums*

*Datuma* vērtība, kas apzīmē beigu datumu periodam, kuram tiek aprēķinātas pamatlīdzekļu summas.

## <a name="return-values"></a>Atgrieztās vērtības

*Konteiners (ieraksts)*

Iegūtā ieraksta vērtība.

## <a name="example"></a>Paraugs

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` atgriež pamatlīdzekļa **COMP-000001** datu konteineru, kas ir sagatavots **Pašreizējam** vērtības modelim un periodam no **Date1** līdz **Date2**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
