---
title: Izmaksu kontrolēšanas mobilā darbvieta
description: Šajā tēmā ir sniegta informācija par mobilo darbvietu Izmaksu kontrolēšana. Šī darbvieta ļauj izmaksu centra vadītājiem skatīt informāciju par izmaksu centra veiktspēju jebkurā laikā un vietā.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4fc35feb4f3a67ba9c8c70c2d2f8c07cb944b0f6
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2020
ms.locfileid: "4445812"
---
# <a name="cost-controlling-mobile-workspace"></a>Izmaksu kontrolēšanas mobilā darbvieta

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par mobilo darbvietu **Izmaksu kontrolēšana**. Šī darbvieta ļauj izmaksu centra vadītājiem skatīt informāciju par izmaksu centra veiktspēju jebkurā laikā un vietā.

Šī mobilā darbvieta ir paredzēta lietošanai kopā ar mobilo programmu Finance and Operations.

## <a name="overview"></a>Pārskats
Mobilā darbvieta **Izmaksu kontrole** sniedz tūlītēju skatu uz izmaksu centru pašreizējo veiktspēju, faktiskās izmaksas salīdzinot ar budžetā paredzētajām izmaksām. Varat skatīt detalizētu informāciju ar atsevišķu izmaksu elementu statusu.

Piemēram, darbinieks saņem uzaicinājumu uz starptautisku konferenci, bet organizācijai ir jāsedz visi ceļa izdevumi. Darbinieks vaicā savam vadītājam, vai var apmeklēt šo konferenci. Vadītājs savā mobilajā ierīcē ātri atver mobilo darbvietu **Izmaksu kontrole**, lai apskatītu, vai ir pieejams budžets, lai darbinieks šo konferenci varētu apmeklēt.

### <a name="data-security"></a>Datu drošība
Darbvietā **Izmaksu kontrole** datus aizsargā lietotāja akreditācijas dati. Izmaksu centra vadītājiem ir atļauts skatīt tikai datus par savu izmaksu centru. Piekļuves līmeņa drošība tiek pārvaldīta modulī **Izmaksu uzskaite**.

Izmaksu grāmatveži mobilās darbvietas **Izmaksu kontrole** konfigurāciju definē modulī **Izmaksu uzskaite**. Pēc darbvietas publicēšanas mobilajā programmā tā ir pieejama programmā. Tādējādi visi organizācijas izmaksu centra vadītāji var skatīt datus vienādā formātā.

### <a name="actions-views-and-links"></a>Darbības, skati un saites
Mobilajā darbvietā **Izmaksu kontrolēšana** ir pieejamas tālāk norādītās darbības, skati un saites.

-   **Darbības:**

    -   Izmantojiet vienumu **Atlasīt konfigurāciju**, lai atlasītu izkārtojumu.
    -   Izmantojiet vienumu **Atlasīt izmaksu objektu**, lai atlasītu izmaksu centrus, par kuriem filtrēt datus.
    
        > [!NOTE]
        > Sarakstā redzamie izmaksu centri ir atkarīgi no modulī **Izmaksu uzskaite** piešķirtajām piekļuves tiesībām.

-   **Skati:** atkarībā no atlasītajām darbībām un konfigurācijas modulī **Izmaksu uzskaite** kartēs tiek rādīta tālāk norādītā informācija.

    -   Faktiski pret budžetu (pašreizējais periods)
    -   Faktiski pret pārskatīto budžetu (pašreizējais periods)
    -   Faktiski pret budžetu (iepriekšējais periods)
    -   Faktiski pret pārskatīto budžetu (iepriekšējais periods)
    -   Faktiski pret budžetu (no gada sākuma)
    -   Faktiski pret pārskatīto budžetu (no gada sākuma)

    Katrā kartē tiek rādītas šādas summas: Faktiski, Budžets, Novirze un Novirze %.

-   **Saites:**

    -   Informācija pašreizējam periodam
    -   Informācija iepriekšējam periodam
    -   Informācija līdzšinējam gadam

    Atlasot saiti, katram izmaksu elementam tiek parādīta karte. Katrā kartē tiek rādītas šādas summas: Faktiski, Budžets, Budžeta novirze, Budžeta novirze %, Pārskatītais budžets, Pārskatītā budžeta novirze un Pārskatītā budžeta novirze %.
    
    [![Izmaksu elementa karte](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Priekšnosacījumi
Priekšnosacījumi atšķiras atkarībā no jūsu organizācijai izvietotās Microsoft Dynamics 365 versijas.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Priekšnosacījumi, ja izmantojat Microsoft Dynamics 365 Finance
Ja jūsu organizācijai ir izvietota programma Finance, sistēmas administratoram ir jāpublicē mobilā darbvieta **Izmaksu kontrolēšana**. Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Priekšnosacījumi, ja izmantojat versiju 1611 ar 3. platformas atjauninājumu vai jaunāku versiju
Ja jūsu organizācijai ir izvietota versija 1611 ar 3. platformas atjauninājumu vai jaunāku tā versiju, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi.

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
<td>Ieviesiet KB 4013633.</td>
<td>Sistēmas administrators</td>

<td>KB 4013633 ir X++ atjauninājums jeb metadatu labojumfails, kurā ir ietverta mobilā darbvieta <strong>Izmaksu kontrolēšana</strong>. Lai ieviestu KB 4013633, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Lejupielādējiet metadatu labojumfailu no portāla Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Lietojiet izvietojamo pakotni</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicējiet mobilo darbvietu <strong>Izmaksu kontrolēšana</strong>.</td>
<td>Sistēmas administrators</td>
<td>Skatiet tēmu <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobilās darbvietas publicēšana</a>.</td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a>Mobilās programmas lejupielāde un instalēšana
Mobilās programmas Finance and Operations lejupielāde un instalēšana.

-   [. Android tālruņiem](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Tālruņiem iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Pierakstīšanās mobilajā programmā

1.  Palaidiet programmu savā mobilajā ierīcē.
2.  Ievadiet savu Dynamics 365 vietrādi URL.
3.  Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.
4.  Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.

[![Velciet, lai atsvaidzinātu](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>Skatiet sava izmaksu centra veiktspēju, izmantojot mobilo darbvietu Izmaksu kontrole

1.  Mobilajā ierīcē atlasiet darbvietu **Izmaksu kontrole**.
2.  Atlasiet vienumu **Izmaksu objektu kontrole**.
3.  Atlasiet **Darbības**.
4.  Atlasiet vienumu **Atlasīt konfigurāciju**, lai atlasītu izmaksu kontroles izkārtojumu.
5.  Atlasiet **Gatavs**.
6.  Atlasiet **Darbības**.
7.  Atlasiet vienumu **Atlasīt izmaksu objektu**, lai atlasītu izmaksu centrus, kuriem jums ir piešķirta piekļuve.
8.  Atlasiet **Gatavs**.
9.  Skatiet vispārēju sava izmaksu centra veiktspēju.
10. Atlasiet saiti **Informācija pašreizējam periodam**.
11. Skatiet atsevišķu izmaksu elementu veiktspēju.
12. Varat arī meklēt konkrētus izmaksu elementus.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]