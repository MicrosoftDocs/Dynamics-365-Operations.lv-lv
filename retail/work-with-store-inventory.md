---
title: "Veikala krājumu pārvaldība"
description: "Šajā rakstā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 1a5f2cd60e09b67cee4bab211bba4e07e9ef181f
ms.contentlocale: lv-lv
ms.lasthandoff: 06/20/2017


---

# <a name="manage-store-inventory"></a>Veikala krājumu pārvaldība

[!include[banner](includes/banner.md)]


Šajā rakstā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.

Lai pārvaldītu savas organizācija krājumus, varat izmantot tālāk uzskaitītos dokumentu tipus.

## <a name="purchase-orders"></a>Pirkšanas pasūtījumi
Pirkšanas pasūtījumi tiek izveidoti galvenajā birojā. Ja pirkšanas pasūtījuma virsrakstā ir iekļauta mazumtirdzniecības noliktava, pasūtījumu var saņemt veikalā, izmantojot programmu Modern POS (MPOS) vai Cloud POS programmatūrā Microsoft Dynamics 365 for Retail. Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Veikalā saņemtie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Retail pieejamā pirkšanas pasūtījuma laukā **Saņemt tūlīt**.

## <a name="transfer-orders"></a>Pārsūtīšanas pasūtījumi
Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, no kura krājumus var sūtīt. Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā izdošanas pieprasījums programmā MPOS vai Cloud POS. Pēc pieprasīto daudzumu izdošanas tie tiek fiksēti un nosūtīti uz centrālo biroju. Veikalā izdotie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Retail pieejamā pārsūtīšanas pasūtījuma laukā **Nosūtīt tūlīt**. Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, uz kuru krājumus var sūtīt. Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā saņemšanas pieprasījums programmā MPOS vai Cloud POS. Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Veikalā saņemtie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Retail pieejamā pārsūtīšanas pasūtījuma laukā **Saņemt tūlīt**.

## <a name="stock-counts"></a>Krājumu uzskaite
Krājumu uzskaites var būt plānotas vai neplānotas. Plānotas krājumu uzskaites tiek uzsāktas galvenajā birojā, kurš norāda uzskaitāmos krājumus. Galvenajā birojā tiek izveidots uzskaites dokuments, ko var saņemt veikalā, kurā faktisko rīcībā esošo krājumu daudzumi ir ievadīto programmā MPOS vai Cloud POS. Veikalā tiek sākta neplānota krājumu uzskaite, programmā MPOS vai Cloud POS tiek atjaunināti faktisko rīcībā esošo krājumu daudzumi. Atšķirībā no ieplānotās krājumu uzskaites neplānotajai krājumu uzskaitei netiek lietots iepriekš definēts krājumu saraksts. Kad abu tipu krājumu uzskaite ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju. Galvenajā birojā uzskaite tiek pārbaudīta un iegrāmatota.

## <a name="inventory-lookup"></a>Krājumu pārlūkošana
Pašreizējo rīcībā esošo preču daudzumu vairākiem veikaliem un noliktavām var skatīt lapā Krājumu uzmeklēšana. Papildus pašreizējam rīcībā esošajam daudzumam katram atsevišķajam veikalam var skatīt arī turpmākos solīšanai pieejamos (ATP) daudzumus. Lai to izdarītu, atlasiet veikalu, kuram vēlaties skatīt ATP, un pēc tam noklikšķiniet uz **Rādīt veikala pieejamību**.





