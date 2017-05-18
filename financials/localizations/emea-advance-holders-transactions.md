---
title: "Avansa turētāju darbības"
description: "Uzziniet, kā strādāt ar avansa turētāju transakcijām programmatūrā Microsoft Dynamics 365 for Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorkerAdvHolderTableListPage_RU
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262554
ms.assetid: 84ff97bb-ae21-4d6d-8160-9325f64134ce
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 422186b595f4dd055320a3f13758e8f1807bf833
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="advance-holder-transactions"></a>Avansa turētāju darbības

[!include[banner](../includes/banner.md)]


Uzziniet, kā strādāt ar avansa turētāju transakcijām programmatūrā Microsoft Dynamics 365 for Operations.

Šiem darbiniekiem, kuri ir avansa turētāji, transakcijas var grāmatot, izmantojot avansa turētāju kontus. Lai izsekotu visas avansa turētāja transakcijas, var izmantot katram avansa turētājam norādīto nodarbinātā ID. Šis numurs kā konta numurs avansa turētāju transakcijām tiek izgūts lapās **Virsgrāmatas žurnāli** un **Avansa turētāju transakcijas**.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Izveidot un grāmatot pirkšanas pasūtījumu ar avansa turētāja informāciju
Vispārīgāku informāciju par pirkšanas pasūtījumiem skatiet rakstā [Pirkšanas pasūtījuma apskats](/manufacturing/procurement/purchase-order-overview). Ja tiek izveidots un grāmatots kreditora rēķins ar avansa turētāja informāciju, tad avansa turētāja bilances tiks grāmatotas darbinieka bilances kontā, nevis kreditora bilances kontā. Lai pirkšanas pasūtījumam pievienotu avansa turētāja informāciju, izpildiet tālāk sniegtos norādījumus.

-   Sadaļas **Cena un atlaide** laukā **Maksājuma nosacījumi** atlasiet maksājuma nosacījumu. <!---For more information about **Terms of payment**, see [Define vendor payment terms](http://ax.help.dynamics.com/en/wiki/define-vendor-payment-terms/).--> Atlasiet maksājumu, kuram lapā **Maksājuma nosacījumi** ir atzīmēta opcija **No avansa turētāja**. Papildinformāciju par maksājumu nosacījumu iestatīšanu avansa turētājiem skatiet rakstā [Avansa turētāji](emea-advance-holders.md).
-   Kopsavilkuma cilnes **Cena un atlaide** laukā **Avansa turētājs** pirkšanas pasūtījumam atlasiet avansa turētāju.

Pirkšanas pasūtījuma grāmatošanas process izveido divas kreditora transakcijas ar pretējām summām un vienu avansa turētāja transakciju. Bez avansa turētāja informācijas tiek izveidota tikai viena kreditora transakcija.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Nosegt avansa turētāja bilances, izmantojot banku
Kad avansa turētāja bilances nosedzat, izmantojot banku, avansa turētāja bilanču slēgšanas žurnāla ieraksti tiek izveidoti virsgrāmatas žurnālā. Žurnāla un bankas kodu varat iestatīt lapas **Kreditoru moduļa parametri** sadaļā **Avansa turētāji**. Plašāku informāciju skatiet rakstā [Avansa turētāji](emea-advance-holders.md). Lai slēgtu avansa turētāja bilanci, izmantojot banku, atveriet sadaļu **Parādi kreditoriem** &gt; **Avansa turētāji** &gt; **Avansa turētāji**. Darbību rūtī noklikšķiniet uz pogas **Bilance** un pēc tam noklikšķiniet uz **Slēgt no bankas**. Lapā **Slēgt no bankas** ievadiet tālāk minēto informāciju.

| Lauks                    | Apraksts |
|------------------------------|-------------------|
| **Maksājuma datums**          | Ievadiet datumu, kad maksājums ir jāgrāmato.|
| **Summa pārskaitīšanai** | Ievadiet bilances summu slēgšanas laikā. Laukā **Summa** norādītā summa formā **Bilance** tiek rādīta pēc noklusējuma. |
| **Automātiski**                | Atzīmējiet izvēles rūtiņu **Automātiski**, lai izveidotu un grāmatotu žurnālu, kurš ir sākotnēji iestatīts lapā **Kreditoru moduļa parametri**.|

## <a name="settle-advance-holder-balances-via-cash"></a>Nosegt avansa turētāja bilances, izmantojot skaidru naudu
Kad nosedzat avansa turētāja bilances, izmantojot skaidru naudu, avansa turētāja bilanču slēgšanas žurnāla ieraksti tiek izveidoti pavadzīmju žurnālā. Žurnāla un skaidras naudas kodu varat iestatīt lapas **Kreditoru moduļa parametri** cilnē **Avansa turētāji**. Plašāku informāciju skatiet rakstā [Avansa turētāji](emea-advance-holders.md). Lai slēgtu avansa turētāja bilanci, izmantojot skaidru naudu, atveriet sadaļu **Parādi kreditoriem** &gt; **Avansa turētāji** &gt; **Avansa turētāji**. Darbību rūtī noklikšķiniet uz pogas **Bilance** un pēc tam noklikšķiniet uz **Slēgt no kases**. Lapā **Slēgt no kases** ievadiet tālāk minēto informāciju.

| Lauks                    | Apraksts
|------------------------------|-----------------|
| **Maksājuma datums**          | Ievadiet datumu, kad maksājums ir jāgrāmato.|
| **Summa pārskaitīšanai** | Ievadiet bilances summu slēgšanas laikā. Laukā **Summa** norādītā summa formā **Bilance** tiek rādīta pēc noklusējuma. |
| **Automātiski**                | Atzīmējiet izvēles rūtiņu **Automātiski**, lai automātiski izveidotu un grāmatotu žurnālu, kurš ir sākotnēji iestatīts lapā **Kreditoru moduļa parametri**.     |

Pēc pavadzīmju žurnāla apstrādāšanas, ja laukā **Summa pārskaitīšanai** summa bija negatīva, tad avansa turētājam tiek ģenerēts izdevumu orderis, kad bilances tiek slēgtas. Ja laukā **Summa pārskaitīšanai** summa bija pozitīva, tad tiek ģenerēts ieņēmumu orderis.




