---
title: "Mobilā darbvieta Pārdošanas pasūtījumi programmai Microsoft Dynamics 365 for Operations"
description: "Izmantojot mobilo darbvietu Pārdošanas pasūtījumi, varat sekot līdzi pārdošanas pasūtījumiem jebkurā vietā un laikā."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Mobilā darbvieta Pārdošanas pasūtījumi programmai Microsoft Dynamics 365 for Operations

Izmantojot mobilo darbvietu Pārdošanas pasūtījumi, varat sekot līdzi pārdošanas pasūtījumiem jebkurā vietā un laikā. 

<a name="prerequisites"></a>Priekšnosacījumi
-------------

| Priekšnoteikumi                                                         | apraksts                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lasīt par Microsoft Dynamics 365 for Operations mobilo platformu | [Dynamics 365 for Operations mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Pārliecinieties, ka izmantojat vidi, kurā ir instalēta Microsoft Dynamics 365 for Operations versija 1611 un Microsoft Dynamics for Operations 3. platformas atjauninājums (2016. gada novembra laidiens). |
| Labojumfails KB 3215650                                                    | Instalējiet labojumfailu, lai iespējotu programmatūrā Microsoft Dynamics 365 for Operations nodrošinātās darbvietas.                                                                       |
| Mobilā ierīce, kurā ir instalēta Dynamics 365 for Operations programma | Lejupielādējiet Dynamics 365 for Operations programmu no mobilo programmu veikala.                                                                                                      |

## <a name="overview"></a>Pārskats
Šī mobilā darbvieta piekļūst lietojumprogrammai Dynamics 365 for Operations un sniedz iespēju skatīt detalizētu informāciju par katru pārdošanas pasūtījumu, piemēram, pasūtījuma statusu, debitora kontaktinformāciju un pasūtījuma saņēmēja kontaktinformāciju. Mobilā darbvieta sniedz iespēju nekavējoties skatīt pārdošanas pasūtījumus. Varat skatīt pārdošanas pasūtījumus pēc debitora, skatīt visus pārdošanas pasūtījumus vai skatīt informāciju par noteiktu pārdošanas pasūtījumu. Mobilā darbvieta nodrošina divus skatus, kas palīdz detalizēti analizēt pārdošanas pasūtījumus.

### <a name="view-all-sales-orders"></a>Skatīt visus pārdošanas pasūtījumus

Šajā skatā tiek rādīti visi pārdošanas pasūtījumi.

-   Izmantojiet kādu no tālāk norādītajiem filtriem, lai atlasītu pārdošanas pasūtījumus, ko vēlaties skatīt.
    -   Meklēt pēc pārdošanas pasūtījuma
    -   Meklēt pēc debitora konta
    -   Meklēt pēc debitora nosaukuma
    -   Meklēt pēc statusa
    -   Meklēt pēc nodošanas izpildei statusa
    -   Meklēt pēc izveides datuma un laika

<!-- -->

-   Pēc pārdošanas pasūtījumu atlases varat skatīt detalizētu informāciju par noteiktiem pasūtījumiem. Varat skatīt tālāk norādīto informāciju.
    -   Debitora nosaukuma un adreses informācija
    -   Dažādi pārdošanas pasūtījuma datumi, piemēram, pieprasītais nosūtīšanas datums un apstiprinātais nosūtīšanas datums
    -   Pasūtījuma saņēmēja kontaktinformācija
    -   Debitora kontaktinformācija
    -   Pasūtījuma rindas
    -   Sūtījumi, kas norāda kā un kad pārdošanas pasūtījums ir nosūtīts

### <a name="view-orders-for-a-customer-"></a>Skatīt noteikta debitora pasūtījumus** **

Šajā skatā tiek rādīti pārdošanas pasūtījumi pēc debitora.

-   Izmantojiet kādu no tālāk norādītajiem filtriem, lai skatītu noteikta debitora pārdošanas pasūtījumus.
    -   Meklēt pēc nosaukuma
    -   Meklēt pēc konta

<!-- -->

-   Pēc debitora atlases varat skatīt tālāk norādīto informāciju.
    -   Debitora nosaukums un grupa
    -   Debitora kontaktinformācija
    -   Debitora pārdošanas pasūtījumi un detalizēta informācija par pārdošanas pasūtījumiem
        -   Debitora nosaukuma un adreses informācija
        -   Dažādi pārdošanas pasūtījuma datumi
        -   Pasūtījuma saņēmēja kontaktinformācija
        -   Debitora kontaktinformācija
        -   Pasūtījuma rindas
        -   Sūtījumi, kas norāda kā un kad pārdošanas pasūtījumi ir nosūtīti

## <a name="get-started"></a>Darba sākšana
Lai savā mobilajā ierīcē sāktu lietot mobilo darbvietu Pārdošanas pasūtījumi, veiciet tālāk norādītās darbības.

1.  Savā mobilo programmu veikalā lejupielādējiet programmu Microsoft Dynamics 365 for Operations un instalējiet to.
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

## <a name="view-information-about-sales-orders-for-a-customer"></a>Informācijas par noteikta debitora pārdošanas pasūtījumiem skatīšana
1.  Mobilajā ierīcē atlasiet darbvietu **Pārdošanas pasūtījumi**.
2.  Atlasiet vienumu **Skatīt noteikta debitora pasūtījumus**.
3.  Izmatojiet informāciju laukos **Konts **vai **Debitora nosaukums**, lai atrastu vajadzīgo debitoru.
4.  Atlasiet debitoru.
5.  Atlasiet vienumu **Kontaktinformācija** vai **Pārdošanas pasūtījumi**.
6.  Ja atlasāt vienumu **Pārdošanas pasūtījumi**, tiek parādīts konkrētā debitora pārdošanas pasūtījumu saraksts.
7.  Atlasiet vienumu **Pārdošanas pasūtījums**.
8.  Šajā sadaļā varat skatīt informāciju par pārdošanas pasūtījuma rindām, sūtīšanām, debitora kontaktinformāciju un pasūtījuma saņēmēja kontaktinformāciju.




