---
title: MOD_97 ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota MOD_97 elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: b58e06a034fc6d26c891b78c26ac53c87a39b92b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744051"
---
# <a name="mod_97-er-function"></a>MOD_97 ER funkcija

[!include [banner](../includes/banner.md)]

`MOD_97` funkcija atgriež *Virknes* vērtību, kas apzīmē kreditora atsauci kā MOD97 izteiksmi, pamatojoties uz norādītā rēķina numura cipariem.

## <a name="syntax"></a>Sintakse

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a>Argumenti

`invoice number digits`: *Virkne*

Teksta vērtība, kas attēlo rēķina numura ciparus.

## <a name="return-values"></a>Atgrieztās vērtības

*Virkne*

Iegūtā teksta vērtība.

## <a name="example"></a>Paraugs

`MOD_97 ("VEND-200002")` atgriež **"20000285"**.

## <a name="additional-resources"></a>Papildu resursi

[Citas (biznesa jomai specifiskas) funkcijas](er-functions-category-other.md)
