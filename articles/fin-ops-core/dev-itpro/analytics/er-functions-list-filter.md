---
title: FILTER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FILTER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: d281fe710381b0ecb075a0d9281d46bd6edf987d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745301"
---
# <a name="filter-er-function"></a>FILTER ER funkcija

[!include [banner](../includes/banner.md)]

`FILTER` funkcija atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību, kad vaicājums ir mainīts tā, ka tas filtrē norādīto nosacījumu.

## <a name="syntax"></a>Sintakse

```vb
FILTER (list, condition)
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

Šī funkcija atšķiras no funkcijas [WHERE](er-functions-list-where.md), jo norādītais nosacījums tiek lietots datu bāzes līmenī visiem elektronisko pārskatu (ER) datu avotiem ar tipu *Tabulas ieraksti*. Sarakstu un nosacījumu var definēt, izmantojot tabulas un relācijas.

Ja viens vai abi argumenti, kas ir konfigurēts šai funkcijai (`list` un `condition`) neļauj šo pieprasījumu tulkot uz tiešo SQL zvanu, noformēšanas laikā tiek rādīts izņēmums. Šis izņēmums informē lietotāju, ka `list` vai `condition` nevar izmantot vaicājuma veikšanai datu bāzē.

## <a name="example-1"></a>1. piemērs

Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, izteiksme `FILTER (Vendors, Vendors.VendGroup = "40")` atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu.

## <a name="example-2"></a>2. piemērs

Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, un ja parametrs **parmVendorBankGroup** ir konfigurēts kā ER datu avots, kurš atgriež vērtību ar datu tipu *Virkne*, izteiksme `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` atgriež sarakstu, kurā ir tikai to kreditoru konti, kas pieder noteiktai banku grupai.

## <a name="example-3"></a>3. piemērs

Ievadāt datu avotu **DS** no veida *Aprēķinātais lauks*, un tas satur izteiksmi `SPLIT ("A,B,C", ",")` Pēc tam ievadāt citu izteiksmi, `FILTER( DS, DS.Value = "B")`. Mēģinot saglabāt šo izteiksmi ER formulas noformētājā, tiek rādīts šāds izņēmums: "Validācijas kļūda: FILTER funkcijas izteiksmju sarakstam nevar veikt vaicājumus."

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)
