---
title: Vidējā svērtā ar fizisko vērtību un iezīmēšanu
description: Svērtais vidējais ir krājumu modelis, kas balstīts uz svērto vidējo principu, kur krājumu izejas plūsmas tiek novērtētas ar vienību vidējo vērtību, kas tiek saņemtas krājumā krājumu noslēgšanas periodā, pluss jebkādi rīcībā esošie krājumi no iepriekšējā perioda.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330230"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Vidējā svērtā ar fizisko vērtību un iezīmēšanu

[!include [banner](../includes/banner.md)]

Vidējais svērtais ir krājumu modelis, kura pamatā ir vidējais rādītājs, kas rodas, reizinot katru komponentu (krājuma darbību) ar koeficientu (izmaksu cenu), kas atspoguļo tā svarīgumu (daudzumu). Vēl viens veids, kā to pateikt, ir tas, ka vidējais svērtais ir krājumu modelis, kas piešķir izejas plūsmas darbību izmaksas, pamatojoties uz visu periodā saņemto krājumu vidējo vērtību, kā arī visus rīcībā esošos krājumus no iepriekšējā perioda.

Palaižot krājumu slēgšanu, izmantojot vidējo svērto krājumu modeli, ir divi veidi, kā var izveidot segšanu. Parasti visas ieejas plūsmas tiek nosegtas ar virtuālo izejas plūsmu, kurā ir kopējais saņemtais daudzums un vērtība. Šai virtuālajai izdošanai ir atbilstoša virtuālā saņemšana, no kuras tā tiek segta. Tādējādi visām izejas plūsmām ir vienādas vidējās izmaksas. Virtuālo izejas plūsmu un saņemšanu var uzskatīt par virtuālo pārsūtīšanu, kas tiek nosaukta par *vidējo svērto krājumu slēgšanas pārsūtīšanu*. Šo nosegšanas *metodi sauc par vidējo svērto apkopoto segšanu*. Ja paredzēta tikai viena saņemšana, ar to var segt visas izdošanas, un virtuālā pārsūtīšana netiks veikta. Šo norēķinu metodi sauc par *tiešo norēķinu*. Visi krājumi, kas ir rīcībā pēc krājumu slēgšanas veikšanas, tiek novērtēti pēc iepriekšējā perioda vidējā svērtā svara un iekļauti vidējā svērtajā aprēķinā nākamajā periodā.

Vidējo svērto principu var ignorēt, atzīmējot krājumu darbības tā, lai noteikta krājumu ieejas plūsma tiktu nosegta ar noteiktu izejas plūsmu. Periodiska krājumu slēgšana ir nepieciešama, ja izmantojat vidējo svērto krājumu modeli, lai izveidotu nosegšanas darbības un koriģētu izejas plūsmas vērtību atbilstoši vidēja svērtā principam. Līdz krājumu slēgšanas procesa palaišanai izejas plūsmas darbības tiek novērtētas pēc izpildes vidējā, kad notika fiziskie un finanšu atjauninājumi. Ja vien neizmantojat iezīmēšanu, izpildes vidējais tiek aprēķināts, kad tiek veikts fiziskais vai finanšu atjauninājums.

Svērtā vidējā krājumu izmaksu aprēķināšanas metode tiek aprēķināta ar šādu formulu:

- Svērtais vidējais = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = darbības daudzums  
P = darījuma cena

Segšanas ir krājuma slēgšanas iegrāmatojumi, kuri koriģē izdošanas pēc svērtā vidējā saskaņā ar slēgšanas datumu. Tālāk sniegtajos piemēros ir attēlota ietekme, ko rada vidējā svērtā izmantošana piecās dažādās konfigurācijās.

- Vidējā svērtā tiešā segšana **bez opcijas Iekļaut fizisko vērtību**
- Svērtā vidējā apkopotā segšana bez **opcijas Iekļaut fizisko vērtību**
- Vidējā svērtā tiešā segšana ar opciju **Iekļaut fizisko vērtību**
- Vidējā svērtā apkopotā segšana ar opciju **Iekļaut fizisko vērtību**
- Svērtais vidējais ar iezīmējumu

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Svērtā vidējā tieša segšana bez opcijas Iekļaut fizisko vērtību

Tiešās segšanas princips izveido nosegšanas darbības tieši starp ieejas plūsmām un izejas plūsmām, neveidojot papildu krājumu darbības. Sistēma izmanto šo tiešo norēķinu principu šādās situācijās:

- Šajā periodā ir iegrāmatota viena saņemšanas pavadzīme un viena vai vairākas izejas plūsmas.
- Periodā ir iegrāmatotas tikai izejas plūsmas, un krājumos ir rīcībā esošie krājumi no iepriekšējās slēgšanas.

Šajā piemērā nodotās **preces krājumu modeļu grupā** tiek notīrīta **izvēles rūtiņa Iekļaut fizisko vērtību**. Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas:

- 1.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 10 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 20,00 par katru.
- 3.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksu cenu USD 10.00 (finansiāli iegrāmatoto darbību izpildes vidējais rādītājs).
- 3.b Krājumu finanšu izejas plūsma daudzumam 1 ar izmaksu cenu USD 10.00 (finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 4.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar USD 10.00 katra izmaksām (finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 4.b Krājumu finanšu izejas plūsma par daudzumu 1 ar USD 10.00 katra izmaksām (finansiāli iegrāmatoto darbību izpildes vidējais rādītājs).
- 5.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar USD 10.00 katra izmaksām (finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 6\. Tiek veikta krājumu slēgšana. Pamatojoties uz vidējo svērto metodi, sistēma izmanto tiešās segšanas metodi, jo periodā finansiāli tiek atjaunināta tikai viena ieejas plūsma. Šajā piemērā tiek izveidota viena nosegšana no 1.b līdz 3.b klasei, bet otra – no 1.b līdz 4.b klasei. Korekcija netiek veikta, jo tekošais vidējais ir tāds pats kā vidējais svērtais.

Šajā diagrammā parādīta šī transakciju sērija ar sekām, ko rada vidējā svērtā krājumu modeļa un tiešās segšanas principa izvēle bez **opcijas Iekļaut fizisko vērtību**.

![WeightedAverage DS bez iekļaut fizisko vērtību.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Ieejas plūsmas krājumos tiek attēlotas ar vertikālām bultiņām virs ass.
- Izejas plūsmas no krājumiem tiek attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs diagrammas datums ir atdalīts ar plānu melnu vertikālu līniju. Datums ir atzīmēts diagrammas apakšā.
- Krājumu slēgšana tiek attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Svērtā vidējā apkopotā segšana bez opcijas Iekļaut fizisko vērtību

Ja periodā ir vairākas ieejas plūsmas, vidējā svērtā vērtība izmanto apkopotās nosegšanas principu, kur visas ieejas plūsmas slēgšanas periodā tiek apkopotas darbībā, ko sauc par *vidējo svērto krājumu slēgšanu*. Visas perioda ieejas plūsmas tiks nosegtas ar jaunizveidotās krājumu darbības izdošanu. Visas perioda izejas plūsmas tiks nosegtas pret jaunās krājumu darbības saņemšanu. Ja pēc krājumu slēgšanas ir atlikusi rīcībā esošo krājumu vērtība, rīcībā esošo krājumu vērtība tiek iekļauta vidējo svērto krājumu slēgšanas darbību ieejas plūsmā.

Turpmākajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli iegrāmatoto darbību izpildes vidējais rādītājs).
- 3.b Krājumu finanšu izejas plūsma daudzumam 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziskā izejas plūsma daudzumam 1 ar izmaksu cenu USD 23.00 (finansiāli grāmatoto darbību vidējais lielums).
- 7\. Tiek veikta krājumu slēgšana.
- 7.a Vidējā svērtā krājumu slēgšanas darbību finanšu izejas plūsma tiek izveidota, lai summētu visu krājumu finanšu ieejas plūsmu nosegšanas darbības.
  - Darbība 1b tiek nosegta par daudzumu 1 ar summu, kas nosegta ar USD 10.00.
  - Darbība 2b tiek nosegta par daudzumu 1 ar nosegto summu USD 22.00.
  - Darbība 5.b tiek nosegta par daudzumu 1 ar nosegto summu USD 30.00.
  - Darījums 7.a Tiek izveidots daudzumam 3 ar nosegto summu USD 62.00. Šī darbība kompensē to trīs ieejas plūsmas darbību summu, kas ir finansiāli atjauninātas periodā.
- 7.b Vidējā svērtā krājumu slēgšanas darbības finanšu ieejas plūsma tiek izveidota kā korespondējošais uz finansiāli iegrāmatotajām izejas plūsmām.
  - Darbība 3b tiek nosegta par daudzumu 1 ar samaksāto summu USD 20.67. Šī darbība tiek koriģēta ar USD 4.67, lai USD 16.00 sākotnējā vērtība būtu 20,67, kas ir perioda finansiāli iegrāmatoto darījumu vidējais svērtais rādītājs.
  - Darījums 7.b Tiek izveidots daudzumam 1 ar nosegto summu USD 20.67, lai kompensētu 3.b. Šī darbība kompensē vienas izejas plūsmas darbības summu, kas ir finansiāli atjaunināta periodā.

Šajā diagrammā parādīta šī darbību sērija ar sekām, ko rada vidējā svērtā krājumu modeļa izvēle un apkopotās nosegšanas princips bez **opcijas Iekļaut fizisko vērtību**.

![Vidējā svērtā SS bez iekļaut fizisko vērtību.](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Ieejas plūsmas krājumos tiek attēlotas ar vertikālām bultiņām virs ass.
- Izejas plūsmas no krājumiem tiek attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs diagrammas datums ir atdalīts ar plānu melnu vertikālu līniju. Datums ir atzīmēts diagrammas apakšā.
- Krājumu slēgšana tiek attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Svērtā vidējā tiešā segšana bez opcijas Iekļaut fizisko vērtību

Parametrs **Iekļaut fizisko vērtību** darbojas atšķirīgi ar vidējo svērto krājumu modeli nekā iepriekšējās preces versijās. Atlasot **opciju Iekļaut krājuma** fizisko vērtību **formā Krājumu modeļu grupa**, sistēma izmanto fiziski atjauninātas ieejas plūsmas, aprēķinot novērtēto izejas plūsmas izmaksu cenu vai izpildes vidējo vērtību. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu slēgšanas laikā finansiāli atjauninātās ieejas plūsmas tiks ņemtas vērā tikai svērtā vidējā aprēķinā.

Turpmākajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 10 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 20,00 par katru.
- 3.a Krājumu fiziskā izejas plūsma daudzumam 1 ar izmaksu cenu USD 15.00 (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 3.b Krājumu finanšu izejas plūsma daudzumam 1 ar izmaksu cenu USD 15.00 (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 4.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksām USD 15.00 katra (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 4.b Krājumu finanšu izejas plūsma par daudzumu 1 ar izmaksām, kas ir USD 15.00 katra (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 5.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksām USD 15.00 katra (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 6\. Tiek veikta krājumu slēgšana. Pamatojoties uz vidējo svērto metodi, sistēma izmanto tiešās segšanas metodi, jo periodā finansiāli tiek atjaunināta tikai viena ieejas plūsma. Šajā piemērā tiek izveidota viena nosegšana no 1.b līdz 3.b klasei, bet otra – no 1.b līdz 4.b klasei. Katrs darījums 3b un 4b tiek koriģēts par USD -5.00, lai vērtība USD 10.00.

Tālāk redzamajā diagrammā ir parādīta šī transakciju sērija ar sekām, ko rada vidējā svērtā krājumu modeļa izvēle un tiešās segšanas princips ar opciju **Iekļaut fizisko vērtību**.

![Vidējais svērtais DS ar iekļaut fizisko vērtību.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Ieejas plūsmas krājumos tiek attēlotas ar vertikālām bultiņām virs ass.
- Izejas plūsmas no krājumiem tiek attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs diagrammas datums ir atdalīts ar plānu melnu vertikālu līniju. Datums ir atzīmēts diagrammas apakšā.
- Krājumu slēgšana tiek attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Svērtā vidējā apkopotā segšana ar opciju Iekļaut fizisko vērtību

Parametrs **Iekļaut fizisko vērtību** darbojas atšķirīgi ar vidējo svērto vērtību nekā iepriekšējās versijās. **Atzīmējiet izvēles rūtiņu Iekļaut krājuma** fizisko vērtību **lapā Krājumu modeļu grupa**. Pēc tam sistēmā novērtēto izmaksu cenas vai pašreizējās vidējās vērtības aprēķinā tiek izmantotas fiziski atjauninātās ieejas plūsmas. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu slēgšanas laikā finansiāli atjauninātās ieejas plūsmas tiks ņemtas vērā tikai svērtā vidējā aprēķinā. Ja lietojat svērtā vidējā krājuma modeli, ieteicam veikt krājumu slēgšanu katru mēnesi. Šajā svērtā vidējā apkopotās segšanas piemērā krājumu modeļa grupa tiek atzīmēta, lai ietvertu fizisko vērtību.

Turpmākajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksu cenu USD 16.00 (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 3.b Krājumu finanšu izejas plūsma par daudzumu 1 ar izmaksu cenu USD 16.00 (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziskā izejas plūsma daudzumam 1 ar izmaksu cenu USD 23.67 (fiziski un finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 7\. Tiek veikta krājumu slēgšana.
- 7.a Vidējā svērtā krājumu slēgšanas darbību finanšu izejas plūsma tiek izveidota, lai summētu visu krājumu finanšu ieejas plūsmu nosegšanas darbības.
  - Darbība 1b tiek nosegta par daudzumu 1 ar summu, kas nosegta ar USD 10.00.
  - Darbība 2b tiek nosegta par daudzumu 1 ar nosegto summu USD 22.00.
  - Darbība 5.b tiek nosegta par daudzumu 1 ar nosegto summu USD 30.00.
  - Darījums 7.a Tiek izveidots daudzumam 3 ar nosegto summu USD 62.00.  
- 7.b Vidējā svērtā krājumu slēgšanas darbības finanšu ieejas plūsma tiek izveidota kā finansiāli slēgto izejas plūsmas darbību korespondējošais konts.
  - Darbība 3b tiek nosegta par daudzumu 1 ar samaksāto summu USD 20.67. Šī darbība tiek koriģēta ar USD 4.67, lai USD 16.00 sākotnējā vērtība būtu 20,67, kas ir perioda finansiāli iegrāmatoto darījumu vidējais svērtais rādītājs.
  - Darījums 7.b Tiek izveidots daudzumam 1 ar nosegto summu USD 20.67, lai kompensētu 3.b.

Šajā diagrammā parādīta šī darbību sērija ar sekām, ko rada vidējā svērtā krājumu modeļa izvēle un apkopotās nosegšanas princips bez **opcijas Iekļaut fizisko vērtību**.

![WeightedAverage SS ar iekļaut fizisko vērtību.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Ieejas plūsmas krājumos tiek attēlotas ar vertikālām bultiņām virs ass.
- Izejas plūsmas no krājumiem tiek attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs diagrammas datums ir atdalīts ar plānu melnu vertikālu līniju. Datums ir atzīmēts diagrammas apakšā.
- Krājumu slēgšana tiek attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-with-marking"></a>Svērtais vidējais ar iezīmējumu

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas.

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā šis ir steidzīgs pasūtījums, jums būs jāmaksā vairāk par šo preci, lai apkalpotu klienta pieprasījumu. Jums ir jānodrošina, ka šīs krājuma vienības izmaksas tiek ietvertas uzcenojumā vai pārdoto preču pašizmaksā (PPPI) šajā pārdošanas pasūtījuma rēķinā.

Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Piemēram, šis pārdošanas pasūtījuma dokuments tiek iezīmējot saistīts ar pirkšanas pasūtījumu pirms pavadzīmes vai rēķina grāmatošanas. Pēc tam krājuma PPPI ir USD 120,00, nevis pašreizējā kārtējo vidējo izmaksu cena šim krājumam. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena.

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Ieejas plūsmas transakcija tiek iezīmējot saistīta ar izejas plūsmas transakciju. Tad novērtēšanas metode, kas izvēlēta krājuma vienību modeļu grupai, tiks ignorēta, un sistēma nosegs šīs darbības vienu ar otru.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pirms transakcijas grāmatošanas. To var paveikt no pārdošanas pasūtījuma rindas, lapā **Pārdošanas pasūtījuma informācija**. Atvērtās saņemšanas darbības ir parādītas lapā **Iezīmēšana**.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu.

Turpmākajā grafikā ir attēlotas šādas darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli iegrāmatoto darbību izpildes vidējais rādītājs).
- 3.b Krājumu finanšu izejas plūsma daudzumam 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 3.c Krājumu finansiālā izdošana 3b ir atzīmēta krājumu finansiālai izdošanai 2b.
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziskā izejas plūsma daudzumam 1 ar izmaksu cenu USD 23.00 (finansiāli grāmatoto darbību vidējais lielums).
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz iezīmēšanas principu, kas izmanto svērtā vidējā metodi, iezīmētās darbības tiek nosegtas viena pret otru. Šajā piemērā 3b tiek nosegta pret 2b, un krājumu USD 6.00 tiek iegrāmatota 3b, lai iegūtu vērtību USD 22.00. Šajā piemērā netiek veiktas papildu nosegšanas, jo aizvēršana izveido segšanas tikai finansiāli atjauninātām darbībām.

Šī diagramma parāda šo darbību sēriju ar ietekmēm, izvēloties svērtā vidējā krājumu modeli ar atzīmēšanu.

![Vidējais svērtais ar apzīmējumu.](media/weighted-average-with-marking.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Ieejas plūsmas krājumos tiek attēlotas ar vertikālām bultiņām virs ass.
- Izejas plūsmas no krājumiem tiek attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs diagrammas datums ir atdalīts ar plānu melnu vertikālu līniju. Datums ir atzīmēts diagrammas apakšā.
- Krājumu slēgšana tiek attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
