---
title: Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba
description: Šajā rakstā skaidrots, kā, plānojot ilgstošus Dynamics 365 Human Resources pakešuzdevumus pēc stundām, atrisināt veiktspējas problēmas ar Microsoft.
author: twheeloc
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6efb0a906bb948a47f03665dd6e7a8dd43434083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896081"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



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

   ![Iestatiet periodiskumu.](media/talent-batch-history-cleanup-recurrence.png)

4. Zem **Definēt periodiskumu** iestatiet **Sākuma datums** un **Sākuma laiks**, kas ir ārpus darba laika, vai nedēļas nogalē. Atlasiet **Bez beigu datuma**. 

   ![Definējiet periodiskuma sākuma datumu un laiku.](media/talent-batch-history-cleanup-define-recurrence.png)

5. Atlasiet **Labi**.

6. Ja nepieciešams, mainiet jebkurus citus parametrus zem **Izpildīt fonā** un pēc tam atlasiet **Labi**.

## <a name="additional-resources"></a>Papildu resursi

[Veiktspējas optimizēšana ar automātiskās tīrīšanas uzdevumiem](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
