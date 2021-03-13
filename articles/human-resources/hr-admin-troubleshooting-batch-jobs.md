---
title: Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba
description: Šajā tēmā ir paskaidrots, kā atrisināt veiktspējas problēmas ar Microsoft Dynamics 365 Human Resources , plānojot ilglaicīgus pakešuzdevumus pēc darba.
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113440"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba

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
