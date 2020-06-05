---
title: Starpuzņēmumu izdevumi
description: Nodarbinātais, kura darba devējs ir viena organizācijas juridiskā persona, varētu veikt darbu citā juridiskajā personā, kas ietilpst tajā pašā organizācijā. Šādā gadījumā varat izmantot starpuzņēmumu izdevumu līdzekli, lai šī nodarbinātā izdevumus piešķirtu tai juridiskajai personai, kurai darbs tika veikts.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390888"
---
# <a name="intercompany-expenses"></a>Starpuzņēmumu izdevumi

[!include [banner](../includes/banner.md)]

Nodarbinātais, kura darba devējs ir viena organizācijas juridiskā persona, varētu veikt darbu citā juridiskajā personā, kas ietilpst tajā pašā organizācijā. Šādā gadījumā varat izmantot starpuzņēmumu izdevumu līdzekli, lai šī nodarbinātā izdevumus piešķirtu tai juridiskajai personai, kurai darbs tika veikts. Juridiskā persona, kura ir nodarbinātā darba devējs, tiek dēvēta par patapināšanas juridisko personu. Juridiskā persona, kurai nodarbinātais izraisa izdevumus, tiek dēvēta par piesaistīšanas juridisko personu. 

Lai nodarbinātais varētu izveidot un iesniegt izdevumus par darbu, kurš tiek veikts citai juridiskajai personai, patapināšanas juridiskās personas lapā **Izdevumu pārvaldības parametri** atlasiet opciju **Atļaut starpuzņēmumu izdevumu rindas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Starpuzņēmumu izdevumu nodokļu grāmatošana

[!include [banner](../includes/banner.md)]

Ja izdevumu pārskatā vēlaties importa nodokļu grupas, kas saistītas ar patapināšanas (avota) juridisko personu, nevis piesaistīšanas (mērķa) juridisko personu, tas ir jākonfigurē Virsgrāmatas PVN iestatījumos. Kad Virsgrāmatas parametrs **Juridiskas personas starpuzņēmumu nodokļu grāmatošana** ir iestatīts uz **Avots** un **Piemērot PVN nodokļu sistēmas nosacījumus** ir iestatīts uz **Nē**, tiks izmantota patapināšanas juridiskās personas nodokļu kombinācija. Ja tas pats parametrs ir iestatīts uz **Mērķis**, tiks izmantota piesaistīšanas juridiskās personas nodokļu kombinācija. Juridiskajām personām Amerikas Savienotajās valstīs, parametram esot iestatītam uz **Avots**, lauks **Saņemtais PVN** ir jākonfigurē arī jaunā **Virsgrāmatas grāmatošanas grupas** lapā. Uzskaites programma izmantos informāciju no šī lauka ar nodokļiem saistītajos uzskaites ierakstos.   
Darbība ir saskaņota izdevumu rindām, kas grāmatotas ar vai bez projekta.  
