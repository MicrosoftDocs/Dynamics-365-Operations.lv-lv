---
title: WHERE ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota funkcija WHERE Electronic Reporting (ER).
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b3f8b01bffd0c530e5095531fc184c960744e751
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273164"
---
# <a name="where-er-function"></a>WHERE ER funkcija

[!include [banner](../includes/banner.md)]

`WHERE` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir filtrēts atbilstoši norādītajiem nosacījumam.

## <a name="syntax"></a>Sintakse

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`condition`: *Būla*

Derīga nosacījuma izteiksme, ko izmanto, lai filtrētu norādītā saraksta ierakstus.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Šī funkcija atšķiras no funkcijas [FILTER](er-functions-list-filter.md), jo norādītais nosacījums tiek lietots datu bāzes līmenī visiem elektronisko pārskatu (ER) datu avotiem ar tipu *Ierakstu saraksts*, kas atrodas atmiņā.

Ja argumenti, kas ir konfigurēts šai funkcijai (`list` un `condition`) neļauj šo pieprasījumu tulkot uz tiešo SQL zvanu, noformēšanas laikā tiek rādīts brīdinājuma ziņojums. Šis ziņojums informē lietotāju, ka tas var uzlabot veiktspēju, ja `WHERE` vietā tiek izmantota funkcija [FILTER](er-functions-list-filter.md).

## <a name="example-1"></a>1. piemērs

Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, izteiksme `WHERE (Vendors, Vendors.VendGroup = "40")` atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu.

## <a name="example-2"></a>2. piemērs

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("A|B|C", "|")`, izteiksme `WHERE( DS, DS.Value = "B")` atgriež sarakstu tikai ar vienu ierakstu kas laukā **Vērtība** satur tekstu **"B"**.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
