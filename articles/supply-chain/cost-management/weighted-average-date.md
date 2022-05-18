---
title: Svērtais vidējais datums ar iekļaut fizisko vērtību un iezīmēšanu
description: Svērtais vidējais datums ir krājumu modelis, kas balstīts uz svērto vidējo principu, kur izsniegšanas no krājumiem tiek vērtētas pie vidējās krājumu vērtības, kas inventarizācijā saņemta katrai atsevišķai dienai krājumu slēgšanas periodā.
author: JennySong-SH
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1497cb08f4cc5a455c832b9bf125c309cd90aa3d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672127"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Svērtais vidējais datums ar iekļaut fizisko vērtību un iezīmēšanu

[!include [banner](../includes/banner.md)]

*Svērtais* vidējais datums ir krājumu modelis, kas ir balstīts uz vidējo, kas tiek aprēķināts, reizinot katru komponentu (krājuma darbību) ar koeficientu (izmaksu cenu), kas atspoguļo tā svarīgumu (daudzumu) katrā perioda dienā. Citiem vārdiem sakot, šis krājumu modelis piešķir izdošanas darbību izmaksas, pamatojoties uz visu katru dienu saņemto krājumu vidējo vērtību plus jebkādus rīcībā esošos krājumus no iepriekšējās dienas.

Kad jūs palaidiet krājumu slēgšanu, izmantojot svērtā vidējā datuma krājumu modeli, divas metodes var izmantot segšanai. Parasti visas saņemšanas tiek segtas pret virtuālo izejas plūsmu, kas ietver kopējo saņemto daudzumu un vērtību. Šai virtuālajai izejas plūsmai ir atbilstoša virtuālā ieejas plūsma, no kuras izejas plūsmas tiek segtas. Šādā veidā visas izejas plūsmas katru dienu iegūst tās pašas vidējās izmaksas. Virtuālā izdošana un virtuālā saņemšana var tikt uzskatīta par virtuālo pārsūtīšanu. Šis virtuālais pārsūtījumos tiek saukts par svērto *vidējo krājumu noslēgšanas pārsūtījumu*. Tāpēc šī segšanas metode ir pazīstama kā svērtā *vidējā apkopota segšana*. Ja ir tikai viena saņemšana, ar to var segt visas izejas plūsmas, un virtuālā pārsūtīšana netiek izveidota. Šo nosegšanas metodi sauc par tiešu *nosegšanu*. Visi krājumi, kas ir rīcībā pēc krājumu slēgšanas, tiek novērtēti ar svērto vidējo no iepriekšējā perioda pēdējās dienas un iekļauti novērtētā vidējā datuma aprēķinā nākamajā periodā.

Varat ignorēt svērtā vidējā datuma principu, iezīmējot krājumu darbības, lai noteikta krājuma saņemšana tiek segta pret noteiktu izdošanu. Ja izmantojat svērtā vidējā datuma krājumu modeli, lai izveidotu segšanas un koriģētu izdošanas vērtību atbilstoši svērtā vidējā datuma principam, ir nepieciešama periodiska krājumu slēgšana. Kamēr nav palaista krājumu slēgšana, izdošanas darbības tiek novērtēts pie tekošā vidējā līmeņa, kad tika veikti fiziskie un finanšu atjauninājumi. Ja vien nelieto atzīmēto, aprēķinātais vidējais tiek aprēķināts, veicot fiziskās vai finanšu atjaunināšanas.

Novērtētā vidējā datuma krājumu izmaksu aprēķināšanas metode tiek aprēķināta, izmantojot sekojošo formulu katru dienu:

*Izmaksas* = \[ (*Qb*<sub>*·*</sub> × *Pb*<sub>*·*</sub>) + &#x2211;<sub>*n*</sub>(*Qn*<sub>*·*</sub> × *Pn*<sub>*·*</sub>)\] ÷ (*Qb*<sub>*·*</sub> + &#x2211;<sub>*nQn)*</sub>*·*<sub>*·*</sub>

- *Q* = darbības daudzums
- *P* = darbības cena

Citiem vārdiem sakot, novērtētās vidējās izmaksas ir vienādas ar sākuma daudzumu, kas ir lielāks par sākuma cenu plus katra saņemšanas daudzuma summa, kas ik reizi tiek pieskaitīta saņemšanas cenai, un visas izmaksas tiek dalītas ar sākuma daudzumu plus saņemšanas daudzumu summu.

Krājumu slēgšanas laikā aprēķins tiek veikts katru dienu slēgšanas perioda laikā.

> [!NOTE]
> Plašāku informāciju par nosegšanu skatiet Krājumu [slēgšanā](inventory-close.md).

Sekojošos piemēros parādīta svērtā vidējā datuma lietošanas ar piecām konfigurācijām ietekme:

- Svērtā vidējā uz datumu tiešā segšana, ja netiek izmantota opcija **Iekļaut fizisko vērtību**
- Svērtā vidējā uz datumu apkopotā segšana, ja netiek izmantota opcija **Iekļaut fizisko vērtību**
- Svērtā vidējā uz datumu tiešā segšana, ja tiek izmantota opcija **Iekļaut fizisko vērtību**
- Svērtā vidējā uz datumu apkopotā segšana, ja tiek izmantota opcija **Iekļaut fizisko vērtību**
- Svērtais vidējais uz datumu, ja tiek izmantota iezīmēšana

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Svērtā vidējā uz datumu tiešā segšana, ja netiek izmantota opcija Iekļaut fizisko vērtību

Tiešās nosegšanas princips izveido nosegšanu tieši starp ieejas un izejas plūsmām, neizveidojot papildu krājumu darbības. Sistēma izmanto šo tiešās nosegšanas principu šādās situācijās:

- Perioda laikā tika iegrāmatota viena saņemšana un viena vai vairākas izejas plūsmas.
- Perioda laikā ir iegrāmatotas tikai izejas plūsmas, un ir pieejami rīcībā esošie krājumi no iepriekšējās slēgšanas.

Šajā piemērā izlaistajām **precei** lapā Krājumu modeļu grupa ir **notīrīta izvēles rūtiņa** Iekļaut fizisko vērtību. Diagramma, kas parāda šīs darbības:

**1. diena.**

- 1.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 10 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 20,00 par katru.
- 3.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 10.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 ar izmaksu cenu USD 10.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).

**2. diena.**

- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu finansiāla izdošana daudzumam 1, kas maksā USD 20.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).

**3. diena.**

- 7\. Tiek veikta krājumu slēgšana. Balstoties uz svērtā vidējā datuma metodi, sistēma izmanto tiešās segšanas metodi 30. decembrī (12/30), jo tikai viena saņemšana ir finansiāli atjaunināta 12/30. Šajā piemērā starp darbībām 1b un 3b tiek izveidota viena segšana. Tiek veikta USD 10.00 korekcija, lai nodrošinātu darbības 3b vērtību līdz 20,00. 31. decembrī (12/31) nav veiktas korekcijas vai segšana, jo 31.02.2001. nav finansiāli atjaunināta izejas plūsmas.

Šajā diagrammā parādītas šīs darījumu sērijas un ietekmēs novērtētā vidējā krājumu modeļa un tiešās nosegšanas principa izmantošana bez **opcijas Iekļaut fizisko** vērtību.

![Novērtētā vidējā datuma tiešā nosegšana bez Iekļaut fizisko vērtību iespējas.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Diagrammas atslēga:**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Datumi tiek atdalīti ar šauras melnas vertikālas līnijas. Datumi ir atzīmēti diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanām vertikālām punktlīnijas rindām.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Svērtā vidējā uz datumu apkopotā segšana, ja netiek izmantota opcija Iekļaut fizisko vērtību

Ja periodā ir vairākas saņemšanas, svērtais vidējais datums izmanto apkopotu segšanas *principu, kur visas saņemšanas vienā dienā tiek summēta darbībā ar nosaukumu "svērtā vidējā krājumu slēgšana"*. Visas šīs dienas saņemšanas tiek segtas attiecībā pret jauni izveidoto krājumu darbību izejas plūsmu. Visas šīs dienas izejas plūsmas tiek segtas attiecībā pret jauno krājumu darbības saņemšanu. Ja rīcībā esošo krājumu vērtība paliek pēc krājumu slēgšanas, rīcībā esošo krājumu vērtība tiek iekļauta svērtā vidējā krājumu slēgšanas darbību saņemšanas darbībā.

Diagramma, kas parāda šīs darbības:

**1. diena.**

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).

**2. diena.**

- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 23.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).

**3. diena.**

- 7\. Tiek veikta krājumu slēgšana.
- 7.a Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darījumu finanšu izejas plūsma, lai summētu visu krājumu finansiālo ieejas plūsmu segšanas.

    - Darbība 1b ir nosegta daudzumam 1 ar segtu summu USD 10.00.
    - Darbība 2b ir nosegta daudzumam 1 ar segtu summu USD 22.00.
    - Darbība 7a tiek izveidota daudzumam 2 ar nosegtu summu USD 32.00. Šī darbība korespondē divu ieejas plūsmas darbību summu, kas perioda laikā ir finansiāli atjauninātas.

- 7.b Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darījumu finanšu ieejas plūsma, kā finansiāli grāmatoto plūsmu korespondējošais konts.

    - Darījums 3b tiek segts ar daudzumu 1 ar segtu summu USD 16.00. Šī darbība netiek koriģēta, jo tā ir finansiāli grāmatoto darbību svērtā vidējā vērtība 1. decembrī (12/1).
    - Darbība 7b tiek izveidota daudzumam 2 ar finansiālu summu USD 32.00 un nosegtā summa 0USD 16.00 darbības 3b. Šī darbība korespondē ar vienas izdošanas darbības summu, kas ir finansiāli atjaunināta periodā. Darbība paliek atvērta, jo joprojām ir viena rīcībā.

Tālāk redzamajā diagrammā ir parādītas šīs darījumu sērijas un ietekmēs novērtētā vidējā krājumu modeļa un apkopotā nosegšanas principa izmantošana, bet **nelietojot opciju Iekļaut fizisko** vērtību.

![Novērtētā vidējā datuma kopsavilkuma nosegšana bez Iekļaut fizisko vērtību opcijas.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Diagrammas atslēga:**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Datumi tiek atdalīti ar šauras melnas vertikālas līnijas. Datumi ir atzīmēti diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanām vertikālām punktlīnijas rindām.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Svērtā vidējā uz datumu tiešā segšana, ja tiek izmantota opcija Iekļaut fizisko vērtību

Pašreizējā produkta versijā opcija **Iekļaut** fizisko vērtību darbojas atšķirīgi ar svērtā vidējā datuma krājumu modeli, nekā tas darbojas agrākās versijās. Kad jūs **atzīmējiet** **izvēles** rūtiņu Iekļaut fizisko vērtību krājumam krājumu modeļu grupas lapā, sistēma izmantos fiziski atjauninātas saņemšanas, kad tā aprēķina novērtēto izdošanas izmaksu cenu vai tekošo vidējo. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu slēgšanas laikā, aprēķinot svērto vidējo, tiek ņemtas vērtā tikai finansiāli atjauninātās ieejas plūsmas.

Diagramma, kas parāda šīs darbības:

**1. diena.**

- 1.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 10 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 10 pie cenas USD 20,00 par katru.
- 3.a Krājumu fiziska izdošana daudzumam 1 ar izmaksu cenu 0USD 15.00 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 par izmaksu cenu USD 15.00 (fiziski vai finansiāli grāmatoto darbību tekošā vidējā vērtība).

**2. diena.**

- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziskā izdošana daudzumam 1, kas maksā USD 21.25 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).

**3. diena.**

- 7\. Tiek veikta krājumu slēgšana. Balstoties uz svērtā vidējā datuma metodi, sistēma izmanto tiešās segšanas metodi 30. decembrī (12/30), jo tikai viena saņemšana ir finansiāli atjaunināta 12/30. Šajā piemērā starp darbībām 1b un 3b tiek izveidota viena segšana. 12/30 izejas plūsmai nav veikti nekādi pielāgojumi. Turklāt 31. decembrī (12/31) netiek veikta korekcija vai segšana, jo nav finansiāli atjaunināta 12.031. izejas plūsmas.

Šajā diagrammā ir parādītas šīs darījumu sērijas un ietekmēs novērtētā vidējā krājumu modeļa un tiešās nosegšanas principa izmantošana ar **opciju Iekļaut fizisko** vērtību.

![Svērtā vidējā tieša segšana ar iekļaut fizisko vērtību.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Diagrammas atslēga:**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Datumi tiek atdalīti ar šauras melnas vertikālas līnijas. Datumi ir atzīmēti diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanām vertikālām punktlīnijas rindām.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Svērtā vidējā uz datumu apkopotā segšana, ja tiek izmantota opcija Iekļaut fizisko vērtību

Pašreizējā produkta versijā opcija Iekļaut fizisko vērtību **darbojas** atšķirīgi ar svērto vidējo, nekā tas darbojas iepriekšējās versijās. Kad jūs **atzīmējiet** **izvēles** rūtiņu Iekļaut fizisko vērtību krājumam krājumu modeļu grupas lapā, sistēma izmantos fiziski atjauninātas saņemšanas, kad tā aprēķina novērtēto izmaksu cenu vai palaiž vidējo. Izejas plūsmas tiks iegrāmatotas, balstoties uz paredzēto izmaksu cenu periodā. Krājumu slēgšanas laikā, aprēķinot svērto vidējo, tiek ņemtas vērtā tikai finansiāli atjauninātās ieejas plūsmas. Ja lietojat svērtā vidējā krājuma modeli, ieteicam veikt krājumu slēgšanu katru mēnesi. Šajā svērtā vidējā datuma kopsavilkuma nosegšanas piemērā krājumu modelis tiek atzīmēts, lai ietvertu fizisko vērtību.

Diagramma, kas parāda šīs darbības:

**1. diena.**

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska izdošana daudzumam 1 ar izmaksu cenu 0USD 16.00 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 par izmaksu cenu USD 16.00 (fiziski vai finansiāli grāmatoto darbību tekošā vidējā vērtība).

**2. diena.**

- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska izdošana daudzumam 1 ar izmaksu cenu 0USD 23.67 (fiziski un finansiāli grāmatoto darbību tekošā vidējā vērtība).

**3. diena.**

- 7\. Tiek veikta krājumu slēgšana.
- 7.a Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darījumu finanšu izejas plūsma, lai summētu visu krājumu finansiālo ieejas plūsmu segšanas.

    - Darbība 1b ir nosegta daudzumam 1 ar segtu summu USD 10.00.
    - Darbība 2b ir nosegta daudzumam 1 ar segtu summu USD 22.00.
    - Darbība 7a tiek izveidota daudzumam 2 ar nosegtu summu USD 32.00. Šī darbība korespondē divu ieejas plūsmas darbību summu, kas perioda laikā ir finansiāli atjauninātas.

- 7.b Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas darījumu finanšu ieejas plūsma, kā finansiāli grāmatoto plūsmu korespondējošais konts.

    - Darījums 3b tiek segts ar daudzumu 1 ar segtu summu USD 16.00. Šī darbība netiek koriģēta, jo tā ir finansiāli grāmatoto darbību svērtā vidējā vērtība 1. decembrī (12/1).
    - Darbība 7b tiek izveidota daudzumam 2 ar finansiālu summu USD 32.00 un nosegtā summa 0USD 16.00 darbības 3b. Šī darbība korespondē ar vienas izdošanas darbības summu, kas ir finansiāli atjaunināta periodā. Darbība paliek atvērta, jo joprojām ir viena rīcībā.

Šajā diagrammā ir parādītas šīs darījumu sērijas un ietekmēs novērtētā vidējā krājumu modeļa un apkopotā nosegšanas principa izmantošana bez **opcijas Iekļaut fizisko** vērtību.

![Svērtā vidējā apkopotā segšana ar iekļaut fizisko vērtību.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Diagrammas atslēga:**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Datumi tiek atdalīti ar šauras melnas vertikālas līnijas. Datumi ir atzīmēti diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanām vertikālām punktlīnijas rindām.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="weighted-average-date-when-marking-is-used"></a>Svērtais vidējais uz datumu, ja tiek izmantota iezīmēšana

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārliecināties par precīzām krājumu izmaksām, kad darbība ir grāmatota vai tiek veikta krājumu slēgšana.

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tādēļ, ka tas ir steidzams pasūtījums, jums būs par šo krājumu jāmaksā vairāk, lai sniegtu klienta pieprasījumu. Jums jābūt pārliecinātos, ka krājuma izmaksas šim pārdošanas pasūtījuma rēķinam tiek atainotas uzcenojuma vai pārdoto preču izmaksās (COGS).

Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja pārdošanas pasūtījums ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina grāmatošanas, COGS būs tikai USD 120.00 pašreizējo krājuma vidējo izmaksu vietā. Ja iezīmēšana notiek pēc pārdošanas pasūtījuma pavadzīmes vai rēķina iegrāmatošanas, COGS būs pie tekošās vidējās izmaksu cenas.

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Ja ieejas plūsmas darbība ir atzīmēta ar izdošanas darbību, novērtēšanas metode, kas ir izvēlēta krājuma modeļa grupai, tiks ignorēta, un sistēma nosegs šīs darbības vienu ar otru.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pirms transakcijas grāmatošanas. Šo iezīmēšanu var veikt no pārdošanas pasūtījuma rindas lapā **Detalizēta informācija par pārdošanas** pasūtījumu. Atvērtās saņemšanas darbības ir parādītas lapā **Iezīmēšana**.

Varat arī iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu.

Diagramma, kas parāda šīs darbības:

**1. diena.**

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3c. Krājumu finansiāla izdošana darbībai 3b ir atzīmēta ar krājumu finansiālo izdošanu darījumam 2b.

**2. diena.**

- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 23.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).

**3. diena.**

- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz iezīmēšanas principu, kas izmanto svērtā vidējā metodi, iezīmētās darbības tiek nosegtas viena pret otru. Šajā piemērā darbība 3b tiek nosegta pret darbību 2b, un korekcija USD 6.00 iegrāmatota darbībā 3b, lai vērtību USD 22.00. Šajā piemērā netiek veiktas papildu nosegšanas, jo aizvēršana izveido segšanas tikai finansiāli atjauninātām darbībām.

Šajā diagrammā parādītas šīs darījumu sērijas un ietekmēs novērtētā vidējā krājumu modeļa izmantošana ar iezīmēšanu.

![Svērtais vidējais ar iezīmējumu.](media/weighted-average-date-with-marking.png)

**Diagrammas atslēga:**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir parādīta ar vertikālām bultām virs ass.
- Krājuma izejas plūsmas ir norādītas ar vertikālām bultām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Datumi tiek atdalīti ar šauras melnas vertikālas līnijas. Datumi ir atzīmēti diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanām vertikālām punktlīnijas rindām.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
