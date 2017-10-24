--- 
title: "Secības ražošanas darbi procesa ražošanai"
description: "Šī procedūra izmanto krāsas produktus kā piemēru, lai parādītu kā izkārtot sērijā plānotos pasūtījumus atbilstoši krāsu un pakotnes lieluma prioritātei."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a25a4575ca1600b07b2dac5949c8775bcd162650
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>Secības ražošanas darbi procesa ražošanai

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra izmanto krāsas produktus kā piemēru, lai parādītu kā izkārtot sērijā plānotos pasūtījumus atbilstoši krāsu un pakotnes lieluma prioritātei. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USPI. Šī procedūra ir paredzēta ražošanas plānotājam.


## <a name="run-master-planning-for-uspi"></a>Palaist vispārējo USPI plānošanu
1. Doties uz Vispārējā plānošana > Vispārējā plānošana > Palaist > Vispārējā plānošana.
2. Laukā Vispārējais plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet Vispārējais plāns.  
4. Noklikšķiniet uz OK.
    * Tas aizsāks vispārējo plānošanu, ieskaitot sērijas procesu. Šis process var aizņemt dažas minūtes.  

## <a name="view-planned-orders-for-the-paint-products"></a>Skatiet plānotos pasūtījumus krāsas precēm
1. Doties uz Vispārējā plānošana > Vispārējā plānošana > Plānotie pasūtījumi.
2. Izvērsiet detalizētu Krājuma papildinformāciju.
3. Izvērsiet detalizētu Grafika papildinformāciju.
4. Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
5. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet Vispārējais plāns.  
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
7. Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P300.
    * Atbloķējiet, lai ritinātu pa labi, lai varētu skatīt pasūtījuma un piegādes datumu. Ņemiet vērā, ka šo krājumu pasūtījuma datums ir Šodiena, un plānoto pasūtījumu piegādes datumiem nav noteikta secība pēc krāsas un iepakojuma izmēra prioritātes, kā parādīts preces nosaukumā. Jūs varat virzīt peli virs krājuma koda, lai skatītu preces nosaukumu un prioritāti.  

## <a name="sequence-planned-orders-for-paint"></a>Ierindot plānotos krāsas pasūtījumus
1. Aizvērt lapu.
2. Doties uz Vispārējā plānošana > Vispārējā plānošana > Ierindotie plānotie pasūtījumi.
3. Izvērsiet detalizētu Krājuma papildinformāciju.
4. Izvērsiet detalizētu Grafika papildinformāciju.
    * Piezīme: Šeit jūs redzat, ka sākuma datuma/laika secība plānotajiem pasūtījumiem tiek noteikta pēc krāsas un iepakojuma lieluma, ar 28 dienu laika intervālu. Šie periodi tiek definēti ar skaitli laukā Kampaņa. Ierindoto plānoto pasūtījumu forma darbojas tāpat kā parastas plānoto pasūtījumu formas, un ražošanas plānotājs var apstiprināt plānotos pasūtījumus šeit.  
5. Atzīmēt visas rindas.
6. Noklikšķiniet uz Akceptēt.
    * Tiks atjaunināti plānotie pasūtījumi ar atlasīto sērijas darbību - Atlikšana vai Turpināšana.  

## <a name="verify-the-sequence-of-the-planned-orders"></a>Pārbaudiet plānoto pasūtījumu secību
1. Aizvērt lapu.
2. Doties uz Vispārējā plānošana > Vispārējā plānošana > Plānotie pasūtījumi.
3. Izvērsiet detalizētu Krājuma papildinformāciju.
4. Izvērsiet detalizētu Grafika papildinformāciju.
5. Laukā Plāns noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet Vispārējais plāns.  
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Izmantojiet ātro filtru, lai Krājuma numura laukā filtrētu pēc vērtības P300.
    * Ņemiet vērā, ka pasūtījumiem tagad tiek noteikta secība atbilstoši krāsu un izmēru prioritātei, un plānoto pasūtījumu izpilde tiek sākta no pirmā pasūtījuma un piegādes datuma. Pārbaudiet pasūtījuma datuma kolonna vai Sākuma datumu grafika papildinformācijas rūtī.  


