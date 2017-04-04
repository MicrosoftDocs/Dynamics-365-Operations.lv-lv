---
title: "Piegādātāja sadarbības mobilo darbvietu Microsoft Dynamics 365 app darbības"
description: "Ar piegādātāja sadarbības mobilo darbvietu jūsu kreditoriem var sekot visam jaunākajam, iepirkuma pasūtījumos, kuri nosūtīti apstiprināšanai, kā _ arī skatīt informāciju par jaunu un atjauninātu pirkšanas pasūtījumus un kontaktus."
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

# <a name="vendor-collaboration-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Piegādātāja sadarbības mobilo darbvietu Microsoft Dynamics 365 app darbības

Ar piegādātāja sadarbības mobilo darbvietu jūsu kreditoriem var sekot visam jaunākajam, iepirkuma pasūtījumos, kuri nosūtīti apstiprināšanai, kā _ arī skatīt informāciju par jaunu un atjauninātu pirkšanas pasūtījumus un kontaktus.

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
<td>Lasiet par Microsoft Dynamics 365 operācijas mobilā platforma</td>
<td><a href="/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dinamika 365 operācijas mobilā platforma</a></td>
</tr>
<tr class="even">
<td>Dinamika 365 operācijām</td>
<td>Pārliecinieties, ka jūs izmantojat vidē, kas ir Microsoft Dynamics 365 darbību versija 1611 un Microsoft Dynamics darbības platformu atjaunināt 3 (2016. gada novembrī).</td>
</tr>
<tr class="odd">
<td><span style="color: #000000;">Mobilā ierīce, kurā ir dinamika 365 operācijas app uzstādīta</span></td>
<td><span style="color: #000000;">Lejupielādējiet Dynamics 365 operācijas app no mobilo app store.</span></td>
</tr>
<tr class="even">
<td>Labojumfailu KB 3215650</td>
<td>Jāinstalē labojumfails, lai iespējotu darbvietu, ar kurām tiek sniegti Dynamics 365 operācijām.</td>
</tr>
<tr class="odd">
<td><span style="color: #ff0000;"><span style="color: #000000;">Labojumfailu KB 3216943</span> </span></td>
<td>Jāinstalē labojumfails, lai piegādātāja sadarbības mobilo darbvietu.</td>
</tr>
<tr class="even">
<td>Kreditoru lietotājam piekļūt piegādātāja sadarbības web interfeiss programmā Dynamics 365 operācijām un piegādātāju sadarbības lietotāja iestatīšana.</td>
<td>Izpildiet darbības, kas aprakstītas šādas tēmas iestatīt un strādāt ar piegādātāja sadarbības web interfeisu.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Piegādātāja sadarbības izmantošana, lai strādātu ar ārējiem kreditoriem</a></li>
<li><a href="manage-vendor-collaboration-users.md">Pārvaldīt kreditoru sadarbības lietotājus</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Iestatīt un uzturēt kreditoru sadarbību</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Piegādātāja sadarbības izmantošana, lai strādātu ar klientu operācijām Dynamics 365</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="overview"></a>Pārskats
Piegādātāja sadarbības mobilo darbvietu pasargā kreditorus informē par jaunajiem pirkšanas pasūtījumiem, tāpēc, ka viņi var skatīt un atbildēt uz pirkšanas pasūtījumu programmā Dynamics 365 operācijas web klienta.  

**Piezīme:** mobilo darbvietu, ir jāizmanto kā piegādātāja sadarbības web interfeisu, bet ne Nomaiņa Pielikums.  

Ar piegādātāja sadarbības mobilo darbvietu jūsu kreditoriem var apskatīt jaunajiem pirkšanas pasūtījumiem, kas nosūtīti apstiprināšanai. To rāda pirkšanas pasūtījuma informāciju, piemēram, produktu daudzumu un pieprasīto piegādes datumu. Cenu ir pieejama informācija, atkarībā no konfigurācijas katram kreditoram.  

Kad lietotājs piesakās kā pārdevēja, viņi redzēs, kuros pirkšanas pasūtījumi ir atsaukušās uz vai kuros pirkšanas pasūtījumi joprojām gaida klientu rīcību. Piegādātājam ir teikuši citu piegādes datumu, kas nav vēl vienojas ar klientu, tāpēc iepirkuma pasūtījumā gaida klientu rīcību. Pirkšanas pasūtījumus, kas ir apstiprināts, bet vēl nav piegādātus sarakstu var apskatīt arī kreditoru.  

Lai atbildētu uz pirkšanas pasūtījumu, piegādātājam ir izmantot kreditoru sadarbības web interfeisu, kas ir pieejams Dynamics 365 operācijas web klienta. Tas ir arī, kur pārdevējs saņems plašāku informāciju par pasūtījumu, piem., dokumenta pielikumu, piegādes adresi katrā rindā un izmaksas, kas saistītas ar kreditoru.  

Ar īpaša drošības loma, kreditors var apskatīt kura kontaktpersona kreditora kontam, kas ir reģistrētas personas. Ar vienu un to pašu drošības lomu, kreditors var skatīt lietotāja pieprasījuma, kas iesniegts statusu.  

Piegādātāja sadarbības interfeisu, kas ir pieejami programmā Dynamics 365 operācijas web klienta jāveic veido jaunus kontaktus un iesniedz jaunu lietotāju pieprasījumus.  

Ar mobilo darbvietu jūsu kreditors var:

-   Apskatiet jaunajiem pirkšanas pasūtījumiem, kas nosūtīti piegādātājam.
-   Skatīt pirkšanas pasūtījumus, ka kreditors ir reaģējusi uz un gaida klientu rīcību.
-   Skatīt pirkšanas pasūtījumus, kas ir apstiprināts valsts un nav saņemta pilnībā.
-   Skatīt kontaktpersonas informācija, kas reģistrēta kreditora kontam (nepieciešams papildu drošības loma).
-   Skatīt informāciju un sekojiet lietotāja iesniegto pieprasījumu piegādātājam (nepieciešams papildu drošības lomas) statusu.

## <a name="get-started"></a>Darba sākšana
Lai sāktu jūsu mobilajā ierīcē:

1.  Mobilo app Store, lejupielādējiet un instalējiet Microsoft Dynamics 365 operācijas app.
2.  Savā ierīcē palaidiet app.
3.  Ievadiet savu dinamiku 365 URL.
4.  Ievadiet uzņēmuma pieteikties. Piemēram, ievadiet **USMF**.
5.  Pirmo reizi piesakoties, jums tiek lūgts ievadīt lietotājvārdu un paroli par jūsu Microsoft Dynamics 365 operāciju kontam. 

Pēc pieteikšanās app, neviena darbvieta ir redzamas. Lai skatītu darbvietu mobilo app, vispirms jāpublicē vajadzīgo darbvietu Dynamics 365 operācijas app. Jums nepieciešams sistēmas administrācijas atļauju publicēt darbvietu.

1.  Dynamics 365 sākt operāciju.
2.  Dodieties uz **sistēmas administrēšanu**&gt;**Setup**&gt;**sistēmas parametru**.
3.  Atlasiet **Manage mobilo app**.
4.  Atlasīt darbvietas **piegādātāja sadarbības** publicēt mobilā platforma.
5.  Atlasiet **publicēt darbvietu**.
6.  Atsvaidzinātu ierīces redzēt publicēto darbvietām.
7.  Atlasiet **piegādātāja sadarbības** darbvietu. Jūs nākošajā lappusē.

[![piegādātāja sadarbības mobile app](./media/vendor-collaboration-mobile-app.png)](./media/vendor-collaboration-mobile-app.png)

## <a name="contacts"></a>Kontaktpersonas
**Kontaktus** lapa ļauj skatīt visus kontaktus, kuriem uzstādītas kreditora kontam. Tas parāda kontaktpersonas nosaukums, primāro e-pasta un lietotājiem aizstājvārds, ja pieejams. Tas arī parāda, vai kontaktpersonas lietotāja konts ir aktīvs. Atlasot kontaktpersonas, redzat kontaktinformāciju, piemēram, kuras juridiskās persona ir kontaktpersona, un kontaktinformācija, piem., tālruņa numuru vai citu e-pasta adresi.

## <a name="user-requests"></a>Lietotāja pieprasījumi
**Lietotāju pieprasījumus** lapa ļauj skatīt visus lietotājs pieprasa, ka jums ir iesniegts, izmantojot piegādātāja sadarbības web interfeisu un sekot statusu. Atlasot lietotāju pieprasījumu, var redzēt, kāda tika pieprasīta, pievienot vai inaktivētu lietotājs, mainīt drošības un redzētu, kura drošības lomas tika pieprasīti lietotājam.

## <a name="purchase-orders-ready-for-review"></a>Pirkšanas pasūtījumus, kas ir gatavi izskatīšanai
**Pirkšanas pasūtījumus, kas ir gatavs pārskatīšanai** lapa ļauj skatīt visus pirkšanas pasūtījumus, kas nosūtīti klientam un netiek atbildēts. Var apskatīt izvēlēto informāciju par pasūtījumu, piemēram, kuri produkti ir uzdots, un kad piegādās. Informācija par cenām ir pieejama tikai tad, ja tas ir konfigurēta šim piegādātājam.  

Jūs varat redzēt, vai iepirkuma pasūtījumā ir piezīmes vai pielikumus. Atvērt pielikumus, jums vajadzēs izmantot piegādātāju sadarbības web klientā. Atlasiet **pirkšanas pasūtījuma rindu,**, lai redzētu visas rindas ar detaļām. Ņemiet vērā, ka katrai rindai indikators parādīs vai ir piezīmes vai pielikumus vai ja ir piegādes adrese, kas ir savādāki nekā to, kāda informācija tiek rādīta virsraksta.  

Lai atbildētu uz pirkšanas pasūtījumu, jāizmanto piegādātāja sadarbības web klientā.

## <a name="awaiting-customer-action"></a>Tiek gaidīta debitora darbība
**Gaida klientu rīcības** lapa ļauj jums atrast pirkšanas pasūtījumus, kas jūs vai kāds jūsu uzņēmumā, kurš ir arī piekļuvi kreditora sadarbība ir atsaukušās uz. Pirkšanas pasūtījumi ir redzams šajā sarakstā, ja klientam ir nepieciešams veikt kādu no šīm darbībām pirkšanas pasūtījumā.

-   Ja pirkšanas pasūtījums tika noraidīta, klientam būtu vai nu nepieciešamību atjaunināt nosūtīto pasūtījumu un nosūtīt vēlreiz, vai atcelt pasūtījumu un atkārtoti. Kad pirkšanas pasūtījums tiek nosūtīta vēlreiz, tas pazudīs no **gaida klientu rīcības** lapā.
-   Ja pirkšanas pasūtījums tika pieņemtas izmaiņas, klientam būtu nepieciešams atjaunināt sākotnējo secību un nosūtīt pārskatīšanai, vai atjauninātu saskaņā ar izmaiņām un nekavējoties to apstiprinātu. Abos gadījumos pirkšanas pasūtījuma pazudīs no **gaida klientu rīcības** lapā.
-   Ja pirkšanas pasūtījums tika pieņemts un parādās **gaida klientu rīcības** lapu, tas ir tāpēc, ka iepirkuma pasūtījumā nav automātiski apstiprināts, kad pieņemšanu tika darīts. Tā gaida iepirkumu aģents, lai mainītu secību uz apstiprināts. Parasti, pirkšanas pasūtījums tiks uzskatīta vienošanās starp klientu un piegādātāju kā kreditors pieņem pasūtījumu. Pārvietojot pirkšanas pasūtījums apstiprināts valsts būtu formalitāte.

Atlasot Pirkšanas pasūtījums, papildu detaļas parādās par atbildi. Var redzēt rindas detaļu un atbildi katrā rindiņā. Rindas statuss rāda, kurš no tālāk aprakstītajām atbildēm ir dota.

-   Pieņemts
-   Noraidījis
-   Apstiprināts ar izmaiņām
-   Aizstāt Aizvietotājs
-   Sadalīt grafiku/grafika rindas

Ņemiet vērā, ka indikators rāda **nogādāšana**= Jā/Nē, kas tiek izmantota, lai norādītu, ka rindas netiks piegādāts. Tas varētu būt, jo rinda tika noraidīts aizstāt vai ja sākotnējais rindiņas nav paredzams piegādāt vai rindu, kas ir sadalīts vairākās grafika rindas un sākotnējās rindas nav paredzams piegādāt pieprasīto saņemtajām pasūtījumu.  

Pasūtījuma rindas atbildi veiktās izmaiņas atainojas izņemot augšupielādēto piezīmēm un pielikumiem, kuru var apskatīt, izmantojot piegādātāja sadarbības web interfeisu.

## <a name="open-confirmed-orders"></a>Apstiprināto atvērtiem pasūtījumiem
Kad pirkšanas pasūtījums ir apstiprināts klients, kas nozīmē, ka pirkšanas pasūtījums tiek mainīts uz apstiprinātā valsts tā parādīsies apstiprināja atvērtās pasūtījuma. Līdz brīdim, kad tas ir reģistrēts kā klients saņem, tā paliks sarakstā.


