---
title: Deleģēt darba vienumus darbplūsmā
description: Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
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
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509457"
---
# <a name="delegate-work-items-in-a-workflow"></a>Darba vienumu deleģēšana darbplūsmā

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a>Manuāla darba vienības deleģēšana

Lai deleģētu atsevišķu darba vienību, atlasiet opciju **Deleģēt** izvēlnē **Darbplūsma** un pēc tam ievadiet deleģējamo lietotāju kopā ar komentāru. Tādējādi darba vienība tiek atkārtoti piešķirta konkrētajam lietotājam, lai šis lietotājs varētu to pabeigt.

## <a name="automatically-delegate-work-items"></a>Automātiska darba vienību deleģēšana

Ja plānojat atrasties ārpus biroja vai noteiktu laika periodu nevarēsiet rīkoties ar darba vienībām citu iemeslu dēļ, varat automātiski deleģēt jaunas darba vienības citiem lietotājiem, izmantojot lapu **Lietotāja opcijas**.

### <a name="set-up-automatic-delegation"></a>Iestatīt automātisku deleģēšanu
1. Dodieties uz Vispārīgi > Iestatīšana > Lietotāja opcijas.
2. Noklikšķiniet uz cilnes Darbplūsma.
    * Pārliecinieties, ka sadaļa Deleģēšana ir izvērsta.    Lai sistēmu konfigurētu automātiskai jūsu darba vienumu deleģēšanai citiem lietotājiem, ir jāizveido deleģēšanas kārtulas, kuras norāda, kad tiek deleģēti noteikta tipa darba vienumi. Lai izveidotu deleģēšanas kārtulu, izpildiet tālāk aprakstītās darbības.  
3. Noklikšķiniet uz Pievienot.
4. Laukā Tvērums atlasiet kādu opciju.
    * Viss — deleģēt visus jums piešķirtos uzdevumus vai darba vienumus.    Modulis — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmas tipu. Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsmas tips.    Darbplūsma — deleģēt tikai tos darba vienumus, kas ir saistīti ar kādu konkrētu darbplūsmu. Ja atlasāt šo opciju, tad laukā Nosaukums ir jāatlasa darbplūsma.  
5. Laukā Deleģēt atlasiet lietotāju, kam deleģēt darba vienumus.
    * Izmantojiet laukus Sākuma datums/laiks un Beigu datums/laiks, lai norādītu, kad vēlaties automātiski deleģēt darba vienumus.  
6. Laukā Sākuma datums/laiks ievadiet datumu un laiku.
7. Laukā Beigu datums/laiks ievadiet datumu un laiku.
8. Atzīmējiet izvēles rūtiņu Iespējots, lai aktivizētu deleģēšanas kārtulu.
    * Ja vienumam Tvērums atlasāt vērtību Modulis, tad laukā Nosaukums ir jāatlasa šis modulis.    Ja vienumam Tvērums atlasāt vērtību Darbplūsma, tad laukā Nosaukums ir jāatlasa konkrētā deleģējamā darbplūsma.  
9. Laukā Komentārs ievadiet komentāru, kurā ir paskaidrots, kāpēc deleģējat šos darba vienumus.

