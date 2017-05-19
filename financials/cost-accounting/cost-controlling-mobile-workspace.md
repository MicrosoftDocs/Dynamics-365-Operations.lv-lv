---
title: "Izmaksu kontrolēšanas mobilā darbvieta"
description: "Šajā tēmā ir sniegta informācija par mobilo darbvietu Izmaksu kontrole, kura ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šī darbvieta ļauj izmaksu centra vadītājiem skatīt informāciju par izmaksu centra veiktspēju jebkurā laikā un vietā."
author: YuyuScheller
manager: AnnBe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 31a9650774b2ddb70827ffa210154ca10c761236
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Izmaksu kontrolēšanas mobilā darbvieta

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta informācija par mobilo darbvietu Izmaksu kontrole, kura ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šī darbvieta ļauj izmaksu centra vadītājiem skatīt informāciju par izmaksu centra veiktspēju jebkurā laikā un vietā. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Pārskats par mobilo darbvietu Izmaksu kontrole
-------------------------------------------------

Mobilā darbvieta **Izmaksu kontrole** sniedz tūlītēju skatu uz izmaksu centru pašreizējo veiktspēju, faktiskās izmaksas salīdzinot ar budžetā paredzētajām izmaksām. Varat skatīt detalizētāku informāciju līdz pat atsevišķu izmaksu elementu statusiem. Piemēram, darbinieks saņem uzaicinājumu uz starptautisku konferenci, bet organizācijai ir jāsedz visi ceļa izdevumi. Darbinieks savam vadītājam vaicā, vai ir iespējams apmeklēt šo konferenci. Vadītājs savā mobilajā ierīcē ātri atver mobilo darbvietu **Izmaksu kontrole**, lai apskatītu, vai ir pieejams budžets, lai darbinieks šo konferenci varētu apmeklēt.

### <a name="data-security"></a>Datu drošība

Darbvietā **Izmaksu kontrole** datus aizsargā lietotāja akreditācijas dati. Izmaksu centra vadītājiem ir atļauts skatīt tikai datus par savu izmaksu centru. Piekļuves līmeņa drošība tiek pārvaldīta modulī **Izmaksu uzskaite**. Izmaksu grāmatveži mobilās darbvietas **Izmaksu kontrole** konfigurāciju definē modulī **Izmaksu uzskaite**. Kad šī darbvieta ir publicēta Microsoft Dynamics 365 for Operations mobilajā programmā, tā ir pieejama programmā. Tādējādi visi organizācijas izmaksu centra vadītāji var skatīt datus vienādā formātā.

### <a name="actions-views-and-links"></a>Darbības, skati un saites

Mobilajā darbvietā **Izmaksu kontrole** programmai Dynamics 365 for Operations ir pieejamas tālāk uzskaitītās darbības, skati un saites.

-   **Darbības:**
    -   Izmantojiet vienumu **Atlasīt konfigurāciju**, lai atlasītu izkārtojumu.
    -   Izmantojiet vienumu **Atlasīt izmaksu objektu**, lai atlasītu izmaksu centrus, par kuriem filtrēt datus. **Piezīme.** Izmaksu centri, kas tiek rādīti sarakstā, ir atkarīgi no pieejas, kas piešķirta modulī **Izmaksu uzskaite**.
-   **Skati.** Atkarībā no atlasītajām darbībām un konfigurācijas modulī **Izmaksu uzskaite** kartēs varat skatīt tālāk aprakstīto informāciju.
    -   Faktiski pret budžetu (pašreizējais periods)
    -   Faktiski pret pārskatīto budžetu (pašreizējais periods)
    -   Faktiski pret budžetu (iepriekšējais periods)
    -   Faktiski pret pārskatīto budžetu (iepriekšējais periods)
    -   Faktiski pret budžetu (no gada sākuma)
    -   Faktiski pret pārskatīto budžetu (no gada sākuma)

    Katrā kartē tiek rādītas šādas summas: Faktiski, Budžets, Novirze un Novirze %.
-   **Saites:**
    -   Informācija pašreizējam periodam
    -   Informācija iepriekšējam periodam
    -   Informācija līdzšinējam gadam

    Atlasot saiti, katram izmaksu elementam tiek parādīta karte. Katrā kartē tiek rādītas šādas summas: Faktiski, Budžets, Budžeta novirze, Budžeta novirze %, Pārskatītais budžets, Pārskatītā budžeta novirze un Pārskatītā budžeta novirze %. 
    
    [![Izmaksu elementa karte ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Priekšnosacījumi
Lai varētu izmantot mobilo darbvietu **Izmaksu kontrole**, pārliecinieties, ka sistēmas administrators ir izpildījis tālāk minētos priekšnosacījumus.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Priekšnoteikumi</th>
<th>Loma</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Jābūt ieviestai Dynamics 365 for Operations versijai 1611 ar 3. vai jaunāku platformas atjauninājumu.</td>
<td>Sistēmas administrators</td>
<td>Ja programma Dynamics 365 for Operations vēl nav izvietota jūsu organizācijā, sistēmas administratoram vajadzētu izlasīt rakstu <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Microsoft Dynamics 365 for Operations izvietošana demonstrācijas vidē</a>.</td>
</tr>
<tr class="even">
<td>Jāievieš KB 4013633.</td>
<td>Sistēmas administrators</td>
<td>KB 4013633 (X++ atjauninājums vai metadatu labojumfails) satur četras mobilās darbvietas piegādes ķēdes pārvaldībai. Lai ieviestu KB 4013633, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības:
<ol>
<li>Lejupielādējiet KB 4013633 no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Lietojiet šo izvietojamo pakotni</a> savai Dynamics 365 for Operations sistēmai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilā darbvieta <strong>Izmaksu kontrole</strong> ir jāpublicē Dynamics 365 for Operations mobilajā programmā.</td>
<td>Sistēmas administrators</td>
<td><ol>
<li>Palaidiet pārlūkprogrammā programmu Dynamics 365 for Operations.</li>
<li>Lapā <strong>Sistēmas parametri</strong> atlasiet <strong>Mobilo darbvietu pārvaldība</strong>.</li>
<li>Atlasiet darbvietu <strong>Izmaksu objektu pārskats</strong>.</li>
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
4.  Pirmajā pierakstīšanās reizē ir jāievada Dynamics 365 for Operations konta lietotājvārds un parole. Ievadiet savus akreditācijas datus.
5.  Pēc pierakstīšanās ir redzamas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā — ja sistēmas administrators vēlāk publicēs jaunu darbvietu, varat vilkt, lai atsvaidzinātu mobilo darbvietu sarakstu. 

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





