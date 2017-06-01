---
title: "Mobilā darbvieta Rīcībā esošie krājumi"
description: "Šajā tēmā ir sniegta informācija par mobilo darbvietu Rīcībā esošie krājumi, kas ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šī darbvieta palīdz mobilajā ierīcē gūt ieskatu par rezervēto un pieejamo krājumu daudzumu jebkurā vietā un laikā."
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
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7387df37e047d5ab7a90b696a6ffa249094499c4
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Mobilā darbvieta Rīcībā esošie krājumi

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegta informācija par mobilo darbvietu Rīcībā esošie krājumi, kas ir pieejama Microsoft Dynamics 365 for Operations mobilajā programmā. Šī darbvieta palīdz mobilajā ierīcē gūt ieskatu par rezervēto un pieejamo krājumu daudzumu jebkurā vietā un laikā.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Pārskats par mobilo darbvietu Rīcībā esošie krājumi
--------------------------------------------------

Parasti uzņēmumos katru dienu tiek veiktas vairākas krājumu nosūtīšanas un saņemšanas darbības. Šīs krājumu kustības dēļ nepārtraukti mainās rīcībā esošo krājumu statuss. Mobilā darbvieta **Rīcībā esošie krājumi** sniedz iespēju skatīt starpuzņēmumu rīcībā esošo krājumu statusu, lai varētu gūt jaunākos ieskatus par krājumu datiem jebkurā mobilajā ierīcē. Neatkarīgi no tā, vai strādājat noliktavā vai iepirkumu, pārdošanas, ražošanas vai vadības nodaļā vai ieņemat citu amatu, varat piekļūt rīcībā esošo krājumu datiem jebkurā laikā un vietā. 

Mobilā darbvieta nodrošina tūlītēju informāciju par rīcībā esošo krājumu statusu dažādās vietās. Tā arī sniedz iespēju skatīt rīcībā esošos krājumus dažādās vietās, pašreizējās materiālu rezervācijas un nerezervētos rīcībā esošos krājumus. Varat arī ievadīt krājumu numurus, lai izveidotu rīcībā esošo krājumu vaicājumu, un veikt rīcībā esošo krājumu preču vai variantu meklēšanu, izmantojot filtrus. 

Mobilā darbvieta nodrošina tālāk norādītos līdzekļus.

-   Varat meklēt pēc preces numura vai nosaukuma, lai atrastu preces, kuru rīcībā esošo krājumu statusu vēlaties skatīt.

-   Varat skatīt tālāk norādīto informāciju par atlasītajām precēm.
    -   Rīcībā esošie krājumi pēc vietas
    -   Rīcībā esošie krājumi pēc noliktavas
    -   Rīcībā esošie krājumi pēc atrašanās vietas
    -   Rīcībā esošie krājumi pēc partijas (precēm, kas tiek komplektētas partijās)
    -   Rīcībā esošie krājumi pēc krājumu statusa
    
-   Preces rīcībā esošie krājumi tiek rādīti tālāk norādītajos veidos.
    -   Pēc fiziskajiem krājumiem (Šajā skatā tiek rādīts kopējais daudzums.)
    -   Pēc rezervētajiem fiziskajiem krājumiem (Šajā skatā tiek rādīts rezervētais daudzums.)
    -   Pēc pieejamajiem fiziskajiem krājumiem (Šajā skatā tiek rādīts pieejamais daudzums, kas nav rezervēts.)

## <a name="prerequisites"></a>Priekšnosacījumi
Lai varētu izmantot mobilo darbvietu **Rīcībā esošie krājumi**, pārliecinieties, vai sistēmas administrators ir izpildījis tālāk minētos priekšnosacījumus.

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
<td>Jābūt ieviestai Microsoft Dynamics 365 for Operation versijai 1611 ar 3. vai jaunāku platformas atjauninājumu.</td>
<td>Sistēmas administrators</td>
<td>Ja programma Dynamics 365 for Operations vēl nav izvietota jūsu organizācijā, sistēmas administratoram vajadzētu izlasīt rakstu <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations izvietošana demonstrācijas vidē</a>.</td>
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
<td>Mobilā darbvieta <strong>Rīcībā esošie krājumi</strong> ir jāpublicē Dynamics 365 for Operations mobilajā programmā.</td>
<td>Sistēmas administrators</td>
<td><ol>
<li>Palaidiet pārlūkprogrammā programmu Dynamics 365 for Operations.</li>
<li>Lapā <strong>Sistēmas parametri</strong> atlasiet <strong>Mobilo darbvietu pārvaldība</strong>.</li>
<li>Atlasiet darbvietu <strong>Rīcībā esošie krājumi</strong>.</li>
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

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>Preces rīcībā esošo krājumu skatīšana, izmantojot mobilo darbvietu Rīcībā esošie krājumi
1.  Mobilajā ierīcē atlasiet darbvietu **Rīcībā esošie krājumi**.
2.  Atlasiet vienumu **Pārbaudīt preces rīcībā esošos krājumus**. Tiek parādīts to preču saraksts, kas ir ielādētas programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju izstrādātāji var skatīt rakstā [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
3.  Ja vajadzīgais krājums nav ietverts sarakstā, atlasiet vienumu **Meklēt vairāk**, lai veiktu tiešsaistes meklēšanu programmatūrā Dynamics 365 for Operations. Meklējiet pēc preces numura vai pārslēdziet uz meklēšanu pēc preces nosaukuma.
4.  Atlasiet preci. Ja krājumam ir attēls, tas tiek parādīts.
5.  Atlasiet vienu no tālāk norādītājām opcijām, lai skatītu rīcībā esošo krājumu statusu.
    -   Skatīt rīcībā esošos krājumus pēc vietas
    -   Skatīt rīcībā esošos krājumus pēc noliktavas
    -   Skatīt rīcībā esošos krājumus pēc atrašanās vietas
    -   Skatīt rīcībā esošos krājumus pēc partijas (precēm, kas tiek komplektētas partijās)
    -   Skatīt rīcībā esošos krājumus pēc krājumu statusa

    Preces rīcībā esošie krājumi tiek rādīti tālāk norādītajos veidos.
    -   Pēc fiziskajiem krājumiem (Šajā skatā tiek rādīts kopējais daudzums.)
    -   Pēc rezervētajiem fiziskajiem krājumiem (Šajā skatā tiek rādīts rezervētais daudzums.)
    -   Pēc pieejamajiem fiziskajiem krājumiem (Šajā skatā tiek rādīts pieejamais daudzums, kas nav rezervēts.)






