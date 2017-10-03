--- 
title: "MK rindas notikumu Kanban kārtulas izveide"
description: "Šis uzdevums fokusējas nepieciešamajam iestatījumam, lai izveidotu notikuma kanban nosacījumu, lai nodrošinātu piegādes ražošanas MK rindām, jauktā racionālā un klasiskā ražošanas vidē."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
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
ms.openlocfilehash: 97fab2f372221cd6757531088d88b28571f07ab8
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a>MK rindas notikumu Kanban kārtulas izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevums fokusējas nepieciešamajam iestatījumam, lai izveidotu notikuma kanban nosacījumu, lai nodrošinātu piegādes ražošanas MK rindām, jauktā racionālā un klasiskā ražošanas vidē. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.


## <a name="create-a-new-kanban-rule"></a>Izveidot jaunu Kanban nosacījumu
1. Dodieties uz Ražošanas kontrole > Periodiskie uzdevumi > Kanban daudzuma aprēķins > Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Veids, atlasiet 'Atvilkums'.
    * Atvilkuma tips tiek izmantots, lai izveidotu pārsūtīšanas Kanban.  
4. Laukā Papildināšanas stratēģija atlasiet "Notikums".
    * Notikumu stratēģija tiek atlasīta, lai izveidotu Kanban pārsūtīšanu, pamatojoties uz notikumu. Vēlāk, uzdevuma rokasgrāmatā, mēs to aktivizēsim, novērtējot ražošanas pasūtījumu.  
5. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Ievadiet vai Atlasiet ReplenishSpeakerComponents. Šai pārsūtīšanas aktivitātei ir saņemšanas (izdošana) noliktava un atrašanās vieta 12, kas nozīmē, ka materiāls tiks pārvietots uz atrašanās vietu noliktavā 12.  
6. Izvērsiet sadaļu Detalizēti.
7. Laukā Prece, ievadiet vai atlasiet M0001.
8. Izvērsiet sadali Notikumi.
9. Laukā MK rinda, atlasiet "Automātisks".
    * Ar MK rindas notikuma lauku iestatītu uz Automātisks, tiks izveidots kanban, lai apmierinātu materiālu vajadzības ražošanas pasūtījuma MK rindām.  
10. Aizvērt lapu.

## <a name="create-and-modify-a-new-production-order"></a>Izveidojiet un modificējiet jaunu ražošanas pasūtījumu.
1. Pārejiet uz sadaļu Ražošanas kontrole > Ražošanas pasūtījumi > Visi ražošanas pasūtījumi.
2. Noklikšķiniet uz Jauns ražošanas pasūtījums.
3. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
    * Ievadiet vai atlasiet 'L0001'. Mēs izmantojam krājumu L0001, jo krājums M0001 ir iekļauts MK krājumam L0001.  
4. Noklikšķiniet uz Izveidot.
5. Sarakstā noklikšķiniet uz saites rindā priekš L0001
6. Noklikšķiniet uz MK.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Noklikšķiniet uz Rediģēt.
9. Laukā Rindas tips atlasiet “Pieprasīta piegāde”.
    * Pieprasīta piegāde tiek atlasīta, lai aktivizētu kanban piegādes izveidi.  
10. Laukā Resursu patēriņš, atlasiet Nē.
    * Notīrot izvēles rūtiņu Resursu patēriņš, ļauj mums mainīt noliktavu.  
11. Izvērsiet sadaļu Krājuma dimensijas.
12. Laukā Noliktava ierakstiet "12".
    * Noliktava ir iestatīta uz 12, jo šī ir ražojumu noliktava atvilkuma aktivitātei.  
13. Laukā Atrašanās vieta, ierakstiet "12".
    * Atrašanās vieta ir iestatīta uz 12, jo šī ir atvilkuma aktivitātes atrašanās vieta.  
14. Aizvērt lapu.
15. Aizvērt lapu.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Novērtējiet ražošanas pasūtījumu, un skatiet izveidoto kanban
1. Noklikšķiniet uz Novērtējums.
    * Ražošanas pasūtījuma novērtēšana aktivizēs saistītā kanban izveidi, lai nodrošinātu krājumu M0001.  
2. Noklikšķiniet uz OK.
3. Aizvērt lapu.
4. Aizvērt lapu.
5. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
6. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet notikumu, ko kanban nosacījums izveidoja krājumam M0001.  
7. Izvērsiet sadaļu Vairāki Kanban.
8. Sarakstā atzīmējiet atlasīto rindu.
    * Ņemiet vērā, kanban, kas tika izveidots M0001 nodrošināšanai, prognozējamajam ražošanas pasūtījumam.  
    * Šis ir pēdējais solis!  


