---
title: "Svērtais vidējais ar fizisko vērtību un iezīmēšanu"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: cdbca6d9c71c901a1f4e7a8e5a2f9be1d3efb355
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="weighted-average-with-physical-value-and-marking"></a>Svērtais vidējais ar fizisko vērtību un iezīmēšanu

[!include[banner](../includes/banner.md)]




Kad tiek veikta krājumu slēgšana, visi saņemšanas darījumi tiek segti pret virtuālajiem izdošanas darījumiem, kuri aptver kopējo saņemto daudzumu un vērtību. Šai virtuālajai izdošanai ir atbilstoša virtuālā saņemšana, no kuras tā tiek segta. Tādējādi visām izejas plūsmām ir vienādas vidējās izmaksas. Virtuālo izejas plūsmu un ieejas plūsmu var uzskatīt par virtuālu pārsūtīšanu, kas tiek saukta par svērtā vidējā krājumu slēgšanas pārsūtīšanu.

Ja paredzēta tikai viena saņemšana, ar to var segt visas izdošanas, un virtuālā pārsūtīšana netiks veikta. 

Ja lietojat svērto vidējo, varat iezīmēt krājumu transakcijas tā, lai atsevišķa krājuma ieejas plūsma tiktu segta ar atsevišķu izejas plūsmu, nevis izmantojot svērtā vidējā kārtulu. 

Ja lietojat svērtā vidējā krājuma modeli, ieteicam veikt krājumu slēgšanu katru mēnesi. 

Svērtā vidējā krājumu izmaksu aprēķināšanas metode tiek aprēķināta ar šādu formulu:
-   Svērtais vidējais = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Krājumu transakcijas, kas rada krājumu izejas plūsmas. Tostarp pārdošanas pasūtījumi, krājumu žurnāli un ražošanas pasūtījumi, tiek apstrādāti ar novērtēto izmaksu cenu grāmatošanas datumā. Paredzētā izmaksu cena tiek arī saukta par esošo vidējo. Krājumu slēgšanas laikā sistēma analizē krājumu transakcijas iepriekšējiem un pašreizējiem periodiem un nosaka, kurš no tālāk norādītajiem slēgšanas principiem ir jāizmanto.
-   Tieša segšana
-   Apkopota segšana

Segšanas ir krājuma slēgšanas iegrāmatojumi, kuri koriģē izdošanas pēc svērtā vidējā saskaņā ar slēgšanas datumu. Tālāk sniegtajos piemēros ir attēlota ietekme, ko rada vidējā svērtā izmantošana piecās dažādās konfigurācijās.
-   Svērtā vidējā tiešā segšana, neizmantojot opciju Iekļaut fizisko vērtību
-   Svērtā vidējā apkopotā segšana bez opcijas Iekļaut fizisko vērtību
-   Svērtā vidējā tiešā segšana bez opcijas Iekļaut fizisko vērtību
-   Svērtā vidējā apkopotā segšana ar opciju Iekļaut fizisko vērtību
-   Svērtais vidējais ar iezīmējumu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Svērtā vidējā tieša segšana bez opcijas Iekļaut fizisko vērtību
Tiešais segšanas princips ir tas pats, kas tiek izmantots svērtajam vidējam iepriekšējās versijās. Sistēma veiks tiešo nosegšanu starp saņemšanas un izdošanas darījumiem. Sistēma izmanto šo tiešās nosegšanas principu noteiktās īpašās situācijās:
-   Perioda laikā tika iegrāmatota viena saņemšana un viena vai vairākas izdošanas
-   Perioda laikā tika iegrāmatotas tikai izdošanas un rīcībā esošie krājumi no iepriekšējas slēgšanas

Turpmākajās sadaļās aprakstītajā scenārijā ir iegrāmatotas finansiāli atjauninātas ieejas un izejas plūsmas. Krājuma slēgšanas laikā sistēma ieejas plūsmu sedz tieši ar izejas plūsmu, tādēļ krājumu izmaksu cenas koriģēšana nav nepieciešama. Diagrammā ir redzamas tālāk norādītās transakcijas.
-   1.a Atjaunota krājumu fiziskā ieejas plūsma daudzumam - 5 par USD 10,00 katrs
-   1.b Atjaunota krājumu finansiālā ieejas plūsma daudzumam - 5 par USD 10,00 katrs
-   2.a Atjaunota krājumu fiziskā izejas plūsma daudzumam - 2 par USD 10,00 katrs
-   2.b Atjaunota krājumu finansiālā izejas plūsma daudzumam - 2 par USD 10,00 katrs
-   3. Tiek veikta krājumu slēgšana, izmantojot tiešās segšanas metodi, lai segtu krājumu finanšu ieejas plūsmu ar krājumu finanšu izejas plūsmu.

Tālāk esošajā diagrammā ir atspoguļota šī transakciju sērija, kā arī ietekme, ko rada svērtā vidējā krājumu modeļa un tiešās segšanas principa izvēlēšanās, neizmantojot opciju Iekļaut fizisko vērtību. 

![WeightedAverage DS bez fizisko vērtību iekļaušanas](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Diagrammas apzīmējumi**
-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība bez iekavām norāda, ka krājuma darbība tika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secīgu identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti Krājuma slēgšana.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Svērtā vidējā apkopotā segšana bez opcijas Iekļaut fizisko vērtību
Svērtā vidējā metodei tiek izmantots segšanas princips, ka visas ieejas plūsmas slēgšanas periodā tiek apkopotas vienā transakcijā, kas tiek saukta par svērtā vidējā krājumu slēgšanu. Visas ieejas plūsmas periodam tiks segtas attiecībā pret jauni izveidoto krājumu pārsūtīšanas darbības izejas plūsmu. Visas izejas plūsmas periodam tiks segtas attiecībā pret jauno krājumu pārsūtīšanas darbības ieejas plūsmu. Ja rīcībā esošie krājumi ir pozitīvi pēc krājumu slēgšanas, rīcībā esošo krājumu un krājumu vērtības tiek summētas jaunā krājuma pārsūtīšanas darbībā (saņemšana). Ja rīcībā esošie krājumi ir negatīvi pēc krājumu slēgšanas, rīcībā esošie krājumi un krājuma vērtība veido atsevišķu nepilni segto krājumu summu. Turpmāk redzamajā scenārijā ir iegrāmatotas vairākas finansiāli atjaunotas ieejas plūsmas un viena izejas plūsma. 

Krājumu noslēgšanas laikā sistēma izveido un iegrāmato apkopotu krājumu pārsūtīšanas transakciju, un visas ieejas plūsmas šim periodam sedz ar apkopoto krājumu pārsūtīšanas izejas plūsmas transakciju. Visas izejas plūsmas, kas iegrāmatotas periodam, tiks segtas attiecībā pret apkopoto krājumu pārsūtīšanas ieejas plūsmas darbību. Svērtais vidējais ir aprēķināts, kā USD 15,00. Izejas plūsma sākotnēji tika iegrāmatota, norādot novērtēto izmaksu cenu USD 14,67. Tāpēc izejas plūsmai tiks grāmatota korekcija ar negatīvu vērtību USD 0,33. Krājumu noslēgšanas datumā rīcībā esošie krājumi ir 3 gabali ar vērtību USD 45,00. 

Tālāk apskatāmajā grafikā ir attēlotas šādas darbības:
-   1.a Fiziska krājuma saņemšana, kas atjaunināta uz 2 vienībām par cenu USD 11,00 katra.
-   1.b Finansiāla krājuma saņemšana, kas atjaunināta uz 2 vienībām par cenu USD 14,00 katra.
-   2.a Fiziska krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 12,00 katra.
-   2.b Atjaunota krājumu finansiālā ieejas plūsma daudzumam - 1 par USD 16,00 katrs
-   3.a Atjaunota krājumu fiziskā izejas plūsma daudzumam - 1 par USD 14,67 katrs (esošais vidējais)
-   3.b Atjaunota krājumu fiziskā izejas plūsma daudzumam - 1 par USD 14,67 katrs (esošais vidējais)
-   4.a Fiziska krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 14,00 katra.
-   4.b Atjaunota krājumu finansiālā ieejas plūsma daudzumam - 1 par USD 16,00 katrs
-   5. Tiek veikta krājumu slēgšana.
-   6.a “Svērtā vidējā krājumu noslēgšanas darbības” finanšu izejas plūsma tiek izveidota, lai summētu visu krājumu finansiālo ieejas plūsmu segšanas.
-   6b. “Svērtā vidējā krājumu noslēgšanas darbības” finansiālais pārskats tiek izveidots, kā korespondējošs darbībai 5a.

Tālāk esošajā diagrammā ir atspoguļota šī transakciju sērija, kā arī ietekme, ko rada svērtā vidējā krājumu modeļa un apkopotās segšanas principa izvēlēšanās, neizmantojot opciju Iekļaut fizisko vērtību. 

![Vidējā svērtā apkopotā apmaksa ar fizisko vērtību iekļaušanu](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Diagrammas apzīmējumi**
-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība bez iekavām norāda, ka krājuma darbība tika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secīgu identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti Krājuma slēgšana.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.
-   Sarkanas bultas attēlo saņemšanas darbības, kuras ir segtas ar sistēmas veidotajām izdošanas darbībām.
-   Zaļas bultas attēlo korespondējošās sistēmas veidoto saņemšanas darbību, ar kuru tika segtas iegrāmatotas izdošanas darbība

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Svērtā vidējā tiešā segšana bez opcijas Iekļaut fizisko vērtību
Parametrs Iekļaut fizisko vērtību ar svērtā vidējā krājumu modeli darbojas atšķirīgi nekā iepriekšējās produkta versijās. Veidlapā Krājumu modeļu grupa atzīmējiet krājumam izvēles rūtiņu Iekļaut fizisko vērtību. Pēc tam sistēmā novērtēto izmaksu cenas vai pašreizējās vidējās vērtības aprēķināšanai tiek izmantotas fiziski atjauninātās ieejas plūsmas. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu slēgšanas laikā finansiāli atjauninātās ieejas plūsmas tiks ņemtas vērā tikai svērtā vidējā aprēķinā. Ja lietojat svērtā vidējā krājuma modeli, ieteicam veikt krājumu slēgšanu katru mēnesi. Šajā svērtā vidējā tiešās segšanas izmantošanas piemērā krājumu modeļu grupai ir atzīmēta opcija Iekļaut fizisko vērtību. 

Tālāk apskatāmajā grafikā ir attēlotas šādas darbības:
-   1.a Fiziska krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 11,00 katra.
-   1.b Finansiāla krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 10,00 katra.
-   2.a Fiziska krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 15,00 katra.
-   3.a Atjaunota krājumu fiziskā izejas plūsma daudzumam - 1 par USD 12,50 katrs (esošās vidējās izmaksas no tā brīža, kad fiziskās ieejas plūsmas vērtība tiek ņemta vērā).
-   3.b Atjaunota krājumu finansiālā izejas plūsma daudzumam - 1 par USD 12,50 katrs (esošās vidējās izmaksas no tā brīža, kad fiziskās ieejas plūsmas vērtība tiek ņemta vērā).
-   4. Tiek veikta krājumu slēgšana. Krājumu noslēgšanas laikā sistēma ignorē visas krājumu transakcijas, kas ir atjaunotas tikai fiziski. Tā vietā tiks izmantots tiešais segšanas princips, jo eksistē tikai viena finansiālā ieejas plūsma. USD 2,50 koriģējums tiks iegrāmatots krājumu darbībai, kas finansiāli ir izsniegta, kā krājumu noslēgšanas datums. Pēc krājumu noslēgšanas rīcībā esošie krājumi būs daudzumā - 1 par USD 15,00 lielu esošo vidējo izmaksu cenu.

Tālāk esošajā diagrammā ir atspoguļota šī transakciju sērija, kā arī ietekme, ko rada svērtā vidējā krājumu modeļa un tiešās segšanas principa izvēlēšanās, izmantojot opciju Iekļaut fizisko vērtību. 

![Vidējā svērtā tiešā apmaksa ar fizisko vērtību iekļaušanu](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Diagrammas apzīmējumi**
-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība bez iekavām norāda, ka krājuma darbība tika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secīgu identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti Krājuma slēgšana.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Svērtā vidējā apkopotā segšana ar opciju Iekļaut fizisko vērtību
Parametrs Iekļaut fizisko vērtību ar svērto vidējo darbojas atšķirīgi nekā iepriekšējās versijās. Lapā Krājumu modeļu grupa atzīmējiet krājumam izvēles rūtiņu Iekļaut fizisko vērtību. Pēc tam sistēmā novērtēto izmaksu cenas vai pašreizējās vidējās vērtības aprēķinā tiek izmantotas fiziski atjauninātās ieejas plūsmas. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu noslēgšanas laikā finansiāli atjaunotās ieejas plūsmas būs tikai ņemtas vērā svērtā vidējā aprēķinā. Ja lietojat svērtā vidējā krājuma modeli, ieteicam veikt krājumu slēgšanu katru mēnesi. Šajā svērtā vidējā apkopotās segšanas piemērā krājumu modeļa grupa tiek atzīmēta, lai ietvertu fizisko vērtību. 

Tālāk apskatāmajā grafikā ir attēlotas šādas darbības:
-   1.a Fiziska krājuma saņemšana, kas atjaunināta uz 2 vienībām par cenu USD 11,00 katra.
-   1.b Finansiāla krājuma saņemšana, kas atjaunināta uz 2 vienībām par cenu USD 14,00 katra.
-   2. Fiziska krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 10,00 katra.
-   3.a Fiziska krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 12,00 katra.
-   3.b Atjaunota krājumu finansiālā ieejas plūsma daudzumam - 1 par USD 16,00 katrs
-   4.a Atjaunota krājumu fiziskā izejas plūsma daudzumam - 1 par USD 13,50 katrs (esošās vidējās izmaksas no tā brīža, kad fiziskās ieejas plūsmas vērtība tiek ņemta vērā).
-   4.b Atjaunota krājumu finansiālā izejas plūsma daudzumam - 1 par USD 13,50 katrs (esošās vidējās izmaksas no tā brīža, kad fiziskās ieejas plūsmas vērtība tiek ņemta vērā).
-   5.a Fiziska krājuma saņemšana, kas atjaunināta uz 1 vienībām par cenu USD 14,00 katra.
-   5.b Atjaunota krājumu finansiālā ieejas plūsma daudzumam - 1 par USD 16,00 katrs
-   6. Tiek veikta krājumu slēgšana. Krājumu noslēgšanas laikā sistēma ignorē visas krājumu transakcijas, kas ir atjaunotas tikai fiziski. Tiks izmantots apkopotais segšanas princips, jo eksistē tikai viena finansiālā ieejas plūsma. USD 1,50 koriģējums tiks iegrāmatots krājumu darbībai, kas finansiāli ir izsniegta, kā krājumu noslēgšanas datums. Pēc krājumu noslēgšanas rīcībā esošie krājumi būs daudzumā - 3 par USD 15,00 lielu esošo vidējo izmaksu cenu.
-   7.a “Svērtā vidējā krājumu noslēgšanas darbības” finanšu izejas plūsma tiek izveidota, lai summētu visu krājumu finansiālo ieejas plūsmu segšanas.
-   7.b “Svērtā vidējā krājumu noslēgšanas darbības” finansiālais pārskats tiek izveidots, kā korespondējošs darbībai 5a.

Tālāk esošajā diagrammā ir atspoguļota šī transakciju sērija, kā arī ietekme, ko rada svērtā vidējā krājumu modeļa un apkopotās segšanas principa izvēlēšanās, neizmantojot opciju Iekļaut fizisko vērtību. 

![WeightedAverage SS ar fizisko vērtību iekļaušanu](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Diagrammas apzīmējumi**
-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība bez iekavām norāda, ka krājuma darbība tika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, 1a. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti Krājuma slēgšana.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.
-   Sarkanas bultas attēlo saņemšanas darbības, kuras ir segtas ar sistēmas veidotajām izdošanas darbībām.
-   Zaļas bultas attēlo korespondējošās sistēmas veidoto saņemšanas darbību, ar kuru tika segtas iegrāmatotas izdošanas darbība

## <a name="weighted-average-with-marking"></a>Svērtais vidējais ar iezīmējumu
Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. 

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā tas ir steidzams pasūtījums, lai izpildītu debitora pieprasījumu, par šo krājumu ir jāmaksā vairāk. Jums ir jānodrošina, ka šīs krājuma vienības izmaksas tiek ietvertas uzcenojumā vai pārdoto preču pašizmaksā (PPPI) šajā pārdošanas pasūtījuma rēķinā. 

Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Piemēram, šis pārdošanas pasūtījuma dokuments tiek iezīmējot saistīts ar pirkšanas pasūtījumu pirms pavadzīmes vai rēķina grāmatošanas. Pēc tam krājuma PPPI ir USD 120,00, nevis pašreizējā kārtējo vidējo izmaksu cena šim krājumam. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena. 

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas. 

Ieejas plūsmas transakcija tiek iezīmējot saistīta ar izejas plūsmas transakciju. Pēc tam tiek ignorēta krājumu modeļu grupai atlasītā novērtēšanas metode un sistēmā šīs transakcijas tiek segtas viena ar otru. 

Varat atzīmēt saņemšanas darbībai paredzēto izdošanas darbību pirms darbība tiek grāmatota. Varat to izdarīt pārdošanas pasūtījuma rindā lapā Pārdošanas pasūtījuma informācija. Atvērtās ieejas plūsmas transakcijas varat skatīt lapā Iezīmēšana. 

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu. 

Tālāk apskatāmajā grafikā ir attēlotas šādas darbības:
-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 20,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   4.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 30,00 katrs.
-   5.a Krājumu fiziskā izejas plūsma daudzumam - 1 par USD 21,25 (finansiāli un fizikāli atjaunotu darbību esošais vidējais).
-   5.b Krājumu finansiāla izdošana ar daudzumu 1 tiek nozīmēta krājumu ieejas plūsmai 2b pirms darbība tiek iegrāmatota. Šī transakcija tik grāmatota, norādot izmaksu cenu USD 20,00.
-   6.a Krājuma fiziska saņemšana par daudzumu 1 par summu USD 21,25 katrs.
-   7. Tiek veikta krājumu noslēgšana. Tā kā finansiāli atjaunotā darbība ir atzīmēta ar esoši ieejas plūsmu, šīs darbības tiek segtas viena ar otru, un netiek veikts nekāds koriģējums.

Jauna pašreizēja vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50. 

Turpmāk redzamajā diagrammā ir atspoguļota darbību sērija ar ietekmēm, izvēloties svērtā vidējā krājumu modeli ar atzīmēšanu. 

![Vidējais svērtais ar apzīmējumu](./media/weightedaveragewithmarking.gif) 

**Diagrammas apzīmējumi**
-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība bez iekavām norāda, ka krājuma darbība tika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secīgu identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti Krājuma slēgšana.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.






