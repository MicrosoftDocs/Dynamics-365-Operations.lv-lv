---
title: FIFO ar fizisko vērtību un iezīmēšanu
description: Pirmie iekšā, pirmie ārā (FIFO) ir krājumu modelis, kur pirmie saņemtie krājumi tiek arī pirmie izdoti. Finansiāli apstrādātie izdotie krājumi tiek nosegti ar pirmajiem finansiāli apstrādātajiem saņemtajiem krājumiem saskaņā ar krājumu darbību finansiālo datumu.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092144"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO ar fizisko vērtību un iezīmēšanu

[!include [banner](../includes/banner.md)]


Pirmais iekšā, pirmais ārā (FIFO) ir krājumu pārvaldības un novērtēšanas metode, kurā vispirms tiek pārdoti, izmantoti vai iznīcināti krājumi, kas ir saražoti vai iegūti vispirms. Inventāra aizvēršanas procesa laikā Microsoft Dynamics 365 Supply Chain Management, sistēma izveidos norēķinus, kuros pirmā kvīts tiek saskaņota ar pirmo izdevumu utt.

Norēķinu un saskaņošanas princips ir balstīts uz inventarizācijas darījumu finanšu datumu. Norēķinu un korekciju provizorisku novērtējumu var veikt, palaižot krājumu pārrēķina procesu.

Varat ignorēt FIFO principu, atzīmējot krājumu transakcijas, lai konkrētas preces saņemšana tiktu dzēsta pret konkrētu problēmu. Periodiska krājumu slēgšana ir nepieciešama, ja izmantojat FIFO uzskaites modeli, lai izveidotu norēķinus un pielāgotu emisiju vērtību saskaņā ar FIFO principu. Kamēr palaižat krājumu aizvēršanas procesu, izdošanas transakcijas tiek novērtētas pēc vidējās vērtības, kad tika veikti fiziskie un finanšu atjauninājumi. Ja vien neizmantojat atzīmēšanu, vidējais rādītājs tiek aprēķināts, veicot fizisko vai finansiālo atjauninājumu. Tālākie piemēri parāda FIFO ietekmi, to lietojot trīs dažādos konfigurācijas veidos:

- FIFO bez opcijas **Iekļaut fizisko vērtību**
- FIFO ar opciju **Iekļaut fizisko vērtību**
- FIFO ar iezīmēšanu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO bez opcijas Iekļaut fizisko vērtību

Šajā piemērā **Iekļaujiet fizisko vērtību** Izlaistā produkta preču modeļu grupā ir notīrīta izvēles rūtiņa. Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska problēma daudzumam 1 par izmaksu cenu USD 16.00 (finansiāli reģistrēto darījumu vidējais rādītājs).
- 3.b Krājumu finanšu problēma daudzumam 1 par izmaksu cenu USD 16.00 (finansiāli reģistrēto darījumu vidējais rādītājs).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska problēma daudzumam 1 par izmaksu cenu USD 23.00 (finansiāli reģistrēto darījumu vidējais rādītājs)
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz FIFO metodi, pirmais finansiāli atjauninātais jautājums tiks apmaksāts ar pirmo finansiāli atjaunināto kvīti utt. Šajā piemērā starp 1b un 3b tiek izveidota viena apdzīvota vieta. 3b tiks veikta korekcija USD 6,00 apmērā, un rezultātā galīgās izmaksas būs USD 10.00.

Jaunā aprēķinātā vidēja izmaksu cena ietekmē finansiāli atjaunoto darījumu vidējo rādītāju. Sekojošās ilustrācijas parāda FIFO krājumu modeļa ietekmi uz šo darbību sēriju, kad opcija **Iekļaut fizisko vērtību** netiek izmantota.

![FIFO bez opcijas Iekļaut fizisko vērtību.](./media/fifo-without-include-physical-value.png)

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskos darījumus attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
- Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar plānu melnu vertikālu līniju. Datums ir norādīts diagrammas apakšā.
- Krājumu slēgšana ir attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO ar fizisko vērtību iekļaušanas opciju

Ja **Iekļaujiet fizisko vērtību** izvēles rūtiņa ir atlasīta vienumam vietnē **Preču modeļu grupa** lapā, sistēma izmanto gan fizisko, gan finanšu ieņēmumu darījumus, lai aprēķinātu tekošo vidējo pašizmaksu. Attiecīgā gadījumā sistēma pielāgo arī fiziski atjaunināto emisijas darījumu. Krājumu slēgšana, kas izmanto FIFO krājumu modeli, veic norēķinus tikai par darījumiem, kas ir finansiāli atjaunināti. Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas.

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska problēma daudzumam 1 par izmaksu cenu USD 16.00 (fiziski un finansiāli reģistrēto darījumu vidējā vērtība).
- 3.b Krājumu finanšu problēma daudzumam 1 par izmaksu cenu USD 16.00 (fiziski un finansiāli reģistrēto darījumu vidējais rādītājs).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska problēma daudzumam 1 par izmaksu cenu USD 23.67 (fiziski un finansiāli reģistrēto darījumu vidējā vērtība).
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz FIFO metodi, pirmais finansiāli atjauninātais jautājums tiks apmaksāts ar pirmo finansiāli atjaunināto kvīti utt. Šajā piemērā starp 1b un 3b tiek izveidota viena apdzīvota vieta. 3b tiks veikta korekcija USD 6,00 apmērā, un rezultātā galīgās izmaksas būs USD 10.00. Turklāt darījums 6.a tiks pielāgots kvīts darījuma izmaksām 2b. Sistēmā šīs transakcijas netiek segtas, jo saņemšana tiek atjaunināta fiziski, bet ne finansiāli. Tā vietā fiziskās emisijas darījumam tiks publicēta tikai korekcija USD 1,67 apmērā, un rezultātā koriģētās izmaksas būs USD 22.00.

![FIFO ar opciju Iekļaut fizisko vērtību.](./media/fifo-with-include-physical-value.png)

Ņemiet vērā, ka krājumu aizvēršanas procesa izpildes rezultāts ir vienāds neatkarīgi no tā, vai atlasāt **Iekļaujiet fizisko vērtību** opcija uz **Preču modeļu grupa** lappuse. The **Iekļaujiet fizisko vērtību** opcija ietekmē tikai vidējo rādītāju.

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskos darījumus attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
- Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar plānu melnu vertikālu līniju. Datums ir norādīts diagrammas apakšā.
- Krājumu slēgšana ir attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="fifo-with-marking"></a>FIFO ar iezīmēšanu

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas.

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā šis pasūtījums ir steidzams pasūtījums, jums ir jāmaksā vairāk par šo preci, lai izpildītu klienta pieprasījumu. Jums ir jāpārliecinās, ka krājuma preces izmaksas ir atspoguļotas pārdošanas pasūtījuma rēķina maržā jeb pārdoto preču izmaksās (COGS). Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja pārdošanas pasūtījuma dokuments ir atzīmēts pirkuma pasūtījumā pirms iepakojuma pavadzīmes vai rēķina grāmatošanas, COGS būs USD 120.00, nevis preces pašreizējās tekošās vidējās izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena. Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Kad saņemšanas transakcija ir atzīmēta kā izdošanas transakcija, preču modeļu grupā definētā vērtēšanas metode netiek ņemta vērā, un sistēma šos darījumus veic savā starpā. Varat manuāli atzīmēt darījumu ar pārdošanas pasūtījuma rindu **Pārdošanas pasūtījuma informācija** lapu, atlasot **Inventārs \> Marķēšana** uz **Pārdošanas pasūtījumu rindas** FastTab. Varat skatīt atvērtās ieejas plūsmas transakcijas lapā **Iezīmēšana**. Varat saskaņot vai atzīmēt izdošanas darījumu ar atvērtu saņemšanas transakciju inventāra precei no iegrāmatotā krājumu korekcijas žurnāla. Sekojošajā ilustrācijā tiek parādītas šīs darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska problēma daudzumam 1 par izmaksu cenu USD 16.00 (finansiāli reģistrēto darījumu vidējais rādītājs).
- 3.b Krājumu finanšu problēma daudzumam 1 par izmaksu cenu USD 16.00 (finansiāli reģistrēto darījumu vidējais rādītājs).
- 3c. Krājumu finanšu emisija 3.b ir atzīmēta kā krājumu finanšu problēma 2.b.
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska problēma daudzumam 1 par izmaksu cenu USD 23.00 (finansiāli reģistrēto darījumu vidējais rādītājs)
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz marķēšanas principu, kurā tiek izmantota FIFO metode, atzīmētie darījumi tiek norēķināti viens pret otru. Šajā piemērā 3b tiek izlīdzināts pret 2b, un USD 6.00 korekcija tiek ievietota 3b, lai vērtību iegūtu USD 22.00. Šajā piemērā papildu norēķini netiek veikti, jo slēgšana veido norēķinus tikai par finansiāli atjauninātiem darījumiem.

Sekojošajā ilustrācijā redzama šī darījumu sērija ar ietekmi, ko rada FIFO krājumu modeļa izvēle ar nozīmēšanu starp izsniegšanas un saņemšanas darījumiem.

![FIFO ar marķējumu.](./media/fifo-with-marking.png)

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskos darījumus attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
- Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar plānu melnu vertikālu līniju. Datums ir norādīts diagrammas apakšā.
- Krājumu slēgšana ir attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Norēķini un marķējumi, kas tiek veikti, aizverot krājumus, ir attēloti ar sarkanām diagonālām punktētām bultiņām, kas pāriet no kvīts uz izdevumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
