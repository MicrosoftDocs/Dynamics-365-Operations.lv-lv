---
title: Veiktspējas optimizēšana ar automātiskās tīrīšanas uzdevumiem
description: Šajā rakstā paskaidrots, kā atrisināt dažas Microsoft Dynamics 365 Human Resources veiktspējas problēmas, dzēšot pakešuzdevumu vēsturi.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053495"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimizēt veiktspēju ar automātiskās tīrīšanas uzdevumiem

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Izejas plūsma**

Microsoft Dynamics 365 Human Resources var rasties veiktspējas problēmas, ja pakešuzdevumu vēsture kļūst pārāk liela.

**Iemesls**

Bieži izpildīti pakešuzdevumi, var izraisīt nestabilu pakešuzdevuma vēstures izaugsmi. Tas var izraisīt veiktspējas problēmas. 

**Novēršana**

Ieplānojiet automātisku jūsu pakešuzdevuma vēstures tīrīšanas uzdevumu. Mēs rekomendējam iestatīt uzdevumu tā, lai tas palaistos reizi nedēļā, taču, atkarībā no jūsu vides, var būt nepieciešams veikt tīrīšanu biežāk vai retāk. Sekojošajā procedūrā ir ietverti mūsu ieteicamie iestatījumi, bet tos var mainīt atbilstoši jūsu vajadzībām.

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Joslā **Meklēšana** ievadiet **Pakešuzdevuma darba vēstures tīrīšana.**

   ![Meklējiet pakešuzdevumu vēstures tīrīšanu](media/talent-batch-history-cleanup-search-bar.png)

3. **Vēstures ierobežojums (dienas)** joslā ievadiet **30**.

   ![Iestatiet vēstures glabāšanu uz 30](media/talent-batch-history-cleanup-history-limit.png)

4. Atlasiet **Palaist fonā** un pēc tam atlasiet **Periodiskums.**

   ![Iestatiet periodiskumu](media/talent-batch-history-cleanup-recurrence.png)

5. Sadaļā **Definēt periodiskumu** iestatiet **Sākuma datums** un **Sākuma laiks**, kas jāveic ārpus darba laika vai nedēļas nogalē, un pēc tam atlasiet **BEZ BEIGU DATUMA.** 

   ![Definējiet periodiskuma sākuma datumu un laiku](media/talent-batch-history-cleanup-define-recurrence.png)

6. Sadaļā **PERIODISKUMA MODELIS** atlasiet **Dienas** un iestatiet **ATKĀRTOT PĒC NORĀDĪTĀ INTERVĀLA** uz **7**.

   ![Iestatiet tīrīšanu tā, lai tā atkārtotos katru nedēļu](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Atlasiet **Labi**.

8. Mainiet jebkurus citus parametrus zem **Izpildīt fonā**, pēc nepieciešamības, un pēc tam atlasiet **Labi**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]