---
title: FILTER ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota FILTER elektroniskā pārskata (ER) funkcija.
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
ms.openlocfilehash: 0e90db1836a93dab42be5dc91e9ea478163a1437
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559703"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]