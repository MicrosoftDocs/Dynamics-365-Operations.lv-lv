---
title: Kanban atvilkuma kārtulas izveide
description: Šī procedūra parāda iestatījumu, kas ir nepieciešams, lai izveidotu atvilkuma kanban nosacījumu, materiāla pārvietošanai racionālās vidē.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba30e9d09e9eeb0cd7428aafc1195d6b7e7caaa4
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574477"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Kanban atvilkuma kārtulas izveide

[!include [banner](../../includes/banner.md)]

Šī procedūra parāda iestatījumu, kas ir nepieciešams, lai izveidotu atvilkuma Kanban nosacījumu materiāla pārvietošanai racionālā vidē. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jauna vai modificēta materiāla papildināšanai.


## <a name="create-new-kanban-rule"></a>Jaunu Kanban nosacījumu izveide
1. Dodieties uz Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Veids atlasiet 'Atvilkums'.
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
    * Tas ir Kanban daudzums, kuram jābūt aktīvam. Šajā gadījumā, 2 Kanban pārsūta pa 5.  
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]