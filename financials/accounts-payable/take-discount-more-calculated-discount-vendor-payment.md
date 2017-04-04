---
title: "Atlaide, kas ir lielāka par aprēķināto atlaidi par kreditora maksājumu veikt"
description: "Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi. Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 22ba73681faa509a5144517163cc173a1267a534
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Atlaide, kas ir lielāka par aprēķināto atlaidi par kreditora maksājumu veikt

Šajā rakstā ir aprakstīts scenārijs, kas izskaidro, kā tiek piemērota termiņatlaide par summu, kas ir lielāka par sākotnēji rēķinā piešķirto atlaidi. Šis scenārijs var īstenoties, ja organizācija noslēdz līgumu ar kreditoru par mazākas summas rēķinā maksāšanu. 

Kreditors 3051 piešķir uzņēmumam Fabrikam termiņatlaidi 4 procentu apmēra, ja rēķins tiek apmaksāts septiņu dienu laikā. Eiprila 29. jūnijā ievada rēķinu par summu 1000,00. Kreditors dod Eiprilai atļauju piemērot atlaidi par summu 60,00 rēķinam aprēķinātās noklusējuma summas 40,00 vietā. Eiprila reģistrē vienreizēju maksājumu, izmantojot kreditoru maksājumu žurnālu. Viņa ienāk kreditora maksājumu un tad atver **norēķiniem par darījumiem** lapā. Viņa atzīmē rēķina un maina vērtību **termiņatlaides summa** lauku, lai **60,00**.
| Atzīmēt     | Izmantot termiņatlaidi | Dokuments   | Konts | Datums      | Izpildes datums  | Rēķins | Summa darījuma valūtā | Valūta | Nosedzamā summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Atlasīts | Parastais            | Rēķ.-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1000,00                       | USD      | 940,00           |

Atlaides informācija ir redzama lapas **Nosegt transakcijas** apakšdaļā.
|                              |           |
|------------------------------|-----------|
| Termiņatlaides datums           | 7/12/2015 |
| Termiņatlaides summa         | 60,00     |
| Izmantot termiņatlaidi            | Parastais    |
| Paņemta termiņatlaides summa          | 0,00      |
| Ņemamā termiņatlaides summa | 60,00     |

Eiprila iegrāmato maksājumu žurnālu. Rēķins tiek pilnībā nosegts, veicot maksājumu par summu 940,00 un piemērojot atlaidi 60,00.


