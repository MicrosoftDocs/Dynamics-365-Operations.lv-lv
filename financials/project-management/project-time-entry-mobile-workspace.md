---
title: "Mobilā darbvieta Projekta laika ieraksts Dynamics 365 for Operations programmai"
description: "Šajā tēmā ir sniegta informācija par mobilo darbvietu Projekta laika ieraksts. Šajā darbvietā lietotāji, izmantojot savu mobilo ierīci, var ievadīt un saglabāt laiku attiecībā pret projektu."
author: annbe
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9c592c301908898915164e9236850759b73543fe
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Projekta laika ieraksta mobilajām ierīcēm paredzēta darbvieta

[!include[banner](../includes/banner.md)]



Šajā tēmā ir sniegta informācija par mobilo darbvietu Projekta laika ieraksts Dynamics 365 for Operations mobilajai programmai. Šajā darbvietā lietotāji, izmantojot savu mobilo ierīci, var ievadīt un saglabāt laiku attiecībā pret projektu.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Apskats par mobilo darbvietu Projekta laika ieraksts
---------------------------------------------------

Kā daļa no ikdienas darba projektu resursi bieži vien atrodas uz vietas vai ceļā. Mobilā darbvieta **Projekta laika ieraksts** lietotājiem pašu izvēlētā mobilajā ierīcē ļauj ievadīt apmaksājamo vai neapmaksājamo laiku attiecībā uz projektu. Tāpēc projekta resursi laika ierakstus var reģistrēt jebkurā laikā un vietā. Tāpat viņi var arī skatīt jau reģistrētos laika ierakstus. 

Mobilā darbvieta **Projekta laika ieraksts** sniedz tālāk aprakstītos līdzekļus.

-   Jebkuram atlasītajam datumam ievadiet stundu skaitu, kuras esat pavadījis, veicot kādu noteiktu uzdevumu.
-   Meklējiet pēc projekta nosaukuma vai debitora, lai atrastu projektu, kuram ievadīt laiku.
-   Norādiet kategoriju un aktivitāti patērētajam laikam.
-   Reģistrējiet laiku kā apmaksājamu vai neapmaksājamu attiecībā uz projektu.
-   Pēc izvēles ievadiet jebkādus ārējus vai iekšējus komentārus.

Lai ieviestu mobilo darbvietu **Projekta laika ieraksts**, skatiet tālāk norādītās sadaļas šajā tēmā.

## <a name="prerequisites"></a>Priekšnosacījumi
Lai varētu ieviest mobilo darbvietu **Projekta laika ieraksts**, pārliecinieties, ka sistēmas administrators ir izpildījis tālāk minētos priekšnosacījumus.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Priekšnosacījums</th>
<th>Loma</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jābūt ieviestai Microsoft Dynamics 365 for Operation versijai 1611 ar 3. vai jaunāku platformas atjauninājumu.</td>
<td>Sistēmas administrators</td>
<td>Ja programma Dynamics 365 for Operations vēl nav izvietota jūsu organizācijā, jūsu sistēmas administratoram vajadzētu izlasīt rakstu <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations izvietošana demonstrācijas vidē</a>.</td>
</tr>
<tr class="even">
<td>Jāievieš KB 4018050.</td>
<td>Sistēmas administrators</td>
<td>KB 4018050 ir X++ atjauninājums vai metadatu labojumfails, kas ietver mobilo darbvietu <strong>Projekta laika ieraksts</strong>. Lai ieviestu KB 4018050, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li>Lejupielādējiet KB 4018050 no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojama pakotni,</a> kas ietver modeļus <strong>ApplicationSuite</strong> un <strong>ProjectMobile</strong>, un pēc tam šo izvietojamo pakotni augšupielādējiet pakalpojumā LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Lietojiet šo izvietojamo pakotni</a> savai Dynamics 365 for Operations sistēmai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilā darbvieta <strong>Projekta laika ieraksts</strong> ir jāpublicē Dynamics 365 for Operations mobilajā programmā.</td>
<td>Sistēmas administrators</td>
<td><ol>
<li>Palaidiet pārlūkprogrammā programmu Dynamics 365 for Operations.</li>
<li>Lapā <strong>Sistēmas parametri</strong>, cilnē <strong>Pārvaldīt mobilās darbvietas</strong> atlasiet darbvietu <strong>Projekta laika ieraksts</strong>.</li>
<li>Noklikšķiniet uz <strong>Publicēt mobilo darbvietu</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Dynamics 365 for Operations mobilās programmas lejupielāde un instalēšana
Mobilo programmu veikalā lejupielādējiet Dynamics 365 for Operations mobilo programmu un instalējiet to.

-   Operētājsistēmai Android: [Dynamics 365 for Operations Google Play veikalā](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Operētājsistēmai iPhone: [Dynamics 365 for Operations iTunes programmu veikalā](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Pierakstīšanās Dynamics 365 for Operations mobilajā programmā
1.  Palaidiet programmu savā mobilajā ierīcē.
2.  Ievadiet Dynamics 365 for Operations URL.
3.  Ievadiet uzņēmumu, kurā pierakstīties. Ievadiet, piemēram, **USMF**.
4.  Pirmajā pierakstīšanās reizē ir jāievada Microsoft Dynamics 365 for Operations konta lietotājvārds un parole. Ievadiet savus akreditācijas datus.
5.  Pēc pierakstīšanās ir redzamas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā! Ja sistēmas administrators jaunu darbvietu publicēs vēlāk, varat vilkt, lai atsvaidzinātu mobilo darbvietu sarakstu.

[![Velciet, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Ievadīt laiku, izmantojot mobilo darbvietu Projekta laika ieraksts
1.  Mobilajā ierīcē atlasiet darbvietu **Projekta laika ieraksts**.
2.  Atlasiet vienumu **Laika ieraksts**. Tiek parādīti kalendāra datumi pašreizējai nedēļai.
3.  Atlasītajam datumam atlasiet vienumu **Darbības** &gt; **Jauns ieraksts**.
4.  Ievadiet reģistrējamo stundu skaitu.
5.  Atlasiet projektu šim laika ierakstam. Tiek parādīts to projektu saraksts, kas ir ielādēti programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju izstrādātāji var skatīt rakstā [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Ja nepieciešamais projekts nav ietverts šajā sarakstā, atlasiet vienumu **Meklēt**, lai veiktu tiešsaistes meklēšanu sistēmā Dynamics 365 for Operations. Meklējiet pēc nosaukuma vai pārslēdziet uz meklēšanu pēc projekta nosaukuma vai debitora.
7.  Atlasiet kategoriju. Tiek parādīts to kategoriju saraksts, kas ir ielādētas programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju izstrādātāji var skatīt rakstā [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Ja vajadzīgā kategorija nav ietverta sarakstā, atlasiet vienumu **Meklēt**, lai veiktu tiešsaistes meklēšanu programmatūrā Dynamics 365 for Operations. Meklējiet pēc kategorijas vai pārslēdzieties uz meklēšanu pēc kategorijas nosaukuma.
9.  Atlasiet kādu aktivitāti. Tiek parādīts to aktivitāšu saraksts, kas ir ielādētas programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju izstrādātāji var skatīt rakstā [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Ja nepieciešamā aktivitāte nav ietverta šajā sarakstā, atlasiet vienumu **Meklēt**, lai veiktu tiešsaistes meklēšanu sistēmā Dynamics 365 for Operations. Meklējiet pēc aktivitātes numura vai pārslēdziet uz meklēšanu pēc nolūka.
11. Atlasiet rindas rekvizītu.
12. Pēc izvēles: ievadiet jebkādus ārējus un iekšējus komentārus.
13. Atlasiet **Gatavs**.






