---
title: LIFO ar fizisko vērtību un iezīmēšanu
description: Pēdējais iesūtītais, Pirmais izsūtītais (pretsecība) ir krājumu modelis, kurā pēdējās (jaunākās) saņemšanas tiek izdotas vispirms. Izdotais krājums nosedz pirmo saņemto krājumu, ņemot vērā krājumu darbības veikšanas fizisko datumu.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd57d58aa91aa87b1c2feff52a568296fc18ed9b
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092168"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO ar fizisko vērtību un iezīmēšanu

[!include [banner](../includes/banner.md)]

Pēdējais iekšā, pirmais ārā (LIFO) ir krājumu pārvaldības un novērtēšanas metode, kurā krājumi, kas saražoti vai iegādāti pēdējie, tiek pārdoti, izmantoti vai iznīcināti vispirms. Inventāra aizvēršanas procesa laikā Microsoft Dynamics 365 Supply Chain Management, sistēma izveidos norēķinus, kuros pēdējā kvīts tiek saskaņota ar pirmo izdevumu utt. Norēķinu un saskaņošanas princips ir balstīts uz inventarizācijas darījumu finanšu datumu. Norēķinu un korekciju provizorisku novērtējumu var veikt, palaižot krājumu pārrēķina procesu.

LIFO principu var ignorēt, atzīmējot krājumu transakcijas, lai konkrētas preces saņemšana tiktu dzēsta pret konkrētu problēmu. Periodiska krājumu slēgšana ir nepieciešama, ja izmantojat LIFO inventarizācijas modeli, lai izveidotu norēķinus un pielāgotu emisiju vērtību saskaņā ar LIFO principu. Kamēr palaižat krājumu aizvēršanas procesu, izdošanas transakcijas tiek novērtētas pēc vidējās vērtības, kad tika veikti fiziskie un finanšu atjauninājumi. Ja vien neizmantojat atzīmēšanu, vidējais rādītājs tiek aprēķināts, veicot fizisko vai finansiālo atjauninājumu.

Tālākie piemēri parāda LIFO ietekmi, to lietojot trīs dažādos konfigurācijas veidos:

- LIFO bez opcijas **Iekļaut fizisko vērtību**
- LIFO ar opciju **Iekļaut fizisko vērtību**
- LIFO ar atzīmi

## <a name="lifo-without-the-include-physical-value-option"></a>Pretsecība bez opcijas Iekļaut fizisko vērtību

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
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz LIFO metodi, pirmais finansiāli atjauninātais jautājums tiks dzēsts pret pēdējo finansiāli atjaunināto kvīti utt. Šajā piemērā starp 5b un 3b tiek izveidota viena apdzīvota vieta. USD 14.00 korekcija tiks veikta uz 3b, un rezultātā galīgās izmaksas būs USD 30.00.

Nākamajā attēlā ir parādīta FIFO krājumu modeļa ietekme uz šo transakciju sēriju, ja netiek izmantota opcija **Iekļaut fizisko vērtību**.

![LIFO bez opcijas Iekļaut fizisko vērtību.](./media/lifo-without-including-physical-value.png)

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskos darījumus attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Inventāra kvītis ir attēlotas ar vertikālām bultiņām virs ass.
- Problēmas no krājumiem ir attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar plānu melnu vertikālu līniju. Datums ir norādīts diagrammas apakšā.
- Krājumu slēgšana ir attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="lifo-with-the-include-physical-value-option"></a>Pretsecība ar opciju Iekļaut fizisko vērtību

Ja **Iekļaujiet fizisko vērtību** izvēles rūtiņa ir atlasīta vienumam vietnē **Preču modeļu grupas** lapā, sistēma izmanto gan fizisko, gan finanšu ieņēmumu darījumus, lai aprēķinātu tekošo vidējo pašizmaksu. Attiecīgā gadījumā sistēma pielāgo arī fiziski atjaunināto emisijas darījumu. Kad **Iekļaujiet fizisko vērtību** izvēles rūtiņa ir notīrīta, krājumu aizvēršana, kas izmanto LIFO krājumu modeli, veic norēķinus tikai par darījumiem, kas ir finansiāli atjaunināti.

Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas.

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
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz LIFO metodi, pirmais finansiāli atjauninātais jautājums tiks dzēsts pret pēdējo finansiāli atjaunināto kvīti utt. Šajā piemērā starp 3b un 5b tiek izveidota viena apdzīvota vieta. USD 14.00 korekcija tiks veikta uz 3b, un rezultātā galīgās izmaksas būs USD 30.00. Turklāt darījums 6a tiks pielāgots kvīts darījuma izmaksām 4a. Sistēmā šīs transakcijas netiek segtas, jo saņemšana tiek atjaunināta fiziski, bet ne finansiāli. Tā vietā fiziskās emisijas darījumā tiks publicēta tikai USD 1.33 korekcija, un rezultātā koriģētās izmaksas būs USD 25.00.

Sekojošā ilustrācija parāda LIFO krājumu modeļa ietekmi uz šo darbību sēriju, kad tiek izmantota opcija **Iekļaut fizisko vērtību**.

![LIFO ar opciju Iekļaut fizisko vērtību.](./media/lifo-with-included-physical-value.png)

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskos darījumus attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Inventāra kvītis ir attēlotas ar vertikālām bultiņām virs ass.
- Problēmas no krājumiem ir attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar plānu melnu vertikālu līniju. Datums ir norādīts diagrammas apakšā.
- Krājumu slēgšana ir attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="lifo-with-marking"></a>LIFO ar iezīmēšanu

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā šis pasūtījums ir steidzams pasūtījums, jums ir jāmaksā vairāk par preci, lai izpildītu klienta pieprasījumu.

Jums ir jāpārliecinās, ka krājuma preces izmaksas ir atspoguļotas pārdošanas pasūtījuma rēķina maržā jeb pārdoto preču izmaksās (COGS). Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja šis pārdošanas dokuments ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina iegrāmatošanas, tad COGS būs USD 120,00, nevis pašreizējas krājuma vidējas izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena.

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pirms transakcijas grāmatošanas. Šo atzīmēšanu var izdarīt no pārdošanas pasūtījuma rindas uz **Pārdošanas pasūtījuma informācija** lapu, atlasot **Inventārs \> Marķēšana** uz **Pārdošanas pasūtījumu rindas** FastTab. Varat skatīt atvērtās ieejas plūsmas transakcijas lapā **Iezīmēšana**.

Varat arī iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu.

Sekojošajā ilustrācijā tiek parādītas šīs darbības:

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
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz marķēšanas principu, kurā tiek izmantota LIFO metode, atzīmētie darījumi tiek savstarpēji norēķināti. Šajā piemērā 3b tiek izlīdzināts pret 2b, un USD 6.00 korekcija tiek ievietota 3b, lai vērtību iegūtu USD 22.00. Šajā piemērā papildu norēķini netiek veikti, jo slēgšana veido norēķinus tikai par finansiāli atjauninātiem darījumiem.

Jauna spēkā esošā vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50.

Sekojošajā ilustrācijā redzama šī darījumu sērija ar ietekmi, ko rada LIFO krājumu modeļa izvēle ar nozīmēšanu starp izsniegšanas un saņemšanas darījumiem.

![LIFO ar marķējumu.](./media/lifo-with-marking.png)

**Diagrammas apzīmējumi**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskos darījumus attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Inventāra kvītis ir attēlotas ar vertikālām bultiņām virs ass.
- Problēmas no krājumiem ir attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar plānu melnu vertikālu līniju. Datums ir norādīts diagrammas apakšā.
- Krājumu slēgšana ir attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Norēķini un marķējumi, kas tiek veikti, aizverot krājumus, ir attēloti ar sarkanām diagonālām punktētām bultiņām, kas pāriet no kvīts uz izdevumu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
