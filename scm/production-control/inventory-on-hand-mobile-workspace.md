---
title: "Mobilā darbvieta Rīcībā esošie krājumi Microsoft Dynamics 365 for Operations programmai"
description: "Mobilā darbvieta Rīcībā esošie krājumi palīdz mobilajā ierīcē gūt ieskatu par rezervēto un pieejamo krājumu daudzumu jebkurā vietā un laikā."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 85058f55-e566-40e2-9234-42d3e4fe5ff6
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 2ad48765528e1d1c6e7c90417b54a248ec79f546
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilā darbvieta Rīcībā esošie krājumi Microsoft Dynamics 365 for Operations programmai

Mobilā darbvieta Rīcībā esošie krājumi palīdz mobilajā ierīcē gūt ieskatu par rezervēto un pieejamo krājumu daudzumu jebkurā vietā un laikā. 

<a name="prerequisites"></a>Priekšnosacījumi
-------------

| Priekšnoteikumi                                                         | apraksts                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lasīt par Microsoft Dynamics 365 for Operations mobilo platformu | [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dynamics 365 for Operations                                          | Vide, kurā ir instalēta Microsoft Dynamics 365 for Operations versija 1611 un Microsoft Dynamics for Operations 3. platformas atjauninājums (2016. gada novembra versija) |
| Labojumfails KB 3215650                                                    | Instalējiet labojumfailu, lai iespējotu programmatūrā Microsoft Dynamics 365 for Operations nodrošinātās darbvietas.                                       |
| Mobilā ierīce, kurā ir instalēta Dynamics 365 for Operations programma | Lejupielādējiet Dynamics 365 for Operations programmu no mobilo programmu veikala.                                                                           |

## <a name="introduction"></a>Ievads
Parasti uzņēmumos katru dienu tiek veiktas vairākas krājumu nosūtīšanas un saņemšanas darbības. Šīs krājumu kustības dēļ nepārtraukti mainās rīcībā esošo krājumu statuss. Mobilā darbvieta Rīcībā esošie krājumi sniedz iespēju skatīt starpuzņēmumu rīcībā esošo krājumu statusu, lai varētu gūt jaunākos ieskatus par krājumu datiem jebkurā mobilajā ierīcē. Neatkarīgi no tā, vai strādājat noliktavā vai iepirkumu, pārdošanas, ražošanas vai vadības nodaļā vai ieņemat citu amatu, varat piekļūt rīcībā esošo krājumu datiem jebkurā laikā un vietā. Mobilā darbvieta nodrošina tūlītēju informāciju par rīcībā esošo krājumu statusu dažādās vietās un sniedz iespēju skatīt rīcībā esošos krājumus dažādās vietās, pašreizējās materiālu rezervācijas un nerezervētos rīcībā esošos krājumus. Varat arī ievadīt krājumu numurus, lai izveidotu rīcībā esošo krājumu vaicājumu, un veikt rīcībā esošo krājumu preču vai variantu meklēšanu, izmantojot filtrus. Mobilā darbvieta nodrošina tālāk norādītos līdzekļus.

-   Varat meklēt pēc preces numura vai nosaukuma, lai atrastu preces, kuru rīcībā esošo krājumu statusu vēlaties skatīt.
-   Varat skatīt tālāk norādīto informāciju par atlasītajām precēm.
    -   Rīcībā esošie krājumi pēc vietas
    -   Rīcībā esošie krājumi pēc noliktavas
    -   Rīcībā esošie krājumi pēc atrašanās vietas
    -   Rīcībā esošie krājumi pēc partijas (precēm, kas tiek komplektētas partijās)
    -   Rīcībā esošie krājumi pēc krājumu statusa

<!-- -->

-   Preces rīcībā esošie krājumi tiek rādīti tālāk norādītajos veidos.
    -   Pēc fiziskajiem krājumiem (Šajā skatā tiek rādīts kopējais daudzums.)
    -   Pēc rezervētajiem fiziskajiem krājumiem (Šajā skatā tiek rādīts rezervētais daudzums.)
    -   Pēc pieejamajiem fiziskajiem krājumiem (Šajā skatā tiek rādīts pieejamais daudzums, kas nav rezervēts.)

## <a name="get-started"></a>Darba sākšana
Lai sāktu darbu mobilajā ierīcē, veiciet tālāk norādītās darbības.

1.  Mobilo programmu veikalā lejupielādējiet Microsoft Dynamics 365 for Operations programmu un instalējiet to.
2.  Palaidiet programmu savā mobilajā ierīcē.
3.  Ievadiet savu Dynamics 365 vietrādi URL.
4.  Ievadiet uzņēmumu, kurā pierakstīties. Ievadiet, piemēram, **USMF**.
5.  Pirmajā pierakstīšanās reizē ir jāievada Microsoft Dynamics 365 for Operations konta lietotājvārds un parole. Ievadiet savus akreditācijas datus. Pēc pierakstīšanās ir redzamas jūsu uzņēmumam pieejamās darbvietas.

Lai darbvietas skatītu savā mobilajā programmā, jums šīs nepieciešamās darbvietas vispirms ir jāpublicē Dynamics 365 for Operations programmā.

1.  Palaidiet Dynamics 365 for Operations.
2.  Dodieties uz **Sistēmas administrēšana** &gt; **Iestatīšana** &gt; **Sistēmas parametri**.
3.  Atlasiet vienumu **Pārvaldīt mobilo programmu**.
4.  Atlasiet darbvietu, kas ir jāpublicē mobilajā platformā.
5.  Atlasiet vienumu **Publicēt darbvietu**.
6.  Atsvaidziniet ierīci, lai redzētu publicētās darbvietas.

## <a name="view-the-onhand-inventory-for-a-product"></a>Preces rīcībā esošo krājumu skatīšana
1.  Mobilajā ierīcē atlasiet darbvietu **Rīcībā esošie krājumi**.
2.  Atlasiet vienumu **Pārbaudīt preces rīcībā esošos krājumus**. Tiek parādīts to preču saraksts, kas ir ielādētas programmā lietošanai bezsaistes režīmā. Pēc noklusējuma ir ielādētas 50 krājumu vienības, taču šo skaitu var mainīt. Papildinformāciju skatiet iepriekš izlasāmajā rokasgrāmatā.
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




