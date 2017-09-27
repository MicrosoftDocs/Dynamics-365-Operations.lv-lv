--- 
title: "Maršrutu izveide (tikai 2016. gada februāris)"
description: "Šajā uzdevumā uzmanība ir vērsta uz ražošanas maršrutu izveidošanu pabeigtai precei un daļēji pabeigtai precei."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 0f8d6a45589886a611fc3a9179b50a8b1ac1c7f4
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="create-routes-february-2016-only"></a>Maršrutu izveide (tikai 2016. gada februāris)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumā uzmanība ir vērsta uz ražošanas maršrutu izveidošanu pabeigtai precei un daļēji pabeigtai precei. Tas ir MK aprēķina sērijas piektais uzdevums. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF.


## <a name="create-a-route-for-a-semi-finished-product"></a>Izveidot maršrutu daļēji pabeigtai precei
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Izlaistās preces.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet vienuma numuru BOM_2.  
3. Darbību rūtī noklikšķiniet uz Inženieris.
4. Noklikšķiniet uz Maršruts.
5. Noklikšķiniet uz Jauns.
6. Noklikšķiniet uz Maršruts un maršruta versija.
7. Apraksta laukā ierakstiet vērtību.
    * Šajā piemērā ierakstiet vērtību ROUTE_2.  
8. Laukā Vieta ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.  
9. Noklikšķiniet uz OK.
10. Noklikšķiniet uz Jauns.
11. Laukā Operācija ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā atlasiet vienumu Montāža.  
12. Laukā Izpildes laiks ievadiet skaitli.
    * Piemēram, ievadiet 1. Izpildes laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.  
13. Laukā Maršruta grupa ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā atlasiet vērtību Std.  
14. Noklikšķiniet uz cilnes Iestatījumi.
15. Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā atlasiet vienumu Montāža.  
16. Noklikšķiniet uz cilnes Reizes.
17. Laukā Uzstādīšanas laiks ievadiet kādu skaitli.
    * Šajā piemērā ierakstiet vērtību 1. Uzstādīšanas laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.  
18. Darbību rūtī noklikšķiniet uz Maršruta versija.
19. Noklikšķiniet uz Apstiprināt.
20. Laukā Vai vēlaties arī apstiprināt šo maršrutu? atlasiet Jā.
21. Noklikšķiniet uz OK.
22. Darbību rūtī noklikšķiniet uz Maršruta versija.
23. Noklikšķiniet uz Aktivizēt.
24. Aizvērt lapu.
25. Aizvērt lapu.

## <a name="create-a-route-for-a-finished-product"></a>Izveidot maršrutu pabeigtai precei
1. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet vienuma numuru BOM_1.  
2. Darbību rūtī noklikšķiniet uz Inženieris.
3. Noklikšķiniet uz Maršruts.
4. Noklikšķiniet uz Jauns.
5. Noklikšķiniet uz Maršruts un maršruta versija.
6. Apraksta laukā ierakstiet vērtību.
    * Šajā piemērā ierakstiet vērtību ROUTE_1.  
7. Laukā Vieta ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā ievadiet vai atlasiet vērtību 1. vieta.  
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz Jauns.
10. Laukā Operācija ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā atlasiet vienumu Iepakošana.  
11. Laukā Izpildes laiks ievadiet skaitli.
    * Šajā piemērā ierakstiet vērtību 1.  
12. Laukā Maršruta grupa ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā atlasiet vērtību Std.  
13. Noklikšķiniet uz cilnes Iestatījumi.
14. Laukā Iestatīšanas kategorija ievadiet vai atlasiet kādu vērtību.
    * Šajā piemērā atlasiet vienumu Iepakošana.  
15. Noklikšķiniet uz cilnes Reizes.
16. Laukā Uzstādīšanas laiks ievadiet kādu skaitli.
    * Šajā piemērā ierakstiet vērtību 1.  
17. Darbību rūtī noklikšķiniet uz Maršruta versija.
18. Noklikšķiniet uz Apstiprināt.
19. Noklikšķiniet uz OK.
20. Darbību rūtī noklikšķiniet uz Maršruta versija.
21. Noklikšķiniet uz Aktivizēt.
22. Aizvērt lapu.
23. Aizvērt lapu.

## <a name="enable-automatic-consumption-of-setup-time"></a>Iespējot uzstādīšanas laika automātisku patēriņu
1. Doties uz Ražošanas kontrole > Iestatīšana > Maršruti > Maršrutu grupas.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Sarakstā atlasiet vērtību Std.  
3. Noklikšķiniet uz Rediģēt.
4. Laukā Uzstādīšanas laiks atlasiet vērtību Jā.
    * Uzstādīšanas laiki bieži vien ir daļa no cenas, kas krājumam tiek aprēķināta.  
5. Noklikšķiniet uz Saglabāt.
6. Aizvērt lapu.

