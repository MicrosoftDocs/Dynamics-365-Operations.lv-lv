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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a62d8d453be096dda221415437e78c695f3e5cf7
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Rīcībā esošo krājumu izmaksu vērtību koriģēšana

[!include[banner](../includes/banner.md)]


Lapu Rīcībā esošo krājumu koriģēšana var izmantot, lai pēc krājumu slēgšanas procesa palaišanas koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību.

Lapu **Rīcībā esošo krājumu koriģēšana** var izmantot, lai koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību pēc krājumu slēgšanas procesa palaišanas. **Piezīme.** Lai atvērtu lapu **Rīcībā esošo krājumu koriģēšana**, lapā **Slēgšana un koriģēšana** atlasiet pabeigta krājuma slēgšanas procesa ierakstu un pēc tam noklikšķiniet uz **Korekcija** &gt; **Rīcībā esošs**. **Piemērs.** Februārī jums ir šādas transakcijas:

-   1. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 2 un izmaksām ar summu 10,00 USD;
-   5. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 1 un izmaksām ar summu 13,00 USD;
-   19. februāris: krājumu finanšu izejas plūsma daudzumam ar vērtību 1 un kārtējām vidējām izmaksām ar summu 11,00 USD.

Šim krājumam bija iestatīts krājumu modelis “pirmais iekšā, pirmais ārā” (first in, first out – FIFO), un krājuma slēgšana notika 28. februārī. Finanšu izejas plūsmas transakcija 11,00 USD apjomā tiks nokārtota pret 1. februāra krājumu ieejas plūsmu, un tiks veikta korekcija 1,00 USD apjomā. Atvērto krājumu daudzumi būs redzami šādās krājumu ieejas plūsmās:

-   1. februāris: daudzums ar vērtību 1 un izmaksas ar summu 10,00 USD.
-   5. februāris: daudzums ar vērtību 1 un izmaksas ar summu 13,00 USD.

Lai šiem diviem krājumiem iestatītu izmaksas USD 15,00 apjomā, izmantojiet rīcībā esošās korekcijas opciju, lai koriģētu atvērtos rīcībā esošos daudzumus no pēdējā krājumu aizvēršanas perioda. **Piezīme.** Rīcībā esošās korekcijas transakcijas grāmatošanas datums būs pēdējās krājumu slēgšanas datums. Šo datumu nevar modificēt.



