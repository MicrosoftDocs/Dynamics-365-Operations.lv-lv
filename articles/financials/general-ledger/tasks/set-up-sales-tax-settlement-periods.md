---
title: Iestatīt PVN apmaksas periodus
description: PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā.
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569590"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Iestatīt PVN apmaksas periodus

[!include [task guide banner](../../includes/task-guide-banner.md)]

PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā. Nomaksas procesu iespējams palaist maksājumu periodam, noteiktam datumu intervālam. Tiks segti visi nodokļu kodi, kas saistīti ar apmaksas periodu. Atkarībā no saistītās PVN iestādes iestatījumiem, nodokļu parāds tiek grāmatots vai nu kreditoram vai Virsgrāmatas kontā.



Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.



1. Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > PVN > PVN apmaksas periodi.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Apmaksas periods.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Iestāde atlasiet PVN iestādi, kas saņem apmaksas perioda pārskatus un maksājumus.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Apmaksas nosacījumi noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
    * Saistītā nodokļu iestāde var tikt iestatīta kā kreditors un PVN apmaksai tiek izveidots atvērts kreditora rēķins. Apmaksas nosacījumi norāda atvērta kreditora rēķina apmaksas datumu.  
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
10. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
11. Atlasiet apmaksas perioda intervālu veidu.
12. Ievadiet perioda intervāla vienību skaitu periodā. Piemēram, ceturksnī ir 3 mēneši.
13. Atlasiet vai notīriet izvēles rūtiņu Izmantot pakešveida apstrādi PVN apmaksai.
    * Apmaksas process apmaksas periodam var tikt apstrādāts fonā kā pakešuzdevums. Tas ir ieteicams gadījumos, kad vienā laika periodā ir liels skaits nodokļu transakciju.  
14. Atzīmējiet izvēles rūtiņu Novērst korespondējošu nodokļu transakciju ģenerēšanu vai noņemiet tās atzīmi.
    * Pēc noklusējuma sistēma ģenerē korespondējošās nodokļu transakcijas, kamēr notiek segšanas process, un tas var radīt veiktspējas problēmas, ja kādā periodā ir liels skaits nodokļu transakciju. Atzīmējiet šo izvēles rūtiņu, lai novērstu korespondējošu nodokļu transakciju ģenerēšanu.
15. Izvērsiet cilni Perioda intervāli.
16. Noklikšķiniet uz Pievienot.
17. Sarakstā atzīmējiet atlasīto rindu.
18. Ievadiet datumu laukā No datuma.
19. Laukā Līdz datumam ievadiet datumu.
20. Noklikšķiniet uz Jauns perioda intervāls.
    * Kad pirmā perioda intervāls ir ievadīts, jaunus periodus var izveidot automātiski. Pēc nepieciešamības varat atgriezties un pievienot jaunus periodu intervālus.  
21. Aizvērt lapu.

