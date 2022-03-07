---
title: CONTAINS ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota CONTAINS elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048874"
---
# <a name="contains-er-function"></a>CONTAINS ER funkcija

[!include [banner](../includes/banner.md)]

`CONTAINS` funkcija nosaka, vai norādītā ievade satur norādīto tekstu. Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade satur norādīto tekstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.

## <a name="syntax"></a>Sintakse

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumenti

`input`: *Virkne*

Veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var saturēt otro argumentu.

`search text`: *Virkne*

Datu veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var būt ietverta pirmajā argumentā.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šo funkciju var izmantot funkcijas [FILTER](er-functions-list-filter.md) nosacījuma izteiksmes norādīšanai tikai tad, ja atbilstošā kartēšana ir konfigurēta [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md), lai piekļūtu [Microsoft Dataverse](/power-platform/admin/data-integrator). Pretējā gadījumā izstrādes laikā tiek izmests izņēmums. Saņemtais ziņojums iesaka izmantot funkciju [WHERE](er-functions-list-where.md), nevis funkciju `FILTER`.

## <a name="example-1"></a>1. piemērs

Izteiksme `CONTAINS ("abc", "d")` atgriež **APLAMS**, savukārt izteiksme `CONTAINS ("abc", "C")` atgriež **PATIESS**.

## <a name="example-2"></a>2. piemērs

Izteiksme `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` atgriež **PATIESS**, ja datu avota **modelis** lauka **Adrese** vērtība ietver virkni **DEU**. Pretējā gadījumā tā atgriež vērtību **FALSE**.

## <a name="additional-resources"></a>Papildu resursi

[Loģiskās funkcijas](er-functions-category-logical.md)
