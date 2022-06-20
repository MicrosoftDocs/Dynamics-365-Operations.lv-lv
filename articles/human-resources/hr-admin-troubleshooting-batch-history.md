---
title: Veiktspējas optimizēšana, izmantojot automātiskās tīrīšanas uzdevumus
description: Šajā rakstā skaidrots, kā uzlabot Microsoft veiktspēju Dynamics 365 Human Resources, tīrot pakešuzdevumu vēsturi.
author: twheeloc
ms.date: 08/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 10d535e54f71e7bb90c7385e09926270a446df7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902203"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Veiktspējas optimizēšana, izmantojot automātiskās tīrīšanas uzdevumus


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Izejas plūsma**

Microsoft Dynamics 365 Human Resources var rasties veiktspējas problēmas, ja pakešuzdevumu vēsture kļūst pārāk liela.

**Iemesls**

Bieži izpildīti pakešuzdevumi, var izraisīt nestabilu pakešuzdevuma vēstures izaugsmi. Tas var izraisīt veiktspējas problēmas. 

**Novēršana**

Ieplānojiet automātisku jūsu pakešuzdevuma vēstures tīrīšanas uzdevumu. Mēs rekomendējam iestatīt uzdevumu tā, lai tas palaistos reizi nedēļā, taču, atkarībā no jūsu vides, var būt nepieciešams veikt tīrīšanu biežāk vai retāk. Sekojošajā procedūrā ir ietverti mūsu ieteicamie iestatījumi, bet tos var mainīt atbilstoši jūsu vajadzībām.

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Joslā **Meklēšana** ievadiet **Pakešuzdevuma darba vēstures tīrīšana.**

   ![Meklējiet pakešuzdevumu vēstures tīrīšanu.](media/talent-batch-history-cleanup-search-bar.png)

3. **Vēstures ierobežojums (dienas)** joslā ievadiet **30**.

   ![Iestatiet vēstures glabāšanu uz 30.](media/talent-batch-history-cleanup-history-limit.png)

4. Atlasiet **Palaist fonā** un pēc tam atlasiet **Periodiskums.**

   ![Iestatiet periodiskumu.](media/talent-batch-history-cleanup-recurrence.png)

5. Sadaļā **Definēt periodiskumu** iestatiet **Sākuma datums** un **Sākuma laiks**, kas jāveic ārpus darba laika vai nedēļas nogalē, un pēc tam atlasiet **BEZ BEIGU DATUMA.** 

   ![Definējiet periodiskuma sākuma datumu un laiku.](media/talent-batch-history-cleanup-define-recurrence.png)

6. Sadaļā **PERIODISKUMA MODELIS** atlasiet **Dienas** un iestatiet **ATKĀRTOT PĒC NORĀDĪTĀ INTERVĀLA** uz **7**.

   ![Iestatiet tīrīšanu tā, lai tā atkārtotos katru nedēļu.](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Atlasiet **Labi**.

8. Mainiet jebkurus citus parametrus zem **Izpildīt fonā**, pēc nepieciešamības, un pēc tam atlasiet **Labi**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
