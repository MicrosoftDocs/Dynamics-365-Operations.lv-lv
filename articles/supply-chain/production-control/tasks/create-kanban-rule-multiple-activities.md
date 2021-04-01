---
title: Kanban kārtulas izveide vairākām aktivitātēm
description: Šajā procedūrā ir parādīts, kā izveidot Kanban nosacījumu, kas ietver vairākas aktivitātes no ražošanas plūsmas.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcf507611d7f85800b2012e8372d5f91bbc8d724
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255185"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Kanban kārtulas izveide vairākām aktivitātēm

[!include [banner](../../includes/banner.md)]

Šajā procedūrā ir parādīts, kā izveidot Kanban nosacījumu, kas ietver vairākas aktivitātes no ražošanas plūsmas. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad viņi sagatavo jaunas vai modificētas preces ražošanu racionālā vidē.


## <a name="create-a-new-kanban-rule"></a>Izveidot jaunu Kanban nosacījumu
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Papildināšanas stratēģija atlasiet “Plānots”.
4. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Atlasiet vērtību SpeakerAssemblyAndPolish.  
5. Atzīmējiet izvēles rūtiņu Vairākas aktivitātes.
    * Mērķis ir Kanban nosacījumā iekļaut vairākas aktivitātes. Ceļu ražošanas plūsmā jūs izvēlaties, kad atlasāt pēdējo plāna aktivitāti.  
6. Laukā Pēdējā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Atlasiet vērtību SpeakerTestAndPackaging. Pēc vērtības atlasīšanas automātiski tiek atvērta lapa. Atlasiet Kanban plūsmu SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Noklikšķiniet uz OK.  
7. Izvērsiet sadaļu Detalizēti.
8. Laukā Prece ievadiet vai atlasiet kādu vērtību.
    * Atlasiet krājumu L0006.  

## <a name="create-kanban-and-view-jobs"></a>Izveidot Kanban un skatīt darbus
1. Izvērsiet sadaļu Vairāki Kanban.
2. Noklikšķiniet uz Pievienot.
3. Laukā Jaunu Kanban skaits ievadiet “1”.
    * Šādi tiks izveidots viens Kanban.  
4. Iestatiet vērtību 3 laikā Preču daudzums.
    * Kanban apstrādās 3 preces.  
5. Laukā Izpildes datums/laiks ievadiet datumu un laiku.
    * Varat ievadīt Šodien.  
6. Noklikšķiniet uz Izveidot.
7. Noklikšķiniet uz Detaļas.
    * Ievērojiet, ka šim Kanban ir divi procesa darbi no ražošanas plūsmas. Pirmais ir SpeakerAssemblyAndPolish, un otrais ir SpeakerTestAndPackaging.  
    * Šis ir pēdējais solis!  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]