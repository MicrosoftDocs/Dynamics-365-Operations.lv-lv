---
title: "Anketu izplatīšana un plānošana"
description: "Šajā tēmā ir skaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: eafcb047117eab73fddbd93c4c1d0aafb0023ebd
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="distribute-and-schedule-questionnaires"></a>Anketu izplatīšana un plānošana

[!include [banner](includes/banner.md)]

Šajā tēmā ir skaidrots, kā jūsu izveidotās anketas izplatīt tā, lai tās būtu pieejamas tai personai vai personu grupai, kas anketas aizpildīs. 

Anketu var izplatīt vairākos veidos:

-   Atzīmējiet anketu kā aktīvu. Pēc tam anketa ir pieejama visiem darbiniekiem, ja vien nav iestatīta anketu grupa, kas tai ierobežotu piekļuvi.
-   Piešķiriet tiesības anketu grupai. Pēc tam anketa ir pieejama visiem atlasītās grupas dalībniekiem.
-   Izveidojiet plānotas atbilžu sesijas. Pēc tam anketa ir pieejama tikai noteiktai personai.
-   Izveidojiet grafiku. Pēc tam anketa var būt pieejama vairākām personām.

## <a name="marking-a-questionnaire-as-active"></a>Anketu kā aktīvas atzīmēšana
Lapā **Anketas** lauku **Aktīvs** iestatot uz **Jā**, šo anketu varat padarīt pieejamu aizpildīšanai visiem darbiniekiem. Respondenti anketu var aizpildīt vairākas reizes. Šī funkcionalitāte noder, ja vēlaties iegūt pastāvīgas atsauksmes visa gada laikā. Piemēram, varat izveidot anketu, ko darbinieki izmanto, lai sniegtu atsauksmes par pusdienu pakalpojumu kafejnīcā.

## <a name="questionnaire-groups"></a>Aptauju grupas
Varat iestatīt anketu grupas un pēc tam iekļaut respondentus, kuriem šī anketa ir jāizplata. 

Anketu grupas varat izveidot no šādām lapām:

-   **Anketu grupas** — atlasīto anketu var aizpildīt tikai anketu grupā iekļautās personas. Piemēram, jūsu mērķauditorija ir darbuzņēmēji, tāpēc jūs izveidojat anketu grupu, kas ir raksturīga šiem respondentiem.
-   **Aptauju grupu dalībnieki** — anketu grupām varat pievienot personas.

Lai anketai piešķirtu anketu grupu, lapā **Anketas** noklikšķiniet uz **Lietotāja tiesības**. Kad anketa ir saglabāta kā aktīva, anketu grupas dalībnieki var aizpildīt šo anketu. Šī funkcionalitāte noder, ja anketu vēlaties testēt ar atlasītu personu grupu, pirms to izplatāt lielākai grupai, vai ja anketu vēlaties izmantot ļoti specifiskai mērķauditorijai.

## <a name="planned-answer-sessions-in-a-questionnaire"></a>Plānotās atbilžu sesijas anketā
Plānotās atbilžu sesijas ir anketas, ko esat izstrādājis un kam esat atlasījis respondentus. 

> **Piezīme.** Pirms iestatāt plānotās atbilžu sesijas, ir jāizveido anketa. 

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

Izmantojiet lapu **Atsauču tipi**, lai anketai iestatītu atsauču tipus. Katrs atsauču tips atbilst tabulai programmā Microsoft Dynamics 365 for Finance and Operations. Kad veidojat anketu grafikus, tabulā varat norādīt atsevišķus ierakstus vai ierakstu diapazonu, ar kuriem anketa būs saistīta. 

Piemēram, ja atlasāt tabulu Kursi, varat izlemt, kuram konkrētajam kursam šī anketa būs paredzēta. Kad iestatāt atsauci tabulai Kursi, lapā **Kursi** kļūst pieejami daži lauki un pogas.

### <a name="questionnaire-schedules"></a>Anketu grafiki

Anketu grafikus varat izmantot, lai ģenerētu vairākas plānotās atbilžu sesijas lietotāju grupai, pamatojoties uz atsauču tipu. Izveidojiet grafiku lapā **Anketu grafiki**. Atlasiet plānošanas tipu, lai kategorizētu šo grafiku, kā arī atlasiet atsauču tipu, kas ir jālieto, lai sistēmai veidotu vaicājumus par konkrētiem lietotājiem. Piemēram, ja atsauču tipu iestatāt uz tabulu Kursi, laukā **Atsauce** varat atlasīt konkrētu kursu. 

Noklikšķiniet uz **Detalizēta informācija par iestatījumu**, lai atlasītu anketu un citus kritērijus. Piemēram, ja anketa ir instruktora novērtējums, kā kritēriju norādiet instruktora vārdu. Kad esat beidzis ievadīt informāciju par iestatījumiem, sistēma ģenerē plānotās atbilžu sesijas vaicājumā iekļautajiem lietotājiem. 

Noklikšķiniet uz **Plānotās atbilžu sesijas**, lai skatītu atbilžu sesijas šim grafikam. Pēc tam varat manuāli izveidot papildu plānotās atbilžu sesijas vai dzēst plānotās atbilžu sesijas, kuras nav atbildētas. 

Lai anketu paradītu pieejamu lietotājiem saistītajās plānotajās atbilžu sesijās, noklikšķiniet uz **Funkcijas** &gt; **Sākums**. Noklikšķiniet uz **Atbildes**, lai skatītu aizpildītās atbildes uz anketas jautājumiem. Anketas grafika iestatījumus, plānotās atbilžu sesijas un atbildes pēc izvēles varat kopēt uz jaunu anketas grafiku.

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a>Ziņošana respondentiem par viņiem pieejamām anketām
Kad izplatāt kādu anketu, jums ir jāpaziņo respondentiem, ka viņiem ir pieejamas anketas. 

### <a name="notifying-respondents-about-a-planned-answer-session"></a>Ziņošana respondentiem par plānoto atbilžu sesiju

Ja izmantojat plānoto atbilžu sesiju, jums persona ir jāinformē tieši, piemēram, pa tālruni vai e-pastu.

### <a name="notifying-respondents-about-a-scheduling"></a>Respondentu informēšana par plānošanu

Izmantojiet lapu **Anketu grafiki**, lai sagatavotu un nosūtītu e-pasta ziņojumus visiem anketai piešķirtajiem respondentiem. Ievadiet e-pasta ziņojuma tekstu cilnē **E-pasta ziņojums, ko sūtīt uz darbinieku pašapkalpošanos**. Kad grafiks ir sācies, noklikšķiniet uz **Funkcijas** &gt; **Nosūtīt e-pastu**, lai ģenerētu un respondentiem nosūtītu e-pasta ziņojumu. Pēc tam respondenti var pierakstīties vietnē un aizpildīt anketu. 

> **Piezīme.** Lai varētu izmantot e-pasta funkcionalitāti, IT administratoram ir jāievada e-pasta iestatījumi lapā **E-pasta parametri**.

## <a name="ending-a-scheduled-questionnaire"></a>Plānotas anketas beigšana
Ieplānoto anketu var pabeigt pēc tam, kad visi respondenti ir aizpildījuši piešķirtās atbilžu sesijas. Kad plānota anketa ir beigusies, tās iestatījumus vairs nevarat kopēt uz jaunu grafiku. 

> **Piezīme.** Ja viens vai vairāki respondenti nav aizpildījuši anketu, bet jūs joprojām vēlaties beigt plānošanu, vispirms šie respondenti ir jāizdzēš no saraksta lapā **Plānotā atbilžu sesija**. Pēc tam grafiku varat beigt.

## <a name="completing-questionnaires"></a>Anketu aizpildīšana
Kad esat izstrādājis un izplatījis kādu anketu, šo anketu var aizpildīt atlasīti respondenti. Jūs varat aizpildīt jums pieejamās aptaujas anketas no divām vietām:

-   Navigācijas rūtī noklikšķiniet uz **Anketas** &gt; **Izplatīt** &gt; **Aizpildīt anketu**.
-   Darbinieku pašapkalpošanās lapā noklikšķiniet uz **Aizpildāmās anketas**.

Anketas var tikt padarītas pieejamas noteiktiem lietotājiem vai lietotāju grupām, vai visiem lietotājiem tīklā.

<a name="additional-resources"></a>Papildu resursi
--------

[Anketu veidošana](design-questionnaires.md)

[Anketu lietošana](questionnaires.md)

[Anketu rezultātu skatīšana un novērtēšana](evaluate-questionnaire-results.md)



