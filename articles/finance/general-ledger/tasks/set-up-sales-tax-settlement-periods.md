---
title: Iestatīt PVN apmaksas periodus
description: Šajā rakstā ir izskaidrots, kā iestatīt PVN apmaksas periodus Dynamics 365 finanses.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f8514494b5d3534fc236def817df0d58fe80d70
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846688"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Iestatīt PVN apmaksas periodus

[!include [banner](../../includes/banner.md)]

Šajā rakstā skaidrots, kā iestatīt PVN maksājumu periodus. PVN nomaksas periodi satur informāciju par periodu intervāliem, par kuriem jāsniedz atskaites un par kuriem tie jānomaksā. Nomaksas procesu iespējams palaist maksājumu periodam, noteiktam datumu intervālam. Tiks segti visi nodokļu kodi, kas saistīti ar apmaksas periodu. Atkarībā no saistītās PVN iestādes iestatījumiem, nodokļu parāds tiek grāmatots vai nu kreditoram vai Virsgrāmatas kontā.

Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet **uz > pvn maksāšanas > PVN > PVN apmaksas periodiem**.
2. Atlasiet **Jauns**.
3. Ierakstiet vērtību laukā **Apmaksas periods**.
4. Laukā **Apraksts** ierakstiet kādu vērtību.
5. Laukā **Iestāde** atlasiet PVN iestādi, kas saņem apmaksas perioda pārskatus un maksājumus.
6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
7. Lauka **Maksājuma nosacījumi** nolaižamajā izvēlnē atlasiet vēlamo ierakstu. Saistītā nodokļu iestāde var tikt iestatīta kā kreditors un PVN apmaksai tiek izveidots atvērts kreditora rēķins. Apmaksas nosacījumi norāda atvērta kreditora rēķina apmaksas datumu.  
8. Atlasiet apmaksas perioda intervālu veidu.
9. Ievadiet perioda intervāla vienību skaitu periodā. Piemēram, ceturksnī ir 3 mēneši.
10. Atlasiet vai notīriet izvēles rūtiņu **Izmantot pakešveida apstrādi PVN apmaksai**. Apmaksas process apmaksas periodam var tikt apstrādāts fonā kā pakešuzdevums. Tas ir ieteicams gadījumos, kad vienā laika periodā ir liels skaits nodokļu transakciju.
11. Atzīmējiet izvēles rūtiņu **Novērst korespondējošu nodokļu transakciju ģenerēšanu** vai noņemiet tās atzīmi. Pēc noklusējuma sistēma ģenerē korespondējošās nodokļu transakcijas, kamēr notiek segšanas process, un tas var radīt veiktspējas problēmas, ja kādā periodā ir liels skaits nodokļu transakciju. Atzīmējiet šo izvēles rūtiņu, lai novērstu korespondējošu nodokļu transakciju ģenerēšanu.
12. Izvērsiet cilni **Perioda intervāli**.
13. Atlasiet **Pievienot**.
14. Jaunās rindas laukā **No datuma** ievadiet datumu.
15. Ievadiet datumu laukā **Līdz datumam**.
16. Atlasiet **Jauns perioda intervāls**. Kad pirmā perioda intervāls ir ievadīts, jaunus periodus var izveidot automātiski. Pēc nepieciešamības varat atgriezties un pievienot jaunus periodu intervālus.  
17. Aizvērt lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
