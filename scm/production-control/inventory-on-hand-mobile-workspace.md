---
title: "Krājuma rīcībā esošo mobilo darbvietu Microsoft Dynamics 365 app darbības"
description: "Rīcībā esošo krājumu mobilo darbvietu palīdz jums iegūt mobilā ieskatu rezervēta un pieejamo krājumu jebkurā laikā un jebkurā vietā."
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

# <a name="inventory-on-hand-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Krājuma rīcībā esošo mobilo darbvietu Microsoft Dynamics 365 app darbības

Rīcībā esošo krājumu mobilo darbvietu palīdz jums iegūt mobilā ieskatu rezervēta un pieejamo krājumu jebkurā laikā un jebkurā vietā. 

<a name="prerequisites"></a>Priekšnosacījumi
-------------

| Priekšnoteikumi                                                         | apraksts                                                                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Lasiet par Microsoft Dynamics 365 operācijas mobilā platforma | [Dinamika 365 operācijas mobilā platforma](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                   |
| Dinamika 365 operācijām                                          | Vidi, kas ir Microsoft Dynamics 365 darbību versija 1611 un Microsoft Dynamics darbības platformu update 3 (2016. gada novembrī) |
| Labojumfailu KB 3215650                                                    | Jāinstalē labojumfails, lai iespējotu darbvietu, ar kurām ir norādītas jūsu Microsoft Dynamics 365 operācijām.                                       |
| Mobilā ierīce, kurā ir dinamika 365 operācijas app uzstādīta | Lejupielādējiet Dynamics 365 operācijas app no mobilo app store.                                                                           |

## <a name="introduction"></a>Ievads
Parasti uzņēmumi ir vairākiem sūtījumiem un vairākas noliktavas saņemšanas katru dienu. Rīcībā esošo krājumu statusu mainīt pastāvīgi šīm kustībām. Krājuma rīcībā esošo mobilo darbvietu var apskatīt visuzņēmuma rīcībā esošo krājumu stāvokli, tāpēc, ka jūs varat iegūt jaunākos ieskatu inventarizācijas datu izvēle jūsu mobilajā ierīcē. Neatkarīgi no tā, vai darbs noliktavu, pirkšanas, pārdošanas, ražošanas vai pārvaldības vai citām lomām, rīcībā esošo krājumu datiem varat piekļūt jebkurā brīdī un jebkur. Mobilo darbvietu nodrošina tērzēšanas skats statusa rīcībā visā iekārtas un ļauj apskatīt rīcībā esošo krājumu, iekārtas, gan pašreizējo materiālu rezervāciju un tiešs rīcībā esošos krājumus. Var ievadīt preču numurus vaicājuma rīcībā esošos krājumus un filtrētu meklēšanas rīcībā esošo produktu vai varianti. Konkrētāk, mobilā darbvieta nodrošina šos līdzekļus:

-   Jūs varat meklēt pēc produkta numuru vai produkta nosaukumu, lai atrastu produktu apskatīt rīcībā esošo krājumu statuss.
-   Izvēlēto produktu, var apskatīt šādu informāciju:
    -   Rīcībā esošie krājumi uz vienu vietu
    -   Rīcībā esošo krājumu noliktavas
    -   Rīcībā esošos krājumus pēc novietojuma
    -   Rīcībā esošie krājumi uz partiju (par partijas kontrolē produkti)
    -   Rīcībā esošie krājumi uz vienu krājumu statuss

<!-- -->

-   Produkts ir rīcībā esošie krājumi tiek parādīts šādi:
    -   Pēc inventarizācijas (Šis skatījums parāda kopējo summu).
    -   Ar fiziski rezervētā (šo viedokli pārstāv rezervēto summu).
    -   Pēc pieejamo fizisko (šo skatu attēlo pieejamā summa, kas nav atrunu.)

## <a name="get-started"></a>Darba sākšana
Lai sāktu jūsu mobilajā ierīcē:

1.  No mobilo app store, lejupielādējiet un instalējiet Microsoft Dynamics 365 operācijas app.
2.  Savā ierīcē palaidiet app.
3.  Ievadiet savu dinamiku 365 URL.
4.  Ievadiet uzņēmuma pieteikties. Piemēram, ievadiet **USMF**.
5.  Pirmo reizi piesakoties, jums tiek lūgts ievadīt lietotājvārdu un paroli par jūsu Microsoft Dynamics 365 operāciju kontam. Ievadiet savus akreditācijas datus. Pēc tam, kad jūs piesakāties sistēmā, jūs redzēt pieejams darbvietā savam uzņēmumam.

Lai skatītu darbvietu mobilo app, vispirms jāpublicē vajadzīgo darbvietu Dynamics 365 operācijas app.

1.  Dynamics 365 sākt operāciju.
2.  Dodieties uz **sistēmas administrēšanu**&gt;**Setup**&gt;**sistēmas parametru**.
3.  Atlasiet **Manage mobilo app**.
4.  Atlasīt darbvietas publicēt mobilā platforma.
5.  Atlasiet **publicēt darbvietu**.
6.  Atsvaidzinātu ierīces redzēt publicēto darbvietām.

## <a name="view-the-onhand-inventory-for-a-product"></a>Skatiet produkta krājumu onhand
1.  Mobilajā ierīcē, atlasiet **rīcībā esošo krājumu** darbvietu.
2.  Atlasiet **pārbaudiet rīcībā esošo krājumu**. Tiek parādīts saraksts ar tādiem produktiem, kuri tiek ielādēta jūsu app lietošanai bezsaistē. Pēc noklusējuma 50 preces iekrauj, bet šo numuru var mainīt. Lai iegūtu papildinformāciju, skatiet iepriekš lasīt rokasgrāmatu.
3.  Ja sarakstā nav vienumu, atlasiet **meklēt vairāk** darīt tiešsaistes meklēšanas programmā Dynamics 365 operācijām. Meklēt pēc produkta numuru, vai pāriet uz meklēšanu pēc produkta nosaukuma.
4.  Atlasiet preci. Ja precei ir attēlu, attēls tiek parādīts.
5.  Atlasiet vienu no šīm opcijām, lai apskatīt rīcībā esošo krājumu statusu:
    -   Skatīt rīcībā esošo katrā vietnē
    -   Skatīt rīcībā esošo noliktavu
    -   Skatīt rīcībā esošo katrā vietā
    -   Skatīt rīcībā esošo katras partijas (par partijas kontrolē produkti)
    -   Skatīt rīcībā uz vienu krājumu statuss

    Produkts ir rīcībā esošie krājumi tiek parādīts šādi:
    -   Pēc inventarizācijas (Šis skatījums parāda kopējo summu).
    -   Ar fiziski rezervētā (šo viedokli pārstāv rezervēto summu).
    -   Pēc pieejamo fizisko (šo viedokli pārstāv pieejamā summa, kas nav atrunu).




