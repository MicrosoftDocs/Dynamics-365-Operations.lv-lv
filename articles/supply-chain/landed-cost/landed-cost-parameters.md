---
title: Kopējo izmaksu parametru iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt vispārējo informāciju un konfigurācijas iestatījumus, kas tiek izmantoti Kopējo izmaksu modulī grāmatošanai, statusa atjauninājumiem, numuru sērijām un uzvedībai.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 3b6678b2579db00a9f8884786fdaacd027fab744
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403980"
---
# <a name="landed-cost-parameters-setup"></a>Kopējo izmaksu parametru iestatīšana

[!include [banner](../../includes/banner.md)]

Lapu **Kopējo izmaksu parametri** var izmantot, lai iestatītu vispārīgu informāciju un konfigurācijas iestatījumus, kas tiek izmantoti **Kopējo izmaksu** modulī grāmatošanai, statusa atjaunināšanai, numuru sērijām un uzvedībai. Parametru iestatījumi tiek koplietoti juridiskajām personām, un tos var modificēt administrators.

## <a name="open-the-landed-cost-parameters-page"></a>Atvērt lapu Kopējo izmaksu parametri

Lai strādātu ar parametriem, dodieties uz sadaļu **Kopējās izmaksas \> Iestatījumi \> Kopējo izmaksu parametri**, tad iestatiet laukus, kā aprakstīts nākamajās sadaļās.

![Kopējo izmaksu parametru lapa.](media/landed-cost-parameters.png "Kopējo izmaksu parametru lapa")

## <a name="general-tab"></a>Cilne Vispārīgi

### <a name="general-fasttab"></a>Cilne Vispārīgi

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami kopsavilkuma cilnes **Vispārīgi** cilnē **Vispārīgi** lapā **Kopējo izmaksu parametri**.

| Iestatījums | Apraksts |
|---|---|
| Izmantot nosūtīšanas likmi | Nosūtīšanas likme ir iestatīta noteiktam periodam un tiek izmantota, lai prognozētu preču, kas izmanto vairākas valūtas, izmaksas. Iestatiet šo opciju kā *Jā*, lai izmantotu nosūtīšanas likmi. |
| Maiņas kursa veids | Noklusējuma maiņas kursu apkopojums, ko izmanto vairāku valūtu aprēķiniem reisu un reisu izmaksām. |
| Atjaunināt pirkšanas pasūtījuma daudzumu | Atlasiet, kas notiek, ja lietotājs maina daudzumu pirkšanas pasūtījuma rindā:<ul><li>**Pieņemt** – reisa daudzums tiek koriģēts automātiski.</li><li>**Brīdinājums** – ja rinda ir pievienota reisam, tiek parādīts brīdinājums, bet reisa daudzums tiek atjaunināts.</li><li>**Kļūda** – ja rinda ir pievienota reisam, tiek rādīts kļūdas ziņojums un pirkšanas pasūtījumu nevar atjaunināt. Tādēļ pasūtījuma rinda vispirms ir jānoņem no reisa.</li></ul> |
| Automātiski atjaunināt kastu skaitu | Kad šī opcija ir iestatīta kā *Jā*, visas kartona kārbas tiek pievienotas kopā un parādītas reisu un konteineru līmeņos. Kad tas ir iestatīts uz *Nē*, kartona kārbu skaits sākotnēji ir iestatīts uz 0 (nulle) un to var manuāli rediģēt pēc vajadzības. |

### <a name="costing-fasttab"></a>Izmaksu kopsavilkuma cilne

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami kopsavilkuma cilnes **Vispārīgi** cilnē **Vispārīgi** lapā **Kopējo izmaksu parametri**.

| Iestatījums | Apraksts |
|---|---|
| Grāmatošanas specifikācija | Atlasiet vērtības korekciju Virsgrāmatā:<ul><li>**Kopsumma** – kopsummas skaitlis tiek grāmatots Virsgrāmatā.</li><li>**Krājumu grupa** – korekciju nosaka katrai krājumu grupai.</li><li>**Krājuma numurs** – korekciju nosaka katram krājumam. Šī vērtība sniedz visvairāk informācijas.</li></ul> |
| Atļaut nulles izmaksas | Iestatiet šo opciju uz *Nē*, lai rādītu kļūdu, ja lietotājs mēģina grāmatot izmaksu novērtējumu reisa rēķinam vai pirkšanas pasūtījumam, kas neietver paredzamo reisa izmaksu vērtību. Kļūdas ziņojums norāda, ka nevar sadalīt izmaksas 0 (nulle) un rēķina grāmatošana neizdosies. Šajā gadījumā lietotājs var manuāli atjaunināt novērtējumu (vai pārkonfigurēt automātiskās izmaksas) un pēc tam vilkt atjaunināto vērtību vai dzēst izmaksas, ja tā nav spēkā.<p>Iestatiet šo opciju kā *Jā*, lai reisa izmaksas varētu būt tukšas. Šajā gadījumā cena 0 (nulle) tiks sadalīta atbilstoši izmaksu apgabalam. Pēc tam kreditora izmaksu rēķinu var apstrādāt attiecībā pret nulles cenas izmaksām, kad ir saņemts reiss.</p><p>Iesakām konfigurēt novērtējumu automātiskajam izmaksu ierakstam, lai novērstu nulles cenas izmaksu parādīšanos. Lai gan šis novērtējums nav pilnībā precīzs, tam joprojām jābūt precīzākam par pieņemamo nulles izmaksu.</p> |
| Korekcijas grāmatošanas datums | Kad grāmatojat Parādu kreditoriem reisu izmaksu rēķinu, tiek atjaunināta arī nosegšanas darbību tabula (krājumu pielāgojumi). Atlasiet datumu, kas pēc noklusējuma iestatīts lapā **Reisu izmaksu atlase**, kamēr esat rēķinu žurnālā:<ul><li>**Darījuma datums** – izmanto žurnāla darījumu grāmatošanas datumu.</li><li>**Pirkšanas pasūtījuma rēķina datums** – izmantojiet krājuma (pirkšanas pasūtījuma) rēķina finanšu grāmatošanas datumu.</li><li>**Atlasītais datums** – lietotājs var norādīt grāmatošanas datumu. Kaut arī datumu var atstāt tukšu, ja izmaksu rēķina grāmatošanas laikā tas joprojām nav tukšs, lietotājs saņems kļūdas ziņojumu.</li></ul> |
| Izmantot pirkuma rēķina kuponu | Kad šī opcija ir iestatīta uz *Jā*, izmaksu uzkrājuma darbības izmantos to pašu dokumenta numuru, kas tiek izmantots pirkšanas rēķinam. Kad tas ir iestatīts uz *Nē*, sistēma izmantos nākamo pieejamo numuru **Izmaksu uzkrāšanas dokumentu** numuru sērijai, kas ir iestatīta cilnē **Numuru sērijas** lapā **Kopējo izmaksu parametri**.<p>Šī problēma rodas, izrakstot rēķinu pirkšanas pasūtījumam, ja opcija **Grāmatot Virsgrāmatas izmaksu kontā** ir iestatīta uz *Jā* cilnē **Rēķins**, kas atrodas lapā **Kreditoru parametri**.</p> |
| Bloķēt manuālu grāmatošanu dzēšanas kontā | Iestatiet šo opciju kā *Jā*, lai neļautu grāmatošanu klīringa kontos, kur darbība nav saistīta ar reisu, atlasot **Funkcijas \> Izvēlieties reisa izmaksas** kreditora rēķinu žurnāla darbību rūtī. Ieteicams iestatīt šo opciju kā *Jā*, lai varētu pareizi nosegt reisa un klīringa kontu. |
| Izmantot izmaksu veida maksas uzkrāšanas kontu | Kad šī opcija ir iestatīta uz *Jā*, izmaksu uzkrāšanas konts, kas ir konfigurēts atbilstošajam izmaksu tipa kodam izmaksu tipu kodu lapā **Izmaksu tipu kodi**, izmantos, lai uzkrātu izmaksas kā izdevumus.<p>Šī problēma rodas, izrakstot rēķinu pirkšanas pasūtījumam, ja opcija **Grāmatot Virsgrāmatas izmaksu kontā** ir iestatīta uz *Jā* cilnē **Rēķins**, kas atrodas lapā **Kreditoru parametri**. |
| Iegrāmatot korekcijas kā izmaiņas | Kad šī opcija ir iestatīta uz *Jā*, tā ignorē standarta funkcionalitāti un liek krājumu korekcijas darbības, kas ir saistītas ar noviržu starp prognozētajām izmaksām un faktiskajām izmaksām, grāmatot noviržu kontā.<p>Kad šī opcija ir uzstādīta uz *Nē*, krājumu korekcijas darbības, kas ir saistītas ar noviržu, tiek apstrādātas, balstoties uz izmaksu grāmatošanas metodes un izmaksu tipa koda konfigurāciju. Standarta izmaksām novirzes joprojām tiks grāmatotas noviržu kontā. Lai pārvietotu svērto vidējo (WMA), novirzes tiks grāmatotas vai nu novirzes kontā, vai krājumos.</p><p>Šī problēma rodas, izrakstot rēķinu pirkšanas pasūtījumam, ja opcija **Grāmatot Virsgrāmatas izmaksu kontā** ir iestatīta uz *Jā* cilnē **Rēķins**, kas atrodas lapā **Kreditoru parametri**.</p> |

### <a name="validation-fasttab"></a>Kopsavilkuma cilne Pārbaude

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami kopsavilkuma cilnes **Vispārīgi** cilnē **Vispārīgi** lapā **Kopējo izmaksu parametri**.

| Iestatījums | Apraksts |
|---|---|
| Vairāki izmaksu rēķini | Atlasiet, kas notiek, ja vienai papildmaksai pret reisu, folio vai konteineru tiek apstrādāti vairāki rēķini.<ul><li>**Pieņemt** – sistēma atļautu vairākus izmaksu rēķinus.</li><li>**Brīdinājums** – tiek parādīts brīdinājums.</li><li>**Kļūda** — tiek parādīts kļūdas ziņojums.</li></ul> |
| Vairāki kreditori vienā folio | Atlasiet to, kas notiek, ja folio tiek pievienoti vairāk nekā viena kreditora pirkšanas pasūtījumi.<ul><li>**Pieņemt** – sistēmai būtu jāatļauj darbība.</li><li>**Brīdinājums** – tiek parādīts brīdinājums, bet darbību joprojām var veikt.</li><li>**Kļūda** – tiek rādīts kļūdas ziņojums, un darbība netiek novērsta.</li></ul><p>Jūsu muitas starpnieks vai lokālie likumi var noteiktai vērtībai šajā laukā.</p> |
| Piegādes tolerances vairāki režīmi | Atlasiet, kas notiek, ja šai reisam tiek pievienotas preces pirkšanas pasūtījumā, kas izmanto citu piegādes veidu nekā reiss.<ul><li>**Pieņemt** – sistēmai būtu jāatļauj darbība.</li><li>**Brīdinājums** – tiek parādīts brīdinājums, bet darbību joprojām var veikt.</li><li>**Kļūda** – tiek rādīts kļūdas ziņojums, un darbība netiek novērsta.</li></ul> |
| Vairāku noliktavu tolerance | Atlasiet, kas notiek, ja reiss ietver vairākas pasūtījuma rindas, kas jāpiegādā dažādās noliktavās. Šīs pasūtījuma rindas var izplatīties starp vienu vai vairākiem pirkšanas pasūtījumiem.<ul><li>**Pieņemt** – sistēmai būtu jāatļauj darbība.</li><li>**Brīdinājums** – tiek parādīts brīdinājums.</li><li>**Kļūda** — tiek parādīts kļūdas ziņojums.</li></ul> |
| Trūkst apjoma | Atlasiet, kas notiek, ja lietotājs pievieno krājumu bez tilpuma reisam.<ul><li>**Pieņemt** – sistēmai būtu jāatļauj darbība.</li><li>**Brīdinājums** – tiek parādīts brīdinājums.</li><li>**Kļūda** — tiek parādīts kļūdas ziņojums.</li></ul><p>Ja apjomus izmanto, lai aprēķinātu un sašautu izmaksas, ieteicams atlasīt *Brīdinājumu* vai *Kļūdu*.</p> |
| Pakalpojumu sniedzējs bez reisa izmaksām | Atlasiet, kas notiek, ja lietotājs mēģina apstrādāt rēķinu pakalpojumu sniedzējam, kas nav saistīts ar reisu. <ul><li>**Pieņemt** – sistēmai būtu jāatļauj darbība.</li><li>**Brīdinājums** – tiek parādīts brīdinājums.</li><li>**Kļūda** — tiek parādīts kļūdas ziņojums.</li></ul><p>Ieteicams atlasīt *Brīdinājumu*.</p> |

### <a name="defaults-fasttab"></a>Kopsavilkuma cilne Noklusētie iestatījumi

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami kopsavilkuma cilnes **Noklusētie iestatījumi** cilnē **Vispārīgi** lapā **Kopējo izmaksu parametri**.

| Iestatījums | Apraksts |
|---|---|
| Žurnāla nosaukums | Atlasiet noklusēto žurnālu, kuram vajadzētu izmantot funkciju *Izveidot saņemšanas žurnālu*. |
| Reisa statuss | Izvēlieties statusu, kādam jābūt reisam, pirms lietotāji var iestatīt sistēmai nomas nosūtīšanas konteineru. Šī darbība parasti notiek, kad preces ir tranzītā vai dokā. |
| Maršruta veidne | Atlasiet noklusējuma ceļojuma veidni, ko izmantot jauniem nomas nosūtīšanas konteineriem. Parasti jūs atlasīsiet ceļojuma veidni, kurā iekļautas nomas izmaksas. |
| Kustība | Ja piegādes daudzums, kas ir virs/zem daudzuma, ir definētā pielaidē, kustības žurnāls tiks apstrādāts automātiski. Atlasiet noklusēto kustības žurnālu, kuru lietot. Atlasītā kustības žurnāla nosaukuma konta nosaukumam ir jābūt vērtībai laukā **Korespondējošais konts**. |
| Pārnesums | Kad nepiegādātās preces ir apstrādātas, īso ieejas plūsmu daudzums tiks pārsūtīts uz netīstās piegādes noliktavu. Atlasiet noklusēto pārsūtīšanas žurnālu, kuru lietot. |
| Atspējot pirkšanas pasūtījumus bez reisiem | Izslēdziet funkcionalitāti Kopējo izmaksas pār piegādātām/nepiegādātām precēm pirkšanas pasūtījumiem, kas nav pievienoti reisam. |
| Atspējot preču, kas nav tranzīta zonā, pirkšanas pasūtījumus | Izslēdziet funkcionalitāti Kopējo izmaksas pār piegādātām/nepiegādātām precēm pirkšanas pasūtījumiem, kas neizmanto tranzīta preču funkciju. |
| Tranzītpreces saņemšanas pagarinājuma periodā | Norādiet dienu skaitu pēc nosūtīšanas konteinera pirmās saņemšanas, ko joprojām var pabeigt šim pārvadāšanas konteineram. |

## <a name="status-updates-tab"></a>Statusa atjaunināšanas cilne

Sistēma izmanto statusa vērtības, lai norādītu katra reisa statusu. Reisa statusa vērtības var automātiski izmantot reisiem, izmantojot reisu izsekošanu vai periodiskus pakešuzdevumus. Alternatīvi tos var lietot manuāli, atverot reisu un pēc tam atlasot statusu **Reisa atjaunināšanas** grupā darbību rūts cilnē **Pārvaldīt**. 

Var izveidot neierobežotu skaitu reisa statusu vērtību. Tomēr četri no tiem ir jādefinē kā izmantoti īpašam nolūkam lapas **Kopējo izmaksu parametri** cilnē **Statusa atjaunināšana**. Nākamajā tabulā ir aprakstīti pieejamie lauki.

| Iestatījums | Apraksts |
|---|---|
| Aprēķinātās izmaksas | Atlasiet reisa statusu, kas norāda, ka reiss ir pabeigts. |
| Tranzītā | Atlasiet reisa statusu, kas norāda, ka reiss ir tranzītā. |
| Sagatavots izmaksu aprēķināšanai | Atlasiet reisa statusu, kas norāda, ka reiss ir sagatavots izmaksu skaitīšanai. Šis statuss tiek izmantots, kad visi krājumu pirkšanas rēķini un reisa izmaksu rēķini, kur lauks **Reisa izmaksu kredīts** ir iestatīts uz *Kreditors* un ir apstrādāts reisa apstrādei. Reisiem, kas neizdos izmaksu procesu, statuss būs *Gatavs izmaksu skaitīšanai*.|
| Iepriekš aprēķinātās izmaksas | Atlasiet reisa statusu, kas norāda, ka reiss ir sagatavots iepriekšēju izmaksu skaitīšanai. Šis statuss tiek izmantots, kad jauna izmaksu darbība tiek pievienota reisam pēc tam, kad tā jau ir izmaksāta. Jaunas izmaksu darbības var tikt pievienotas iepriekš grāmatotam reisam, kad tiek saņemts otrs kravas rēķins vai neparedzēta izdevumu maksa. Šis statuss tiek automātiski piemērots, kad maksu par reisu tiek pievienotas jaunai reisa maksai. |

## <a name="voyage-creator-tab"></a>Cilne Reisa veidotājs

Tabulā ir aprakstītas sadaļas lapas **Kopējo izmaksu parametri** cilnē **Reisa veidotājs**.

| Sadaļa | Apraksts |
|---|---|
| Tolerances | Lauki **Ārējā tilpuma tolerance** un **Ārpus svara tolerance** definē sliekšņus, virs kuriem preces tiek uzskatītas par pārāk daudz summu un lieko svaru. Ja lietotājs pievieno preces **Reisu redaktora** lapā, ja apjoms vai svars pārsniedz šeit iestatīto vērtību, sistēma parāda brīdinājumu. Katra lauka vērtība ir izteikta kā maksimālā tilpuma vai svara procentuālā vērtība, kas iestatīta kravu pārvadāšanas konteinera veidam. Ieteicams, lai vērtība būtu no 5 līdz 10 procentiem no maksimālā tilpuma vai svara. |
| Folio izveides iestatīšana | Reisa izveides procesa laikā sistēma var izveidot vairākus ražošanas procesus. Lietojiet šo sadaļu, lai definētu, kad jāizveido jauns folio. Katrai šīs sadaļas rindai sistēma pārbauda norādīto tabulu un lauku un izveidos folio katrai unikālai lauka vērtībai. |

## <a name="cost-estimates-tab"></a>Cilne Izmaksu novērtējumi

Lapas **Kopējie izmaksu parametri** cilne **Izmaksu novērtējumi** nodrošina tikai vienu lauku: **Noklusējuma izmaksu versija**. Šis lauks tiek lietots tikai tad, kad izmaksu metode ir *Standarta izmaksu aprēķināšana*. Atlasiet noklusēto izmaksu versiju, ko izmantot *Krājuma izmaksu cenas atjaunināšanas* periodiskajam uzdevumam. Iespējams, šis iestatījums būs jāmaina katru reizi, kad sākas jauns finanšu gads.

## <a name="inventory-dimensions-tab"></a>Cilne Krājumu dimensijas

Izmantojiet cilni **Krājumu dimensijas** lapā **Kopējo izmaksu parametri**, lai kontrolētu, kuras pieejamās krājumu dimensijas pēc noklusējuma ir jārāda katrā Kopējo izmaksu lapā, kur tiek izmantotas dimensijas.

Atlasiet dimensiju un pēc tam iestatiet opciju **Reisa rindas**, **Tranzīta krava** un/vai **Izmaksu novērtējumi** uz *Jā* katrai lapai, kurā pēc noklusējuma ir jārāda šī dimensija. Pēc vajadzības atkārtojiet šo darbību citām dimensijām.

Šīs cilnes iestatījumi izveido noklusējuma dimensijas katrai no juridiskajām personām nozīmētajai lapai. Tomēr lietotāji, kuri strādā vienā no norādītām lapām, var ignorēt noklusējuma dimensijas, darbību rūtī atlasot **Krājumi \> Rādīt dimensijas**.

## <a name="number-sequences-tab"></a>Cilne Numuru sērijas

Lapas **Kopējie izmaksu parametri** cilne **Numuru sērijas** uzskaita katru atsauces numuru secības tipu, kas ir nepieciešamas landed izmaksām, bet kas netiek koplietots juridiskajām personām. Katrai saraksta atsaucei atlasiet katras atsauces numuru sērijas kodu.

> [!NOTE]
> Vairāku uzņēmumu konfigurācijā katram uzņēmumam (juridiskajai personai) ir jāizveido dažādas numuru sērijas.

## <a name="shared-number-sequences-tab"></a>Cilne Kopīgoto numuru secība

Lapas **Kopējie izmaksu parametri** cilne **Numuru sērijas** uzskaita katru atsauces numuru secības tipu, kas ir nepieciešamas kopējām izmaksām, bet kas netiek koplietots juridiskajām personām. Sarakstā ir tikai viena numuru sērija. Šī numuru sērija tiek izmantota reisa ID.

Lapā **Visi reisi** lietotāji var skatīt visus reisus visām juridiskajām personām. Tomēr, lai rediģētu un apstrādātu reisu, lietotājiem jābūt atlasītā ieraksta juridiskajā personā.

## <a name="feature-visibility-tab"></a>Līdzekļu redzamības cilne

Ar Kopējām izmaksām tiek pievienotas funkcijas (lauki un funkcijas) vairākām bieži izmantotajām Microsoft Dynamics 365 Supply Chain Management lapām. Šīs lapas ietver lapas, kas ir saistītas ar kreditoru pamatdatiem, izlaistajām precēm, pirkšanas pasūtījumiem, pārsūtīšanas pasūtījumiem un noliktavas iestatījumiem. Ja izmantojat Kopējās izmaksas, šīs funkcijas ir jāizveido redzamās visur, kur var gūt labumu no tām. Ja neizmantojat Kopējās izmaksas, ir iespējams paslēpt funkcijas, lai novērstu to izgāšanu.

Lapas **Kopējo izmaksu parametri** cilnē **Līdzekļu redzamība** iestatiet opciju **Aktivizēt** uz *Jā*, lai redzētu Kopīgo izmaksu funkcijas vienmēr, kad tās ir pieejamas. Iestatiet to uz *Nē*, lai paslēptu iezīmes kopējās lapās ārpus Kopīgajām izmaksām. Tomēr, pat ja opcija ir iestatīta uz *Nē*, pats modulis, tostarp lapa **Kopējo izmaksu parametri**, būs pieejams lietotājiem ar pareizām atļaujām, lai piekļūtu tam.
