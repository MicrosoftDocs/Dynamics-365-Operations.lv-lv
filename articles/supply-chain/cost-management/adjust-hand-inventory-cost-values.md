---
title: Rīcībā esošo krājumu izmaksu vērtību koriģēšana
description: Lapu Rīcībā esošo krājumu koriģēšana var izmantot, lai pēc krājumu slēgšanas procesa palaišanas koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62122454b2fe0f6a9f04f073057156603e66bb22
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673303"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Rīcībā esošo krājumu izmaksu vērtību koriģēšana

[!include [banner](../includes/banner.md)]

Lapu Rīcībā esošo krājumu koriģēšana var izmantot, lai pēc krājumu slēgšanas procesa palaišanas koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību.

Lapu **Rīcībā esošo krājumu koriģēšana** var izmantot, lai koriģētu rīcībā esošo krājumu daudzuma izmaksu vērtību pēc krājumu slēgšanas procesa palaišanas. **Piezīme:** Lai atvērtu lapu **Rīcībā esošo krājumu koriģēšana**, lapā **Slēgšana un koriģēšana** atlasiet pabeigta krājuma slēgšanas procesa ierakstu un pēc tam noklikšķiniet uz **Korekcija** &gt; **Rīcībā esošs**. **Piemērs.** Februārī jums ir šādas transakcijas:

-   1. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 2 un izmaksām ar summu 10,00 USD;
-   5. februāris: krājumu finanšu ieejas plūsma daudzumam ar vērtību 1 un izmaksām ar summu 13,00 USD;
-   19. februāris: krājumu finanšu izejas plūsma daudzumam ar vērtību 1 un kārtējām vidējām izmaksām ar summu 11,00 USD.

Šim krājumam bija iestatīts krājumu modelis “pirmais iekšā, pirmais ārā” (first in, first out – FIFO), un krājuma slēgšana notika 28. februārī. Finanšu izejas plūsmas transakcija 11,00 USD apjomā tiks nokārtota pret 1. februāra krājumu ieejas plūsmu, un tiks veikta korekcija 1,00 USD apjomā. Atvērto krājumu daudzumi būs redzami šādās krājumu ieejas plūsmās:

-   1. februāris: daudzums ar vērtību 1 un izmaksas ar summu 10,00 USD.
-   5. februāris: daudzums ar vērtību 1 un izmaksas ar summu 13,00 USD.

Lai šiem diviem krājumiem iestatītu izmaksas USD 15,00 apjomā, izmantojiet rīcībā esošās korekcijas opciju, lai koriģētu atvērtos rīcībā esošos daudzumus no pēdējā krājumu aizvēršanas perioda. **Piezīme.** Rīcībā esošās korekcijas transakcijas grāmatošanas datums būs pēdējās krājumu slēgšanas datums. Šo datumu nevar modificēt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]