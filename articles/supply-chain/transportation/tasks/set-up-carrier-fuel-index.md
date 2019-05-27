---
title: Pārvadātāja degvielas rādītāja iestatīšana
description: Šajā ceļvedī parādīts, kā izveidot degvielas rādītāja reģionu, degvielas rādītāju un pārvadātāja degvielas rādītāju.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552096"
---
# <a name="set-up-a-carrier-fuel-index"></a>Pārvadātāja degvielas rādītāja iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā ceļvedī parādīts, kā izveidot degvielas rādītāja reģionu, degvielas rādītāju un pārvadātāja degvielas rādītāju. Degvielas rādītāja reģions norāda, uz kuru reģionu degvielas rādītājs attiecas, un degvielas rādītājs norāda degvielas cenu noteiktā laika periodā. Lai atspoguļotu degvielas cenu izmaiņas laika gaitā, ar pārvadātāju varat saistīt vairākus degvielas rādītājus.  Šos uzdevumus parasti veic transportēšanas koordinators. Šo procedūru varat lietot demonstrācijas datu uzņēmumā USMF vai savos datos.


## <a name="create-a-fuel-index-region"></a>Degvielas rādītāja reģiona izveide
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Degvielas rādītāji > Degvielas rādītāju reģioni.
    * Vispirms ir jāizveido dažādi reģioni, kuros darbojas jūsu uzņēmums un tiek aprēķinātas citas degvielas izmaksas.  
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Reģions.
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Noklikšķiniet uz Saglabāt.

## <a name="create-a-fuel-index"></a>Degvielas rādītāja izveide
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Degvielas rādītāji > Degvielas rādītāji.
    * Iestatītajiem reģioniem ir jāievada pašreizējās degvielas cenas.  
2. Noklikšķiniet uz Jauns.
3. Laukā Reģions noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Ievadiet skaitli laukā Cena par galonu.
6. Laukā Spēkā stāšanās datums un laiks ievadiet datumu un laiku.
7. Noklikšķiniet uz Saglabāt.

## <a name="create-a-carrier-fuel-index"></a>Pārvadātāja degvielas rādītāja izveide
1. Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Degvielas rādītāji > Pārvadātāju degvielas rādītāji.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Pārvadātāja degvielas rādītājs.
4. Apraksta laukā ierakstiet vērtību.
5. Klikšķiniet Jauns.
6. Laukā Spēkā stāšanās datums un laiks ievadiet datumu un laiku.
7. Ievadiet skaitli laukā CPG No.
    * Šajā piemērā varat iestatīt CPG No laukā vērtību 1,95.  
8. Ievadiet skaitli laukā CPG Līdz.
    * Šajā piemērā varat iestatīt CPG Uz laukā vērtību 2.  
9. Ievadiet skaitli laukā Procenti.
    * Šajā piemērā varat iestatīt procentu vērtību 3.  
10. Laukā Valūta noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Noklikšķiniet uz Saglabāt.

