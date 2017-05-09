---
title: "Mobilā darbvieta Kreditoru sadarbība Microsoft Dynamics 365 for Operations programmai"
description: "Izmantojot kreditoru sadarbības mobilo darbvietu, jūsu kreditori var uzzināt aktuālo informāciju par pirkšanas pasūtījumiem, kas viņiem ir nosūtīti apstiprināšanai, un apskatīt informāciju par jauniem un atjauninātiem pirkšanas pasūtījumiem un kontaktpersonām."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-01-12 16 - 36 - 37
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267074
ms.assetid: fe8e912d-8446-4584-8a24-d8892e9028cd
ms.search.region: global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 9f441508b745d22218316128572c9ec6aeb7207b
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilā darbvieta Kreditoru sadarbība Microsoft Dynamics 365 for Operations programmai

Izmantojot kreditoru sadarbības mobilo darbvietu, jūsu kreditori var uzzināt aktuālo informāciju par pirkšanas pasūtījumiem, kas viņiem ir nosūtīti apstiprināšanai, un apskatīt informāciju par jauniem un atjauninātiem pirkšanas pasūtījumiem un kontaktpersonām.

<a name="prerequisites"></a>Priekšnosacījumi
-------------

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Priekšnoteikumi</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lasīt par Microsoft Dynamics 365 for Operations mobilo platformu</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operations mobilā platforma</a></td>
</tr>
<tr class="even">
<td>Dynamics 365 for Operations</td>
<td>Pārliecinieties, ka izmantojat vidi, kurā ir instalēta Microsoft Dynamics 365 for Operations versija 1611 un Microsoft Dynamics for Operations 3. platformas atjauninājums (2016. gada novembra versija).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobilā ierīce, kurā ir instalēta Dynamics 365 for Operations programma</span></td>
<td><span style="color: #000000;">Lejupielādējiet Dynamics 365 for Operations programmu no mobilo programmu veikala.</span></td>
</tr>
<tr class="even">
<td>Labojumfails KB 3215650</td>
<td>Instalējiet labojumfailu, lai iespējotu sistēmā Dynamics 365 for Operations nodrošinātās darbvietas.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Labojumfails KB 3216943</span> </span></td>
<td>Instalējiet labojumfailu, lai iespējotu kreditoru sadarbības mobilo darbvietu.</td>
</tr>
<tr class="even">
<td>Kreditora lietotājam ir nepieciešama piekļuve kreditoru sadarbības tīmekļa interfeisam sistēmā Dynamics 365 for Operations un ir jāiestata kreditora sadarbības lietotājs.</td>
<td>Izpildiet nākamajās tēmās aprakstītās darbības, lai iestatītu kreditoru sadarbības tīmekļa interfeisu un strādātu ar to.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Lietot kreditoru sadarbību, lai strādātu ar ārējiem kreditoriem</a></li>
<li><a href="manage-vendor-collaboration-users.md">Pārvaldīt kreditoru sadarbības lietotājus</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Iestatīt un uzturēt kreditoru sadarbību</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Lietot kreditoru sadarbību, lai strādātu ar debitoriem sistēmā Dynamics 365 for Operations</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Pārskats
Mobilā darbvieta Kreditoru sadarbība kreditoriem pastāvīgi nodrošina informāciju par jaunajiem pirkšanas pasūtījumiem, lai viņi varētu redzēt pirkšanas pasūtījumus Dynamics 365 for Operations tīmekļa klientā un uz tiem reaģēt.  

**Piezīme.** Mobilajā darbvieta ir jālieto kā papildinājums kreditoru sadarbības tīmekļa interfeisam, nevis kā aizstājējs.  

Izmantojot mobilo darbvietu Kreditoru sadarbība, jūsu kreditori var apskatīt jaunus pirkšanas pasūtījumus, kas ir nosūtīti apstiprināšanai. Tajā tiek rādīta pirkšanas pasūtījuma informācija, piemēram, preces, daudzums un pieprasītie piegādes datumi. Informācija par cenu ir pieejama atkarībā no katra kreditora konfigurācijas.  

Kad lietotājs piesakās kā kreditors, šim lietotājam ir redzams, uz kuriem pirkšanas pasūtījumiem ir atbildēts vai kuriem pirkšanas pasūtījumiem joprojām tiek gaidīta debitora darbība. Kreditors var būt ieteicis citu piegādes datumu, par kuru ar debitoru vēl nav noslēgta vienošanās, tāpēc tiek gaidīta debitora darbība. Kreditoram ir redzams arī saraksts ar pirkšanas pasūtījumiem, kas ir apstiprināti, bet vēl nav piegādāti.  

Lai atbildētu uz pirkšanas pasūtījumu, kreditoram ir jālieto kreditoru sadarbības tīmekļa interfeiss, kas ir pieejams Dynamics 365 for Operations tīmekļa klientā. Šī ir arī tā vieta, kur kreditors saņem papildinformāciju par pasūtījumu, piemēram, dokumentu pielikumus, piegādes adresi katrai rindai, kā arī ar kreditoru saistītās izmaksas.  

Izmantojot īpašu drošības lomu, kreditors var apskatīt, kuras kontaktpersonas ir reģistrētas kādam kreditora kontam. Izmantojot to pašu drošības lomu, kreditors var apskatīt statusu jebkuram iesniegtajam lietotāja pieprasījumam.  

Jaunu kontaktpersonu izveidošanai un jaunu lietotāju pieprasījumu iesniegšanai ir jāizmanto kreditoru sadarbības tīmekļa interfeiss, kas ir pieejams Dynamics 365 for Operations tīmekļa klientā.  

Izmantojot mobilo darbvietu, jums ir tālāk uzskaitītās iespējas.

-   Skatiet jaunus, kreditoram nosūtītus pārdošanas pasūtījumus.
-   Skatiet pārdošanas pasūtījumus, uz kuriem kreditors ir atbildējis un kuri gaida debitora darbību.
-   Skatiet pirkšanas pasūtījumus, kuru statuss ir Apstiprināts un kuri vēl nav saņemti pilnībā.
-   Skatiet šim kreditora kontam reģistrētas kontaktpersonas informāciju (ir nepieciešama papildu drošības loma).
-   Skatiet informāciju par kreditora iesniegtu lietotāja pieprasījumu un sekojiet līdzi tā statusam (ir nepieciešama papildu drošības loma).

## <a name="get-started"></a>Darba sākšana
Lai sāktu darbu mobilajā ierīcē, veiciet tālāk norādītās darbības.

1.  Savā mobilo programmu veikalā lejupielādējiet programmu Microsoft Dynamics 365 for Operations un instalējiet to.
2.  Palaidiet programmu savā mobilajā ierīcē.
3.  Ievadiet savu Dynamics 365 vietrādi URL.
4.  Ievadiet uzņēmumu, kurā pierakstīties. Ievadiet, piemēram, **USMF**.
5.  Pirmajā pierakstīšanās reizē ir jāievada Microsoft Dynamics 365 for Operations konta lietotājvārds un parole. 

Pēc pieteikšanās programmā nav redzama neviena darbvieta. Lai darbvietas skatītu savā mobilajā programmā, jums šīs nepieciešamās darbvietas vispirms ir jāpublicē Dynamics 365 for Operations programmā. Lai darbvietu publicētu, jums ir nepieciešama sistēmas administrēšanas atļauja.

1.  Palaidiet Dynamics 365 for Operations.
2.  Dodieties uz **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **Sistēmas parametri**.
3.  Atlasiet vienumu **Pārvaldīt mobilo programmu**.
4.  Atlasiet darbvietu **Kreditoru sadarbība**, ko publicēt mobilajā platformā.
5.  Atlasiet vienumu **Publicēt darbvietu**.
6.  Atsvaidziniet ierīci, lai redzētu publicētās darbvietas.
7.  Atlasiet darbvietu **Kreditoru sadarbība**. Tiek atvērta tālāk redzamā lapa.

[![vendor-collaboration-mobile-app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktpersonas
Lapā **Kontaktpersonas** varat redzēt visas kontaktpersonas, kas ir iestatītas attiecīgajam kreditora kontam. Tajā tiek rādīts kontaktpersonas vārds, primārais e-pasts un lietotāja aizstājvārds, ja pieejams. Tur tiek arī rādīts, vai kontaktpersonas lietotāja konts ir aktīvs. Kad atlasāt kādu kontaktpersonu, ir redzama informācija par šo kontaktpersonu, piemēram, ar kurām juridiskajām personām šai personai ir kontakti, kā arī kontaktinformācija, piemēram, tālruņa numurs vai cita e-pasta adrese.

## <a name="user-requests"></a>Lietotāja pieprasījumi
Lapā **Lietotāju pieprasījumi** varat redzēt lietotāju pieprasījumus, kas ir iesniegti, izmantojot kreditoru sadarbības tīmekļa interfeisu, kā arī varat sekot to statusam. Ja atlasāt kādu lietotāja pieprasījumu, varat redzēt, kas tika pieprasīts, pievienot vai deaktivizēt lietotāju, mainīt drošību un redzēt, kuras drošības lomas šim lietotājam tika pieprasītas.

## <a name="purchase-orders-ready-for-review"></a>Pārskatīšanai gatavie pirkšanas pasūtījumi
Lapā **Pārskatīšanai gatavie pirkšanas pasūtījumi** varat redzēt visus debitora sūtītos un vēl neatbildētos pirkšanas pasūtījumus. Varat apskatīt atlasītu informāciju par pasūtījumu, piemēram, kuras preces ir pieprasītas un kad tās ir jāpiegādā. Informācija par cenu ir pieejama tikai tad, ja kreditoram tā ir konfigurēta.  

Varat redzēt, vai pirkšanas pasūtījumam ir kādas piezīmes vai pielikumi. Lai atvērtu pielikumus, ir jālieto kreditoru sadarbība tīmekļa klientā. Atlasiet vienumu **Pirkšanas pasūtījuma rinda**, lai redzētu visas rindas ar informāciju. Ievērojiet, ka katrai rindai indikators norāda, vai pastāv piezīmes vai pielikumi un vai pastāv piegādes adrese, kas atšķiras no virsrakstā rādītās.  

Lai atbildētu uz pirkšanas pasūtījumu, jums ir jālieto kreditoru sadarbības tīmekļa klients.

## <a name="awaiting-customer-action"></a>Tiek gaidīta debitora darbība
Lapā **Tiek gaidīta debitora darbība** varat atrast pirkšanas pasūtījumus, uz kuriem esat atbildējuši jūs vai kāds cits jūsu uzņēmumā, kuram ir piekļuve kreditoru darbībai. Pirkšanas pasūtījumi šajā sarakstā ir redzami tikai tad, ja debitoram šajā pirkšanas pasūtījumā ir jāizpilda viena vai vairākas no tālāk norādītajām darbībām.

-   Ja pirkšanas pasūtījums tika noraidīts, debitoram būtu jāatjaunina nosūtītais pasūtījums un jāsūta vēlreiz vai jāatceļ šis pasūtījums un jānosūta atkārtoti. Kad pirkšanas pasūtījums ir nosūtīts vēlreiz, tas pazūd no lapas **Tiek gaidīta debitora darbība**.
-   Ja pirkšanas pasūtījums tika apstiprināts ar izmaiņām, tad debitoram būtu jāatjaunina sākotnējais pasūtījums un jāsūta atkārtoti pārskatīšanai, vai tas jāatjaunina saskaņā ar izmaiņām un nekavējoties jāapstiprina. Abos gadījumos pirkšanas pasūtījums pazūd no lapas **Tiek gaidīta debitora darbība**.
-   Ja pirkšanas pasūtījums tika pieņemts un kļūst redzams lapā **Tiek gaidīta debitora darbība**, tad tas notiek tādēļ, ka pieņemšanas laikā šis pirkšanas pasūtījums netika apstiprināts automātiski. Tiek gaidīts, līdz pirkšanas aģents šī pasūtījuma statusu nomaina uz Akceptēts. Parasti pirkšanas pasūtījums tiktu ģenerēts kā līgums starp debitoru un kreditoru, līdzko kreditors pieņem pasūtījumu. Pirkšanas pasūtījuma pārvietošana uz statusu Apstiprināts būtu formalitāte.

Atlasot pirkšanas pasūtījumu, par atbildi tiek parādīta papildu informācija. Varat redzēt rindas informāciju un atbildi par katru rindu. Rindas statuss norāda, kura no tālāk uzskaitītajām atbildēm tika sniegta.

-   Pieņemts
-   Noraidījis
-   Apstiprināts ar izmaiņām
-   Aizstāts/Aizstājējs
-   Sadalīts grafikā/Grafika rinda

Ievērojiet, ka indikators rāda **Tiek piegādāts**=jā/nē, un tas tiek izmantots, lai norādītu, ka rindas netiks piegādātas. Iemesls varētu būt tāds, ka šī rinda tika noraidīta, vai arī iesniegta tur, kur sākotnējas rindas nav paredzēts piegādāt, vai tā ir rinda, kas ir sadalīta vairākās grafika rindās un kuras sākotnējo rindu nav paredzēts piegādāt, kā tas ir pieprasīts saņemtajā pasūtījumā.  

Tiek rādītas visas pasūtījuma rindas atbildē veiktās izmaiņas, izņemot augšupielādētās piezīmes un pielikumus, kurus varat apskatīt, izmantojot kreditoru sadarbības tīmekļa interfeisu.

## <a name="open-confirmed-orders"></a>Atvērtie apstiprinātie pasūtījumi
Kad debitors apstiprina pirkšanas pasūtījumu — tas nozīmē, ka pirkšanas pasūtījuma statuss mainās uz Apstiprināts —, tas tiek parādīts atvērto apstiprināto pasūtījumu sarakstā. Tas šajā sarakstā paliek, līdz debitors to reģistrē kā saņemtu.


