---
title: Pamatlīdzekļu pārklasificēšana
description: Šī tēma izskaidro aktīvu pārklasificēšanas procesu. Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5fadebe685810d6833d1cb0581ed9a4869cc124
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883650"
---
# <a name="reclassify-fixed-assets"></a>Pamatlīdzekļu pārklasificēšana

[!include [banner](../../includes/banner.md)]

Lai pārklasificētu pamatlīdzekli, tas ir jāpārsūta uz jaunu pamatlīdzekļu grupu vai tam ir jāpiešķir jauns pamatlīdzekļa numurs tajā pašā grupā. 

Kad pamatlīdzeklis ir pārklasificētas:

- Visas esošā pamatlīdzekļa grāmatas tiek izveidotas jaunajam pamatlīdzeklim. Visa sākotnējam pamatlīdzeklim iestatītā informācija tiek kopēta uz jauno pamatlīdzekli. Grāmatu statuss oriģinālajam pamatlīdzeklim ir Slēgts. 

- Jaunā pamatlīdzekļa jaunās grāmatas satur pārklasificēšanas datumu laukā **Iegādes datums**. Datums laukā **Nolietojuma sākuma datums** tiek kopēts no sākotnējā līdzekļa informācijas. Ja nolietojums jau ir sākts, tad laukā **Pēdējais nolietojuma aprēķināšanas datums** ir redzams pārklasificēšanas datums. 

- Esošās pamatlīdzekļa transakcijas sākotnējam pamatlīdzeklim tiek atceltas un pārģenerētas jaunajam pamatlīdzeklim.

- Kad pamatlīdzeklis, kam ir pārsūtīšanas transakcija, tiek pārklasificēts, sistēma **Darbību centrā** parādīs ziņojumu, lai norādītu, ka pārklasificēšanas procesa laikā pārsūtīšanas transakcija netika pabeigta. Jāpabeidz pārsūtīšanas transakcija, lai pārvietotu esošās pārklasificēšanas transakcijas uz atbilstošām finanšu dimensijām. 

   Pārklasificēšanas procesa laikā sistēma palaiž šādas darbības, lai pārklasificētu līdzekļu bilanci no sākotnējā pamatlīdzekļa uz jaunu līdzekli. 
   
   - Pārklasificēšanas process kopē datus no sākotnējās pamatlīdzekļu grāmatas uz jauno pamatlīdzekļu grāmatu.

   - Pārklasificēšanas transakcija izmanto informāciju no oriģinālās iegrāmatotās iegādes, kas ietver finanšu dimensijas informāciju, kas ir iekļauta iegādes transakcijā.  
   
   - Tajā pašā laikā pārklasificēšanas process atceļ sākotnējo līdzekļa iegādes un līdzekļa pārsūtīšanas transakciju. 

Šajā diagrammā un procedūrā dots pārklasificēšanas procesa piemērs. 

[![Diagramma, kas parāda pārklasifikācijas procesu.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Lai pārklasificētu pamatlīdzekli, veiciet tālāk minētās darbības.

1. Dodieties uz **Pamatlīdzekļi > Periodiskie uzdevumi > Pārklasificēšana.**
2. Laukā **Pamatlīdzekļu grupa** atlasiet grupu, ko vēlaties pārklasificēt.
3. Laukā **Pamatlīdzekļa numurs** atlasiet, kuru pamatlīdzekli pārklasificēt.
4. Laukā **Jauna pamatlīdzekļu grupa** atlasiet grupu, uz kuru pārsūtīt šo pamatlīdzekli.
    * Ja jaunā pamatlīdzekļu grupa ir pievienota kādai numuru sērijai, tad lauks **Jauns pamatlīdzekļa numurs** tiek atjaunināts ar numuru no jaunās pamatlīdzekļu grupas numuru sērijas. Pretējā gadījumā lauks **Jauns pamatlīdzekļa numurs** tiek atjaunināts ar numuru no numuru sērijas, kas ir iestatīta lapā **Pamatlīdzekļu parametri**. Ja lapā **Pamatlīdzekļu parametri** nav iestatīta numuru sērija, ievadiet kādu numuru laukā **Jauns pamatlīdzekļa numurs**.  
5. Laukā **Pārklasificēšanas datums** ievadiet kādu datumu.
6. Laukā **Dokumentu sērijas** ievadiet vai atlasiet kādu vērtību.
7. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
