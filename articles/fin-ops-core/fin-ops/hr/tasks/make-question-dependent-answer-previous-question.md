---
title: Jautājuma izveide, kas atkarīgs no iepriekšējā jautājuma atbildes
description: Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e49ee4dd1f2d4a5af3112d27eaf8d697904d2487
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178943"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Jautājuma izveide, kas atkarīgs no iepriekšējā jautājuma atbildes

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes. Piemēram, ja jautājat "Jums labāk garšo kafija vai tēja?", loģisku turpinājuma jautājumu var noteikt atkarībā no tā, vai atbildētājs atbildē izvēlas kafiju vai tēju. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="find-the-existing-questionnaire"></a>Atrodiet pastāvošu anketu
1. Pārejiet uz sadaļu Anketa > Dizains > Anketas.
2. Sarakstā atlasiet WorkFH anketa.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Pievienojiet anketai visus jautājumus un to pakārtotos jautājumus
1. Noklikšķiniet uz Jautājumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Jautājums atlasiet jautājumu ar numuru 00016.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Iestatiet anketas secību par nosacītu un norādiet, ka jautājums ir atkarīgs no atbilstoša jautājuma
1. Noklikšķiniet uz Rediģēt.
2. Izvērsiet sadaļu Iestatīšana.
3. Laukā Jautājumu secība atlasiet vērtību Nosacījuma.
4. Noklikšķiniet uz Nosacījuma jautājums.
5. Koka struktūrā atlasiet "Jautājumi\Paskaidrojiet, kāpēc sniedzāt šādu atbildi uz iepriekšējo jautājumu?".
6. Laukā Primārais jautājums atlasiet jautājumu ar numuru 00009
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā Atbilde ievadiet tās atbildes opcijas atbilžu sērijas ID, no kuras vēlaties padarīt atkarīgu šo jautājumu. Piemēram, ievadiet 1, lai norādītu uz pirmo atbildes opciju.
9. Klikšķiniet Saglabāt.
10. Koka struktūrā atlasiet "Jautājumi\Par padarīto darbu saņemu pienācīgu atalgojumu."
    * Ievērojiet, ka jautājumu koks tika atjaunināts, lai attēlotu sakarību.  
