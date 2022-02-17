---
title: ORDERBY ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota ORDERBY elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075178"
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
> Šī sintakse tiek atbalstīta Microsoft Dynamics 365 Finance versija 10.0.25 un jaunāka versija.

## <a name="arguments"></a>Argumenti

`location`:*[Stīga](er-formula-supported-data-types-primitive.md#string)*

Vieta, kur jāveic šķirošana. Ir derīgas šādas opcijas:

- "Vaicājums"
- "Atmiņā"

`list`:*[Ierakstu saraksts](er-formula-supported-data-types-composite.md#record-list)*

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

Datu šķirošana vienmēr tiek veikta lietojumprogrammu servera atmiņā. Sīkāku informāciju skatiet [piemērs 1](#example-1).

### <a name="syntax-2"></a>Sintakse 2

### <a name="sorting-in-memory"></a>Kārtošana atmiņā

Kad`location` arguments ir norādīts kā **Atmiņā**, datu šķirošana tiek veikta lietojumprogrammu servera atmiņā. Sīkāku informāciju skatiet [2. piemērs](#example-2).

### <a name="sorting-in-database"></a>Kārtošana datu bāzē

Kad`location` arguments ir norādīts kā **Vaicājums**, datu šķirošana tiek veikta datu bāzes līmenī. Šajā gadījumā,`list` argumentam jānorāda uz vienu no tālāk norādītajiem [Elektroniskā ziņošana (ER)](general-electronic-reporting.md) datu avoti, kas norāda lietojumprogrammas avotu, kuram var izveidot tiešu datu bāzes vaicājumu:

- Datu avots *Tabulas ieraksti* veids
- Saistība ar datu avotu *Tabulas ieraksti* veids
- Datu avots *Aprēķinu lauks* veids

The`expression 1` un`expression N` argumentiem ir jānorāda uz ER datu avota laukiem, kas norāda attiecīgos lietojumprogrammas avota laukus, kuriem var izveidot arī tiešu datu bāzes vaicājumu.

Ja nevar izveidot tiešu datu bāzes vaicājumu, tiek veikta validācija [kļūda](er-components-inspections.md#i18) notiek ER modeļa kartēšanas izstrādātājā. Ziņojumā, ko saņemat, norādīts, ka ER izteiksmi, kas ietver funkciju `ORDERBY`, nevar palaist izpildlaikā.

Lai nodrošinātu labāku veiktspēju, mēs iesakām izmantot **Vaicājums** opciju, ja kārtošana ir konfigurēta lietojumprogrammu datu avotiem, kas var saturēt lielu skaitu ierakstu (piemēram, darījumu lietojumprogrammu tabulām).

> [!NOTE]
> The`ORDEBY` pašu funkciju nevar pārtulkot tiešā datu bāzes vaicājumā. Tāpēc ER datu avots, kas satur šo funkciju, nav vaicājams. To nevar izmantot arī ER funkciju ietvaros, piemēram, [FILTRA](er-functions-list-filter.md) un [ALLITEMSQUERY](er-functions-list-allitemsquery.md), kur var izmantot tikai vaicājumus datu avotus.

Sīkāku informāciju skatiet [3. piemērs](#example-3) un [4. piemērs](#example-4).

### <a name="comparability"></a>Salīdzināmība

Tā kā SQL datu bāzes dzinējs un finanšu lietojumprogrammu serveris var izmantot atšķirīgu ranžēšanas vērtību vienai rakstzīmei, viena un tā paša ierakstu saraksta kārtošanas rezultāts var atšķirties, ja [Stīga](er-formula-supported-data-types-primitive.md#string) lauks tiek izmantots šķirošanai. Sīkāku informāciju skatiet [5. piemērs](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a> 1. piemērs: noklusējuma izpilde atmiņā

Ja ievadāt datu avotu **DS** tipam *Aprēķinātais lauks* un tajā ir izteiksme `SPLIT ("C|B|A", "|")`, izteiksme `FIRST( ORDERBY( DS, DS. Value)).Value` atgriež teksta vērtību **A**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a> 2. piemērs: skaidra izpilde atmiņā

Ja **Pārdevējs** ir konfigurēts kā ER datu avots *Tabulas ieraksti* veids, kas attiecas uz **VendTable** tabula, gan izteiksme`ORDERBY (Vendor, Vendor.'name()')` un izteiksme`ORDERBY ("InMemory", Vendor, Vendor.'name()')` atgriezt piegādātāju sarakstu, kas ir sakārtots pēc nosaukuma augošā secībā.

Kad konfigurējat izteiksmi`ORDERBY ("Query", Vendor, Vendor.'name()')` ER modeļa kartēšanas izstrādātājā apstiprinājums [kļūda](er-components-inspections.md#i8) notiek projektēšanas laikā, jo`Vendor.'name()'` ceļš attiecas uz lietojumprogrammas metodi, kurai ir loģika, kuru nevar pārtulkot tiešā datu bāzes vaicājumā.

## <a name="example-3-database-query"></a><a name="example-3"></a> 3. piemērs: datu bāzes vaicājums

Ja **TaxTransaction** ir konfigurēts kā ER datu avots *Tabulas ieraksti* veids, kas attiecas uz **TaxTrans** tabula, izteiksme`ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` sakārto ierakstus lietojumprogrammu datu bāzes līmenī un atgriež nodokļu darījumu sarakstu, kas ir sakārtots pēc nodokļu koda augošā secībā.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a> 4. piemērs. Pieprasāmi datu avoti

Ja **TaxTransaction** ir konfigurēts kā ER datu avots *Tabulas ieraksti* veids, kas attiecas uz **TaxTrans** galds, **TaxTransactionFiltered** ER datu avotu var konfigurēt tā, lai tajā būtu ietverta izteiksme`FILTER(TaxTransaction, TaxCode="VAT19")` kas ienesīs darījumus ar noteiktu nodokļu kodu. Tā kā konfigurētais **TaxTransactionFiltered** ER datu avots ir vaicājams, izteiksmi `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` var konfigurēt tā, lai filtrēto nodokļu darbību saraksts, kas sakārtots pēc darbības datuma augošā secībā, atgrieztos.

Konfigurējot **TaxTransactionOrdered** kā VR datu avotu *ar aprēķināto lauka* tipu, kas satur izteiksmi `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` un VER datu avotu *ar aprēķināto lauka* tipu, kas satur izteiksmi `FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, ER modeļa kartēšanas noformētājā noformēšanas laikā rodas validācijas [kļūda](er-components-inspections.md#i18). Šī kļūda rodas tāpēc, ka funkcijas FILTER pirmajam argumentam [ir jāatsaucas uz vaicājamu ER datu avotu, bet](er-functions-list-filter.md#usage-notes) TaxTransactionOrdered **datu avots, kurā ir** funkcija, nav vaicājams.`ORDERBY`

## <a name="example-5-comparability"></a><a name="example-5"></a> 5. piemērs: Salīdzināmība

### <a name="prerequisites"></a>Priekšnosacījumi

1. Ievadiet datu avotu **DS1** ar *lauka* tipu Aprēķinātais, kurā ir izteiksme `SPLIT ("D1|_D2|D3", "|")`.
2. **[Atveriet lapu Finanšu dimensijas vērtības](../../../finance/general-ledger/financial-dimensions.md)** un atlasiet **dimensiju CostCenter**.
3. Ievadiet šādas dimensijas vērtības: **D1**, **\_ D2** un **D3**.

### <a name="sorting-in-memory"></a>Kārtošana atmiņā

1. Konfigurējiet datu avotu **DS2** *ar aprēķināto lauka* tipu, kurā ir izteiksme `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Ievērojiet, ka izteiksme `FIRST(DS2).Value` atgriež teksta vērtību **"D1"**, izteiksme `INDEX(DS2, COUNT(DS2)).Value` atgriež teksta vērtību **"\_ D2"**, un izteiksme `STRINGJOIN(DS2, DS2.Value, "|")` atgriež teksta vērtību **"D1D3D2\|\|\_"**.

### <a name="sorting-in-database"></a>Kārtošana datu bāzē

1. Ievadiet datu avotu DS3 **ar** tabulas ierakstu *tipu, kas attiecas uz entītiju* FinancialDimensionValueEntity **·**.
2. Konfigurējiet datu avotu **DS4** lauka *tipam* Aprēķinātais, kurā ir izteiksme `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Konfigurējiet datu avotu **DS5** ar *lauka* tipu Aprēķinātais, kurā ir izteiksme `ORDERBY(DS4, DS4.DimensionValue)`.
4. Ievērojiet, ka izteiksme `FIRST(DS5).Value` atgriež teksta vērtību **"\_ D2"**, izteiksme `INDEX(DS5, COUNT(DS5)).Value` atgriež teksta vērtību **"D3"**, un izteiksme `STRINGJOIN(DS5, DS5.Value, "|")` atgriež teksta vērtību **"\_ D2D1D3\|\|"**.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
