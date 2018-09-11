--- 
title: Kanban procesa darbu izpilde
description: "Šī procedūra fokusējas uz kanban procesa darbu izpildi."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 752eab976f740606154d416678ba2381641697df
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="execute-kanban-process-jobs"></a>Kanban procesa darbu izpilde

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šī procedūra fokusējas uz kanban procesa darbu izpildi. Pirmais darbs tiek pabeigts ar paredzamo daudzumu un bez kļūdām. Otrs darbs tiek pabeigts ar kļūdām. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. Šī procedūra ir paredzēta mašīnas operatoram.


## <a name="select-a-kanban-job"></a>Atlasiet kanban darbu.
1. Pārejiet uz sadaļu Ražošanas kontrole > Kanban > Kanban panelis procesa darbiem.
2. Laukā Darba šūna noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Noklikšķiniet uz rindas ar resursu grupu 1250. Šādi atfiltrēsiet darbu sarakstu, lai parādītu tikai darbus šūnai 1250.
    * Iezīmējiet rindu, kurā ir plānotā darba statuss.  

## <a name="complete-a-job-with-expected-quantity"></a>Pabeidziet darbu ar paredzēto daudzumu
1. Izvērsiet vai sakļaujiet sadaļu Detalizēta informācija.
    * Šajā sadaļā tiek parādīta svarīga informācija par kartes numuru, preces numuru, pasūtīto daudzumu un aktivitātes nosaukums.  
2. Izvērsiet vai sakļaujiet sadaļu Ražošanas instrukcija.
    * Šajā sadaļā tiek parādītas ražošanas instrukcijas aktivitātei. Instrukcijas var būt teksts, attēli, zīmējumi un citi dokumenti.  
3. Noklikšķiniet uz Sākt.
    * Atlasiet darbu, kas nav pabeigts. Izmantojiet darba statusa lauka statusa ikonas, lai skatītu darba statusu.      
4. Noklikšķiniet uz Pabeigt.
    * Darbs ir pabeigts ar paredzamo kvalitāti.  

## <a name="complete-a-job-with-errors"></a>Pabeidziet darbu ar kļūdām
1. Noklikšķiniet uz Sākt.
    * Kad darbs ir pabeigts, nākamais darbs sarakstā tiek atlasīts automātiski. Šī iemesla dēļ nav nepieciešams atlasīt darbu, pirms noklikšķināt uz Sākt.  
2. Darbību rūtī noklikšķiniet uz Ražošana.
3. Noklikšķiniet uz Pabeigt (informācija).
4. Sarakstā atzīmējiet atlasīto rindu.
5. Ierakstiet skaitli laukā Kļūdu daudzums.
6. Laukā Derīgais daudzums ierakstiet kādu skaitli.
7. Noklikšķiniet uz OK.


