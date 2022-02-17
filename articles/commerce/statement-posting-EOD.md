---
title: Izrakstu grāmatošanas funkcionalitātes uzlabojumi
description: Šajā tēmā ir aprakstīti izrakstu grāmatošanas līdzeklim veiktie uzlabojumi.
author: analpert
ms.date: 01/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 6ee0cea76be05634aa21643acef5b341f19d75ef
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087607"
---
# <a name="improvements-to-statement-posting-functionality"></a>Izrakstu grāmatošanas funkcionalitātes uzlabojumi

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīti pirmie izrakstu grāmatošanas līdzeklim veiktie uzlabojumi. Šie uzlabojumi ir pieejami versijā Microsoft Dynamics 365 for Finance and Operations 7.3.2.

## <a name="activation"></a>Aktivizēšana

Pēc noklusējuma versijas Finance and Operations 7.3.2 izvietošanas laikā programma ir iestatīta izrakstu grāmatošanas mantoto līdzekļu izmantošanai. Lai iespējotu uzlaboto izrakstu grāmatošanas līdzekli, jums tam ir jāaktivizē konfigurācijas atslēga.

- Dodieties uz **Sistēmas administrēšana** \> **Iestatīšana** \> **Licences konfigurācija** un pēc tam zarā **Retail un Commerce** noņemiet atzīmi izvēles rūtiņai **Izraksti (mantojuma)** un atzīmējiet izvēles rūtiņu **Izraksti**.

Kad ir ieslēgta jaunā konfigurācijas atslēga **Izraksti**, ir pieejams jauns izvēlnes vienums ar nosaukumu **Izraksti**. Šis izvēlnes elements ļauj jums manuāli izveidot, aprēķināt un grāmatot izrakstus. Jebkurš izraksts, kas izraisa kļūdu, kad tiek izmantots pakešveida grāmatošanas process, ir pieejams arī, izmantojot šo izvēlnes vienumu. (Kad ir ieslēgta konfigurācijas atslēga **Izraksti (mantojuma)**, šī izvēlnes vienuma nosaukums ir **Atvērtie izraksti**.)

Commerce ietver tālāk norādītās validācijas, kas ir saistītas ar šīm konfigurācijas atslēgām.

- Abas konfigurācijas atslēgas nevar būt ieslēgtas vienlaikus.
- Visām operācijām, kas attiecīgajam izrakstam tiek veiktas tā dzīves cikla laikā (operācijām Izveidot, Aprēķināt, Notīrīt, Grāmatot un citām) ir jāizmanto tā pati konfigurācijas atslēga. Piemēram, nevar izveidot un aprēķināt kādu izrakstu, kamēr ir ieslēgta konfigurācijas atslēga **Izraksts (mantojuma)**, un pēc tam mēģināt to pašu izrakstu grāmatot, kamēr ir ieslēgta konfigurācijas atslēga **Izraksts**.

> [!NOTE]
> Iesakām izmantot konfigurācijas atslēgu **Izraksti** uzlabotajam izrakstu grāmatošanas līdzeklim, ja vien jums nav pārliecinoši iemesli konfigurācijas atslēgas **Izraksti (mantojuma)** izmantošanai tās vietā. Microsoft turpinās ieguldīt jaunajā un uzlabotajā izrakstu grāmatošanas līdzeklī, un ir svarīgi, lai jūs pārietu uz tā lietošanu pēc iespējas ātrāk, izmantojot tā sniegtās priekšrocības. Mantojuma izrakstu grāmatošanas līdzeklis ir novecojis, sākot ar 8.0 laidienu.

## <a name="setup"></a>Iestatīšana

Kā daļa no izrakstu grāmatošanas līdzekļa uzlabojumiem lapas **Commerce parametri** cilnes **Grāmatošana** kopsavilkuma cilnē **Izraksts** ir ieviesti trīs jauni tālāk aprakstītie parametri.

- **Atspējot izraksta notīrīšanu** — šī opcija ir pieejama tikai mantojuma izrakstu grāmatošanas līdzeklim. Iesakām šo opciju iestatīt uz **Nē**, lai neļautu lietotājiem notīrot izrakstus, kas atrodas daļēji grāmatotā stāvoklī. Ja tiek notīrīti izraksti, kas ir daļēji grāmatotā stāvoklī, dati tiek bojāti. Šī opcija ir jāiestata uz **Jā** tikai izņēmuma gadījumos.
- **Rezervēt krājumus aprēķināšanas laikā** — krājuma rezervēšanai iesakām lietot pakešuzdevumu **Grāmatot krājumus** un šo opciju iestatīt uz **Nē**. Kad šī opcija ir iestatīta uz **Nē**, uzlabotais izrakstu grāmatošanas līdzeklis aprēķināšanas laikā nemēģina izveidot krājumu rezervēšanas ierakstus (ja ieraksti vēl nav izveidoti, izmantojot pakešuzdevumu **Grāmatot krājumus**). Tā vietā šis līdzeklis izveido krājumu rezervēšanas ierakstus tikai grāmatošanas laikā. Šī implementācija bija dizaina izvēle, un tā bija balstīta uz faktu, ka laika intervāls starp aprēķināšanas procesu un grāmatošanas procesu parasti ir mazs. Taču, ja vēlaties rezervēt krājumus aprēķināšanas laikā, šo opciju varat iestatīt uz **Jā**.

    Mantojuma izrakstu grāmatošanas līdzeklis vienmēr rezervē krājumus izraksta aprēķināšanas procesa laikā (ja rezervācija vēl nav veikta, izmantojot pakešuzdevumu **Grāmatot krājumus**), neatkarīgi no šīs opcijas iestatījuma.

- **Atspējot nepieciešamo uzskaiti** — kad šī opcija ir iestatīta uz **Jā**, grāmatošanas process izrakstam turpinās pat tad, ja starpība starp aprēķināto summu un transakcijas summu izrakstā ir ārpus sliekšņa vērtības, kas veikaliem ir definēta kopsavilkuma cilnē **Izraksts**.

> [!NOTE]
> Kopš Commerce versijas 10.0.14 izlaišanas, kad **Mazumtirdzniecības paziņojumi — Trickle feed** funkcija ir iespējota, **Izlikt inventarizāciju** pakešu darbs vairs nav piemērojams, un to nevar palaist.

Turklāt kopsavilkuma cilnē **Pakešveida apstrāde** cilnē **Posting** lapā **Commerce rekvizīti** ir ieviesti tālāk minētie parametri. 

- **Maksimālais paralēli grāmatojamo izrakstu skaits** — šajā laukā noteikts pakešuzdevumu skaits, kas tiks izmantoti vairāku izrakstu grāmatošanai. 
- **Maksimālais pasūtījumu apstrādes pēc ieraksta pavedienu skaits** — šis lauks atspoguļo maksimālo pavedienu skaitu, ko izmanto ieraksta grāmatošanas pakešuzdevums, lai izveidotu pārdošanas pasūtījumus vienam ierakstam un izrakstītu rēķinu. Kopējais pavedienu skaits, kas tiks izmantots izraksta grāmatošanas procesā, tiks aprēķināts, ņemot vērā vērtību šajā parametrā, kas reizināta ar parametra **Maksimālais paralēli grāmatojamo izrakstu skaits** vērtību. Iestatot pārāk lielu šī parametra vērtību par lielu, var negatīvi ietekmēt izraksta grāmatošanas procesa veiktspēju.
- **Maksimālais apkopojumā iekļauto transakciju rindu skaits** — šis lauks nosaka transakciju rindu skaitu, kas tiks iekļautas vienā apkopotā transakcijā, pirms tiek izveidota jauna. Apkopotās transakcijas tiek veidotas, pamatojoties uz dažādiem apkopošanas kritērijiem, piemēram, debitors, biznesa datums vai finanšu dimensijas. Ir svarīgi atzīmēt, ka vienas transakcijas rindas netiks sadalītas pa dažādām apkopotām transakcijām. Tas nozīmē, ka pastāv iespēja, ka rindu skaits apkopotā darījumā ir nedaudz lielāks vai mazāks, pamatojoties uz tādiem faktoriem kā atšķirīgu produktu skaits.
- **Maksimālais pavedienu skaits veikala transakciju pārbaudei** — šis lauks nosaka pavedienu skaitu, kas tiks izmantoti transakciju pārbaudei, Transakciju pārbaude ir obligāta darbība, kas jāizpilda, pirms transakcijas var tikt ievilktas pārskatos. Turklāt ir nepieciešams definēt **Dāvanu kartes preci** kopsavilkuma cilnē **Dāvanu karte** (pieejama cilnē **Grāmatošana**, kas pieejama lapā **Commerce parametri**). Tas ir jādefinē, pat ja organizācija neizmanto dāvanu kartes.

Nākamajā tabulā ir norādītas ieteicamās vērtības iepriekšējiem parametriem. Šīs vērtības ir jāpārbauda un jāpielāgo izvietošanas konfigurācijai un pieejamajai infrastruktūrai. Jebkurš ieteicamo vērtību palielinājums var negatīvi ietekmēt citu pakešu apstrādi, un tas ir jāapstiprina.

| Parametrs | Ieteicamā vērtība | Detalizētā informācija |
|-----------|-------------------|---------|
| Maksimālais paralēli grāmatojamo pārskatu skaits | <p>Iestatiet šo parametru uz pakešuzdevumu skaitu, kas ir pieejams pakešu grupai, kurā darbojas **Paziņojums, apgalvojums** darbs.</p><p>**Vispārējs noteikums:** Reiziniet lietojumprogrammu objektu servera (AOS) virtuālo serveru skaitu ar vienam AOS virtuālajam serverim pieejamo pakešu uzdevumu skaitu.</p> | Šis parametrs nav piemērojams, ja **Mazumtirdzniecības paziņojumi — Trickle feed** funkcija ir iespējota. |
| Maksimālais pavedienu skaits pasūtījumu apstrādei katram pārskatam | Sāciet pārbaudīt vērtības plkst **4**. Parasti vērtība nedrīkst pārsniegt **8**. | Šis parametrs norāda pavedienu skaitu, kas tiek izmantoti, lai izveidotu un publicētu pārdošanas pasūtījumus. Tas norāda diegu skaitu, kas ir pieejami publicēšanai vienā paziņojumā. |
| Maksimālais transakcijas rindu skaits, kas iekļauts apkopojumā | Sāciet pārbaudīt vērtības plkst **1000**. Atkarībā no galvenās mītnes konfigurācijas mazāki pasūtījumi var būt izdevīgāki veiktspējai. | Šis parametrs nosaka rindu skaitu, kas izraksta grāmatošanas laikā tiks iekļautas katrā pārdošanas pasūtījumā. Kad šis skaitlis būs sasniegts, rindas tiks sadalītas jaunā secībā. Lai gan pārdošanas rindu skaits nebūs precīzs, jo sadalīšana notiek pārdošanas pasūtījuma līmenī, tas būs tuvu iestatītajam skaitam. Šis parametrs tiek izmantots, lai ģenerētu pārdošanas pasūtījumus mazumtirdzniecības darījumiem, kuriem nav norādīts klients. |
| Maksimālais pavedienu skaits veikala transakciju pārbaudei | Mēs iesakām iestatīt šo parametru uz **4**, un palielināt to tikai tad, ja nesasniedzat pieņemamu veiktspēju. Šajā procesā izmantoto pavedienu skaits nedrīkst pārsniegt pakešserverim pieejamo procesoru skaitu. Ja šeit piešķirat pārāk daudz pavedienu, tas var ietekmēt citu pakešu apstrādi. | Šis parametrs kontrolē darījumu skaitu, ko konkrētam veikalam var apstiprināt vienlaikus. |

> [!NOTE]
> Visi iestatījumi un parametri, kas ir saistīti ar izrakstu grāmatojumiem un kas ir definēti mazumtirdzniecības veikaliem un lapā **Commerce parametri**, ir lietojami uzlabotajam izrakstu grāmatošanas līdzeklim.

## <a name="processing"></a>Apstrādāšana

Izrakstus var aprēķināt un grāmatot pakešveidā, izmantojot izvēlnes vienumus **Aprēķināt izrakstus partijā** un **Grāmatot izrakstus partijā**. Tāpat izrakstus var manuāli aprēķināt un grāmatot, izmantojot izvēlnes vienumu **Izraksti**, kuru nodrošina uzlabotais izrakstu grāmatošanas līdzeklis.

Procedūras un darbības izrakstu aprēķināšanai un grāmatošanai pakešveidā ir tādi paši kā tie, kādi tika izmantoti mantotajā izrakstu grāmatošanas līdzeklī. Taču ir veikti būtiski uzlabojumi izrakstu aizmugursistēmas pamata apstrādē. Ar šiem uzlabojumiem apstrāde ir padarīta elastīgāka, kā arī ir nodrošināts labāks ieskats informācijā par stāvokļiem un kļūdām. Tādēļ lietotāji var risināt kļūdu galvenos cēloņus un pēc tam turpināt grāmatošanas procesu, neizraisot datu bojājumus un neizraisot nepieciešamību pēc datu labojumiem.

Nākamajās sadaļās ir aprakstīti daži galvenie izrakstu grāmatošanas līdzekļa uzlabojumi, kas tiek rādīti lietotāja interfeisā izrakstos un grāmatotajos izrakstos.

### <a name="status-details"></a>Detalizēta statusa informācija

Izrakstu grāmatošanas procedūrā visos aprēķināšanas un grāmatošanas procesos ir ieviests jauns stāvokļa modelis.

Nākamajā tabulā ir aprakstīti dažādie stāvokļi un to secība aprēķināšanas procesa laikā.

| Stāvokļu secība | Stāvoklis      | Apraksts |
|-------------|------------|-------------|
| 1           | Sākts    | Izraksts ir izveidots un ir gatavs aprēķināšanai. |
| 2           | Iezīmēts     | Izraksta tvērumā ietilpstošās transakcijas ir identificētas, pamatojoties uz izraksta parametriem, un tās ir atzīmētas ar izraksta ID. |
| 3           | Aprēķināts | Izraksta rindas ir aprēķinātas un parādītas. |

Nākamajā tabulā ir aprakstīti dažādie stāvokļi un to secība grāmatošanas procesa laikā.

| Stāvokļu secība | Stāvoklis                   | Apraksts |
|-------------|-------------------------|-------------|
| 1           | Pārbaudīts                 | Ir izpildītas vairākas validācijas, kas ir saistītas ar parametriem (piemēram, atgriešanas maksa) un ar izrakstu un izraksta rindām (piemēram, uzskaitītās summas un transakcijas summas starpība). |
| 2           | Apkopots              | Pārdošanas transakcijas klientiem ar nosaukumu un bez nosaukuma ir apkopotas, pamatojoties uz konfigurāciju. Katra apkopotā transakcija visbeidzot tiek konvertēta uz pārdošanas pasūtījumu. |
| 3           | Debitora pasūtījums ir izveidots  | Pamatojoties uz apkopoto transakciju, sistēmā ir izveidoti pārdošanas pasūtījumi. |
| 4           | Debitora pasūtījumam ir izrakstīts rēķins | Pārdošanas pasūtījumiem ir izrakstīts rēķins. |
| 5           | Atlaides ir iegrāmatotas        | Periodisko atlaižu žurnāli ir iegrāmatoti, pamatojoties uz konfigurāciju. |
| 6           | Ienākumi/izdevumi ir iegrāmatoti   | Ieņēmumu/izdevumu transakcijas ir iegrāmatotas kā dokumenti. |
| 7           | Dokumenti ir saistīti         | Maksājumu žurnāli ir izveidoti un saistīti ar atbilstošo rēķinu. |
| 8           | Maksājumi ir iegrāmatoti         | Maksājumu žurnāli ir iegrāmatoti. |
| 9           | Dāvanu kartes ir iegrāmatotas       | Dāvanu karšu transakcijas ir iegrāmatotas kā dokumenti. |
| 10          | Iegrāmatots                  | Izraksts ir atzīmēts kā iegrāmatots. |

Katrs stāvoklis iepriekšējās tabulās ir neatkarīgs, un starp stāvokļiem tiek veidota hierarhiska atkarība. Šī atkarība plūst no augšas uz leju. Ja kāda stāvokļa apstrādāšanas laikā sistēma konstatē kļūdas, izraksta statuss tiek atgriezts uz iepriekšējo stāvokli. Visi turpmākie procesa atkārtotie mēģinājumi tiek atsākti no nesekmīgā stāvokļa un turpina virzīties uz priekšu. Šai metodei ir tālāk noradītās priekšrocības.

- Lietotājam ir pilnīgi pārredzams stāvoklis, kur radās kļūda.
- Netiek pieļauta datu bojāšana. Piemēram, mantotajā izrakstu grāmatošanas līdzeklī bija gadījumi, kur par dažiem pārdošanas pasūtījumiem bija izrakstīti rēķini, bet citi pasūtījumi joprojām bija atvērti. Bija arī gadījumi, kur dažiem maksājumu žurnāliem segšanai nebija atbilstoša rēķina, jo rēķina grāmatošanā radās kļūda.
- Izraksta pašreizējo stāvokli lietotāji var redzēt, izmantojot pogu **Detalizēta informācija par statusu** izraksta grupā **Detalizēta informācija par izpildi**. Detalizētas statusa informācijas lapā ir trīs tālāk aprakstītās sadaļas.

    - Pirmajā sadaļā ir redzams izraksta pašreizējais statuss kopā ar kļūdas kodu un detalizētu kļūdas ziņojumu, ja ir radusies kāda kļūda.
    - Otrajā sadaļā ir redzami aprēķināšanas procesa dažādie stāvokļi. Vizuālās norādes ziņo par stāvokļiem, kas ir sekmīgi izpildīti, stāvokļiem, kurus nevarēja izpildīt kļūdu dēļ, un stāvokļiem, kas vēl nav pildīti.
    - Trešajā sadaļā ir redzami grāmatošanas procesa dažādie stāvokļi. Vizuālās norādes ziņo par stāvokļiem, kas ir sekmīgi izpildīti, stāvokļiem, kurus nevarēja izpildīt kļūdu dēļ, un stāvokļiem, kas vēl nav pildīti.

Turklāt otrās un trešās sadaļas galvenēs tiek rādīts attiecīgā procesa vispārējais statuss.

### <a name="event-logs"></a>Notikumu žurnāli

Izrakstam tiek izpildītas dažādas operācijas (piemēram, Izveidot, Aprēķināt, Notīrīt un Grāmatot), un izraksta dzīves cikla laikā var tikt izsauktas vairākas tās pašas operācijas instances. Piemēram, kad izraksts ir izveidots un aprēķināts, lietotājs var notīrīt šo izrakstu un aprēķināt to vēlreiz. Poga **Notikumu žurnāli** izraksta grupā **Detalizēta informācija par izpildi** sniedz pilnīgus auditācijas pierakstus par dažādajām operācijām, kuras tika izsauktas kādam izrakstam, kopā ar informāciju par šo operāciju izsaukšanas laiku.

### <a name="aggregated-transactions"></a>Apkopotās transakcijas

Grāmatošanas procesa laikā skaidras naudas darījumi tiek apkopoti pēc klienta un produkta. Tāpēc tiek samazināts izveidoto pārdošanas pasūtījumu un rindu skaits. Apkopotie darījumi tiek saglabāti sistēmā un tiek izmantoti pārdošanas pasūtījumu izveidošanai. Katra apkopotā transakcija sistēmā veido vienu atbilstošo pārdošanas pasūtījumu. 

Ja izraksts nav pilnībā publicēts, pārskatā varat skatīt apkopotos darījumus. Darbību rūtī, uz **Paziņojums, apgalvojums** cilnē **Izpildes detaļas** grupu, izvēlieties **Apkopotie darījumi**.

![Apkopoto darījumu poga izrakstam, kas nav pilnībā publicēts.](media/aggregated-transactions.png)

Ievietotajiem pārskatiem varat skatīt apkopotos darījumus vietnē **Ievietoti paziņojumi** lappuse. Darbību rūtī atlasiet **Uzziņas** un pēc tam atlasiet **Apkopotie darījumi**.

![Apkopoto darījumu komanda publicētajiem izrakstiem.](media/aggregated-transactions-posted-statements.png)

The **Pārdošanas pasūtījuma informācija** Apkopotā darījuma FastTab parāda šādu informāciju:

- **Ieraksta ID** — apkopotās transakcijas ID.
- **Izraksta numurs** — izraksts, pie kura pieder apkopotā transakcija.
- **Datums** — datums, kad apkopotā transakcija tika izveidota.
- **Pārdošanas ID** — pārdošanas pasūtījuma ID (ja no apkopotās transakcijas tiek izveidots pārdošanas pasūtījums). Ja šis lauks ir tukšs, atbilstošais pārdošanas pasūtījums nav izveidots.
- **Apkopoto rindu skaits** — apkopotās transakcijas un pārdošanas pasūtījuma kopējais rindu skaits.
- **Statuss** — apkopotās transakcijas pēdējais statuss.
- **Rēķina ID** — pārdošanas rēķina ID (ja par pārdošanas pasūtījumu apkopotajai transakcijai tika izveidots rēķins). Ja šis lauks ir tukšs, rēķins pārdošanas pasūtījums nav grāmatots.
- **Kļūdas kods** – Šis lauks ir iestatīts, ja apkopojums ir kļūdas stāvoklī.
- **Kļūdas ziņojums** – Šis lauks ir iestatīts, ja apkopojums ir kļūdas stāvoklī. Tas parāda detalizētu informāciju par to, kas izraisīja procesa neveiksmi. Varat izmantot kļūdas kodā esošo informāciju, lai novērstu problēmu, un pēc tam manuāli restartēt procesu. Atkarībā no atrisinājuma veida, apkopotie pārdošanas apjomi, iespējams, būs jādzēš un jāapstrādā jaunā paziņojumā.

![Pārdošanas pasūtījuma informācijas lauki apkopotā darījuma ātrās cilnes.](media/aggregated-transactions-error-message-view.png)

The **Darījuma informācija** Apkopotā darījuma FastTab parāda visus darījumus, kas ir iekļauti apkopotajā darījumā. Apkopotās transakcijas apkopotajās rindās tiek rādīti visi no transakcijām apkopotie ieraksti. Apkopotajās rindās tiek rādīta arī tāda detalizētā informācija kā krājums, variants, daudzums, cena, neto summa, vienība un noliktava. Būtībā katra apkopotā rinda atbilst vienai pārdošanas pasūtījuma rindai.

![Darījuma informācija Apkopotā darījuma ātrā cilne.](media/aggregated-transactions-sales-details.png)

Dažās situācijās apkopotajiem darījumiem var neizdoties publicēt to konsolidēto pārdošanas pasūtījumu. Šādās situācijās kļūdas kods tiks saistīts ar paziņojuma statusu. Lai skatītu tikai apkopotos darījumus, kuros ir kļūdas, varat iespējot **Rādīt tikai neveiksmes** filtrēt apkopoto darījumu skatā, atzīmējot izvēles rūtiņu. Iespējojot šo filtru, rezultāti tiek ierobežoti līdz apkopotiem darījumiem, kuros ir kļūdas, kuras ir jāatrisina. Informāciju par šo kļūdu labošanu skatiet sadaļā [Rediģēt un pārbaudīt tiešsaistes pasūtījumu un asinhrono klientu pasūtījumu darījumus](edit-order-trans.md).

![Apkopoto transakciju skata izvēles rūtiņa filtram Rādīt tikai kļūdas.](media/aggregated-transactions-failure-view.png)

Uz **Apkopotie darījumi** lapā varat lejupielādēt XML konkrētam apkopotam darījumam, atlasot **Eksportēt apkopojuma datus**. Varat pārskatīt XML jebkurā XML formatētājā, lai redzētu faktiskos datus, kas saistīti ar pārdošanas pasūtījuma izveidi un ievietošanu. XML faila lejupielādēšanas funkcionalitāte apkopotajām transakcijām nav pieejama izrakstiem, kas ir grāmatoti.

![Poga Eksportēt apkopotos datus lapā Apkopotie darījumi.](media/aggregated-transactions-export.png)

Ja kļūdu nevar novērst, labojot datus par pārdošanas pasūtījumu vai datus, kas atbalsta pārdošanas pasūtījumu, **Dzēst klienta pasūtījumu** poga ir pieejama. Lai dzēstu pasūtījumu, atlasiet apkopoto darījumu, kas neizdevās, un pēc tam atlasiet **Dzēst klienta pasūtījumu**. Tiks dzēsts gan apkopotais darījums, gan atbilstošais pārdošanas pasūtījums. Tagad varat pārskatīt darījumus, izmantojot rediģēšanas un audita funkcionalitāti. Tos var arī atkārtoti apstrādāt, izmantojot jaunu paziņojumu. Kad visas kļūmes ir novērstas, varat atsākt izraksta publicēšanu, palaižot attiecīgā priekšraksta funkciju Post izraksta.

![Poga Dzēst klientu pasūtījumu apkopoto darījumu skatā.](media/aggregated-transactions-delete-cust-order.png)

Apkopoto darījumu skats nodrošina šādas priekšrocības:

- Lietotājam ir pārredzamas apkopotās transakcijas, kuras neizdevās izpildīt pārdošanas pasūtījuma izveidošanas laikā, un pārdošanas pasūtījumi, kurus neizdevās izpildīt rēķina izrakstīšanas laikā.
- Lietotājam ir pārredzams veids, kā transakcijas tiek apkopotas.
- Lietotājam ir pilnīgi auditācijas pieraksti, no transakcijām līdz pārdošanas pasūtījumiem, līdz pārdošanas rēķiniem. Šie auditācijas pieraksti nebija pieejami mantotajā izrakstu grāmatošanas līdzeklī.
- Apkopotais XML fails ļauj vieglāk identificēt problēmas pārdošanas pasūtījuma izveides un rēķinu izrakstīšanas laikā.

### <a name="journal-vouchers"></a>Žurnālu dokumenti

Poga **Žurnālu dokumenti** izraksta grupā **Detalizēta informācija par izpildi** rāda visas dažādās dokumentu transakcijas, kas ir izveidotas kādam izrakstam un kas ir saistītas ar atlaidēm, ieņēmumu/izdevumu kontiem, dāvanu kartēm un citiem iestatījumiem.

Pašlaik šos datus programma rāda tikai iegrāmatotiem izrakstiem.

### <a name="payment-journals"></a>Maksājumu žurnāli

Poga **Maksājumu žurnāli** izraksta grupā **Detalizēta informācija par izpildi** rāda visus dažādos maksājumu žurnālus, kas ir izveidotu kādam izrakstam.

Pašlaik šos datus programma rāda tikai iegrāmatotiem izrakstiem.

## <a name="other-improvements"></a>Citi uzlabojumi

Izrakstu grāmatošanas līdzeklim ir veikti citi, aizmugursistēmas uzlabojumi, kurus lietotājs var redzēt. Daži piemēri:

- Apkopošana neņem vērā personāla, termināļa un maiņas elementus. Tā kā ir mazāk apkopošanas parametru, ir jāapstrādā mazāk pārdošanas pasūtījumu rindu.
- Strupsaķeres rašanās transakciju tabulās ir samazināta, ieviešot papildu paplašinājuma tabulas un transakciju tabulās veicot ievietošanas operācijas, nevis atjaunināšanas operācijas.
- Darbināto pakešuzdevumu skaits ir parametrizēts un ierobežots. Tāpēc šo skaitu var precīzi pielāgot noteiktajai klienta videi. Mantotajā izrakstu grāmatošanas līdzeklī vienlaikus tika izveidots neierobežots skaits pakešuzdevumu. Tādēļ pakešapstrādes serverī radās grūti pārvaldāmas kravas, pieskaitāmās izmaksas un sastrēgumi.
- Izraksti ir efektīvi sarindoti apstrādei, nosakot prioritātes izrakstiem, kam ir maksimālais transakciju skaits.
- Pakešveida procesi, piemēram, **Aprēķināt izrakstus partijā** un **Grāmatot izrakstus partijā**, tiek darbināti vienīgi pakešveida režīmā. Mantotajā izrakstu grāmatošanas līdzeklī lietotāji varēja izvēlēties pakešveida procesu palaišanu interaktīvā režīmā, kas ir viena pavediena operācija, atšķirībā no pakešveida procesiem, kas ir vairākpavedienu operācijas.
- Mantotajā izrakstu grāmatošanas līdzeklī jebkura pakešuzdevuma kļūme visam pakešuzdevumam izraisa kļūdas stāvokli. Uzlabotajā līdzeklī pakešuzdevumu kļūmes neizraisa kļūmes stāvokli visam pakešuzdevumam, ja pārējie pakešuzdevumi ir izpildīti sekmīgi. Jums ir jānovērtē grāmatošanas stāvoklis pakešuzdevuma izpildei, izmantojot lapu **Izraksti**, kurā ir redzami visi izraksti, kas netika grāmatoti kļūdu dēļ.
- Mantotajā izrakstu grāmatošanas līdzeklī pirmās izraksta kļūmes rašanās izraisa visa pakešveida procesa kļūmi. Atlikušie izraksti netiek apstrādāti. Uzlabotajā līdzeklī pakešveida process turpina apstrādāt visus izrakstus pat tad, ja dažu izrakstu apstrāde bija nesekmīga. Viena priekšrocība ir tāda, ka lietotāji var pārredzēt precīzu skaitu ar izrakstiem, kuros ir kļūdas. Tāpēc lietotāji neiestrēgst nepārtrauktā kļūdu labošanas un izraksta grāmatošanas procesā, līdz ir iegrāmatoti visi izraksti.

## <a name="general-guidance-about-the-statement-posting-process"></a>Vispārēji norādījumi par izrakstu grāmatošanas procesu

- Izrakstu grāmatošanas procesu ieteicams darbināt partijā, jo pakešapstrāde var izmantot pakešuzdevumu vairākpavedienu struktūru. Vairākpavedienu struktūra ir nepieciešama, lai apstrādātu milzīgos transakciju apjomus, kas parasti ir redzami izrakstu grāmatojumos.
- Iesakām ieslēgt negatīvus fiziskos krājumus krājumu modeļu grupai, lai jums būtu viengabalaina grāmatošanas funkcionalitāte. Dažos scenārijos negatīvos pārskatus var grāmatot tikai tad, ja pastāv negatīvi fiziskie krājumi. Piemēram, teorētiski, ja krājumos ir tikai viena vienība un šim krājumam ir notikusi pārdošanas transakcija un atgriešanas transakcija, tad transakciju vajadzētu varēt grāmatot pat tad, ja negatīvie krājumi nav ieslēgti. Taču, tā kā izraksta grāmatošanas procesā gan pārdošanas transakcija, gan atgriešanas transakcija tiek uzkrāta vienā debitora pasūtījumā, nav nekādas garantijas, ka pārdošanas rinda tiks grāmatota pirmā un ka atgriešanas rinda tiks grāmatota pēc tam. Tādēļ var rasties kļūdas. Ja šajā scenārijā ir ieslēgti negatīvi krājumi, transakciju grāmatošana netiek negatīvi ietekmēta un sistēma krājumus atspoguļo pareizi.
- Iesakām izmantot apkopošanu, kamēr aprēķināt un grāmatojat izrakstus. Tāpēc dažiem no apkopošanas parametriem ir ieteicami tālāk norādītie iestatījumi.

    - Pārejiet uz sadaļu **Retail un Commerce** \> **Headquarters iestatīšana** \> **Parametri** \> **Commerce parametri**. Pēc tam cilnē **Grāmatošana**, kopsavilkuma cilnē **Krājumu atjaunināšana**, laukā **Detalizācijas līmenis** atlasiet **Kopsavilkums**.
    - Pārejiet uz sadaļu **Retail un Commerce** \> **Headquarters iestatīšana** \> **Parametri** \> **Commerce parametri**. Pēc tam cilnē **Grāmatošana**, kopsavilkuma cilnē **Apkopošana** opciju **Dokumentu transakcijas** iestatiet uz **Jā**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
