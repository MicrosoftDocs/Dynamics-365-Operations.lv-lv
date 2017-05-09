---
title: "Veikala krājumu pārvaldība"
description: "Šajā rakstā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fbe9945799f1e65ed6ad624a3df270fa4eb72b88
ms.lasthandoff: 03/31/2017


---

# <a name="manage-store-inventory"></a>Veikala krājumu pārvaldība

[!include[banner](includes/banner.md)]


Šajā rakstā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.

Lai pārvaldītu savas organizācija krājumus, varat izmantot tālāk uzskaitītos dokumentu tipus.

## <a name="purchase-orders"></a>Pirkšanas pasūtījumi
Pirkšanas pasūtījumi tiek izveidoti galvenajā birojā. Ja pirkšanas pasūtījuma galvenā ir iekļauta mazumtirdzniecības noliktava, pasūtījumu var saņemt veikalā, izmantojot programmu Modern POS (MPOS) vai Cloud POS programmatūrā Microsoft Dynamics 365 for Operations — Retail. Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Veikalā saņemtie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Operations pieejamā pirkšanas pasūtījuma laukā **Saņemt tūlīt**.

## <a name="transfer-orders"></a>Pārsūtīšanas pasūtījumi
Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, no kura krājumus var sūtīt. Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā izdošanas pieprasījums programmā MPOS vai Cloud POS. Pēc pieprasīto daudzumu izdošanas tie tiek fiksēti un nosūtīti uz centrālo biroju. Veikalā izdotie daudzumi galvenajā birojā tiek rādīti programmatūrā Dynamics 365 for Operations pieejamā pārsūtīšanas pasūtījuma laukā** Nosūtīt tūlīt**. Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, uz kuru krājumus var sūtīt. Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā saņemšanas pieprasījums programmā MPOS vai Cloud POS. Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Veikalā saņemtie daudzumi centrālajā birojā tiek rādīti programmatūrā Dynamics 365 for Operations pieejamā pārsūtīšanas pasūtījuma laukā **Saņemt tūlīt**.

## <a name="stock-counts"></a>Krājumu uzskaite
Krājumu uzskaites var būt plānotas vai neplānotas. Plānotas krājumu uzskaites tiek uzsāktas galvenajā birojā, kurš norāda uzskaitāmos krājumus. Galvenajā birojā tiek izveidots uzskaites dokuments, ko var saņemt veikalā, kurā faktisko rīcībā esošo krājumu daudzumi ir ievadīto programmā MPOS vai Cloud POS. Veikalā tiek sākta neplānota krājumu uzskaite, programmā MPOS vai Cloud POS tiek atjaunināti faktisko rīcībā esošo krājumu daudzumi. Atšķirībā no ieplānotās krājumu uzskaites neplānotajai krājumu uzskaitei netiek lietots iepriekš definēts krājumu saraksts. Kad abu tipu krājumu uzskaite ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju. Galvenajā birojā uzskaite tiek pārbaudīta un iegrāmatota.






