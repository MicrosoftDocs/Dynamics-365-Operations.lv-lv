---
title: "Aptaujas izplatīšana un aizpildīšana"
description: "Šajā tēmā ir paskaidrots, kā izplatīt anketas, kas tiek būvēta, tā, lai tie būtu pieejami cilvēks vai cilvēku grupa, kas tās aizpildīt."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: 8e09c6b042d557e3b2d608fb5e278169fc3c1d88
ms.lasthandoff: 03/31/2017


---

# <a name="distribute-and-complete-a-questionnaire"></a>Aptaujas izplatīšana un aizpildīšana

Šajā tēmā ir paskaidrots, kā izplatīt anketas, kas tiek būvēta, tā, lai tie būtu pieejami cilvēks vai cilvēku grupa, kas tās aizpildīt. 

Anketu var izplatīt vairākos veidos:

-   Atzīmējiet anketu kā aktīvu. Pēc tam anketa ir pieejama visiem darbiniekiem, ja vien nav iestatīta anketu grupa, kas tai ierobežotu piekļuvi.
-   Piešķiriet tiesības anketu grupai. Pēc tam anketa ir pieejama visiem atlasītās grupas dalībniekiem.
-   Izveidojiet plānotas atbilžu sesijas. Pēc tam anketa ir pieejama tikai noteiktai personai.
-   Izveidojiet grafiku. Pēc tam anketa var būt pieejama vairākām personām.

## <a name="marking-a-questionnaire-as-active"></a>Anketu kā aktīvas atzīmēšana
Iestatot **Active** lauku, lai **Jā** par **anketas** lapu, jūs anketa būs pieejama visiem darbiniekiem, lai pabeigtu. Respondenti var aizpildīt anketu vairākas reizes. Šī funkcionalitāte noder, ja vēlaties ievākt atsauksmes nepārtraukti, visu gadu. Piemēram, varat izveidot anketu, ko darbinieki izmanto, lai sniegtu atsauksmes par pusdienu pakalpojumu kafejnīcā.

## <a name="questionnaire-groups"></a>Aptauju grupas
Varat iestatīt anketu grupas un pēc tam iekļaut respondentus, kuriem šī anketa ir jāizplata. 

Anketu grupas varat izveidot no šādām lapām:

-   **Anketu grupas **— atlasīto anketu var aizpildīt tikai anketu grupā iekļautās personas. Piemēram, jūsu mērķauditorija ir darbuzņēmēji, tāpēc jūs izveidojat anketu grupu, kas ir raksturīga šiem respondentiem.
-   **Aptauju grupu dalībnieki** — anketu grupām varat pievienot personas.

Piešķirtu anketu grupas anketai, par **anketas** lapu, noklikšķiniet uz **lietotāja tiesību**. Pēc anketas tiek saglabāta kā aktīvu, anketu grupas locekļi var aizpildīt anketu. Šī funkcija ir noderīga, ja vēlaties pārbaudīt anketu par atlasiet personu grupu, pirms jūs roll to lielākai grupai, vai mērķa anketu ar ļoti specifisku auditoriju.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Plānotās atbilžu sesijas anketā
Plānotās atbilžu sesijas ir anketas, ko esat izstrādājis un kam esat atlasījis respondentus. 

**Piezīme.** Pirms iestatāt plānotās atbilžu sesijas, ir nepieciešams izveidot anketu. 

Lapā **Plānotā atbilžu sesija** varat izveidot plānoto atbilžu sesiju atsevišķam darbiniekam. Lapas sarakstā tiek rādītas visas plānotās anketas. 

Plānotās atbilžu sesijas tiek lietotas arī lapā **Anketu grafiki**, kur varat plānot anketas vairākām personām:

-   Darbinieki
-   Kursu dalībnieki
-   Organizācijas vienības

Katra persona uz anketu var atbildēt tikai vienu reizi.

## <a name="scheduling-a-questionnaire"></a>Anketas plānošana
Pēc izvēles anketu varat plānot vairākiem respondentiem.

### <a name="planning-types"></a>Plānošanas tipi

Ja plānotās atbilžu sesijas vēlaties plānot vairākiem respondentiem, plānošanas tipi ir obligāti. Plānošanas tipi tiek izmantoti, lai klasificētu anketu grafikus. Piemēram, anketas varat plānot tālāk norādītajiem mērķiem.

-   Novērtējums
-   Aptauja
-   Testēšana

Anketas grafikam plānošanas tipu varat norādīt lapā **Anketu grafiki**.

### <a name="reference-types-for-questionnaire"></a>Anketas atsauču tipi

Atsauču tipus var izmantot, lai ievadītu kritērijus respondentiem, kurus varat atlasīt, kad plānojat anketu. 

Izmantojiet lapu **Atsauču tipi**, lai anketai iestatītu atsauču tipus. Tabulu programmā Microsoft Dynamics 365 operācijas atbilst katram atsauču tipam. Kad veidojat anketu grafikus, tabulā varat norādīt atsevišķus ierakstus vai ierakstu diapazonu, ar kuriem anketa būs saistīta. 

Piemēram, ja atlasāt tabulu Kursi, varat izlemt, kuram konkrētajam kursam šī anketa būs paredzēta. Kad iestatāt atsauci tabulai Kursi, lapā **Kursi** kļūst pieejami daži lauki un pogas.

### <a name="questionnaire-schedules"></a>Anketu grafiki

Aptaujas grafiki var izmantot, lai radītu vairākas plānotās atbilžu sesijas grupu lietotājiem, balstoties uz atsauces tipu. Izveidot grafiku **aptaujas grafiki** lapā. Atlasiet plānošanas tipa kategorizēt grafiku un arī atlasiet atsauces tips, kas jāizmanto, lai vaicātu sistēma noteiktiem lietotājiem. Piemēram, ja kursi tabulas atsauces tipu, varat atlasīt īpašu kursu **references** lauks. 

Noklikšķiniet uz **Detalizēta informācija par iestatījumu**, lai atlasītu anketu un citus kritērijus. Piemēram, norādiet instruktora vārdu kā kritēriju, ja anketa ir instruktors izvērtējums. Pēc tam, kad esat pabeidzis ievadīt iestatīšanas detaļas, sistēma ģenerē plānoto atbilžu sesijas lietotāji, kas iekļauti vaicājuma. 

Noklikšķiniet uz **Plānotās atbilžu sesijas**, lai skatītu atbilžu sesijas šim grafikam. Pēc tam varat manuāli izveidot papildu plānotās atbilžu sesijas vai dzēst plānotās atbilžu sesijas, kuras nav atbildētas. 

Noklikšķiniet uz **funkcijas**&gt;**sākt** anketa būs pieejama lietotājiem saistīto plānotās atbilžu sesijas. Noklikšķiniet uz **Atbildes**, lai skatītu aizpildītās atbildes uz anketas jautājumiem. Anketas grafika iestatījumus, plānotās atbilžu sesijas un atbildes pēc izvēles varat kopēt uz jaunu anketas grafiku.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Ziņošana respondentiem par viņiem pieejamām anketām
Kad izplatāt kādu anketu, jums ir jāpaziņo respondentiem, ka viņiem ir pieejamas anketas. 

**Piezīme:** respondentu jābūt lietotājiem Microsoft Dynamics 365 operācijām, lai aizpildītu anketu.

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Ziņošana respondentiem par plānoto atbilžu sesiju

Ja izmantojat plānoto atbilžu sesiju, jums persona ir jāinformē tieši, piemēram, pa tālruni vai e-pastu.

### <a name="notifying-respondents-about-a-scheduling"></a>Respondentu informēšana par plānošanu

Izmantojiet lapu **Anketu grafiki**, lai sagatavotu un nosūtītu e-pasta ziņojumus visiem anketai piešķirtajiem respondentiem. Ievadiet e-pasta ziņojuma tekstu cilnē **E-pasta ziņojums, ko sūtīt uz darbinieku pašapkalpošanos**. Pēc tam, kad ir uzsākta grafiku, noklikšķiniet uz **funkcijas**&gt;**sūtīt e-pastu** sagatavot un nosūtīt e-pastu uz respondentu. Respondenti pēc tam varat pieteikties mājas lapā un aizpildīt anketu. 

**Piezīme.** Lai varētu izmantot e-pasta funkcionalitāti, IT administratoram ir jāievada e-pasta iestatījumi lapā **E-pasta parametri**.

## <a name="ending-a-scheduled-questionnaire"></a>Plānotas anketas beigšana
Ieplānoto anketu var pabeigt pēc tam, kad visi respondenti ir aizpildījuši piešķirtās atbilžu sesijas. Kad plānota anketa ir beigusies, tās iestatījumus vairs nevarat kopēt uz jaunu grafiku. 

**Piezīme.** Ja viens vai vairāki respondenti nav aizpildījusi anketu, bet jūs joprojām vēlaties beigt plānošanu, jums vispirms šie respondenti ir jāizdzēš no saraksta lapā **Plānotā atbilžu sesija**. Pēc tam grafiku varat beigt.

## <a name="completing-questionnaires"></a>Anketu aizpildīšana
Kad esat izstrādājis un izplatījis kādu anketu, šo anketu var aizpildīt atlasīti respondenti. Jūs varat aizpildīt jums pieejamās aptaujas anketas no divām vietām:

-   Navigācijas rūtī noklikšķiniet uz **anketas**&gt;**izkliedēt**&gt;**anketas**.
-   Darbinieku pašapkalpošanās lapā noklikšķiniet uz **Aizpildāmās anketas**.

Anketas var tikt padarītas pieejamas noteiktiem lietotājiem vai lietotāju grupām, vai visiem lietotājiem tīklā.

<a name="see-also"></a>Skatiet arī
--------

[Anketu veidošana](design-questionnaires.md)

[Anketu lietošana](questionnaires.md)

[Apskate un anketu rezultātu izvērtēšanai](evaluate-questionnaire-results.md)


