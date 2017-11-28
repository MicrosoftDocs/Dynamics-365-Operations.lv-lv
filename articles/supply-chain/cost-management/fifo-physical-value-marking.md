---
title: "FIFO ar fizisko vērtību un iezīmēšanu"
description: "Pirmie iekšā, pirmie ārā (FIFO) ir krājumu modelis, kur pirmie saņemtie krājumi tiek arī pirmie izdoti. Finansiāli apstrādātie izdotie krājumi tiek nosegti ar pirmajiem finansiāli apstrādātajiem saņemtajiem krājumiem saskaņā ar krājumu darbību finansiālo datumu."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2d3a6c412e497952c0c7f5b113990bbe693b0f22
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="fifo-with-physical-value-and-marking"></a>FIFO ar fizisko vērtību un iezīmēšanu

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Pirmie iekšā, pirmie ārā (FIFO) ir krājumu modelis, kur pirmie saņemtie krājumi tiek arī pirmie izdoti. Finansiāli apstrādātie izdotie krājumi tiek nosegti ar pirmajiem finansiāli apstrādātajiem saņemtajiem krājumiem saskaņā ar krājumu darbību finansiālo datumu. 

Lietojot FIFO metodi, varat izvēlēties neizmantot FIFO noteikumus. Tā vietā, varat atzīmēt krājuma darbības tā, lai atsevišķa saņemšanas darbība tiktu segta ar atsevišķu izdošanas darbību. Ja lietojat FIFO krājumu modeli, ieteicam periodiski veikt krājumu slēgšanu. Tālākie piemēri parāda FIFO ietekmi, to lietojot trīs dažādos konfigurācijas veidos:

-   FIFO bez opcijas **Iekļaut fizisko vērtību**
-   FIFO ar opciju **Iekļaut fizisko vērtību**
-   FIFO ar iezīmēšanu

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO bez opcijas Iekļaut fizisko vērtību
Šajā FIFO piemērā krājumu modeļa grupa nav marķēta fizisko vērtību iekļaušanai. Sekojošajā ilustrācijā tiek parādītas šīs darbības:

-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 2 pie cenas USD 10,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 2 par summu USD 10,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   4.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 30,00 katrs.
-   5.a Krājumu fiziskā izdošana daudzumam 1, kur katra izmaksu cena ir USD 20,00 (darbinot finansiāli atjaunināto darbību vidējo rādītāju).
-   5.b Krājumu finansiālā izdošana daudzumam 1, kur katra izmaksu cena ir USD 20,00 (darbinot finansiāli atjaunināto darbību vidējo rādītāju).
-   6. Tiek veikta krājumu slēgšana. Balstoties uz FIFO metodi, pirmā finansiāli apstrādātā izdošana tiks nosegta ar pirmo finansiāli apstrādāto saņemšanu. Šīs izdošanas darbībai tiks veikts USD –10,00 pārrēķins.

Jaunā aprēķinātā vidēja izmaksu cena ietekmē finansiāli atjaunoto darījumu vidējo rādītāju. Sekojošās ilustrācijas parāda FIFO krājumu modeļa ietekmi uz šo darbību sēriju, kad opcija **Iekļaut fizisko vērtību** netiek izmantota. ![FIFO bez fizisko vērtību iekļaušanas](./media/fifowithoutincludephysicalvalue.gif) 

**Diagrammas atslēga**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība netika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO ar fizisko vērtību iekļaušanas opciju
Ja krājumam lapā **Krājumu modeļu grupa** ir atzīmēta izvēles rūtiņa **Iekļaut fizisko vērtību**, sistēmā faktiskās vidējās izmaksu cenas aprēķinam tiek izmantotas gan fiziskās, gan finansiālās ieejas plūsmas transakcijas. Kur nepieciešams, sistēma veic korekcijas arī fiziski apstrādātajām izdošanas darbībām. Ja izvēles rūtiņa **Iekļaut fizisko vērtību** nav atlasīta, tad krājumu slēgšanas ar FIFO krājumu modeli veiks nosegšanu tikai finansiāli apstrādātiem darījumiem. Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas.

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
-   7. Tiek veikta krājumu slēgšana. Balstoties uz FIFO metodi, pirmais finansiālais izdošanas darījums tiks pielāgots vai nosegts ar pirmo apstrādāto saņemšanas darbību, finansiālu vai fizisku.

Ar darījumu 5b tiks nosegta saņemšanas darbība 1b. Šai izdošanas darbībai būs korekcija USD –11,25 apjomā. Jauna spēkā esošā vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50. Sekojošā ilustrācija parāda FIFO krājumu modeļa ietekmi uz šo darbību sēriju, kad tiek izmantota opcija **Iekļaut fizisko vērtību**. ![FIFO ar fizisko vērtību iekļaušanu](./media/fifowithincludephysicalvalue.gif) 

**Diagrammas atslēga**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība netika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.

## <a name="fifo-with-marking"></a>FIFO ar iezīmēšanu
Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā tas ir steidzams pasūtījums, lai izpildītu debitora lūgumu, par šo krājumu jāmaksā vairāk. Jāpārbauda, vai krājuma vienības cena šajā pārdošanas pasūtījuma rēķinā tiek iekļauta peļņas aprēķinā vai pārdoto preču pašizmaksā (COGS). Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja šis pārdošanas dokuments ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina iegrāmatošanas, tad COGS būs USD 120,00, nevis pašreizējas krājuma vidējas izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena. Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas. Kad ieejas plūsmas transakcija atbilst izejas plūsmas transakcijai, tad tiek ignorēta krājumu modeļu grupai definētā novērtēšanas metode un sistēma savstarpēji sedz šīs transakcijas. Varat atzīmēt saņemšanas darbībai paredzēto izdošanas darbību pirms darbība tiek grāmatota. To var paveikt no pārdošanas pasūtījuma rindas, lapā **Pārdošanas pasūtījuma informācija**. Jūs varat skatīt atvērtās saņemšanas darbības lapā **Iezīmēšana**. Varat arī iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu. Sekojošajā ilustrācijā tiek parādītas šīs darbības:

-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 20,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   4.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 30,00 katrs.
-   5.a Krājuma fiziska izdošana par daudzumu 1 par izmaksu cenu USD 21,25 katrs (aprēķinot finansiāli un fiziski atjaunināto darbību vidējo).
-   5.b Krājumu finansiāla izdošana ar daudzumu 1 tiek nozīmēta krājumu saņemšanas darbībai 2.b pirms darbība tiek iegrāmatota. Šī darbība tiek iegrāmatota ar izmaksu cenu USD 20,00.
-   6.a Krājuma fiziska saņemšana par daudzumu 1 par summu USD 21,25 katrs.
-   7. Tiek veikta krājumu slēgšana. Tādēļ, ka finansiāli apstrādātā FIFO darbība tiek nozīmēta esošajai saņemšanai, tad šīs darbības tiek nosegtas viena ar otru un netiek veiktas nekādas korekcijas.

Jauna spēkā esošā vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50. Sekojošajā ilustrācijā redzama šī darījumu sērija ar ietekmi, ko rada FIFO krājumu modeļa izvēle ar nozīmēšanu starp izsniegšanas un saņemšanas darījumiem. ![FIFO ar apzīmējumu](./media/fifowithmarking.gif) 

**Diagrammas atslēga**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs (vai zem) katras vertikālas bultas ir norādīta krājumu transakcijas vērtība šādā formātā: Quantity@Unitprice.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība tika iegrāmatota krājumā fiziski.
-   Krājuma darbības vērtība iekavās norāda, ka krājuma darbība netika iegrāmatota krājumā finansiāli.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas ir veiktas, noslēdzot krājumus, un atzīmētas ar sarkanām diagonālām punktlīnijas bultām, kas savieno saņemšanu un izdošanu.





