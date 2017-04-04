---
title: "Veikala krājumu pārvaldība"
description: "Šis raksts apraksta veidu dokumentu, ko var izmantot, lai pārvaldītu krājumus."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
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

Šis raksts apraksta veidu dokumentu, ko var izmantot, lai pārvaldītu krājumus.

Lai pārvaldītu savas organizācija krājumus, varat izmantot tālāk uzskaitītos dokumentu tipus.

## <a name="purchase-orders"></a>Pirkšanas pasūtījumi
Pirkšanas pasūtījumi tiek izveidoti galvenajā birojā. Ja mazumtirdzniecības noliktava ir iekļauta pirkšanas pasūtījuma virsrakstu, izmantojot mūsdienu POS (MPOS) vai mākonis POS Microsoft Dynamics 365 operācijām - mazumtirdzniecības kārtību var saņemt veikalā. Pēc tam, kad ievadīti daudzumiem, kas saņemti noliktavā, tās var saglabāt lokāli papildu modificēšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Galvenajā birojā, daudzumus, kas tika saņemtas noliktavā tiek parādīti programmā Dynamics 365 operācijām, **saņemt tagad** lauku pirkšanas pasūtījumā.
Pārsūtīšanas pasūtījumi
---------------

Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, no kura krājumus var sūtīt. Šajā gadījumā pārsūtīšanas pasūtījuma parādās veikalā kā izdošanas pieprasījumu MPOS vai POS mākonis. Pēc daudzumiem, kas ir pieprasītas ir jāpaņem, tie ir izdarījuši un galvenais birojs nosūtīja. Galvenajā birojā, daudzumus, kas tika izdots veikalā tiek parādīti programmā Dynamics 365 operācijām, **kuģis tagad** laukā pārvietošanas pasūtījumā. Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, uz kuru krājumus var sūtīt. Šajā gadījumā pārsūtīšanas pasūtījuma parādās veikalā kā saņēmēja pieprasījuma MPOS vai POS mākonis. Pēc tam, kad ievadīti daudzumiem, kas saņemti noliktavā, tās var saglabāt lokāli papildu modificēšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Galvenajā birojā, daudzumus, kas tika saņemtas noliktavā tiek parādīti programmā Dynamics 365 operācijām, **saņemt tagad** laukā pārvietošanas pasūtījumā.

## <a name="stock-counts"></a>Krājumu uzskaite
Krājumu uzskaites var būt plānotas vai neplānotas. Plānotas krājumu uzskaites tiek uzsāktas galvenajā birojā, kurš norāda uzskaitāmos krājumus. Galvenais birojs izveido inventarizācijas dokumentu, kas var saņemt pie veikala, kur faktiskā rīcībā esošo krājumu daudzumu tiek ievadīti MPOS vai POS mākonis. Neplānotas akciju skaits tiek uzsākti veikalā un reālo rīcībā esošo krājumu daudzumu tiek atjaunināta MPOS vai POS mākonis. Atšķirībā no plānoto akciju skaitu akciju neieplānotu skaitiem nav iepriekš definēto elementu sarakstu. Kad abu tipu krājumu uzskaite ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju. Galvenajā birojā uzskaite tiek pārbaudīta un iegrāmatota.




