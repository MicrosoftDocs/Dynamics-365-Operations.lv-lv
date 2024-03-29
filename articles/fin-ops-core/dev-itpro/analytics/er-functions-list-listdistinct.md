---
title: LISTDISTINCT ER funkcija
description: Šajā rakstā ir sniegta informācija par to, kā tiek izmantota FUNKCIJA LISTDISTINCT Elektroniskie pārskati (ER).
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285281"
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
