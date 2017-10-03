--- 
title: "Kanban kārtulas izveide, izmantojot Kanban rindas notikumu"
description: "Ar šo procedūru tiek izveidots Kanban nosacījums, izmantojot Kanban rindas notikuma iestatījumu izvilkuma aktivizēšanai no procesa aktivitātes."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: cc8c3ff5e98ccce56a7a19b16c1aceac650cdf5a
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a>Kanban kārtulas izveide, izmantojot Kanban rindas notikumu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ar šo procedūru tiek izveidots Kanban nosacījums, izmantojot Kanban rindas notikuma iestatījumu izvilkuma aktivizēšanai no procesa aktivitātes. Kanban nosacījums tiek aktivizēts ar Kanban procesa aktivitāti un ar daudzumu, kas katrs ir vienāds ar vai lielāks par 25. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad viņi sagatavo jaunas vai modificētas preces ražošanu racionālā vidē.


## <a name="create-a-kanban-rule"></a>Kanban nosacījumu izveide
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Papildināšanas stratēģija atlasiet "Notikums".
    * Šādi Kanban tiek ģenerēti tieši no pieprasījuma. Šī procedūra tiek izmantota, lai iestatītu kārtulas, kas definē pasūtījuma veikšanas scenāriju.  
4. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Ievadiet vai atlasiet vērtību SpeakerAssemblyAndPolish. Pirmā ražošanas Kanban nosacījuma aktivitāte ir procesa aktivitāte ražošanas plūsmā. Kad atlasāt šo aktivitāti, aktivitātes derīguma datumi tiek kopēti uz Kanban nosacījumu derīguma datumiem.  
5. Izvērsiet sadaļu Detalizēti.
6. Laukā Prece ierakstiet “L0001”.
7. Izvērsiet sadali Notikumi.
8. Laukā Kanban rindas notikums atlasiet “Automātisks”.
    * Šādi notikumu Kanban tiek ģenerēti pēc pieprasījuma.  Šis lauks tiek izmantots, lai konfigurētu Kanban nosacījumus, kuri papildina materiālu, kas ir nepieciešams lejupstraumes procesa aktivitātei. Kad atlasāt Automātisks, notikumu Kanban tiek izveidoti ar pieprasījumu. Šis iestatījums ir ieteicams, ja ražošanu plānojat izpildīt tajā pašā dienā.  
9. Iestatiet Minimālais notikumu daudzums uz "25".
    * Notikumu Kanban tiek ģenerēti, kad pieprasījuma daudzums ir vienāds ar vai lielāks par vērtību šajā laukā. Tas ir noderīgi, ja pasūtījuma daudzumu, kas ir mazāks par šī lauka vērtību, vēlaties ražot vienā mašīnā, bet daudzumu, kas ir lielāks par šī lauka vērtību, vēlaties ražot citā mašīnā.  
10. Noklikšķiniet uz Saglabāt.

## <a name="create-sales-order-and-trigger-kanban-chain"></a>Izveidot pārdošanas pasūtījumu un aktivizēt Kanban ķēdi
1. Pārejiet uz sadaļu Pārdošana un mārketings > Pārdošanas pasūtījumi > Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Debitora konts US-003, Forest Wholesales.  
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods ierakstiet L0001.
    * L0001 ir krājums, kuram jūs izveidojāt šo Kanban nosacījumi.  
6. Daudzuma laukā iestatiet vērtību 27.
    * Tā kā vērtība 27 ir lielāka par Kanban nosacījuma minimālo daudzumu 25, tad ar šo tiks aktivizēts notikuma Kanban.  
7. Laukā Vieta ierakstiet “1”.
8. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
    * Atlasiet noliktavu 13.  
9. Noklikšķiniet uz Saglabāt.

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a>Skatīt Kanban nosacījuma ģenerētu Kanban
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Izvērsiet sadaļu Vairāki Kanban.
    * Ņemiet vērā, ka Kanban vērtībai 27 tika izveidots, lai apstrādātu aktivitāti, pamatojoties uz izveidoto Kanban nosacījumu.  
    * Šis ir pēdējais solis.  


