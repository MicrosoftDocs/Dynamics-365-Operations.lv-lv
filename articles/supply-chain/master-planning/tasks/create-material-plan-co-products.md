---
title: Izveidot materiālu plānu līdzproduktiem
description: Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214374"
---
# <a name="create-a-material-plan-for-co-products"></a>Izveidot materiālu plānu līdzproduktiem

[!include [banner](../../includes/banner.md)]

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
1. Aizvērt lapu.
2. Aizvērt lapu.
3. Noklikšķiniet uz Vispārējā plānošana.
4. Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Piemērs: MasterPlan  
6. Noklikšķiniet uz Palaist.
7. Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.
8. Noklikšķiniet uz Filtrēt.
9. Sarakstā atlasiet rindu Lauks = Krājuma numurs.
10. Laukā Kritēriji ierakstiet kādu vērtību.
    * Piemērs: P6003  
11. Noklikšķiniet uz OK.
12. Noklikšķiniet uz OK.
13. Noklikšķiniet uz Plānotie pasūtījumi.
14. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".
    * Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.  
15. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet jebkuru filtra atgriezto rindu.  
16. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
17. Izvērsiet vai sakļaujiet sadaļu Piesaiste.
18. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.  
19. Aizvērt lapu.

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
1. Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Piemērs: MasterPlan  
3. Noklikšķiniet uz Palaist.
4. Izvērsiet vai sakļaujiet sadaļu Iekļaujamie ieraksti.
5. Noklikšķiniet uz Filtrēt.
6. Sarakstā atlasiet rindu Lauks = Krājuma numurs.
7. Laukā Kritēriji ierakstiet kādu vērtību.
    * Piemērs: P6003  
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz Plānotie pasūtījumi.
11. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Krājuma numurs, izmantojot vērtību "P6000".
    * Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.  
12. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet jebkuru filtra atgriezto rindu.  
13. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
14. Izvērsiet vai sakļaujiet sadaļu Piesaiste.
15. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.  
16. Aizvērt lapu.
17. Noklikšķiniet uz Vispārējā plānošana.
18. Doties uz Vispārējā plānošana > Iestatīšana > Vispārējas plānošanas parametri.
19. Laukā Atspējot visus plānošanas procesus atlasiet Nē.
20. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]