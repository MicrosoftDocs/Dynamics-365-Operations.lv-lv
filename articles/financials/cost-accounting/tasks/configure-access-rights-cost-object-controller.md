--- 
title: "Piekļuves tiesību konfigurēšana izmaksu objekta kontrolierim"
description: "Izmantojiet šo procedūru, lai konfigurētu izmaksu objekta kontroliera piekļuves tiesības."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.openlocfilehash: 9c5f79b7d9d62b29f21f2ddd1f6507ff82b381cc
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Piekļuves tiesību konfigurēšana izmaksu objekta kontrolierim

[!include[task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai konfigurētu izmaksu objekta kontroliera piekļuves tiesības. Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.


## <a name="assign-the-cost-object-controller-role"></a>Izmaksu objekta kontroliera lomas piešķire
1. Pārejiet uz sadaļu Sistēmas administrēšana > Lietotāji > Lietotāji.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Lietotājvārds, izmantojot vērtību "alicia".
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Noklikšķiniet uz Piešķirt lomas.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
6. Noklikšķiniet uz OK.

## <a name="enable-access-list-security"></a>Piekļuves saraksta drošības iespējošana
1. Dodieties uz Izmaksu uzskaite > Dimensijas > Dimensiju hierarhijas.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet Organizācija.  
3. Noklikšķiniet uz Rediģēt.
4. Laukā Piekļuves sarakstu hierarhija atlasiet Jā.
5. Noklikšķiniet uz Skatīt hierarhiju.

## <a name="assign-access-rights-to-user"></a>Piekļuves tiesību piešķiršana lietotājam
1. Noklikšķiniet uz Jauns.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Laukā Lietotāja ID ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Administrators.  
4. Kokā atlasiet Organization\CEO\CFO\FIM.
5. Noklikšķiniet uz Jauns.
6. Sarakstā atzīmējiet atlasīto rindu.
7. Laukā Lietotāja ID ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Alīsija.  
8. Noklikšķiniet uz Saglabāt.

## <a name="enable-access-rights-in-cost-accounting"></a>Piekļuves tiesību iespējošana vidē Izmaksu uzskaite
1. Dodieties uz Izmaksu uzskaite > Iestatījumi > Parametri.
2. Noklikšķiniet uz cilnes Vispārīgi.
3. Laukā Iespējot skatīšanas piekļuvi izmaksu objekta dimensijas elementiem atlasiet Jā.
4. Noklikšķiniet uz Saglabāt.
5. Aizvērt lapu.
6. Dodieties uz Izmaksu uzskaite > Iestatījumi > Izmaksu kontroles darbvietas konfigurācija.
7. Noklikšķiniet uz Rediģēt.
8. Laukā Publicēts atlasiet Jā.
    * Atlasot Jā, lietotājs, kuram ir piešķirta viena no tālāk minētajām četrām lomām, var redzēt pārskatus izmaksu kontroles darbvietā: izmaksu uzskaites vadītājs, izmaksu grāmatvedis, izmaksu grāmatvedības darbinieks un izmaksu objekta kontrolieris. Atlasot Nē, tikai lietotājs, kuram ir piešķirta viena no tālāk minētajām četrām lomām, var redzēt pārskatus: izmaksu uzskaites vadītājs un izmaksu grāmatvedības darbinieks.    
9. Noklikšķiniet uz Saglabāt.

