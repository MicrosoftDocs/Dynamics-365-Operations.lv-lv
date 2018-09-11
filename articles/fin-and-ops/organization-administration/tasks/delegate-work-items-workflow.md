--- 
title: "Deleģēt darba vienumus darbplūsmā"
description: "Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem."
author: jasongre
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4765fec0cdce0e2f8859c979ff97d20aa6b20bfa
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a>Deleģēt darba vienumus darbplūsmā

[!include [task guide banner](../../includes/task-guide-banner.md)]

Ja plānojat kādu laiku neatrasties birojā vai citu iemeslu dēļ nespēt reaģēt uz darba vienumiem, tad darba vienumus varat deleģēt vai mainīt to piešķiri pret citiem lietotājiem. Šī procedūra jums palīdz konfigurēt sistēmu, lai savus darba vienumus automātiski deleģētu citam lietotājam.



Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="set-up-automatic-delegation"></a>Iestatīt automātisku deleģēšanu
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


