---
title: Kanban daudzuma ieteikumu aprēķins
description: Šajā procedūrā parādīts, kā optimizēt Kanban lielumu un daudzumu konkrētam Kanban nosacījumam, izmantojot Kanban daudzuma aprēķinus.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 540dd32c5da5859ef5e69f55d6806eada90bc840
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "348990"
---
# <a name="calculate-kanban-quantity-suggestions"></a>Kanban daudzuma ieteikumu aprēķins

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā parādīts, kā optimizēt Kanban lielumu un daudzumu konkrētam Kanban nosacījumam, izmantojot Kanban daudzuma aprēķinus. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta vērtību plūsmas pārvaldniekam. Šīs procedūras priekšnosacījums ir paveikta procedūra Jaunas Kanban daudzuma aprēķināšanas politikas pievienošana Kanban nosacījumam.


## <a name="create-a-kanban-quantity-calculation"></a>Kanban daudzuma aprēķina izveide
1. Pārejiet uz sadaļu Ražošanas kontrole > Periodiskie uzdevumi > Kanban daudzuma aprēķins > Aprēķināt Kanban daudzumu.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet Speaker2016.
4. Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Atlasiet politiku, ko izveidojāt procedūrā Jaunas Kanban daudzuma aprēķināšanas politikas pievienošana Kanban nosacījumam. Piemēram, Speaker2016.  
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Laukā Nosacījums aktīvs no datuma iestatiet datumu un laiku 2012-12-17T08:00:00'.
    * Šis datums tiek izmantots, lai noteiktu, kuri fiksētie Kanban nosacījumi ir ietverti Kanban daudzuma aprēķinos.  
7. Laukā Izpildītā pieprasījuma perioda sākuma datums iestatiet datumu un laiku 2012-11-17T09:00:00.
    * Datums, no kura tiek iekļauti pagātnes pieprasījuma darījumi, lai aprēķinātu Kanban daudzumu.  
8. Laukā Izpildītā pieprasījuma perioda beigu datums iestatiet datumu un laiku 2012-12-17T07:59:59.
    * Datums, līdz kuram pagātnes pieprasījuma darījumi tiek iekļauti, lai aprēķinātu Kanban daudzumu.  
9. Laukā Pieprasījuma perioda sākuma datums iestatiet datumu un laiku 2012-12-17T08:00:00.
    * Datums, no kura tiek iekļauti pašreizējie pieprasījuma darījumi, lai aprēķinātu Kanban daudzumu.  
10. Laukā Pieprasījuma perioda beigu datums iestatiet datumu un laiku 2013-01-16T07:59:59.
    * Datums, līdz kuram tiek iekļauti pašreizējie pieprasījuma darījumi, lai aprēķinātu Kanban daudzumu.  

## <a name="generate-kanban-quantity-proposal"></a>Kanban daudzuma priekšlikuma ģenerēšana
1. Noklikšķiniet uz Saglabāt.
2. Noklikšķiniet uz Ģenerēt.
    * Tas ģenerē Kanban daudzuma priekšlikuma rindu Kanban nosacījumam 000020.  

## <a name="run-kanban-quantity-calculation"></a>Kanban daudzuma aprēķināšanas izpilde
1. Noklikšķiniet uz Aprēķināt.
    * Tas aprēķina Kanban daudzuma priekšlikumu.  
2. Noklikšķiniet uz OK.
3. Sarakstā atzīmējiet atlasīto rindu.
    * Ievērojiet, ka ieteicamais Kanban daudzums ir 2.  

## <a name="change-product-quantity-and-calculate-again"></a>Preču daudzuma maiņa un atkārtots aprēķins
1. Iestatiet vērtību 5 laikā Preču daudzums.
2. Noklikšķiniet uz Aprēķināt.
3. Noklikšķiniet uz OK.
    * Ievērojiet, ka ar Kanban daudzumu 5, ieteikums tiek mainīts uz Kanban daudzumu 4.  
    * To ietekmē fakts, ka ar zemāku preču daudzumu nepieciešams vairāk Kanban sistēmu, lai apmierinātu pieprasījumu.  

## <a name="update-kanban-rule"></a>Kanban nosacījuma atjaunināšana
1. Laukā Nosacījuma spēkā stāšanās datums ievadiet datumu un laiku.
    * Iestatiet nākotnes datumu laukā Nosacījums aktīvs no datuma. Piemēram, šodiena + viens gads.  
2. Noklikšķiniet uz Atjaunināt.
3. Noklikšķiniet uz OK.
4. Aizvērt lapu.

## <a name="validate-change-on-kanban-rule"></a>Kanban nosacījuma izmaiņu pārbaude
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet Kanban nosacījumu, kas tika izveidots iepriekšējā apakšuzdevumā. Tam būtu jābūt pirmajam Kanban nosacījumam sarakstā, kad tas sakārtots pēc numura.  
3. Pārslēdziet sadaļas Detalizēti paplašinājumu.
    * Ievērojiet spēkā stāšanās datumu, kas nozīmē, ka šis nosacījums līdz šim datumam nav aktivizēts.  
4. Pārslēdziet sadaļas Daudzumi paplašinājumu.
    * Ņemiet vērā, ka tas ir noklusētais daudzums, kuru ievadījāt Kanban daudzuma aprēķinā.  
    * Ņemiet vērā, ka 4 ir fiksētais Kanban daudzums, kas noteikts Kanban daudzuma aprēķinā.  
5. Noklikšķiniet uz cilnes ListPanel.

