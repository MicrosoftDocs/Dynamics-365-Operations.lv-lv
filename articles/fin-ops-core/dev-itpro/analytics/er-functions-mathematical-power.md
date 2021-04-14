---
title: POWER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota POWER elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750160"
---
# <a name="power-er-function"></a>POWER ER funkcija

[!include [banner](../includes/banner.md)]

`POWER` funkcija atgriež *Reālu* vērtību, kas atspoguļo rezultātu norādītā pozitīvā skaitļa palielināšanai līdz norādītajai jaudai.

## <a name="syntax"></a>Sintakse

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumenti

`number`: *Reāls* vai *Vesels skaitlis*

Skaitliska vērtība, kas ir jāpaaugstina līdz norādītajai jaudām.

`power`: *Reāls* vai *Vesels skaitlis*

Skaitliska vērtība, kas apzīmē konkrēto jaudu.

## <a name="return-values"></a>Atgrieztās vērtības

*Reāls*

Iegūtā skaitliskā vērtība.

## <a name="example-1"></a>1. piemērs

`POWER (10, 2)` atgriež **100**.

## <a name="example-2"></a>2. piemērs

`POWER (4, 0.5)` atgriež **2**.

## <a name="additional-resources"></a>Papildu resursi

[Matemātiskās funkcijas](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]