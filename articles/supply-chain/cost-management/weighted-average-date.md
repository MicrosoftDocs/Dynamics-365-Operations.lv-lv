---
title: "Vidējā svērtā uz datumu"
description: "Svērtais vidējais datums ir krājumu modelis, kas balstīts uz svērto vidējo principu, kur izsniegšanas no krājumiem tiek vērtētas pie vidējās krājumu vērtības, kas inventarizācijā saņemta katrai atsevišķai dienai krājumu slēgšanas periodā."
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a258c7d6314546262a3f9d07d06da5cad797d99b
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="weighted-average-date"></a>Vidējā svērtā uz datumu

[!INCLUDE [banner](../includes/banner.md)]

[!INCLUDE [retail name](../includes/retail-name.md)]

Svērtais vidējais uz datumu ir krājumu modelis, kura pamatā ir svērtā vidējā princips. Izmantojot svērtā vidējā principu, krājumu izejas plūsmas tiek novērtētas atbilstoši krājumu ieejas plūsmu vidējai vērtībai katrā atsevišķā dienā krājumu slēgšanas perioda laikā. 

Veicot krājumu slēgšanu, izmantojot svērto vidējo uz datumu, visas dienas ieejas plūsmas tiek segtas ar virtuālu izejas plūsmu. Šī virtuālā izejas plūsma satur kopējo ieejas plūsmas daudzumu un vērtību šajā dienā. Virtuālajai izejas plūsmai ir atbilstoša virtuālā ieejas plūsma, ar ko tiks segta izejas plūsma. Tāpēc visām izejas plūsmām ir vienādas vidējās izmaksas. Virtuālo izejas plūsmu un virtuālo ieejas plūsmu var uzskatīt par virtuālu pārsūtīšanu, ko sauc par *svērtā vidējā krājumu slēgšanas pārsūtīšanu*. 

Ja konkrētajā datumā vai pirms tā ir bijusi tikai viena ieejas plūsma, vidējā vērtība nav jāaprēķina. Tā kā visas izejas plūsmas tiek segtas ar šo ieejas plūsmu, virtuālā pārsūtīšana netiek izveidota. Tāpat, ja konkrētajā datumā ir bijušas tikai izejas plūsmas un nav bijusi neviena ieejas plūsma, no kā var aprēķināt vidējo vērtību, virtuālā pārsūtīšana netiek izveidota. Ja izmantojat svērto vidējo uz datumu, varat iezīmēt krājumu transakcijas, lai noteikta krājumu ieejas plūsma tiktu segta ar noteiktu izejas plūsmu. Šādā gadījumā netiek izmantota svērtā vidējā uz datumu kārtula. Ja izmantojat svērtā vidējā datuma krājumu modeli, ieteicama ikmēneša krājumu slēgšana. 

Vidējā svērtā datuma izmaksu aprēķināšanas metodei tiek izmantota tālāk norādītā formula. 

Svērtais vidējais = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q*n* × P*n*\]) ÷ (Q1 + Q2 + Q*n*) 

Krājumu slēgšanas laikā aprēķins tiek veikts katru dienu visā slēgšanas perioda laikā, kā parādīts nākamajā attēlā. 

![Vidējā svērtā datuma ikdienas aprēķina modelis](./media/weightedaveragedatedailycalculationmodel.gif) 

Krājumu izejas plūsmas transakcijas, piemēram, pārdošanas pasūtījumi, krājumu žurnāli un ražošanas pasūtījumi, tiek veiktas, izmantojot novērtēto izmaksu cenu grāmatošanas datumā. Šī novērtēto izmaksu cena tiek saukta arī par kārtējo vidējo izmaksu cenu. Krājumu slēgšanas dienā sistēmā tiek analizētas krājumu transakcijas par iepriekšējiem periodiem, iepriekšējām dienām un pašreizējo dienu. Šī analīze tiek izmantota, lai noteiktu, kurš no tālāk norādītajiem slēgšanas principiem ir jāizmanto.

-   Tieša segšana
-   Apkopota segšana

Segšanas ir krājuma slēgšanas iegrāmatojumi, kuri koriģē izdošanas pēc svērtā vidējā saskaņā ar slēgšanas datumu. 

**Piezīme.** Papildinformāciju par segšanu skatiet rakstā par krājumu slēgšanu. Tālāk sniegtajos piemēros ir parādīta ietekme, ko rada svērtā vidējā izmantošana piecās konfigurācijās.

-   Svērtā vidējā uz datumu tiešā segšana, ja netiek izmantota opcija **Iekļaut fizisko vērtību**
-   Svērtā vidējā uz datumu apkopotā segšana, ja netiek izmantota opcija **Iekļaut fizisko vērtību**
-   Svērtā vidējā uz datumu tiešā segšana, ja tiek izmantota opcija **Iekļaut fizisko vērtību**
-   Svērtā vidējā uz datumu apkopotā segšana, ja tiek izmantota opcija **Iekļaut fizisko vērtību**
-   Svērtais vidējais uz datumu, ja tiek izmantota iezīmēšana

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Svērtā vidējā uz datumu tiešā segšana, ja netiek izmantota opcija Iekļaut fizisko vērtību
Pašreizējā versijā tiek izmantots tas pats tiešās segšanas princips, kas tika izmantots svērtajam vidējam iepriekšējās versijās. Sistēmā tiek veikta ieejas plūsmas un izejas plūsmas tiešā segšana. Sistēma izmanto šo tiešās nosegšanas principu īpašās situācijās:

-   Perioda laikā ir iegrāmatota viena ieejas plūsma un viena vai vairākas izejas plūsmas.
-   Perioda laikā ir iegrāmatotas tikai izejas plūsmas, un ir pieejami rīcībā esošie krājumi no iepriekšējās slēgšanas.

Tālāk aprakstītajā scenārijā ir iegrāmatotas finansiāli atjauninātas ieejas un izejas plūsmas. Krājumu slēgšanas laikā sistēmā ieejas plūsma tiek tieši segta ar izejas plūsmu, un nav nepieciešams koriģēt izejas plūsmas izmaksu cenu. 

Šīs transakcijas ir attēlotas tālāk esošajā ilustrācijā.

-   1.a Tiek atjaunināta krājumu fiziskā ieejas plūsma — daudzums: 5, vienas vienības izmaksas: USD 10,00.
-   1.b Tiek atjaunināta krājumu finanšu ieejas plūsma — daudzums: 5, vienības izmaksas: USD 10,00.
-   2.a Tiek atjaunināta krājumu fiziskā izejas plūsma — daudzums: 2, vienības izmaksas: USD 10,00.
-   2.b Tiek atjaunināta krājumu finanšu izejas plūsma — daudzums: 2, vienības cena: USD 10,00.
-   3. Tiek veikta krājumu slēgšana, izmantojot tiešās segšanas metodi, lai segtu krājumu finanšu ieejas plūsmu ar krājumu finanšu izejas plūsmu.

![Novērtētā vidējā datuma tiešā nosegšana bez Iekļaut fizisko vērtību iespējas](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Attēla apzīmējumi:**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs vai zem katras vertikālās bultas ir norādīta krājumu transakcijas vērtība formātā *Daudzums*@*Vienības cena*.
-   Ja krājumu transakcijas vērtība ir ietverta iekavās, krājumu transakcija tiek fiziski iegrāmatota krājumos.
-   Ja krājumu transakcijas vērtība nav ietverta iekavās, krājumu transakcija tiek finansiāli iegrāmatota krājumos.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas tiek veiktas, slēdzot krājumus, ir apzīmētas ar sarkanām pārtrauktu līniju bultām, kas pa diagonāli savieno ieejas plūsmu un izejas plūsmu.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Svērtā vidējā uz datumu apkopotā segšana, ja netiek izmantota opcija Iekļaut fizisko vērtību
Svērtā vidējā pamatā ir princips, ka visas slēgšanas perioda laikā saņemtās ieejas plūsmas tiek apkopotas jaunā krājumu pārsūtīšanas transakcijā. Šī transakcija tiek saukta par *svērtā vidējā krājumu slēgšanu*. Visas ieejas plūsmas konkrētajā dienā tiek segtas ar jaunās krājumu pārsūtīšanas transakcijas izejas plūsmu. Visas izejas plūsmas konkrētajā dienā tiek segtas ar jaunās krājumu pārsūtīšanas transakcijas ieejas plūsmu. Ja pēc krājumu slēgšanas rīcībā esošo krājumu vērtība ir pozitīva, rīcībā esošie krājumi un krājumu vērtība tiek apkopti jaunās krājumu pārsūtīšanas transakcijas ieejas plūsmā. Ja pēc krājumu slēgšanas rīcībā esošo krājumu vērtība ir negatīva, rīcībā esošie krājumi un krājumu vērtība veido atsevišķo pilnībā nesegto izejas plūsmu summu. 

Tālāk aprakstītajā scenārijā perioda laikā ir grāmatotas vairākas finansiāli atjauninātas ieejas un izejas plūsmas. Krājumu slēgšanas laikā sistēmā tiek novērtēti dati par katru dienu, lai noteiktu, kā slēgšanas laikā apstrādāt katru dienu. 

Šīs transakcijas ir attēlotas tālāk esošajā ilustrācijā. 

**1. diena.**

-   1.a Tiek atjaunināta krājumu fiziskā ieejas plūsma — daudzums: 3, vienības izmaksas: USD 15,00.
-   1.b Tiek atjaunināta krājumu finanšu ieejas plūsma — daudzums: 3, vienības izmaksas: USD 15,00.
-   2.a Krājumu fiziska izsniegšana ar daudzumu 1 pie aprēķinātām vidējām izmaksām USD 15,00.
-   2.b Krājumu finansiāla saņemšana ar daudzumu 1 pie aprēķinātām vidējām izmaksām USD 15,00.

1. dienai sistēma izmanto tiešās nosegšanas metodi. 

**2. diena.**

-   3.a Krājumu fiziskā izejas plūsma — daudzums: 1, kārtējās vidējās izmaksas: USD 15,00
-   3.b Krājumu finanšu izejas plūsma — daudzums: 1, kārtējās vidējās izmaksas: USD 15,00

2. dienai sistēma izmanto tiešās nosegšanas paņēmienu. 

**3. diena.**

-   4.a Krājumu fiziskā izejas plūsma — daudzums: 1, kārtējās vidējās izmaksas: USD 15,00
-   4.b Krājumu finanšu izejas plūsma — daudzums: 1, kārtējās vidējās izmaksas: USD 15,00
-   5.a Krājumu fiziskā ieejas plūsma — daudzums: 1, vienības izmaksas: USD 17,00
-   5.b Krājumu finanšu ieejas plūsma — daudzums: 1, vienības izmaksas: USD 17,00

Tiek veikta krājumu slēgšana. Ir jāizmanto tiešā segšana, jo pastāv vairākas ieejas plūsmas vairāku dienu laikā.

-   7.a Tiek izveidota svērtā vidējā krājumu slēgšanas transakcijas finanšu izejas plūsma ar daudzumu 2 un izmaksām USD 32,00, lai apkopotu visu neslēgto krājumu finanšu izejas plūsmu segšanu uz konkrēto datumu.
-   7.b Tiek izveidots novērtētā vidējā rādītāja krājumu slēgšanas pārsūtīšanas finansiālās saņemšanas darījums kā korespondējošā darbība 7a.

Sistēmā tiek ģenerētas un grāmatotas apkopotās krājumu pārsūtīšanas transakcijas. Turklāt sistēmā visas ieejas plūsmas konkrētajā dienā un rīcībā esošie krājumi no iepriekšējām dienām tiek segti ar apkopotās krājumu pārsūtīšanas izejas plūsmas transakciju. Visas izejas plūsmas konkrētajā dienā tiek segtas ar apkopoto krājumu pārsūtīšanas ieejas plūsmas transakciju. Aprēķinātā svērto vidējo izmaksu cena ir USD 16,00. Tiks veikta izejas plūsmas korekcija par sumu USD 1,00, lai to pielāgotu svērtajām vidējām izmaksām. Jaunā tekošā vidējā izmaksu cena ir USD 16,00. 

Tālāk esošajā ilustrācijā ir attēlotas šīs transakcijas, kā arī ietekme, ko rada svērtā vidējā krājumu modeļa un apkopotās segšanas principa izmantošana, ja netiek izmantota opcija **Iekļaut fizisko vērtību**. 

![Novērtētā vidējā datuma kopsavilkuma nosegšana bez Iekļaut fizisko vērtību opcijas](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Attēla apzīmējumi**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs vai zem katras vertikālās bultas ir norādīta krājumu transakcijas vērtība formātā *Daudzums*@*Vienības cena*.
-   Ja krājumu transakcijas vērtība ir ietverta iekavās, krājumu transakcija tiek fiziski iegrāmatota krājumos.
-   Ja krājumu transakcijas vērtība nav ietverta iekavās, krājumu transakcija tiek finansiāli iegrāmatota krājumos.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas tiek veiktas, slēdzot krājumus, ir apzīmētas ar sarkanām pārtrauktu līniju bultām, kas pa diagonāli savieno ieejas plūsmu un izejas plūsmu.
-   Ar sarkanajām nepārtrauktu līniju diagonālajām bultām ir norādītas ieejas plūsmas transakcijas, kas tiek segtas ar sistēmā izveidoto izejas plūsmas transakciju.
-   Ar zaļo nepārtrauktas līnijas diagonālo bultu ir norādīta sistēmā ģenerētā korespondējošā ieejas plūsmas transakcija, ar ko tiek segta sākotnēji grāmatotā izejas plūsmas transakcija.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Svērtā vidējā uz datumu tiešā segšana, ja tiek izmantota opcija Iekļaut fizisko vērtību
Svērtajam vidējam uz datumu pašreizējā versijā tiek izmantots tas pats tiešās segšanas princips, kas tika izmantots iepriekšējās versijās. Sistēmā tiek veikta ieejas plūsmas un izejas plūsmas tiešā segšana. Sistēma izmanto šo tiešās nosegšanas principu īpašās situācijās:

-   Perioda laikā ir iegrāmatota viena ieejas plūsma un viena vai vairākas izejas plūsmas.
-   Šī perioda laikā ir iegrāmatotas tikai izejas plūsmas, un ir pieejami rīcībā esošie krājumi no iepriekšējās slēgšanas.

Ja lapā **Krājumu modeļu grupa** krājumam atzīmējat izvēles rūtiņu **Iekļaut fizisko vērtību**, sistēmā novērtēto izmaksu cenas vai pašreizējās vidējās vērtības aprēķinam tiek izmantotas fiziski atjauninātas ieejas plūsmas. Izejas plūsmas tiek grāmatotas, pamatojoties uz šo novērtēto izmaksu cenu perioda laikā. Krājumu slēgšanas laikā, aprēķinot svērto vidējo, tiek ņemtas vērtā tikai finansiāli atjauninātās ieejas plūsmas.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Svērtā vidējā uz datumu apkopotā segšana, ja tiek izmantota opcija Iekļaut fizisko vērtību
Ja lapā **Krājumu modeļu grupa** krājumam atzīmējat izvēles rūtiņu **Iekļaut fizisko vērtību**, sistēmā novērtēto izmaksu cenas vai pašreizējās vidējās vērtības aprēķinam tiek izmantotas fiziski atjauninātas ieejas plūsmas. Izejas plūsmas tiek grāmatotas, pamatojoties uz šo novērtēto izmaksu cenu perioda laikā. Krājumu slēgšanas laikā, aprēķinot svērto vidējo, tiek ņemtas vērtā tikai finansiāli atjauninātās ieejas plūsmas. Svērtā vidējā segšanas pamatā ir princips, ka ieejas plūsmas slēgšanas periodā tiek apkopotas jaunā krājumu pārsūtīšanas transakcijā, kas tiek saukta par *svērtā vidējā krājumu slēgšanu*. Visas ieejas plūsmas konkrētajā dienā tiek segtas ar jaunās krājumu pārsūtīšanas transakcijas izejas plūsmu. Visas izejas plūsmas konkrētajā dienā tiek segtas ar jaunās krājumu pārsūtīšanas transakcijas ieejas plūsmu. Ja pēc krājumu slēgšanas rīcībā esošo krājumu vērtība ir pozitīva, šie rīcībā esošie krājumi un krājumu vērtība tiek apkopti jaunā krājumu pārsūtīšanas transakcijā (ieejas plūsmā). Ja pēc krājumu slēgšanas rīcībā esošo krājumu vērtība ir negatīva, rīcībā esošie krājumi un krājumu vērtība veido atsevišķo pilnībā nesegto izejas plūsmu summu.

## <a name="weighted-average-date-when-marking-is-used"></a>Svērtais vidējais uz datumu, ja tiek izmantota iezīmēšana
Atzīmēšana ir process, kas sniedz iespēju izejas plūsmas transakciju saistīt ar ieejas plūsmas transakciju. Atzīmēšana var parādīties gan pirms, gan pēc darbības grāmatošanas. Kā arī varat lietot iezīmēšanu, ja vēlaties pārbaudīt precīzas krājuma izmaksas pēc darbības iegrāmatošanas vai pēc krājumu slēgšanas. 

Piemēram, jūsu Klientu apkalpošanas nodaļa saņēma steidzamu pasūtījumu no svarīga klienta. Tā kā tas ir steidzams pasūtījums, lai izpildītu debitora pieprasījumu, par šo krājumu ir jāmaksā vairāk. Jums ir jānodrošina, ka šīs krājuma vienības izmaksas tiek ietvertas uzcenojumā vai pārdoto preču pašizmaksā (PPPI) šajā pārdošanas pasūtījuma rēķinā. Iegrāmatojot pirkšanas pasūtījumu, tiek saņemts krājums ar vērtību USD 120,00. Pārdošanas pasūtījuma dokuments tiek iezīmējot saistīts ar pirkšanas pasūtījumu pirms pavadzīmes vai rēķina grāmatošanas. Pēc tam krājuma PPPI ir USD 120,00, nevis pašreizējā kārtējo vidējo izmaksu cena šim krājumam. Ja pārdošanas pasūtījuma pavadzīme vai rēķins tiek iegrāmatots pirms iezīmēšanas, COGS būs norādītas kā pašreizējo krājuma vidējo izmaksu cena. Pirms krājumu slēgšanas šīs darbības var būt savstarpēji iezīmētas. Ja ieejas plūsmas transakcija tiek iezīmējot saistīta ar izejas plūsmas transakciju, krājumam tiek ignorēta krājumu modeļu grupā definētā vērtēšanas metode. Tā vietā sistēmā šīs transakcijas tiek segtas viena ar otru. 

Varat atzīmēt saņemšanas darbībai paredzēto izdošanas darbību pirms darbība tiek grāmatota. To var paveikt no pārdošanas pasūtījuma rindas, lapā **Pārdošanas pasūtījuma informācija**. Varat skatīt atvērtās ieejas plūsmas transakcijas lapā **Iezīmēšana**. Varat iezīmējot saistīt izejas plūsmas transakciju ar ieejas plūsmas transakciju pēc transakcijas grāmatošanas. Varat saskaņot vai iezīmējot saistīt inventarizēta krājuma izejas plūsmas transakciju ar atvērtu ieejas plūsmas transakciju, izmantojot grāmatoto krājumu korekciju žurnālu. Šīs transakcijas ir attēlotas tālāk esošajā ilustrācijā.

-   1.a Krājumu fiziska saņemšana ar daudzumu 1 pie izmaksu cenas USD 10,00.
-   1.b Krājumu finansiāla saņemšana ar daudzumu 1 pie izmaksu cenas USD 10,00.
-   2.a Krājumu fiziska saņemšana ar daudzumu 1 pie izmaksu cenas USD 20,00.
-   2.b Krājumu finansiāla saņemšana ar daudzumu 1 pie izmaksu cenas USD 20,00.
-   3.a Krājumu fiziska saņemšana ar daudzumu 1 pie izmaksu cenas USD 25,00.
-   4.a Krājumu fiziska saņemšana ar daudzumu 1 pie izmaksu cenas USD 30,00.
-   4.b Krājumu finansiāla saņemšana ar daudzumu 1 pie izmaksu cenas USD 30,00.
-   5.a Krājumu fiziskā izejas plūsma — daudzums: 1, izmaksu cena: USD 21,25 (finansiāli un fiziski atjaunināto transakciju kārtējās vidējās izmaksas).
-   5.b Krājumu finansiāla izdošana ar daudzumu 1 tiek nozīmēta krājumu ieejas plūsmai 2b pirms darbība tiek iegrāmatota. Šī darbība tiek iegrāmatota ar izmaksu cenu USD 20,00.
-   6.a Krājumu fiziska izsniegšana ar daudzumu 1 pie izmaksu cenas USD 21,25.
-   7. Tiek veikta krājumu slēgšana. Tā kā finansiāli atjauninātā transakcija ir iezīmējot saistīta ar esošu ieejas plūsmu, šīs transakcijas tiek segtas viena ar otru un netiek veiktas nekādas korekcijas.

Jauna pašreizēja vidējā izmaksu cena attēlo finansiāli vai fiziski atjaunināto darbību vidējo par summu USD 27,50. Tālāk esošajā ilustrācijā ir attēlotas šīs transakcijas, kā arī ietekme, ko rada svērtā vidējā uz datumu krājumu modeļa un iezīmēšanas izmantošana.

![Novērtētais vidējais datums ar iezīmēšanu](./media/weightedaveragedatewithmarking.gif) 

**Attēla apzīmējumi:**

-   Krājuma darbības ir atzīmētas ar vertikālām bultām.
-   Krājuma saņemšana ir atzīmēta ar vertikālām bultām virs laika skalas.
-   Krājuma izdošana ir atzīmēta ar vertikālām bultām zem laika skalas.
-   Virs vai zem katras vertikālās bultas ir norādīta krājumu transakcijas vērtība formātā *Daudzums*@*Vienības cena*.
-   Ja krājumu transakcijas vērtība ir ietverta iekavās, krājumu transakcija tiek fiziski iegrāmatota krājumos.
-   Ja krājumu transakcijas vērtība nav ietverta iekavās, krājumu transakcija tiek finansiāli iegrāmatota krājumos.
-   Katra jauna krājuma saņemšanas vai izdošanas darbība tiek atzīmēta ar jaunu etiķeti.
-   Katra vertikāla bulta ir atzīmēta ar secības identifikatoru, piemēram, *1a*. Identifikators norāda uz krājumu darbību iegrāmatošanas kārtību laika intervālā.
-   Krājuma slēgšanas, kas atzīmētas ar sarkanu vertikālu punktlīniju un etiķeti *Krājuma slēgšana*.
-   Segšanas, kas tiek veiktas, slēdzot krājumus, ir apzīmētas ar sarkanām pārtrauktu līniju bultām, kas pa diagonāli savieno ieejas plūsmu un izejas plūsmu.





