---
title: Pārdošanas notikuma Kanban kārtulas izveide
description: Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumu, kas tiek izraisīts pārdošanas pasūtījuma izveides laikā.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9325bbb8d28587baeb60cdf1fc37121c236f1a10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828926"
---
# <a name="create-a-sales-event-kanban-rule"></a>Pārdošanas notikuma Kanban kārtulas izveide

[!include [banner](../../includes/banner.md)]

Šī procedūra fokusējas uz iestatījumiem, kas ir vajadzīgi, lai izveidotu Kanban nosacījumu, kas tiek izraisīts pārdošanas pasūtījuma izveides laikā. Notikuma Kanban nosacījums papildina prasības, kas cēlušās no pārdošanas pasūtījuma rindām. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei. Tie ir paredzēti procesa inženierim vai vērtību plūsmas pārvaldniekam, kad tie gatavojas jaunas vai modificētas preces ražošanai.




## <a name="create-a-new-kanban-rule"></a>Izveidot jaunu Kanban nosacījumu
1. Dodieties uz Kanban nosacījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Papildināšanas stratēģija atlasiet "Notikums".
    * Ja atlasīt Notikums, tas nozīmē, ka Kanban nosacījumu izraisa notikums, piemēram, pārdošanas pasūtījuma rindas izveide.   Tas attiecas uz jomām, kur katram Kanban jāaptver specifisku pieprasījumu.  
4. Laukā Pirmā plāna aktivitāte ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Galīgā montāža.  
5. Izvērsiet sadaļu Detalizēti.
6. Laukā Prece ievadiet vai atlasiet kādu vērtību.
    * Atlasiet L0050.  

## <a name="define-an-event"></a>Notikuma definēšana
1. Izvērsiet sadali Notikumi.
2. Laukā Pārdošanas notikums atlasiet "Automātisks".
    * Ja atlasīt pārdošanas notikumu Automātisks, šis Kanban nosacījums tiks izsaukts automātiski, pārdošanas rindai atbilstot preces un saņemšanas novietojumam. Šajā procedūrā tā ir prece L0050 noliktavā 13.  
3. Iestatiet Minimālais notikumu daudzums uz "50".
    * Ar minimālo notikumu daudzumu 50, Kanban nosacījumu izraisīs tikai notikumi ar daudzumu 50 vai vairāk.  
4. Izvērsiet sadaļu Ražošanas plūsma.
    * Ievērojiet, ka Saņemšanas vieta ir noliktava 13. Tas nozīmē, ka šis Kanban nosacījums tiks izraisīts šim novietojumam.  
    * Šajā piemērā Kanban nosacījumu izraisīs pārdošanas rinda precei L0050 ar daudzumu 50 vai vairāk noliktavā 13.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Pārdošanas rinda izveide notikuma Kanban nosacījuma izraisīšanai
1. Dodieties uz Visi pārdošanas pasūtījumi.
    * Brīdinājums tiek parādīts, kad tiek saglabāts Kanban nosacījums, kas nozīmē, ka vairāki Kanban tiks izveidoti reāllaikā pārdošanas pasūtījuma izveides laikā.  
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
    * Ievadiet daudzumu 50 vai lielāku, lai izraisītu izveidoto Kanban nosacījumu.  

## <a name="verify-that-kanban-is-created"></a>Pārbaude, vai Kanban ir izveidots
1. Noklikšķiniet uz Preces un piegādes.
2. Noklikšķiniet uz Skatīt piesaistes koku.
    * Ņemiet vērā, ka tiek izveidots Kanban ar tādu pašu daudzumu kā pārdošanas rindā. Varat arī redzēt, ko problēmām ar materiāliem vajadzēja saražot L0050. Šā ir pēdējā darbība šajā procedūrā.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]