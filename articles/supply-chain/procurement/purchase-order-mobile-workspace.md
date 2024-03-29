---
title: Pirkšanas pasūtījuma apstiprināšanas mobilā darbvieta
description: Šajā rakstā ir sniegta informācija par Pirkšanas pasūtījuma apstiprinājuma mobilo darbvietu, kas ļauj skatīt pirkšanas pasūtījumus un atbildēt uz tiem, izmantojot darbības. Piemēram, varat apstiprināt vai noraidīt pirkšanas pasūtījumu.
author: GalynaFedorova
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b5336549937edca6beb94137896f84b460f257f7
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111336"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Pirkšanas pasūtījuma apstiprināšanas mobilā darbvieta

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Šajā rakstā ir sniegta informācija par pirkšanas pasūtījuma **apstiprinājuma mobilo** darbvietu. Šajā darbvietā var apskatīt pirkšanas pasūtījumus un atbilstoši reaģēt ar darbībām. Piemēram, varat apstiprināt vai noraidīt pirkšanas pasūtījumu.
 
## <a name="overview"></a>Pārskats 
Apstiprināmajiem pirkšanas pasūtījumiem ir jāizmanto apstiprināšanas darbplūsma. Darbplūsma var ietvert dažādus soļus, kam nepieciešams, lai darbības veic viena vai vairākas personas. Piemēram, personai var būt nepieciešams izpildīt uzdevumu vai apstiprināt pirkšanas pasūtījumu. 

**Pirkšanas pasūtījuma apstiprināšanas** mobilo darbvietu var viegli apskatīt un atbildēt uz pirkšanas pasūtījumiem no mobilās ierīces. Šī darbvieta arī sniedz iespēju veikt tas pašas darbplūsmas darbību, ko var veikt tīmekļa klientā.

## <a name="prerequisites"></a>Priekšnosacījumi
Priekšnosacījumi atšķiras atkarībā no jūsu organizācijai izvietotās Supply Chain Management versijas.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Priekšnosacījumi, ja izmantojat Supply Chain Management 
Ja jūsu organizācijai ir izvietota programmatūra Supply Chain Management, sistēmas administratoram ir jāpublicē mobilā darbvieta **Pirkšanas pasūtījuma apstiprināšana**. Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Priekšnosacījumi, ja izmantojat Microsoft Dynamics 365 for Operations versiju 1611 ar 3. platformas atjauninājumu vai jaunāku versiju
Ja jūsu organizācijai ir izvietota Microsoft Dynamics 365 for Operations versija 1611 ar 3. platformas atjauninājumu vai jaunāku tā versiju, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi. 

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
<td>Ieviesiet KB 4017918.</td>
<td>Sistēmas administrators</td>
<td>KB 4017918 ir X++ atjauninājums vai metadatu labojumfails, kas ietver mobilo darbvietu <strong>Pirkšanas pasūtījuma apstiprināšana</strong>. Lai ieviestu KB 4017918, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lejupielādējiet metadatu labojumfailu no portāla Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Lietojiet izvietojamo pakotni</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publicējiet <strong>Pirkšanas pasūtījuma apstiprināšanas</strong> mobilo darbvietu.</td>
<td>Sistēmas administrators</td>
<td>Skatiet tēmu <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobilās darbvietas publicēšana</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobilās programmas lejupielāde un instalēšana
Lejupielādējiet un instalējiet finanšu un operāciju mobilo programmu:

- [Programma Android tālruņiem](https://go.microsoft.com/fwlink/?linkid=850662)
- [Tālruņiem iPhone](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Pierakstīšanās mobilajā programmā

1. Palaidiet programmu savā mobilajā ierīcē.
2. Ievadiet savu Microsoft Dynamics 365 vietrādi URL.
3. Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.
4. Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.

![Pirkšanas pasūtījuma apstiprināšanas darbvieta pieejamo darbvietu sarakstā.](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Piešķirto pasūtījumu skatīšana
1. Mobilajā ierīcē atlasiet darbvietu **Pirkšanas pasūtījuma apstiprināšana**.
2. Atlasiet **Man piešķirtie pasūtījumi**, lai skatītu visus pirkšanas pasūtījumus, saistībā ar kuriem jums ir uzdots veikt darbības pirkšanas pasūtījuma apstiprināšanas darbplūsmā.
3. Atlasiet pasūtījumu. Lapā **Pasūtījumu informācija** redzēsit pasūtījuma virsraksta informāciju un rindas. Norādījumus varat atrast arī darbplūsmas uzdevumā.
4. Atlasiet **Uzskaites sadale**, lai atvērtu lapu **Virsraksta uzskaites sadale**.
5. Atgriezieties lapā **Pasūtījuma informācija** un atlasiet rindu. No pasūtījuma rindas informācijas var pārlūkot arī līniju uzskaites sadales.

## <a name="complete-an-action-on-the-purchase-order"></a>Darbības izpilde no pirkšanas pasūtījuma
Pēc tam, kad apskatījāt pirkšanas pasūtījumu, kas jums ir piešķirts, un izlasījāt darbplūsmas instrukcijas, jums jābūt gataviem izpildīt darbību.

1. Mobilajā ierīcē atlasiet darbvietu **Pirkšanas pasūtījuma apstiprināšana**.
2. Atlasiet **Man piešķirtie pasūtījumi**, lai skatītu visus pirkšanas pasūtījumus, saistībā ar kuriem jums ir uzdots veikt darbības pirkšanas pasūtījuma apstiprināšanas darbplūsmā.
3. Atlasiet pasūtījumu un skatiet detalizētas informācijas lapu.
4. Atlasiet vienumu **Darbības**, lai parādītu pieejamās darbības. Pieejamās darbības ir atkarīgas no uzdevuma, kas jums ir piešķirts.

    | Uzdevuma darbības    | Apstiprināšanas darbība  |
    |----------------|------------------|
    | Aizpildīt       | Akceptēt          |
    | Atgriezt         | Noraidīt           |
    | Pieprasīt izmaiņas | Pieprasīt izmaiņas   |
    | Deleģēt       | Deleģēt         |

5. Atlasīt atbilstošu darbību.
6. Lapā **Uzdevuma izpilde** ievadiet komentāru. Ņemiet vērā! Atlasot darbību **Deleģēt**, ir jāatlasa lietotājs, kam deleģēt uzdevumu.
7. Atlasiet **Gatavs**. Pēc darbvietas atsvaidzināšanas pirkšanas pasūtījums vairs nebūs jūsu sarakstā. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

