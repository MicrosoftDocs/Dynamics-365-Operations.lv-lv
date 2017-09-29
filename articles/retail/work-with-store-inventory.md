---
title: "Veikala krājumu pārvaldība"
description: "Šajā rakstā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 42091a5ec94bae3015fd9afca3ddcf1ef24f6eb4
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

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




