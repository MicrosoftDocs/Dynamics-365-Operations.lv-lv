---
title: "Projekta laika ieraksta mobilajām ierīcēm paredzēta darbvieta"
description: "Šajā tēmā ir sniegta informācija par mobilo darbvietu Projekta laika ieraksts. Šajā darbvietā lietotāji, izmantojot savu mobilo ierīci, var ievadīt un saglabāt laiku attiecībā pret projektu."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9bf79af6eea6f899158fc3c8d523587cb11c90ad
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="project-time-entry-mobile-workspace"></a>Projekta laika ieraksta mobilajām ierīcēm paredzēta darbvieta

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par mobilo darbvietu **Projekta laika ieraksts**. Šajā darbvietā lietotāji, izmantojot savu mobilo ierīci, var ievadīt un saglabāt laiku attiecībā pret projektu.

Šī mobilā darbvieta ir paredzēta lietošanai, izmantojot mobilo programmu Microsoft Dynamics 365 for Unified Operations. 

## <a name="overview"></a>Pārskats
Kā daļa no ikdienas darba projektu resursi bieži vien atrodas uz vietas vai ceļā. Mobilā darbvieta **Projekta laika ieraksts** lietotājiem pašu izvēlētā mobilajā ierīcē ļauj ievadīt apmaksājamo vai neapmaksājamo laiku attiecībā uz projektu. Tāpēc projekta resursi laika ierakstus var reģistrēt jebkurā laikā un vietā. Tāpat viņi var arī skatīt jau reģistrētos laika ierakstus. 

Jo īpaši **Projekta laika ieraksts** mobilo darbvietā, lietotāji var veikt šādus uzdevumus:

-   Jebkuram atlasītajam datumam ievadiet stundu skaitu, kuras esat pavadījis, veicot kādu noteiktu uzdevumu.
-   Meklējiet pēc projekta nosaukuma vai debitora, lai atrastu projektu, kuram ievadīt laiku.
-   Norādiet kategoriju un aktivitāti patērētajam laikam.
-   Reģistrējiet laiku kā apmaksājamu vai neapmaksājamu attiecībā uz projektu.
-   Pēc izvēles ievadiet jebkādus ārējus vai iekšējus komentārus.

## <a name="prerequisites"></a>Priekšnosacījumi
Priekšnosacījumi atšķiras atkarībā no jūsu organizācijai izvietotās Microsoft Dynamics 365 versijas.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Programmas Microsoft Dynamics 365 for Finance and Operations izmantošanas priekšnoteikumi
Ja jūsu organizācijai ir izvietota programmatūra Microsoft Dynamics 365 for Finance and Operations, sistēmas administratoram ir jāpublicē mobilā darbvieta **Projekta laika ieraksts**. Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Priekšnosacījumi, ja lietojat Microsoft Dynamics 365 for Operations versiju 1611 ar 3. platformas atjauninājumu vai jaunāku tā versiju.
Ja jūsu organizācija ir izvietota Microsoft Dynamics 365 for Operations versija 1611 ar 3. platformu atjauninājumu vai jaunāku tā versiju, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi. 

<table>
<thead>
<tr class="header">
<th>Priekšnoteikumi</th>
<th>Loma</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Ieviesiet KB 4018050.</td>
<td>Sistēmas administrators</td>
<td>KB 4018050 ir X++ atjauninājums vai metadatu labojumfails, kas ietver mobilo darbvietu <strong>Projekta laika ieraksts</strong>. Lai ieviestu KB 4018050, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Lejupielādējiet metadatu labojumfailu no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Izveidojiet izvietojama pakotni,</a> kas ietver modeļus <strong>ApplicationSuite</strong> un <strong>ProjectMobile</strong>, un pēc tam šo izvietojamo pakotni augšupielādējiet pakalpojumā LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Lietojiet izvietojamo pakotni</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicējiet <strong>Projekta laika ierakstu</strong> mobilajā darbvietā.</td>
<td>Sistēmas administrators</td>
<td>Skatiet tēmu <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobilās darbvietas publicēšana</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobilās programmas lejupielāde un instalēšana

Lejupielādējiet un instalējiet mobilo programmu Dynamics 365 for Unified Operations.

-   [Android tālruņiem](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Tālruņiem iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Pierakstīšanās mobilajā programmā
1.  Palaidiet programmu savā mobilajā ierīcē.
2.  Ievadiet savu Dynamics 365 vietrādi URL.
3.  Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.
4.  Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.

[![Velciet, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Ievadīt laiku, izmantojot mobilo darbvietu Projekta laika ieraksts
1.  Mobilajā ierīcē atlasiet darbvietu **Projekta laika ieraksts**.
2.  Atlasiet vienumu **Laika ieraksts**. Tiek parādīti kalendāra datumi pašreizējai nedēļai.
3.  Atlasītajam datumam atlasiet vienumu **Darbības** &gt; **Jauns ieraksts**.
4.  Ievadiet reģistrējamo stundu skaitu.
5.  Atlasiet projektu šim laika ierakstam. Sarakstā tiek parādīts to projektu saraksts, kas ir ielādēti programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju skatiet rakstā [Mobilā platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Ja jūsu projekts nav sarakstā, atlasiet **Meklēšana**. Meklējiet pēc nosaukuma vai pārslēdziet uz meklēšanu pēc projekta nosaukuma vai debitora.
7.  Atlasiet kategoriju. Sarakstā tiek parādītas kategorijas, kas ir ielādēti programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju skatiet rakstā [Mobilā platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Ja jūsu kategorija nav sarakstā, atlasiet **Meklēšana**. Meklējiet pēc kategorijas vai pārslēdzieties uz meklēšanu pēc kategorijas nosaukuma.
9.  Atlasiet kādu aktivitāti. Sarakstā tiek parādītas aktivitātes, kas ir ielādētas programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju skatiet rakstā [Mobilā platforma](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Ja jūsu aktivitāte nav sarakstā, atlasiet **Meklēšana**. Meklējiet pēc aktivitātes numura vai pārslēdziet uz meklēšanu pēc nolūka.

11. Atlasiet rindas rekvizītu.
12. Pēc izvēles: ievadiet jebkādus ārējus un iekšējus komentārus.
13. Atlasiet **Gatavs**.

