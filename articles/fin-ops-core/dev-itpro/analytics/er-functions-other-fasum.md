---
title: FA_SUM ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FA_SUM elektroniskā pārskata (ER) funkcija.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916986"
---
# <a name="FA_SUM">FA_SUM ER funkcija</a>

[!include [banner](../includes/banner.md)]

`FA_SUM` funkcija atgriež *Konteinera (ieraksta)* vērtību, kas sastāv no pamatlīdzekļa summu datiem par norādīto pamatlīdzekļa krājumu, vērtības modeļa kodu, pārskata gadu un datumu periodu.

## <a name="syntax"></a>Sintakse

```
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
