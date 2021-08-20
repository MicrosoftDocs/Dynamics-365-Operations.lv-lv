---
title: Kanban kārtulas izveide, izmantojot minimālo krājumu notikumu
description: Šī procedūra koncentrējas uz iestatīšanu, kas ir nepieciešama, lai izveidotu Kanban nosacījumu, izmantojot minimālo krājumu notikumu, tādējādi nodrošinot, ka konkrētā novietojumā vienmēr ir pieejama konkrēta prece.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3213fac9875a1fd7824be71236cc0d2efb3274a81b33335756a0dd7391fcbfdb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745530"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Kanban kārtulas izveide, izmantojot minimālo krājumu notikumu

[!include [banner](../../includes/banner.md)]

Šī procedūra koncentrējas uz iestatīšanu, kas ir nepieciešama, lai izveidotu Kanban nosacījumu, izmantojot minimālo krājumu notikumu, tādējādi nodrošinot, ka konkrētā novietojumā vienmēr ir pieejama konkrēta prece. Kanban nosacījums tiek izveidots, lai materiālu pārsūtītu uz novietojumu, kad krājumu līmenis kļūst mazāks nekā 200 gab. Palaižot pieprasījuma notikuma apstrādi, tiek izveidoti nepieciešamie Kanban. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo uzdevumu, ir USMF. Šis uzdevums ir paredzēts procesa inženierim vai vērtību plūsmas pārvaldniekam, kad viņi sagatavo jaunas vai modificētas preces ražošanu racionālā vidē.


## <a name="create-a-new-kanban-rule"></a>Izveidot jaunu Kanban nosacījumu
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

## <a name="set-the-minimum-quantity-for-the-item"></a>Iestatīt krājumam minimālo daudzumu
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

## <a name="run-the-batch-event-creation-job"></a>Palaist pakešveida notikuma izveidošanas darbu
1. Doties uz Ražošanas kontrole > Periodiskie uzdevumi > Kanban darbu pakešveida apstrāde > Pieprasījuma notikuma apstrāde.
2. Noklikšķiniet uz OK.
3. Pārejiet uz sadaļu Preču informācijas pārvaldība > Lean manufacturing > Kanban nosacījumi.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
    * Atlasiet Kanban nosacījumu, kuru izveidojāt iepriekš.  
5. Izvērsiet sadaļu Vairāki Kanban.
    * Ņemiet vērā, ka Kanban tika izveidots, lai nepieciešamos materiālus pārsūtītu uz noliktavu 12.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]