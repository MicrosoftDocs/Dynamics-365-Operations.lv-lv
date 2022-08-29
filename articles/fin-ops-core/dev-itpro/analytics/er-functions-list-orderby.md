---
title: ORDERBY ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota orderBY elektronisko pārskatu (ER) funkcija.
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
ms.openlocfilehash: 23ace859bf75b2adb6ef8604475519a015486948
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282567"
---
# <a name="orderby-er-function"></a>ORDERBY ER funkcija

[!include [banner](../includes/banner.md)]

Funkcija `ORDERBY` atgriež norādīto sarakstu kā *Ierakstu saraksta* vērtību pēc tam, kad tas ir sakārtots atbilstoši norādītajiem argumentiem. Šos argumentus var definēt kā izteiksmes.

## <a name="syntax-1"></a><a name="syntax-1"></a>Sintakse 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Sintakse 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Šī sintakse tiek atbalstīta Microsoft Dynamics 365 Finanšu versijai 10.0.25 vai jaunākai versijai.

## <a name="arguments"></a>Argumenti

`location`: *[virkne](er-formula-supported-data-types-primitive.md#string)*

Vieta, kur jāveic kārtošana. Ir derīgas šādas opcijas:

- "Vaicājums"
- "InMemory"

`list`: *[ierakstu saraksts](er-formula-supported-data-types-composite.md#record-list)*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`expression 1`: *Lauks*

Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā. Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam. Šis arguments ir obligāts.

`expression N`: *Lauks*

Derīgs datu avota lauka ceļš, uz kuru ir atsauce izsauktās funkcijas `list` argumentā. Laukam, uz kuru ir atsauce, jābūt primitīva datu tipa laukam. Šie papildu argumenti nav obligāti.

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

### <a name="syntax-1"></a>Sintakse 1

Datu kārtošana vienmēr tiek veikta programmas servera atmiņā. Detalizētāku informāciju skatiet [1. piemērā](#example-1).

### <a name="syntax-2"></a>Sintakse 2

### <a name="sorting-in-memory"></a>Kārtošana atmiņā

Ja arguments `location` norādīts kā **InMemory**, datu kārtošana tiek veikta programmu servera atmiņā. Detalizētāku informāciju skatiet [2. piemērā](#example-2).

### <a name="sorting-in-database"></a>Kārtošana datu bāzē

Ja arguments `location` norādīts kā **Vaicājums**, datu bāzes līmenī tiek veikta datu kārtošana. Šajā gadījumā argumentam jānorāda uz vienu no šiem elektronisko pārskatu (ER)`list` datu avotiem, kas norāda programmas avotu, [kam](general-electronic-reporting.md) var izveidot tiešu datu bāzes vaicājumu:

- Tabulas ierakstu *tipa datu* avots
- Tabulas ierakstu tipa datu *avota* relācija
- Aprēķina lauka tipa *datu* avots

Argumentiem `expression 1``expression N` un argumentiem ir jānorāda uz ER datu avota laukiem, kas norāda atbilstīgos programmas avota laukus, kuriem var izveidot arī tiešu datu bāzes vaicājumu.

Ja nevar izveidot tiešu datu bāzes vaicājumu, ER modeļu kartēšanas [veidotājā](er-components-inspections.md#i18) rodas apstiprināšanas kļūda. Ziņojumā, ko saņemat, norādīts, ka ER izteiksmi, kas ietver funkciju `ORDERBY`, nevar palaist izpildlaikā.

Lai uzlabotu veiktspēju, ieteicams lietot opciju Query **,** ja kārtošana ir konfigurēta programmas datu avotiem, kas var saturēt lielu skaitu ierakstu (piemēram, transakciju programmas tabulām).

> [!NOTE]
> Pašu `ORDEBY` funkciju nevar tulkot tiešās datu bāzes vaicājumā. Tāpēc ER datu avots, kas satur šo funkciju, nav vaicājams. To nevar izmantot arī ER [funkciju, piemēram, FILTER](er-functions-list-filter.md)[un ALLITEMSQUERY](er-functions-list-allitemsquery.md), t.i., ietverot tikai vaicājamus datu avotus.

Papildinformāciju skatiet [3. un](#example-3)[4. piemērā](#example-4).

### <a name="comparability"></a>Salīdzināmību

Tā kā SQL datu bāzes programma un finanšu programmas serveris vienai rakstzīmei var izmantot atšķirīgu rangu vērtību, [viena un tā paša ierakstu saraksta kārtošanas rezultāts var atšķirties, ja Virknes](er-formula-supported-data-types-primitive.md#string) lauks tiek izmantots kārtošanai. Detalizētāku informāciju skatiet [5. piemērā](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a> 1. piemērs: noklusējuma izpilde atmiņā

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( ORDERBY( DS, DS. Value)).Value` atgriež teksta vērtību **A**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a> 2. piemērs: atmiņā precīzi formulēta izpilde

Ja **kreditors ir konfigurēts kā ER** *datu* avots tabulas ierakstu tipam, kas attiecas uz VendTable **tabulu, gan izteiksme, gan izteiksme atgriež kreditoru sarakstu,**`ORDERBY (Vendor, Vendor.'name()')` kas sakārtots pēc nosaukuma augošā secībā.`ORDERBY ("InMemory", Vendor, Vendor.'name()')`

Konfigurējot `ORDERBY ("Query", Vendor, Vendor.'name()')` izteiksmi ER modeļa kartēšanas veidotājā, [izstrādes](er-components-inspections.md#i8) laikā rodas apstiprināšanas kļūda, jo ceļš attiecas uz programmas metodi, `Vendor.'name()'` kam ir loģika, ko nevar tulkot tiešajā datu bāzes vaicājumā.

## <a name="example-3-database-query"></a><a name="example-3"></a> 3. piemērs: datu bāzes vaicājums

**Ja TaxTransaction** ir konfigurēts kā tabulas ierakstu tipa *ER* **datu avots, kas attiecas uz tabulu TaxTrans**, `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` izteiksme kārto ierakstus programmas datu bāzes līmenī un atgriež to nodokļu darbību sarakstu, kas kārtotas pēc nodokļu koda augošā secībā.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a> 4. piemērs: Vaicājami datu avoti

**Ja TaxTransaction** ir konfigurēts kā tabulas ierakstu tipa *ER* **datu avots, kas attiecas uz tabulu TaxTrans**, **taxTransactionFiltered** ER `FILTER(TaxTransaction, TaxCode="VAT19")` datu avotu var konfigurēt, lai tas satur izteiksmi, kura ienestu darbības norādītajam nodokļu kodam. Tā kā konfigurētais **TaxTransactionFiltered** ER datu avots ir vaicājums, `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` izteiksmi var konfigurēt, lai atgrieztu filtrēto nodokļu darbību sarakstu, kas sakārtots pēc darbības datuma augošā secībā.

**Ja taxTransactionOrdered** konfigurējat kā aprēķinātā lauka tipa *ER*`ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` datu avotu, kas satur izteiksmi un aprēķinātā lauka tipa, kas satur izteiksmi, ER *·*`FILTER(TaxTransactionOrdered, TaxCode="VAT19")` datu avotu, apstiprināšanas [kļūda](er-components-inspections.md#i18) rodas izstrādes laikā ER modeļu kartēšanas veidotājā. Šī kļūda rodas, jo pirmajam filtra funkcijas argumentam [ir](er-functions-list-filter.md#usage-notes) jāatsaucas uz vaicājumāmu ER datu avotu, **bet TaxTransactionOrdered** datu `ORDERBY` avots, kas ietver funkciju, nav vaicājams.

## <a name="example-5-comparability"></a><a name="example-5"></a> 5. piemērs: Pieturamība

### <a name="prerequisites"></a>Priekšnosacījumi

1. Ievadiet aprēķinātā **lauka tipa datu avotu** *DS1*, kas satur izteiksmi `SPLIT ("D1|_D2|D3", "|")`.
2. Atveriet lapu **[Finanšu dimensijas](../../../finance/general-ledger/financial-dimensions.md)** vērtības un atlasiet izmaksu **centra dimensiju**.
3. Ievadiet šādas dimensiju vērtības: **D1**, **\_ D2** un **D3**.

### <a name="sorting-in-memory"></a>Kārtošana atmiņā

1. Konfigurējiet aprēķinātā **lauka tipa datu avotu** *DS2*, kas satur izteiksmi `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Ievērojiet, ka `FIRST(DS2).Value` izteiksme atgriež teksta vērtību "D1"**,**`INDEX(DS2, COUNT(DS2)).Value` izteiksme atgriež teksta vērtību "**D2"\_,**`STRINGJOIN(DS2, DS2.Value, "|")` un izteiksme atgriež teksta vērtību "D1 **D3\| D2"\|\_.**

### <a name="sorting-in-database"></a>Kārtošana datu bāzē

1. Ievadiet tabulas **ierakstu tipa datu avotu** *DS3*, kas attiecas uz elementu **FinancialDimensionValueEntity**.
2. Konfigurējiet aprēķinātā **lauka tipa datu avotu** *DS4*, kas satur izteiksmi `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Konfigurējiet aprēķinātā **lauka tipa datu avotu** *DS5*, kas satur izteiksmi `ORDERBY(DS4, DS4.DimensionValue)`.
4. Ievērojiet, ka `FIRST(DS5).Value`**izteiksme atgriež teksta vērtību "\_ D2"**, `INDEX(DS5, COUNT(DS5)).Value`**izteiksme atgriež teksta vērtību "D3"**, `STRINGJOIN(DS5, DS5.Value, "|")`**un izteiksme atgriež teksta vērtību "\_ D2\| D1\| D3"**.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
