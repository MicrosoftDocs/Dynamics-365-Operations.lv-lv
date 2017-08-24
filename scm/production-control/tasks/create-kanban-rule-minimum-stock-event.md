--- 
title: "Kanban kārtulas izveide, izmantojot minimālo krājumu notikumu"
description: "Šī procedūra koncentrējas uz iestatīšanu, kas ir nepieciešama, lai izveidotu Kanban nosacījumu, izmantojot minimālo krājumu notikumu, tādējādi nodrošinot, ka konkrētā novietojumā vienmēr ir pieejama konkrēta prece."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: c655f9e2cb3967a44c357f16d18884ec0bc55357
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# Kanban kārtulas izveide, izmantojot minimālo krājumu notikumu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra koncentrējas uz iestatīšanu, kas ir nepieciešama, lai izveidotu Kanban nosacījumu, izmantojot minimālo krājumu notikumu, tādējādi nodrošinot, ka konkrētā novietojumā vienmēr ir pieejama konkrēta prece. Kanban nosacījums tiek izveidots, lai materiālu pārsūtītu uz novietojumu, kad krājumu līmenis kļūst mazāks nekā 200 gab. Palaižot pieprasījuma notikuma apstrādi, tiek izveidoti nepieciešamie Kanban. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad viņi sagatavo jaunas vai modificētas preces ražošanu racionālā vidē.


## Izveidot jaunu Kanban nosacījumu
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Veids, atlasiet 'Atvilkums'.
    * Šis tips tiek izmantots, lai izveidotu pārsūtīšanas Kanban.  
4. Laukā Papildināšanas stratēģija atlasiet "Notikums".
    * Notikumu stratēģija tiek izmantota, lai izveidotu pārsūtīšanas Kanban, pamatojoties uz notikumu. Vēlāk šajā procedūrā jūs aktivizēsiet pārsūtīšanas Kanban, izmantojot krājumu papildināšanu.  
5. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Ievadiet vai Atlasiet ReplenishSpeakerComponents. Šai pārsūtīšanas aktivitātei ir ieejas plūsmas (izvades) noliktava un novietojums 12, kas nozīmē, ka materiāli tiks pārvietoti uz novietojumu 12 noliktavā 12.  
6. Izvērsiet sadaļu Detalizēti.
7. Laukā Prece ievadiet vai atlasiet kādu vērtību.
    * Atlasiet M0007.  
8. Izvērsiet sadali Notikumi.
9. Laukā Krājumu papildināšanas notikums “Partija”.
    * Ar šo tiek izveidoti Kanban materiālu vajadzību izpildīšanai saistītajā novietojumā, kamēr notiek Pieprasījuma notikuma apstrāde.  

## Iestatīt krājumam minimālo daudzumu
1. Noklikšķiniet, lai sekotu saitei laukā Prece.
2. Noklikšķiniet, lai sekotu saitei laukā Krājuma kods.
3. Izvērsiet preces attēla papildinformāciju.
4. Darbību rūtī noklikšķiniet uz Plānot.
5. Noklikšķiniet uz Krājumu vajadzība.
6. Noklikšķiniet uz Jauns.
7. Sarakstā atzīmējiet atlasīto rindu.
8. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
    * Iestatiet Noliktava uz 12.  
9. Vērtību Minimums iestatiet uz “200”.

## Palaist pakešveida notikuma izveidošanas darbu
1. Doties uz Ražošanas kontrole > Periodiskie uzdevumi > Kanban darbu pakešveida apstrāde > Pieprasījuma notikuma apstrāde.
2. Noklikšķiniet uz OK.
3. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet Kanban nosacījumu, kuru izveidojāt iepriekš.  
5. Izvērsiet sadaļu Vairāki Kanban.
    * Ņemiet vērā, ka Kanban tika izveidots, lai nepieciešamos materiālus pārsūtītu uz noliktavu 12.  


