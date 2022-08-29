---
title: ENDSWITH ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota ENDSWITH elektronisko pārskatu (ER) funkcija.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 2608593238e5b2f738b452fb042837238f17e44e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271619"
---
# <a name="endswith-er-function"></a>ENDSWITH ER funkcija

[!include [banner](../includes/banner.md)]

`ENDSWITH` funkcija nosaka, vai norādītā ievade beidzas ar norādīto tekstu. Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade beidzas ar norādīto tekstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.

## <a name="syntax"></a>Sintakse

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Argumenti

`input`: *Virkne*

Veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var beigties ar otro argumentu.

`start text`: *Virkne*

Datu veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var būt pirmā argumenta beigās.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šo funkciju var izmantot funkcijas [FILTER](er-functions-list-filter.md) nosacījuma izteiksmes norādīšanai tikai tad, ja atbilstošā kartēšana ir konfigurēta [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md), lai piekļūtu [Microsoft Dataverse](/power-platform/admin/data-integrator). Pretējā gadījumā izstrādes laikā tiek izmests izņēmums. Saņemtais ziņojums iesaka izmantot funkciju [WHERE](er-functions-list-where.md), nevis funkciju `FILTER`.

## <a name="example-1"></a>1. piemērs

Izteiksme `ENDSWITH ("abc", "d")` atgriež **APLAMS**, savukārt izteiksme `ENDSWITH ("abc", "C")` atgriež **PATIESS**.

## <a name="example-2"></a>2. piemērs

Izteiksme `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` atgriež **PATIESS**, ja datu avota **modelis** lauka **Adrese** vērtība beidzas ar virkni **USA**. Pretējā gadījumā tā atgriež vērtību **FALSE**.

## <a name="additional-resources"></a>Papildu resursi

[Loģiskās funkcijas](er-functions-category-logical.md)
