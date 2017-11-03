---
title: "Projektu līgumi"
description: "Šajā rakstā aprakstīti projektu līgumi, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī sniegti to piemēri, un aprakstīts, kā var pārvaldīt līgumus un izrakstīt projekta rēķinus debitoriem programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="project-contracts"></a>Projekta līgumi

[!include[banner](../includes/banner.md)]


Šajā rakstā aprakstīti projektu līgumi, ko var izveidot dažādu veidu projektiem un finansējuma avotiem, kā arī sniegti to piemēri, un aprakstīts, kā var pārvaldīt līgumus un izrakstīt projekta rēķinus debitoriem programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise.

Projekta tips, ko izveidojat projekta līgumam, nosaka metodi, kas tiek izmantota projekta debitoru rēķinu izrakstīšanai. Varat mainīt projekta līgumu un saistīto projektu, bet projekta tipu nevar mainīt. 

Izmantojot projekta līgumu, vienlaicīgi varat izrakstīt rēķinu vienam vai vairākiem projektiem. Projekta līgums palīdz arī garantēt konsekventu rēķinu izrakstīšanas procedūru katram projekta struktūrā iekļautajam apakšprojektam. 

Katram projektam, kam tiks izrakstīts rēķins, ir jābūt saistītam ar projekta līgumu. Projekta līguma iestatījumi attiecas uz visiem projektiem un apakšprojektiem, kas ir saistīti ar attiecīgo projekta līgumu. 

Projekta līgumā var norādīt vienu vai vairākus finansējuma avotus. Līdz ar to norēķinus varat sadalīt starp vairākiem finansētājiem, iestatīt finansējuma ierobežojumus, lai no finansējuma avotiem netiktu iekasēts vairāk par noteikto summu, un konfigurēt iekasējamo izdevumu finansējuma nosacījumus.

## <a name="funding-for-project-contracts"></a>Projekta līgumu finansējums
Noteiktos projektu līgumos ir norādīts, ka par projekta izmaksu finansēšanu kopīgi atbild vairākas puses. Daži piemēri:

-   Liels debitors ar vairākām nodaļām pieprasa, lai projekta finansējums tiktu sadalīts pēc nodaļas.
-   Jūsu uzņēmumam un kādai ārējai organizācijai ir kopējas izmaksas par lielu projektu.
-   Divas pašvaldības kopīgi finansē ceļubūves projektu.
-   Tilta projektu finansē valsts dotācijas un privāta korporācija.

Programmatūrā Finance and Operations norēķinus par vienu transakciju vai visu projektu varat sadalīt starp vairākiem debitoriem, dotācijām vai organizācijām. 

Projektos, kuriem ir vairāki finansētāji, visas puses, kas sniedz līdzekļus projekta papildu finansēšanai, tiek saukti par finansējuma avotiem. Kad debitors, organizācija vai dotācija ir definēti kā finansējuma avots, to var piešķirt vienam vai vairākiem finansējuma nosacījumiem. Finansējuma nosacījumi ietver kritērijus, kas nosaka, kā izmaksas tiek sadalītas starp projekta dažādajiem finansējuma avotiem. 

Tā kā uzkrātos krājumus, piemēram, tādus, kas ir minēti pirkšanas pieprasījumos un pirkšanas pasūtījumos, nevar sadalīt, sadales laikā šo izmaksu summu nevar sadalīt starp vairākiem finansējuma avotiem. Tāpēc finansējuma avota vērtība paliek 0 (nulle), līdz tiek iegrāmatota krājumu izejas plūsma. Kad tiek grāmatota krājumu izejas plūsma, izmaksu summa tiek sadalīta saskaņā ar projekta konta sadales nosacījumiem.

Tālāk ir aprakstītas dažas darbības, kas varētu atvieglot norēķinu sadali starp vairākiem finansējuma avotiem.

-   Norādiet, ka visās projektam ievadītajās transakcijās ir jāizmanto tā pati pārdošanas valūta kā projekta līgumā.
-   Iestatiet finansējuma ierobežojumus, lai finansējuma avotam netiktu izrakstīts rēķins, kas pārsniedz noteiktu summu saistībā ar projektu.
-   Konfigurējiet finansējuma nosacījumus un finansējuma ierobežojumus katram darbiniekam, krājumam, kategorijai, kategoriju grupai un transakcijas tipam (vai visiem transakciju tipiem).
-   Atlasiet papildu sākuma un beigu datumus, lai definētu periodu, kad ir spēkā katrs finansējuma nosacījums.
-   Norādiet procentus, par ko ir atbildīgs katrs finansējuma avots.
-   Norādiet, kurš finansējuma avots ir atbildīgs par noapaļošanas atšķirībām, ko izraisa finansējuma sadalījuma aprēķini.
-   Iestatiet kārtulas, kas nosaka veidu, kādā par projekta izmaksām tiek izrakstīti rēķini ārējiem debitoriem un kā projekta izmaksas tiek iekasētas iekšējām organizācijām.
-   Reģistrējiet transakcijas aizturēšanas finansējuma kontā, līdz var iegūt papildu finansējumu vai līdz izlemjat šīs izmaksas segt iekšēji.

Lai noteiktu, kuru nodokļu grupu saistīt ar kādu transakciju, projektā tiek meklēta nodokļu grupas piešķire. Ja nodokļu grupas piešķire nav veikta projekta līmenī, tiek meklēts projekta līgumā.

### <a name="example-multiple-funding-sources-simple"></a>Piemērs. Vairāki finansējuma avoti (vienkārši)

Nākamajā tabulā ir sniegti scenāriji finansējuma sadalījuma pārvaldīšanai starp vairākiem finansējuma avotiem. Šie scenāriji ir balstīti uz šādiem pieņēmumiem:

-   Prioritātes iestatījumi ir iestrādāti līdzekļu sadalījumā, pirms tiek lietoti citi finansējuma nosacījumu kritēriji.
-   Nav norādīts datumu diapazons, lai definētu periodu d, kad ir spēkā šie finansējuma nosacījumi.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenārijs</strong></td>
<td><strong>Finansējuma avots </strong></td>
<td><strong>Sadalījuma procenti </strong></td>
<td><strong>Sadalījuma prioritāte </strong></td>
</tr>
<tr class="even">
<td>Jūs vēlaties piešķirt izmaksas vienam finansējuma avotam, līdz tā līdzekļi ir beigušies, piešķirt izmaksas otram finansējuma avotam, līdz tā līdzekļi ir beigušies, un visbeidzot atlikušās izmaksas piešķirt trešajam finansējuma avotam.</td>
<td><ul>
<li>1.　finansējuma　avots</li>
<li>2.　finansējuma　avots</li>
<li>3.　finansējuma　avots</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Jūs vēlaties 75 procentus izmaksu piešķirt vienam finansējuma avotam un 25 procentus piešķirt otram finansējuma avotam. Kad kādam no šiem finansējuma avotiem ir beigušies līdzekļi, jūs vēlaties atlikušās izmaksas samaksāt no trešā finansējuma avota.</td>
<td><ul>
<li>1.　finansējuma　avots</li>
<li>2.　finansējuma　avots</li>
<li>3.　finansējuma　avots</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Jūs vēlaties 75 procentus izmaksu piešķirt vienam finansējuma avotam un 25 procentus piešķirt otram finansējuma avotam. Kad kādam no šiem finansējuma avotiem ir beigušies līdzekļi, jūs vēlaties atlikušās izmaksas sadalīt starp trešo finansējuma avotu un ceturto finansējuma avotu.</td>
<td><ul>
<li>1.　finansējuma　avots</li>
<li>2.　finansējuma　avots</li>
<li>3.　finansējuma　avots</li>
<li>4.　finansējuma　avots</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Jūs vēlaties pirmos 25 procentus izmaksu piešķirt vienam finansējuma avotam, un pārējo piešķirt otram finansējuma avotam.</td>
<td><ul>
<li>1.　finansējuma　avots</li>
<li>2.　finansējuma　avots</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Piemērs. Vairāki finansējuma avoti (kompleksi)

Jums ir trīs finansējuma avoti, kurus vēlaties izmantot šādā secībā:

1.  Izmantot 2. finansējuma avotu 3. finansējuma avotu vienādi, līdz 2. finansējuma avota līdzekļi ir beigušies.
2.  Turpināt lietot 3. finansējuma avotu, līdz tā līdzekļi ir beigušies.
3.  Lietot 1. finansējuma avotu pēc tam, kad 3. finansējuma avota līdzekļi ir beigušies.

Lai sasniegtu šo mērķi, jums ir jārīkojas tālāk aprakstītajā veidā.

-   Iestatiet finansējuma ierobežojumus 2. finansējuma avotam un 3. finansējuma avotam to attiecīgajām summām.
-   Izveidojiet šādus finansējuma nosacījumus:
    -   1. nosacījums (1. prioritāte): 50 procentus no transakcijām piešķirt 2. finansējuma avotam un 50 procentus piešķirt 3. finansējuma avotam.
    -   2. nosacījums (2. prioritāte): 100 procentus no transakcijām piešķirt 3. finansējuma avotam.
    -   3. nosacījums (3. prioritāte): 100 procentus no transakcijām piešķirt 1. finansējuma avotam.

Šāds iestatījums darbojas, jo transakcijas tiek pārbaudītas attiecībā pret nosacījumiem un ierobežojumiem, lai noteiktu, vai kāds no tiem attiecas uz šo transakciju. Ja uz transakciju neattiecas kādi īpaši nosacījumi vai ierobežojumi, tiek lietots nosacījums Visas transakcijas. Nosacījums Visas transakcijas salīdzina visas transakcijas. 

Ja tiek atrasts nosacījums, kas atbilst transakcijai, tad vispirms tiek lietots procentuālais daudzums, kurš ir piešķirts šajā nosacījumā, bet tikai pēc tam, kad atbilstības ir pārbaudītas pret visiem iestatītajiem ierobežojumiem. Ja ir sasniegts ierobežojums un finansējuma avota līdzekļi ir beigušies, ar šo finansējuma ierobežojumu saistītie finansējuma nosacījumi tiek ignorēti, un programma pārbauda nākamos piemērojamos nosacījumus. 

Noteiktos gadījumos saskaņā ar nosacījumiem sadali var izpildīt tikai daļai no transakcijas. Tā var notikt, jo transakcijas sadales laikā tiek sasniegts ierobežojums. Šajā gadījumā saskaņā ar šo nosacījumu tiek sadalīta tikai noteikta summa, piemēram, 50 procenti katram finansējuma avotam. Tā notiek 1. nosacījumā, kas šajā sadaļā tika aprakstīts iepriekš. Atlikums tiek sadalīts saskaņā ar nākamo piemērojamo nosacījumu attiecīgajā secībā. 

Nākamajā tabulā šis scenārijs ir izpētīts detalizētāk.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokuss </strong></td>
<td><strong>Detalizēta informācija</strong></td>
</tr>
<tr class="even">
<td>Finansējuma nosacījumi</td>
<td><ul>
<li>1. nosacījums (1. prioritāte): Visas transakcijas. Piešķirt 2. finansējuma avotam 50% un 3. finansējuma avotam 50%.</li>
<li>2. nosacījums (2. prioritāte): Visas transakcijas. Piešķirt 3. finansējuma avotam 100%.</li>
<li>3. nosacījums (2. prioritāte): Visas transakcijas. Piešķirt 1. finansējuma avotam 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansējuma ierobežojumi</td>
<td><ul>
<li>1. finansējuma avota ierobežojums = 10 000,00</li>
<li>2. finansējuma avota ierobežojums = 500,00</li>
<li>3. finansējuma avota ierobežojums = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>1. transakcija</td>
<td><strong>Transakcijas summa:</strong> 100,00<strong>Finansējums:</strong> transakcija tiek apmaksāta tikai saskaņā ar 1. nosacījumu, jo pēc 1. nosacījuma piemērošanas transakcija ir apmaksāta pilnībā. Transakcijas finansēšana tiek vienādi sadalīta starp 2. finansējuma avotu un 3. finansējuma avotu.
<ul>
<li>2. finansējuma avots: 50,00</li>
<li>3. finansējuma avots: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>2. transakcija</td>
<td><strong>Transakcijas summa:</strong> 5000,00<strong>Finansējums:</strong> transakcija tiek apmaksāta saskaņā ar visiem trim nosacījumiem.<strong>1. nosacījums</strong>
<ul>
<li>2. finansējuma avots: 450,00</li>
<li>3. finansējuma avots: 450,00</li>
</ul>
<strong>2. nosacījums</strong>
<ul>
<li>3. finansējuma avots: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>3. nosacījums</strong>
<ul>
<li>1. finansējuma avots: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Kopējie līdzekļi, kas tiek sadalīti katram finansējuma avotam</td>
<td><ul>
<li>1. finansējuma avots: 3850,00</li>
<li>2. finansējuma avots: 500,00</li>
<li>3. finansējuma avots: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Norēķinu noteikumi
Veicot pārrunas ar debitoru par projekta līgumu, jums jānorāda, kā un kad jūs varat debitoram izrakstīt rēķinu par darbu pie projekta. Kad esat iestatījis projekta līgumu un projektu, varat projektam iestatīt norēķinu kārtulas. Norēķinu kārtulu pamatā ir projekta nosacījumi, kas norādīti projekta līgumā. Norēķinu kārtulas, ko varat izveidot, ir atkarīgas no projekta līguma nosacījumiem un projekta veida, piemēram, laika un materiālu vai fiksētas cenas projekta, ko saistāt ar norēķinu kārtulu. Varat izveidot vairāk nekā vienu norēķinu kārtulu projekta līgumam. Norēķinu kārtulu varat piešķirt arī vairākiem projektiem, kas ir saistīti ar vienu projekta līgumu un kuriem ir līdzīgi norēķinu nosacījumi. 

Varat iestatīt tālāk norādīto veidu norēķinu kārtulas.

-   **Piegādes vienība** — rēķins debitoram tiek izrakstīts pēc piegādes vienības pabeigšanas. Piegādes vienības tiek definētas līgumā.
-   **Norise** — rēķins debitoram tiek izrakstīts, kad ir pabeigta noteikta procentuālā daļa no projekta. Varat iestatīt norēķinu kārtulas, lai automātiski aprēķinātu pabeigtā darba procentuālo daļu, vai arī varat manuāli aprēķināt pabeigtā darba procentuālo daļu un debitora rēķina summu.
-   **Atskaites punkts** — rēķins debitoram tiek izrakstīts par pilnu projekta atskaites punkta summu, kad ir sasniegts šis atskaites punkts.
-   **Papildmaksa** — rēķins debitoram tiek izrakstīts par jūsu pakalpojumiem, kā arī par pārvaldības maksu, kas parasti ir procentuāls daudzums no pakalpojumu izmaksām.
-   **Laiks un materiāli** — rēķins debitoram tiek izrakstīts par projektam patērēto laiku un materiāliem.

Visu veidu norēķinu kārtulām varat norādīt ieturamo procentuālo daļu, kas tiek atņemta no debitora rēķiniem, līdz projekts sasniedz iepriekš noteikto stadiju. Maksājumu ieturējuma procentuālā daļa ir norādīta projekta līgumā. Summa tiek aprēķināta, pamatojoties uz debitora rēķina rindu kopējās vērtības, un atņemta no tās. 

Norēķinu kārtulām **Laiks un materiāli** un **Norise** varat piešķirt rēķinā iekļaujamas kategorijas. Rēķinā iekļaujamās kategorijas norāda transakcijas, kas būtu jāiekļauj debitoru rēķinos. 

Kad esat gatavs izrakstīt debitoram rēķinu, projekta rēķinā iekļaujamā summa tiek aprēķināta, pamatojoties uz norēķinu kārtulām, un tiek izveidots projekta rēķina priekšlikums. 

Nākamajās sadaļās ir sniegti piemēri, kuros parādīts, kā iestatīt un pārvaldīt projekta norēķinu kārtulas.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Piemērs. Uz piegādāto vienību skaitu balstītas norēķinu kārtulas izveide

Jūsu organizācijai noslēdz līgumu par kopā piecu apmācību sesiju nodrošināšanu debitora darbiniekiem un katras apmācības sesijas maksu 10 000. Pēc katras apmācību sesijas jūs izrakstāt debitoram rēķinu. 

Kad iestatāt norēķinu kārtulas šim līgumam, jūs izmantojat tālāk norādītās vērtības.

-   Piegādes vienība ir viena apmācību sesija.
-   Vienības cena ir 10 000 par vienu apmācības sesiju.
-   Kopējais vienību skaits ir piecas apmācības sesijas.

Kad esat pabeidzis vienu apmācības sesiju, varat izveidot rēķinu 10 000 apmērā par pirmo vienību, kas ir piegādāta, un nosūtīt šo rēķinu debitoram.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Piemērs. Uz noteiktu projekta pabeigtības procentuālo daļu balstītas norēķinu kārtulas izveide (manuāls aprēķins)

Jūsu organizācija, programmatūras konsultāciju uzņēmums, noslēdz līgumu ar klientu par izstrādes procesā esoša klienta produkta daļas izstrādāšanu. Jūsu organizācija apņemas piegādāt programmatūras kodu sešu mēnešu periodā. Klients piekrīt maksāt jūsu organizācijai par darbu kopumā 100 000. Jūs izveidojat norēķinu kārtulu, lai izrakstītu rēķinu debitoram, pamatojoties uz projekta ietvaros pabeigtā darba procentuālo daļu, kā norādīts līgumā.

-   Pirmā mēneša beigās jūs tiekaties ar klientu, lai noteiktu pabeigtā darba procentuālo daļu. Pēc projekta pārskatīšanas jūs un debitors izlemjat, ka projekta pabeigtības līmenis ir 15 procenti.
-   Jūs izveidojat rēķinu par 15 000 (15 procenti no 100 000) un nosūtāt to debitoram.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Piemērs. Uz noteiktu projekta pabeigtības procentuālo daļu balstītas norēķinu kārtulas izveide (automātisks aprēķins)

Jūsu organizācija, programmatūras izstrādes firma, piekrīt debitoram izstrādāt algu uzskaites pakotni par 30 000. Klients piekrīt maksāt jūsu organizācijai, pamatojoties uz pabeigtā darba procentuālo daļu. Jūs novērtējat, ka projekta izmaksas ir 20 000. Projekta līgumā ir norādītas darba kategorijas, ko jūs izmantojat norēķinu procesā. Iestatiet norēķinu nosacījumus, kas automātiski aprēķina rēķina summas procentuālajam daudzumam darba, kas ir pabeigts katrai kategorijai. Katrai kategorijai jāiestata budžets.

-   **Izstrāde** — izmaksas 15 000 un ieņēmumi 20 000
-   **Uzstādīšana** — izmaksas 5000 un ieņēmumi 10 000

Pirmo reizi izveidojot debitora rēķinu, rēķina summa tiek automātiski aprēķināta, pamatojoties uz tālāk norādīto informāciju.

-   Pēc mēneša projekta darbinieks iesniedz projekta darba laika uzskaites tabulu. Darbinieka darba stundu izmaksas ir 5000 par izstrādi un 1000 par uzstādīšanu. Izstrādes darba pabeigtība ir 33 procenti (5000 faktiskās izmaksas/15 000 budžeta izmaksas), un uzstādīšanas darba pabeigtība ir 20 procenti (1000 faktiskās izmaksas/5000 budžeta izmaksas).
-   Rēķina summa 8667 tiek aprēķināta automātiski (33 procenti no 20 000 + 20 procenti no 10 000).
-   Jūs izveidojat rēķinu par 8667 un nosūtāt to debitoram.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Piemērs. Uz saskaņotiem atskaites punktiem balstītas norēķinu kārtulas izveide

Jūsu organizācija, vadības konsultāciju uzņēmums, piekrīt veikt tirgus izpēti par patēriņa preci, ko debitors plāno pārdot. Klients piekrīt izmantot jūsu pakalpojumus trīs mēnešus — sākot no marta — un piekrīt maksāt jūsu organizācijai 50 000. Projektam ir trīs atskaites punkti:

-   1. atskaites punkts: patērētāju datu apkopošana — 31. marts
-   2. atskaites punkts: patēriņa datu analīze — 30. aprīlis
-   3. atskaites punkts: priekšlikuma iesniegšana par preču dzīvotspēju — 31. maijs

Debitors piekrīt maksāt jūsu organizācijai 10 000 par pirmo atskaites punktu, 20 000 par otro atskaites punktu, un 20 000 par trešo atskaites punktu. 

Kad iestatāt projekta līgumu, jūs piekrītat debitoram izrakstīt rēķinu, pamatojoties uz izpildīto atskaites punktu. Norēķinu kārtulas iestatīšanā ietvertas tālāk norādītās darbības.

-   Definējiet projekta atskaites punktus.
-   Nosakiet debitora rēķinā iekļaujamo summu, kad tiek pabeigts katrs atskaites punkts.

Kad 31. martā tiek pabeigts pirmais atskaites punkts, jūs atzīmējat šo atskaites punktu kā pabeigtu, un pēc tam izveidojat rēķinu par 10 000 un nosūtāt to debitoram. Rēķinu par atskaites punktu nevar izveidot, kamēr šo atskaites punktu neesat atzīmējis kā pabeigtu.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Piemērs. Uz pakalpojumiem un pārvaldības maksu pamatotas norēķinu kārtulas izveide

Jūsu organizācija, vadības konsultāciju firma, piekrīt veikt tirgus izpēti, lai novērtētu dzīvotspēju kādam produktam, ko izstrādā debitors — kāds mazumtirdzniecības uzņēmums. Līguma nosacījumos ir norādīts, ka jūs nodrošināsiet trīs labāko vadības konsultantu pakalpojumus, kuri veikts izpēti, pamatojoties uz patērēto laiku un materiāliem. Debitors piekrīt maksāt summu 100/stundā, kā arī pārvaldības maksu 10 procentu apmērā par konsultāciju stundām, kuras tiek apmaksātas projekta ietvaros. 

Iestatot projekta līgumu, izveidojiet norēķinu kārtulu, kas pievieno 10 procentu pārvaldības maksu konsultāciju stundām, kuras tiek apmaksātas projekta ietvaros. 

Izveidojot rēķinu klientam, tajā iekļauta 10 procentu pārvaldības maksa, kā arī konsultāciju stundu izmaksas. Piemēram, ja trīs konsultanti projekta ietvaros kopā ir strādājuši 200 stundas, rēķins par summu 22 000 tiek izveidots, pamatojoties uz tālāk norādīto aprēķinu.

-   200 stundas par likmi 100 stundā = 20 000
-   10 procentu pārvaldības maksa = 2000
-   Rēķina kopsumma = 22 000

Ja klientam piemērojamās maksas ir ar apliekamas ar nodokli un projekta līgumā tiek atlasīta PVN grupa, maksu norēķinu kārtulā tiek automātiski ievadīta PVN grupa.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Piemērs. Norēķinu kārtulas izveidošana par patērēto laiku un izmantotajiem materiāliem

Jūsu organizācija, programmatūras konsultāciju uzņēmums, piekrīt nodrošināt piecus tehniskos konsultantus, kas nākamo sešu mēnešu laikā debitoram strādās pie programmatūras izstrādes projekta. Debitors piekrīt maksāt summu 150 par katru konsultācijas stundu, kā arī segt kancelejas piederumu izmaksas. Jūsu organizācija nosūta rēķinu klientam katra mēneša beigās. 

Kad iestatāt projekta līgumu, jūs piekrītat debitoram katru mēnesi izrakstīt rēķinu par projektā patērēto laiku un izmantotajiem materiāliem. Jāizveido norēķinu kārtula ar tālāk norādīto informāciju.

-   Līguma periods ir seši mēneši.
-   Konsultāciju laiks tiek aprēķināts atbilstoši likmei 150/stundā.
-   Kancelejas preču izmaksas tiek iekļautas rēķinā, un projekta kopējās izmaksas nedrīkst pārsniegt 10 000.
-   Debitora rēķins projekta laikā tiek izveidots katra kalendārā mēneša beigās.

Pirmajā mēnesī projekta konsultanti ieraksta kopumā 800 stundas. Kancelejas preču izmaksas, kuras tiek iekļautas projekta rēķinā, ir 2000. Līdz ar to mēneša beigās jūs izveidojat rēķinu par summu 122 000, kura tiek aprēķināta kā 800 stundas par likmi 150/stundā, kā arī 2000 par kancelejas precēm.




