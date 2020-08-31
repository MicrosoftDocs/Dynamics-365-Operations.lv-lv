---
title: Novietojuma direktīvu izveide
description: Šajā tēmā izskaidrots, kā izveidot novietojuma direktīvas. Novietojuma direktīvas ir lietotāja definēti nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bdd99b5faefd7054023b45a91fad070aac055a26
ms.sourcegitcommit: ecad92c9cb7e9e57688e678f79f747673c921df5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2020
ms.locfileid: "3692142"
---
# <a name="create-location-directives"></a>Novietojuma direktīvu izveide

[!include [banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā izveidot novietojuma direktīvas. Novietojuma direktīvas ir lietotāja definēti nosacījumi, kas palīdz identificēt izdošanas un izvietošanas novietojumus krājumu kustībai. Piemēram, pārdošanas pasūtījuma transakcijai novietojuma direktīva nosaka, kur krājumi tiks izdoti un kur izdotie krājumi tiks izvietoti.

> [!NOTE]
> Šī tēma attiecas uz moduļa **Noliktavas pārvaldība** līdzekļiem. Tas neattiecas uz līdzekļiem modulī [Krājumu vadība](../inventory/inventory-home-page.md).

Varat izmantot novietojuma direktīvas, lai veiktu tālāk norādītos uzdevumus.

- Ienākošo krājumu izvietošanai.
- Izejošajām transakcijām paredzēto krājumu izdošanai un organizēšanai.
- Izejvielu izdošanai un nodošanai ražošanai.
- Novietojumu papildināšanai.

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms jūs varat izveidot novietojumu direktīvu, jums ir jāveic šādas darbības, lai nodrošinātu, ka tiek ievēroti priekšnosacījumi.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Noliktava \> Noliktavas**.
1. Izveidojiet noliktavu.
1. Kopsavilkuma cilnē **Noliktava** iestatiet **Izmantot noliktavas pārvaldības procesus** opciju uz *Jā*.
1. Izveidojiet novietojumus, novietojumu veidus, novietojumu profilus un novietojumu formātus. Lai iegūtu papildu informāciju, skatiet [Konfigurēt novietojumus WMS iespējotā noliktavā](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Izveidojiet vietas, zonas un zonu grupas. Lai iegūtu papildu informāciju, skatiet [Noliktavu iestatīšana](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) un [Konfigurēt novietojumus WMS iespējotā noliktavā](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Iestatīt

### <a name="create-location-directives"></a>Novietojuma direktīvu izveide

Lai izveidotu novietojuma direktīvu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Novietojuma direktīvas**.
1. Saraksta rūtī iestatiet lauku **Darba pasūtījuma veids** uz krājumu darbību tipu, kuram veidojat novietojuma direktīvu.
1. Lai izveidotu novietojuma direktīvu, darbību rūtī atlasiet **Jauns**.
1. Jaunajai novietojuma direktīvai iestatiet laukus, kā aprakstīts sekojošajā tabulā.

    | Lauks | apraksts |
    |---|---|
    | Sērijas numurs | Ievadiet veselu skaitli, kas norāda novietojuma direktīvas secības pozīciju. Secības pozīcijas nosaka, kad katra novietojuma direktīva tiek apstrādāta atlasītajam darba pasūtījuma tipam. |
    | Vārds, uzvārds | Ievadiet novietojuma direktīvas nosaukumu. | 
    | Darba veids | Atlasiet veicamā darba veidu. Vērtību saraksts balstās uz laukā **Darba pasūtījuma tips** atlasītā krājumu transakcijas veidu. Var būt pieejamas šādas vērtības:<ul><li>**Izdošana** – novietojuma direktīva mēģinās atrast labāko vietu, lai izvietotu vai atrastu krājumu, kas nonāk sistēmā, izmantojot saņemšanas, ražošanas vai krājumu korekcijas. Novietojuma direktīva tiek izmantota arī, lai noteiktu izvietošanas novietojumu vai beigu durvju nosūtīšanas vietu izejošajā plūsmā.</li><li>**Saņemšana** – atrašanās vietas direktīva mēģinās atrast labākas vietas, no kurienes fiziski rezervēt krājumus (izveidot darbu). Izdošanu var pabeigt (tas ir, izdošanas darba rindu var slēgt) arī tad, ja darbs nav pabeigts. Lietotājs var veikt fizisku izdošanu. Sistēmā šī darbība ir izdošanas solis. Lietotājs pēc tam var atcelt darbību, izmantojot mobilo ierīci, un pabeigt darbu (piemēram, izdošanu) vēlāk. Tomēr, pabeidzot galīgo izdošanu, pirmais darba virsraksts tiek slēgts.</li><li>**Inventarizācija**, **Korekcijas**, **Muita**, **Krājumu statusa maiņa**, **Unikāla noliktavas vienības identifikatora izveide**, **Drukāšana**, **Statusa maiņa** un **Iepakot ligzdotos unikālos noliktavas vienības identifikatoros** – šīs vērtības nevar izmantot jebkādas vietas direktīvas iestatīšanai.</li></ul> |
    | Vieta | Atlasiet vietu, kurā darbs jāpabeidz. |
    | Noliktava | Atlasiet noliktavas novietojumu, kurā darbs jāpabeidz. |
    | Direktīvas kods | Atlasiet direktīvas kodu, lai virzītu ar darba veidni saistīto novietojuma direktīvu atlasi, ievietojot rindās, kur piešķirts šis kods. Lapā **Direktīvas kods** varat izveidot jaunus kodus, ko var izmantot, lai savienotu darba veidni ar novietojuma direktīvu. Varat izmantot arī lapu starp jebkuras darba veidnes rindas un vietas direktīvas (piemēram, angāra durvis vai sagatavošanas vietas) izveidošanai. Plašāku informāciju par to, kā konfigurēt direktīvas kodu ar darba veidni, skatiet sadaļā [Noliktavas darbu kontrolēšana, izmantojot darba veidnes un novietojuma direktīvas](control-warehouse-location-directives.md).<p>Ja direktīvas kods ir iestatīts, ģenerējot darbu, sistēma meklē vietas direktīvas pēc direktīvas koda, nevis secības. Šādā veidā varat precīzāk norādīt, kāda vietas veidne darba veidnē tiek izmantota konkrētai darbībai, piemēram, materiālu sagatavošana.</p> |
    | Atgriešanas metodes kods | Atlasiet izvietojuma kodu, lai saņemto krājumu izvietošanu novirzītu uz novietojumu. (Papildu informāciju skatiet [Iestatīt izvietojumu kodus](tasks/set-up-dispositions-codes.md).) Šis lauks ir pieejams tikai tad, ja lauks **Darba pasūtījuma tips** ir iestatīts uz *Pirkšanas pasūtījumiem*, *Atgriešanas pasūtījumiem* vai *Pabeigtām precēm*. |
    | Vairākas NV | Iestatiet šo opciju uz *Jā*, lai novietojumā izmantotu vairākas noliktavas vienības (SKU). Piemēram, šai opcijai angāra durvīm ir jābūt iestatītai uz *Jā*.<p>Ja opcija **Vairāki SKU** ir iestatīta uz *Jā*, izdošanas vieta tiks norādīta darbā (kā paredzēts). Tomēr izdošanas atrašanās vieta varēs apstrādāt vairākus elementus tikai tad, ja darbā būs iekļauti dažādi SKU, kas jāsavāc un jāievieto, nevis tad, ja darbs ietver tikai vienu SKU, kas jāievieto.</p><p>Ja opcija **Vairāki SKU** ir iestatīta uz *Nē*, izdošanas vieta tiks norādīta tikai tad, ja izdošana ietver tikai viena veida SKU.</p><p>Lai izmantotu abas pieejas, jānorāda divas rindas ar vienādu struktūru un iestatījumiem, bet ir jāiestata opcija **Vairāki SKU** uz *Jā* vienai no rindām, un *Nē* otrai. Citiem vārdiem sakot, pārdošanas darbībām ir vajadzīgas divas identiskas atrašanās vietas direktīvas, pat ja darba ID jums nav jānošķir vienas un vairākas SKU. Ja jums ir pasūtījums, kas ietver vairāk nekā vienu krājumu, izdošanai ir jāiestata arī atrašanās vietas direktīva.</p><p>**Piezīme.** Ja iestatāt **Vairāki SKU** opciju uz *Jā* *Izdošanas* darba tipa novietojuma direktīvai, sistēma vienmēr atlasīs pirmo novietojuma direktīvas rindu neatkarīgi no citiem rindās izveidotajiem ierobežojumiem.</p> |

1. Nav obligāti: Darbību rūtī atlasiet **Rediģēt vaicājumu**, lai atlasītu novietojumus vai norādītu ierobežojumus, kas ir spēkā, kad atlasāt noteiktu novietojuma direktīvu.
1. Kopsavilkuma cilnē **Rindas** izveidojiet vienu vai vairākas rindas, lai norādītu vienības un novietotu vai rezervētu daudzumu noliktavā.
1. Katrā jaunā rindā iestatiet laukus, kā aprakstīts sekojošajā tabulā.

    | Lauks | apraksts |
    |---|---|
    | Sērijas numurs | Ievadiet veselu skaitli, kas norāda novietojuma direktīvas secības pozīciju. Secības pozīcijas nosaka, kad katra novietojuma direktīva tiek apstrādāta atlasītajam darba tipam. |
    | No daudzuma | Norādiet sākuma daudzuma diapazonu, ja ir jāatlasa vidēja līmeņa režģa secība. Laukā **Vienība** norādiet šim daudzumam izmantojamo mērvienību. |
    | Līdz daudzumam | Norādiet beigu daudzuma diapazonu, ja ir jāatlasa vidēja līmeņa režģa secība. Laukā **Vienība** norādiet šim daudzumam izmantojamo mērvienību. |
    | Vienība | Atlasiet krājumu mērvienību.<p>Varat norādīt minimālo daudzumu un maksimālo daudzumu, uz kuru attiecas direktīva. Var arī norādīt, ka direktīva ir jāizmanto specifiskai krājuma vienībai. **Vienības** lauks tiek izmantots tikai daudzuma novērtēšanai.</p><p>Lai noteiktu, vai ir spēkā novietojuma direktīvas rinda, sistēma novērtē daudzumus, izmantojot **Vienības** vērtību, kas norādīta rindā. Katru reizi, kad piekļūst atrašanās vietas noteikšanas direktīvas rindai, sistēma mēģinās pārveidot pieprasījuma vienību uz rindu norādīto vienību. Ja mērvienību pārvēršana nepastāv, sistēma pārvietosies uz nākamo rindu.</p> |
    | Novietot daudzumu | Šis lauks ir derīgs tikai tad, ja noliktavā tiek mēģināts izdot vai atrast daudzumu. Citiem vārdiem, tas ir derīgs tikai *Izvietošanas* darbiem. Atlasiet metodi, ko izmanto, lai pārbaudītu, vai daudzums atbilst laukos **No daudzuma** un **Līdz daudzumam** iestatītajam diapazonam. Ja novietojuma direktīva ir ienākošajai transakcijai, atlasiet vienu no tālāk norādītajām opcijām:<ul><li>**Noliktavas vienības daudzums** — lai novērtētu, vai daudzums atbilst mērķa daudzuma diapazonam, izmantojiet daudzumu, kas norādīts saņemtajai noliktavas vienībai.</li><li>**Reģistrētais daudzums** — lai novērtētu, vai daudzums atbilst mērķa daudzuma diapazonam, izmantojiet daudzumu, kas tiek reģistrēts transakcijas laikā. Piemēram, ja noliktavā varat saņemt daudzumu 1000 un sadalīt to 10 noliktavas vienībās pa 100 katrā, varat izmantot vienību daudzumu 1000, nevis noliktavas vienību daudzumu 100.</li><li>**Atlikušais daudzums** — lai novērtētu, vai daudzums atbilst mērķa daudzuma diapazonam, izmantojiet atlikušo daudzumu pašlaik pārbaudītajā pirkšanas pasūtījuma rindā.</li><li>**Paredzamais daudzums** — lai novērtētu, vai daudzums atbilst mērķa daudzuma diapazonam laukā “No” un “Uz”, izmantojiet kopējo daudzumu pirkšanas pasūtījuma rindā neatkarīgi no tā daudzuma, kas jau ir saņemts.</li></ul> |

1. Nav obligāti: kopsavilkuma cilnē **Rindas** varat iestatīt tālāk norādītos laukus.

    | Lauks | apraksts |
    |---|---|
    | Ierobežot atbilstoši vienībai | Atzīmējiet šo izvēles rūtiņu, lai ierobežotu mērvienības, kas tiek uzskatītas par derīgiem novietojuma direktīvas rindu atlases kritērijiem. Ja ir norādītas mērvienības, rindas izvēlei par derīgām tiks uzskatītas tikai tās vienības, kurās mērvienība atbilst vismaz vienai vienībai, kas definēta vienību secības grupai.<p>Piemēram, vienība ir ierobežota paletēs, un krājums ir saistīts ar vienību secību grupu, kas ietver *paletes* vienību. Šādā gadījumā vienības tiek uzskatītas par derīgu opciju novietojuma direktīvai.</p><p>Tomēr izvēles rūtiņa **Ierobežot pēc vienības** nekontrolē vienību vai vienības, kas tiek pielietotas darba rindās. Vienības ierobežojums attiecas tikai uz vienībām, kas padarītas pieejamas, izmantojot vienību secību grupu.</p><p>Piemēram, vienība ir saistīta ar vienību secību grupu, kas ietver gan *paletes*, gan *gabalu* vienības. Mērvienības ir definētas, kad 1 palete = 100 gabali, un novietojuma direktīvā tiek izmantota funkcionalitāte **Ierobežot pēc vienības** tikai paletēm. Turklāt ir definēta darba veidne, kas ierobežo darba virsraksta izveidi uz 50 gab. Šādā gadījumā tiks izveidotas darba rindas no 50 gabaliem.</p><p>Lai norādītu ierobežojuma mērvienību, veiciet tālāk norādītās darbības</p><ol><li>Kopsavilkuma cilnē **Rindas** atlasiet **Ierobežot pēc vienības**. Šī poga kļūst pieejama tikai pēc tam, kad rindā esat atlasījis izvēles rūtiņu **Ierobežot pēc vienības** un pēc tam atlasījis **Saglabāt**.</li><li>Laukā **Vienība** atlasiet mērvienību, ar ko ierobežot saņemšanas un izdošanas procesus.</li></ol> |
    | Noapaļot uz augšu līdz vienībai | Atlasiet šo opciju, lai norādītu, ka izejmateriālu izdošana ir jānoapaļo uz augšu līdz laukā **Ierobežot pēc vienības** norādītās materiālu apstrādes vienības reizinājumam. Šis lauks attiecas tikai uz izejmateriālu izdošanu un novietojuma direktīvām, kuru tips ir *Saņemšana*. |
    | Meklēt iepakojuma daudzumu | Atlasiet šo izvēles rūtiņu, ja iepakojuma vienības daudzums ir norādīts lapā **Pārdošanas pasūtījums**. Atzīmējot šo izvēles rūtiņu, tiek atlasīti tikai novietojumi ar šo iepakojuma vienību daudzumu. |
    | Atļaut sadalījumu | Atzīmējiet šo izvēles rūtiņu, lai sadalītu daudzumu pa vairākiem novietojumiem. |
    | Tūlītējas papildināšanas veidne | Izveidojiet savienojumu ar papildināšanas veidni, lai nekavējoties sāktu papildināšanu, ja krājumi nav piešķirti. Ja atstājat šo lauku tukšu, krājumu papildināšana netiks sākta, līdz visas atrašanās vietas direktīvas rindas nebūs apstrādātas.<p>Šis lauks ir pieejams tikai atlasītajos darba pasūtījumu tipos, kur ir atļauta papildināšana, piemēram, *Pārdošanas pasūtījumi* un *Izejmateriālu saņemšana*.</p> |

1. Kopsavilkuma cilnē **Novietojuma direktīvas darbības** atlasiet **Jauns**, lai atlasītu novietojumu vai novietojumu diapazonu.
1. **Sērijas numura** lauks parāda secību, kādā novietojuma direktīva tiks apstrādāta atlasītajam darba tipam. Šo secību varat mainīt. Tomēr esiet piesardzīgs attiecībā uz atrašanās vietas direktīvas darbību secības numuriem, jo novietojuma direktīvas darbības vienmēr tiks izpildītas šajā secībā.
1. Laukā **Nosaukums** ievadiet novietojuma direktīvas darbības nosaukumu. Esiet precīzs, lai būtu saprotams, ar ko darbība ir saistīta.
1. Nav obligāti: Atlasiet **Rediģēt vaicājumu**, lai mainītu noliktavu novietojumus un citus kritērijus.
1. Nav obligāti: novietojuma direktīvai varat iestatīt tālāk norādītos papildu laukus.

    | Lauks | apraksts |
    |---|---|
    | Fiksētā novietojuma lietojums | Atlasiet, kurus novietojumus novietojumu direktīvai ir jāapsver:<ul><li>**Fiksētas un nefiksētas vietas** - vietas direktīva ņem vēra visas vietas.</li><li>**Tikai fiksētas vietas precei** - vietas direktīva ņem vērā precēm tikai fiksētas vietas.</li><li>**Tikai fiksētas vietas preces variantam** - vietas direktīva ņem vērā preces variantiem tikai fiksētas vietas.</li></ul> |
    | Atļaut negatīvu krājumu daudzumu | Atzīmējiet šo izvēles rūtiņu, lai atļautu negatīvus krājumus norādītajā noliktavas novietojumā. |
    | Partija iespējota. | Atzīmējiet šo izvēles rūtiņu, lai lietotu partijas stratēģijas krājumiem, kam ir iespējotas partijas. Ja ir atzīmēta šī izvēles rūtiņa, un **Stratēģijas** lauks ir iestatīts uz *Nav*, sistēma pārvietosies uz nākamo darbības rindu. |
    | Stratēģija | Atlasiet stratēģiju, ko izmantot novietojuma direktīvā:<ul><li>**Nav** – neviena stratēģija netiks izmantota.</li><li>**Saskaņo iepakojuma daudzumu** - šī stratēģija pārbauda, vai saņemšanas vietā ir norādītais iepakojuma daudzums. Šī stratēģija ir derīga tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Saņemt*.</li><li>**Konsolidēt** - šī stratēģija konsolidē krājumus noteiktā vietā, ja jau ir pieejami līdzīgi krājumi. Šī stratēģija ir derīga tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Izdot*. Parastas izdošanas iestatīšanas sistēmā tā mēģina konsolidēt pirmajā darbības rindā un pēc tam otrajā darbības rindā to mēģina izveidot bez konsolidācijas. Preču konsolidēšana padara efektīvāku vēlāku izdošanu.</li><li>**FEFO partijas rezervēšana** - šī stratēģija tiek izmantota, ja krājumi tiek novietoti, izmantojot partijas beigu datumu, un tiek piešķirti partijas rezervācijai. Pirmās beigu termiņa (FEFO) partijas rezervēšanas stratēģija tiek izmantota arī tad, ja krājumi tiek atrasti, papildus beigu datumam izmantojot arī partijas derīguma termiņa datumu. Šo stratēģiju var izmantot tikai krājumiem, kuriem iespējotas partijas. Šī stratēģija ir derīga tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Saņemt*. Kad atlasāt šo stratēģiju, tiek ignorēta visu lietoto partijas numuru vaicājumu kārtošana.</li><li>**Noapaļot uz augšu līdz pilnai NV** - šī stratēģija noapaļo krājumu daudzumu, lai tas atbilstu noliktavas vienību daudzumam, kas ir piešķirts izdodamajiem krājumiem. Šo stratēģiju var izmantot tikai atrašanās vietas direktīvu papildināšanas tipam un tikai tad, ja lauks **Darba veids** ir iestatīts kā *Saņemšana*.</li><li>**Tukša vieta bez ienākoša darba** - šo stratēģiju izmanto, lai atrastu tukšas vietas. Novietojums tiek uzskatīts par tukšu, ja tam nav fizisku krājumu un nav gaidāms ienākošais darbs. Šī stratēģija ir derīga tikai tad, ja **Darba tipa** lauks ir iestatīts uz *Izdot*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Novietojuma direktīvas izmantošanas piemērs

Šajā piemērā ir aprakstīts pirkšanas pasūtījuma process, kur vietas direktīvai ir jāatrod brīva vieta noliktavā krājuma vienībām, kas ir tikko reģistrētas saņemšanas dokā. Vispirms ir jāatrod brīva vieta noliktavā, konsolidējot rīcībā esošos krājumus. Ja konsolidācija nav iespējama, tad ir jāatrod tukša vieta.

Šādā gadījumā ir jādefinē divas vietas direktīvas darbības. Pirmajai darbībai secībā ir jāizmanto stratēģija **Konsolidēt** un otrajai vajadzētu izmantot stratēģiju **Tukšs novietojums bez ienākoša darba**. Ja tiek definēta trešā darbība pārpildes scenārija apstrādei, iespējami divi galarezultāti, kurā noliktavā vairs nav vietas: darbu var izveidot arī tad, ja nav definētas vietas, vai darba izveides process var neizdoties. Rezultātu nosaka iestatījumi lapā **Novietojuma direktīvas kļūmes**, kur varat izlemt, vai atlasīt opciju **Pārtraukt darbu, ja rodas ar novietojuma direktīvu saistīta kļūme** katram darba pasūtījuma tipam.

## <a name="next-step"></a>Nākošais solis

Pēc novietojuma direktīvu izveides katru direktīvas kodu var saistīt ar darba izveides darba veidnes kodu. Papildinformāciju skatiet šeit: [Noliktavas darba kontrolēšana, izmantojot darbu veidnes un novietojuma direktīvas](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Tehniskā informācija sistēmas administratoriem

Ja nevarat piekļūt lapām, kas tiek izmantotas šī uzdevuma izpildīšanai, sazinieties ar sistēmas administratoru un sniedziet nākamajā tabulā redzamo informāciju.

| Kategorija | Priekšnoteikumi |
|---|---|
| Configuration Keys | Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Licences konfigurācija**. Izvērsiet **Tirdzniecības** licences atslēgu un tad atlasiet **Noliktavas un transportēšanas pārvaldības** konfigurācijas atslēgu. |
