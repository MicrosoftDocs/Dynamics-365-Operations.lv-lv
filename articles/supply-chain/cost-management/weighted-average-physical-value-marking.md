---
title: Vidējā svērtā ar fizisko vērtību un iezīmēšanu
description: Svērtais vidējais ir krājumu modelis, kas balstīts uz svērto vidējo principu, kur krājumu izejas plūsmas tiek novērtētas ar vienību vidējo vērtību, kas tiek saņemtas krājumā krājumu noslēgšanas periodā, pluss jebkādi rīcībā esošie krājumi no iepriekšējā perioda.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c80dcdc08432bb68478827c8763735e644aa4a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675268"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Vidējā svērtā ar fizisko vērtību un iezīmēšanu

[!include [banner](../includes/banner.md)]

Svērtais vidējais ir krājumu modelis, kas balstīts uz vidējo, ko rada katras sastāvdaļas (krājuma darbības) reizināšanas ar faktoru (izmaksu cenu), kas ataino tā svarīgumu (daudzumu). Cits veids, kā noteikt, ka svērtais vidējais ir krājumu modelis, kas piešķir izdošanas darbību izmaksas, pamatojoties uz visu perioda laikā saņemto krājumu vidējo vērtību plus jebkādus rīcībā esošos krājumus no iepriekšējā perioda.

Kad jūs palaidiet krājumu slēgšanu, izmantojot svērtā vidējā krājumu modeli, ir divi veidi, kā segšana var tikt izveidota. Parasti visas saņemšanas tiek segtas pret virtuālo izejas plūsmu, kas ietver kopējo saņemto daudzumu un vērtību. Šai virtuālajai izdošanai ir atbilstoša virtuālā saņemšana, no kuras tā tiek segta. Tādējādi visām izejas plūsmām ir vienādas vidējās izmaksas. Virtuālo izejas un ieejas plūsmu var redzēt, kā virtuālo pārsūtīšanu, ko sauc par novērtēto *vidējo krājumu slēgšanas pārsūtīšanu*. Šī segšanas metode tiek saukta par svērtā *vidējā apkopotu segšanu*. Ja paredzēta tikai viena saņemšana, ar to var segt visas izdošanas, un virtuālā pārsūtīšana netiks veikta. Šo nosegšanas metodi sauc par tiešu *nosegšanu*. Visi krājumi, kas ir rīcībā pēc krājumu slēgšanas, tiek novērtēti ar svērto vidējo vērtību no iepriekšējā perioda un iekļauti svērtā vidējā aprēķinā nākamajā periodā.

Varat ignorēt svērtā vidējā principu, iezīmējot krājumu darbības, lai noteikta krājuma saņemšana tiek segta pret noteiktu izdošanu. Ja izmantojat svērtā vidējā krājumu modeli, lai izveidotu segšanas un koriģētu izejas plūsmas vērtību atbilstoši svērtā vidējā principam, ir nepieciešama periodiska krājumu slēgšana. Kamēr nav veikti krājumu slēgšanas procesi, izdošanas darbības tiek vērtībās pēc tekošā vidējā, kad tika veikti fiziskie un finanšu atjauninājumi. Ja vien nelieto atzīmēto, aprēķinātais vidējais tiek aprēķināts, veicot fiziskās vai finanšu atjaunināšanas.

Svērtā vidējā krājumu izmaksu aprēķināšanas metode tiek aprēķināta ar šādu formulu:

- Svērtais vidējais = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = darbības daudzums  
P = darbības cena

Segšanas ir krājuma slēgšanas iegrāmatojumi, kuri koriģē izdošanas pēc svērtā vidējā saskaņā ar slēgšanas datumu. Tālāk sniegtajos piemēros ir attēlota ietekme, ko rada vidējā svērtā izmantošana piecās dažādās konfigurācijās.

- Svērtā vidējā tieša segšana bez opcijas **Iekļaut fizisko** vērtību
- Svērtā vidējā apkopotā segšana bez opcijas **Iekļaut fizisko** vērtību
- Svērtā vidējā tieša segšana ar opciju **Iekļaut fizisko** vērtību
- Svērtā vidējā apkopotā segšana ar opciju **Iekļaut fizisko** vērtību
- Svērtais vidējais ar iezīmējumu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Svērtā vidējā tieša segšana bez opcijas Iekļaut fizisko vērtību

Tiešās nosegšanas princips izveido nosegšanu tieši starp ieejas un izejas plūsmām, neizveidojot papildu krājumu darbības. Sistēma izmanto šo tiešās nosegšanas principu šādās situācijās:

- Perioda laikā tika iegrāmatota viena saņemšana un viena vai vairākas izejas plūsmas.
- Perioda laikā tika iegrāmatotas tikai izejas plūsmas un rīcībā esošie krājumi no iepriekšējās slēgšanas.

Šajā piemērā izlaistajām **precei** krājumu modeļu grupā ir notīrīta **izvēles rūtiņa Iekļaut** fizisko vērtību. Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas:

- 1.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 10 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 20,00 par katru.
- 3.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 10.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 ar izmaksu cenu USD 10.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 4.a Krājumu fiziska izdošana daudzumam 1, kas maksā USD 10.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 4.b Krājumu finansiāla izdošana daudzumam 1, kas maksā USD 10.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 5.a Krājumu fiziska izdošana daudzumam 1, kas maksā USD 10.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 6\. Tiek veikta krājumu slēgšana. Balstoties uz svērtā vidējā metodi, sistēma izmanto tiešās segšanas metodi, jo šajā periodā finansiāli tiek atjaunināta tikai viena saņemšana. Šajā piemērā viena segšana tiek izveidota starp 1b un 3b, un otru starp 1b un 4b. Netiek veikts nekāds koriģēšana, jo tekošais vidējais ir tāds pats kā svērtais vidējais.

Tālāk redzamajā diagrammā ir atspoguļota darbību sērija ar ietekmēm, izvēloties svērto vidējo krājumu modeli un tiešu segšanas principu bez **opcijas Iekļaut fizisko** vērtību.

![WeightedAverage DS bez fizisko vērtību iekļaujiet.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Svērtā vidējā apkopotā segšana bez opcijas Iekļaut fizisko vērtību

Ja periodā ir vairākas saņemšanas, svērtais vidējais izmanto apkopotu segšanas *principu, kur visas ieejas plūsmas slēgšanas periodā tiek apkopotas darbībā, kas tiek saukta par svērtā vidējā krājumu slēgšanu*. Visas ieejas plūsmas periodam tiks segtas attiecībā pret jauni izveidoto krājumu darbību izejas plūsmu. Visas izejas plūsmas periodam tiks segtas attiecībā pret jauno krājumu darbības saņemšanu. Ja rīcībā esošo krājumu vērtība paliek pēc krājumu slēgšanas, rīcībā esošo krājumu vērtība tiek iekļauta svērtā vidējā krājumu slēgšanas darbību saņemšanas darbībā.

Tālāk sniegtajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 23.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 7\. Tiek veikta krājumu slēgšana.
- 7.a Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darījumu finanšu izejas plūsma, lai summētu visu krājumu finansiālo ieejas plūsmu segšanas.
  - Darbība 1b nosegta daudzumam 1 ar summu, kas nosegta USD 10.00.
  - Darbība 2b tiek nosegta par daudzumu 1 ar summu, kas nosegta USD 22.00.
  - Darbība 5b ir nosegta daudzumam 1 ar summu, kas nosegta USD 30.00.
  - Darbība 7a. Izveidots daudzumam 3 ar summu, kas nosegta USD 62.00. Šī darbība korespondē trīs ieejas plūsmas darbību summu, kas perioda laikā ir finansiāli atjauninātas.
- 7.b Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darījumu finanšu ieejas plūsma, kā finansiāli grāmatoto plūsmu korespondējošais konts.
  - Darbība 3b tiek nosegta par daudzumu 1 ar summu, kas nosegta USD 20.67. Šī darbība tiek koriģēta ar USD 4.67, lai vērtība laukā USD 16.00 20,67, kas ir finansiāli grāmatoto darbību sākotnējā vērtība periodam.
  - Darbība 7b. Izveidots daudzumam 1 ar summu, kas nosegta par USD 20.67, lai kompensētu 3b. Šī darbība korespondē ar vienas izdošanas darbības summu, kas ir finansiāli atjaunināta periodā.

Tālāk redzamajā diagrammā ir atspoguļota darbību sērija ar ietekmēm, izvēloties svērto vidējo krājumu modeli un apkopoto segšanas principu bez **opcijas Iekļaut fizisko** vērtību.

![Vidējā svērtā bez fizisko vērtību svērtās vērtības.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Svērtā vidējā tiešā segšana bez opcijas Iekļaut fizisko vērtību

Parametrs **Iekļaut fizisko** vērtību darbojas atšķirīgi ar svērtā vidējā krājumu modeli nekā iepriekšējās produkta versijās. Atlasot opciju **Iekļaut** **fizisko** vērtību krājumam formā Krājumu modeļu grupa, sistēma izmantos fiziski atjauninātas saņemšanas, aprēķinot novērtēto izejas plūsmas izmaksu cenu vai palaižot vidējo. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu slēgšanas laikā finansiāli atjauninātās ieejas plūsmas tiks ņemtas vērā tikai svērtā vidējā aprēķinā.

Tālāk sniegtajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 10 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 20,00 par katru.
- 3.a Krājumu fiziska izdošana daudzumam 1 ar izmaksu cenu 0USD 15.00 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 par izmaksu cenu USD 15.00 (fiziski vai finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 4.a Krājumu fiziskā izdošana daudzumam 1, kas maksā USD 15.00 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 4.b Krājumu finansiāla izdošana daudzumam 1, kas maksā USD 15.00 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 5.a Krājumu fiziskā izdošana daudzumam 1, kas maksā USD 15.00 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 6\. Tiek veikta krājumu slēgšana. Balstoties uz svērtā vidējā metodi, sistēma izmanto tiešās segšanas metodi, jo šajā periodā finansiāli tiek atjaunināta tikai viena saņemšana. Šajā piemērā viena segšana tiek izveidota starp 1b un 3b, un otru starp 1b un 4b. Darbība 3b un 4b katrs tiek koriģēti par USD -5,00, lai piesaistītu vērtību USD 10.00.

Šī diagramma parāda šo darbību sēriju ar ietekmēm, izvēloties svērto vidējo krājumu modeli un tiešu segšanas principu **ar opciju Iekļaut fizisko** vērtību.

![Vidējā svērtā summa ar fizisko vērtību iekļautu.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Svērtā vidējā apkopotā segšana ar opciju Iekļaut fizisko vērtību

Parametrs **Iekļaut fizisko** vērtību darbojas atšķirīgi ar svērto vidējo nekā iepriekšējās versijās. Atzīmējiet **izvēles rūtiņu** Iekļaut fizisko vērtību krājumam krājumu **modeļu grupas** lapā. Pēc tam sistēmā novērtēto izmaksu cenas vai pašreizējās vidējās vērtības aprēķinā tiek izmantotas fiziski atjauninātās ieejas plūsmas. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu slēgšanas laikā finansiāli atjauninātās ieejas plūsmas tiks ņemtas vērā tikai svērtā vidējā aprēķinā. Ja lietojat svērtā vidējā krājuma modeli, ieteicam veikt krājumu slēgšanu katru mēnesi. Šajā svērtā vidējā apkopotās segšanas piemērā krājumu modeļa grupa tiek atzīmēta, lai ietvertu fizisko vērtību.

Tālāk sniegtajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska izdošana daudzumam 1 ar izmaksu cenu 0USD 16.00 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 par izmaksu cenu USD 16.00 (fiziski vai finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska izdošana daudzumam 1 ar izmaksu cenu 0USD 23.67 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 7\. Tiek veikta krājumu slēgšana.
- 7.a Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darījumu finanšu izejas plūsma, lai summētu visu krājumu finansiālo ieejas plūsmu segšanas.
  - Darbība 1b nosegta daudzumam 1 ar summu, kas nosegta USD 10.00.
  - Darbība 2b tiek nosegta par daudzumu 1 ar summu, kas nosegta USD 22.00.
  - Darbība 5b ir nosegta daudzumam 1 ar summu, kas nosegta USD 30.00.
  - Darbība 7a. Izveidots daudzumam 3 ar summu, kas nosegta USD 62.00.  
- 7.b Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darbības finanšu ieejas plūsma, kā finansiāli slēgto izdošanas darbību korespondējošais konts.
  - Darbība 3b tiek nosegta par daudzumu 1 ar summu, kas nosegta USD 20.67. Šī darbība tiek koriģēta ar USD 4.67, lai vērtība laukā USD 16.00 20,67, kas ir finansiāli grāmatoto darbību sākotnējā vērtība periodam.
  - Darbība 7b. Izveidots daudzumam 1 ar summu, kas nosegta par USD 20.67, lai kompensētu 3b.

Tālāk redzamajā diagrammā ir atspoguļota darbību sērija ar ietekmēm, izvēloties svērto vidējo krājumu modeli un apkopoto segšanas principu bez **opcijas Iekļaut fizisko** vērtību.

![WeightedAverage SS ar fizisko vērtību iekļautu.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-with-marking"></a>Svērtais vidējais ar iezīmējumu

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas.

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā tas ir steidzams pasūtījums, jums būs par šo krājumu jāmaksā vairāk, lai sniegtu klienta pieprasījumu. Jums ir jānodrošina, ka šīs krājuma vienības izmaksas tiek ietvertas uzcenojumā vai pārdoto preču pašizmaksā (PPPI) šajā pārdošanas pasūtījuma rēķinā.

Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Piemēram, šis pārdošanas pasūtījuma dokuments tiek iezīmējot saistīts ar pirkšanas pasūtījumu pirms pavadzīmes vai rēķina grāmatošanas. Pēc tam krājuma PPPI ir USD 120,00, nevis pašreizējā kārtējo vidējo izmaksu cena šim krājumam. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena.

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Ieejas plūsmas transakcija tiek iezīmējot saistīta ar izejas plūsmas transakciju. Tad novērtēšanas metode, kas izvēlēta krājuma vienību modeļu grupai, tiks ignorēta, un sistēma nosegs šīs darbības vienu ar otru.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pirms transakcijas grāmatošanas. To var paveikt no pārdošanas pasūtījuma rindas, lapā **Pārdošanas pasūtījuma informācija**. Atvērtās saņemšanas darbības ir parādītas lapā **Iezīmēšana**.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu.

Tālāk sniegtajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3c. Krājumu finansiālā izdošana 3b ir atzīmēta krājumu finansiālai izdošanai 2b.
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 23.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz iezīmēšanas principu, kas izmanto svērtā vidējā metodi, iezīmētās darbības tiek nosegtas viena pret otru. Šajā piemērā 3b tiek nosegta pret 2b, un korekcija USD 6.00 iegrāmatota 3b, lai vērtība ienestu USD 22.00. Šajā piemērā netiek veiktas papildu nosegšanas, jo aizvēršana izveido segšanas tikai finansiāli atjauninātām darbībām.

Šī diagramma parāda šo darbību sēriju ar ietekmēm, izvēloties svērtā vidējā krājumu modeli ar atzīmēšanu.

![Vidējais svērtais ar apzīmējumu.](media/weighted-average-with-marking.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
