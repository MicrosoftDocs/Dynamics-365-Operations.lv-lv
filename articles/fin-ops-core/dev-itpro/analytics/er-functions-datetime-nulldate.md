---
title: NULLDATE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota NULLDATE elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 657766a838fbcd32c6b8bb0ba1f728e9dbbac92e103c219f3eeeab7ecd8c747d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749756"
---
# <a name="nulldate-er-function"></a>NULLDATE ER funkcija

[!include [banner](../includes/banner.md)]

`NULLDATE` funkcija atgriež *Datuma* vērtību, kas apzīmē **nulles** datumu (1900. gada 1. janvāris).

## <a name="syntax"></a>Sintakse

```vb
NULLDATE () as 
```

## <a name="return-values"></a>Atgrieztās vērtības

*Datums*

Iegūtā datuma vērtība.

## <a name="example-1"></a>1. piemērs

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` atgriež **nulles** datumu, 1900. gada 1. janvāri, kā **"1900-01-01"**, pamatojoties uz norādīto pielāgoto formātu.

## <a name="example-2"></a>2. piemērs

Izteiksme `IF( Invoice.DocumentDate = NULLDATE(), true, false)` atgriež **True**, ja lauka **DocumentDate** vērtība ir vienāda ar **nulles** datumu. Šajā piemērā **Rēķins** ir elektronisko pārskatu (ER) datu avots ar veidu **Finanšu/Tabulas ieraksti**, un tas atsaucas uz tabulu CustInvoiceJour.

## <a name="additional-resources"></a>Papildu resursi

[Datuma un laika funkcijas](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]