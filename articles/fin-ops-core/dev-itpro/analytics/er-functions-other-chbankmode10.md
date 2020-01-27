---
title: CH_BANK_MOD_10 funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CH_BANK_MOD_10 elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915882"
---
# <a name="CH_BANK_MOD_10">CH_BANK_MOD_10 funkcija</a>

[!include [banner](../includes/banner.md)]

`CH_BANK_MOD_10` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD10 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem.

## <a name="syntax"></a>Sintakse

```
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a>Argumenti

`invoice number digits`: *Virkne*

Teksta vērtība, kas attēlo rēķina numura ciparus.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`CH_BANK_MOD_10 ("VEND-200002")` atgriež **3**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)
