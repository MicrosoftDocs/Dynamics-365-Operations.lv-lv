--- 
title: "Ierobežotā plāna ģenerēšana"
description: "Šajā procedūrā ir parādīts, kā izveidot plānu, kurš ņem vērā gan materiālu, gan noslodzes ierobežojumus."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6735f0287e7a61ff494a48c97c44480c6038097c
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-constrained-plan"></a>Ierobežotā plāna ģenerēšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā izveidot plānu, kurš ņem vērā gan materiālu, gan noslodzes ierobežojumus. Šis plāns nodrošina, ka ražošana nesākas, pirms materiāli kļūst pieejami, un resursiem netiek pārsniegta rezervācija. 

Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta ražošanas plānotājam.


## <a name="set-up-a-constrained-plan"></a>Iestatīt ierobežotu plānu
1. Noklikšķiniet uz Vispārējā plānošana.
2. Noklikšķiniet uz Vispārējie plāni.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Piemērs: StaticPlan  
4. Laukā Ierobežota noslodze atlasiet Jā.
5. Laukā Ierobežotās noslodzes periods ievadiet “30”.
6. Izvērsiet sadaļu Periodi dienās.
7. Laukā Noslodze atlasiet Jā.
8. Laukā Noslodzes plānošanas periods (dienās) ievadiet kādu skaitli.
    * Piemērs: 60  
9. Laukā Aprēķinātās aizkaves atlasiet Jā.
10. Laukā Aprēķināt aizkaves periodu (dienās) ievadiet kādu skaitli.
    * Piemērs: 60  
11. Izvērsiet sadaļu Aprēķinātās aizkaves.
12. Laukā Pieprasījuma datumam pieskaitīt aprēķināto aizkavi atlasiet Jā.
13. Laukā Pieprasījuma datumam pieskaitīt aprēķināto aizkavi atlasiet Jā.
14. Laukā Pieprasījuma datumam pieskaitīt aprēķināto aizkavi atlasiet Jā.
15. Aizvērt lapu.

## <a name="create-a-constrained-plan"></a>Ierobežota plāna izveide
1. Noklikšķiniet uz Palaist.
2. Laukā Vispārējais plāns ievadiet vai atlasiet kādu vērtību.
    * Atlasiet plānu, kuram esat iestatījis ierobežojumus.  
3. Noklikšķiniet uz OK.
    * Tas var aizņemt kādu laiku.  
4. Noklikšķiniet uz Plānotie pasūtījumi.


