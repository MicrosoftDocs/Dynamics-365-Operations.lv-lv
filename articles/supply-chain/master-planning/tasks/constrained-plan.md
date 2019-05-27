---
title: Ierobežotā plāna ģenerēšana
description: Šajā procedūrā ir parādīts, kā izveidot plānu, kurš ņem vērā gan materiālu, gan noslodzes ierobežojumus.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556027"
---
# <a name="generate-a-constrained-plan"></a>Ierobežotā plāna ģenerēšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

