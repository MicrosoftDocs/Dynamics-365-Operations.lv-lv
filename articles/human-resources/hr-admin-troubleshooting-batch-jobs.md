---
title: Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba
description: Šajā tēmā ir paskaidrots, kā atrisināt veiktspējas problēmas ar Microsoft Dynamics 365 Human Resources , plānojot ilglaicīgus pakešuzdevumus pēc darba.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500509"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Veiktspējas optimizēšana, plānojot pakešuzdevumus pēc darba

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
