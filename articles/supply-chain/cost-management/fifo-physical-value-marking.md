---
title: FIFO ar fizisko vērtību un iezīmēšanu
description: Pirmie iekšā, pirmie ārā (FIFO) ir krājumu modelis, kur pirmie saņemtie krājumi tiek arī pirmie izdoti. Finansiāli apstrādātie izdotie krājumi tiek nosegti ar pirmajiem finansiāli apstrādātajiem saņemtajiem krājumiem saskaņā ar krājumu darbību finansiālo datumu.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 663dce9f871e96fec7017616732428c49b1224a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676248"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO ar fizisko vērtību un iezīmēšanu

[!include [banner](../includes/banner.md)]


Pirmais in, pirmais ārā (First in, first out – FIFO) ir krājumu vadības un novērtēšanas metode, kurā krājums, kas tiek ražots vai iegūts pirmais, tiek pārdots, izmantots vai izslēgts no tā vispirms. Microsoft krājumu slēgšanas procesa laikā Dynamics 365 Supply Chain Management sistēma izveidos segšanas, kur pirmā saņemšana tiek saskaņota ar pirmo izdošanu utt.

Nosegšanas un saskanības princips ir balstīts uz krājumu darbību finanšu datumu. Nosegšanas un pārrēķinu priekšnovērtējumu var veikt, palaižot krājumu pārrēķināšanas procesu.

Varat ignorēt FIFO principu, iezīmējot krājumu darbības tā, lai noteikta krājuma saņemšana tiek segta pret noteiktu izejas plūsmu. Ja izmantojat FIFO krājumu modeli, lai izveidotu segšanas un koriģētu izejas plūsmas vērtību saskaņā ar FIFO principu, nepieciešama periodiska krājumu slēgšana. Kamēr nav veikti krājumu slēgšanas procesi, izdošanas darbības tiek vērtībās pēc tekošā vidējā, kad tika veikti fiziskie un finanšu atjauninājumi. Ja vien nelieto atzīmēto, aprēķinātais vidējais tiek aprēķināts, veicot fiziskās vai finanšu atjaunināšanas. Tālākie piemēri parāda FIFO ietekmi, to lietojot trīs dažādos konfigurācijas veidos:

- FIFO bez opcijas **Iekļaut fizisko vērtību**
- FIFO ar opciju **Iekļaut fizisko vērtību**
- FIFO ar iezīmēšanu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO bez opcijas Iekļaut fizisko vērtību

Šajā piemērā izlaistajām **precei** krājumu modeļu grupā ir notīrīta izvēles rūtiņa Iekļaut fizisko vērtību. Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziska izsniegšana ar daudzumu 1, kuras izmaksu cena ir USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 3.b Krājumu finansiāla izdošana ar daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziska izsniegšana ar daudzumu 1 pie izmaksu cenas USD 23.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība)
- 7\. Tiek veikta krājumu slēgšana. Balstoties uz FIFO metodi, pirmā finansiāli atjauninātā izdošana tiks nosegta ar pirmo finansiāli atjaunināto saņemšanu utt. Šajā piemērā starp 1b un 3b tiek izveidota viena segšana. USD –6,00 koriģēšana tiks veikta uz 3b, un rezultātā iegūtās gala izmaksas USD 10.00.

Jaunā aprēķinātā vidēja izmaksu cena ietekmē finansiāli atjaunoto darījumu vidējo rādītāju. Sekojošās ilustrācijas parāda FIFO krājumu modeļa ietekmi uz šo darbību sēriju, kad opcija **Iekļaut fizisko vērtību** netiek izmantota.

![FIFO bez Fizisko vērtību ietveršanas iespējas](./media/fifo-without-include-physical-value.png)

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
- Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO ar fizisko vērtību iekļaušanas opciju

Ja krājumu **modeļu grupas lapas** **krājumam** atzīmēta izvēles rūtiņa Iekļaut fizisko vērtību, sistēma izmanto gan fiziskās, gan finansiālās saņemšanas darbības, lai aprēķinātu tekošo vidējo izmaksu cenu. Ja piemērojams, sistēma arī pielāgo fiziski atjaunināto izdošanas darbību. Krājumu slēgšana, kas izmanto FIFO krājumu modeli, veic nosegšanu tikai finansiāli atjauninātām darbībām. Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas.

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
- 7\. Tiek veikta krājumu slēgšana. Balstoties uz FIFO metodi, pirmā finansiāli atjauninātā izdošana tiks nosegta ar pirmo finansiāli atjaunināto saņemšanu utt. Šajā piemērā starp 1b un 3b tiek izveidota viena segšana. USD –6,00 koriģēšana tiks veikta uz 3b, un rezultātā iegūtās gala izmaksas USD 10.00. Turklāt darbība 6a tiks pielāgota saņemšanas darbības izmaksām 2b. Sistēmā šīs transakcijas netiek segtas, jo saņemšana tiek atjaunināta fiziski, bet ne finansiāli. Tāpēc fiziskās izdošanas darbībai tiks grāmatots tikai USD -1,67 pārrēķins, un rezultātā koriģētās izmaksas tiks USD 22.00.

![FIFO ar fizisko vērtību ietveršanas opciju.](./media/fifo-with-include-physical-value.png)

Ievērojiet, ka krājumu slēgšanas procesa rezultāts ir vienāds neatkarīgi no tā, **·** **vai krājumu modeļu grupas lapā atlasāt opciju Iekļaut fizisko** vērtību. Opcija **Iekļaut fizisko vērtību** ietekmē tikai tekošo vidējo.

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
- Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="fifo-with-marking"></a>FIFO ar iezīmēšanu

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas.

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā šis pasūtījums ir steidzams pasūtījums, lai izpildītu klienta pieprasījumu, par šo krājumu jums jāmaksā vairāk. Jums ir jānodrošina, lai krājumu izmaksas pārdošanas pasūtījuma rēķinam tiek atainotas uzcenojuma vai pārdoto preču izmaksās (COGS). Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja pārdošanas pasūtījums ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina grāmatošanas, COGS būs tikai USD 120.00, nevis pašreizējas krājuma vidējās izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena. Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Kad saņemšanas darbība ir atzīmēta ar izdošanas darbību, novērtēšanas metode, kas ir definēta krājumu modeļa grupā, tiek ignorēta, un sistēma sedz šīs darbības vienu ar otru. Jūs varat manuāli atzīmēt darbību **pret** **\>** **pārdošanas pasūtījuma rindu lapā Pārdošanas pasūtījuma detaļas, kopsavilkuma cilnē Pārdošanas pasūtījuma** rindas atlasot Krājumu iezīmēšana. Varat skatīt atvērtās ieejas plūsmas transakcijas lapā **Iezīmēšana**. Grāmatotajā krājumu korekciju žurnālā varat salīdzināt vai atzīmēt izdošanas darbību ar atvērtu saņemtā krājuma saņemšanas darbību. Sekojošajā ilustrācijā tiek parādītas šīs darbības:

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
- 6.a Krājumu fiziska izsniegšana ar daudzumu 1 pie izmaksu cenas USD 23.00 (finansiāli grāmatoto darbību tekošā vidējā vērtība)
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz iezīmēšanas principu, kas izmanto FIFO metodi, iezīmētās darbības tiek nosegtas viena pret otru. Šajā piemērā 3b tiek nosegta pret 2b, un korekcija USD 6.00 iegrāmatota 3b, lai vērtība ienestu USD 22.00. Šajā piemērā netiek veikta papildu segšana, jo aizvēršana izveido segšanas tikai finansiāli atjauninātām darbībām.

Sekojošajā ilustrācijā redzama šī darījumu sērija ar ietekmi, ko rada FIFO krājumu modeļa izvēle ar nozīmēšanu starp izsniegšanas un saņemšanas darījumiem.

![FIFO ar iezīmēšanu.](./media/fifo-with-marking.png)

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības ir norādītas ar īsākām, gaišpelēkām bultām.
- Finanšu darbības ir norādītas ar garākām melnām bultām.
- Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
- Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs datums diagrammā ir atdalīts ar šaurs melnas krāsas vertikālu līniju. Datums ir norādīts diagrammas apakšdaļā.
- Krājuma slēgšanas, kas apzīmētas ar sarkanu vertikālu punktlīnijas rindu.
- Segšanas un iezīmējumi, kas ir veikti, noslēdzot krājumus, un atzīmēti ar sarkanām diagonālām svītras bultām, kas iet no saņemšanas līdz izdošanai.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
