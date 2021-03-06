---
title: STARTSWITH ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota STARTSWITH elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048846"
---
# <a name="startswith-er-function"></a>STARTSWITH ER funkcija

[!include [banner](../includes/banner.md)]

`STARTSWITH` funkcija nosaka, vai norādītā ievade sākas ar norādīto tekstu. Tā atgriež *Būla* vērtību **PATIESS**, ja norādītā ievade sākas ar norādīto tekstu. Pretējā gadījumā tā atgriež *Būla* vērtību **FALSE**.

## <a name="syntax"></a>Sintakse

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Argumenti

`input`: *Virkne*

Veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var sākties ar otro argumentu.

`start text`: *Virkne*

Datu veida *Virkne* datu avotu elementa vai virknes konstantes derīgais ceļš, kura vērtība var būt pirmā argumenta sākumā.

## <a name="return-values"></a>Atgrieztās vērtības

*Būla*

Iegūtā *Būla* vērtība.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šo funkciju var izmantot funkcijas [FILTER](er-functions-list-filter.md) nosacījuma izteiksmes norādīšanai tikai tad, ja atbilstošā kartēšana ir konfigurēta [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md), lai piekļūtu [Microsoft Dataverse](/power-platform/admin/data-integrator). Pretējā gadījumā izstrādes laikā tiek izmests izņēmums. Saņemtais ziņojums iesaka izmantot funkciju [WHERE](er-functions-list-where.md), nevis funkciju `FILTER`.

## <a name="example-1"></a>1. piemērs

Izteiksme `STARTSWITH ("abc", "d")` atgriež **APLAMS**, savukārt izteiksme `STARTSWITH ("abc", "A")` atgriež **PATIESS**.

## <a name="example-2"></a>2. piemērs

Izteiksme `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` atgriež **PATIESS**, ja datu avota **modelis** lauka **Adrese** vērtība sākas ar virkni **123 Coffee Street**. Pretējā gadījumā tā atgriež vērtību **FALSE**.

## <a name="additional-resources"></a>Papildu resursi

[Loģiskās funkcijas](er-functions-category-logical.md)
