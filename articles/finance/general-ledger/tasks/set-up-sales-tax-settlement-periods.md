---
title: PVN apmaksas periodu iestatīšana
description: Šajā tēmā paskaidrots, kā iestatīt PVN apmaksas periodus programmā Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c17a0240c29dad58c958ab1ce844ee5d8384bd1f
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658933"
---
# <a name="set-up-sales-tax-settlement-periods"></a>PVN apmaksas periodu iestatīšana

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā tēmā paskaidrots, kā iestatīt PVN apmaksas periodus. PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā. Nomaksas procesu iespējams palaist maksājumu periodam, noteiktam datumu intervālam. Tiks segti visi nodokļu kodi, kas saistīti ar apmaksas periodu. Atkarībā no saistītās PVN iestādes iestatījumiem, nodokļu parāds tiek grāmatots vai nu kreditoram vai Virsgrāmatas kontā.

Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Navigācijas rūtī atveriet **Moduļi > Nodokļi > Netiešie nodokļi > PVN > PVN apmaksas periodi**.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Apmaksas periods**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Iestāde** atlasiet PVN iestādi, kas saņem apmaksas perioda pārskatus un maksājumus.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Lauka **Maksājuma nosacījumi** nolaižamajā izvēlnē atlasiet vēlamo ierakstu. Saistītā nodokļu iestāde var tikt iestatīta kā kreditors un PVN apmaksai tiek izveidots atvērts kreditora rēķins. Apmaksas nosacījumi norāda atvērta kreditora rēķina apmaksas datumu.  
8. Atlasiet apmaksas perioda intervālu veidu.
9. Ievadiet perioda intervāla vienību skaitu periodā. Piemēram, ceturksnī ir 3 mēneši.
10. Atlasiet vai notīriet izvēles rūtiņu **Izmantot pakešveida apstrādi PVN apmaksai**. Apmaksas process apmaksas periodam var tikt apstrādāts fonā kā pakešuzdevums. Tas ir ieteicams gadījumos, kad vienā laika periodā ir liels skaits nodokļu transakciju.  
    > [!NOTE]
    > Pašlaik tas netiek atbalstīts Spānijā, Japānā un Nīderlandē.
11. Atzīmējiet izvēles rūtiņu **Novērst korespondējošu nodokļu transakciju ģenerēšanu** vai noņemiet tās atzīmi. Pēc noklusējuma sistēma ģenerē korespondējošās nodokļu transakcijas, kamēr notiek segšanas process, un tas var radīt veiktspējas problēmas, ja kādā periodā ir liels skaits nodokļu transakciju. Atzīmējiet šo izvēles rūtiņu, lai novērstu korespondējošu nodokļu transakciju ģenerēšanu.
12. Izvērsiet cilni **Perioda intervāli**.
13. Atlasiet **Pievienot**.
14. Jaunās rindas laukā **No datuma** ievadiet datumu.
15. Ievadiet datumu laukā **Līdz datumam**.
16. Atlasiet **Jauns perioda intervāls**. Kad pirmā perioda intervāls ir ievadīts, jaunus periodus var izveidot automātiski. Pēc nepieciešamības varat atgriezties un pievienot jaunus periodu intervālus.  
17. Aizvērt lapu.
