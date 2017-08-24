--- 
title: "Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu"
description: "Šajā uzdevuma ceļvedī aprakstīts, kā izmantot rēķinu reģistru, lai izveidotu rēķinus."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 08f66db0f62d5d985177b1d4ec0161df0b9961b3
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Rēķinu datu ievade kreditoru sistēmā, izmantojot rēķinu kopu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevuma ceļvedī aprakstīts, kā izmantot rēķinu reģistru, lai izveidotu rēķinus.  Pēc tam izmantojiet rēķinu kopu, lai saskaņotu rēķinu ar pirkšanas pasūtījumu un pabeigtu izdevumu kreditora rēķina lapā.


## <a name="create-a-purchase-order"></a>Pirkšanas pasūtījuma izveide
1. Dodieties uz Kreditori > Pirkšanas pasūtījumi > Pirkšanas pasūtījumi.
2. Lai izveidotu pirkšanas pasūtījumu, noklikšķiniet uz Jauns.
3. Laukā Kreditora konts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
4. No saraksta atlasiet kreditoru. Piemēram, kreditors 1001.
5. Noklikšķiniet uz Labi.
6. Laukā Krājuma kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
7. Sarakstā atrodiet pakalpojumu krājuma numuru. Piemēram, atlasiet S0001.
8. Noklikšķiniet uz krājuma numura un atlasiet to.
    * Neto summa ir 75,00.  Tā ir summa, kuru sagaidām rēķinā.  
9. Darbību rūtī noklikšķiniet uz Pirkšana.
10. Noklikšķiniet uz Apstiprināt.

## <a name="create-and-post-and-invoice"></a>Izveidot un grāmatot rēķinu
1. Pārejiet uz sadaļu Kreditori > Rēķini > Rēķinu reģistrs.
2. Noklikšķiniet uz Jauns.
3. Lai atlasītu nosaukumu rēķinu reģistram, kuru vēlaties izmantot, atveriet uzmeklēšanu.
4. Atlasiet nosaukumu tam rēķinu reģistram, kuru vēlaties lietot.
5. Noklikšķiniet uz Rindas, lai atvērtu reģistru un ievadītu izdevumu rindas.
6. Uzmeklēšanas skatā atlasiet kreditoru. Piemēram, noklikšķiniet uz kreditors 1001.
7. Laukā Rēķins ievadiet rēķina numuru.
8. Laukā Apraksts ierakstiet kādu vērtību.
9. Laukā Kredīts ievadiet kādu skaitli.
10. Laukā Pirkšanas pasūtījums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
11. Atlasiet iepriekš izveidoto pirkšanas pasūtījumu.
12. Laukā Apstiprināja noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
13. Iezīmējiet apstiprinātāju un noklikšķiniet uz Atlasīt, lai atlasītu šo apstiprinātāju.
14. Noklikšķiniet uz Grāmatot.
15. Aizveriet formu.
16. Aizveriet formu.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Lai pabeigtu rēķina izveides procesu, atveriet rēķinu no kopas un salīdziniet to ar pirkšanas pasūtījumu.
1. Pārejiet uz sadaļu Kreditori > Rēķini > Rēķinu kopa.
2. Lai no kopas rēķina izveidotu kreditora rēķinu, noklikšķiniet uz Pirkšanas pasūtījums.
3. Atlasiet rēķinu, kuru vēlaties pārskatīt.
4. Lai pabeigtu salīdzināšanu, noklikšķiniet uz Atjaunot atbilstības statusu.
5. Darbību rūtī noklikšķiniet uz opcijas.
6. Noklikšķiniet uz Mainīt skatījumu.
7. Noklikšķiniet uz Režģa skats.
8. Noklikšķiniet uz Grāmatot.
9. Aizveriet formu.
10. Dodieties uz Parādi kreditoriem > Kreditori > Kreditori.
11. Atlasiet kreditoru, kuram tika sastādīts pirkšanas pasūtījums. Piemēram, atlasiet kreditors 1001.
12. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
13. Darbību rūtī noklikšķiniet uz Kreditors.
14. Noklikšķiniet uz Transakcijas.
15. Atlasiet izveidoto rēķinu.
    * Rēķinu reģistra uzkrāšana tika atsaukta un iegrāmatota atbilstošajā izdevumu kontā.  


