---
title: Pārvaldīt reisus
description: Šajā tēmā ir aprakstīts, kā strādāt ar reisiem. Parasti reiss ir kuģis. Tomēr atkarībā no jūsu prakses un procedūrām var pārstāvēt kreditoru, pirkšanas pasūtījumu vai kādu citu krājumu, kas ir noderīgs jūsu organizācijai.
author: sherry-zheng
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 953677a0d7ebe3343b888fdff2867334ef69d861d85a9145aa003177617434d6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757834"
---
# <a name="manage-voyages"></a>Pārvaldīt reisus

[!include [banner](../../includes/banner.md)]

Parasti reiss ir kuģis. Tomēr atkarībā no jūsu prakses un procedūrām var pārstāvēt kreditoru, pirkšanas pasūtījumu vai kādu citu krājumu, kas ir noderīgs jūsu organizācijai.

Lapa **Visi reisi** sniedz informāciju par reisiem, piegādes un izmaksu informāciju un informāciju par krājumiem, pirkšanas pasūtījumiem un pārsūtīšanas pasūtījumiem. Lai atvērtu lapu **Visi reisi**, dodieties uz sadaļu **Kopējās izmaksas \> Reisi \> Visi reisi**. Šajā lapā ir parādīts visu pašreizējo reisu saraksts. Jūs varat izmantot pogas Darbību rūtī, lai izveidotu, dzēstu un darbotos ar reisiem. Sarakstā atlasiet jebkuru reisu, lai skatītu detalizētu informāciju par to.

> [!NOTE]
> Nosūtīšanas konteineri un folio ir saistīti ar reisu. Pirkšanas rindas ir saistītas ar nosūtīšanas konteineru. Ja transportēšanas konteineri un konteineri ir izslēgti, tos var arī saistīt ar reisu. Turklāt šeit ievadītās izmaksas tiek pievienotas visām pievienotajām pirkšanas rindām.

## <a name="action-pane"></a>Darbības rūts

Darbību rūts lapā **Reisi** nodrošina pogas, kas ļauj strādāt ar atlasīto reisu. Katra poga veic vienu darbību. Darbību rūtī ir ietvertas arī cilnes, katra no tām savukārt sniedz saistītu pogu kopu. Izņemot gadījumus, kad atzīmēts, visas pogas un cilnes ir pieejamas gan **Visu reisu** lapas sarakstā, gan atsevišķa atlasītā reisa detalizētajā skatā.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Pogas, kas parādās tieši darbību rūtī

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas tieši darbību rūtī.

| Poga | Apraksts |
|---|---|
| Jauna | Reisa izveide. <!-- KFM: Link to scenario --> |
| Delete | Dzēst šo reisu. Var dzēst tikai reisus, kuru reisa statuss ir *Apstiprināts*. Reisam atstājot ostu un apstrādājot tranzīta preces, to vairs nevar dzēst. |
| Reisa redaktors | Atveriet lapu **Reisu redaktors**, kur var pievienot vai noņemt reisa pirkšanas rindas, izveidot jaunus konteinerus un modificēt detalizētu informāciju par pašu reisu. |
| Reisa izmaksas | Atvērt lapu **Reisu izmaksas**, kurā var skatīt un pievienot reisu izmaksas visām reisa precēm. Kad reisu izmaksas tiek manuāli pievienotas reisam, tās automātiski tiek pievienotas **Izmaksu pieprasījuma** lapai un izmaksātas katrai labākās preces atbilstoši metodei, kas ir norādīta lapā **Reisu izmaksas**. |

### <a name="buttons-on-the-voyage-tab"></a>Pogas cilnē Reisi

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas darbību rūts cilnē **Reisi**. Šī cilne ir pieejama tikai tad, kad strādājat lapas **Visi reisi** saraksta skatā.

| Poga | Apraksts |
|---|---|
| Nosūtīšanas konteiners | Atveriet lapu ar visu to sūtījumu konteineru rādījumiem, kas ir saistīti ar atlasīto reisu. Var būt viens konteiners vai vairāki konteineri. |
| Folio | Atveriet lapu ar visiem folio, kas ir saistīti ar atlasīto reisu. Var būt viens folio vai vairāki folio. |

### <a name="buttons-on-the-manage-tab"></a>Pogas cilnē Pārvaldīt

Šajā tabulā ir aprakstītas darbības, kas ir pieejamas darbību rūts cilnē **Pārvaldīt**.

| Poga | Apraksts |
|---|---|
| Saņemtie dokumenti | Atjauniniet reisu, lai opcija **Saņemtie dokumenti** ir iestatīta uz *Jā*. Šo pogu var izmantot, lai bloķētu krājumu un/vai pirkšanas rindu tā, ka to vairs nevar atjaunināt. |
| Tranzītā | Atjauniniet **Reisa statusa** lauku uz tranzīta statusu, kas ir izveidots lapā **[Kopējo izmaksu parametri](landed-cost-parameters.md)**. Šim procesam vairs nav loģikas. Reisu var arī automātiski atjaunināt uz tranzīta statusu, pamatojoties uz [Izsekošanas kontroles centra iestatījumiem](delivery-information-setup.md).
| Sagatavots izmaksu aprēķināšanai | Atjauniniet **Reisa statusa** lauku uz gatavo izmaksu piemērošanas statusu, kas ir izveidots lapā **[Kopējo izmaksu parametri](landed-cost-parameters.md)**. Reisa izmaksas var tikt izmaksātas, kad ir apstrādāti visi rēķini (gan krājumu rēķini, gan reisa izmaksu rēķini) un preces ir saņemtas. Ja ar reisu saistītās novērtētās izmaksas nav aprēķinātas, mēģinot apstrādāt reisa izmaksas, rodas kļūda. |
| Aprēķinātās izmaksas | Iztīriet ikvienu izmaksu aprēķināšanas veidu pēc rēķina eksistē visiem pirkšanas pasūtījumiem un reisa izmaksām. Atlasot šo pogu, parādās dialoglodziņš **Reisa atjaunināšana - izmaksāts**. Tur var atlasīt grāmatošanai standarta finanšu datumā vai norādīt grāmatošanas datumu un pēc tam palaist darbību. Varat palaist darbību neierobežotu reižu skaitu. Var izmantot arī dialoglodziņu **Reisa atjaunināšana – Izmaksas**, lai izveidotu grafiku darbības palaišanai kā periodisku uzdevumu (pakešuzdevumu). Ieteicams regulāri palaist darbību, iestatot to kā pakešuzdevumu. |
| Grāmatot saņemšanas sarakstu | Grāmatojiet saņemšanas sarakstu visām pirkšanas pasūtījuma rindām reisā. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns saņemšanas saraksta grāmatošanas dialoglodziņš, kas jāizmanto katrā juridiskajā personā. |
| Grāmatot produktu ieejas plūsmu | Grāmatojiet saņemto preču pavadzīmi visām pirkšanas pasūtījuma rindām reisā. Produktu ieejas plūsmas process pirkšanas pasūtījuma rindām, kas ir saistītas ar reisu, tiks izmantots tikai tad, ja preces **netiks** pārdotas tranzītā. Ja preces tiks apstrādātas tranzītā, mēģinot grāmatot produktu ieejas plūsmu pirkšanas pasūtījuma rindai, tiek parādīta kļūda. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns piegādes saraksta grāmatošanas dialoglodziņš. |
| Grāmatot rēķinu | Grāmatojiet rēķinu visām pirkšanas pasūtījuma rindām reisā. Ja reisa preces tiks veiktas tranzītā caur tranzītapstrādes precēm, pirms saņemšanas procesa beigām tiks izrakstīts rēķins pirkšanas pasūtījuma rindām. Kad sākotnējais pirkšanas pasūtījums ir iekļauts rēķinā, tiks izveidoti ar oriģinālajām pirkšanas pasūtījuma rindām saistītie preču tranzīta pasūtījumi. Šos pasūtījumus pēc tam var saņemt noliktava. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns rēķina grāmatošanas dialoglodziņš. |
| Nosūtīšanas pārsūtīšanas pasūtījums | Grāmatojiet pārsūtīšanas pasūtījuma reisu visām pirkšanas pasūtījuma rindām reisā. Kad šī poga ir atlasīta, atjaunināšanai būs pieejami tikai pārsūtīšanas pasūtījumi. |
| Saņemt pārsūtīšanas pasūtījumu | Grāmatojiet pārsūtīšanas pasūtījuma reisu visām pirkšanas pasūtījuma rindām reisā. |
| Saņemtās tranzītpreces | Saņemt visas pasūtījuma rindas, kas ir tranzītā reisā. Šī poga ir viena no trim opcijām, kas ir pieejamas preču saņemšanai tranzītā reisā. (Pārējās divas opcijas ir **Izveidojiet saņemšanas žurnāla** pogu, kas vēlāk ir aprakstīta šajā tabulā, un Warehouse Management mobile programmā.) Šī opcija ir vienkāršākā opcija, un apstrādās preces tranzītā no tranzītkrājumu noliktavas un galamērķa noliktavā. Ja vēlaties veikt lielāku procesa kontroli, izmantojiet saņemšanas žurnālu vai mobilo ierīci, lai apstrādātu preču saņemšanu. |
| Atrast automātiskās izmaksas | Atrast atbilstošās reisa izmaksas. Ja šīs izmaksas jau ir atrastas vai atjauninātas, tiek saņemts šāds ziņojums: "Pastāv rēķinā neiekļautas izmaksu rindas. Vai vēlaties tos pārrakstīt?" Tiks atrastas visas izmaksas, kas nebija saistītas ar reisu izveides laikā. Ievērojiet, ka reisu izmaksas, kas ir pievienotas reisam un kurām izrakstīts rēķins, netiks pārrakstītas. |
| Izveidot saņemšanas žurnālu | <p>Atveriet dialoglodziņu **Izveidot saņemšanas žurnālu**, kurā varat izveidot saņemšanas žurnālu, kas nosaka atrašanās vietu. Minētajā dialoglodziņā ir pieejamas šādas opcijas:</p><ul><li>**Izveidojiet no tranzīt precēm** vai **Izveidot no pārsūtīšanas pasūtījuma** – šīs opcijas etiķete mainās atkarībā no tā, vai izmantojat preču tranzīta procesu. Iestatiet to uz *Jā*, lai atvērtu saņemšanas žurnāla lapu, kas ļauj apstrādāt standarta saņemšanas žurnālu tranzīt precēm, kas ir saistītas ar reisu. Ja krājums jau ir saņemts gala adresāta noliktavā, tas netiks pievienots saņemšanas žurnāla rindām.</li><li>**Inicializēt daudzumu** — iestatiet šo opciju kā *Jā*, lai inicializētu saņemto daudzumu, pamatojoties uz preču daudzumu, kas norādīts reisa rindā. Ja reisa rinda ir daļēji saņemta, šis daudzums ir atlikušais daudzums. Ieteicams saglabāt šo opciju iestatīt uz *Jā*.</li><li>**Izveidot no pasūtījuma rindām** – iestatiet šo opciju uz *Jā*, lai izmantotu pasūtījuma rindu vērtību.</li></ul><p>Šī poga ir viena no trim opcijām, kas ir pieejamas preču saņemšanai tranzīta reisā. (Citas opcijas ir **Saņemt tranzīta preces** poga, kas iepriekš aprakstīta šajā tabulā, un Warehouse Management mobile programma.)</p> |
| Uzkrāt izmaksas | Uzkrāt izmaksas, kur izmaksu tipam ir norādīts debeta Virsgrāmatas konts. Šī poga parasti tiek lietota, kad krājums ir tranzītā vai kad preces ir saņemtas un iekļautas rēķinā. |
| Apkopot izmaksas | Pārvietojiet izmaksas no nosūtīšanas konteinera līmeņa uz reisa līmeni. Šo pogu var izmantot koplietotos pakalpojumos/nosūtīšanas scenārijā, kur vairākiem elementiem ir kopīga pārvadāšanas konteinera vai kartona kārbas vieta. Piemēram, reisam ir 40 pēdu kravas pārvadāšanas konteiners un 20 pēdu kravas pārvadāšanas konteiners, un iedalīšana tiek veikta pēc apjoma. Šajā gadījumā iespējams, ka preces/entītijas, kas koplieto vai izmanto vietu 20 pēdu kravas pārvadāšanas konteinerā, var tikt inicializētas. Lai pašizmaksas sadalītu vienmērīgi, dažas organizācijas varētu vēlēties pārsūtīt izmaksas uz reisu un sadalīt tās, balstoties uz reisa līmeņa iedalīšana metodi. |
| Mainīt maršruta veidni | Atveriet dialoglodziņu, kur var nomainīt reisa veidni. Pēc veidnes maiņas reisa izmaksas tiks dzēstas. Tāpēc, iespējams, būs jāatlasa **Meklēt automātiskās izmaksas** (skatiet aprakstu iepriekš šajā tabulā) vai vēlreiz jāpievieno izmaksas manuāli. |

### <a name="buttons-on-the-general-tab"></a>Pogas cilnē Vispārīgi

Šajā tabulā ir aprakstītas pogas, kas ir pieejamas darbību rūts cilnē **Vispārīgi**.

| Poga | Apraksts |
|---|---|
| Saņemšanas saraksts | Atveriet saņemšanas preču sarakstu visām pirkšanas pasūtījuma rindām reisā. Ja tiek izmantotas vairāku uzņēmumu kravas, katram uzņēmumam tiek atvērts jauns saņemšanas saraksta grāmatošanas dialoglodziņš. Ja produktu ieejas plūsmu saraksti nav apstrādāti, šī poga nav pieejama. |
| Produktu ieejas plūsma | Atveriet produktu ieejas plūsmas ierakstu pirkšanas pasūtījuma rindām, kas ir saistītas ar reisu, ja tiek izmantots šis ieraksts. Ja produktu ieejas plūsmu saraksti nav grāmatoti, šī poga nav pieejama. Produktu ieejas plūsmas process netiks izmantots, ja izmantojat tranzītā kravu apstrādi. |
| Krājumu saņemšana | Atveriet krājumu saņemšanas žurnālu, ja tas tiek izmantots. |
| Izsekošana | Atveriet **Ienākošo sūtījumu izsekošanas** lapu, kurā jūs varat atjaunināt paredzēto preču saņemšanas datumu nosūtīšanas konteinerā un reisā, un pēc tam atjaunināt pirkšanas pasūtījuma rindu paredzamos piegādes datumus. |
| Izmaksu pieprasījums | <p>Atvērt lapu **Izmaksas uzziņas**, kurā parādītas visas reisa izmaksas.</p><p>Darbības rūtī atlasiet **Skatīt**, lai pielāgotu skatu. Varat apskatīt jebkuru no līmeņiem, plus krājuma un izmaksu tipa kodu.</p><p>**Izmaksu pieprasījuma** lapā ir redzami tikai izmaksu tipu kodi, kas ir tieši saistīti ar krājumu darbībām. Noņemot šos izmaksu tipu kodus, varat pielāgot lapu, grupējot izmaksas. Šī iespēja var būt noderīga, ja izmantojat izmērus un krāsas.</p><p>Lapa **Izmaksu uzziņas** rāda tikai tos izmaksu tipu kodus, kur lauks **Debets** ir iestatīts uz *Krājums*.</p> |
| Tranzītpreču pasūtījumi | Atvērt lapu **Tranzīta preču pasūtījumi**, kurā ir redzami tikai atlasītā reisa preču tranzīta ieraksti. |

## <a name="lines-view"></a>Rindu skats

Lai atvērtu **Rindu** skatu, atveriet reisu un pēc tam atlasiet cilni **Rindas** reisa galvenes augšējā labajā stūrī.

### <a name="information-on-the-voyage-header-fasttab"></a>Informācija par Reisa virsraksta kopsavilkuma cilni

**Reisa virsraksta** kopsavilkuma cilne reisa **Rindu** skatā satur pamatinformāciju, kas apraksta reisu. Daudzi no šajā kopsavilkuma cilnē parādītajiem laukiem tiek parādīti arī **Galvenes** skatījumā, kā aprakstīts tālāk šajā tēmā.

### <a name="information-on-the-voyage-lines-fasttab"></a>Informācija par Reisa rindu kopsavilkuma cilni

**Reisa rindu** kopsavilkuma cilne **Rindu** skatā ir saistīta ar informāciju par reisu un informāciju par izmaksām, kas piemērojamas reisa līmenī. Šeit var pārskatīt nosūtīšanas konteinerus, folio un krājumus, kas pievienoti reisam. Tiek parādīta arī reisa krājumu cena un daudzums. Varat skatīt jebkuru nosūtīšanas konteineru vai folio, kas ir uzskaitīts, atlasot atbilstošo saiti.

### <a name="information-on-the-line-details-fasttab"></a>Kopsavilkuma cilnes Rindas informācija

Kopsavilkuma cilne **Detalizēta informācija par rindām** **Rindu** skatā rāda detalizētu informāciju par pirkšanas pasūtījuma rindu, kas pašlaik ir atlasīta kopsavilkuma cilnē **Rindas**. Ievērojiet, ka šajā kopsavilkuma cilnē ir ietverta detalizēta informācija par pozīciju, kādu katra rinda ieņem konteinerā, un tas ir deklarētais daudzums.

## <a name="header-view"></a>Virsraksta skatījums

Lai atvērtu **Galvenes** skatu, atveriet reisu un pēc tam atlasiet cilni **Galvene** reisa galvenes augšējā labajā stūrī.

### <a name="settings-on-the-general-fasttab"></a>Kopsavilkuma cilnes Vispārīgi iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami folio **Galvenes** skata kopsavilkuma cilnē **Vispārīgi**.

| Lauks | Apraksts |
|---|---|
| Reiss | Ievadiet reisa vai reisa numuru. |
| Rezervēšanas atsauce | Ja kravas nosūtītājs vai nosūtīšanas centrs nodrošina atsauces numuru reisa identifikācijai (t.i., kravas nosūtītāja vai nosūtīšanas centra iekšējo atsauci), ievadiet to šeit. |
| Kuģis | Ievadiet vai atlasiet kuģi. Ja kuģis nav uzskaitīts kā vērtība, kuģa ID varat ievadīt kā brīvu tekstu. Tādā gadījumā galvenā tabula netiek atjaunināta tā, lai vēlāk šajā laukā varētu atlasīt kuģa ID. |
| Ārējais reisa ID | Ievadiet publiski pieejamo reisa ID (piemēram, reisa numuru). |
| Vispārējā gaisa kravas pavadzīme/preču transporta pavadzīme | Ievadiet vispārējo gaisa ceļa laiku vai preču transporta pavadzīmes numuru. Šo vērtību var norādīt, izmantojot gaisa pārvadājumus. |
| Sākotnējā gaisa kravas pavadzīme/preču transporta pavadzīme | Kravas konteineram var norādīt mājas gaisa ceļa laiku vai preču transporta pavadzīmi. |
| Noma | Atzīmējiet šo izvēles rūtiņu, lai norādītu, ka konteiners ir nomas konteiners, kas ir jāatgriež. |
| Apraksts | Ievadiet reisa aprakstu, lai būtu vieglāk atpazīt. |
| Reisa statuss | Reisa statuss. Vērtībās ir *Izveidots*, *Tranzītā*, *Saņemtie dokumenti* un *Izmaksas*. Šis lauks nav aprēķināts, pamatojoties uz loģiku. To atjaunina tikai, izmantojot grāmatošanas darbību. *Izmaksu* vērtība norāda, ka ir saņemts rēķins par krājumu un visām reisu izmaksām. Ja vien rēķins nav saņemts, reisa statuss nevar būt *Izmaksas*. |
| Pirkšanas pasūtījuma statuss | Augstākais statuss, kas ir sasniegts starp visiem pirkšanas pasūtījumiem, kas ir saistīti ar reisu. |
| Saņemtie dokumenti | Vērtība, kas norāda, vai jūsu uzņēmums ir saņēmis visus dokumentus, kas ir saistīti ar reisu. Lai mainītu vērtību, atlasiet **Saņemtie dokumenti** grupā **Reisa atjaunināšana** darbību rūts cilnē **Pārvaldīt**. |
| Nosūtīšanas uzņēmums | Atlasiet šim reisam nosūtīšanas uzņēmumu. Šo lauku var izmantot, lai noteiktu automātiskās izmaksas. |
| Vārds, uzvārds | Uzņēmuma nosaukums, kas ir atlasīts laukā **Nosūtīšanas uzņēmums**. |
| Mērījums | Šis lauks aktivizē mērījumu norādīšanu automātiskajās izmaksās. Bieži vien mērījumus izmanto organizācijas, kas nezina preču individuālo tilpumu vai svaru, bet pieprasa daudz precīzāku sadali nekā to sniedz daudzums vai skaits. Kravas ekspediators vai aģents nodrošina organizāciju ar svara vai kubikmetru krājumu līmenī vai pirkšanas pasūtījuma līmenī. Ja parametrs ir atlasīts, to var atjaunināt automātiski vai ievadīt manuāli. |
| Mērvienība | Mērvienība, kas attiecas uz skaitli laukā **Mērījums**. |
| Palešu skaits | Norādiet reisa rindā palešu skaitu. Šis lauks tiek automātiski atjaunināts, ja opcija **Automātiski atjaunināt kartona kārbu skaitu** ir iestatīta uz *Jā* lapas **Kopējo izmaksu parametri** cilnē **Vispārīgi**. |

### <a name="settings-on-the-delivery-fasttab"></a>Kopsavilkuma cilnes Dimensijas iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami reisa **Galvenes** skata kopsavilkuma cilnē **Piegāde**.

| Lauks | Apraksts |
|---|---|
| Izveidošanas datums un laiks | Reisa ieraksta izveidošanas datums un laiks. |
| Produkta izvešanas no rūpnīcas datums | Šis lauks atlasa agrāko no fabrikas datumu starp pirkšanas pasūtījumiem, kas ir saistīti ar reisu. No fabrikas datums ir pieejams pirkšanas pasūtījuma galvenē un tiek atjaunināts, izmantojot izsekošanas kontroles iespēju. |
| Nosūtīšanas datums | Plānotais datums, kad lidmašīna vai kuģis faktiski atstāj izcelsmes vietu. |
| Izbraukšanas datums | Izlidošanas datums parasti ir datums, kad lidmašīnu vai kuģis faktiski atstāj aizjūras ostu. Nav jāatbilst nosūtīšanas datumam un izbraukšanas datumam. Lauks **Izlidošanas datums** ir tikai informatīvs. Tas netiek izmantots, lai prognozētu paredzamo piegādes datumu. Izsekošanas kontroles līdzeklis tiek izmantots, lai prognozētu piegādes datumu, un šo lauku var iestatīt tā, lai to automātiski aizpildītu izsekošanas kontroles funkcija. |
| Nonākšanas veikalā datums | Šis lauks atlasa agrāko datumu, kad pārdošanai būs pieejamas preces no pirkšanas pasūtījumiem, kas ir saistīti ar reisu. |
| Aprēķinātais piegādes datums | Plānotais piegādes datums parasti ir datums, kad preces pienāks noliktavā. Šis lauks ir paredzēts tikai informatīviem nolūkiem. Tas netiek izmantots preču vispārējai plānošanai. Pirkšanas pasūtījuma rindā paredzētais piegādes datums tiek izmantots preču vispārējai plānošanai reisā un tiek atjaunināts, izmantojot izsekošanas kontroles funkciju. Šo lauku var iestatīt, lai tiek aizpildīts ar izsekošanas kontroles funkciju. |
| Faktiskais piegādes datums | Agrākais piegādes datums, balstoties uz precēm, kas saistītas ar reisu. |
| ETA nosūtīšanas ostā | Ievadiet datumu, kad jūs sagaidāt reisa pienākšanu nosūtīšanas ostā, pamatojoties uz informāciju, ko sniedza jūsu nosūtīšanas aģents. |
| Oriģinālais dokuments saņemts | Ievadiet sākotnējo dokumentu saņemšanas datumu. |
| Brokeris ieteica | Ievadiet muitas starpnieka ieteikšanas datumu. |
| Sākotnējā preču transporta pavadzīme nosūtīta | Ievadiet datumu, kad tika nosūtīta sākotnējā preču transporta pavadzīme. |
| Preces izpildītas | Ievadiet datumu, kad preces tika izlaistas no muitas. |
| Norunātā tikšanās ar klientu | Ievadiet debitora norīkojuma datumu, kas ir datums, kad debitors plāno īpašumtiesības precēm. |
| Sūtījums piegādāts noliktavā | Ievadiet datumu, kad preces tika piegādātas noliktavā. |
| Pārbaudes datums | Ievadiet pārbaudes datumu. |
| Piegādes instrukcijas | IEvadiet datumu, kad tika saņemtas piegādes instrukcijas. |
| Piegādes veids | Šajā laukā ir sniegta informācija par metodi, kas tiek izmantota reisa piegādei, un ar šo piegādes metodi saistīto automātisko izmaksu izmaksu atlase. |
| No ostas | Nosūtīšanas osta, no kuras nāk reiss. |
| Uz ostu | Reisa saņemšanas osta. Sūtījuma konteineram var būt dažādas ostas, jo kuģis var piestāt vairākās ostās. Pārbaudot ostu "uz" pārvadāšanas konteinera līmenī, jūs nodrošināt precīzu informāciju par ostu katram reisa konteineram. Ar kravas transportēšanu saistītās automātiskās izmaksas tiek noteiktas, pamatojoties uz pārvadāšanas konteinera tipa, porta "uz" un "no" porta kombināciju. |
| Vietējais ekspeditors | Šis lauks ir paredzēts tikai informatīviem nolūkiem. Lokālajam ekspeditoram jābūt atlasāmam no kreditoru tabulas. |
| Vietējā transporta datums | Ievadiet datumu, kurā ir rezervēts vietējais transports. Šis lauks var palīdzēt noliktavai veikt tās plānošanu. |
| Vietējā transporta laiks | Ievadiet laika posmu, kurā ir rezervēts vietējais transports. Šis lauks var palīdzēt noliktavai veikt tās plānošanu. |
| Maršruta veidne | Ceļojuma veidne, kas ir norādīta reisam. Ceļojuma veidne tiek izmantota, lai ievadītu pārvadāšanas konteinera un reisa portu "uz" un "no". Šīs vērtības savukārt palīdz noteikt automātiskās izmaksas, kas ir saistītas ar reisu. |

### <a name="settings-on-the-other-fasttab"></a>Kopsavilkuma cilnes Citi iestatījumi

Šajā tabulā ir aprakstīti lauki, kas ir pieejami folio **Galvenes** skata kopsavilkuma cilnē **Citi**.

| Lauks | Apraksts |
|---|---|
| Atzīmes | Ievadiet papildu informāciju, kas saistīta ar reisu. |
| Apstiprināšanas datums | Atlasiet agrāko no fabrikas datumu starp pirkšanas pasūtījumiem, kas ir saistīti ar reisu. |
| Neapstiprināts reiss | Varat to izmantot, lai norādītu, vai jūsu sūtījums vai reiss vēl nav atlicis. Tā ir paredzēta tikai informatīviem nolūkiem.  |
| Nosūtīšanas konteineru pārdēvēšana | Reisiem, kuriem ir vairāk nekā viens konteiners, vēl nav saņemts konteineru skaits. |

## <a name="voyage-update-periodic-tasks"></a>Reisa atjaunināšanas periodiskie uzdevumi

**Kopējo izmaksu** modulī ir ietverti vairāki ar reisiem saistīti periodiskie uzdevumi, kas var veikt vairāku reisu lielapjoma atjauninājumu aspektus. Lai palaistu vai ieplānotu šos periodiskos uzdevumus, dodieties uz **Kopējās izmaksas \> Periodiskie uzdevumi \> Reisa atjauninājumi**, tad atlasiet vienu no šādiem uzdevumu tipiem:

- **Saņemtie dokumenti** – šis uzdevums ļauj iestatīt **Saņemtos dokumentus** kā *Jā* vairākiem reisiem vienlaicīgi. Izmantojiet **Filtra** iestatījumus, lai definētu reisu kopu, ko vēlaties atjaunināt.
- **Tranzītā** – šis uzdevums ļauj iestatīt **Reisa statusa** lauku uz tranzīta statusu, kas ir izveidots **[Kopējo izmaksu parametru](landed-cost-parameters.md)** lapā vairākiem reisiem vienlaicīgi. Izmantojiet **Filtra** iestatījumus, lai definētu reisu kopu, ko vēlaties atjaunināt.
- **Tranzītā** – šis uzdevums ļauj iestatīt **Reisa statusa** lauku uz tranzīta statusu, kas ir izveidots **[Kopējo izmaksu parametru](landed-cost-parameters.md)** lapā vairākiem reisiem vienlaicīgi. Parasti jūs iestatīsiet, lai šis uzdevums darbotos saskaņā ar grafiku.
- **Izmaksas** — šis uzdevums ļauj iestatīt **Reisa statusa** lauku izmaksu statusam, kas ir izveidots **[Kopējo izmaksu parametru](landed-cost-parameters.md)** lapā vienlaicīgi ar noteikumu, ka tiem ir izmaksātas izmaksas, bet nav vēl atjauninātas reisā. Parasti jūs iestatīsiet, lai šis uzdevums darbotos saskaņā ar grafiku.
