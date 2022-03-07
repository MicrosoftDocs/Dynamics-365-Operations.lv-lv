---
title: Maksimālais decimāldaļu skaits noliktavas vienībai ir 0
description: Mēģinot grāmatot krājumu darbību vai krājumu rezervēšanu, tiek saņemta kļūda "Maksimālais decimāldaļu skaits noliktavas mērvienībai ir 0".
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477023"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Maksimālais decimāldaļu skaits noliktavas vienībai ir 0


## <a name="symptoms"></a>Simptomi

Mēģinot grāmatot krājumu darbību vai krājumu rezervēšanu, saņemat šādu kļūdas ziņojumu:

> Maksimālais decimāldaļu skaits noliktavas vienībai ir 0.

Šī problēma rodas, ja krājumu darbības daudzums ir norādīts kā decimālskaitļa vērtība, kas ir zem precizitātes līmeņa, ko lauks atbalsta. Piemēram, krājuma darbībai norādīts daudzums *0,5*, bet tiek atbalstīti tikai veseli skaitļi. Tāpēc vērtībai ir jābūt *1*, nevis *0,5*.

## <a name="resolution"></a>Novēršana

1. Lai krājumu darbībās noapaļotu daudzumus, palaidiet SQL Server instancē šādu skriptu. Šis skripts izlabos vērtības tabulā **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Palaidiet rīcībā esošo konsekvences pārbaudi, ja ir ieslēgta opcija **labot kļūdas**. Šis skripts izlabos vērtības tabulā **inventSum**.

> [!IMPORTANT]
> Ir stingri ieteicams rūpīgi rediģēt skriptu, kā tas nepieciešams jūsu videi, pārbaudīt to pārbaudes vidē un pēc tam pārbaudīt iegūtos datus pirms skripta palaišanas ražošanas vidē.
