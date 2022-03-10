---
title: LIFO datums ar fizisku vērtību un marķējumu
description: Pēdējais iekšā, Pirmais izejas datums (LIFO datums) ir krājumu modelis, kura pamatā ir LIFO princips. Izdotais krājums nosedz pirmo saņemto krājumu, ņemot vērā krājumu darbības veikšanas fizisko datumu. Izmantojot LIFO datumu, ja pirms emisijas nav ieejas plūsmas, izejas plūsma tiek nosegta ar visām ieejas plūsmām, kas rodas pēc emisijas datuma. Vairākas izdošanas vienā un tajā pašā datumā ir jānosedz secībā – pēdējā izdošana, pēdējā saņemšana.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6f5f447724ace473bece3007a96c4b56e90a908
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330280"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO datums ar fizisku vērtību un marķējumu

[!include [banner](../includes/banner.md)]

Pēdējais sākuma datums (LIFO datums) ir krājumu pārvaldības un vērtēšanas metode, kurā vispirms tiek pārdoti, izmantoti vai atsavināti krājumi, kas ražoti vai iegūti pēdējie. Krājumu slēgšanas procesa laikā programmā Microsoft Dynamics 365 Supply Chain Management sistēma izveidos nosegšanas darbības, kurās pēdējā ieejas plūsma tiek saskaņota ar katra norādītā datuma pirmo izejas plūsmu, sākot ar vecāko datumu vispirms utt. Ja izmantojat pēdējo krājumu modeli, pirmais izejas datums (LIFO datums), ja pirms izejas plūsmas nav ieejas plūsmas, izejas plūsma tiek nosegta pret visām ieejas plūsmām, kas rodas pēc izejas plūsmas datuma. Nosegšanas un atbilstības princips ir balstīts uz krājumu darbību finanšu datumu. Ja vienā un tajā pašā datumā ir vairāki jautājumi, tie tiek atrisināti pēdējās izdošanas, pēdējās kvīts secībā. Nosegšanas un korekciju iepriekšēju novērtējumu var veikt, palaižot krājumu pārrēķināšanas procesu.

Lifo datuma principu var ignorēt, atzīmējot krājumu darbības, lai noteikta krājumu ieejas plūsma tiktu nosegta ar noteiktu izejas plūsmu. Periodiska krājumu slēgšana ir nepieciešama, ja izmantojat LIFO datuma krājumu modeli, lai izveidotu nosegšanas darbības un pielāgotu izejas plūsmas vērtību atbilstoši LIFO principam. Līdz krājumu slēgšanas procesa palaišanai izejas plūsmas darbības tiek novērtētas pēc izpildes vidējā, kad notika fiziskie un finanšu atjauninājumi. Ja vien neizmantojat iezīmēšanu, izpildes vidējais tiek aprēķināts, kad tiek veikts fiziskais vai finanšu atjauninājums.

Lietojot LIFO datuma krājumu modeli, ieteicams periodiski slēgt krājumus.

Tālāk sniegtajos piemēros ir parādīts LIFO datuma izmantošanas efekts trīs konfigurācijās:

- LIFO datums bez **opcijas Iekļaut fizisko vērtību**
- LIFO datums ar opciju **Iekļaut fizisko vērtību**
- LIFO datums ar marķējumu

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO datums bez opcijas Iekļaut fizisko vērtību

Šajā FIFO piemērā krājumu modeļa grupa nav marķēta fizisko vērtību iekļaušanai. Sekojošajā ilustrācijā tiek parādītas šīs darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli iegrāmatoto darbību izpildes vidējais rādītājs).
- 3.b Krājumu finanšu izejas plūsma daudzumam 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziskā izejas plūsma daudzumam 1 ar izmaksu cenu USD 23.00 (finansiāli grāmatoto darbību izpildes vidējais rādītājs)
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz LIFO datuma metodi, pirmā finansiāli atjauninātā izejas plūsma tiks atrisināta pret pēdējo finansiāli atjaunināto ieejas plūsmu, sākot no pirmā datuma utt. Šajā piemērā tiek izveidota viena nosegšana no 3.b līdz 2.b klasei. USD 6.00 korekcija tiks veikta līdz 3.b klasei, un no tā izrietošās galīgās izmaksas tiks USD 22.00.

Nākamajā attēlā ir parādīta LIFO datumu krājumu modeļa ietekme, **ja netiek izmantota opcija Iekļaut fizisko vērtību**.

![LIFO datums bez opcijas Iekļaut fizisko vērtību.](media/lifo-date-without-include-physical-value.png)

**Diagrammas atslēga**

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO datums ar opciju Iekļaut fizisko vērtību

**Ja lapā Krājumu modeļu grupas** krājumam **ir atzīmēta izvēles rūtiņa Iekļaut fizisko vērtību**, sistēma izmanto gan fiziskās, gan finanšu ieejas plūsmas darbības, lai aprēķinātu darbojošos vidējo izmaksu cenu. Attiecīgā gadījumā sistēma pielāgo arī fiziski atjaunināto emisijas darījumu. **Kad izvēles rūtiņa Iekļaut fizisko vērtību** ir notīrīta, krājumu slēgšana, kas izmanto LIFO datuma krājumu modeli, veic nosegšanas darbības tikai tām darbībām, kas ir finansiāli atjauninātas.

Šajā piemērā krājumu modeļu grupai ir atzīmēta fiziskās vērtības iekļaušana. 

Tālāk esošajā ilustrācijā ir redzamas tālāk norādītās transakcijas:

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
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz LIFO datuma metodi, pirmā finansiāli atjauninātā izejas plūsma tiks atrisināta pret pēdējo finansiāli atjaunināto kvīti par katru datumu, kas sākas pirmajā datumā utt. Šajā piemērā tiek izveidota viena nosegšana no 2.b līdz 3.b klasei. USD 6.00 korekcija tiks veikta līdz 3.b klasei, un no tā izrietošās galīgās izmaksas tiks USD 22.00. Turklāt 6.a darbība tiks koriģēta atbilstoši ieejas plūsmas darījuma izmaksām 5.b. Sistēma nenorēķināsies ar šīm darbībām, jo kvīts tiek atjaunināta fiziski, bet ne finansiāli. Tā vietā fiziskās izejas plūsmas darbībai tiks grāmatota tikai USD 6.33 korekcija, un iegūtās koriģētās izmaksas tiks USD 30.00.

Tālāk redzamajā ilustrācija ir parāda ietekme, ko rada LIFO krājumu modeļa izmantošana, ja tiek izmantota opcija **Iekļaut fizisko vērtību**.

![LIFO datums ar opciju Iekļaut fizisko vērtību.](media/lifo-date-with-include-physical-value.png)

**Diagrammas atslēga**

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

## <a name="lifo-date-with-marking"></a>LIFO datums ar marķējumu

Atzīmēšana ir process, kas sniedz iespēju izdošanas transakciju saistīt jeb atzīmēt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā šis pasūtījums ir steidzīgs pasūtījums, jums ir jāmaksā vairāk par preci, lai izpildītu klienta pieprasījumu.

Ir jāpārliecinās, vai krājuma izmaksas tiek atspoguļotas pārdošanas pasūtījuma rēķina uzcenojumā vai pārdoto preču (PPP) izmaksās. Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Ja šis pārdošanas dokuments ir atzīmēts kā pirkšanas pasūtījums pirms pavadzīmes vai rēķina iegrāmatošanas, tad COGS būs USD 120,00, nevis pašreizējas krājuma vidējas izmaksas. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena.

Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas.

Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pirms transakcijas grāmatošanas. Šo marķēšanu var veikt no pārdošanas pasūtījuma rindas lapā Detalizēta informācija **par** pārdošanas pasūtījumu, kopsavilkuma cilnē Pārdošanas pasūtījuma rindas **atlasot \> Krājumu** marķēšana **·**. Varat skatīt atvērtās ieejas plūsmas transakcijas lapā **Iezīmēšana**.

Varat arī iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu.

Sekojošajā ilustrācijā tiek parādītas šīs darbības:

- 1.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 10,00 par katru.
- 1.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 10,00 katrs.
- 2.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 20,00 par katru.
- 2.b Krājuma finansiāla saņemšana par daudzumu 1 par summu USD 22,00 katrs.
- 3.a Krājumu fiziskā izejas plūsma par daudzumu 1 ar izmaksu cenu USD 16.00 (finansiāli iegrāmatoto darbību izpildes vidējais rādītājs).
- 3.b Krājumu finanšu izejas plūsma daudzumam 1 ar izmaksu cenu USD 16.00 (finansiāli grāmatoto darbību izpildes vidējais rādītājs).
- 3.c Krājumu finanšu izejas plūsma 3b ir atzīmēta ar krājumu finanšu izejas plūsmu 1b.
- 4.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 25,00 par katru.
- 5.a Krājumu fiziska saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 5.b Krājumu finansiāla saņemšana daudzumam 1 pie cenas USD 30,00 par katru.
- 6.a Krājumu fiziskā izejas plūsma daudzumam 1 ar izmaksu cenu USD 23.00 (finansiāli grāmatoto darbību izpildes vidējais rādītājs)
- 7\. Tiek veikta krājumu slēgšana. Pamatojoties uz marķēšanas principu, kas izmanto LIFO datuma metodi, atzīmētās darbības tiek nosegtas viena pret otru. Šajā piemērā 3b tiek nosegts pret 1b, un korekcija USD -6.00 tiek grāmatota uz 3.b, lai vērtība tiktu USD 10.00. Šajā piemērā papildu nosegšana netiek veikta, jo slēgšana izveido nosegšanas darbības tikai finansiāli atjauninātām darbībām.

Šajā attēlā ir parādīta LIFO datuma krājumu modeļa ietekme, ja tiek izmantota iezīmēšana starp izejas plūsmām un ieejas plūsmām. 

![LIFO datums ar marķējumu.](media/lifo-date-with-marking.png)

**Diagrammas atslēga**

- Krājuma darbības ir atzīmētas ar vertikālām bultām.
- Fiziskās darbības attēlo īsākas gaiši pelēkas bultiņas.
- Finanšu darījumus attēlo garākas melnas bultiņas.
- Ieejas plūsmas krājumos tiek attēlotas ar vertikālām bultiņām virs ass.
- Izejas plūsmas no krājumiem tiek attēlotas ar vertikālām bultiņām zem ass.
- Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
- Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
- Katrs diagrammas datums ir atdalīts ar plānu melnu vertikālu līniju. Datums ir atzīmēts diagrammas apakšā.
- Krājumu slēgšana tiek attēlota ar sarkanu vertikālu pārtrauktu līniju.
- Nosegšanas un atzīmes, ko veic krājumu slēgšana, tiek attēlotas ar sarkanām diagonālām pārtrauktām bultiņām, kas pāriet no ieejas plūsmas uz izejas plūsmu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
