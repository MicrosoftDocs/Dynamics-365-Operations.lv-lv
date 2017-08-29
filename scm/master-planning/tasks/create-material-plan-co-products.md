--- 
title: "Materiālu plāna izveide līdzproduktiem"
description: "Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4eb36b0de53f40f882950628d55d6ac08ac5fdde
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Materiālu plāna izveide līdzproduktiem

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.


## <a name="create-requirement-for-a-co-product"></a>Vajadzības izveide līdzproduktam
1. Dodieties uz Noklusējuma informācijas panelis.
2. Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.
3. Klikšķiniet Jauns.
4. Noklikšķiniet uz Pārdošanas pasūtījums.
5. Laukā Debitora konts ierakstiet kādu vērtību.
    * Piemērs: US-001  
6. Noklikšķiniet uz OK.
7. Laukā Krājuma kods ierakstiet kādu vērtību.
    * Piemērs: P6003  
8. Laukā Daudzums ievadiet skaitli.
    * Piemērs: 50000  
9. Noklikšķiniet uz Saglabāt.

## <a name="create-a-material-plan-for-co-products"></a>Materiālu plāna izveide līdzproduktiem
1. Noklikšķiniet uz Vispārējā plānošana.
2. Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Piemērs: MasterPlan  
4. Noklikšķiniet uz Palaist.
5. Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.
6. Noklikšķiniet uz Filtrēt.
7. Sarakstā atlasiet rindu Lauks = Krājuma numurs.
8. Laukā Kritēriji ierakstiet kādu vērtību.
    * Piemērs: P6003  
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz OK.
11. Noklikšķiniet uz Plānotie pasūtījumi.
12. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".
    * Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.  
13. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet jebkuru filtra atgriezto rindu.  
14. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
15. Izvērsiet vai sakļaujiet sadaļu Piesaiste.
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.  
17. Aizvērt lapu.


