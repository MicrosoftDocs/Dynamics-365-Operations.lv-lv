---
title: "Pārdošanas pasūtījumu mobilā darbvieta"
description: "Šajā tēmā ir sniegta informācija par mobilo darbvietu Pārdošanas pasūtījumi, kura ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šī darbvieta jums palīdz pastāvīgi būt informētam par saviem pārdošanas pasūtījumiem jebkurā vietā un jebkurā laikā."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11898146a13756a6bb22a769e37e8773484e0d04
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Pārdošanas pasūtījumu mobilā darbvieta

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta informācija par mobilo darbvietu Pārdošanas pasūtījumi, kura ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šī darbvieta jums palīdz pastāvīgi būt informētam par saviem pārdošanas pasūtījumiem jebkurā vietā un jebkurā laikā. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Apskats par mobilo darbvietu Pārdošanas pasūtījumi
---------------------------------------------

Mobila darbvieta **Pārdošanas pasūtījumi** piekļūst sistēmai Microsoft Dynamics 365 for Operations un ļauj jums apskatīt detalizētu informāciju par katru pārdošanas pasūtījumu. Šī informācija ietver pasūtījuma statusu, kontaktinformāciju par debitoru un kontaktinformāciju par pasūtījuma veicēju. Mobilā darbvieta **Pārdošanas pasūtījumi** sniedz iespēju nekavējoties skatīt pārdošanas pasūtījumus. Varat skatīt visus pārdošanas pasūtījumus, skatīt pārdošanas pasūtījumus pēc debitora vai skatīt informāciju par konkrētu pārdošanas pasūtījumu. 

Mobilā darbvieta nodrošina divus skatus, kas palīdz detalizēti analizēt pārdošanas pasūtījumus.

### <a name="view-all-sales-orders"></a>Skatīt visus pārdošanas pasūtījumus

Šajā skatā tiek rādīti visi pārdošanas pasūtījumi.

-   Lai atlasītu apskatāmos pārdošanas pasūtījumus, izmantojiet kādu no tālāk norādītajiem filtriem.
    -   Meklēt pēc pārdošanas pasūtījuma
    -   Meklēt pēc debitora konta
    -   Meklēt pēc debitora nosaukuma
    -   Meklēt pēc statusa
    -   Meklēt pēc nodošanas izpildei statusa
    -   Meklēt pēc izveides datuma un laika
    
-   Pēc pārdošanas pasūtījumu atlasīšanas varat skatīt detalizētu informāciju par noteiktiem pasūtījumiem. Varat aplūkot tālāk aprakstīto informāciju.
    -   Debitora nosaukuma un adreses informācija
    -   Dažādi datumi saistībā ar pārdošanas pasūtījumu, piemēram, pieprasītais nosūtīšanas datums un apstiprinātais nosūtīšanas datums
    -   Kontaktinformācija par pasūtījuma veicēju
    -   Debitora kontaktinformācija
    -   Pasūtījuma rindas
    -   Sūtījumi, kas norāda pārdošanas pasūtījuma nosūtīšanas veidu un laiku

### <a name="view-orders-for-a-customer"></a>Skatīt noteikta debitora pasūtījumus

Šajā skatā tiek rādīti pārdošanas pasūtījumi pēc debitora.

-   Lai skatītu noteikta debitora pārdošanas pasūtījumus, izmantojiet tālāk norādītos filtrus,.
    -   Meklēt pēc nosaukuma
    -   Meklēt pēc konta

-   Kad esat atlasījis debitoru, varat aplūkot tālāk norādīto informāciju.
    -   Debitora nosaukums un grupa
    -   Debitora kontaktinformācija
    -   Debitora pārdošanas pasūtījumi un detalizēta informācija par šiem pārdošanas pasūtījumiem.
        -   Debitora nosaukuma un adreses informācija
        -   Dažādi pārdošanas pasūtījumu datumi
        -   Kontaktinformācija par pasūtījuma veicēju
        -   Debitora kontaktinformācija
        -   Pasūtījuma rindas
        -   Sūtījumi, kas norāda pārdošanas pasūtījuma nosūtīšanas veidu un laiku

## <a name="prerequisites"></a>Priekšnosacījumi
Lai varētu izmantot mobilo darbvietu **Pārdošanas pasūtījumi**, pārliecinieties, ka sistēmas administrators ir izpildījis tālāk minētos priekšnosacījumus.

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
<td>Jābūt ieviestai Dynamics 365 for Operations versijai 1611 ar 3. vai jaunāku platformas atjauninājumu.</td>
<td>Sistēmas administrators</td>
<td>Ja programma Dynamics 365 for Operations vēl nav izvietota jūsu organizācijā, sistēmas administratoram vajadzētu izlasīt rakstu <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment/">Microsoft Dynamics 365 for Operations izvietošana demonstrācijas vidē</a>.</td>
</tr>
<tr class="even">
<td>Jāievieš KB 4013633.</td>
<td>Sistēmas administrators</td>
<td>KB 4013633 (X++ atjauninājums vai metadatu labojumfails) satur četras mobilās darbvietas piegādes ķēdes pārvaldībai. Lai ieviestu KB 4013633, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības:
<ol>
<li>Lejupielādējiet KB 4013633 no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Lietojiet šo izvietojamo pakotni</a> savai Dynamics 365 for Operations sistēmai.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilajai darbvietai <strong>Pārdošanas pasūtījumi</strong> ir jābūt publicētai Dynamics 365 for Operations mobilajā programmā.</td>
<td>Sistēmas administrators</td>
<td><ol>
<li>Palaidiet pārlūkprogrammā programmu Dynamics 365 for Operations.</li>
<li>Lapā <strong>Sistēmas parametri</strong> atlasiet <strong>Mobilo darbvietu pārvaldība</strong>.</li>
<li>Atlasiet darbvietu <strong>Pārdošanas pasūtījumi</strong>.</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Skatīt informāciju par pārdošanas pasūtījumiem kādam debitoram, izmantojot mobilo darbvietu
1.  Mobilajā ierīcē atlasiet darbvietu **Pārdošanas pasūtījumi**.
2.  Atlasiet vienumu **Skatīt noteikta debitora pasūtījumus**.
3.  Debitora atrašanas nolūkos izmatojiet konta vai debitora nosaukuma informāciju.
4.  Atlasiet debitoru.
5.  Atlasiet vienumu **Kontaktinformācija** vai **Pārdošanas pasūtījumi**. Ja atlasāt vienumu **Pārdošanas pasūtījumi**, tiek parādīts šī debitora pārdošanas pasūtījumu saraksts.
6.  Atlasiet vienumu **Pārdošanas pasūtījums**. Tagad varat skatīt informāciju par pārdošanas pasūtījuma rindām, informāciju par sūtījumiem, debitora kontaktinformāciju un pasūtījuma veicēja kontaktinformāciju.





