---
title: Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram
description: Izmantojiet žurnāla dokumentu, lai reģistrētu informāciju ar iepriekšēju datumu datētam čekam, pirms čeku izsniedzat kreditoram.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 312f7c58352e3cb86c22f8c34b1b6c11456c0083
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779484"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a>Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram

[!include [banner](../../includes/banner.md)]

Izmantojiet žurnāla dokumentu, lai reģistrētu informāciju ar iepriekšēju datumu datētam čekam, pirms čeku izsniedzat kreditoram. Var arī grāmatot ar iepriekšēju datumu datēto čeku un ģenerētu finanšu transakcijas. Pirms reģistrējat un grāmatojat ar iepriekšēju datumu datētu čeku, ko esat saņēmis no kreditora, izpildiet tālāk norādīto uzdevumu: 

Iestatiet grāmatotos čekus **lapā Skaidras naudas un bankas pārvaldība**. 

Šī uzdevuma izpildei nepieciešama loma Kasieris. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Dodieties uz Acounts **maksājamo > Maksājumu > maksājumu žurnāls**.
2. Klikšķiniet **Jauns**.
3. **Laukā Name (Nosaukums**) ierakstiet "VendPay".
4. Noklikšķiniet uz **Rindas**.
5. Laukā **Konts** norādiet vēlamās vērtības.
6. Sarakstā atzīmējiet atlasīto rindu.
7. Laukā **Debets** ievadiet kādu skaitli.
8. **Laukā Maksājuma** metode noklikšķiniet uz nolaižamās izvēlnes pogas, lai atvērtu uzmeklēšanu.
    * Maksāšanas tipa atlasīšana ar iepriekšēju datumu datētajam čekam  
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Noklikšķiniet uz **cilnes Grāmatotās pārbaudes**.
12. Laukā **Pārbaudes numurs** ierakstiet vērtību.
    * Ievadiet vai rediģējiet ar iepriekšēju datumu datētā čeka numuru.  
13. **Laukā Izdevējbankas nosaukums** ierakstiet vērtību.
    * Ievadiet izdevēja bankas informāciju.  
14. Noklikšķiniet uz **cilnes Saraksts**.
15. Noklikšķiniet uz **Grāmatot**.
16. Aizvērt lapu.
17. Noklikšķiniet uz cilnes Ar iepriekšēju datumu datēti čeki.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
