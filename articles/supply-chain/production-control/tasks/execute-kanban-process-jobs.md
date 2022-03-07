---
title: Kanban procesa darbu izpilde
description: Šī procedūra fokusējas uz kanban procesa darbu izpildi.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ac6f0f6139fe17532f6fbd996b314e0b14f3d90
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566583"
---
# <a name="execute-kanban-process-jobs"></a>Kanban procesa darbu izpilde

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]