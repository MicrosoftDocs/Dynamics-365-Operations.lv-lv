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
ms.openlocfilehash: a2336cafe7e2c914c2592c91c888b1e0ae1bc608
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728680"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Aptauju sadalīšana, izmantojot plānošanu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Izmantojot anketēšanas plānošanu, var plānot un sadalīt anketas vairākiem respondentiem. USMF ir paraugdatu uzņēmums, kas tiek izmantots šīs procedūras izveidei.

## <a name="create-a-questionnaire-schedule"></a>Izveidot anketas grafiku

1. Dodieties uz **·** > **anketu** > **sadales grafikiem**.

2. Klikšķiniet **Jauns**.

3. **Laukā** Plānošana ierakstiet vērtību.

4. Laukā **Apraksts** ierakstiet kādu vērtību.
    * Iestatiet grafiku uz **·** Anonīms, ja atbildes ir jāieraksta bez nosaukumiem, kas saistīti ar atbildi.  
    * Lai iespējotu anonīmus rezultātus, vispirms ir jāiestata personāla vadības parametrus.  

5. Laukā **·** Tips atlasiet plānošanas tipu.  Šajā piemērā mēs izmantosim **apmierinājuma** tipu.

6. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.

8. Laukā **Datums** ievadiet datumu.

9. Izvērsiet **sadaļu E-pasts darbinieku** pašapkalpošanās pakalpojumam.

10. Laukā **Temats** ievadiet vērtību.

    * Piemērs: Anketa pieejama  

11. Laukā **·** Teksts ierakstiet e-pasta ziņojuma pamattekstu. Ņemiet vērā, ka mainīgais var tikt izmantots, lai aizstātu vērtības sistēmā.

    * Piemērs: Cien. %P%! Lūdzu, piesakieties darbinieku pašapkalpes pakalpojumā, lai aizpildītu darbaspēka veselības novērtējuma anketu.  Contoso  

12. Noklikšķiniet uz **Saglabāt**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Izmantojiet detalizētu informācija par Iestatīšanu, lai atlasītu anketu(as), kura(s) jāatbild, kā arī vaicājumus, kas ir jāizmanto respondentu atlasei.

1. Noklikšķiniet uz **Detalizēta informācija par** iestatījumu.

2. Sarakstā atlasiet vaicājumu, ko izmantot, lai veiktu anketas respondentu meklēšanu sistēmā.

    * Piemērs: Darbinieki  

3. Noklikšķiniet **uz skatīt vai modificēt vaicājumu, lai atlasītu** noteiktus cilvēkus vai pielāgotu vaicājumu, lai atrastu personas, kas atbilst konkrētiem kritērijiem.

    * Ņemiet vērā, ka visiem respondentiem ir jābūt arī sistēmas lietotājiem.  

4. Sarakstā atzīmējiet personu rindu.

5. Ievadiet vai atlasiet vērtību laukā **Kritēriji**.

    * Atlasiet Jūlija Funderburka  

6. Sarakstā atlasiet Jūlija Funderburka

7. Noklikšķiniet uz **Labi**.

8. Noklikšķiniet uz **cilnes** Anketas.

9. Koka struktūrā izvērsiet anketas tipa Apmierinātības aptauja **·** zaru.

10. Kokā pārbaudiet 'Darbaspēka veselības novērtējums'.

11. Noklikšķiniet uz **Labi**.

12. Noklikšķiniet **uz Plānotā atbilžu** sesija.

    * **Ievērojiet, ka plānotās** atbilžu sesijas ir izveidotas katram atlasītajam/vaicājuma lietotājam.  

13. Aizvērt lapu.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Sāciet anketēšanas grafiku, lai respondents var piekļūt anketai un to aizpildīt.

1. Noklikšķiniet uz **Funkcijas**.

2. Noklikšķiniet uz **Sākt**.

3. Noklikšķiniet uz **Labi**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Nosūtiet e-pasta ziņojumu, lai informētu respondentus par pieejamo anketu.

1. Noklikšķiniet uz **Funkcijas**.

2. Noklikšķiniet uz **Sūtīt e-pastu.**

3. Noklikšķiniet uz **Atcelt**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Izmantojiet plānotās atbilžu sesijas, lai pārraudzītu, kam ir jāaizpilda anketa.

1. Noklikšķiniet **uz Plānotā atbilžu** sesija.

    * Dzēsiet visas atlikušās plānotās atbilžu sesijas, kad viss ir sagatavots plānotās sesijas pabeigšanai.  

2. Noklikšķiniet uz **Dzēst**.

3. Noklikšķiniet uz pogas **Jā**.

4. Aizvērt lapu.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Kad visi respondenti ir aizpildījuši anketu, varat plānošanu beigt, un/vai visas atlikušās plānotās atbilžu sesijas ir dzēstas.

1. Noklikšķiniet uz **Funkcijas**.
2. Noklikšķiniet **uz** Beigt.
3. Noklikšķiniet uz **Labi**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
