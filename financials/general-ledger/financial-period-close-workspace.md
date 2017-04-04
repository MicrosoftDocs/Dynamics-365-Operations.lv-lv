---
title: "Finanšu perioda slēgšanas darbvieta"
description: "Šajā rakstā ir sniegts pārskats par finanšu perioda slēgšanas darbvietu un saistīto konfigurāciju."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Finanšu perioda slēgšanas darbvieta

Šajā rakstā ir sniegts pārskats par finanšu perioda slēgšanas darbvietu un saistīto konfigurāciju.

Finanšu perioda slēgšanas darbvieta

**Finanšu perioda aizvērt** darbvietā ļauj izsekot jūsu finanšu slēgšanas procesu starp uzņēmumiem un darbības jomām, kā arī cilvēki. Atkarībā no jūsu viedokļa **finanšu perioda aizvērt** darbvietas, jūs redzēsiet, vai nu visus uzdevumus un stāvokļus slēgšanas grafiks vai vienkārši jums piešķirtos uzdevumus. 

Vispirms jāatlasa slēgšanas grafiks darbvietas augšpusē. Visi dati, kas tiek rādīta darbvietā tad filtrē ar atlasītajiem slēgšanas grafiks.

### <a name="summary-tiles"></a>Kopsavilkuma elementi

**Kopsavilkuma** elementos ir sniegts pārskats par procesu un indikatori, kas palīdz izsekot slēgšanas procesa izpildi. Jūs varat redzēt uzdevumus, kas ir pagātnes dēļ, atlikušos uzdevumus šodien, uzdevumi, kuru izpildes datums ir šodiena, bet tiek bloķētas jo atkarības un visus pārējos uzdevumus procesam. Šī informācija ir domāta visiem uzņēmumiem, kas iekļauti atlasītajiem slēgšanas grafiks.

### <a name="tasks-and-status-section"></a>Uzdevumu un statusa sadaļā

Šajā **uzdevumiem un statusa** sadaļas vispārējo statusu slēgšanas grafiks ir sadalīti dažādos veidos: statusu pēc uzņēmuma statusu pēc platības un statusu, persona, kura ir atbildīga. Statusu var skatīt, jo visi uzdevumi slēgšanas grafiks, tikai uzdevumi, kuru izpildes datums ir šodiena, vai uzdevumus, kas ir kavēts, mainot filtrs kartes saraksta augšdaļā. Varat arī atlasīt uzņēmuma filtrs, lai skatītu konkrēta uzņēmuma statusu. Katras zīmnes statuss dod sadalījums procentos, kas ir pabeigta, gan vairākus uzdevumus, kas paliek. Noklikšķiniet uz kartes vai **apskatīt** darbības detalizētu uzdevumu sarakstu filtrēt pēc atlasītā karte. 

Pēdējās cilnes ir detalizēta uzdevumu sarakstā. Šis saraksts rāda pilnu uzdevumu sarakstu un var filtrēt tā, ka tas parāda tikai tos uzdevumus, kas jūs interesē. Varat filtrēt uzdevumu sarakstā vairākos veidos. Piemēram, varat filtrēt pēc uzdevuma izpildes datumu, saistīto uzņēmumu un saistītā jomā. Varat arī izvēlēties rādīt vai slēpt Pabeigtie uzdevumi uzdevumu sarakstā. 

Uzdevumiem tiek izmantoti divi tālāk minētie rādītāji.

-   Izsaukuma ikona norāda, ka uzdevums ir kavēts. Uzdevumiem, kas tiek kavēts, apmaksas datums arī tiek iezīmēts ar sarkanu krāsu.
-   Piekaramās slēdzenes ikona norāda, ka uzdevums ir atkarīgs no citiem uzdevumiem, kas vēl nav pabeigts. Uzdevumu, kas ir bloķējusi atkarības nav atzīmēts kā pabeigts. Atkarības uzdevumam var iestatīt, izmantojot **noteikt atkarības** darbību.

Uzdevuma nosaukums ir hipersaiti uz Microsoft Dynamics 365 operāciju lappusi vai citu interneta lapu, kur lietotājs ir jāiet, lai pabeigtu darbu. Šo hipersaiti var iestatīt, izmantojot **uzdevuma saiti** lauks, rediģēt vai izveidot uzdevumu. 

Var pievienot failus, piezīmju, attēlu un URL uzdevumu, izmantojot **pielikumus** darbību. Piemēram, var norādīt žurnāla numuri, kas tiek izmantoti kā daļu no uzdevuma, pievienot komentārus par konkrēta uzdevuma vai pievienot ziņojumu failu, kas tika drukāts uzdevumam. Tiek parādīta ikona **pielikumu** kolonnu uzdevumu, ja pielikums ir klāt. 

**Uzdevumu pabeigt** opciju manuāli jāizvēlas pēc uzdevuma pabeigšanas. Kad uzdevums tiek atzīmēts kā pabeigts, **pabeigšanas datumu** lauks tiek automātiski atjaunināts ar pašreizējo datumu un laiku. Pēc vajadzības tiek atjauninātas arī atkarības rādītāji.

## <a name="all-financial-period-close-tasks-list-page"></a>Visu finanšu periodu slēgšanas uzdevumu saraksta lapa
Var apskatīt visus pašreizējā un iepriekšējā perioda aizvērt uzdevumus no **visus finanšu perioda aizvērt uzdevumu** saraksta lapu. Šī saraksta lapu vislabāk izmantot vēsturisko slēgšanas procesā, analīzei, jo tajā ir iekļauta informācija par plānoto izpildes datumu, faktisko pabeigšanas datumu un personai, kas aizpildījusi uzdevums. Informāciju par šī saraksta lapas var viegli eksportēt uz Microsoft Excel atskaišu un revīziju mērķiem.

## <a name="financial-period-close-configuration-page"></a>Finanšu perioda slēgšanas konfigurācijas lapa
Pirms varat izmantot **finanšu perioda aizvērt** darbvietas, jums jākonfigurē process Microsoft Dynamics 365 operācijām, izmantojot **finanšu perioda aizvērt konfigurācijas** lapā. (Noklikšķiniet uz **Virsgrāmatas**&gt;**perioda aizvērt**&gt;**finanšu perioda aizvērt konfigurācijas**.)

### <a name="resources"></a>Resursi

Par **resursu** tab, nosaka cilvēki, kuri ir iesaistīti slēgšanas procesu. Jebkuru darbinieku, kurš būs atbildīgs par uzdevuma slēgšanas jābūt piešķirtam vispirms šeit. Ir jānorāda darbinieka viedokļa darbvietu. Pieejamas šādas opcijas

-   **Tikai piešķirtie uzdevumi** — lietotājs redzēs tikai viņam(-ai) piešķirtos uzdevumus;
-   **Visi uzdevumi un statuss** — lietotājs redzēs visus slēgšanas uzdevumus un vispārīgo procesa statusu.

Lietotāji, kuriem ir atļauja skatīt tikai viņam(-ai) piešķirtos uzdevumus nevar uzdevumus pievienot uzdevumu sarakstam, kā arī rediģēt vai noņemt uzdevumus no uzdevumu saraksta.

### <a name="task-areas"></a>Uzdevumu apgabali

Uzdevumu jomas tiek izmantotas slēgšanas uzdevumu grupēšanai loģiskas īpašumtiesību jomās jūsu organizācijā. Piemēram, Kreditori, Debitori vai Virsgrāmata var izmantot kā uzdevumu jomas.

### <a name="calendars"></a>Kalendāri

Veidojiet un labojiet finanšu slēgšanas kalendāri, kalendāri tab lietošana.  Šī ir vieta, kur noteiks darba dienas slēgšanas procesu, un tiks izmantots plānošanai slēguma uzdevumus.  Izveidojiet jaunu kalendāru un norādītu darba dienas uzdevumu plānošanai jāizmanto.  Ieteicams izveidot kalendāru ilgu laiku, piemēram, gadu vai vairākus gadus, jo to var labot pēc izveides.  Pēc veidojot kalendāru, noklikšķiniet uz pogas Rediģēt, lai atjauninātu kalendāru, īpašas dienas, piemēram, brīvdienas.  Aizverot uzdevumu tiks plānoti par dienām, kad vadīklas vērtība ir iestatīts Atvērt.  Ja noslēguma uzdevumus grafikam noteiktā dienā nevajadzētu būt, šajā dienā ir vadīklas vērtībai, kas noteikta uz slēgts.

### <a name="templates"></a>Veidnes

Finanšu aizveriet veidni izmanto, lai definētu visus uzdevumus, kurus slēgšanas procesa sastāvdaļa. Slēgšanas uzdevums ir periodisks darbs pūles, kas piešķirti individuāli katram slēgšanas procesa pabeigšanai. Veidnē, relatīvā apmaksas datums ir jānosaka katra uzdevuma slēgšanas. Relatīvā apmaksas datums ir dienu skaits pirms vai pēc noteikta perioda beigu datums, kas šo uzdevumu, būs jāmaksā katram periodam. Izpildes laiks ir piešķirta katru uzdevumu. Izpildes laiks tiek iestatīts, izmantojot saistībā ar savu laika joslu un laika joslu, katram lietotājam tiek konvertētas. 

Uzdevuma veidnē var piešķirt vienam vai vairākiem uzņēmumiem, kas gadījumos, kad piemēro šo uzdevumu. Ja cita persona ir piešķirts, lai pabeigtu šo darbu pūles katrā uzņēmumā, var būt noderīgi vairāki uzdevumu veidošanai pašu darba intensitāti. Izveidojiet vienu uzdevumu katram uzņēmumam. 

**Uzdevuma saiti** izvēlnes elements ir saistīts ar uzdevumu darba intensitātes un var tikt izmantotas, lai dotos tieši uz saistīto lapu no uzdevuma saiti darbvietā. Piemēram, noslēguma uzdevumu, kuru jāpalaiž kreditoru valūtas pārvērtēšanas process var būt saistīts ar saistīto **ārvalstu valūtas pārvērtēšanas** lapu Microsoft Dynamics 365 operācijām. Varat arī saistīt ar ārējo vietrādi URL. 

> [! Hint] Ja vēlaties piesaistīt finanšu perioda aizvērt uzdevumu noteiktu apsaimniekošanas reportieris atskaiti, var izmantot atskaiti URL. Lai piekļūtu ziņojumu URL, atveriet atskaiti atskaišu izstrādes rīks un pēc tam noklikšķiniet uz **failu**&gt;**atskaites skatīšana** lai atskaiti atvērtu web pārlūkprogrammu. Pēc tam varat kopēt URL no pārlūkprogrammas adreses joslas un ielīmēt to laukā **Uzdevuma saites** **URL**. 

Veidnē var definēt uzdevumu atkarības. Ja uzdevums ir iestatīts atkarīgi viens vai vairāki uzdevumi, darbplūsmas uzdevumu nevar atzīmēts kā pabeigts līdz brīdim, kad ir pabeigtas visas atkarības. 

Var izveidot vairākus finanšu aizveriet veidnes. Dažādas veidnes var izmantot lai izsekotu periodu dažāda, piemēram, mēneša beigās vai gada beigās slēguma procesiem vai uzņēmumiem, kas izmanto dažādus slēguma procesiem izsekot. Pēc vienas veidnes izveidošanas var iekopēt jaunajā veidnē un veikt nepieciešamās izmaiņas. Var piešķirt tikai vienu veidni katru slēgšanas grafiks.

### <a name="closing-schedules"></a>Slēgšanas grafiki

Slēgšanas grafikā izmanto, lai piešķirtu finanšu aizveriet veidni finanšu periodu, kas ir jāaizver. Uzdevumus, izmantojot šo veidni, tad automātiski ģenerēts norādītajam periodam un jauns slēgšanas grafiks ir pievienot darbvietai. Veidojot jaunu slēgšanas grafiku, **perioda beigu datums** lauks tiek izmantots, lai noteiktu faktisko izpildes datumu slēguma uzdevumus, pamatojoties uz relatīvo apmaksas datums, kas tiek piešķirts finanšu aizveriet veidni. 

Piešķirtu atbilstošu slēgšanas grafiks, lai norādītu darba dienas uzdevumu plānošanā izmantot kalendāru. Ja nav definēt konkrētu kalendāra, uzdevumu izpildes datumiem tiks izmantot visu nedēļas dienu pilnu formu. 

Ir jādefinē arī uzņēmumiem, kas tiks saistīta ar slēgšanas grafiks. Ja veidni uzdevumi tiek piešķirti vairāki uzņēmumi, atsevišķi uzdevumi tiks izveidota katram uzņēmumam, kas atrodas slēgšanas grafiks un veidnes uzdevumam piešķirto. 

Pēc slēgšanas grafiks ir pabeigta, izvēlieties **slēgts** variants, par to. Uzdevuma vēsture joprojām būs pieejami no **visus finanšu perioda aizvērt uzdevumu** saraksta lappuses, bet slēgšanas grafiks tiks noņemta no darbvietas. Pēc slēgšanas grafiks bija atzīmēts kā **slēgts**, jums nebūs iespēja pievienot uzdevumus, rediģēt uzdevumus vai noņemtu uzdevumus.


