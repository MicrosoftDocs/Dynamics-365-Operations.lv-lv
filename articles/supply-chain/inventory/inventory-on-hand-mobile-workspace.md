---
title: Mobilā darbvieta Rīcībā esošie krājumi
description: Šajā tēmā ir sniegta informācija par mobilo darbvietu Rīcībā esošie krājumi. Šī darbvieta palīdz mobilajā ierīcē gūt ieskatu par rezervēto un pieejamo krājumu daudzumu jebkurā vietā un laikā.
author: yufeihuang
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yufeihuang
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9e67e16acc8ed72d571e9010131723038c8586a9
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573901"
---
# <a name="inventory-on-hand-mobile-workspace"></a>Mobilā darbvieta Rīcībā esošie krājumi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegta informācija par mobilo darbvietu **Rīcībā esošie krājumi**. Šī darbvieta jums palīdz jebkurā vietā un laikā gūt ieskatu par rezervēto un pieejamo krājumu daudzumu.

Šī mobilā darbvieta ir paredzēta lietošanai kopā ar mobilo programmu Finance and Operations.

## <a name="overview"></a>Pārskats
Parasti uzņēmumos katru dienu tiek veiktas vairākas krājumu nosūtīšanas un saņemšanas darbības. Šīs krājumu kustības dēļ nepārtraukti mainās rīcībā esošo krājumu statuss. Mobilā darbvieta **Rīcībā esošie krājumi** sniedz iespēju skatīt starpuzņēmumu rīcībā esošo krājumu statusu, lai varētu gūt visjaunākos ieskatus par krājumu datiem jebkurā mobilajā ierīcē. Neatkarīgi no tā, vai strādājat noliktavā vai iepirkumu, pārdošanas, ražošanas vai vadības nodaļā vai ieņemat citu amatu, varat piekļūt rīcībā esošo krājumu datiem jebkurā laikā un vietā. 

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
Priekšnosacījumi atšķiras, pamatojoties uz jūsu organizācijai izvietoto Supply Chain Management versiju.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Priekšnosacījumi, ja izmantojat Supply Chain Management
Ja jūsu organizācijai ir izvietota Supply Chain Management programmatūra, sistēmas administratoram ir jāpublicē mobilā darbvieta **Rīcībā esošie krājumi**. Norādījumus skatiet tēmā [Mobilās darbvietas publicēšana](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-platform-update-3-or-later"></a>Priekšnosacījumi, ja izmantojat platformas 3. atjauninājumu vai jaunāku versiju 
Ja jūsu organizācijai ir izvietots 3. platformas atjauninājums vai jaunāka tā versija, sistēmas administratoram ir jāizpilda tālāk norādītie priekšnoteikumi. 

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

<td>KB 4013633 ir X++ atjauninājums jeb metadatu labojumfails, kurā ir ietverta mobilā darbvieta <strong>Rīcībā esošie krājumi</strong>. Lai ieviestu KB 4013633, jūsu sistēmas administratoram ir jāizpilda tālāk minētās darbības.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Lejupielādējiet metadatu labojumfailu no portāla Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instalējiet metadatu labojumfailu</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Izveidojiet izvietojamu pakotni,</a> kas ietver modeli <strong>SCMMobile</strong>, un pēc tam augšupielādējiet izvietojamo pakotni pakalpojumā LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Lietojiet izvietojamo pakotni</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publicējiet mobilo darbvietu <strong>Rīcībā esošie krājumi</strong>.</td>
<td>Sistēmas administrators</td>
<td>Skatiet tēmu <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobilās darbvietas publicēšana</a>.</td>
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

    [![Velciet, lai atsvaidzinātu.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>Skatīt preces rīcībā esošos krājumus, izmantojot mobilo darbvietu Rīcībā esošie krājumi

1.  Mobilajā ierīcē atlasiet darbvietu **Rīcībā esošie krājumi**.

2.  Atlasiet vienumu **Pārbaudīt preces rīcībā esošos krājumus**. Tiek parādīts to preču saraksts, kas ir ielādētas programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču izstrādātājs šo skaitu var mainīt. Plašāku informāciju izstrādātājiem ir jāskata rakstā [Mobilā platforma](../../fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Ja jūsu krājuma sarakstā nav, atlasiet vienumu **Meklēt vēl**. Meklējiet pēc preces numura vai pārslēdziet uz meklēšanu pēc preces nosaukuma.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]