---
title: TODAY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota TODAY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 9288baf4e6123a7c03152f524a852eae9b671dde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567920"
---
# <a name="today-er-function"></a>TODAY ER funkcija

[!include [banner](../includes/banner.md)]

`TODAY` funkcija atgriež *Datuma* vērtību, kas apzīmē pašreizējo lietojumprogrammu servera datumu.

## <a name="syntax"></a>Sintakse

```xpp
TODAY ()
```

## <a name="return-values"></a>Atgrieztās vērtības

*Datums*

Iegūtā datuma vērtība.

## <a name="example"></a>Paraugs

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` pašreizējās programmas servera datumu/vērtību, 2015. gada 24. decembri, atgriež kā virkni **"24-12-2015"** atbilstoši norādītajam pielāgotajam formātam.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]