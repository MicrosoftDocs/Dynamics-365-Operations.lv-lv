---
title: Kreditoru sadarbības mobilā darbvieta
description: Šajā rakstā ir sniegta informācija par Kreditoru sadarbības mobilo darbvietu. Šī darbvieta palīdz kreditoriem pastāvīgi būt informētiem par pirkšanas pasūtījumiem, kas viņiem ir nosūtīti apstiprināšanai. Viņi var skatīt arī informāciju par jauniem un atjauninātiem pirkšanas pasūtījumiem un kontaktpersonām.
author: GalynaFedorova
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: gfedorova
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 75c044d1133e1c4765cd97f4ab7e2a08ba998c35
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112156"
---
# <a name="vendor-collaboration-mobile-workspace"></a>Kreditoru sadarbības mobilā darbvieta

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Šajā rakstā ir sniegta informācija par Kreditoru sadarbības **mobilo** darbvietu. Šī darbvieta palīdz kreditoriem pastāvīgi būt informētiem par pirkšanas pasūtījumiem, kas viņiem ir nosūtīti apstiprināšanai. Viņi var skatīt arī informāciju par jauniem un atjauninātiem pirkšanas pasūtījumiem un kontaktpersonām.

Šo mobilo darbvietu ir paredzēts izmantot ar finanšu un operāciju (Dynamics 365) mobilo programmu.

## <a name="overview"></a>Pārskats 
Mobilā darbvieta **Kreditoru sadarbība** kreditoriem pastāvīgi nodrošina informāciju par jaunajiem pirkšanas pasūtījumiem, lai viņi varētu redzēt pirkšanas pasūtījumus un uz tiem reaģēt tīmekļa klientā. 

>[!NOTE]
> Mobilā darbvieta ir jālieto kā papildinājums kreditoru sadarbības tīmekļa interfeisam, nevis kā tā aizstājējs. 

Izmantojot mobilo darbvietu **Kreditoru sadarbība**, jūsu kreditori var skatīt jaunos pirkšanas pasūtījumus, kas viņiem ir nosūtīti apstiprināšanai. Tajā tiek rādīta pirkšanas pasūtījuma informācija, piemēram, preces, daudzumi un pieprasītie piegādes datumi. Ir pieejama arī informācija par cenu atkarībā no katra kreditora konfigurācijas. 

Lietotājs, kas pierakstās kā kreditors, var redzēt, uz kuriem pirkšanas pasūtījumiem ir atbildēts un kuriem pirkšanas pasūtījumiem joprojām tiek gaidīta debitora darbība. Piemēram, pirkšanas pasūtījums var gaidīt debitora darbību, jo kreditors ir ieteicis citu piegādes datumu, bet debitors vēl nav piekritis šim datumam. Kreditoram ir redzams arī saraksts ar pirkšanas pasūtījumiem, kas ir apstiprināti, bet vēl nav piegādāti. 

Lai atbildētu uz pirkšanas pasūtījumu, kreditoram ir jālieto kreditoru sadarbības tīmekļa interfeiss, kas ir pieejams tīmekļa klientā. Tur kreditors var saņemt arī papildinformāciju par pasūtījumu, piemēram, dokumentu pielikumus, piegādes adresi katrai rindai, kā arī ar kreditoru saistītās izmaksas. 

Kreditori, kam ir īpaša drošības loma, var redzēt, kuras kontaktpersonas ir reģistrētas kādam kreditora kontam. Tā pati drošības loma ļauj kreditoram skatīt statusu jebkuram iesniegtajam lietotāja pieprasījumam. 

Kreditoru sadarbības tīmekļa interfeiss tīmekļa klientā ir jāizmanto, lai izveidotu jaunas kontaktpersonas un iesniegtu jaunus lietotāju pieprasījumus. 

Mobilā darbvieta **Kreditoru sadarbība** kreditoram ļauj veikt tālāk norādītos uzdevumus.

-   Skatiet jaunus pirkšanas pasūtījumus, kas ir nosūtīti kreditoram.
-   Skatiet pirkšanas pasūtījumus, uz kuriem kreditors ir atbildējis un kuri gaida debitora darbību.
-   Skatiet pirkšanas pasūtījumus, kas ir apstiprināti, bet vēl nav saņemti pilnībā.
-   Skatiet kontaktpersonas informāciju, kas ir reģistrēta kreditora kontam. (Šim uzdevumam ir nepieciešama papildu drošības loma.)
-   Skatiet informāciju par kreditora iesniegto lietotāja pieprasījumu un sekojiet līdzi pieprasījuma statusam. (Šim uzdevumam ir nepieciešama papildu drošības loma.)

## <a name="prerequisites"></a>Priekšnosacījumi
Priekšnosacījumi atšķiras atkarībā no jūsu organizācijai izvietotās Microsoft Dynamics 365 versijas.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Priekšnosacījumi, ja izmantojat Supply Chain Management
Ja jūsu organizācijai ir izvietota programmatūra Supply Chain Management, sistēmas administratoram ir jāpublicē mobilā darbvieta **Kreditoru sadarbība**. Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Priekšnosacījumi, ja izmantojat Microsoft Dynamics 365 for Operations versiju 1611 ar 3. platformas atjauninājumu vai jaunāku versiju
Ja jūsu organizācijai ir izvietota Microsoft Dynamics 365 for Operations versija 1611 ar 3. platformas atjauninājumu vai jaunāku tā versiju, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi. 

<table>
<thead>
<tr class="header">
<th>Priekšnoteikumi</th>
<th>Loma</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ja izmantojat 3. platformas atjauninājumu, ir&#39;jāievieš KB 3216943.</td>
<td>Sistēmas administrators</td>
<td>KB 3216943 ir binārais atjauninājums, kas ir&#39;nepieciešams, ja izmantojat 3. platformas atjauninājumu. Lai ieviestu šo KB, sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li>Lejupielādējiet KB 3216943 no pakalpojuma Microsoft Dynamics Lifecycle Services (LCS).</li>
<li>Instalējiet bināro atjauninājumu, kas ir nodrošināts kā izvietojama pakotne. Informāciju par to, kā lietot izvietojamu pakotni, skatiet sadaļā <a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Lietot izvietojamu pakotni</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Jāievieš KB 4013633.</td>
<td>Sistēmas administrators</td>
<td>KB 4013633 ir X++ atjauninājums jeb metadatu labojumfails, kurā ir ietverta mobilā darbvieta <strong>Rīcībā esošie krājumi</strong>. Lai ieviestu KB 4013633, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lejupielādējiet metadatu labojumfailu no LCS</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li><li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Lietojiet izvietojamo pakotni</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Mobilajai darbvietai <strong>Kreditoru sadarbība</strong> ir jābūt publicētai.</td><td>Sistēmas administrators</td>
<td>Skatiet tēmu <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobilās darbvietas publicēšana</a>.</td>
</tr>
<tr class="even">
<td>Piegādātāja lietotājam ir jānodrošina piekļuve kreditoru sadarbības tīmekļa interfeisam tīmekļa klientā un ir jāiestata kreditoru sadarbības lietotājs.</td><td>Iepirkumu speciālisti un sistēmas administrators</td>
<td>Lai iestatītu un strādātu ar kreditora sadarbības web interfeisu, rīkojieties saskaņā ar tālāk minētajiem rakstiem.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Lietot kreditoru sadarbību, lai strādātu ar ārējiem kreditoriem</a></li>
<li><a href="manage-vendor-collaboration-users.md">Pārvaldīt kreditoru sadarbības lietotājus</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Kreditoru sadarbības iestatīšana un uzturēšana</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Lietot kreditoru sadarbību, lai strādātu ar debitoriem programmatūrā Supply Chain Managements</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobilās programmas lejupielāde un instalēšana

Lejupielādējiet un instalējiet finanšu un operāciju (Dynamics 365) mobilo programmu:

-   [Programma Android tālruņiem](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Tālruņiem iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Pierakstīšanās mobilajā programmā
1.  Palaidiet programmu savā mobilajā ierīcē.
2.  Ievadiet savu Microsoft Dynamics 365 vietrādi URL.
4.  Pirmajā pierakstīšanās reizē tiek prasīts ievadīt lietotājvārdu un paroli. Ievadiet savus akreditācijas datus.
5.  Pēc pierakstīšanās tiek parādītas jūsu uzņēmumam pieejamās darbvietas. Ņemiet vērā, ka gadījumā, ja sistēmas administrators vēlāk publicēs jaunu darbvietu, jums būs jāatsvaidzina mobilo darbvietu saraksts.

    [![Velciet, lai atsvaidzinātu.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Mobilās darbvietas Kreditoru sadarbība lietošana
Atlasot darbvietu **Kreditoru sadarbība**, būs redzamas tālāk norādītās opcijas.

![Kreditoru sadarbības mobilā darbvieta.](./media/vendor-collaboration-mobile-app.png)

Darbvietā **Kreditoru sadarbība** ir tālāk aprakstītās lapas.

### <a name="contacts"></a>Kontaktpersonas
Lapā **Kontaktpersonas** varat redzēt visas kontaktpersonas, kas ir iestatītas attiecīgajam kreditora kontam. Tajā parādīts kontaktpersonas vārds, primārā e-pasta adrese un lietotāja aizstājvārds, ja kontaktpersonai tāds ir. Šajā lapā tiek arī rādīts, vai kontaktpersonas lietotāja konts ir aktīvs. Atlasot kontaktpersonu, varat skatīt tādu informāciju par kontaktpersonu kā juridiskās personas, kam šī persona ir kontaktpersona. Varat arī skatīt kontaktinformāciju, piemēram, tālruņa numuru vai alternatīvo e-pasta adresi.

### <a name="user-requests"></a>Lietotāja pieprasījumi
Lapā **Lietotāju pieprasījumi** varat redzēt visus lietotāju pieprasījumus, ko esat iesniedzis, izmantojot kreditoru sadarbības tīmekļa interfeisu. Varat arī sekot šo pieprasījumu statusam. Ja atlasāt kādu lietotāja pieprasījumu, varat redzēt, kas tika pieprasīts, pievienot vai deaktivizēt lietotāju, mainīt drošību un redzēt, kuras drošības lomas šim lietotājam tika pieprasītas.

### <a name="purchase-orders-ready-for-review"></a>Pārskatīšanai gatavie pirkšanas pasūtījumi
Lapā **Pārskatīšanai gatavie pirkšanas pasūtījumi** varat redzēt visus debitora sūtītos pirkšanas pasūtījumus, uz ko vēl nav atbildēts. Varat apskatīt noteiktu informāciju par pasūtījumu, piemēram, kuras preces tika pieprasītas un kad šīs preces ir jāpiegādā. Atkarībā no kreditora konfigurācijas ir pieejama arī informācija par cenu.

Varat arī redzēt, vai pirkšanas pasūtījumam ir kādas piezīmes vai pielikumi. Tomēr, lai atvērtu piezīmes un pielikumus, ir jāizmanto kreditoru sadarbības tīmekļa interfeiss tīmekļa klientā. Atlasiet vienumu **Pirkšanas pasūtījuma rinda**, lai skatītu visas rindas kopā ar to informāciju. Katrai rindai indikators norāda, vai pastāv piezīmes vai pielikumi un vai piegādes adrese atšķiras no virsrakstā rādītās.

Lai atbildētu uz pirkšanas pasūtījumu, ir jāizmanto kreditoru sadarbības tīmekļa interfeiss tīmekļa klientā.

### <a name="awaiting-customer-action"></a>Tiek gaidīta debitora darbība
Lapā **Tiek gaidīta debitora darbība** varat atrast pirkšanas pasūtījumus, uz kuriem esat atbildējis jūs vai cita persona jūsu uzņēmumā, kam ir piekļuve kreditoru sadarbībai. Pirkšanas pasūtījumi šajā sarakstā ir redzami tikai tad, ja debitoram šajā pirkšanas pasūtījumā ir jāizpilda viena no tālāk norādītajām darbībām.

-   Ja pirkšanas pasūtījums tika noraidīts, debitoram ir jāatjaunina vai jāatceļ sākotnējais pasūtījums un pēc tam tas jānosūta atkārtoti. Kad pirkšanas pasūtījums ir nosūtīts vēlreiz, tas vairs nav redzams lapā **Tiek gaidīta debitora darbība**.
-   Ja pirkšanas pasūtījums tika pieņemts ar izmaiņām, debitoram ir jāatjaunina sākotnējais pasūtījums un jāsūta atkārtoti pārskatīšanai vai jāatjaunina pasūtījums atbilstoši pieprasītajām izmaiņām un nekavējoties jāapstiprina. Abos gadījumos pirkšanas pasūtījums vairs netiek rādīts lapā **Tiek gaidīta debitora darbība**.
-   Ja pirkšanas pasūtījums tika pieņemts, bet joprojām ir redzams lapā **Tiek gaidīta debitora darbība**, tad nozīmē, ka pieņemšanas laikā šis pirkšanas pasūtījums netika apstiprināts automātiski. Tiek gaidīts, līdz pirkšanas aģents šī pasūtījuma statusu nomainīs uz **Apstiprināts**. Parasti pirkšanas pasūtījums tiek uzskatīts par līgumu starp debitoru un kreditoru, līdzko kreditors pieņem pasūtījumu. Tāpēc atjaunināšana uz statusu **Apstiprināts** parasti ir tikai formalitāte.

Kad atlasāt pirkšanas pasūtījumu, par atbildi tiek parādīta papildu informācija. Varat redzēt rindas informāciju un atbildi par katru rindu. Rindas statuss norāda, kura no tālāk uzskaitītajām atbildēm tika sniegta.

-   Pieņemts
-   Noraidīts
-   Apstiprināts ar izmaiņām
-   Aizstāts/Aizstājējs
-   Sadalīts grafikā/Grafika rinda

Ņemiet vērā, ka lauks **Tiek piegādāts** ir iestatīts uz **Jā** vai **Nē**, lai norādītu, vai rindas tiks piegādātas. Rindu var nepiegādāt tālāk norādīto iemeslu dēļ.

- Rinda tika noraidīta.
- Tika veikta aizvietošana, un sākotnējo rindu nav paredzēts piegādāt, kā tas ir pieprasīts saņemtajā pasūtījumā.
- Rinda tika sadalīta vairākās grafika rindās, un sākotnējo rindu nav paredzēts piegādāt, kā tas ir pieprasīts saņemtajā pasūtījumā.

Tiek rādītas visas pasūtījuma rindas atbildē veiktās izmaiņas. Taču augšupielādētās piezīmes un pielikumi netiek rādīti. Lai skatītu piezīmes un pielikumus, ir jāizmanto kreditoru sadarbības tīmekļa interfeiss tīmekļa klientā.

### <a name="open-confirmed-orders"></a>Atvērtie apstiprinātie pasūtījumi
Kad debitors apstiprina pirkšanas pasūtījumu (t.i., pirkšanas pasūtījuma statuss mainās uz **Apstiprināts**), tas tiek parādīts atvērto apstiprināto pasūtījumu sarakstā. Tas šajā sarakstā paliek, līdz debitors to reģistrē kā saņemtu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

