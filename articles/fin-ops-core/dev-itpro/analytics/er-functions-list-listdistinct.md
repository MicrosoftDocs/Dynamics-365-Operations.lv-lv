---
title: LISTDISTINCT ER funkcija
description: Šajā tēmā ir sniegta informācija par to, kā tiek izmantota LISTDISTINCT elektroniskā pārskata (ER) funkcija.
author: NickSelin
ms.date: 7/30/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 7cc51695d261a63521ae88e2a9362b6f30b9618ed89300bcaeb606b050c81350
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735578"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT ER funkcija

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`LISTDISTINCT` funkcija aprēķina norādīto izteiksmi kā atlasītāju katram norādītā saraksta ierakstam. Tiek atgriezta jauna *Ierakstu saraksta* vērtība, kurā ir viens ieraksts katrai unikālajai atlasītāja vērtībai.

## <a name="syntax"></a>Sintakse

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumenti

`list`: *Ierakstu saraksts*

*Ierakstu saraksta* tipa datu avota datu tipa derīgs ceļš.

`selector`: *Primitīvu datu tips*

Derīga izteiksme, ko izmanto, lai aprēķinātu atlasītāja vērtību katram ierakstam norādītajā sarakstā.

Šim parametram tiek atbalstīti šādi datu tipi:

- Būla
- Datums
- Datums un laiks
- GUID
- Vesels skaitlis
- Int64
- Reāls
- Virkne

## <a name="return-values"></a>Atgrieztās vērtības

*Ierakstu saraksts*

Iegūtais ierakstu saraksts.

## <a name="usage-notes"></a>Lietošanas piezīmes

Izveidotā saraksta struktūra atbilst norādītā saraksta struktūrai.

Norādītajam sarakstam var tikt aprēķināta vienāda atlasītāja vērtība vairākiem ierakstiem. Šajā gadījumā atbilstošā ieraksta lauka vērtības izveidotajā sarakstā ir vienādas ar vērtību pirmajam ierakstam no norādītā saraksta, kam tiek aprēķināta atlasītāja vērtība.

Šīs funkcijas izpilde tiek veikta jebkurā atmiņā esošā *Ierakstu saraksta* tipa [Elektroniskā pārskata (ER)](general-electronic-reporting.md) datu avota.

**GROUPBY** datu avotu var arī izmantot, lai ģenerētu to ierakstu sarakstu, kuriem tiek aprēķināts atlasītājs, kuram ir noteiktas vērtības. Tomēr no veiktspējas un atmiņas patēriņa perspektīvas ir labāk izmantot `LISTDISTINCT` funkciju nekā **GROUPBY** datu avotu, jo funkcijas izpilde tiek veikta atmiņā.

## <a name="example"></a>Paraugs

Sekojošais piemērs parāda, kā var iegūt unikālo debitoru kontu numuru sarakstu, kas ir izsniegts vismaz vienam pārdošanas vai projekta rēķinam noteiktā periodā.

1. Ievadiet **SalesInvoice** datu avotu `Record list` tipam, kas attiecas uz **CustInvoiceJour** pieteikumu tabulu un filtrē rēķinus par noteiktiem periodiem.

    Šī datu avota `InvoiceAccount` lauks atgriež rēķinā iekļauta debitora konta numuru.

2. Ievadiet **ProjectInvoice** datu avotu `Record list` tipam, kas attiecas uz **ProjInvoiceJour** pieteikumu tabulu un filtrē projektu rēķinus par noteiktiem periodiem.

    Šī datu avota `InvoiceAccount` lauks atgriež rēķinā iekļauta debitora konta numuru.

3. Konfigurējiet `Calculated field` tipa **AllInvoices** datu avotu, kas satur izteiksmi `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    Šajā datu avotā tiek atgriezts pārdošanas rēķinu un projekta rēķinu apvienotais saraksts.

4. Konfigurējiet `Record list` tipa **InvoicedCustomer** datu avotu, kas satur izteiksmi `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    Šis datu avots atgriež jaunu sarakstu, kurā ir viens ieraksts katram unikālam debitoram, kuram noteiktajā periodā ir izrakstīts rēķins. Šī saraksta `InvoiceAccount` lauks satur debitora konta numuru.

## <a name="additional-resources"></a>Papildu resursi

[Saraksta funkcijas](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]