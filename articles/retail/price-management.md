---
title: "Mazumtirdzniecības pārdošanas cenu pārvaldība"
description: "Šajā tēmā ir aprakstītas koncepcijas pārdošanas cenu izveidošanai un pārvaldīšanai programmatūrā Microsoft Dynamics 365 for Retail."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/27/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a7e6babe1bfec60ece4f84a77bbd838faf7274e0
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="retail-sales-price-management"></a>Mazumtirdzniecības pārdošanas cenu pārvaldība

[!INCLUDE [banner](includes/banner.md)]

Šajā tēmā ir sniegta informācija par procesu, ar kādu tiek izveidotas un pārvaldītas pārdošanas cenas programmatūrā Microsoft Dynamics 365 for Retail. Galvenā uzmanība ir pievērsta ar šo procesu saistītajiem jēdzieniem, kā arī dažādo konfigurācijas opciju ietekmei uz pārdošanas cenām.

## <a name="terminology"></a>Terminoloģija
Šajā tēmā tiek izmantoti tālāk norādītie termini.

| Termins | Definīcija, lietojums un piezīmes |
|---|---|
| Cena | Summa, par kādu viena preces vienība tiek pārdota pārdošanas punktā (Point of Sale — POS) debitoram vai pārdošanas pasūtījumā. Šajā tēmā termins *cena* vienmēr attiecas uz pārdošanas cenu, nevis uz krājumu cenu vai izmaksu cenu. |
| Pamatcena | Cena, kas izlaistai precei ir iestatīta laukā **Cena**. |
| Tirdzniecības līguma cena | Cena, kas precei vai variantam ir iestatīta, izmantojot tirdzniecības līgumu ar tipu **Cena (pārdošana)**. |
| Labākā cena | Ja precei var piemērot vairākas cenas vai atlaides — mazākā cenas summa un/vai lielākā atlaides summa, kura veido vismazāko iespējamo neto summu, kas debitoram ir jāmaksā. Šajā tēmā labākās cenas jēdziens vienmēr tiek saukts par “labāko cenu”. Šī labākā cena atšķiras no uzskaitījuma vērtības **Labākā cena**, kura tiek izmantota atlaižu vienlaicīguma režīmam, un šos jēdzienus nedrīkst sajaukt. |

## <a name="price-groups"></a>Cenu grupas
Cenu grupas veido Retail programmatūras cenu un atlaižu pārvaldības kodolu. Cenu grupas tiek izmantotas, lai cenas un atlaides piešķirtu mazumtirdzniecības entītijām (tas ir, kanāliem, katalogiem, piederībām un lojalitātes programmām). Tā kā cenu grupas tiek lietotas visām cenu noteikšanām un atlaidēm, ir ļoti svarīgi vēl pirms sākšanas izplānot veidu, kādā jūs tās izmantosiet.

Pati par sevi cenu grupa ir tikai nosaukums, apraksts un, ja vēlaties, cenu noteikšanas prioritāte. Galvenais, kas jāatceras saistībā ar cenu grupām — tās tiek izmantotas, lai pārvaldītu attiecības “daudzi pret daudziem”, kādas atlaidēm un cenām ir ar mazumtirdzniecības entītijām.

Nākamajā attēlā ir parādīts, kā cenu grupas tiek izmantotas. Ievērojiet, ka šajā attēlā “Cenu grupa” burtiski atrodas cenu noteikšanas un atlaižu pārvaldības centrā. Mazumtirdzniecības entītijas, kuras varat izmantot, lai pārvaldītu atšķirīgās cenas un atlaides, atrodas pa kreisi, un faktisko cenu un atlaižu ieraksti atrodas pa labi.

![Cenu grupas](./media/PriceGroups.png "Cenu grupas")

Kad veidojat cenu grupas, vienu un to pašu cenu grupu nevajadzētu izmantot vairākiem mazumtirdzniecības entītiju tipiem. Pretējā gadījumā varētu būt sarežģīti noteikt, kāpēc kādai transakcijai tiek piemērota noteikta cena vai atlaide.

Kā attēlā ir norādīts ar sarkano pārtraukto līniju, programmatūra Retail neatbalsta Microsoft Dynamics 365 pamata funkcionalitāti cenu grupai, kas ir iestatīta tieši debitoram. Taču šajā gadījumā jūs saņemat tikai pārdošanas cenas tirdzniecības līgumus. Ja vēlaties lietot no debitora atkarīgas cenas, ieteicams neiestatīt cenu grupas tieši debitoram. Tā vietā vajadzētu izmantot piederības.

Nākamajās sadaļās ir sniegta plašāka informācija par mazumtirdzniecības entītijām, kuras varat izmantot, lai iestatītu atšķirīgas cenas, kad tiek izmantotas cenu grupas. Cenu un atlaižu konfigurēšana visām šīm entītijām ir procedūra no divām darbībām. Šīs darbības var izpildīt jebkādā secībā. Taču loģiskā secība ir vispirms iestatīt cenu grupas entītijām, jo šī darbība, visticamāk, ir vienreizēja iestatīšana, kas tiek veikta ieviešanas laikā. Pēc tam, kad tiek veidotas cenas un atlaides, varat iestatīt cenu grupas šīm cenām un atlaidēm atsevišķi.

### <a name="channels"></a>Kanāli
Mazumtirdzniecības nozarē dažādos kanālos parasti ir dažādas cenas. Divi primārie faktori, kas ietekmē no kanāla atkarīgās cenas, ir izmaksas un vietējā tirgus apstākļi.

- **Izmaksas** — jo tālāk kanāls atrodas no preces avota, jo vairāk izmaksā šīs preces krājumu nodrošināšana. Piemēram, jaunai produkcijai ir ierobežots glabāšanas laiks un pastāv īpašas ražošanas prasības (piemēram, augšanas sezona). Ziemas laikā svaigas salātlapas, visticamāk, ziemeļu reģionos izmaksā vairāk nekā dienvidu reģionos. Ja iestatāt cenas kanāliem lielā ģeogrāfiskajā apgabalā, visticamāk, ir nepieciešams dažādiem kanāliem iestatīt dažādas cenas.
- **Vietējā tirgus apstākļi** — veikals, kura tiešais konkurents atrodas otrpus ielai, ir daudz jutīgāks pret cenas ietekmi nekā veikals, kuram tuvumā nav tiešo konkurentu.
 
### <a name="affiliations"></a>Piederības
Piederības vispārējā definīcija ir saikne vai saistība ar kādu grupu. Programmatūrā Retail piederības ir debitoru grupas. Piederības ir daudz elastīgāks instruments debitoru cenu noteikšanai un atlaidēm nekā Microsoft Dynamics 365 pamata debitoru grupu un atlaižu grupu jēdziens. Pirmkārt — piederību var izmantot gan cenām, gan atlaidēm, savukārt cenu noteikšanai, kas nav paredzēta mazumtirdzniecībai, ir atšķirīga grupa katram atlaižu un cenu tipam. Otrkārt — debitors var piederēt vairākām piederībām, bet var piederēt tikai vienai katra tipa cenu noteikšanas grupai tādai cenu noteikšanai, kas nav paredzēta mazumtirdzniecībai. Visbeidzot — lai gan piederības var iestatīt tā, lai tās būtu saistītas ar kādu debitoru, tas nav obligāti. Ekspromta piederību POS programmatūrā var izmantot anonīmiem debitoriem. Tipisks anonīmas piederības atlaides piemērs ir senioru vai studentu atlaide, kur debitors var saņemt atlaidi, vienkārši parādot grupas dalībnieka karti.

Lai gan piederības visbiežāk ir saistītas ar atlaidēm, tās varat izmantot arī, lai iestatītu atšķirīgu cenu noteikšanu. Piemēram, kad mazumtirgotājs kaut ko pārdod darbiniekam, tas varētu vēlēties mainīt pārdošanas cenu, nevis piemērot atlaidi papildus standarta cenai. Cits piemērs — mazumtirgotājs, kurš pārdod gan patērētājiem, gan biznesa klientiem, saviem biznesa klientiem varētu piedāvāt labākas cenas, ņemot vērā to pirkšanas apjomu. Piederības ļauj izmantot abus šos scenārijus.

### <a name="loyalty-programs"></a>Lojalitātes programmas
Saistībā ar cenām un atlaidēm lojalitātes programmas faktiski ir tikai piederības, kurām ir īpašs nosaukums. Gan cenas, gan atlaides var iestatīt lojalitātes programmai tieši tāpat, kā tās var iestatīt piederībai. Taču veids, kādā debitori saņem lojalitātes programmas cenu noteikšanu transakcijas vai pasūtījuma laikā, atšķiras no veida, kādā viņi saņem piederības cenu noteikšanu. Debitori var saņemt lojalitātes programmas cenu noteikšanu tikai tad, ja transakcijai tiek pievienota lojalitātes programmas karte. Kad transakcijai tiek pievienota lojalitātes programmas karte, tiek pievienota arī lojalitātes programma. Pēc tam lojalitātes programma ļauj izmantot īpašas cenas un atlaides.

Lojalitātes programmām var būt vairāki līmeņi, un dažādos līmeņos atlaides var atšķirties. Tādējādi mazumtirgotāji biežākiem debitoriem var piedāvāt lielāku atlīdzību bez nepieciešamības šos debitorus manuāli ievietot kādā īpašā grupā.

Lojalitātes programmas ir papildu funkcionalitāte, kas ir pieejama papildus cenām un atlaidēm. Taču no cenu noteikšanas un atlaižu viedokļa tās ir vienādas ar piederībām.

### <a name="catalogs"></a>Katalogi
Daži mazumtirgotāji izmanto fiziskus vai virtuālus katalogus, lai savas preces reklamētu un to cenu noteiktu īpaši mērķētām debitoru grupām. Daļu no viņu biznesa modeļa veido mērķēts mārketings, izmantojot katalogu, tāpēc šie mazumtirgotāji dažādos katalogos var iestatīt dažādas cenas. Microsoft Dynamics 365 atbalsta šo iespēju, ļaujot jums definēt no kataloga atkarīgas atlaides un cenas tieši tāpat, kā varat definēt no kanāla atkarīgas vai no piederības atkarīgas atlaides. Kad rediģējat kādu katalogu, ar šo katalogu varat saistīt cenu grupas tieši tāpat, kā tās varat saistīt ar kanālu, piederību vai lojalitātes programmu.

### <a name="best-practices-for-price-groups"></a>Labākās prakses cenu grupām
Nelietojiet cenu grupu vairākiem mazumtirdzniecības entītiju tipiem. Tā vietā izmantojiet vienu cenu grupu kopu kanāliem, citu cenu kopu — piederībām vai lojalitātes programmām, un tamlīdzīgi. Cenu grupas nosaukumā varat izmantot prefiksu vai sufiksu, lai vizuāli grupētu dažādos izmantotos cenu grupu tipus.

Centieties neiestatīt cenu grupas tieši debitoram. Tā vietā izmantojiet piederību. Šādi visus cenu un atlaižu tipus varat piešķirt debitoriem, nevis tikai pārdošanas cenas tirdzniecības līgumiem.

## <a name="pricing-priority"></a>Cenu noteikšanas prioritāte
Pati par sevi cenu noteikšanas prioritāte ir tikai skaitlis un apraksts. Cenu noteikšanas prioritātes var lietot cenu grupām, vai tās var lietot tieši atlaidēm. Kad tiek izmantotas cenu noteikšanas prioritātes, tās ļauj mazumtirgotājam ignorēt labākās cenas principu, kontrolējot secību, kādā cenas un atlaides tiek lietotas precēm. Lielāks cenu noteikšanas prioritātes skaitlis tiek novērtēts pirms mazāka cenu noteikšanas prioritātes skaitļa. Turklāt, ja pie jebkura prioritātes skaitļa tiek atrasta kāda cena vai atlaide, tiek ignorētas visas cenas un atlaides, kam ir mazāks prioritātes skaitlis.

Šī cena un atlaide var tikt iegūtas no divām dažādām cenu noteikšanas prioritātēm, jo cenu noteikšanas prioritātes cenām un atlaidēm tiek lietotas neatkarīgi.

Lai izmantotu cenu noteikšanas prioritāti cenām, cenu noteikšanas prioritāte ir jāpiešķir kādai cenu grupai un pēc tam ir jāizveido pārdošanas cenas tirdzniecības līgums šai cenu grupai.

Cenu noteikšanas prioritātes līdzeklis tika ieviests, lai atbalstītu scenāriju, kur mazumtirgotājs vēlas piemērot augstākas cenas kādā noteiktā veikalu kopā. Piemēram, mazumtirgotājs ir definējis reģionālās cenas Amerikas Savienoto Valstu austrumkrastam, bet vēlas norādīt augstākas cenas dažām precēm Ņujorkas veikalos, jo šajā pilsētā preču tirgošana izmaksā vairāk un/vai vietējā tirgū var izmantot augstāku cenu.

Kā jau aprakstīts šīs tēmas sadaļā “Labākā cena”, mazumtirdzniecības cenu noteikšanas programma parasti atlasa mazāko no abām cenām. Tāpēc mazumtirgotājam parasti tiek liegts izmantot augstāko no abām cenām tādā veikalā, kas ietilpst gan cenu grupā Austrumkrasts, gan cenu grupā Ņujorka. Lai atrisinātu šo problēmu pirms cenu noteikšanas prioritātes līdzekļa ieviešanas, mazumtirgotājam bija nepieciešams definēt cenas katrai precei divas reizes un nedrīkstēja piešķirt abas cenu grupas. Vai arī šim mazumtirgotājam bija jāizveido papildu cenu grupas, lai preces, kurām ir augstākas cenas, nošķirtu no precēm, kurām ir parastās, t.i., zemākās cenas.

Taču cenu noteikšanas prioritātes līdzeklis ļauj mazumtirgotājam izveidot cenu noteikšanas prioritāti veikala cenām, kas ir augstāka par cenu noteikšanas prioritāti reģionālajām cenām. Vai arī mazumtirgotājs var izveidot cenu noteikšanas prioritāti tikai veikala cenām, bet reģionālajām cenām atstāt noklusējuma cenu noteikšanas prioritāti, kas ir 0 (nulle). Abi iestatījumi palīdz nodrošināt, ka veikala cenas vienmēr tiek izmantotas pirms reģionālajām cenām.

### <a name="pricing-priority-example"></a>Cenu noteikšanas prioritātes piemērs
Aplūkosim piemēru, kur veikala cenas ignorē pārējās cenas.

Valsts līmeņa mazumtirgotājs vairumu cenu iestata atkarībā no reģiona, un tam ir četri reģioni: Ziemeļaustrumi, Dienvidaustrumi, Vidējie rietumi un Rietumi. Tas ir noteicis vairākus augstu izmaksu tirgus, kuros var izmantot augstākas cenas. Šie tirgi ir Ņujorkas pilsētā (New York City — NYC), Čikāgā un Sanfrancisko līča apgabalā.

Šajā piemērā mēs detalizēti aplūkojam Ziemeļaustrumu reģionu. 1. veikals atrodas Bostonā, un 2. veikals atrodas Manhetenā. Bostonas veikalam ar kanālu ir saistītas divas cenu grupas: Ziemeļaustrumi un 1. veikals. Manhetenas veikalam ar kanālu ir saistītas trīs cenu grupas: Ziemeļaustrumi, NYC un 2. veikals.

Mazumtirgotājs iestata divas cenu noteikšanas prioritātes: Augstām izmaksām prioritātes skaitlis ir 5, un Veikala cenām prioritātes skaitlis ir 10. (Atcerieties — pēc noklusējuma cenu noteikšanas prioritāte ir 0 \[nulle\], un cena vai atlaide, kurai ir lielāks prioritātes skaitlis, tiek izmantota pirms cenas vai atlaides, kurai ir mazāks prioritātes skaitlis.) Ziemeļaustrumu cenu grupas cenu noteikšanas prioritātei tiek atstāta noklusējuma vērtība **0** (nulle). NYC cenu grupai cenu noteikšanas prioritāte ir iestatīta uz **5**, jo Ņujorkas pilsēta ir augstu izmaksu tirgus. 1. veikala un 2. veikala cenu grupām cenu noteikšanas prioritāte ir iestatīta uz **10**.

Divas mazumtirgotāja pārdotās preces ir 1. prece, parasts T-krekls, un 2. prece, īpaša zīmola moderni džinsi.

| Prece | Ziemeļaustrumu cena | NYC cena | Veikala cena |
|---|---|---|---|
| T-krekls | 15 USD | Nav iestatīts | Nav iestatīts |
| Moderni džinsi | 50 USD | 70 USD | Nav iestatīts |

T-krekls tiek pārdots par to pašu cenu (t.i., 15 USD) gan Bostonas, gan Manhetenas veikalos, jo tikai viena cena ir iestatīta Ziemeļaustrumu cenu grupā, kura ir saistīta ar abiem kanāliem. Modernie džinsi Bostonas veikalā tiek pārdoti par 50 USD, jo tā ir vienīgā cena, kas ir pieejama šajā veikalā. Taču Manhetenas veikalā ir pieejamas divas cenas: 50 USD un 70 USD. Tā kā NYC cenu grupas cenu noteikšanas prioritātes skaitlis 5 ir lielāks nekā Zemeļaustrumu cenu grupas cenu noteikšanas prioritātes skaitlis 0 (nulle), šī cena POS sistēmā tiks aktivizēta kā 70 USD.

> [!NOTE]
> Katrai cenu noteikšanas prioritātei ir nepieciešama pilnīga mazumtirdzniecības cenu noteikšanas programmas loģikas izpildīšana. Tāpēc, lai palīdzētu uzturēt cenu un atlaižu aprēķina veiktspēju, cenu noteikšanas prioritātes vajadzētu izmantot ar mēru.

## <a name="types-of-prices"></a>Cenu tipi
Programmatūrā Microsoft Dynamics 365 preces cenu varat iestatīt trīs tālāk norādītajās vietās.

- Tieši precei (pamatcena)
- Pārdošanas cenas tirdzniecības līgumā
- Cenas korekcijā

Pamatcena un tirdzniecības līguma cena ir daļa no pamata programmatūras Microsoft Dynamics 365, un tās ir pieejamas pat tad, ja nelietojat programmatūru Retail. Cenas korekcijas funkcionalitāte ir pieejama tikai programmatūrā Retail. Nākamā sadaļā ir sniegta papildu informācija par katru no šīm opcijām cenu iestatīšanai, kā arī paskaidrots, kā šīs opcijas darbojas kopā.

## <a name="setting-prices"></a>Cenu iestatīšana
### <a name="base-price"></a>Pamatcena
Vienkāršākā vieta, kur precei iestatīt cenu, ir tieši attiecīgajai precei. Vērtība, kuru jūs iestatāt tieši precei, bieži tiek saukta par šīs preces Pamatcenu. Pamatcena tiek iestatīta laukā **Cena**, lapas **Informācija par izlaistajām precēm** cilnē **Pārdot**. Jūsu ievadītā vērtība ir uzņēmuma valūtā. Pēc noklusējuma šī cena ir par 1 mērvienību (Mērvienība), kas ir iestatīta laukā **Vienība**, cilnē **Pārdot**. Faktiskā cena par vienu preces vienību ir atkarīga no Mērvienības, cenas daudzuma un valūtas.

Ja kādai precei ir vienāda cena neatkarīgi no pircēja, pamatcena nodrošina visefektīvāko veidu šīs preces cenas pārvaldīšanai. Pat ja preču iestatīšanai izmantojat tirdzniecības līgumus, precei varat iestatīt arī pamatcenu. Pēc tam, ja neizmantojat tirdzniecības līgumu **Visi**, jums ir regresa cena, kas tiek izmantota, kad nav piemērojams neviens tirdzniecības līgums.

Ja kāda mazumtirdzniecības kanāla valūta atšķiras no uzņēmuma valūtas, pamatcena attiecīgajā mazumtirdzniecības kanālā tiek noteikta, izmantojot valūtas konvertēšanu cenai, kas ir iestatīta šai precei.

Lai gan cenas vienība nav izplatīts mazumtirdzniecības scenārijs, mazumtirdzniecības cenu noteikšanas programma to atbalsta. Ja cenas vienība ir iestatīta uz vērtību, kas nav **0** (nulle), vienības cena tiek aprēķināta pēc formulas Cena ÷ Cenas vienība. Piemēram, ja kādas preces cena ir 10,00 USD un cenas vienība ir 50, cena par daudzumu 1 ir 0,20 USD (= 10,00 USD ÷ 50).

### <a name="sales-price-trade-agreement"></a>Pārdošanas cenas tirdzniecības līgums
Izmantojot tirdzniecības līgumu žurnālu, varat izveidot pārdošanas cenas tirdzniecības līgumus katrai precei. Programmatūrā Microsoft Dynamics 365 ir trīs debitoru tvērumi attiecībā uz pārdošanas cenas tirdzniecības līgumiem: **Tabula**, **Grupa** un **Visi**. Debitoru tvērums nosaka debitorus, uz kuriem attiecas noteikts pārdošanas cenas tirdzniecības līgums.

Pārdošanas cenas tirdzniecības līgums **Tabula** ir paredzēts atsevišķam debitoram, kas tiek iestatīts tieši pārdošanas līgumam. Šis scenārijs nav tipiskais mazumtirdzniecības scenārijs “no uzņēmuma patērētājam” (Business-to-Consumer — B2C). Taču, ja tāds rodas, cenas noteikšanai mazumtirdzniecības cenu noteikšanas programma izmanto tirdzniecības līgumus **Tabula**. 

Pārdošanas cenas tirdzniecības līgums **Grupa** ir tāds tips, kas visbiežāk tiek izmantots ar Retail funkcionalitāti. Ārpus Retail pārdošanas cenas tirdzniecības līgumi **Grupa** ir paredzēti vienkāršai debitoru grupai. Taču programmatūrā Retail debitoru grupas jēdziens ir paplašināts, lai tas būtu vispārīgāka mazumtirdzniecības cenu grupa. Cenu grupu var saistīt ar mazumtirdzniecības kanālu, piederību, lojalitātes programmu vai katalogu. Detalizētu informāciju par cenu grupām skatiet agrākā šīs tēmas sadaļā “Cenu grupas”.

> [!NOTE]
> Tirdzniecības līguma cena vienmēr tiek izmantota pirms pamatcenas.

### <a name="price-adjustment"></a>Cenas korekcija
Kā jau nosaukums norāda, cenu korekcija tiek izmantota, lai modificētu cenu, kas bija iestatīta tieši precei vai bija iestatīta, izmantojot tirdzniecības līgumu. Cenas korekciju var izmantot tikai cenas pazemināšanai, bet ne tās paaugstināšanai. Cenas korekcija ir ieteicamais veids, kā mazumtirgotājiem izveidot, izsekot un pārvaldīt savu preču nocenošanu laika gaitā. 

Pastāv trīs tipu cenas korekcijas: atņemts procentuālais daudzums, atņemta summa un cena. Cenas korekcijas tips, kurā tiek atņemts procentuālais daudzums vai atņemta summa, vienmēr tiek lietots pārdošanas transakcijām. Taču cenas korekcija, kuras tips ir cena, tiek lietota tikai tad, ja koriģētā cena ir mazāka par cenu, kura bija iestatīta, izmantojot pamatcenu vai tirdzniecības līguma cenu. Tādēļ, ja ar cenas korekciju iestatītā cena ir lielāka par nekoriģēto cenu, cenas korekcija netiek izmantota.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Cenas noteikšana precei transakcijā

Transakcijā iesaistītās cenas un atlaides aprēķināšanai tiek izmantots debitoram vislabākās cenas atrašanas princips. Saskaņā ar šo principu gadījumā, ja tiek atrastas vairākas cenas, tiek izmantota zemākā cena. Turklāt tiek izmantota atlaižu kombinācija, kas visai transakcijai veido vislielāko atlaides summu. Noteiktos gadījumos ir jāizmanto mazāka atlaide vienai precei, lai pārējām transakcijā iesaistītajām precēm varētu lietot papildu atlaides.

Debitoram labākās cenas atrašanas principam vienīgais izņēmums ir opcija komplektēt lētākās atlaides. Šī opcija ļauj izmantot lētākās atlaides, kas nāk par labu mazumtirgotājam, kad preces tiek atlasītas un grupētas. Tādēļ gadījumos, kad transakcijā ietilpst vairāk preču, nekā ir nepieciešams, lai kvalificētos lētākajai atlaidei, mazumtirdzniecības cenu noteikšanas programma atlasa preces, kas debitoram veido vismazāko iespējamo atlaides summu.

Mazumtirdzniecības cenu noteikšanas programma attiecībā uz katru preci atgriež trīs cenas: pamatcenu, tirdzniecības līguma cenu un aktīvo cenu.

Pamatcena ir tikai preces rekvizīts, un tā visiem un visur ir vienāda. 

Ja pārdošanas cenas tirdzniecības līgumā opcija **Atrast nākamo** ir iestatīta uz **Jā**, kā tirdzniecības līguma cena tiek izmantota piemērojamajiem pārdošanas cenas tirdzniecības līgumiem viszemākā atrastā cena. Tirdzniecības līgumi ir atrodami, izmantojot cenu grupas vai konta kodu **VISI**. Tirdzniecības līgumus var arī piešķirt tieši debitoram. Ja opcija **Atrast nākamo** ir iestatīta uz **Nē**, tiek lietota pirmā atrastā tirdzniecības līguma cena. Ja netiek atrasts neviens pārdošanas cenas tirdzniecības līgums, tad tirdzniecības līguma cena tiek iestatīta vienāda ar pamatcenu.

Aktīvā cena tiek aprēķināta, tirdzniecības līguma cenai piemērojot vislielāko cenas korekciju, kas attiecas uz šo preci. Ja netiek atrasta neviena cenas korekcija vai ja aprēķinātā aktīva cena ir lielāka par tirdzniecības līguma cenu, tad aktīvā cena tiek iestatīta vienāda ar tirdzniecības līguma cenu. Iegaumējiet, ka nevar paaugstināt preces cenu, izmantojot cenas korekciju. Piemērojamās cenas korekcijas ir atrodamas, tikai izmantojot cenu grupas, kas ir piešķirtas kanālam, katalogam, piederībai vai lojalitātes programmai.

## <a name="category-price-rules"></a>Kategorijas cenu kārtulas
Kategorijas cenu kārtulu līdzeklis programmatūrā Retail jums nodrošina vienkāršu veidu, kā izveidot jaunus tirdzniecības līgumus visām precēm kādā kategorijā. Šis līdzeklis arī ļauj automātiski atrast esošos tirdzniecības līgumus attiecīgajā kategorijā esošajām precēm un izbeigt tos.

Kad atlasāt opciju izbeigt esošus tirdzniecības līgumus, sistēma izveido jaunu tirdzniecības līgumu žurnālu precēm attiecīgajā kategorijā, kam ir aktīvs tirdzniecības līgums. Taču šo žurnālu ir nepieciešams manuāli grāmatot. Turklāt kategorijas cenu kārtulas varat atrast esošos tirdzniecības līgumus tikai tad, ja izmantojat to pašu cenu kārtulu (tas ir, ja izveidojat jaunu cenu kārtulu, kas izmanto to pašu kategoriju, kas tika izmantota iepriekš). Ja neizmantojat to pašu cenu kārtulu, esošie tirdzniecības līgumi netiek izbeigti.

Cenas var paaugstināt vai pazemināt, izmantojot kategorijas cenas kārtulu laukus **Cenas kārtula** un **Cenas bāze**.

- Laukā **Cenas kārtula** atlasiet, kādu cenas izmaiņas tipu vēlaties izmantot.

    - **Uzcenojums** — pārdošanas cenas aprēķināšanai tiek izmantots procentuāls daudzums no cenas bāzes. Piemēram, precei, kas maksā 10,00 un ko pārdod par 15,00, uzcenojums ir 50 procenti.
    - **Peļņa** — peļņas summas aprēķināšanai tiek izmantots procentuāls daudzums no pārdošanas cenas. Piemēram, precei, kas maksā 10,00 un ko pārdod par 15,00, peļņa ir 33,3 procenti.
    - **Fiksēta summa** — pārdošanas cenas aprēķināšanai tiek izmantota summa, kas tiek pieskaitīta cenas bāzei. Piemēram, precei, kas maksā 10,00 un ko pārdod par 15,00, fiksēta summa ir 5,00.

- Laukā **Cenas bāze** atlasiet modificējamās cenas tipu.

    - **Bāzes izmaksas** — summa, ko mazumtirgotājs samaksāja piegādātājam.
    - **Bāzes cena** — pārdošanas cena pirms tirdzniecības līgumu un cenas korekciju piemērošanas.
    - **Pašreizējā cena** — pārdošanas cena pēc tirdzniecības līgumu un cenas korekciju piemērošanas.

Lai ērti atjauninātu cenas dažādām precēm no dažādām preču kategorijām, kopā ar kategorijas cenu kārtulām varat izmantot papildu preču kategorijas.

## <a name="best-practices"></a>Labākās prakses
Sistēma Microsoft SQL Server Express bieži tiek izmantota kanālu datu bāzēm izmaksu dēļ (tā ir bezmaksas). Paturiet prātā, ka sistēmai SQL Server Express pastāv aparatūras ierobežojumi un datu apjoma ierobežojumi. Ja neplānojat pareizi, drīz vien varat sasniegt SQL Server Express datu apjoma ierobežojumu. Šis apsvērums attiecas ne tikai uz cenu noteikšanu, bet arī uz citām preču jomām. Tālāk ir norādītas dažas labākās prakses, kas jums varētu noderēt, lai samazinātu savu datu apjomu.

- Ja izmantojat tirdzniecības līgumus un jūsu cenas mainās, jums vajadzētu izbeigt vecos tirdzniecības līgumus, iestatot beigu datumu. Laika gaitā šī metode palīdz samazināt tirdzniecības līgumus skaitu, kas tiek glabāts kanāla datu bāzēs. Tā palīdz arī samazināt datu apjomu, ar kādu ir jāstrādā cenas aprēķināšanas algoritmam.
- Ja jūsu cenas atšķiras atkarībā no preces varianta, apsveriet iespēju izmantot preces pamatcenu kā visbiežākā varianta cenu. Pēc tam izmantojiet tirdzniecības līgumus tikai variantu cenām, kas ir izņēmumi. Šī metode palīdz samazināt tirdzniecības līgumu ierakstu skaitu. Tā kā datus importēt sistēmā Microsoft Dynamics 365 ir tik vienkārši, jums varētu būt kārdinājums importēt tirdzniecības līgumu ikvienam katras preces variantam. Taču šī prakse var radīt daudzus tirdzniecības līgumus, kuriem ir tāda pati vērtība. Tādēļ tas var lieki palielināt datus apjomu.
- Programmatūra Retail no varianta atkarīgās cenas apstrādā secībā no konkrētākajām līdz vispārīgākajām. Ja kāda preces dimensija neietekmē cenu, nav nepieciešams tai definēt tirdzniecības līgumus. Piemēram, prece ir pieejama trīs krāsās un četros izmēros, bet cena mainās tikai atkarībā no izmēra. Ja definējat tirdzniecības līgumu katram variantam, jūs izveidojat 12 ierakstus. Tā vietā varat definēt tirdzniecības līgumu tikai katram izmēram un krāsu dimensiju varat atstāt tukšu. Tādā gadījumā jūs izveidojat tikai četrus ierakstus.

    Vai arī — ja ne katra dimensijas vērtība izveido atšķirīgu cenu — varat definēt vienu tirdzniecības līgumu preces šablonam un visas preces dimensijas atstāt tukšas. Pēc tam definējiet atsevišķu tirdzniecības līgumu tikai katrai dimensijas vērtībai, kas veido atšķirīgu cenu. Piemēram, ja XXL izmēram ir augstāka cena, bet visiem pārējiem izmēriem ir vienāda cena, jums ir nepieciešami tikai divi tirdzniecības līgumi: viens līgums preces šablonam un viens — XXL izmēram.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Cenas, kas ietver nodokļus, salīdzinājumā ar cenām, kas neietver nodokļus
Kad iestatāt pārdošanas cenas programmatūrā Microsoft Dynamics 365, jūs nenorādāt, vai jūsu iestatītā cenas vērtība ietver vai neietver nodokļus. Šī vērtība ir tikai cena. Taču iestatījums **Cena ietver PVN** mazumtirdzniecības kanālos jums ļauj konfigurēt mazumtirdzniecības kanālus, lai tie cenās ietvertu vai neietvertu nodokļus. Šis iestatījums tiek iestatīts kanālam, un to var mainīt pat vienā uzņēmumā.

Ja strādājat gan ar ietvertu, gan neietvertu nodokļu tipiem, ir ļoti svarīgi cenas iestatīt pareizi, jo kopējā summa, kas debitoram ir jāmaksā, mainās atkarībā no tā, vai attiecīgajam kanālam ir mainīts iestatījums **Cena ietver PVN**.

### <a name="effect-of-the-price-includes-sales-tax-setting-on-financial-postings"></a>Iestatījuma “Cena ietver PVN” ietekme uz finanšu grāmatojumiem
Iestatījums **Cena ietver PVN** ietekmē visas summas, kas virsgrāmatā tiek grāmatotas ieņēmumu un atlaižu kontiem. Nākamajā piemērā ir parādīts, kā šis iestatījums ietekmē finanšu grāmatojumus.

Šajā piemērā ir aplūkoti tikai pārdošanas grāmatojumi, jo iestatījums **Cena ietver PVN** neietekmē krājumu izmaksu grāmatojumus.

#### <a name="example"></a>Piemērs
Šajā piemērā atlaižu summas ir konfigurētas tā, lai tās tiktu grāmatotas atsevišķi no ieņēmumiem.

Jūs pārdodat 100 USD preces, kuras nodokļa likme ir 10 procenti, un tiek piemērota 5 procentu atlaide. Tiek izmantoti tālāk uzskaitītie konti no USRT demonstrācijas datiem.

- **Ieņēmumi:** 401100
- **Atlaide:** 403200
- **Nodoklis:** 202100

**1. gadījums: Neietver nodokli (sauktu arī par PVN)**

- **Ieņēmumi:** 100 USD
- **Atlaide:** 5 USD
- **Nodoklis:** 9,5 USD (= 10 procenti no 95 USD)

**2. gadījums: Ietver nodokli (sauktu arī par pievienotās vērtības nodokli \[PVN\])**

- **Ieņēmumi:** 90 USD
- **Atlaide:** 4,5 USD (= 5 procenti no 90 USD)
- **Nodoklis:** 10 USD

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Atšķirības starp mazumtirdzniecības cenu noteikšanu un cenu noteikšanu, kas nav paredzēta mazumtirdzniecībai
Tiek izmantota viena un tā pati cenu noteikšanas programma, lai aprēķinātu mazumtirdzniecības cenas visos kanālos: Zvanu centrā, Mazumtirdzniecības veikalā un Tiešsaistes veikalos. Tas palīdz iespējojot vienotos komercijas scenārijus. 

Mazumtirdzniecības cenu noteikšanu ir paredzēta darbam ar mazumtirdzniecības entītijām, nevis ar entītijām, kas nav mazumtirdzniecības entītijas. Tas ir — tā ir paredzēta cenu noteikšanai pēc veikala, nevis pēc noliktavas.

Mazumtirdzniecības cenu noteikšanas programma neatbalsta tālāk uzskaitītos cenu noteikšanas līdzekļus.

- Cenas noteikšana, izmantojot noliktavas dimensijas Novietojums un Noliktava.
- Atribūtam atbilstoša cenas noteikšana
- Kreditora atlaides pāreja

Turklāt **tikai** mazumtirdzniecības cenu noteikšanas programma atbalsta tālāk uzskaitītos cenu noteikšanas līdzekļus.

- Cena ir balstīta uz preču dimensijām, secībā no konkrētākā varianta cenas līdz vispārīgākajai varianta cenai, līdz preces šablona cenai. Cena, kas ir iestatīta, izmantojot divas preces dimensijas (piemēram, Krāsa un Lielums), tiek izmantota pirms cenas, kas ir iestatīta, izmantojot tikai vienu preces dimensiju (piemēram, Lielums).
- Cenu noteikšanas un atlaižu kontrolēšanai var izmantot tās pašas cenu grupas.
