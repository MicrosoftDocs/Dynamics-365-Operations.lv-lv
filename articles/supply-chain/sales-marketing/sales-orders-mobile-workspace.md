---
title: Pārdošanas pasūtījumu mobilā darbvieta
description: Šajā rakstā ir sniegta informācija par pārdošanas pasūtījumu mobilo darbvietu. Šī darbvieta jums palīdz pastāvīgi būt informētam par saviem pārdošanas pasūtījumiem jebkurā vietā un jebkurā laikā.
author: Henrikan
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 38971f2a5f3f3d2692de0e52365e2215170101cc
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103186"
---
# <a name="sales-orders-mobile-workspace"></a>Pārdošanas pasūtījumu mobilā darbvieta

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Šajā rakstā ir sniegta informācija par pārdošanas pasūtījumu **mobilo** darbvietu. Šī darbvieta jums palīdz pastāvīgi būt informētam par saviem pārdošanas pasūtījumiem jebkurā vietā un jebkurā laikā. 

Šo mobilo darbvietu ir paredzēts izmantot ar finanšu un operāciju (Dynamics 365) mobilo programmu.

## <a name="overview"></a>Pārskats
Mobilajā darbvietā **Pārdošanas pasūtījumi** var apskatīt detalizētu informāciju par katru pārdošanas pasūtījumu. Šī informācija ietver pasūtījuma statusu, kontaktinformāciju par debitoru un kontaktinformāciju par pasūtījuma veicēju. Mobilā darbvieta **Pārdošanas pasūtījumi** sniedz iespēju nekavējoties skatīt pārdošanas pasūtījumus. Varat skatīt visus pārdošanas pasūtījumus, skatīt pārdošanas pasūtījumus pēc debitora vai skatīt informāciju par konkrētu pārdošanas pasūtījumu. 

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
Priekšnosacījumi atšķiras atkarībā no jūsu organizācijai izvietotās Microsoft Dynamics 365 versijas.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Priekšnosacījumi, ja izmantojat Supply Chain Management 
Ja jūsu organizācijai ir izvietota programmatūra Supply Chain Management, sistēmas administratoram ir jāpublicē mobilā darbvieta **Pārdošanas pasūtījumi**. Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Priekšnosacījumi, ja izmantojat Dynamics 365 for Operations versiju 1611 ar 3. platformas atjauninājumu vai jaunāku versiju
Ja jūsu organizācijai ir izvietota Dynamics 365 for Operations versija 1611 ar 3. platformas atjauninājumu vai jaunāku tā versiju, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi. 

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

<td>KB 4013633 ir X++ atjauninājums jeb metadatu labojumfails, kurā ir ietverta mobilā darbvieta <strong>Pārdošanas pasūtījumi</strong>. Lai ieviestu KB 4013633, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lejupielādējiet metadatu labojumfailu no portāla Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Lietojiet izvietojamo pakotni</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicējiet mobilo darbvietu <strong>Pārdošanas pasūtījumi</strong>.</td>
<td>Sistēmas administrators</td>
<td>Skatiet tēmu <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobilās darbvietas publicēšana</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobilās programmas lejupielāde un instalēšana
Lejupielādējiet un instalējiet finanšu un operāciju (Dynamics 365) mobilo programmu:

-   [Programma Android tālruņiem](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Tālruņiem iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Pierakstīšanās mobilajā programmā

1.  Palaidiet programmu savā mobilajā ierīcē.
2.  Ievadiet savu Dynamics 365 vietrādi URL.
3.  Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.
4.  Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.

[![Velciet, lai atsvaidzinātu.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Informācijas par kāda debitora pārdošanas pasūtījumiem skatīšana, izmantojot mobilo darbvietu Pārdošanas pasūtījums

1.  Mobilajā ierīcē atlasiet darbvietu **Pārdošanas pasūtījumi**.
2.  Atlasiet vienumu **Skatīt noteikta debitora pasūtījumus**.
3.  Debitora atrašanas nolūkos izmatojiet konta vai debitora nosaukuma informāciju.
4.  Atlasiet debitoru.
5.  Atlasiet vienumu **Kontaktinformācija** vai **Pārdošanas pasūtījumi**. Ja atlasāt vienumu **Pārdošanas pasūtījumi**, tiek parādīts šī debitora pārdošanas pasūtījumu saraksts.
6.  Atlasiet vienumu **Pārdošanas pasūtījums**. Tagad varat skatīt informāciju par pārdošanas pasūtījuma rindām, informāciju par sūtījumiem, debitora kontaktinformāciju un pasūtījuma veicēja kontaktinformāciju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

