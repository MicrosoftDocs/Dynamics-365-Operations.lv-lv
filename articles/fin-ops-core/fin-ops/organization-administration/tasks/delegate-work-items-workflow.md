---
title: Deleģēt darba vienumus darbplūsmā
description: Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140586"
---
# <a name="delegate-work-items-in-a-workflow"></a>Darba vienumu deleģēšana darbplūsmā

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a>Manuāla darba vienības deleģēšana

Lai deleģētu atsevišķu darba vienību, atlasiet opciju **Deleģēt** izvēlnē **Darbplūsma** un pēc tam ievadiet deleģējamo lietotāju kopā ar komentāru. Tādējādi darba vienība tiek atkārtoti piešķirta konkrētajam lietotājam, lai šis lietotājs varētu to pabeigt.

## <a name="automatically-delegate-work-items"></a>Automātiska darba vienību deleģēšana

Ja plānojat atrasties ārpus biroja vai noteiktu laika periodu nevarēsiet rīkoties ar darba vienībām citu iemeslu dēļ, varat automātiski deleģēt jaunas darba vienības citiem lietotājiem, izmantojot lapu **Lietotāja opcijas**.

### <a name="set-up-automatic-delegation"></a>Iestatīt automātisku deleģēšanu
1. Pārejiet uz sadaļu **Kopējs > Iestatīšana > Lietotāja opcijas**.
2. Noklikšķiniet uz cilnes **Darbplūsma**. Pārliecinieties, vai sadaļa Deleģēšana ir izvērsta. Lai sistēmu konfigurētu automātiskai jūsu darba vienumu deleģēšanai citiem lietotājiem, ir jāizveido deleģēšanas kārtulas, kuras norāda, kad tiek deleģēti noteikta tipa darba vienumi. Lai izveidotu deleģēšanas kārtulu, izpildiet tālāk aprakstītās darbības.  
3. Noklikšķiniet uz **Pievienot**.
4. Atlasiet opciju laukā **Detalizācijas līmenis**.
    - Viss — deleģēt visus jums piešķirtos uzdevumus vai darba vienumus.
    - Modulis — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmas tipu. Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsmas tips.
    - Darbplūsma — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmu. Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsma.  
5. Laukā **Pārstāvis** atlasiet lietotāju, kuram deleģēt darba vienumus. Izmantojiet laukus Sākuma datums/laiks un Beigu datums/laiks, lai norādītu, kad vēlaties automātiski deleģēt darba vienumus.  
6. Laukā **Sākuma datums/laiks** ievadiet datumu un laiku.
7. Laukā **Beigu datums/laiks** ievadiet datumu un laiku.
8. Atlasiet izvēles rūtiņu **Iespējots** deleģēšanas noteikumu aktivizēšanai. Atlasot **Moduli** kā Tvērumu, tālāk jums ir jāatlasa modulis laukā Nosaukums. Atlasot **Darbplūsmu** kā Tvērumu, tālāk jums ir jāatlasa noteikta darbplūsma deleģēšanai laukā Nosaukums.  
9. Laukā **Komentārs** ievadiet paskaidrojošu komentāru, kāpēc deleģējat šos darba vienumus.

