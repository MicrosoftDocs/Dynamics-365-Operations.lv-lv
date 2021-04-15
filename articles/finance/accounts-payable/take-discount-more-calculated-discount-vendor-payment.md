---
title: Vairāk par kreditora maksājumam aprēķinātās atlaides iekasēšana
description: Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi. Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62f2088ff04a0ef5ffe6ffe47b85f47e6957264d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810250"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>Vairāk par kreditora maksājumam aprēķinātās atlaides iekasēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi. Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu. 

Kreditors 3051 piešķir uzņēmumam Fabrikam termiņatlaidi 4 procentu apmēra, ja rēķins tiek apmaksāts septiņu dienu laikā. Eiprila 29. jūnijā ievada rēķinu par summu 1000,00. Kreditors dod Eiprilai atļauju piemērot atlaidi par summu 60,00 rēķinam aprēķinātās noklusējuma summas 40,00 vietā. Eiprila reģistrē vienreizēju maksājumu, izmantojot kreditoru maksājumu žurnālu. Viņa ievada maksājuma kreditoru un pēc tam atver lapu **Transakciju nosegšana**. Viņa atzīmē rēķinu un maina lauka **Termiņatlaides summa** vērtību uz **-60,00**.

| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | Rēķ.-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1000,00                       | USD      | 940,00           |

Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.

| Lauks                        | Vērtība     |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2015 |
| Termiņatlaides summa         | 60.00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 60,00     |

Eiprila iegrāmato maksājumu žurnālu. Rēķins tiek pilnībā nosegts, veicot maksājumu par summu 940,00 un piemērojot atlaidi 60,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]