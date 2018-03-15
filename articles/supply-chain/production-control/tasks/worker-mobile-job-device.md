--- 
title: "Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci"
description: "Šajā procedūrā parādīts, kā piešķirt pareizas lomas darbinieka lietotāja kontam un pēc tam ļaut darbiniekam veikt ražotnes ražotnes reģistrācijas."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: f9de2f79c68fead5ede714ff05bba97118874aad
ms.contentlocale: lv-lv
ms.lasthandoff: 02/06/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Nodarbinātā konfigurēšana, izmantojot mobilo darba ierīci

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā piešķirt pareizas lomas darbinieka lietotāja kontam un pēc tam ļaut darbiniekam veikt ražotnes ražotnes reģistrācijas.


## <a name="assign-roles-to-user-account"></a>Lomu piešķiršana lietotāja kontam
1. Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.
2. Izmantojiet ātro filtru, lai filtrētu pēc darbinieka vārda, ja lietotāja konts ir saistīts ar mašīnas operatora lomu. Parauga datos vārds ir Šenona.
3. Iezīmējiet lietotāja konta ierakstu.
4. Sarakstā noklikšķiniet uz saites "Vārds" atlasītajā rindā, lai skatītu detalizētu informāciju par lietotāja kontu.
5. Kokā atlasiet Lomas\Mašīnu operators.
6. Aizveriet detalizētas lietotāja informācijas lapu.
7. Aizvērt lapu.

## <a name="configure-worker-account"></a>Konfigurējiet lietotāja kontu.
1. Pārejiet uz sadaļu Personāla vadība > Darbinieki > Darbinieki.
2. Izmantojiet ātro filtru, lai filtrētu pēc darbinieka vārda, ja lietotāja konts ir saistīts ar mašīnas operatora lomu. Parauga datos vārds ir Šenona.
3. Iezīmējiet lietotāja konta ierakstu.
4. Sarakstā noklikšķiniet uz saites "Vārds" atlasītajā rindā, lai skatītu detalizētu informāciju par lietotāja kontu.
5. Noklikšķiniet uz cilnes Nodarbinātība.
6. Izvērsiet kopsavilkuma cilni Laika reģistrēšana un noklikšķiniet uz Aktivizēt reģistrācijas terminālos.
7. Noklikšķiniet uz Aktivizēt reģistrācijas terminālos.
8. Ievadiet vai atlasiet vērtību laukā Aprēķinu grupa.
9. Ievadiet vai atlasiet vērtību laukā Noklusējuma aprēķinu grupa.
10. Laukā Apstiprinājumu grupa ievadiet vai atlasiet kādu vērtību.
11. Laukā Standarta profils ievadiet vai atlasiet kādu vērtību.
12. Laukā Profilu grupa ievadiet vai atlasiet kādu vērtību.
13. Noklikšķiniet uz Labi.
14. Noklikšķiniet uz Rediģēt, lai ievadītu jauna laika reģistrācijas darbinieka žetona numuru.
15. Laukā Žetona ID ierakstiet kādu vērtību.
16. Klikšķiniet Saglabāt.
17. Lietojiet saīsni SaveRecord.
18. Aizveriet darbinieku detalizētas informācijas lapu.
19. Aizvērt lapu.

## <a name="assign-worker-to-device-group"></a>Piešķiriet darbinieku ierīču grupai.
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Ražošanas izpilde > Konfigurēt ierīču darba karti.
2. Noklikšķiniet uz Pievienot.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Rediģēt.
6. Laukā Ražošanas vienība var iestatīt noklusējuma filtru darbiniekam. Tas nodrošinās, ka, darbiniekam piesakoties ierīcē, tiek rādīti tikai ražošanas darbi atlasītajai ražošanas vienībai.
7. Aizvērt lapu.

