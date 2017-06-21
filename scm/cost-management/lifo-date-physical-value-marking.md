---
title: "LIFO uz datums ar fizisko vērtību un iezīmēšanu"
description: "Pēdējie iekšā, pirmie ārā uz datumu (LIFO uz datumu) ir krājumu modelis, kura pamatā ir LIFO princips. Izdotais krājums nosedz pirmo saņemto krājumu, ņemot vērā krājumu darbības veikšanas fizisko datumu. Izmantojot vienumu LIFO datums, ja pirms izdošanas nav nevienas saņemšanas, izdošana nosedz jebkuru saņemšu, kas rodas pēc izdošanas datuma. Vairākas izdošanas vienā un tajā pašā datumā ir jānosedz secībā – pēdējā izdošana, pēdējā saņemšana."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 96089fed3e8b522fb3a8646ffd87fadff8fe1f3e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO uz datums ar fizisko vērtību un iezīmēšanu

[!include[banner](../includes/banner.md)]


Pēdējie iekšā, pirmie ārā uz datumu (LIFO uz datumu) ir krājumu modelis, kura pamatā ir LIFO princips. Izdotais krājums nosedz pirmo saņemto krājumu, ņemot vērā krājumu darbības veikšanas fizisko datumu. Izmantojot vienumu LIFO datums, ja pirms izdošanas nav nevienas saņemšanas, izdošana nosedz jebkuru saņemšu, kas rodas pēc izdošanas datuma. Vairākas izdošanas vienā un tajā pašā datumā ir jānosedz secībā – pēdējā izdošana, pēdējā saņemšana. 

Ja izmantojat krājumu modeli Pēdējie iekšā, pirmie ārā uz datumu (LIFO uz datums) un pirms izejas plūsmas nav nevienas ieejas plūsmas, izejas plūsma tiek segta ar jebkuru ieejas plūsmu pēc izejas plūsmas datuma. Vairākas izejas plūsmas vienā un tajā pašā datumā var segt šādā secībā: pēdējā izejas plūsma, pirmā ieejas plūsma. Ja izmantojat LIFO uz datumu, nav jāizmanto LIFO uz datumu kārtula. Tā vietā, varat atzīmēt krājuma darbības tā, lai atsevišķa saņemšanas darbība tiktu segta ar atsevišķu izdošanas darbību. 

Ja lietojat Pretsecības datuma krājumu modeli, ieteicam periodiski veikt krājumu slēgšanu. 

Tālāk sniegtajos piemēros ir parādīta ietekme, ko rada LIFO uz datumu izmantošana trīs konfigurācijās.

-   LIFO uz datumu, neizmantojot opciju **Iekļaut fizisko vērtību**
-   LIFO uz datumu, izmantojot opciju**Iekļaut fizisko vērtību**
-   LIFO datums ar atzīmi

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO datums bez opcijas Fizisko vērtību iekļaušana
Šajā FIFO piemērā krājumu modeļa grupa nav marķēta fizisko vērtību iekļaušanai. Sekojošajā ilustrācijā tiek parādītas šīs darbības:

-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 20,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziskā izejas plūsma — daudzums: 1, izmaksu cena: USD 15,00 (finansiāli atjaunināto transakciju kārtējās vidējās izmaksas).
-   4.b Krājumu finanšu izejas plūsma — daudzums: 1, izmaksu cena: USD 15,00. (finansiāli atjaunināto transakciju kārtējās vidējās izmaksas).
-   5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   6. Tiek veikta krājumu slēgšana. Pamatojoties uz LIFO uz datumu metodi, pēdējā finansiāli atjauninātā izejas plūsma tiks segta ar pēdējo finansiāli atjaunināto ieejas plūsmu atbilstoši datumam. Izdošanas darbībai tiks veikta korekcija USD 5,00 apmērā. Šīs transakcijas tiks segtas viena ar otru.

Jaunā aktīvā vidējā izmaksu cena ataino finansiāli atjaunināto darbību vidējo vērtību pie USD 15,00. 

Tālāk redzamajā ilustrācija ir parāda ietekme, ko rada LIFO uz datumu krājumu modeļa izmantošana, ja netiek izmantota opcija **Iekļaut fizisko vērtību**. ![LIFO datums ar fizisko vērtību iekļaušanu](./media/lifodatewithoutincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO datums ar opciju Fizisko vērtību iekļaušana
Varat atzīmēt krājuma izvēles rūtiņu **Iekļaut fizisko vērtību** lapā **Krājumu modeļu grupas**. Šādā gadījumā sistēmā faktiskās vidējās izmaksu cenas aprēķināšanai tiek izmantotas gan fiziskās, gan finansiālās ieejas plūsmas transakcijas. Kur nepieciešams, sistēma veic korekcijas arī fiziski apstrādātajām izdošanas darbībām. Ja ir noņemta atzīme no izvēles rūtiņas **Iekļaut fizisko vērtību**, tad, veicot krājumu slēgšanu ar LIFO uz datumu krājumu modeli, tiek veikta tikai finansiāli atjaunināto transakciju segšana. 

Šajā piemērā krājumu modeļu grupai ir atzīmēta fiziskās vērtības iekļaušana. 

Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas.

-   1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
-   1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
-   2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
-   2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 20,00 katrs.
-   3.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
-   4.a Krājumu fiziskā izdošana daudzumam 1, kur katra izmaksu cena ir USD 18,33 (darbinot finansiāli atjaunināto darbību vidējo rādītāju).
-   4.b Krājumu finanšu izejas plūsma — daudzums: 1, vienības izmaksu cena: USD 18,33 (finansiāli atjaunināto transakciju kārtējās vidējās izmaksas).
-   5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
-   6. Tiek veikta krājumu slēgšana. Pamatojoties uz LIFO uz datumu metodi, pēdējā atjauninātā izejas plūsma tiks koriģēta vai segta ar pēdējo atjaunināto ieejas plūsmu atbilstoši datumam. Šīs transakcijas netiks segtas viena ar otru, jo finanšu ieejas plūsmas transakcija ir koriģēta ar fiziskās atjaunināšanas transakciju. Tā vietā izejas plūsmas transakcijai tiks veikta tikai korekcija USD 6,67 apmērā.

Jaunā aktīvā vidējā izmaksu cena ataino finansiāli atjaunināto darbību vidējo vērtību pie USD 20,00. 

Tālāk redzamajā ilustrācija ir parāda ietekme, ko rada LIFO krājumu modeļa izmantošana, ja tiek izmantota opcija **Iekļaut fizisko vērtību**. ![LIFO datums ar fizisko vērtību iekļaušanu](./media/lifodatewithincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-marking"></a>LIFO datums ar atzīmi
Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. 

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā tas ir steidzams pasūtījums, lai izpildītu debitora pieprasījumu, par šo krājumu ir jāmaksā vairāk. Jāpārbauda, vai krājuma vienības cena šajā pārdošanas pasūtījuma rēķinā tiek iekļauta peļņas aprēķinā vai pārdoto preču pašizmaksā (COGS). 

Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja šis pārdošanas dokuments ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina iegrāmatošanas, tad COGS būs USD 120,00, nevis pašreizējas krājuma vidējas izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena. 

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas. 

Piemēram, ieejas plūsmas transakcija ir iezīmējot saistīta ar izejas plūsmas transakciju. Šādā gadījumā tiek ignorēta krājuma vienības krājumu modeļu grupai definētā novērtēšanas metode un sistēmā šī transakcijas tiek segtas viena ar otru. 

Varat atzīmēt saņemšanas darbībai paredzēto izdošanas darbību pirms darbība tiek grāmatota. To var paveikt no pārdošanas pasūtījuma rindas, lapā **Pārdošanas pasūtījuma informācija**. Jūs varat skatīt atvērtās saņemšanas darbības lapā **Iezīmēšana**. 

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
-   7. Tiek veikta krājumu slēgšana. Tā kā finansiāli atjauninātā FIFO (pirmie iekšā, pirmie ārā) transakcija ir iezīmējot saistīta ar esošu ieejas plūsmu, šīs transakcijas tiek segtas viena ar otru un netiek veiktas nekādas korekcijas.

Jauna pašreizēja vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50. 

Tālāk redzamajā ilustrācija ir parāda ietekme, ko rada LIFO krājumu modeļa izmantošana, ja tiek izmantota izejas un ieejas plūsmu saistīšana iezīmējot. ![LIFO datums ar apzīmējumu](./media/lifodatewithmarking.gif) 

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





