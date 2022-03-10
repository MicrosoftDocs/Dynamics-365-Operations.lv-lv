---
title: Aptauju sadalīšana, izmantojot plānošanu
description: Izmantojot anketēšanas plānošanu, var plānot un sadalīt anketas vairākiem respondentiem.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4885c11f0cb508edb8ebf3aef14748e819113264
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067406"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Aptauju sadalīšana, izmantojot plānošanu


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Izmantojot anketēšanas plānošanu, var plānot un sadalīt anketas vairākiem respondentiem. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.

## <a name="create-a-questionnaire-schedule"></a>Izveidot anketas grafiku

1. Iet uz **Anketa** > **Izplatīt** > **Anketu grafiki**.

2. Klikšķiniet **Jauns**.

3. Iekš **Plānošana** laukā ierakstiet vērtību.

4. Laukā **Apraksts** ierakstiet kādu vērtību.
    * Iestatiet grafiku uz **Anonīms** ja atbildes būtu jāreģistrē bez nosaukumiem, kas saistīti ar atbildi.  
    * Lai iespējotu anonīmus rezultātus, vispirms ir jāiestata personāla vadības parametrus.  

5. Iekš **Tips** laukā atlasiet plānošanas veidu.  Šajā piemērā mēs izmantosim **Apmierinātība** veids.

6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

8. Laukā **Datums** ievadiet datumu.

9. Paplašiniet **E-pasts darbinieku pašapkalpošanās dienestam** sadaļā.

10. Laukā **Temats** ievadiet vērtību.

    * Piemērs: Anketa pieejama  

11. Iekš **Teksts** laukā ierakstiet e-pasta ziņojuma pamattekstu. Ņemiet vērā, ka mainīgais var tikt izmantots, lai aizstātu vērtības sistēmā.

    * Piemērs: Cien. %P%! Lūdzu, piesakieties darbinieku pašapkalpes pakalpojumā, lai aizpildītu darbaspēka veselības novērtējuma anketu.  Contoso  

12. Noklikšķiniet uz **Saglabāt**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Izmantojiet detalizētu informācija par Iestatīšanu, lai atlasītu anketu(as), kura(s) jāatbild, kā arī vaicājumus, kas ir jāizmanto respondentu atlasei.

1. Klikšķis **Iestatīšanas informācija**.

2. Sarakstā atlasiet vaicājumu, ko izmantot, lai veiktu anketas respondentu meklēšanu sistēmā.

    * Piemērs: Darbinieki  

3. Klikšķis **Skatiet vai mainiet vaicājumu** lai atlasītu konkrētas personas vai pielāgotu vaicājumu, lai atrastu cilvēkus, kas atbilst noteiktiem kritērijiem.

    * Ņemiet vērā, ka visiem respondentiem ir jābūt arī sistēmas lietotājiem.  

4. Sarakstā atzīmējiet rindu Personai.

5. Ievadiet vai atlasiet vērtību laukā **Kritēriji**.

    * Atlasiet Jūlija Funderburka  

6. Sarakstā atlasiet Jūlija Funderburka

7. Noklikšķiniet uz **Labi**.

8. Noklikšķiniet uz **Anketas** cilne.

9. Kokā izvērsiet anketas veida mezglu **Apmierinātības aptauja**.

10. Kokā pārbaudiet 'Darbaspēka veselības novērtējums'.

11. Noklikšķiniet uz **Labi**.

12. Klikšķis **Plānotā atbilžu sesija**.

    * Pieraksti to **Plānotās atbilžu sesijas** ir izveidoti katram atlasītajam/vaicātajam lietotājam.  

13. Aizvērt lapu.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Sāciet anketēšanas grafiku, lai respondents var piekļūt anketai un to aizpildīt.

1. Noklikšķiniet uz **Funkcijas**.

2. Noklikšķiniet uz **Sākt**.

3. Noklikšķiniet uz **Labi**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Nosūtiet e-pasta ziņojumu, lai informētu respondentus par pieejamo anketu.

1. Noklikšķiniet uz **Funkcijas**.

2. Klikšķis **Sūtīt e-pastu**.

3. Noklikšķiniet uz **Atcelt**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Izmantojiet plānotās atbilžu sesijas, lai pārraudzītu, kam ir jāaizpilda anketa.

1. Klikšķis **Plānotā atbilžu sesija**.

    * Dzēsiet visas atlikušās plānotās atbilžu sesijas, kad viss ir sagatavots plānotās sesijas pabeigšanai.  

2. Noklikšķiniet uz **Dzēst**.

3. Noklikšķiniet uz pogas **Jā**.

4. Aizvērt lapu.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Kad visi respondenti ir aizpildījuši anketu, varat plānošanu beigt, un/vai visas atlikušās plānotās atbilžu sesijas ir dzēstas.

1. Noklikšķiniet uz **Funkcijas**.
2. Klikšķis **Beigas**.
3. Noklikšķiniet uz **Labi**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
