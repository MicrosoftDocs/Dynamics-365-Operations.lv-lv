---
title: Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba
description: Šajā tēmā ir paskaidrots, kā atrisināt veiktspējas problēmas ar Microsoft Dynamics 365 Human Resources , plānojot ilglaicīgus pakešuzdevumus pēc darba.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 92dd281ed718be5c7ebd843d015c108ee121f30a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794929"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Izsniegt

Microsoft Dynamics 365 Human Resources var rasties veiktspējas problēmas, ja ilglaicīgi pakešuzdevumi darbojas ierastajā darba laikā.

## <a name="resolution"></a>Novēršana

Šādus pakešuzdevumus ieplānojiet ārpus darba laika. Ieteicams pārskatīt arī bieži izpildāmo pakešuzdevumu biežumu. Ja iespējams, samaziniet pakešuzdevuma atkārtošanos. Daudzos gadījumos noklusējuma frekvence ir pietiekama.

Šādus pakešuzdevumus ieteicams izpildīt naktī vai pēc darba. Noteikti pārbaudiet periodisko pakešuzdevumu laika joslu. Daži pakešuzdevumi izmanto Klusā okeāna standarta laiku (PST).

| Pakešuzdevums | Noklusējuma atkārtojums |
| --- | --- |
| Pakešuzdevuma vēstures tīrīšana | 1 reizi mēnesī |
| Eksporta sagatavošanas posmu tīrīšana | 1 reizi dienā |
| Common Data Service integrācijas neizpildīto pieprasījumu sinhronizēšana | 1 reizi dienā |
| Datu bāzes saspiešanas sistēmas darbs, kas jāveic regulāri, ārpus darba laikā | 1 reizi dienā |
| Datu bāzes indeksa pārbūves sistēmas darbs, kas jāveic regulāri, ārpus darba laikā | 1 reizi dienā |

1. Human Resources atlasiet **Sistēmas administrēšana**.

2. Joslā **Meklēšana** meklējiet vienu no iepriekš minētajiem pakešuzdevumiem.

3. Atlasiet **Palaist fonā** un pēc tam atlasiet **Periodiskums**.

   ![Iestatiet periodiskumu](media/talent-batch-history-cleanup-recurrence.png)

4. Zem **Definēt periodiskumu** iestatiet **Sākuma datums** un **Sākuma laiks**, kas ir ārpus darba laika, vai nedēļas nogalē. Atlasiet **Bez beigu datuma**. 

   ![Definējiet periodiskuma sākuma datumu un laiku](media/talent-batch-history-cleanup-define-recurrence.png)

5. Atlasiet **Labi**.

6. Ja nepieciešams, mainiet jebkurus citus parametrus zem **Izpildīt fonā** un pēc tam atlasiet **Labi**.

## <a name="additional-resources"></a>Papildu resursi

[Veiktspējas optimizēšana ar automātiskās tīrīšanas uzdevumiem](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]