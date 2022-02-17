---
title: Jautājuma izveide, kas atkarīgs no iepriekšējā jautājuma atbildes
description: Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMCollection, KMCollectionQuestion, KMCollectionQuestionTree, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28f75a902121f23c92a919b539517dbdb191447
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066729"
---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Jautājuma izveide, kas atkarīgs no iepriekšējā jautājuma atbildes


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Nosacījuma jautājumi ļauj norādīt, kurš turpinājuma jautājums tiks attēlots respondentam, pamatojoties uz iepriekšējā jautājuma atbildes. Piemēram, ja jautājat "Jums labāk garšo kafija vai tēja?", loģisku turpinājuma jautājumu var noteikt atkarībā no tā, vai atbildētājs atbildē izvēlas kafiju vai tēju. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.


## <a name="find-the-existing-questionnaire"></a>Atrodiet pastāvošu anketu
1. Dodieties uz **QuestionnaireDesignQuestionnaires** > **·** > **·**.
2. Sarakstā atlasiet WorkFH anketa.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Pievienojiet anketai visus jautājumus un to pakārtotos jautājumus
1. Noklikšķiniet uz **Jautājumi**.
2. Klikšķiniet **Jauns**.
3. Laukā **Jautājums** atlasiet jautājuma numuru 00016.
4. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
5. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
6. Noklikšķiniet uz **Saglabāt**.
7. Aizvērt lapu.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>Iestatiet anketas secību par nosacītu un norādiet, ka jautājums ir atkarīgs no atbilstoša jautājuma
1. Noklikšķiniet uz **Rediģēt**.
2. Izvērsiet sadaļu **Iestatīšana**.
3. Laukā **Jautājumu pasūtījums** atlasiet "Nosacīts".
4. Noklikšķiniet uz **Nosacījuma** jautājums.
5. Koka struktūrā atlasiet "Jautājumi\Paskaidrojiet, kāpēc sniedzāt šādu atbildi uz iepriekšējo jautājumu?".
6. Laukā Primārais **jautājums** atlasiet jautājumu 00009.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Laukā **Atbilde** ievadiet atbildes opcijas atbilžu secības ID, no kuras vēlaties padarīt jautājumu atkarīgu. Piemēram, ievadiet 1, lai norādītu uz pirmo atbildes opciju.
9. Noklikšķiniet uz **Saglabāt**.
10. Koka struktūrā atlasiet "Jautājumi\Par padarīto darbu saņemu pienācīgu atalgojumu."
    * Ievērojiet, ka jautājumu koks tika atjaunināts, lai attēlotu sakarību.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
