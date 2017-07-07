---
title: "LIFO ar fizisko vērtību un iezīmēšanu"
description: "Pēdējais iesūtītais, Pirmais izsūtītais (pretsecība) ir krājumu modelis, kurā pēdējās (jaunākās) saņemšanas tiek izdotas vispirms. Izdotais krājums nosedz pirmo saņemto krājumu, ņemot vērā krājumu darbības veikšanas fizisko datumu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 9910919d8b2a4f670710099b5150d7c7858a87cb
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="lifo-with-physical-value-and-marking"></a>LIFO ar fizisko vērtību un iezīmēšanu

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Pēdējais iesūtītais, Pirmais izsūtītais (pretsecība) ir krājumu modelis, kurā pēdējās (jaunākās) saņemšanas tiek izdotas vispirms. Izdotais krājums nosedz pirmo saņemto krājumu, ņemot vērā krājumu darbības veikšanas fizisko datumu. 

Krājuma modelī Pēdējais saņemtais, Pirmais izdotais (Last in, First out — LIFO) pēdējās (visjaunākās) saņemtās vienības tiek izdotas pirmās. Krājuma vienību izdošana nosedz pēdējo krājuma vienību saņemšanu pēc krājumu transakcijas datuma. Ja tiek izmantots LIFO modelis, var neizmantot LIFO modeļa kārtulu. Tā vietā var atzīmēt krājuma transakcijas tā, lai konkrēta krājuma izdošanas transakcija tiek segta ar konkrētu saņemšanas transakciju. Ja lietojat pretsecības krājumu modeli, ieteicam periodiski veikt krājumu slēgšanu. 

Tālākie piemēri parāda LIFO ietekmi, to lietojot trīs dažādos konfigurācijas veidos:

-   LIFO bez opcijas **Iekļaut fizisko vērtību**
-   LIFO ar opciju **Iekļaut fizisko vērtību**
-   LIFO ar atzīmi

## <a name="lifo-without-the-include-physical-value-option"></a>Pretsecība bez opcijas Iekļaut fizisko vērtību
Šajā FIFO piemērā krājumu modeļa grupa nav marķēta fizisko vērtību iekļaušanai. Sekojošajā ilustrācijā tiek parādītas šīs darbības:

-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 20,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   4.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 30,00 katrs.
-   5.a Krājumu fiziskā izdošana daudzumam 1, kur katra izmaksu cena ir USD 20,00 (darbinot finansiāli atjaunināto darbību vidējo rādītāju).
-   5.b Krājumu finansiālā izdošana daudzumam 1, kur katra izmaksu cena ir USD 20,00 (darbinot finansiāli atjaunināto darbību vidējo rādītāju).
-   6. Tiek veikta krājumu slēgšana. Pēc LIFO metodes pēdējā finansiāli atjauninātā izdošanas transakcija tiek nosegta ar pēdējo finansiāli atjaunināto saņemšanas transakciju. Šīs izdošanas darbībai tiks veikts USD 10,00 pārrēķins.

Jaunā faktiskā vidējo izmaksu cena attiecas uz finansiāli atjaunināto transakciju vidējo vērtību USD 15,00. Nākamajā attēlā ir parādīta LIFO krājumu modeļa ietekme uz šo transakciju sēriju, ja netiek izmantota opcija **Iekļaut fizisko vērtību**. ![LIFO bez fizisko vērtību iekļaušanas](./media/lifowithoutincludephysicalvalue.gif) 

**Diagrammas atslēga**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unit cena.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība netika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="lifo-with-the-include-physical-value-option"></a>Pretsecība ar opciju Iekļaut fizisko vērtību
Ja krājumam lapā **Krājumu modeļu grupas** ir atzīmēta izvēles rūtiņa **Iekļaut fizisko vērtību**, sistēmā faktiskās vidējās izmaksu cenas aprēķinam tiek izmantotas gan fiziskās, gan finansiālās ieejas plūsmas transakcijas. Kur nepieciešams, sistēma veic korekcijas arī fiziski apstrādātajām izdošanas darbībām. Ja izvēles rūtiņa **Iekļaut fizisko vērtību** nav atlasīta, tad krājumu slēgšanas ar LIFO krājumu modeli veiks nosegšanu tikai finansiāli apstrādātiem darījumiem. 

Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas.

-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 20,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   4.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 30,00 katrs.
-   5.a Krājuma fiziska izdošana par daudzumu 1 par izmaksu cenu USD 21,25 katrs (aprēķinot finansiāli un fiziski atjaunināto darbību vidējo).
-   5.b Krājuma finansiālā izdošana par daudzumu 1 par izmaksu cenu USD 21,25 katrs (aprēķinot finansiāli un fiziski atjaunināto darbību vidējo).
-   6.a Krājuma fiziska saņemšana par daudzumu 1 par summu USD 21,25 katrs.
-   7. Tiek veikta krājumu slēgšana. Pēc LIFO metodes pēdējā izdošanas transakcija tiek koriģēta vai segta ar pēdējo atjaunināto saņemšanas transakciju.

Transakcija 6a tiek koriģēta atbilstoši saņemšanas transakcijai 4b. Sistēmā šīs transakcijas netiek segtas, jo saņemšana tiek atjaunināta fiziski, bet ne finansiāli. Tāpēc fiziskās izdošanas darbībai tiks grāmatots tikai USD 8,75 pārrēķins. Transakcija 5b tiek koriģēta atbilstoši saņemšanas transakcijai 3a. Sistēmā šīs transakcijas netiek segtas, jo tās abas nav atjauninātas finansiāli. Tāpēc šī izdošanas transakcija tiek tikai koriģēta ar vērtību USD –3,75. Jauna spēkā esošā vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 20,00. 

Sekojošā ilustrācija parāda LIFO krājumu modeļa ietekmi uz šo darbību sēriju, kad tiek izmantota opcija **Iekļaut fizisko vērtību**. ![LIFO ar fizisko vērtību iekļaušanu](./media/lifowithincludephysicalvalue.gif) 

**Diagrammas atslēga**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unit cena.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība netika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="lifo-with-marking"></a>LIFO ar atzīmi
Atzīmēšana ir process, kas sniedz iespēju saistīt jeb atzīmēt izdošanas transakciju ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā tas ir steidzams pasūtījums, lai izpildītu debitora lūgumu, par šo krājumu jāmaksā vairāk. 

Jāpārbauda, vai krājuma vienības cena šajā pārdošanas pasūtījuma rēķinā tiek iekļauta peļņas aprēķinā vai pārdoto preču pašizmaksā (COGS). Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja šis pārdošanas dokuments ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina iegrāmatošanas, tad COGS būs USD 120,00, nevis pašreizējas krājuma vidējas izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena. 

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas. 

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pirms transakcijas grāmatošanas. To var paveikt no pārdošanas pasūtījuma rindas, lapā **Pārdošanas pasūtījuma informācija**. Jūs varat skatīt atvērtās saņemšanas darbības lapā **Iezīmēšana**. 

Varat arī iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu. 

Sekojošajā ilustrācijā tiek parādītas šīs darbības:

-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 20,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   4.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 30,00 katrs.
-   5.a Krājuma fiziska izdošana par daudzumu 1 par izmaksu cenu USD 21,25 katrs (aprēķinot finansiāli un fiziski atjaunināto darbību vidējo).
-   5.b Krājumu finansiāla izdošana ar daudzumu 1 tiek nozīmēta krājumu saņemšanas darbībai 2.b pirms darbība tiek iegrāmatota. Šī darbība tik grāmatota ar izmaksas cenu USD 20,00 katram.
-   6.a Krājuma fiziska saņemšana par daudzumu 1 par summu USD 21,25 katrs.
-   7. Tiek veikta krājumu slēgšana. Tādēļ, ka finansiāli apstrādātā FIFO darbība tiek nozīmēta esošajai saņemšanai, tad šīs darbības tiek nosegtas viena ar otru un netiek veiktas nekādas korekcijas.

Jauna spēkā esošā vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50. 

Sekojošajā ilustrācijā redzama šī darījumu sērija ar ietekmi, ko rada LIFO krājumu modeļa izvēle ar nozīmēšanu starp izsniegšanas un saņemšanas darījumiem. ![LIFO ar apzīmējumu](./media/lifowithmarking.gif) 

**Diagrammas atslēga**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unit cena.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība netika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.





