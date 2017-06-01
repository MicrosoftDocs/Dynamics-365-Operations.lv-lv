---
title: "Darba sadalījuma struktūras"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1a700f61bcc6e6d9c699987999be25649862b0d8
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="work-breakdown-structures"></a>Darba sadalījuma struktūras

[!include[banner](../includes/banner.md)]




Darba sadalījuma struktūras Darba sadalījuma struktūra (WBS) ir projekta ietvaros veicamā darba apraksts. Tā ir uzdevumu hierarhija, kas norāda projekta grupas izpratni par darba saturu un katra komponenta vai uzdevuma lielumu, izmaksām un ilgumu. WBS ir trīs galvenie mērķi:

-   Aprakstīt uzdevumos ietilpstošo darbu sadalījumu vai sastāvu.
-   Plānot projekta darbu.
-   Novērtēt katra uzdevuma izmaksas.

Detalizācijas pakāpe WBS ir atkarīga no precizitātes, kas nepieciešama novērtējumiem, un izsekošanas līmeņa, kas nepieciešams attiecīgajiem novērtējumiem. Projektiem, kuriem ir ļoti zema pielaide attiecībā uz novirzēm grafikā vai izmaksās, parasti nepieciešama detalizētāka WBS un rūpīga darba norises un izmaksu izsekošana, salīdzinot tās ar WBS. Šāda veida projekti ir izplatīti būvniecības un mašīnbūves nozarē. 

Turpretim projekti tādās jomās kā plašsaziņas līdzekļi un reklāma, programmatūra un IT infrastruktūra mēdz būt unikāli un produktivitāte ir atkarīga no uzdevuma veicēja pieredzes un kompetences. Tādēļ šajās nozarēs WBS tiek izmantota, lai noteiktu aptuvenu projekta lielumu, nevis lai detalizēti izsekotu attiecīgā projekta norisi. 

WBS izveide ir intensīvs process, kurš parasti tiek veikts ilgā laikposmā un kuram nepieciešama sadarbība un informācija, ko nodrošina dažādas personas. Šajā tēmā ir aprakstīts, kā varat izmantot WBS uzlabojumus programmatūrā Microsoft Dynamics 365 for Operations, lai apmierinātu savas novērtēšanas un izsekošanas vajadzības.

## <a name="prerequisites-for-creating-a-wbs"></a>WBS izveides priekšnoteikumi
Lai izveidotu WBS, jums jāvar izveidot darba grafiku un novērtēt darba izmaksas.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Darba grafika izveides priekšnoteikumi

Lai pilnībā izmantotu plānošanas iespējas, ko sniedz WBS līdzekļi, veiciet tālāk norādītos iestatījumus.

1.  Iestatiet noklusējuma kalendāru un projekta kalendāru:
    1.  Noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Plānošana**. Laukā **Darba laika noklusējuma kalendārs** norādiet noklusējuma kalendāru. Tas būs darba laika noklusējuma kalendārs visiem jaunizveidotajiem projektiem.
    2.  Jūs varat mainīt noklusējuma kalendāru noteiktam projektam. Noklikšķiniet uz projekta detalizētas informācijas lapas un pēc tam kopsavilkuma cilnē **Projekta grupa un plānošana** atjauniniet lauku **Plānošanas kalendārs**, atlasot citu kalendāru.

2.  Iestatiet standarta darba dienas un darba stundas. Kalendārs, kas attiecīgajam projektam iestatīts kā darba laika kalendārs, tiks izmantots WBS, lai noteiktu šādu informāciju:

-   Darba dienas un brīvdienas
-   Darba stundu skaits dienā

Lai iestatītu kalendāra darba dienas un darba stundas vai izveidotu jaunu kalendāru, noklikšķiniet uz **Organizācijas administrēšana** &gt; **Vispārīgi** &gt; **Kalendāri**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Darba izmaksu novērtēšanas priekšnoteikumi

Lai pilnībā izmantotu izmaksu novērtēšanas iespējas, ko sniedz WBS, ir jāiestata izmaksas un pārdošanas cenas darbiniekiem, darbaspēka, izdevumu un maksu kategorijām un krājumiem.

-   Lai iestatītu darbaspēka, izdevumu un maksu kategoriju izmaksas un pārdošanas cenu, noklikšķiniet uz **Projektu vadība un uzskaite** &gt; **Iestatījumi** &gt; **Cenas**.
-   Lai iestatītu krājumu izmaksas un pārdošanas cenu, izmantojiet lapu **Tirdzniecības līgumi**katram krājumam saraksta lapā **Izlaistās preces** sadaļā Preču informācijas pārvaldība.

## <a name="creating-a-wbs"></a>WBS izveide
WBS izveidē ietilpst trīs darbības:

1.  **Darba dekompozīcija** — sadaliet darbu pārvaldāmās daļās vai uzdevumos.
2.  **Darba grafiks** — novērtējiet laiku, kas nepieciešams uzdevuma pabeigšanai, iestatiet uzdevumu savstarpējo saistību un atlasiet uzdevumu sākuma un beigu datumus.
3.  **Izmaksu novērtējums** — novērtējiet katra uzdevuma izmaksas.

Tālāk esošajās sadaļās ir aprakstīts, kā WBS iespējas var palīdzēt veikt katru no šīm darbībām.

### <a name="work-decomposition"></a>Darba dekompozīcija

Darba sadalījuma vai dekompozīcijas izveide parasti ir pirmais solis WBS izveides procesā. WBS funkcionalitāte atbalsta tālāk norādītās darbu sadalījuma vai dekompozīcijas pamatstruktūras. 

**Projekta saknes uzdevums** Projekta saknes uzdevums ir augstākā līmeņa kopsavilkuma uzdevums projektam. Visi pārējie projekta uzdevumi tiek izveidoti pakārtoti. Saknes uzdevuma nosaukums vienmēr tiek iestatīts kā projekta nosaukums. Saknes zara darbs, datumi un ilgums sniedz kopsavilkumu par vērtībām uzdevumiem, kuri pakārtoti saknes uzdevumam. Saknes mezgla rekvizītus nevar modificēt vai dzēst.

**Kopsavilkuma vai konteineruzdevumi** Kopsavilkuma uzdevums ir uzdevums, kuram ir pakārtoti apakšuzdevumi vai komponentu uzdevumi. Kopsavilkuma uzdevumam nav atsevišķa darba vai izmaksu. Tā vietā kopsavilkuma uzdevuma darbs un izmaksas ir vienāds ar tā komponentu uzdevumu darba un izmaksu summu. Komponentu uzdevumu agrākais sākuma datums tiek izmantots kā kopsavilkuma uzdevuma sākuma datums, un komponentu uzdevumu vēlākais beigu datums tiek izmantots kā beigu datums. Ir iespējams modificēt kopsavilkuma uzdevuma nosaukumu, bet nevar modificēt plānošanas rekvizītus darbam, datumiem un ilgumam. Dzēšot kopsavilkuma uzdevumu, tiks izdzēsti arī visi komponentu uzdevumi. 

**Lapas mezgla uzdevumi** Lapas mezglu uzdevums ir fragmentārākā darba pakotne projektā. Lapas mezglam ir novērtētais darbs, plānotais resursu skaits, plānotais sākuma datums un beigu datums un ilgums. 

Jūs varat veikt šādas hierarhijas darbības, lai iespējotu darbu hierarhijas izveidi vai projekta dekompozīciju. 

**Jauns uzdevums** Visi jaunie uzdevumu, kurus izveidosiet, automātiski tiek pievienoti saknes mezglā, un uzdevumam tiek automātiski piešķirts WBS numurs. WBS numurs norāda uzdevuma līmeni hierarhijā. Uzdevumiem projekta saknes uzdevuma pirmajā līmenī tiek izmantota numerācija 1, 2, 3 un tā tālāk. Uzdevumiem pirmajā līmenī tiek izmantota numerācija 1.1, 1.2, 1.3 un tā tālāk. Katram līmenim, kas tiek pakārtots iepriekšējam līmenim, aiz punkta tiek pievienota jauna numuru sērija. 

Pašlaik WBS numerāciju nevar pielāgot. 

**Izveidot uzdevuma atkāpi** Izveidojot uzdevuma atkāpi, tas kļūst par iepriekšējā uzdevuma apakšuzdevumu. Jaunā apakšuzdevuma WBS numurs tiek automātiski pārrēķināts, pamatojoties uz tā jaunā pamatuzdevuma WBS numuru. Attiecīgais pamatuzdevums tagad ir kopsavilkuma vai konteineruzdevums un līdz ar to kļūst par komponentu uzdevumu apkopojumu. 

> [!NOTE] 
> Ja izveidojat tāda uzdevuma atkāpi, kura augšējā līmeņa uzdevums pirms atkāpes izveides operācijas bija lapas mezgls, tiek zaudēta informācija par jaunizveidotā kopsavilkuma uzdevuma datumiem, darbu un resursu skaitu. Tagad tam tiek izmantotas jauno komponentu vērtību kopsavilkuma vērtības. 

**Izveidot uzdevuma pārkaru atkāpi** Izveidojot uzdevuma pārkaru atkāpi, tas vairs nav pamatuzdevuma komponentu uzdevums. Šī uzdevuma WBS numurs tiek automātiski pārrēķināts, lai parādītu uzdevuma jauno līmeni hierarhijā. Uzdevuma līdzšinējā pamatuzdevuma darbs, izmaksas un datumi tiek pārrēķināti, lai izslēgtu attiecīgo uzdevumu. 

**Pārvietot uz augšu un Pārvietot uz leju** Noklikšķinot uz **Pārvietot uz augšu** un **Pārvietot uz leju**, tiek mainīta uzdevuma pozīcija tā vecākhierarhijā. Uzdevuma pozīcija neietekmē uzdevuma darbu, izmaksas, datumus vai ilgumu. Tomēr uzdevuma WBS numurs tiek automātiski pārrēķināts, lai parādītu uzdevuma jauno pozīciju.

### <a name="schedule-estimation"></a>Grafika novērtējums

Grafika novērtējums parasti ir otrais solis, veidojot WBS. Saskaņā ar paraugpraksi grafika novērtējums ir jāveic pēc uzdevumu izveides. Lapai **Darba sadalījuma struktūra** programmatūrā Microsoft Dynamics 365 for Operations ir divas sadaļas. Augšējā rūts ir paredzēta grafika novērtējumam, un apakšējā rūtī ir cilne **Novērtētās izmaksas un ieņēmumi**, kuru varat izmantot izmaksu novērtējumam. 
**Uzdevumu atkarības** WBS struktūrā iespējams izveidot pirmstecīgās attiecības starp uzdevumiem. Piešķirot uzdevumam pirmstecīgo uzdevumu, attiecīgo uzdevumu var sākt tikai pēc tam, kad ir pabeigti tā pirmstecīgie uzdevumi. Uzdevuma plānotais sākuma datums automātiski tiek iestatīts uz pirmstecīgo uzdevumu pēdējo datumu. 

**Uzdevumu plānošana programmatūrā Microsoft Dynamics 365 for Operations** Lapas mezgla uzdevumu plānošanu nosaka tālāk norādītie faktori.

-   Pirmstecīgas aktivitātes
-   Darbs
-   Resursu skaits
-   Sākuma un beigu datumi

Tāda lapas mezgla uzdevumu sākuma datums, kuram nav pirmstecīgu uzdevumu, tiek iestatīts automātiski uz projekta plānošanas sākuma datumu. Lapas mezgla uzdevuma ilgums vienmēr tiek aprēķināts kā darba dienu skaits starp sākuma un beigu datumu. 

****Plānošanas kārtulas**** Ja ir ieslēgta automātiskās plānošanas palīdzība, uz lapas mezgla uzdevumu plānošanu attiecas tālāk norādītie noteikumi.

-   Uzdevuma sākuma un beigu datumam jābūt darba dienai saskaņā ar projekta plānošanas kalendāru.
-   Tāda uzdevuma sākuma datums, kuram ir pirmstecīgie uzdevumi, automātiski tiek iestatīts uz pirmstecīgo uzdevumu pēdējo beigu datumu.
-   Uzdevuma darbs tiek automātiski aprēķināts šādi:

cilvēku skaits × ilgums × stundu skaits projekta kalendāra standarta darba dienā. 

Iespējams, reizēm vēlaties atkāpties no šīm kārtulām. Varat izslēgt automātisko plānošanu, lai programmatūrā Microsoft Dynamics 365 for Operations netiktu automātiski iestatīti vai laboti lapas mezgla uzdevumu rekvizīti. Ievadot uzdevuma informāciju, kas izraisa plānošanas kārtulu pārkāpumu, attiecīgajam uzdevumam tiek parādīta plānošanas kļūdas ikona. Ja nevēlaties, lai plānošanas kļūdas tiktu parādītas, noklikšķiniet uz **Plānošanas kļūdas tiek rādītas**, lai izslēgtu šo līdzekli. 

> [!NOTE] 
> Kopsavilkuma uzdevuma vai konteineruzdevuma vērtības arī turpmāk tiek aprēķinātas kā komponentu uzdevumu vērtību summa neatkarīgi no tā, vai automātiskās plānošanas palīdzība ir ieslēgta vai izslēgta. 

**Plānošanas kļūdu labošana** Kad automātiskās plānošanas palīdzība ir ieslēgta, plānošanas kļūdu rašanās ir maz ticama. Tomēr, ja automātiskās plānošanas palīdzība tiek izslēgta un pēc tam ieslēgta, WBS struktūrā var parādīties plānošanas kļūdas ikonas. 

**Plānošanas kļūdu labošana pēc uzdevuma** Veicot dubultklikšķi uz plānošanas kļūdas ikonas noteiktam uzdevumam, dialoglodziņā tiek parādītas visas plānošanas kļūdas attiecīgajam uzdevumam. Jūs varat izlemt, kuras plānošanas kļūdas uzdevumam labot. 

**Visu plānošanas kļūdu labošana** Ja vēlaties, lai programmatūrā Microsoft Dynamics 365 for Operations tiktu labotas visas plānošanas kļūdas WBS struktūrā, darbības rūtī noklikšķiniet uz **Labot visas plānošanas neatbilstības**. 

> [!NOTE] 
> Šis līdzeklis var izraisīt nozīmīgas WBS modifikācijas. Kļūdas tiek labotas šādā secībā:

1.  Novērtētais darbs visiem uzdevumiem tiek modificēts tā, lai tas būtu vienāds ar noslodzi, kas definēta projekta kalendārā.
2.  Katra uzdevuma sākuma datums tiek modificēts tā, lai uzdevums sāktos pēc tam, kad ir pabeigti visi tā pirmstecīgie uzdevumi.
3.  Katra uzdevuma sākuma datums tiek modificēts, lai likvidētu pārtraukumus starp priekštecīgo uzdevumu sākuma datumiem.

### <a name="cost-estimation"></a>Izmaksu novērtējums

Kā tika minēts iepriekš šajā dokumentā, katram lapas mezgla uzdevumam izmaksu novērtējumu ievada, izmantojot cilni **Novērtētās izmaksas un ieņēmumi** apakšējā rūtī lapā **Darba sadalījuma struktūra**. 

> [!NOTE] 
> Nevarat modificēt kopsavilkuma uzdevuma vai konteineruzdevuma izmaksu novērtējumu. Izmaksu novērtējums kopsavilkuma uzdevumam ir vienāds ar tā lapas mezgla uzdevumu izmaksu novērtējumu summu. Novērtētās kopējās izmaksas katram uzdevumam tiek aprēķinātas kā novērtēto izmaksu summas šādiem darbību veidiem:

-   Darbaspēks
-   Krājums vai materiāls
-   Izdevumi

Darbības veids **Papildmaksa** tiek izmantots, lai novērtētu ar papildmaksu saistītos ieņēmumus. Šim darbības veidam nav izmaksu sastāvdaļas, tādēļ tas netiek ņemts vērā, novērtējot izmaksas. 

Darījuma veids **Starpkonts** tiek izmantots, lai reģistrētu līgumā noteikto pārdošanas vērtību fiksētas vērtības tipa projektā. Šis darbības veids arī netiek ņemts vērā, aprēķinot izmaksas. 

Aprēķinot darbaspēka, materiālu un izdevumu izmaksas katram uzdevumam, attiecīgajām novērtētajām izmaksām ir jāpiešķir projekta kategorija. 

**Darbaspēka izmaksu novērtēšana** Piešķiriet darbu stundās un noklusējuma kategoriju katram lapas mezgla uzdevumam. Tādējādi, iestatot grafiku uzdevumam, darbaspēka izmaksu novērtējums attiecīgajam uzdevumam tiek automātiski iekļauts darbaspēka noklusējuma kategorijā. Šis izmaksu novērtējums tiek parādīts cilnē **Novērtētās izmaksas un ieņēmumi** attiecīgā uzdevuma režģī **Detalizēta rindas informācija**. Ja jums ir nepieciešami papildu darbaspēka izmaksu aprēķini, tos var pievienot šajā cilnē. Palielinot vai samazinot stundu skaitu darbaspēka izmaksu novērtējumā, uzdevuma grafiks tiek automātiski pārrēķināts. 

**Izdevumu un materiālu izmaksu novērtēšana** Cilne **Novērtētās izmaksas un ieņēmumi** arī ļauj uzdevumam novērtēt izdevumu un materiālu izmaksas, ja jums ir nepieciešami novērtējumi. 

Katras darbaspēka vai izdevumu novērtējuma rindas izmaksas un pārdošanas cena ir noteiktas, pamatojoties uz iestatījumiem, kas ir definēti katrai kategorijai cenu noteikšanas tabulās sadaļā **Projekta vadība un uzskaite** &gt; **Iestatījumi** &gt; **Cenu noteikšana**. Krājumiem izmaksas un pārdošanas cena tiek pievienota pēc noklusējuma no krājumu un tirdzniecības līgumiem saraksta lapā **Izlaistās preces** sadaļā Preču informācijas pārvaldība.

## <a name="tracking-progress-on-the-wbs"></a>Sekošana norisei WBS struktūrā
Dažās nozarēs sekošana projekta norisei, salīdzinot to ar WBS struktūru, tiek veikta ļoti fragmentārā līmenī, savukārt citās jomās sekošana projekta norisei tiek īstenota augstākā WBS līmenī. Šajā sadaļā ir aprakstīts, kā jūs varat izmantot WBS izsekošanu jūsu projekta prasībām. 

Programmatūrā Microsoft Dynamics 365 for Operations ir pieejami trīs projekta WBS struktūras skati: plānošanas skats, darba izsekošanas skats un izmaksu izsekošanas skats.

### <a name="planning-view"></a>Plānošanas skats

Plānošanas skatā tiek pardādīta informācija par grafiku un izmaksu plānoto vai bāzlīnijas novērtējumu. Kaut arī nav līdzekļu projekta WBS struktūras versijas un bāzlīnijas izsekošanai, vērtības šajā skatā ir paredzētas bāzlīnijas versijas norādīšanai. Šīs tēmas sadaļās Grafika novērtējums un Izmaksu novērtējums ir aprakstīts šis skats un kā tas tiek izmantots, lai izveidotu WBS.

### <a name="effort-tracking-view"></a>Darba izsekošanas skats

Darba izsekošanas skatā tiek parādīta norises izsekošana uzdevumiem WBS struktūrā. Tājā tiek salīdzinātas uzkrātās faktiskās darba stundas uzdevumam ar plānotajām darba stundām. Darba izsekošanas skatā vērtības ir sniegtas, izmantojot šādas formulas:

-   Norises procentuālā vērtība = līdz šim faktiski paveiktais darbs ÷ plānotais uzdevuma darbs
-   Atlikušais darbs (saukts arī par novērtējumu beigu stadijā \[ETC\]) = plānotais darbs – līdz šim faktiski paveiktais darbs
-   Galīgo izmaksu novērtējums (EAC) = atlikušais darbs + līdz šim faktiski paveiktais darbs
-   Plānotā darba novirze = plānotais darbs – EAC

Darba izsekošanas skatā ir parādīta plānotā darba novirze attiecīgajam uzdevumam, balstoties uz to, vai EAC ir lielāka vai mazāka par plānoto darbu:

-   Ja EAC ir lielāks par plānoto darbu, paredzams, ka uzdevums prasīs vairāk laika, nekā sākotnēji plānots, un atpaliek no grafika.
-   Ja EAC ir mazāks par plānoto darbu, paredzams, ka uzdevums prasīs mazāk laika, nekā sākotnēji plānots, un apsteidz grafiku.

**Projekta vadītāja atkārtota darba prognoze** Laiku pa laikam projekta vadītājam vai citai personai, kas seko projekta norisei, būs jāpārskata uzdevuma sākotnējie novērtējumi. Uzdevuma izpilde var notikt ātrāk vai lēnāk, nekā sākotnēji paredzēts, dažādu iemeslu dēļ. Piemēram, ir sašaurināta uzdevuma darbības joma vai darbinieku pieredzes līmenis ir zemāks, nekā sākotnēji plānots. Prognozes ir projekta vadītāja izpratne par novērtējumiem, pamatojoties uz pašreizējo projekta statusu. Parasti bāzlīnijas skaitļus nedrīkst mainīt, jo projekta bāzlīnija ir plaši publicēts dokuments projekta grafika un izmaksu novērtējumam, par kuru vienojušās visas ieinteresētās personas attiecīgā projekta ietvaros. 

Projektu vadītāji var modificēt darbu divos veidos.

-   Modificēt atlikušo darbu, kuram ir iestatīts automātiski atjaunināt uzdevuma faktiski atlikušo darbu.
-   Modificēt norises procentuālo vērtību, kurai ir iestatīts automātiski atjaunināt uzdevuma faktisko norisi.

Abu šo pieeju rezultātā tiek veikts uzdevuma ETC, EAC un norises procentuālo vērtību, kā arī uzdevuma plānotās darba novirzes pārrēķins. Tiek veikts arī kopsavilkuma uzdevumu EAC, ETC un norises procentuālo vērtību pārrēķins, kā arī tiek atjaunināta to plānotā darba novirze. 

**Modificēts darbs kopsavilkuma uzdevumos** Jūs varat modificēt darbu kopsavilkuma vai konteineruzdevumos. Neatkarīgi no tā, vai modificējat šīs vērtības, izmantojot kopsavilkuma uzdevumu atlikušo darbu vai norises procentuālo vērtību, aprēķini tiek veikti automātiski šādā secībā:

1.  Tiek aprēķināti uzdevuma EAC, ETC un norises procentuālā vērtība.
2.  Jaunais EAC tiek sadalīts apakšuzdevumiem tādās pašās proporcijās kā sākotnējā EAC summa.
3.  Tiek aprēķināts jaunais EAC katram lapas mezgla uzdevumam.
4.  Visiem ietekmētajiem apakšuzdevumiem tiek pārrēķināts atlikušais darbs un norises procentuālā vērtība, pamatojoties uz jauno EAC vērtību. Tiek pārrēķināta arī uzdevuma darba novirze.
5.  Kopsavilkuma uzdevumu EAC arī tiek pārrēķināts no lapu mezgliem.

Noklikšķiniet uz **Izvērst līdz līmenim** darba izsekošanas skatā, lai iestatītu līmeni, kurā veikt WBS izsekošanu un uzturēšanu. WBS tiek automātiski izvērsta līdz attiecīgajam līmenim darba izsekošanas skatā ikreiz, kad to atverat.

### <a name="cost-tracking-view"></a>Izmaksu izsekošanas skats

Izmaksu izsekošanas skats parāda izmaksu patēriņu izsekošanu uzdevumam. Šajā skatā faktiskās izmaksas, kas ir izlietotas uzdevumam līdz attiecīgajam datuma, tiek salīdzinātas ar plānotajām uzdevuma izmaksām. Izmaksu izsekošanas skatā vērtības ir sniegtas, izmantojot šādas formulas:

-   Procenti no patērētajām izmaksām = līdz šim faktiski izlietotās izmaksas ÷ plānotās uzdevuma izmaksas
-   Pabeigšanas izmaksas (CTC) = plānotās izmaksas – līdz šim faktiski izlietotās izmaksas
-   Galīgo izmaksu novērtējums (EAC) = CTC + līdz šim faktiski izlietotās izmaksas
-   Plānotā izmaksu novirze = plānotās izmaksas – EAC

Izmaksu izsekošanas skatā ir parādīta plānotā izmaksu novirze attiecīgajam uzdevumam, balstoties uz to, vai EAC ir lielāks vai mazāks par plānotajām izmaksām:

-   Ja EAC ir lielāks par plānotajām izmaksām, paredzams, ka uzdevumam būs nepieciešami lielāki naudas līdzekļi, nekā sākotnēji plānots, un budžets tiks pārsniegts.
-   Ja EAC ir mazāks par plānotajām izmaksām, paredzams, ka uzdevumam būs nepieciešami mazāki naudas līdzekļi, nekā sākotnēji plānots, un budžets netiks pārsniegts.

**Projekta vadītāja atkārtota izmaksu prognoze** Projektu vadītājiem ir jāizmanto CTC, lai pārskatītu sākotnējo uzdevuma izmaksu novērtējumu. Projekta vadītājs var mainīt CTC vērtību uz vērtību, kas ir nepieciešama, lai pabeigtu uzdevumu. Ja modificējat CTC vērtību, tiek pārrēķināti uzdevuma CTC, EAC un procenti no patērētajām izmaksām, kā arī uzdevuma plānotā izmaksu novirze. Tiek pārrēķināti arī kopsavilkuma uzdevumu EAC, ETC un procenti no patērētajām izmaksām, kā arī tiek atjaunināta to plānotā izmaksu novirze. 

> [!NOTE] 
> Kad darbu izsekošanas skatā pārskatāt WBS uzdevuma darbu, izmaksu izsekošanas skatā tiek pārrēķināts uzdevuma CTC, EAC, procenti no patērētajām izmaksām un plānotā izmaksu novirze. Tomēr izmaksu pārskatīšana neietekmē vērtības darba izsekošanas skatā, jo netiek pārskatītas izmaksas pēc darbības veida (darbaspēks, materiāls vai izdevumi) vai projekta kategorijas. 

**Prognozes pārskatīšana izmaksām kopsavilkuma uzdevumos** Jūs varat pārskatīt izmaksas kopsavilkuma uzdevumos, un aprēķini tiek veikti automātiski šādā secībā:

1.  Tiek pārrēķināti EAC, CTC un procenti no uzdevumā patērētajām izmaksām.
2.  Jaunais EAC tiek sadalīts apakšuzdevumiem tādās pašās proporcijās kā sākotnējais EAC attiecīgajos uzdevumos.
3.  Tiek aprēķināts jauns EAC katram uzdevumam.
4.  Ietekmētajiem apakšuzdevumiem tiek pārrēķināti CTS un procenti no patērētajām izmaksām, pamatojoties uz EAC vērtību. Tiek pārrēķināta arī uzdevuma izmaksu novirze.
5.  Pamatojoties uz šīm izmaiņām, tiek pārrēķināts EAC visiem kopsavilkuma uzdevumiem.

Noklikšķiniet uz **Izvērst līdz līmenim** izmaksu izsekošanas skatā, lai iestatītu līmeni, kurā veikt WBS izsekošanu un uzturēšanu. WBS tiek izvērsta līdz attiecīgajam līmenim izmaksu izsekošanas skatā ikreiz, kad to atverat.

### <a name="earned-value-management"></a>Iegūtās vērtības pārvaldība

Varat izmantot iegūtās vērtības metodi (EVM), lai izsekotu projekta norisi. Iegūtās vērtības rādītājus var skatīt projekta pārvaldnieka lomu centrā. Iegūtās vērtība diagrammas komponents norāda plānotās vērtības un faktisko izmaksu laika periodos sadalītās vērtības. Iegūtā vērtība pašreizējā datumā tiek parādīta kā punkts. Laika periodos sadalītie iegūtās vērtības dati pašlaik nav pieejami. 

Laika posms iegūtās vērtības diagrammā tiek parādīts pa nedēļām vai mēnešiem. Šajā sadaļā ir aprakstīti EVM trīs pamatelementi: plānotā vērtība, iegūtā vērtība un faktiskās izmaksas. 

**Plānotā vērtība** Saskaņā ar EVM teorētisko pamatojumu plānotās vērtības grafiks norāda ātrumu, ar kuru projekta grupa plānoja iegūt vērtību attiecīgajā projektā. 

Programmatūrā Microsoft Dynamics 365 for Operations plānotās vērtības grafika veidošanas laikā tiek izmantots pelnīšanas noteikums 0:100. Saskaņā ar šo noteikumu uzdevuma vērtība tiek grāmatota uzdevumā tā beigu datumā. Vērtība netiek grāmatota, līdz projekta pabeigtība sasniedz 100 procentus. 

Sadaļā Projektu vadība un uzskaite, ievadiet lapu mezglu beigu datumu un plānotās izmaksas. Kad plānotās vērtības grafiks ir parādīts pa nedēļām, plānotā vērtība tiek summēta pa nedēļām visiem lapas mezgla uzdevumiem visā projekta periodā. 

**Iegūtā vērtība** Saskaņā ar EVM teorētisko pamatojumu iegūtās vērtības grafiks norāda ātrumu, ar kuru projekta grupa faktiski iegūst vērtību attiecīgajā projektā. 

Programmatūrā Microsoft Dynamics 365 for Operations iegūtās vērtības grafika veidošanas laikā tiek izmantots pelnīšanas noteikums 0:100. Saskaņā ar šo noteikumu uzdevuma vērtība tiek grāmatota uzdevumā tā beigu datumā. Vērtība netiek grāmatota, līdz projekta pabeigtība sasniedz 100 procentus. 

Aprēķinot iegūto vērtību, tiek ņemta vērā katra uzdevuma norises procentuālā vērtība. Saskaņā ar 0:100 pelnīšanas kārtulu tikai uzdevumi, kas ir pabeigti attiecīgajā periodā, tiek ņemti vērā iegūtās vērtības aprēķinā attiecīgā perioda beigās. Iegūtā vērtība projektam tiek aprēķināta visiem uzdevumiem, kuri ir pabeigti grafika izveides brīdī. 

> [!NOTE] 
> Pašlaik WBS izsekošanas sistēmā nav pieejamas datu struktūras katra uzdevuma norises vēsturiskās procentuālās vērtības saglabāšanai. Tādēļ iegūto vērtību var iekļaut pārskatā tikai brīdī, kad kubs ir apstrādāts. Veiciet kuba apstrādi regulāri, lai atjauninātu iegūtās vērtības datus, kas tiek rādīti lomu centrā. 

**Faktiskās izmaksas** Saskaņā ar EVM teorētisko pamatojumu faktisko izmaksu grafiks norāda ātrumu, ar kuru naudas līdzekļi attiecīgajā projektā tiek tērēti. 

Projektā grāmatotās darbības tiek izmantotas, lai atzīmētu grafikā faktisko izmaksu līniju. Izmaksas tiek summētas pēc datuma. Šie dati pēc tam tiek izmantoti, lai attēlotu faktiskās izmaksas pa nedēļām vai mēnešiem iegūtās vērtības diagrammā.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Plānotās vērtības, iegūtās vērtības un faktisko izmaksu koncepciju izmantošana

**Grafika novirze** Plānošanas laikā jūs veidojat prognozi darbam laika skalā. Tāpēc plānotā vērtība ir ātrums, ar kuru projekta plānotāji bija paredzējuši pabeigt darbu projekta ietvaros. Pēc tam, kad projekts ir norises procesā, darbs tiek pabeigts un projekta ietvaros tiek iegūta vērtība. Salīdzinot plānoto vērtību ar iegūto vērtību, var skatīt, kā norisinās darbs pie projekta. Šā salīdzinājuma rezultātu sauc par grafika novirzi. 

Ja plānotā vērtība periodā pārsniedz iegūto vērtību, darba apjoms, kas paveikts projekta ietvaros, ir mazāks par to, kas tika plānots. Tādējādi projekts atpaliek no grafika. Tā kā plānotā vērtība un iegūtā vērtība ir norādītas naudas izteiksmē, projekta aizkavēšanās laikam arī ir sniegta monetāra vērtība. 

Ja plānotā vērtība periodā ir mazāka par iegūto vērtību, darba apjoms, kas paveikts projekta ietvaros, pārsniedz plānoto apjomu. Tādējādi projekts apsteidz grafiku. Šis izpildes laiks ir norādīts arī naudas izteiksmē.

**Izmaksu novirze** Tā kā iegūtajai vērtībai izmaksu cena tiek izmantota kā reizinātājs, iegūtā vērtība norāda projekta ietvaros veiktā darba izmaksas. Projekta norises gaitā darbību žurnāls sniedz uzskaites datus par projektam faktiski izlietotajiem naudas līdzekļiem. Salīdzinot iegūto vērtību ar faktiskajām izmaksām, var salīdzināt izlietoto naudas summu ar iegūto vērtību. Šā salīdzinājuma rezultātu sauc par izmaksu novirzi. 

Ja faktiskās periodā izmantotās izmaksas pārsniedz iegūto vērtību, tika iztērēti lielāki naudas līdzekļi nekā nopelnīti. Tādējādi projekta budžets ir pārsniegts. 

Ja faktiskās periodā izmantotās izmaksas ir mazākas par iegūto vērtību, tika nopelnīti lielāki naudas līdzekļi nekā iztērēti. Tādējādi vērtība ir mazāka par projekta budžetā noteikto.

## <a name="wbs-templates"></a>WBS veidnes
Varat izmantot WBS veidņu funkcionalitāti, lai izveidotu projektu standarta veidnes. Ja projektos, kurus piedāvā jūsu uzņēmums, ir daudz darbu, kas atkārtojas, ieteicams izveidot WBS veidni. 

WBS veidni var izveidot no esoša projekta WBS, lai zināšanas un paraugprakses, kuras ir apkopotas attiecīgā projekta plānošanas laikā, varētu atkārtoti izmantot līdzīgiem projektiem nākotnē. Tomēr dažreiz nav lietderīgi saglabāt visu WBS kā veidni. Tādēļ veidnes var izveidot arī no projekta WBS daļām.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projekta WBS kā veidnes saglabāšana

Kad ir izveidota veidne, to var importēt jaunā projekta WBS struktūrā zem saknes mezgla vai zem jebkura uzdevuma, kas ietilpst projekta WBS struktūrā.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>WBS veidnes importēšana projekta WBS struktūrā

Importējot uzdevumus, uzdevumi veidnē tiek organizēti, pamatojoties uz tā uzdevuma sākuma datumu, zem kura tie tiek importēti. Importēšanas laikā pirmstecīgās attiecības veidnes uzdevumos tiek izmantotas, lai aprēķinātu importēto uzdevumu sākuma datumus. Mērķa projekta standarta darba kalendārs tiek lietots, lai aprēķinātu importēto uzdevumu beigu datumus, lai pašreizējā projekta darba kalendārā definētās darba dienas un standarta darba stundas tiktu saglabātas. 

Izmaksu summas un pārdošanas cenas novērtējuma rindās tiek lietotas, lai nodrošinātu, ka cenām, kas ir unikālas attiecīgajam projektam vai projekta līgumam, būtu derīgi datumi.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Atšķirības starp projekta WBS un WBS veidni

-   Uzdevumiem WBS veidnēs nav sākuma datumu un beigu datumu.

WBS veidnēm nav iestatītas darba dienas un brīvdienas.

-   WBS veidnēm vienmēr tiek izmantots plānošanas kalendārs, kas iestatīts kā noklusējuma kalendārs visiem projektiem.

Noklusējuma plānošanas kalendārs tiek izmantots tikai, lai uzzinātu stundas standarta darba dienā.

-   WBS veidnei netiek kopētas pirmstecīgās attiecības.

Tā kā WBS veidnēm nav datumu, nav nepieciešama sākuma datumu loģika, kas ir balstīta uz priekštecīgā uzdevuma beigu datumu.

-   Izveidojot WBS veidnē uzdevumu, tiek automātiski izveidota darbaspēka izmaksu novērtējuma rinda. Pārdošanas cena un izmaksu summa tiek kopēta no atlasītā darbinieka.

Izdevumu un krājumu izmaksas var izveidot manuāli tāpat kā projekta WBS struktūrā.

-   Ja ir novirzes no šādas formulas, tiek parādītas plānošanas kļūdas:

Darbs = Resursu skaits × Ilgums × Stundu skaits standarta darba dienā 

Visas plānošanas kļūdas varat labot vienlaicīgi, noklikšķinot uz **Labot visas plānošanas kļūdas**. 

Vai arī varat labot plānošanas kļūdas atsevišķi, noklikšķinot uz brīdinājuma ikonas katram uzdevumam.




