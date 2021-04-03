---
title: ORDERBY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ORDERBY elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 5a995713a795b3f24a4fcfadcc4be596e932a22c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564170"
---
# <a name="orderby-er-function"></a>ORDERBY ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `ORDERBY` atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir sakārtots atbilstoši norādītajiem argumentiem. Šos argumentus var definēt kā izteiksmes.

## <a name="syntax"></a>Sintakse

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`expression 1`: *Lauks*

Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā. Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam. Šis arguments ir obligāts.

`expression N`: *Lauks*

Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā. Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="example-1"></a>1. piemērs

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( ORDERBY( DS, DS. Value)).Value` atgriež teksta vērtību **A**.

## <a name="example-2"></a>2. piemērs

Ja parametrs **Kreditors** ir konfigurēts kā elektronisko pārskatu (ER) datu avots, kurš atsaucas uz tabulu VendTable, tad izteiksme `ORDERBY (Vendors, Vendors.'name()')` atgriež sarakstu ar kreditoriem, kuri ir sakārtoti augošā secībā pēc nosaukuma.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]