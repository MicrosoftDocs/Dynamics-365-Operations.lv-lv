---
title: WHERE ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota WHERE elektroniskā pārskata (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916089"
---
# <a name="WHERE">WHERE ER funkcija</a>

[!include [banner](../includes/banner.md)]

`WHERE` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir filtrēts atbilstoši norādītajiem nosacījumam.

## <a name="syntax"></a>Sintakse

```
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
