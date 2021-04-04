---
title: INT64VALUE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota INT64VALUE elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 9db2e9abcac36a8331a494c886218bbfc82e93aa
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561498"
---
# <a name="int64value-er-function"></a>INT64VALUE ER funkcija

[!include [banner](../includes/banner.md)]

`INT64VALUE` funkcija atgriež *Int64* vērtību, kas apzīmē norādīto virkni.

## <a name="syntax-1"></a>Sintakse 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Sintakse 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumenti

`text`: *Virkne*

Teksta vērtība, kas ir jāpārvērš par *Int64* skaitli.

`number`: *Reāls* vai *Vesels skaitlis*

Skaitliska *Reālā* vai *Veselā skaitļa* vērtība , kas ir jāpārvērš par *Int64* skaitli.

## <a name="return-values"></a>Atgrieztās vērtības

*Int64*

Iegūtā skaitliskā vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Tiek aprautas visas decimāldaļas.

## <a name="example-1"></a>1. piemērs

`INT64VALUE ("22565422744")` atgriež *Int64* vērtību **22565422744**.

## <a name="example-2"></a>2. piemērs

`INT64VALUE ( VALUE("22565422744.77"))` atgriež *Int64* vērtību **22565422744**.

## <a name="additional-resources"></a>Papildu resursi

[Tipa pārveidošanas funkcijas](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]