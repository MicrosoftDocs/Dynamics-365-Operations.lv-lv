---
title: Slēgta jautājuma izveide
description: Slēgto jautājumu atbildēm varat norādīt opcijas, no kurām respondents var izvēlēties.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e4f9697fc00798d917db6f7f50d7e3b8739233
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "858656"
---
# <a name="create-a-closed-ended-question"></a>Slēgta jautājuma izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Slēgto jautājumu atbildēm varat norādīt opcijas, no kurām respondents var izvēlēties. Pirmkārt, nepieciešams izveidot atbilžu grupu ar atbildēm, tad jāizveido jautājums, kas izmantos šo atbilžu grupu. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-an-answer-group"></a>Atbilžu grupas izveide
1. Dodieties uz Anketa > Dizains > Atbilžu grupas.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Atbilžu grupa.
4. Apraksta laukā ierakstiet vērtību.
    * Izmantojiet funkcionalitāti Kārtot nejaušā secībā, lai nejauši izvietotu atbildes citā secībā katru reizi, kad atbilžu grupa tiek izmantota jautājumam.  
5. Noklikšķiniet uz Atbilde.
6. Noklikšķiniet uz Jauns.
    * Sērijas numurs kontrolē secību, kādā tiek parādītas atbildes, ja vien atbilžu grupai nav atzīmēta funkcionalitāte Kārtot nejaušā secībā.  
    * Atbildēm var piešķirt punktus, kuri tiek izmantoti anketas vērtēšanā.  
7. Ievadiet skaitli laukā Punkti.
    * Pareizo atbildi var iezīmēt, lai norādītu, ka atlasītā atbilde ir pareiza. To var izmantot anketas punktu skaitīšanai.  
8. Ierakstiet vērtību laukā Atbilde.
    * Turpiniet veidot atbilžu grupas atbilžu atlases opcijas.  
9. Noklikšķiniet uz Jauns.
10. Ievadiet skaitli laukā Punkti.
11. Ierakstiet vērtību laukā Atbilde.
12. Klikšķiniet Jauns.
13. Ievadiet skaitli laukā Punkti.
14. Ierakstiet vērtību laukā Atbilde.
15. Klikšķiniet Jauns.
16. Ievadiet skaitli laukā Punkti.
17. Ierakstiet vērtību laukā Atbilde.
18. Klikšķiniet Jauns.
19. Ievadiet skaitli laukā Punkti.
20. Ierakstiet vērtību laukā Atbilde.
21. Aizvērt lapu.
22. Aizvērt lapu.

## <a name="create-the-question"></a>Jautājuma izveide
1. Pārejiet uz sadaļu Anketa> Dizains > Jautājumi.
2. Noklikšķiniet uz Jauns.
3. Izmantojiet lauku Tips, lai sagrupētu saistītus jautājumus.
    * Slēgtiem jautājumiem varat izmantot tādus ievades tipus kā izvēles rūtiņa, alternatīvā poga vai kombinētais lodziņš.  
4. Atlasiet opciju laukā Ievades tips.
5. Laukā Atbilžu grupa ievadiet vai atlasiet kādu vērtību.
6. Ierakstiet vērtību laukā Teksts.

