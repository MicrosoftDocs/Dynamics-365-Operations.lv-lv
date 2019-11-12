---
title: Procesa veidnes izveidošana programmā Attract
description: Šajā tēmā ir sniegta inf. par to, kā izveidot procesa veidni programmā Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 533b9abd3d57c5bf8f3d9da85020c86012436f2f
ms.sourcegitcommit: dd991154231280aff9c9c5799e42799e2bfc02fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622722"
---
# <a name="create-a-process-template-in-attract"></a>Procesa veidnes izveidošana programmā Attract

[!include [banner](includes/banner.md)]

*Darbā pieņemšanas procesa veidnē* ir visas aktivitātes, kas ir jāietver kādas vakances darbā pieņemšanas procesā. Šajā tēmā ir aprakstīti procesa veidnes elementi programmā Microsoft Dynamics 365 Talent: Attract. Tajā ir arī paskaidrots, kā izveidot veidni.

> [!NOTE]
> Veidnes izveidošana veido daļu no visaptverošās darbā pieņemšanas pievienojumprogrammas programmai Attract.

## <a name="template-management"></a>Veidņu pārvaldība

Organizācijas var izlemt, vai procesu veidnes programmā Attract var izveidot darba grupas dalībnieki vai tikai administratori. Lai konfigurētu veidņu pārvaldību, dodieties uz **Administrēšanas centrs** \> **Veidņu pārvaldība**. Lai ļautu darba grupas dalībniekiem veidot pašiem savas veidnes, ieslēdziet veidņu pārvaldību. Ja neieslēdzat veidņu pārvaldību, veidnes var izveidot tikai administratori.

## <a name="default-template"></a>Noklusējuma veidne

Noklusējuma veidni var iestatīt tikai administratori. Noklusējuma veidne tiek lietota, ja darba veidošanas laikā nav atlasīta neviena veidne. Lai iestatītu noklusējuma veidni, dodieties uz **Administrēšanas centrs** \> **Veidņu pārvaldība**. Veidnei, kuru vēlaties izmantot kā noklusējuma veidni, veidnes kartītē atlasiet daudzpunktes pogu (**...**) un pēc tam atlasiet **Iestatīt kā noklusējumu**.

## <a name="create-a-process-template"></a>Procesa veidnes izveidošana

Procesu veidnes var izveidot administratori, personāla atlases darbinieki un par pieņemšanu darbā atbildīgie vadītāji. Procesa veidni veido *posmi* un *aktivitātes*. Posmos tiek grupētas viena vai vairākas aktivitātes. Pēc noklusējuma ikvienai procesa veidnei ir aktivitātes Potenciālais klients, Pieteikums un Piedāvājums. Posmus, kuros ir šīs aktivitātes, var pārdēvēt. Varat pievienot papildu posmus, atlasot **+ Jauns posms**. Aktivitātes posmam varat pievienot, tās velkot uz atbilstošo posmu vai veicot dubultklikšķi uz attiecīgajām aktivitātēm aktivitāšu sarakstā.

> [!NOTE]
> Posmu nosaukumi kandidātiem ir redzami lapā **Pieteikuma statuss**. Šo faktu jums vajadzētu ņemt vērā, kad izvēlaties posmu nosaukumus.

Plašāku informāciju par aktivitātēm skatiet šeit: [Darbā pieņemšanas procesa aktivitātes pakalpojumā Attract](./activities-attract.md).

Lai izveidotu darbā pieņemšanas procesa veidni, izpildiet tālāk aprakstītos norādījumus.

1. Dodieties uz **Veidnes**.
2. Atlasiet **Jauns**.
3. Laukā **Veidnes nosaukums** ievadiet nosaukumu šai veidnei un pēc tam atlasiet **Izveidot**.
4. Sarakstā **Izvēlēties apstiprināšanas procesu** atlasiet **Noklusējums**, lai darbam pieprasītu apstiprinājumu.
5. Atlasiet iespējot vai atspējot potenciālos darba ņēmējus.
6. Neobligāti: pievienojiet vai noņemiet posmus.

    - Lai pievienotu posmu, atlasiet **+ jauns posms**.
    - Lai noņemtu kādu posmu, virziet peles rādītāju pār attiecīgo posmu un pēc tam atlasiet parādīto atkritnes pogu.

        > [!NOTE]
        > Posmus Potenciālais klients, Pieteikums un Piedāvājums nevar noņemt, bet tos var pārdēvēt.

7. Neobligāti: pievienojiet vai noņemiet aktivitātes.

    - Lai pievienotu kādu aktivitāti, no aktivitāšu saraksta labajā pusē velciet to uz atbilstošo posmu. Vai arī veiciet dubultklikšķi uz aktivitātes un pēc tam atlasiet posmu, kuram to pievienot.
    - Lai noņemtu kādu aktivitāti, izvērsiet to un pēc tam atlasiet atkritnes pogu šīs aktivitātes galvenē.

8. Atlasiet **Saglabāt**.
