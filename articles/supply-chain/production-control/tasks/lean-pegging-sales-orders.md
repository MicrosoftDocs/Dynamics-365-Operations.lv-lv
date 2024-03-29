---
title: Racionālā piesaiste no pārdošanas pasūtījumiem
description: Šajā procedūrā aprakstīts piesaistes koka validācijas process no pārdošanas rindas, kur krājums tiek ražots ar Kanban.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8eca21f8bd988ca352c07e839295b3edd9669929
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580628"
---
# <a name="lean-pegging-from-sales-orders"></a>Racionālā piesaiste no pārdošanas pasūtījumiem

[!include [banner](../../includes/banner.md)]

Šajā procedūrā aprakstīts piesaistes koka validācijas process no pārdošanas rindas, kur krājums tiek ražots ar Kanban. Pēc piesaistes koka validācijas, visu Kanban darbu statuss ir Plānots. Tas ir noderīgi saistībā ar tādiem pasūtījumiem, kur pasūtījuma ņēmējam ir jānodrošina, ka ražošanu var sākt nekavējoties. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta papildu pasūtījuma ņēmējam, kas strādā aizdevumu pakalpojumu uzņēmumā.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Pārdošanas pasūtījuma izveide Kanban kontrolētam krājumam
1. Dodieties uz Visi pārdošanas pasūtījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Debitora konts ievadiet vai atlasiet kādu vērtību.
    * Lietojiet formu ASV-001.  
4. Noklikšķiniet uz OK.
5. Laukā Krājuma kods ierakstiet L0001.
6. Daudzuma laukā iestatiet vērtību 30.
    * Ir svarīgi, ka daudzuma vērtība ir lielāka par 24, lai aktivizētu notikuma Kanban nosacījumus.  

## <a name="open-a-pegging-tree"></a>Piesaistes koka atvēršana 
1. Noklikšķiniet uz Preces un piegādes.
2. Noklikšķiniet uz Skatīt piesaistes koku.
    * Ņemiet vērā! Piesaistes kokā tiek rādīti visi pārdošanas pasūtījuma rindai nepieciešamie piesaistes līmeņi. Šajā gadījumā ir divu līmeņu Kanban un visi nepieciešamie komponenti.  

## <a name="plan-the-pegging-tree"></a>Piesaistes koka plānošana
1. Kokā atlasiet Pārdošanas rinda 000832\Kanban 000558.
2. Izvērsiet sadaļu Kanban darbi.
    * Ņemiet vērā! Kanban darba statuss ir Nav plānots.  
3. Noklikšķiniet uz Plānot visu piesaistes koku.
    * Tādējādi tiks plānoti visi piesaistes kokā esošie Kanban darbi, mainot lauka Darba statuss vērtību no Nav plānots uz Plānots.  
4. Atsvaidziniet lapu.
    * Ņemiet vērā! Kanban darba statuss tika mainīts no Nav plānots uz Plānots.  
5. Koka struktūrā atlasiet Pārdošanas rinda 000832\Kanban 000558\L0001 izdošana\Kanban 000559.
    * Otrā Kanban darba status arī ir Plānots, jo visa piesaistes koka statuss ir Plānots. Ņemiet vērā! Kanban darba statuss tika mainīts no Nav plānots uz Plānots.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]