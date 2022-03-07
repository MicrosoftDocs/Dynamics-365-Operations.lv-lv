---
title: Izveidot materiālu plānu līdzproduktiem
description: Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: deae0d7e0295aa02f5ad512f67e9e3d2148c2e33
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578300"
---
# <a name="create-a-material-plan-for-co-products"></a>Izveidot materiālu plānu līdzproduktiem

[!include [banner](../../includes/banner.md)]

Ražošanas plānotājs plāno materiālu vajadzības krājumiem, kas ir formulas līdzprodukti. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USP2.

## <a name="create-requirement-for-a-co-product"></a>Vajadzības izveide līdzproduktam

1. Dodieties uz **Pārdošana un mārketings \> Darbvietas \> Pārdošanas pasūtījumu apstrāde un pieprasījums**.
1. Atlasiet **Jauns**.
1. Atlasiet vienumu **Pārdošanas pasūtījums**.
1. Laukā **Debitora konts** ierakstiet kādu vērtību.
    * Piemērs: US-001  
1. Atlasiet **Labi**.
1. Laukā **Krājuma kods** ierakstiet vērtību.
    * Piemērs: P6003  
1. Laukā **Daudzums** ierakstiet kādu skaitli.
    * Piemērs: 50000  
1. Atlasiet **Saglabāt**.

## <a name="create-a-material-plan-for-co-products"></a>Materiālu plāna izveide līdzproduktiem

1. Aizvērt lapu.
1. Aizvērt lapu.
1. Atlasiet **Vispārējā plānošana**.
1. Laukā **Plāns** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.
1. Sarakstā atlasiet saiti atlasītajā rindā.
    * Piemērs: MasterPlan  
1. Atlasiet **Izpildīt**.
1. Izvērsiet vai sakļaujiet sadaļu **Iekļaujamie ieraksti**.
1. Atlasiet **Filtrēt**.
1. Sarakstā atlasiet rindu **Lauks** = *Krājuma numurs*.
1. Laukā **Kritēriji** ierakstiet kādu vērtību.
    * Piemērs: P6003  
1. Atlasiet **Labi**.
1. Atlasiet **Labi**.
1. Atlasiet **Plānotie pasūtījumi**.
1. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību "P6000".
    * Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.  
1. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet jebkuru filtra atgriezto rindu.  
1. Sarakstā atlasiet saiti atlasītajā rindā.
1. Izvērsiet sadaļu **Piesaiste**.
1. Sarakstā atlasiet saiti atlasītajā rindā.
    * Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.  
1. Aizvērt lapu.

## <a name="create-a-second-requirement-for-a-co-product"></a>Otras vajadzības izveide līdzproduktam

1. Dodieties uz **Pārdošana un mārketings \> Darbvietas \> Pārdošanas pasūtījumu apstrāde un pieprasījums**.
1. Atlasiet **Jauns**.
1. Atlasiet vienumu **Pārdošanas pasūtījums**.
1. Laukā **Debitora konts** ierakstiet kādu vērtību.
    * Piemērs: US-001  
1. Atlasiet **Labi**.
1. Laukā **Krājuma kods** ierakstiet vērtību.
    * Piemērs: P6003  
1. Laukā **Daudzums** ierakstiet kādu skaitli.
    * Piemērs: 50000  
1. Atlasiet **Saglabāt**.

## <a name="create-a-second-material-plan-for-co-products"></a>Otra materiālu plāna izveide līdzproduktiem

1. Laukā **Plāns** atlasiet nolaižamo pogu uzmeklēšanas atvēršanai.
2. Sarakstā atlasiet saiti atlasītajā rindā.
    * Piemērs: MasterPlan  
3. Atlasiet **Izpildīt**.
4. Izvērsiet vai sakļaujiet sadaļu **Iekļaujamie ieraksti**.
5. Atlasiet **Filtrēt**.
6. Sarakstā atlasiet rindu **Lauks** = *Krājuma numurs*.
7. Laukā *Kritēriji* ierakstiet kādu vērtību.
    * Piemērs: P6003  
8. Atlasiet **Labi**.
9. Atlasiet **Labi**.
10. Atlasiet **Plānotie pasūtījumi**.
11. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka **Krājuma numurs**, izmantojot vērtību "P6000".
    * Filtrējiet pēc formulas krājuma, kuram ir krājuma līdzprodukts, kuram izveidojāt pārdošanas pasūtījumu.  
12. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet jebkuru filtra atgriezto rindu.  
13. Sarakstā atlasiet saiti atlasītajā rindā.
14. Izvērsiet vai sakļaujiet sadaļu **Piesaiste**.
15. Sarakstā atlasiet saiti atlasītajā rindā.
    * Plānotais pasūtījums ir piesaistīts līdzprodukta pārdošanas pasūtījumam.  
16. Aizvērt lapu.
17. Atlasiet **Vispārējā plānošana**.
18. Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Vispārējas plānošanas parametri**.
19. Laukā **Atspējot visus plānošanas procesus** atlasiet *Nē*.
20. Aizvērt lapu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]