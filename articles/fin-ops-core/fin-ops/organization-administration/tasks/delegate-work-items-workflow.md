---
title: Deleģēt darba vienumus darbplūsmā
description: Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem.
author: ChrisGarty
manager: AnnBe
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48d8fd06217d318fa8208e11ffa5624f6be25be1
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796710"
---
# <a name="delegate-work-items-in-a-workflow"></a>Darba vienumu deleģēšana darbplūsmā

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Manuāla darba vienības deleģēšana

Lai deleģētu atsevišķu darba vienību, atlasiet opciju **Deleģēt** izvēlnē **Darbplūsma** un pēc tam ievadiet deleģējamo lietotāju kopā ar komentāru. Tādējādi darba vienība tiek atkārtoti piešķirta konkrētajam lietotājam, lai šis lietotājs varētu to pabeigt.

## <a name="manually-delegate-multiple-work-items"></a>Manuāli deleģēt vairākus darba vienumus

Vairākus darba vienumus var deleģēt kopā no lapas **Man piešķirtie darba vienumi**. Masveida deleģēšanai ir piemēroti šādi darbplūsmas tipi: Pirkšanas līguma apstiprināšanas darbplūsma, Pirkšanas pasūtījumu darbplūsma, Pirkšanas pieprasījuma pārskats un Kreditora rēķina darbplūsma. Līdzeklis **Deleģēt vairākus darba vienumus** ir atspējots pēc noklusējuma, un to var iespējot sadaļā **Darbvietas > Līdzekļu pārvaldība**. Sazinieties ar sistēmas administratoru, lai saņemtu palīdzību šī līdzekļa iespējošanā.
1.  Dodieties uz **Vispārīgi > Vispārīgi > Darba vienumi > Man piešķirtie darba vienumi**.
2.  Atlasiet darba vienumus, kas tiks deleģēti.
3.  Noklikšķiniet uz izvēlnes **Darba vienumu deleģēšana**.
4.  Laukā **Lietotājs** atlasiet lietotāju, kuram deleģēt darba vienumus.
5.  Laukā **Komentārs** ievadiet paskaidrojošu komentāru, kāpēc deleģējat šos darba vienumus.
6.  Noklikšķiniet uz pogas **Deleģēt darba vienumus**, lai pabeigtu darba vienuma deleģēšanu.

## <a name="automatically-delegate-work-items"></a>Automātiska darba vienību deleģēšana

Ja plānojat atrasties ārpus biroja vai noteiktu laika periodu nevarēsiet rīkoties ar darba vienībām citu iemeslu dēļ, varat automātiski deleģēt jaunas darba vienības citiem lietotājiem, izmantojot lapu **Lietotāja opcijas**.

### <a name="set-up-automatic-delegation"></a>Iestatīt automātisku deleģēšanu
1. Pārejiet uz sadaļu **Kopējs > Iestatīšana > Lietotāja opcijas**.
2. Noklikšķiniet uz cilnes **Darbplūsma**. Pārliecinieties, vai sadaļa Deleģēšana ir izvērsta. Lai sistēmu konfigurētu automātiskai jūsu darba vienumu deleģēšanai citiem lietotājiem, ir jāizveido deleģēšanas kārtulas, kuras norāda, kad tiek deleģēti noteikta tipa darba vienumi. Lai izveidotu deleģēšanas kārtulu, izpildiet tālāk aprakstītās darbības.  
3. Noklikšķiniet uz **Pievienot**.
4. Laukā **Tvērums** atlasiet opciju:
    - Viss — deleģēt visus jums piešķirtos uzdevumus vai darba vienumus.
    - Modulis — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmas tipu. Ja atlasāt šo opciju, tad laukā **Nosaukums** ir jāatlasa darbplūsmas veids.
    - Darbplūsma — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmu. Ja atlasāt šo opciju, tad laukā **Nosaukums** ir jāatlasa darbplūsma.  
5. Laukā **Nosaukums**:
    - Tvērumam **Modulis** atlasiet mērķa moduli.
    - Tvērumam **Darbplūsma** atlasiet mērķa darbplūsmu.
6. Laukā **Pārstāvis** atlasiet lietotāju, kuram deleģēt darba vienumus. Izmantojiet laukus **Sākuma datums/laiks** un **Beigu datums/laiks**, lai norādītu, kad vēlaties automātiski deleģēt darba vienumus.  
7. Laukā **Sākuma datums/laiks** ievadiet datumu un laiku.
8. Laukā **Beigu datums/laiks** ievadiet datumu un laiku.
9. Atlasiet izvēles rūtiņu **Iespējots** deleģēšanas noteikumu aktivizēšanai. 
10. Laukā **Komentārs** ievadiet paskaidrojošu komentāru, kāpēc deleģējat šos darba vienumus.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]