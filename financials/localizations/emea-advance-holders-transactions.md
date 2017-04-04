---
title: "Avansa turētāju darbības"
description: "Uzziniet, kā strādāt ar avansa turētāja darbības Microsoft Dynamics 365 operācijām."
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
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: c819fbbb4a68dd5b8b192416fedb34827bbf3823
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holder-transactions"></a>Avansa turētāju darbības

Uzziniet, kā strādāt ar avansa turētāja darbības Microsoft Dynamics 365 operācijām.

Šiem darba ņēmējiem, kuri ir avansa turētāji var grāmatot, izmantojot avansa turētāja kontu darbības. Darbinieka ID, kurā norādīts katra avansa turētāja var izmantot, lai izsekotu visu avansa turētāja darbības. Šis numurs tiek iegūts kā konta numurs avansa turētāja darījumiem **Virsgrāmatas žurnālos** un **avansa turētāja darbības** lapas.

## <a name="create-and-post-a-purchase-order-with-advance-holder-details"></a>Izveidotu un grāmatotu pirkšanas pasūtījumu ar avansa turētāja detaļas
Vispārīga informācija par iepirkuma pasūtījumu, skatiet [pirkšanas pasūtījumu pārskats](/manufacturing/procurement/purchase-order-overview). Ja kreditora rēķins izveidots un publicēts ar avansa turētāja detaļas, avansa turētāja bilances tiks grāmatotas darbinieku bilances kontā, nevis piegādātāja bilances kontu. Pievienot pirkšanas pasūtījumam avansa turētāja detaļas, rīkojieties šādi:

-   Šajā **maksāšanas** lauku **cenu un atlaižu** sadaļu, atlasiet apmaksas termiņš. <!---For more information about **Terms of payment**, see [Define vendor payment terms](http://ax.help.dynamics.com/en/wiki/define-vendor-payment-terms/).-->Atlasiet maksājuma termiņu, kas ir **no avansa turētāja** opciju, kas atlasīta cilnē **maksāšanas** lapā. Plašāku informāciju par maksāšanas avansa turētāji iestatīšanu, skatiet [avansa turētāji](emea-advance-holders.md).
-   Šajā **avansa turētāja** lauku **cenu un atlaižu** FastTab, atlasiet avansa turētāja pirkšanas pasūtījumam.

Iepirkuma pasūtījuma grāmatošanas procesu veido divas kreditoru darbību ar pretēju summām un vienu avansa turētāja darbības. Tikai viena kreditora darbība tiek izveidota bez avansa turētāja detaļas.

## <a name="settle-advance-holder-balances-via-a-bank"></a>Avansa turētāja bilances norēķināties ar bankas starpniecību
Kad iestatāt avansa turētāja bilances ar bankas starpniecību, dienasgrāmatas ierakstu beigu atlikumiem avansa turētāja izveidotas Virsgrāmatas žurnālā. Varat iestatīt žurnāla un bankas kods **avansa turētāji** sadaļu par **debitoru kreditoru parametrus** lapā. Lai iegūtu papildinformāciju, skatiet [avansa turētāji](emea-advance-holders.md). Slēgt avansa turētāja bilance ar bankas starpniecību, atveriet **kreditoru parādi**&gt;**avansa turētāji**&gt;**avansa turētāji**. Noklikšķiniet uz **atlikums** pogas darbību rūtī un pēc tam noklikšķiniet uz **tuvu caur bankas**. Ievadiet tālāk minēto informāciju **cieši ar bankas starpniecību** lapā.

| Lauks                    | apraksts |
|------------------------------|-------------------|
| **Date of payment**          | Ievadiet datumu, kurā jāgrāmato maksājumu.|
| **Summa pārsūtīšanai** | Ievadiet vienlaikus slēguma bilances summa. Summa, kas norādīta **summu** lauku **atlikums** forma tiek atvērta pēc noklusējuma. |
| **Automatic**                | Atlasiet **automātisko** izvēles rūtiņu, lai veidotu un grāmatotu žurnālu, kas ir iestatīts uz **debitoru kreditoru parametrus** lapā.|

## <a name="settle-advance-holder-balances-via-cash"></a>Avansa turētāja bilances caur kases apmesties
Kad iestatāt avansa turētāja bilances caur kases, dienasgrāmatas ieraksti avansa turētāja bilances slēgšanas tiek izveidotas pavadzīmes žurnāls. Varat uzstādīt kodu žurnāla un naudas **avansa turētāji** cilni **debitoru kreditoru parametrus** lapā. Lai iegūtu papildinformāciju, skatiet [avansa turētāji](emea-advance-holders.md). Slēgt avansa turētāja bilance caur kases, atveriet **kreditoru parādi**&gt;**avansa turētāji**&gt;**avansa turētāji**. Noklikšķiniet uz **atlikums** pogas darbību rūtī un pēc tam noklikšķiniet uz **Close, izmantojot naudas**. Ievadiet tālāk minēto informāciju **Close, izmantojot naudas** lapā.

| Lauks                    | apraksts
|------------------------------|-----------------|
| **Date of payment**          | Ievadiet datumu, kurā jāgrāmato maksājumu.|
| **Summa pārsūtīšanai** | Ievadiet vienlaikus slēguma bilances summa. Summa, kas norādīta **summu** lauku **atlikums** forma tiek atvērta pēc noklusējuma. |
| **Automatic**                | Atlasiet **automātisko** izvēles rūtiņu, lai veidotu un grāmatotu automātiski žurnālu, kas ir iestatīts uz **debitoru kreditoru parametrus** lapā.     |

Pēc pavadzīmes žurnāls tiek apstrādāts, ja summa **summa jāpārskaita** laukumā bija negatīvs, izdevumu orderis tiek ģenerēta avansa turētāja bilances aizverot. Ja summa **summa jāpārskaita** lauks bija pozitīvs, ieņēmumu orderis tiek ģenerēts.


