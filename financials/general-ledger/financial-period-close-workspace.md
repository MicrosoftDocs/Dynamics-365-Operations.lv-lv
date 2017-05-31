---
title: "Finanšu perioda slēgšanas darbvieta"
description: "Šajā rakstā ir sniegts pārskats par finanšu perioda slēgšanas darbvietu un saistīto konfigurāciju."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 788b0af30eb750cad8f958ecc4c33cf989b2a417
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="financial-period-close-workspace"></a>Finanšu perioda slēgšanas darbvieta

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par finanšu perioda slēgšanas darbvietu un saistīto konfigurāciju.

Finanšu perioda slēgšanas darbvieta

Darbvietā **Finanšu perioda slēgšana** varat sekot līdzi savu uzņēmumu, jomu un personu finanšu slēgšanas procesiem. Atkarībā no skata darbvietā **Finanšu perioda slēgšana** ir redzami vai nu visi slēgšanas grafika uzdevumi un statusi, vai tikai jums piešķirtie uzdevumi. 

Vispirms ir jāatlasa slēgšanas grafiks darbvietas augšpusē. Visi darbvietā rādītie dati pēc tam tiek filtrēti pēc atlasītā slēgšanas grafika.

### <a name="summary-tiles"></a>Kopsavilkuma elementi

**Kopsavilkuma** elementos ir sniegts pārskats par procesu un indikatori, kas palīdz izsekot slēgšanas procesa izpildi. Var redzēt nokavētos uzdevumus, šodien atlikušos uzdevumus, uzdevumus, kuru izpildes datums ir šodiena, bet tie ir bloķēti atkarību dēļ, kā arī visus pārējos procesa uzdevumus. Šī informācija ir paredzēta visiem uzņēmumiem, kas ir iekļauti atlasītajā slēgšanas grafikā.

### <a name="tasks-and-status-section"></a>Uzdevumu un statusa sadaļā

Sadaļā **Uzdevumi un statuss** vispārējā slēgšanas grafika statuss tiek dažādi sadalīts: statuss pēc uzņēmuma, statuss pēc apgabala un statuss pēc atbildīgās personas. Mainot filtru karšu saraksta augšpusē, varat skatīt statusu visiem slēgšanas grafikā iekļautajiem uzdevumiem, tikai šodien izpildāmajiem uzdevumiem vai nokavētajiem uzdevumiem. Varat arī atlasīt uzņēmuma filtru, lai skatītu statusu noteiktam uzņēmumam. Katra statusa cilne sniedz detalizētu informāciju gan pēc izpildītā procentuālā daudzuma, gan pēc atlikušo uzdevumu skaita. Noklikšķiniet uz kartes vai darbības **Skatīt detalizētu informāciju**, lai detalizēto uzdevumu sarakstu filtrētu pēc atlasītās kartes. 

Pēdējā cilne ir paredzēta detalizētajam uzdevumu sarakstam. Šajā sarakstā ir ietverts pilns uzdevumu saraksts, un to var filtrēt tā, lai parādītu tikai jums interesējošos uzdevumus. Uzdevumu sarakstu varat filtrēt vairākos veidos. Varat, piemēram, filtrēt pēc uzdevumu izpildes datuma, saistītā uzņēmuma un saistītā apgabala. Varat arī izvēlēties uzdevumu sarakstā rādīt vai paslēpt pabeigtos uzdevumus. 

Uzdevumiem tiek izmantoti divi tālāk minētie rādītāji.

-   Ikona ar izsaukuma zīmi norāda, ka uzdevuma izpilde ir nokavēta. Uzdevumiem, kuru izpilde ir nokavēta, arī apmaksas datums tiek izcelts sarkanā krāsā.
-   Ikona ar slēdzeni norāda, ka uzdevums ir atkarīgs no citiem uzdevumiem, kas vēl nav izpildīti. Uzdevumu, kas ir bloķēts atkarību dēļ, nevar atzīmēt kā pabeigtu. Atkarības uzdevumam var iestatīt, izmantojot darbību **Iestatīt atkarību**.

Uzdevuma nosaukums ir hipersaite uz Microsoft Dynamics 365 for Operations lapu vai citu tīmekļa lapu, kur lietotājam ir jāpariet, lai pabeigtu darbu. Šo hipersaiti varat iestatīt, izmantojot lauku **Uzdevuma saite**, kad rediģējat vai izveidojat kādu uzdevumu. 

Uzdevumam varat pievienot failus, piezīmes, attēlus un vietrāžus URL, izmantojot darbību **Pielikumi**. Piemēram, varat norādīt žurnāla numurus, kas tiek izmantoti kā daļa no uzdevuma, pievienot komentārus par noteiktu uzdevumu vai pievienot pārskata failu, kas tika izdrukāts kādam uzdevumam. Ja pastāv pielikums, uzdevumam tiek parādīta ikona kolonnā **Pielikums**. 

Opcija **Uzdevums pabeigts** ir manuāli jāatlasa pēc tam, kad uzdevums ir pabeigts. Kad uzdevums ir atzīmēts kā pabeigts, lauks **Pabeigšanas datums** automātiski tiek atjaunināts ar pašreizējo datumu un laiku. Arī atkarību rādītāji tiek atbilstoši atjaunināti.

## <a name="all-financial-period-close-tasks-list-page"></a>Visu finanšu periodu slēgšanas uzdevumu saraksta lapa
Visus pašreizējos un iepriekšējo periodu slēgšanas uzdevumus varat skatīt saraksta lapā **Visi finanšu perioda slēgšanas uzdevumi**. Šo saraksta lapu vislabāk izmantot slēgšanas procesa vēsturisko datu analīzē, jo tajā ir ietverta informācija par plānoto izpildes datumu, faktisko pabeigšanas datumu un personu, kas šo uzdevumu pabeidza. Šīs saraksta lapas informāciju varat ērti eksportēt uz programmu Microsoft Excel, lai veidotu pārskatus un veiktu auditus.

## <a name="financial-period-close-configuration-page"></a>Finanšu perioda slēgšanas konfigurācijas lapa
Lai varētu izmantot darbvietu **Finanšu perioda slēgšana**, process ir jākonfigurē sistēmā Microsoft Dynamics 365 for Operations, izmantojot lapu **Finanšu perioda slēgšanas konfigurācija**. (Noklikšķiniet uz **Virsgrāmata** &gt; **Perioda slēgšana** &gt; **Finanšu perioda slēgšanas konfigurācija**.)

### <a name="resources"></a>Resursi

Cilnē **Resursi** ir jādefinē personas, kuras ir iesaistītas slēgšanas procesos. Jebkurš darbinieks, kurš būs atbildīgs par kādu slēgšanas uzdevumu, vispirms ir jāpiešķir šeit. Tāpat jums ir jānorāda darbinieku skats uz šo darbvietu. Pieejamas šādas opcijas

-   **Tikai piešķirtie uzdevumi** — lietotājs redzēs tikai viņam(-ai) piešķirtos uzdevumus;
-   **Visi uzdevumi un statuss** — lietotājs redzēs visus slēgšanas uzdevumus un vispārīgo procesa statusu.

Lietotāji, kuriem ir atļauja skatīt tikai viņam(-ai) piešķirtos uzdevumus nevar uzdevumus pievienot uzdevumu sarakstam, kā arī rediģēt vai noņemt uzdevumus no uzdevumu saraksta.

### <a name="task-areas"></a>Uzdevumu apgabali

Uzdevumu jomas tiek izmantotas slēgšanas uzdevumu grupēšanai loģiskas īpašumtiesību jomās jūsu organizācijā. Piemēram, Kreditori, Debitori vai Virsgrāmata var izmantot kā uzdevumu jomas.

### <a name="calendars"></a>Kalendāri

Finanšu slēgšanas kalendāri ir jāveido un jārediģē, izmantojot cilni Kalendāri.  Šajā cilnē varat definēt slēgšanas procesu darbdienas, un tā tiks izmantota slēgšanas uzdevumu plānošanai.  Izveidojiet jaunu kalendāru un norādiet darbdienas, kas jāizmanto uzdevuma plānošanai.  Kalendāru ieteicams izveidot ilgam periodam, piemēram, gadam vai vairākiem gadiem, jo pēc izveidošanas to var rediģēt.  Pēc kalendāra izveidošanas noklikšķiniet uz pogas Rediģēt, lai atjauninātu kalendāru noteiktām dienām, piemēram, svētku dienām.  Slēgšanas uzdevumi tiks ieplānoti dienās, kad vienumam Kontrole ir iestatīta vērtība Atvērts.  Ja slēgšanas uzdevumi nav jāplāno noteiktā dienā, šajā dienā vienumam Kontrole ir jāiestata vērtība Slēgts.

### <a name="templates"></a>Veidnes

Finanšu slēgšanas veidni varat izmantot, lai definētu visus uzdevumus, kas ir daļa no slēgšanas procesa. Slēgšanas uzdevums ir periodisks darbs, kas tiek piešķirts kādai personai, un tas ir jāizpilda katra slēgšanas procesa ietvaros. Veidnē relatīvais izpildes datums ir jādefinē katram slēgšanas uzdevumam. Relatīvais izpildes datums ir dienu skaits pirms vai pēc definētā perioda beigu datuma, kad šis uzdevums ir jāizpilda katrā periodā. Katram uzdevumam tiek piešķirts arī izpildes laiks. Izpildes laiks tiek noteikts, ņemot vērā jūsu laika joslu, un tas tiks pārveidots uz katram lietotājam atbilstošo laika joslu. 

Veidnē uzdevumu var piešķirt vienam vai vairākiem uzņēmumiem, uz kuriem šis uzdevums attiecas. Ja katrā uzņēmumā šī darba izpildei tiek piešķirta cita persona, var būt noderīgi vienam darbam izveidot vairākus uzdevumus. Izveidojiet vienu uzdevumu katram uzņēmumam. 

Izvēlnes vienums **Uzdevuma saite** ir saistīts ar uzdevuma darbu, un to var izmantot, lai no uzdevuma saites darbvietā pārietu tieši uz saistīto lapu. Piemēram, lai palaistu valūtas pārvērtēšanas procesu kreditoriem, slēgšanas uzdevumu var saistīt ar attiecīgo lapu **Ārvalstu valūtas pārvērtēšana** sistēmā Microsoft Dynamics 365 for Operations. Varat arī saistīt ar ārējo vietrādi URL. 

> [!Ieteikums] Lai finanšu perioda slēgšanas uzdevumam piesaistītu noteiktu pārvaldības pārskata sastādītāja pārskatu, var izmantot pārskata URL. Lai piekļūtu pārskata vietrādim URL, pārskatu veidotājā atveriet šo pārskatu un pēc tam noklikšķiniet uz **Fails** &gt; **Skatīt pārskatu**, lai pārskatu atvērtu tīmekļa pārlūkprogrammā. Pēc tam varat kopēt URL no pārlūkprogrammas adreses joslas un ielīmēt to laukā **Uzdevuma saites** **URL**. 

Veidnē varat definēt uzdevumu atkarības. Ja uzdevums ir iestatīts tā, lai būtu atkarīgs no viena vai vairākiem uzdevumiem, šo uzdevumu nevar atzīmēt kā pabeigtu, kamēr nav pabeigtas visas tā atkarības. 

Var izveidot vairākas finanšu slēgšanas veidnes. Pēc tam dažādās veidnes varat izmantot, lai izsekotu dažādu perioda tipu, piemēram, mēneša beigu vai gada beigu, slēgšanas procesiem vai izsekotu uzņēmumiem, kas izmanto atšķirīgus slēgšanas procesus. Kad viena veidne ir izveidota, to varat to kopēt, lai izveidotu jaunu veidni, kurā veikt nepieciešamās izmaiņas. Katram slēgšanas grafikam var piešķirt tikai vienu veidni.

### <a name="closing-schedules"></a>Slēgšanas grafiki

Slēgšanas grafiks tiek izmantots, lai finanšu slēgšanas veidni piešķirtu noteiktam finanšu periodam, kas ir jāslēdz. Pēc tam uzdevumi no veidnes tiek automātiski ģenerēti norādītajam periodam, un jaunais slēgšanas grafiks tiek pievienots darbvietai. Kad veidojat jaunu slēgšanas grafiku, lauks **Perioda beigu datums** tiek izmantots, lai faktiskos izpildes datumus slēgšanas uzdevumiem noteiktu, pamatojoties uz relatīvo izpildes datumu, kas tiek piešķirts finanšu slēgšanas veidnē. 

Piešķiriet kalendāru, kas ir piemērots slēgšanas grafikam, lai norādītu uzdevuma plānošanā izmantojamās darbdienas. Ja nedefinējat noteiktu kalendāru, uzdevumu izpildes datumiem tiks izmantotas visas nedēļas dienas. 

Ir jādefinē arī uzņēmumi, kas tiks piesaistīti attiecīgajam slēgšanas grafikam. Ja veidnes uzdevumi tiek piešķirti vairākiem uzņēmumiem, atsevišķi uzdevumi tiek izveidoti katram uzņēmumam, kas tika iekļauts slēgšanas grafikā un piešķirts veidnes uzdevumam. 

Kad slēgšanas grafiks ir pabeigts, atlasiet tam opciju **Slēgts**. Uzdevumu vēsture joprojām būs pieejama saraksta lapā **Visi finanšu perioda slēgšanas uzdevumi**, bet šis slēgšanas grafiks tiks noņemts no darbvietas. Kad slēgšanas grafiks ir atzīmēts kā **Slēgts**, tam vairs nevarat pievienot uzdevumus, rediģēt uzdevumus vai no tā noņemt uzdevumus.




