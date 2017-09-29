--- 
title: "Atvilkuma Kanban kārtulas izveide"
description: "Šī procedūra parāda iestatījumu, kas ir nepieciešams, lai izveidotu atvilkuma kanban nosacījumu, materiāla pārvietošanai racionālās vidē."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.openlocfilehash: c3172f5c932b94b2a9e442286eb61159286297fb
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a>Atvilkuma Kanban kārtulas izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra parāda iestatījumu, kas ir nepieciešams, lai izveidotu atvilkuma kanban nosacījumu, materiāla pārvietošanai racionālās vidē. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jauna vai modificēta materiāla papildināšanai.


## <a name="create-new-kanban-rule"></a>Jaunu Kanban nosacījumu izveide
1. Dodieties uz Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Veids, atlasiet 'Atvilkums'.
    * Atvilkuma veids tiek izmantots kanban nosacījumiem, lai pārsūtītu materiālus vai preces.  
4. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Atlasiet ReplenishSpeakerComponents.   Šī aktivitātei ir iestatīta, lai pārvietotu komponentus no noliktavas 11, atrašanās vietas 11 uz noliktavu 12 un atrašanās vietu 12.  
5. Laukā Prece ievadiet vai atlasiet kādu vērtību.
    * Atlasiet M0007.  
6. Laukā Izpildes laiks ievadiet kādu skaitli.
    * Piemēram, 60.  
7. Laukā Mērvienība ievadiet vai atlasiet kādu vērtību.
    * Piemēram, Minūtes.  

## <a name="set-quantities-for-kanban"></a>Iestatiet Kanban daudzumus
1. Vienumam Noklusējuma daudzums iestatiet vērtību "5".
    * Tas ir daudzums, kas tiks pārsūtīts katram Kanban.  
2. Laukā Fiksētais Kanban daudzums ievadiet "2".
    * Tas ir Kanban daudzums, kuram jābūt aktīvam. Šajā gadījumā, katrs no 2 Kanban pārsūta 5.  
3. Laukā Minimālā brīdinājuma robeža ievadiet "1".
    * Izmantojiet, lai sekotu līdzi pilnu Kanban minimālajam skaitam, kuram jābūt galamērķī. Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.  
4. Laukā Maksimālā brīdinājuma robeža ievadiet "2".
    * Izmantojiet, lai sekotu līdzi pilnu Kanban maksimālajam skaitam, kuram jābūt galamērķī. Piemēram, tas tiek izmantots Kanban daudzuma pārskatā.  

## <a name="create-kanbans"></a>Izveidot Kanban darbus
1. Noklikšķiniet uz Saglabāt.
    * Lai Kanban varētu izveidot, Kanban nosacījumi ir jāsaglabā.  
2. Noklikšķiniet uz Pievienot.
    * Ņemiet vērā, ka nav neviena aktīva Kanban, tāpēc ieteicamais "Jauno Kanban skaits" ir 2. Tas ir vienāds ar "Fiksēto Kanban daudzumu".  
3. Noklikšķiniet uz Izveidot.
    * Šādi tiks izveidoti divi Kanban.  
    * Ņemiet vērā, ka šim atvilkuma Kanban nosacījumam tika izveidoti 2 Kanban pa 5 katrs.  Šā ir pēdējā darbība šajā procedūrā.  

