---
title: Optimizēt veiktspēju ar automātiskās tīrīšanas uzdevumiem
description: Šajā tēmā tiek skaidrots, kā atrisināt dažas veiktspējas problēmas ar Microsoft Dynamics 365 Talent , iztīrot pakešuzdevuma vēsturi.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 1e9d237817024800ad9880ec58db3505ac1c493f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2027088"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a>Optimizēt veiktspēju ar automātiskās tīrīšanas uzdevumiem

[!include [banner](../includes/banner.md)]

**Izejas plūsma**

Microsoft Dynamics 365 Talent var rasties veiktspējas problēmas, ja pakešuzdevumu vēsture kļūst pārāk liela.

**Iemesls**

Bieži izpildīti pakešuzdevumi, var izraisīt nestabilu pakešuzdevuma vēstures izaugsmi. Tas var izraisīt veiktspējas problēmas. 

**Novēršana**

Ieplānojiet automātisku jūsu pakešuzdevuma vēstures tīrīšanas uzdevumu. Mēs rekomendējam iestatīt uzdevumu tā, lai tas palaistos reizi nedēļā, taču, atkarībā no jūsu vides, var būt nepieciešams veikt tīrīšanu biežāk vai retāk. Sekojošajā procedūrā ir ietverti mūsu ieteicamie iestatījumi, bet tos var mainīt atbilstoši jūsu vajadzībām.

1. Pakalpojumā Talant atlasiet **Sistēmas administrēšana**.

2. Joslā **Meklēšana** ievadiet **Pakešuzdevuma darba vēstures tīrīšana.**

   ![Meklējiet pakešuzdevumu vēstures tīrīšanu](media/talent-batch-history-cleanup-search-bar.png)

3. **Vēstures ierobežojums (dienas)** joslā ievadiet **30**.

   ![Iestatiet vēstures glabāšanu uz 30](media/talent-batch-history-cleanup-history-limit.png)

4. Atlasiet **Palaist fonā** un pēc tam atlasiet **Periodiskums.**

   ![Iestatiet periodiskumu](media/talent-batch-history-cleanup-recurrence.png)

5. Sadaļā **Definēt periodiskumu**iestatiet **Sākuma datums** un **Sākuma laiks**, kas jāveic ārpus darba laika vai nedēļas nogalē, un pēc tam atlasiet **BEZ BEIGU DATUMA.** 

   ![Definējiet periodiskuma sākuma datumu un laiku](media/talent-batch-history-cleanup-define-recurrence.png)

6. Sadaļā **PERIODISKUMA MODELIS** atlasiet **Dienas** un iestatiet **ATKĀRTOT PĒC NORĀDĪTĀ INTERVĀLA** uz **7**.

   ![Iestatiet tīrīšanu tā, lai tā atkārtotos katru nedēļu](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. Atlasiet **Labi**.

8. Mainiet jebkurus citus parametrus zem **Izpildīt fonā**, pēc nepieciešamības, un pēc tam atlasiet **Labi**.

