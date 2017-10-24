--- 
title: "Pārdošanas notikumu Kanban kārtulas izveide"
description: "Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumus, kas tiek izraisīti pārdošanas pasūtījuma izveides laikā."
author: ChristianRytt
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
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f1f66157b2e74ad1b490e10112cbc121ac9826fb
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-sales-event-kanban-rule"></a>Pārdošanas notikumu Kanban kārtulas izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumus, kas tiek izraisīti pārdošanas pasūtījuma izveides laikā. Notikumu Kanban nosacījumi papildina prasības, kas cēlušās no pārdošanas pasūtījuma rindām. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Tie ir paredzēti procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.




## <a name="create-a-new-kanban-rule"></a>Izveidot jaunu Kanban nosacījumu
1. Dodieties uz Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Papildināšanas stratēģija atlasiet "Notikums".
    * Ja atlasīt Notikums, tas nozīmē, ka Kanban nosacījumus izraisa notikums, piemēram, pārdošanas pasūtījuma rindas izveide.   Tas attiecas uz jomām, kur katram Kanban jāaptver specifisku pieprasījumu.  
4. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Galīgā montāža.  
5. Izvērsiet sadaļu Detalizēti.
6. Laukā Prece ievadiet vai atlasiet kādu vērtību.
    * Atlasiet L0050.  

## <a name="define-an-event"></a>Notikuma definēšana
1. Izvērsiet sadali Notikumi.
2. Laukā Pārdošanas notikums atlasiet "Automātisks".
    * Ja atlasīt pārdošanas notikumu Automātisks, šie Kanban nosacījumi tiks izsaukti automātiski, kad pārdošanas rinda atbilst preču un saņemšanas novietojumam. Šajā procedūrā tā ir prece L0050 noliktavā 13.  
3. Iestatiet Minimālais notikumu daudzums uz "50".
    * Ar minimālo notikumu daudzumu 50, Kanban nosacījumus izraisīs tikai notikumi ar daudzumu 50 vai vairāk.  
4. Izvērsiet sadaļu Ražošanas plūsma.
    * Ievērojiet, ka Saņemšanas vieta ir noliktava 13. Tas nozīmē, ka šie Kanban nosacījumi tiks izraisīti šim novietojumam.  
    * Šajā piemērā Kanban nosacījumus izraisīs pārdošanas rinda precei L0050 ar daudzumu 50 vai vairāk noliktavā 13.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Pārdošanas rinda izveide notikumu Kanban nosacījumu izraisīšanai
1. Dodieties uz Visi pārdošanas pasūtījumi.
    * Brīdinājums tiek parādīts, kad tiek saglabāti Kanban nosacījumi, kas nozīmē, ka vairāki Kanban tiks izveidoti reāllaikā pārdošanas pasūtījuma izveides laikā.  
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet US-003.  
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods ierakstiet L0050.
6. Laukā Vieta ierakstiet “1”.
    * Atlasiet Vieta 1, jo Noliktava 13 atrodas Vietā 1.  
7. Laukā Noliktava ievadiet vai atlasiet kādu vērtību.
    * Iestatiet Noliktava uz 13.  
8. Daudzuma laukā iestatiet vērtību 75.
    * Ievadiet daudzumu 50 vai lielāku, lai izraisītu izveidotos Kanban nosacījumus.  

## <a name="verify-that-kanban-is-created"></a>Pārbaude, vai Kanban ir izveidots
1. Noklikšķiniet uz Preces un piegādes.
2. Noklikšķiniet uz Skatīt piesaistes koku.
    * Ņemiet vērā, ka tiek izveidots Kanban ar tādu pašu daudzumu kā pārdošanas rindā. Varat arī redzēt, ko problēmām ar materiāliem vajadzēja saražot L0050. Šā ir pēdējā darbība šajā procedūrā.  


