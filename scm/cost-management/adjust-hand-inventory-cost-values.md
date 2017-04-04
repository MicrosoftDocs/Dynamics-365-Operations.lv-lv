---
title: "Rīcībā esošo krājumu izmaksu vērtību koriģēšana"
description: "Lapu Rīcībā esošo krājumu koriģēšana var izmantot, lai pēc krājumu slēgšanas procesa palaišanas koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Rīcībā esošo krājumu izmaksu vērtību koriģēšana

Lapu Rīcībā esošo krājumu koriģēšana var izmantot, lai pēc krājumu slēgšanas procesa palaišanas koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību.

Lapu **Rīcībā esošo krājumu koriģēšana** var izmantot, lai koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību pēc krājumu slēgšanas procesa palaišanas. **Piezīme:** atvērt **pieejamo krājumu korekcija** lapa par **slēgšanas un pielāgošanas** lapu, atlasiet pabeigto krājumu tuvu procesa ieraksts un pēc tam noklikšķiniet uz **korekciju**&gt;**rīcībā**. **Piemērs.** Februārī jums ir šādas transakcijas:

-   1. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 2 un izmaksām ar summu 10,00 USD;
-   5. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 1 un izmaksām ar summu 13,00 USD;
-   19. februāris: krājumu finanšu izejas plūsma daudzumam ar vērtību 1 un kārtējām vidējām izmaksām ar summu 11,00 USD.

Šis vienums tika izveidota pirmais iekšā, pirmais ārā (FIFO) krājumu modeļu un krājumu tuvumā tika veikta gada 28. februārī. USD 11.00 darījuma finansiālo jautājumu tiks nosegti finanšu kvīti, kas datēts 1. februāris, un būs jākoriģē, USD 1.00. Atvērto krājumu daudzumi būs redzami šādās krājumu ieejas plūsmās:

-   1. februāris: daudzums ar vērtību 1 un izmaksas ar summu 10,00 USD.
-   5. februāris: daudzums ar vērtību 1 un izmaksas ar summu 13,00 USD.

Lai šiem diviem krājumiem iestatītu izmaksas USD 15,00 apjomā, izmantojiet rīcībā esošās korekcijas opciju, lai koriģētu atvērtos rīcībā esošos daudzumus no pēdējā krājumu aizvēršanas perioda. **Piezīme.** Rīcībā esošās korekcijas transakcijas grāmatošanas datums būs pēdējās krājumu slēgšanas datums. Šo datumu nevar modificēt.


