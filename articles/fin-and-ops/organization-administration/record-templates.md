---
title: Ierakstu veidnes
description: "Šajā rakstā tiek iepazīstināts ar ierakstu veidņu koncepciju un paskaidrots, kā tās var izmantot, lai veidotu ierakstus, kuri koplieto informāciju."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ef5e95d9d6beed10cd6c80aa131c5cbef85c07a8
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="record-templates"></a>Ierakstu veidnes

[!include [banner](../includes/banner.md)]

Šajā rakstā tiek iepazīstināts ar ierakstu veidņu koncepciju un paskaidrots, kā tās var izmantot, lai veidotu ierakstus, kuri koplieto informāciju.

Ierakstu veidnes var palīdzēt ātrāk izveidot ierakstus programmatūrā Microsoft Dynamics 365 for Finance and Operations. Programmatūrā Microsoft Dynamics 365 for Finance and Operations var izveidot tikai dažu ierakstu tipu ierakstu veidnes.

Piemēram, iedomājieties, ka jūs ievadāt nomas informāciju par automašīnu nomas darījumu, kas atrodas San Francisko. Tā kā lielākā daļa klientu visdrīzāk ir no San Francisko apvidus, būtu jauki, ja jūs varētu automātiski aizpildīt nomas veidlapas lauku **Administratīvais apgabals**, **Valsts**, un **Pilsēta** vērtības.

> [!NOTE]
> Veidnes varat lietot tikai tādiem Finance and Operations apgabaliem, kuriem jums ir piekļuve. Tomēr ir redzami visi veidņu nosaukumi, kad izveidojat jaunu ierakstu, un tie ir redzami arī citiem lietotājiem, ja jūs izveidojat veidnes, kas būs pieejamas visiem lietotājiem. Paturiet to prātā, kad piešķirsiet veidnēm nosaukumus. Piemēram, centieties neizmantot nosaukumus, kuri satur tādus vārdus kā “komisija”, ja ne visiem lietotājiem būtu jāzina, ka dažiem uzņēmuma darbiniekiem algas ir balstītas uz komisiju.

Kad specifiskai formai pastāv viena vai vairākas veidnes, kam jums ir piekļuve, un jūs mēģināt izveidot jaunu ierakstu šajā formā, tiek parādīta lapa **Atlasiet veidni, kas paredzēta...**. Kad atlasāt veidni no saraksta, tiek izveidots jauns ieraksts, kas satur uz atlasīto veidni balstītu noklusējuma informāciju. Ja nevēlaties izmantot veidnes jaunu ierakstu izveidei, atzīmējiet izvēles rūtiņu **Nejautāt atkārtoti** lapā **Atlasiet veidni, kas paredzēta**. Lai atkal tiktu parādīts veidnes atlases dialoglodziņš, ar peles labo pogu noklikšķiniet uz jebkura ieraksta, noklikšķiniet uz **Informācija par ierakstu** un pēc tam noklikšķiniet uz **Parādīt veidnes atlasi**.

