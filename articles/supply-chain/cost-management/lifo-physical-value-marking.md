---
title: LIFO ar fizisko vērtību un iezīmēšanu
description: Pēdējais iesūtītais, Pirmais izsūtītais (pretsecība) ir krājumu modelis, kurā pēdējās (jaunākās) saņemšanas tiek izdotas vispirms. Izdotais krājums nosedz pirmo saņemto krājumu, ņemot vērā krājumu darbības veikšanas fizisko datumu.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45316c40cce988c0758e70af627b0123ec1f7873
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670445"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO ar fizisko vērtību un iezīmēšanu

[!include [banner](../includes/banner.md)]

"Pēdējais ārā" (Last in, first out – LIFO) ir krājumu vadības un novērtēšanas metode, kurā krājums, kurš tika ražots vai iegūts pēdējais, ir pārdots, izmantots vai izslēgts no tā vispirms. Microsoft krājumu slēgšanas procesa laikā Dynamics 365 Supply Chain Management sistēma izveidos segšanas, kur pēdējā saņemšana tiek saskaņota ar pirmo izejas plūsmu utt. Nosegšanas un saskanības princips ir balstīts uz krājumu darbību finanšu datumu. Nosegšanas un pārrēķinu priekšnovērtējumu var veikt, palaižot krājumu pārrēķināšanas procesu.

Varat ignorēt LIFO principu, iezīmējot krājumu darbības tā, lai noteikta krājuma saņemšana tiek segta pret noteiktu izejas plūsmu. Ja izmantojat LIFO krājumu modeli, lai izveidotu segšanas un koriģētu izejas plūsmas vērtību atbilstoši LIFO principam, nepieciešama periodiska krājumu slēgšana. Kamēr nav veikti krājumu slēgšanas procesi, izdošanas darbības tiek vērtībās pēc tekošā vidējā, kad tika veikti fiziskie un finanšu atjauninājumi. Ja vien nelieto atzīmēto, aprēķinātais vidējais tiek aprēķināts, veicot fiziskās vai finanšu atjaunināšanas.

Tālākie piemēri parāda LIFO ietekmi, to lietojot trīs dažādos konfigurācijas veidos:

- LIFO bez opcijas **Iekļaut fizisko vērtību**
- LIFO ar opciju **Iekļaut fizisko vērtību**
- LIFO ar atzīmi

## <a name="lifo-without-the-include-physical-value-option"></a>Pretsecība bez opcijas Iekļaut fizisko vērtību

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
- 7\. Tiek veikta krājumu slēgšana. Balstoties uz liFO metodi, pirmā finansiāli atjauninātā izdošana tiks nosegta ar pēdējo finansiāli atjaunināto saņemšanu utt. Šajā piemērā starp 5b un 3b tiek izveidota viena segšana. Valūtas pārrēķins USD 14.00 3b, un rezultātā iegūtās gala izmaksas tiks USD 30.00.

Nākamajā attēlā ir parādīta FIFO krājumu modeļa ietekme uz šo transakciju sēriju, ja netiek izmantota opcija **Iekļaut fizisko vērtību**.

![Pretpārdot bez opcijas Iekļaut fizisko vērtību.](./media/lifo-without-including-physical-value.png)

**Diagrammas atslēga**

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

## <a name="lifo-with-the-include-physical-value-option"></a>Pretsecība ar opciju Iekļaut fizisko vērtību

Ja izvēles **rūtiņa Iekļaut fizisko** **vērtību** ir atzīmēta krājuma modeļu grupu lapā, sistēma izmanto gan fiziskās, gan finansiālās saņemšanas darbības, lai aprēķinātu tekošo vidējo izmaksu cenu. Ja piemērojams, sistēma arī pielāgo fiziski atjaunināto izdošanas darbību. Ja izvēles rūtiņa **Iekļaut fizisko vērtību** ir notīrīta, krājumu slēgšana, kas izmanto LIFO krājumu modeli, nosegšanu veic tikai finansiāli atjauninātām darbībām.

Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas.

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
- 7\. Tiek veikta krājumu slēgšana. Balstoties uz liFO metodi, pirmā finansiāli atjauninātā izdošana tiks nosegta ar pēdējo finansiāli atjaunināto saņemšanu utt. Šajā piemērā starp 3b un 5b tiek izveidota viena segšana. Valūtas pārrēķins USD 14.00 3b, un rezultātā iegūtās gala izmaksas tiks USD 30.00. Turklāt darbība 6a tiks pielāgota saņemšanas darbības izmaksām 4a. Sistēmā šīs transakcijas netiek segtas, jo saņemšana tiek atjaunināta fiziski, bet ne finansiāli. Tā vietā fiziskās izdošanas USD 1.33 tiks iegrāmatots tikai krājuma pārrēķins, un rezultātā koriģētās izmaksas tiks USD 25.00.

Sekojošā ilustrācija parāda LIFO krājumu modeļa ietekmi uz šo darbību sēriju, kad tiek izmantota opcija **Iekļaut fizisko vērtību**.

![Pretpārdot ar opciju Iekļaut fizisko vērtību.](./media/lifo-with-included-physical-value.png)

**Diagrammas atslēga**

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

## <a name="lifo-with-marking"></a>LIFO ar iezīmēšanu

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā šis pasūtījums ir steidzams pasūtījums, lai izpildītu klienta pieprasījumu, par krājumu jāmaksā vairāk.

Jums ir jānodrošina, lai krājumu izmaksas pārdošanas pasūtījuma rēķinam tiek atainotas uzcenojuma vai pārdoto preču izmaksās (COGS). Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja šis pārdošanas dokuments ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina iegrāmatošanas, tad COGS būs USD 120,00, nevis pašreizējas krājuma vidējas izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena.

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pirms transakcijas grāmatošanas. Šo iezīmēšanu var veikt no pārdošanas pasūtījuma **rindas lapā Detalizēta informācija par pārdošanas pasūtījumu,** **\>** kopsavilkuma cilnē Pārdošanas pasūtījuma rindas atlasot Krājumu **iezīmēšana.** Varat skatīt atvērtās ieejas plūsmas transakcijas lapā **Iezīmēšana**.

Varat arī iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu.

Sekojošajā ilustrācijā tiek parādītas šīs darbības:

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
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz atzīmēšanas principu, kas izmanto PRETfo metodi, iezīmētās darbības tiek nosegtas viena ar otru. Šajā piemērā 3b tiek nosegta pret 2b, un korekcija USD 6.00 iegrāmatota 3b, lai vērtība ienestu USD 22.00. Šajā piemērā netiek veikta papildu segšana, jo aizvēršana izveido segšanas tikai finansiāli atjauninātām darbībām.

Jauna spēkā esošā vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50.

Sekojošajā ilustrācijā redzama šī darījumu sērija ar ietekmi, ko rada LIFO krājumu modeļa izvēle ar nozīmēšanu starp izsniegšanas un saņemšanas darījumiem.

![LIFO ar atzīmi.](./media/lifo-with-marking.png)

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
- Segšanas un iezīmējumi, kas ir veikti, noslēdzot krājumus, un atzīmēti ar sarkanām diagonālām svītras bultām, kas iet no saņemšanas līdz izdošanai.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
