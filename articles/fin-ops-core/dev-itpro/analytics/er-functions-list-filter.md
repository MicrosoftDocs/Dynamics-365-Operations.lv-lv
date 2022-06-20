---
title: FILTER ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota elektronisko pārskatu filtra (ER) funkcija.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: dfa4afdcfad8c1855a10e1fa37c36cc5b20682ef
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884522"
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

## <a name="usage-notes"></a><a name="usage-notes"></a>Lietošanas piezīmes

Šī funkcija atšķiras no funkcijas [WHERE](er-functions-list-where.md), jo norādītais nosacījums tiek lietots datu bāzes līmenī visiem elektronisko pārskatu (ER) datu avotiem ar tipu *Tabulas ieraksti*. Sarakstu un nosacījumu var definēt, izmantojot tabulas un relācijas.

Ja viens vai abi argumenti, kas ir konfigurēts šai funkcijai (`list` un `condition`) neļauj šo pieprasījumu tulkot uz tiešo SQL zvanu, noformēšanas laikā tiek rādīts izņēmums. Šis izņēmums informē lietotāju, ka `list` vai `condition` nevar izmantot vaicājuma veikšanai datu bāzē.

> [!NOTE]
> Funkcija `FILTER` atbilst funkcijai, kas atšķiras no `WHERE` funkcijas, [`VALUEIN`](er-functions-logical-valuein.md) kad tiek lietota funkcija, kas norāda atlases kritērijus.
> 
> - Ja funkcija `VALUEIN` tiek `WHERE` izmantota funkcijas tvērumā un otrais arguments attiecas uz datu avotu, `VALUEIN` kas atgriež nekādus ierakstus, tiek apsvērta Būla *[Vērtība Aplams](er-formula-supported-data-types-primitive.md#boolean)*`VALUEIN`, kas atgriež. Tādējādi izteiksme neatgriež `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` kreditoru ierakstus, ja **VendGroups datu** avots neatgriež kreditoru grupas ierakstus.
> - Ja funkcija `VALUEIN` tiek `FILTER` izmantota funkcijas tvērumā un otrais arguments attiecas uz datu avotu, `VALUEIN` kas atgriež bez ierakstiem, Būla *[Vērtība False](er-formula-supported-data-types-primitive.md#boolean)*`VALUEIN`, kas atgriež, tiek ignorēta. Tāpēc izteiksme atgriež `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` visus kreditoru **datu** avota kreditoru ierakstus, **pat ja VendGroups** datu avots neatgriež kreditoru grupas ierakstus.

## <a name="example-1"></a>1. piemērs

Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, izteiksme `FILTER (Vendors, Vendors.VendGroup = "40")` atgriež tikai kreditoru grupā 40 ietverto kreditoru sarakstu.

## <a name="example-2"></a>2. piemērs

Ja parametrs **Kreditors** ir konfigurēts kā ER datu avots, kurš atsaucas uz tabulu VendTable, un ja parametrs **parmVendorBankGroup** ir konfigurēts kā ER datu avots, kurš atgriež vērtību ar datu tipu *Virkne*, izteiksme `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` atgriež sarakstu, kurā ir tikai to kreditoru konti, kas pieder noteiktai banku grupai.

## <a name="example-3"></a>3. piemērs

Ievadāt datu avotu **DS** no veida *Aprēķinātais lauks*, un tas satur izteiksmi `SPLIT ("A,B,C", ",")` Pēc tam ievadāt citu izteiksmi, `FILTER( DS, DS.Value = "B")`. Mēģinot saglabāt šo izteiksmi ER formulas noformētājā, tiek rādīts šāds izņēmums: "Validācijas kļūda: FILTER funkcijas izteiksmju sarakstam nevar veikt vaicājumus."

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
