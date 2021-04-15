---
title: Aptauju sadalīšana, izmantojot plānošanu
description: Izmantojot anketēšanas plānošanu, var plānot un sadalīt anketas vairākiem respondentiem.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ddad70792c4ebc1785698812fe12406142f07a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790624"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Aptauju sadalīšana, izmantojot plānošanu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Izmantojot anketēšanas plānošanu, var plānot un sadalīt anketas vairākiem respondentiem. Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.

## <a name="create-a-questionnaire-schedule"></a>Izveidot anketas grafiku

1. Pārejiet uz sadaļu Anketa > Sadale > Anketēšanas grafiki.

2. Noklikšķiniet uz Jauns.

3. Ierakstiet vērtību laukā Plānošana.

4. Apraksta laukā ierakstiet vērtību.
    * Iestatiet grafika statusu Anonīms, ja atbildes ir jāreģistrē bez vārda un uzvārda saistīšanas ar atbildi.  
    * Lai iespējotu anonīmus rezultātus, vispirms ir jāiestata personāla vadības parametrus.  

5. Laukā Veids atlasiet plānošanas veidu.  Šajā piemērā tiks izmantots Apmierinātības tips.

6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

8. Laukā Datums ievadiet kādu datumu.

9. Izvērsiet sadaļu E-pasta ziņojums darbinieku patstāvīgai izmantošanai.

10. Ierakstiet vērtību laukā Tēma.

    * Piemērs: Anketa pieejama  

11. Teksta laukā ierakstiet e-pasta ziņojuma pamattekstu. Ņemiet vērā, ka mainīgais var tikt izmantots, lai aizstātu vērtības sistēmā.

    * Piemērs: Cien. %P%! Lūdzu, piesakieties darbinieku pašapkalpes pakalpojumā, lai aizpildītu darbaspēka veselības novērtējuma anketu.  Contoso  

12. Noklikšķiniet uz Saglabāt.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Izmantojiet detalizētu informācija par Iestatīšanu, lai atlasītu anketu(as), kura(s) jāatbild, kā arī vaicājumus, kas ir jāizmanto respondentu atlasei.

1. Noklikšķināt uz Detalizēta informācija par iestatīšanu.

2. Sarakstā atlasiet vaicājumu, ko izmantot, lai veiktu anketas respondentu meklēšanu sistēmā.

    * Piemērs: Darbinieki  

3. Noklikšķiniet uz Skatīt vai mainīt vaicājumu, lai atlasītu konkrētas personas vai pielāgotu vaicājumu un atrastu personas, kas atbilst noteiktiem kritērijiem.

    * Ņemiet vērā, ka visiem respondentiem ir jābūt arī sistēmas lietotājiem.  

4. Sarakstā atzīmējiet rindu Personai

5. Laukā Kritēriji ievadiet vai atlasiet kādu vērtību.

    * Atlasiet Jūlija Funderburka  

6. Sarakstā atlasiet Jūlija Funderburka

7. Noklikšķiniet uz OK.

8. Noklikšķiniet uz cilnes Anketas.

9. Kokā izvērsiet 'mezglu anketas tipam Apmierinātības aptauja'.

10. Kokā pārbaudiet 'Darbaspēka veselības novērtējums'.

11. Noklikšķiniet uz OK.

12. Noklikšķiniet uz Plānotā atbilžu sesija.

    * Ņemiet vērā, ka plānotās atbilžu sesijas ir izveidotas katram atlasītajam vai anketētajam lietotājam.  

13. Aizvērt lapu.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Sāciet anketēšanas grafiku, lai respondents var piekļūt anketai un to aizpildīt.

1. Noklikšķiniet uz Funkcijas.

2. Noklikšķiniet uz Sākt.

3. Noklikšķiniet uz OK.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Nosūtiet e-pasta ziņojumu, lai informētu respondentus par pieejamo anketu.

1. Noklikšķiniet uz Funkcijas.

2. Noklikšķiniet uz Sūtīt e-pasta ziņojumu.

3. Noklikšķiniet uz Atcelt.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Izmantojiet plānotās atbilžu sesijas, lai pārraudzītu, kam ir jāaizpilda anketa.

1. Noklikšķiniet uz Plānotā atbilžu sesija.

    * Dzēsiet visas atlikušās plānotās atbilžu sesijas, kad viss ir sagatavots plānotās sesijas pabeigšanai.  

2. Noklikšķiniet uz Dzēst.

3. Noklikšķiniet uz Jā.

4. Aizvērt lapu.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Kad visi respondenti ir aizpildījuši anketu, varat plānošanu beigt, un/vai visas atlikušās plānotās atbilžu sesijas ir dzēstas.

1. Noklikšķiniet uz Funkcijas.
2. Noklikšķiniet uz Beigt.
3. Noklikšķiniet uz OK.



[!INCLUDE[footer-include](../includes/footer-banner.md)]