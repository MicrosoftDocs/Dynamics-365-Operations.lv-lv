---
title: GS1 svītrkodi
description: Šajā tēmā ir aprakstīts, kā iestatīt GS1 svītrkodus un QR kodus, lai etiķetes varētu skenēt noliktavā.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ea928bc8a020035adb36ae2e7873c656e8c3985d
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625283"
---
# <a name="gs1-bar-codes"></a>GS1 svītrkodi

[!include [banner](../includes/banner.md)]

Lai reģistrētu krājuma, paletes vai konteinera pārvietošanu, izmantojot mobilās ierīces skeneri, noliktavas darbiniekiem bieži ir jāveic vairāki uzdevumi. Šie uzdevumi var ietvert gan svītrkodu skenēšanu, gan informācijas manuālu ievadi mobilajā ierīcē. Svītrkodiem tiek izmantots uzņēmuma formāts, kuru jūs definējat un pārvaldāt, izmantojot Microsoft Dynamics 365 Supply Chain Management.

GS1 svītrkodi nosūtīšanas etiķetēm tika izstrādātas, lai nodrošinātu globālu datu apmaiņas standartu starp uzņēmumiem. Tās ir pieejamas gan lineārās (1D) simbolu (svītrkoda formātos), kā, piemēram, GS1-128, gan 2D symbologies, piemēram, GS1 DataMatrix un GS1 QR kodi. GS1 svītrkodi ne tikai *kodē datus, bet arī ļauj izmantot iepriekš definētu programmas identifikatoru* sarakstu, lai definētu šo datu nozīmi. GS1 standarts definē datu formātu un dažādus datu veidus, ko var izmantot, lai tos kodētu. Atšķirībā no vecāka svītrkoda standarta GS1 svītrkodiem var būt vairāki datu elementi. Tāpēc, veicot vienu svītrkoda skenēšanu, var iegūt vairāku veidu informāciju par produktu, piemēram, partiju un beigu datumu.

GS1 atbalsts Piegādes ķēžu pārvaldībā ievērojami vienkāršo skenēšanas procesu noliktavās, kurās paletes un konteineri ir iezīmēti, izmantojot svītrkodus GS1 formātā. Noliktavas darbinieki var izgūt visu nepieciešamo informāciju, veicot vienu GS1 svītrkoda skenēšanu. Novēršot nepieciešamību veikt vairākas skenēšanas un/vai manuāli ievadīt informāciju, GS1 svītrkodi palīdz samazināt uzdevumu veikšanai nepieciešamo laiku. Tajā pašā laikā tie arī palīdz uzlabot precizitāti.

Loģistikas pārvaldītājiem ir jāiestata nepieciešamais programmas identifikatoru saraksts un katrs no tiem jāsaista ar atbilstošajiem mobilās ierīces izvēlnes elementiem. Programmas identifikatorus pēc tam var izmantot visās noliktavās kā globālo iestatījumu pārvietošanas un iepakošanas nolūkiem. Tāpēc visām nosūtīšanas etiķetēm būs vienota forma.

Ja vien nav norādīts citādi, šai *tēmai* tiek izmantots termins svītrkods, lai atsauktos gan uz lineāriem (1D), gan uz 2D svītrkodiem.

## <a name="the-gs1-bar-code-format"></a>GS1 svītrkoda formāts

GS1 vispārīgās specifikācijas norāda, kurus simbolus var lietot GS1 svītrkodiem un kā šifrēt datus svītrkodā. Šajā sadaļā sniegts īss tēmas ievads. Lai iegūtu pilnīgu informāciju, skatiet [GS1 vispārīgās specifikācijas](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf), ko publicēja GS1. GS1 specifikāciju dokuments tiek regulāri atjaunināts, un informācija, kas to nodrošina, ir atjaunināta ar GS1 vispārējām specifikācijām, izlaidiet 22.0.

GS1 svītrkodos tiek lietoti šādi simboli:

- **Lineāri vai 1D svītrkodi** – GS1-128 un GS1 DataBar
- **2D svītrkodi** – GS1 DataMatrix, GS1 QR kods un GS1 Dotcode

Ievērojiet, ka GS1 ir īpašas norādes GS1-128, kas ir parasta 128. koda lineārā svītrkoda, GS1 DataMatrix un GS1 QR koda īpašais gadījums. Atšķirība starp GS1 versiju un versiju, kas nav GS1, attiecas uz īpašu rakstzīmi (FNC1) kā pirmo rakstzīmi svītrkoda datos. FNC1 rakstzīmes klātbūtne norāda, ka dati svītrkodā jāinterpretē atbilstoši GS1 specifikācijai.

Dati svītrkodā sastāv no vairākiem datu elementiem, no kuriem katrs ir identificēts ar programmas identifikatoru lauka sākumā. Parasti dati zem svītrkoda tiek attēloti arī personas nolasāmā formātā, kur programmas identifikators tiek rādīts iekavās. Tālāk minēts piemērs: `(01) 09521101530001 (17) 210119 (10) AB-123`. Šis svītrkods satur trīs elementus:

- **Programmas identifikators 01** – krājuma GS1 globālās tirdzniecības krājuma numurs (GTIN).
- **Programmas identifikators 17** – beigu datums.
- **Programmas identifikators 10** – partijas numurs.

Katram elementam datiem var būt iepriekš definēts garums vai mainīgs garums. Pastāv fiksēts programmas identifikatoru saraksts, kuriem ir iepriekš definēti garumi. Visiem pārējiem programmas identifikatoriem ir mainīgs garums, un GS1 programmas identifikatoru saraksts norāda datu maksimālo garumu un formātu. Piemēram, programmas identifikatoram 01 ir iepriekš definēts garums 16 rakstzīmes (divas pašas programmas identifikatoram un pēc tam 14 priekš GTIN), un programmas identifikatoram 17 ir iepriekš definēts astoņu rakstzīmju garums (divas pašas programmas identifikatoram un tad seši datumam). Tomēr programmas identifikatoram 10 ir divi numuri pašam programmas identifikatoram un pēc tam līdz 20 burtciparu rakstzīmēm.

Ja elements seko mainīga garuma elementam, jāizmanto atdalītāja rakstzīme. Šis atdalītājs var būt īpaša FNC1 rakstzīme vai grupas atdalītāja rakstzīme (nedrukājama rakstzīme, kam ir ASCII kods 29 un heksadecimālais kods 1D). Atdalītāju nedrīkst izmantot pēc pēdējā elementa. Lai arī atdalītāju nebūtu jāizmanto pēc elementiem, kuriem ir iepriekš definēts garums, tā klātbūtne nav kritiska kļūda.

Svītrkoda datos no iepriekšējā piemēra svītrkodam, kas satur programmas identifikatorus 01, 17 un 10, dati kodam 128, QR kodam vai DataMatrix `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` simbolam tiks iekodēti kā (programmas identifikatori ir parādīti treknrakstā). Saskaņā ar labāko praksi beigās jāliek visi elementi ar mainīgu garumu, lai novērstu papildu grupas atdalītāja rakstzīmes nepieciešamību. Tomēr svītrkodam var būt arī atšķirīga elementu secība, kur atdalītājs ir obligāts. Šeit parādīts piemērs:`<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Datumi un decimāldaļskaitļi

Datumi vienmēr tiek attēloti *GGMMDD* formātā, kur gada gadsimtu nosaka GS1 specifikācijas. Turpmāk var attēlot tikai datumus no 49 gadiem līdz 50 gadiem nākotnē (attiecībā pret pašreizējo gadu).

Daži datu elementi satur decimālskaitļus. Piemēram, programmas identifikatori 3100, 3101, ... 3105 attēlo neto svaru kilogramos. Sakarā ar to, ka šiem programmas identifikatoriem iepriekš definēts garums ir 10, daudzumam ir pieejami seši cipari. Decimāl komata pozīcija ir norādīta pēc programmas identifikatora pēdējā numura. Tāpēc šo programmas identifikatoru saime var tikt attēlota arī kā *310n*. Tā kā GS1 standarts norāda, ka vienmēr ir jābūt vismaz vienam skaitlim pa kreisi no decimālpunkta, ir atļauta ne vairāk kā piecas decimāldaļas vietas.

Daži piemēri, kas parāda, 123456 *numurus* interpretēs dažādi programmas identifikatori (treknrakstā):

- **`3100`**`123456`&rarr; 123456 (vesels skaitlis)
- **`3101`**`123456`&rarr; 12345.6 (viena decimāldaļa)
- **`3102`**`123456`&rarr; 1234,56 (divas decimāldaļas vietas)
- **`3103`**`123456`&rarr; 123.456 (trīs decimāldaļas)
- **`3104`**`123456`&rarr; 12,3456 (četras decimāldaļas vietas)
- **`3105`**`123456`&rarr; 1.23456 (piecas decimāldaļas)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>GS1 svītrkodu skenēšana piegādes ķēžu pārvaldībā

Lai skenētu GS1 svītrkodus, noliktavas darbinieki izmanto skeneri, kas ir iebūvēts mobilajā ierīcē vai ir savienots ar to. Pēc tam skeneris skenēto svītrkodu pārsūta uz mobilo programmu Noliktavas pārvaldība kā tastatūras notikumu sērija. Šis darbības režīms ir zināms arī kā tastatūras *āmais vai* *āmais*. Tad mobilā programma nosūta saņemto tekstu piegādes ķēžu pārvaldībai. Kad sistēma saņem ievades datus, tā vispirms nosaka, vai dati sākas ar vienu no konfigurētajiem prefiksiem, kas norāda, ka dati faktiski ir GS1 svītrkods ([skatiet sadaļu Globālo GS1 opciju](#set-gs1-options) iestatīšana). Ja skenēto datu sākums ir viens no šiem prefiksiem, sistēma izmanto GS1 parsētāju, lai parsēt datus un izgūtu atsevišķus datu elementus atbilstoši to izmantošanas identifikatoriem. Kad dati ir parsēti, pašreizējais ievades lauks vai vairāki lauki tiks aizpildīti ar skenētajiem datiem.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Svītrkodu skenera aparatūras un programmatūras konfigurācija

Lai piegādes ķēdes pārvaldība varētu pareizi atpazīt un atšifrēt GS1 svītrkodus, aparatūras skeneris vai atbalsta programmatūra ir jākonfigurē, lai veiktu šādas darbības:

- Pievienojiet skenētajiem svītrkodiem prefiksu, lai sistēma varētu atpazīt GS1 svītrkodu.
- Konvertējiet nedrukājamo ASCII grupas atdalītāja rakstzīmi (ASCII kods 29 vai heksadecimālais kods 1D) par drukājamu rakstzīmi, piemēram, tiālo (~).

Lai arī skenētajam svītrkodam varat pievienot jebkādu prefiksu, ir viena opcija, lai pievienotu ISO/IEC 15424 simbolu identifikators, kas tiek saukts arī par *GUID identifikatoru*. Šis trīs rakstzīmju identifikators sākas ar `]`, tad tai ir viena rakstzīme, kas identificē izmantoto simbolu, un pēc tam ir numurs, kas tiek izmantots kā vēl viens modifikators. Piemēram, IDENTIFIER identifikators NORĀDA `]C1` kodu 128 svītrkodu (`C` rakstzīmes dēļ) un modifikatoru `1` norāda, ka datu pirmajā pozīcijā ir FNC1 rakstzīme. No otras puses, `]C0` ir koda 128 svītrkods, kuram kā datu pirmajai rakstzīmei ir cits simbols.

Šādi pieci simbolu identifikatori atbilst GS1 svītrkodiem, kam ir programmas identifikatora elementi:

- `]C1`– kods 128 (`C`) ar FNC1 rakstzīmi pirmajā pozīcijā (`1`), zināms arī kā GS1-128.
- `]e0`– GS1 DataBar.
- `]d2`– DataMatrix (`d`) ar ECC 200 un FNC1 pirmajā amatā (`2`), kas pazīstama arī kā GS1 DataMatrix.
- `]Q3`– QR kods (`Q`) 2. modeļa simbols ar FNC1 pirmajā pozīcijā (`3`), zināms arī kā GS1 QR kods.
- `]J1`– GS1 DotCode.

Ja izmantojat šos identifikatorus, saderībai ar svītrkodiem, kas nav GS1, ir nepieciešams, lai skeneri vai skenēšanas programmatūra būtu konfigurēta tā, lai noņemtu visus identifikatorus, kas neatbilst GS1 identifikatoriem. Piemēram, skenot "parastu" koda 39 svītrkodu, prefikss `]A0` tiks pievienots. Tā kā sistēma šo prefiksu nevarēs saprast kā vienu no GS1 prefiksiem, tā interpretēs to kā datus un izveidos neparedzētus rezultātus.

> [!NOTE]
> Lai būtu ērti, 2.0.17.0 noliktavas pārvaldības mobilās programmas versijai un jaunākai versijai tiks noņemti visi PREFIKSI, kas nav ietverti iepriekšējā sarakstā. Šis režīms atbalsta gadījumus, kad skeneri var konfigurēt, lai pievienotu prefiksu MĒRĶIS, bet neizņemt nevajadzīgos prefiksus.

### <a name="single-and-multiple-field-scanning"></a>Viena un vairāku lauku skenēšana

Kad dati ir parsēti no svītrkoda, tie tiks ievadīti mobilās ierīces plūsmas vadīklās. Pastāv divas metodes, kas savukārt tiks apstrādātas:

- **Viena lauka skenēšana** - šī metode aizpilda tikai lauku, kurā svītrkods tika skenēts. Piemēram, ja svītrkodu `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`**skenēsiet**, kamēr kursors atrodas laukā Prece, tad šajā laukā tiks ievadīts GTIN `09521101530001` no svītrkoda. Ja skenēsiet **to pašu svītrkodu, kamēr kursors atrodas laukā Paketes ID**, `AB-123` tiks ievadīts partijas numurs no svītrkoda. Šis režīms darbojas visiem laukiem visās plūsmās un pieprasa konfigurēt tikai GS1 vispārīgo iestatījumu. Ja svītrkodā ir ietverti vairāki elementi, tas joprojām ir jāskenē vairākas reizes, jo vienlaikus mobilās ierīces plūsmā tiks ievadīta tikai viena svītrkoda daļa. Šo darbību kontrolē GS1 vispārējie iestatījumi, kā aprakstīts [vispārējā GS1 iestatījuma sadaļā](#generic-gs1-setup).
- **Vairāku lauku skenēšana** — šī metode aizpilda vairākus laukus, kad tiek skenēts viens svītrkods, virzot papildu datus mobilās ierīces plūsmas stāvoklī. Piemēram, politika ir konfigurēta, lai laukā uz kontroles un programmas identifikatoru 10 iespiež programmas identifikatoru 01`ItemId``InventBatchId`. Šādā gadījumā, ja skenējat svītrkodu `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, dati abiem mainīgajiem tiks vienlaicīgi nospiesti. Tādēļ sistēma nevaicās jums krājuma un/vai partijas numuru plūsmā. Šo darbību kontrolē GS1 politikas, kas ir saistītas ar izvēlnes vienumiem, [kā aprakstīts sadaļā Iestatīt GS1 politikas uz mobilās ierīces izvēlnes vienumiem](#policies-for-menus).

> [!WARNING]
> Noklusējuma GS1 politikas ir testētas uz darbu bez neparedzētas uzvedības. Tomēr GS1 politiku pielāgošana, kas ir saistītas ar izvēlnes elementiem, var izraisīt neparedzētu uzvedību, jo plūsma var neprognozēt noteiktu datu pieejamību konkrētā laikā.

## <a name="turn-on-the-gs1-feature"></a>GS1 līdzekļa iespējošana

Lai varētu izmantot šo līdzekli, sistēmā tas vispirms ir jāiespējo. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu. Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:

- **Modulis:** *Noliktavas pārvaldība*
- **Funkcionalitātes nosaukums:** *Skenēt GS1 svītrkodus*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Ieslēgt uzlaboto parsētāju GS1 svītrkodu funkcijai

Ja izmantojat GS1 svītrkodus, ieteicams iespējot arī *uzlaboto parsētāju GS1 svītrkodu līdzeklim*. Šis līdzeklis nodrošina uzlabotu GS1 svītrkoda parsētāja ieviešanu. Tas pievieno šādus uzlabojumus:

- Atbilstoši specifikācijai GS1 vispārīgās specifikācijas algoritms simbolu datu parsēšana apstiprina, ka dati simbolikā ir derīgi.
- Nav nepieciešams iestatīt maksimālo identifikatoru vērtības **garumu** un izmantot visgarāko prefiksa atbilstību no konfigurētajiem programmas identifikatoriem.
- Tas ļauj vieglāk konfigurēt decimāldaļskaitļu programmas identifikatorus, izmantojot burtu *n*, lai saskaņotu jebkuru skaitli. Piemēram, atsevišķu programmas identifikatoru (3101, 3102 *·* *,* 3103 *u.c.) vietā varat konfigurēt tikai vienu programmas identifikatoru (* *310n*).
- Tā labo problēmu, kad nepareizi šifrēti dati tiek interpretēti kā lauka dati.
- Tā ir atsevišķa klase, kuru var atkārtoti izmantot citos kontekstos un kas ļauj izmantot paplašināmības punktu, lai manipulētu ar skenētajiem datiem pirms plūsmas lauku aizpildīšanas.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>GS1 globālo opciju iestatīšana

Lapā **Noliktavas pārvaldības parametri** sniegti vairaki iestatījumi, kas veido globālās GS1 opcijas.

Lai iestatītu globālās GS1 opcijas, rīkojieties tālāk aprakstītajā veidā.

1. Doties uz **Noliktavas vadība \> Iestatīšana \> Noliktavas vadības parametri**.
1. Kopsavilkuma cilnē **Svītrkodi** iestatiet tālāk minētos laukus.

    - **FNC1 Character**, **Datamatrix character** un **QR koda rakstzīme** – norādiet rakstzīmes, kas jāinterpretē kā prefikss katram GS1 svītrkoda tipam.
    - **Grupu atdalītājs** – norādiet rakstzīmi, kas aizstāj ASCII grupas atdalītāja rakstzīmi.
    - **Identifikatora maksimālais garums** — norādiet maksimālo rakstzīmju skaitu, kas atļauts programmas identifikatoram. Šis lauks nav nepieciešams, ja sistēmā *ir ieslēgta funkcija Uzlabots GS1 Parser*.

> [!NOTE]
> Prefiksi norāda sistēmai, ka svītrkods ir iekodēts atbilstoši GS1 standartam. Vienlaicīgi un dažādiem nolūkiem var izmantot līdz trim prefiksiem (**FNC1 rakstzīme**, **Datu matricas rakstzīme** un **QR koda rakstzīme**).

## <a name="gs1-application-identifiers"></a>GS1 lietojumprogrammas identifikatori

GS1 formāti ne tikai kodē datus, bet arī ļauj izmantot iepriekš definētu programmas identifikatoru sarakstu, lai definētu datu nozīmi. Loģistikas pārvaldītājiem ir jāiestata nepieciešamais programmas identifikatoru saraksts un katrs no tiem jāsaista ar atbilstošajiem mobilās ierīces izvēlnes elementiem. Identifikatorus pēc tam var izmantot visās noliktavās kā globālo iestatījumu pārvietošanas un iepakošanas nolūkiem. Tāpēc visām nosūtīšanas etiķetēm būs vienota forma.

Sistēma izmanto datus, it īpaši iepriekš definētos programmas identifikatorus, lai izveidotu noteikumus, kas jāpiemēro attiecīgajai skenētās informācijai daļai.

Katrs programmas identifikators norāda sistēmai, ka turpmākās rakstzīmes skenētajā svītrkodā jāuzskata par šifrētas informācijas bloku. Pietieikuma identifikatoru iestatījums nosaka, kā sistēmai būtu jāinterpretē svītrkods un jāsaglabā tas kā vērtība sistēmā.

Loģistikas pārvaldītāji var izmantot standarta starptautiskos programmas identifikatorus un/vai izveidot savus.

### <a name="load-the-standard-application-identifiers"></a>Standarta programmas identifikatoru ielāde

Lai ātri sāktu darbu, varat ielādēt kopējo starptautisko programmas identifikatoru sarakstu. Pēc tam sarakstu pēc nepieciešamības vēlāk var paplašināt vai rediģēt.

Lai ielādētu standarta programmas identifikatorus, veiciet tālāk minētās darbības.

1. Atveriet **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 programmas identifikatori**.
1. Darbību rūtī atlasiet **Izveidot noklusējuma iestatījumus**.

> [!WARNING]
> Ar komandu **Izveidot noklusējuma iestatījumus** tiek dzēsti visi pašlaik definētie programmas identifikatori un tie tiek aizstāti ar standarta sarakstu. Taču pēc noklusējuma iestatījumu ielādes varat pielāgot sarakstu pēc nepieciešamības.

### <a name="set-up-custom-application-identifiers"></a>Pielāgoto programmas identifikatoru iestatīšana

Ja daži vai visi jūsu uzņēmuma izmantotie programmas identifikatori atšķiras no standarta kopas, varat izveidot savus kodus no nulles vai pielāgot standarta kopu pēc nepieciešamības.

Lai iestatītu un pielāgotu savus GS1 programmas identifikatorus, veiciet tālāk minētās darbības.

1. Atveriet **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 programmas identifikatori**.
1. Izpildiet kādu no šīm darbībām:

    - Lai izveidotu jaunu isentifikatoru: darbību rūtī atlasiet **Jauns**.
    - Lai rediģētu esošu identifikatoru: atlasiet identifikatoru un pēc tam darbību rūtī atlasiet **Rediģēt**.

1. Iestatiet jaunajam vai atlasītajam identifikatoram tālāk norādītos laukus.

    - **Programmas identifikators** — ievadiet programmas identifikatora identifikācijas kodu. Parasti šis kods ir divciparu vesels skaitlis, bet tas var būt arī garāks. Decimālskaitļu vērtībām pēdējais cipars norāda decimāldaļu vietu skaitu. Papildinformāciju skatiet tālāk šī saraksta izvēles rūtiņas **Decimāldaļas** aprakstā. *Ja ir iespējota funkcija Uzlabotais parsētājs* GS1 svītrkodiem, varat izveidot vienu programmas identifikatoru visiem decimāldaļu vietas variantiem *, kā pēdējo rakstzīmi izmantojot burtu n* programmas identifikatorā. Piemēram, jūs varat konfigurēt tikai vienu programmas identifikatoru (*310n*), nevis atsevišķu programmas identifikatoru katram decimāldaļu skaitam (*3101*, *3102*, *3103* utt.).
    - **Apraksts** — ievadiet īsu identifikatora aprakstu.
    - **Fiksēts garums** — atlasiet šo izvēles rūtiņu, ja vērtībām, kas tiek skenētas, izmantojot šo programmas identifikatoru, ir fiksēts rakstzīmju skaits. Ja vērtību garums ir mainīgs, notīriet šo izvēles rūtiņu. Šajā gadījumā jānorāda vērtības beigas, izmantojot grupas atdalītāja rakstzīmi, ko norādījāt lapā **Noliktavas pārvaldības parametri**.
    - **Garums** — ievadiet maksimālo rakstzīmju skaitu, kas var tikt parādīts vērtībām, kas tiek skenētas, izmantojot šo programmas identifikatoru. Ja ir atlasīta izvēles rūtiņa **Fiksēts garums**, ir paredzēts tieši šis rakstzīmju skaits.
    - **Veids** — atlasiet to vērtības veidu, kas tiek skenēts, izmantojot šo programmas identifikatoru (*Skaitlisks*, *Burtciparu* vai *Datums*). Papildinformāciju par to, kā datumi un numuri tiek attēloti svītrkoda datos, skatiet sadaļā [Datumi un decimāldaļskaitļi](#dates-and-decimal-numbers).
    - **Decimāls** — atlasiet šo izvēles rūtiņu, ja vērtība ietver fiksētu decimālpunktvietu. Ja ir atzīmēta šī rūtiņa, sistēma izmantos programmas identifikatora pēdējo ciparu, lai noteiktu decimāldaļskaitļu skaitu. Papildinformāciju par to, kā datumi un numuri tiek attēloti svītrkoda datos, skatiet sadaļā [Datumi un decimāldaļskaitļi](#dates-and-decimal-numbers).

> [!WARNING]
> Kaut arī sistēma ļaus iestatīt izvēles rūtiņu Fiksēts garums jebkuram programmas identifikatoram, tas **jālieto** tikai to programmas identifikatoru apakškopai, kuriem ir iepriekš definēts garums uz GS1 vispārējām specifikācijām. Uzlabotais GS1 parsētājs jau ietver visu programmas identifikatoru sarakstu, kam ir iepriekš definēti garumi.

> [!NOTE]
> Noliktavas **pārvaldības parametru** lapā norādītā grupas **atdalītāja** vērtība nav obligāta, ja vērtībai, kam seko programmas identifikators, ir fiksēts garums.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Vispārīgo GS1 iestatījumu izveide

Vispārīgie GS1 iestatījumi izveido kopējo kartējumu kolekciju. Šie kartējumi atbilst katram atbilstošajam mobilās programmas ievades laukam ar programmas identifikatoru, kas nosaka, kā šajā laukā ir jāinterpretē un jāglabā skenēto svītrkodu vērtības. Pēc noklusējuma šie iestatījumi attiecas uz visu mobilās ierīces izvēlnes elementu skenēšanu. Tomēr tos var pārrakstīt vienam vai vairākiem konkrētiem laukiem ar GS1 politiku, kas piešķirta konkrētam izvēlnes elementam.

Vispārīgie GS1 iestatījumi ļauj vienlaikus skenēt tikai vienu vērtību. Tādēļ, ja vēlaties ielādēt vairākas lauku vērtības no vienas skenēšanas, atbilstošajiem izvēlnes elementiem ir jāiestata GS1 politika.

Plašāku informāciju par GS1 politikām skatiet nākamajā sadaļā.

### <a name="load-the-standard-generic-gs1-setup"></a>Standarta vispārīgo GS1 iestatījumu ielāde

Lapā **GS1 vispārīgie iestatījumi** varat ielādēt standarta kartējumu kopu starp mobilās ierīces laukiem un standarta programmas identifikatoriem, kas tiek izveidoti ar noklusējuma iestatījumu.

Lai izveidotu vispārīgus GS1 iestatījumus, atveriet sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 vispārīgie iestatījumi**. Pēc tam atlasiet **Izveidot noklusējuma iestatījumus**, lai automātiski piešķirtu piemērotu programmas identifikatoru katram laukam, ko parasti izmanto mobilās ierīces izvēlnes elementi.

> [!WARNING]
> Ja jau pastāv kādi vispārīgi GS1 iestatījumi, komanda **Izveidot noklusējuma iestatījumus** tos pilnībā izdzēš un ielādē standarta iestatījumus.

### <a name="customize-the-standard-generic-gs1-setup"></a>Standarta vispārīgo GS1 iestatījumu pielāgošana

Lai pielāgotu vispārīgos GS1 iestatījumus, veiciet tālāk minētās darbības.

1. Atveriet sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 vispārīgi iestatījumi**.
1. Izpildiet kādu no šīm darbībām:

    - Lai izveidotu jaunu kartējumu: darbību rūtī atlasiet **Jauns**.
    - Lai rediģētu esošu kartējumu: atlasiet kartējumu un pēc tam darbību rūtī atlasiet **Rediģēt**.

1. Iestatiet jaunajam vai atlasītajam kartējumam tālāk norādītos laukus.

    - **Lauks** — atlasiet vai ievadiet mobilās programmas ievades lauku, kam jāpiešķir ienākošā vērtība. Vērtība nav parādāmais nosaukums, ko redz darbinieki. Tā vietā tas ir atslēgas nosaukums, kas piešķirts pamatā esošā koda laukam. Noklusējuma iestatījumi nodrošina lauku, kas, iespējams, būs noderīgi, apkopojumu un ietver intuitīvus atslēgas nosaukumus katram laukam un atbilstošu programmētu funkcionalitāti. Tomēr, iespējams, jums būs jārunā ar saviem izstrādes partneriem, lai atrastu pareizo izvēli ieviešanai.
    - **Programmas identifikators** — atlasiet piemērojamo programmas identifikatoru, kā definēts lapā **GS1 programmas identifikatori**. Identifikators nosaka, kā svītrkods tiks interpretēts un saglabāts kā nosauktā lauka vērtība. Pēc programmas identifikatora atlases laukā **Apraksts** ir redzams tā apraksts.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a> Iestatīt GS1 politikas attiecībā uz mobilās ierīces izvēlnes vienumiem

GS1 standarta mērķis ir ļaut darbiniekiem ielādēt vairākas vērtības, skenējot vienu svītrkodu vienu reizi. Lai sasniegtu šo mērķi, loģistikas vadītājiem ir jāiestata GS1 politikas, kas paziņo sistēmai, kā interpretēt vairāku vērtību svītrkodus. Vēlāk varat piešķirt politikas mobilās ierīces izvēlnes elementiem, lai kontrolētu, kā svītrkods tiek interpretēts, kad darbinieki to skenē, izmantojot noteiktu izvēlnes elementu.

Ja izvēlnes elementam nav piešķirta GS1 politika, sistēma var tvert tikai vienu vērtību. Šī vērtība tiek piemērota mobilās programmas ievadei, kas tiek atlasīta, kad darbinieks veic skenēšanu, kā norādīts vispārīgajos GS1 iestatījumos. Ja izvēlnes elementam ir piešķirta GS1 politika, sistēma joprojām izmanto vispārīgos GS1 iestatījumus, lai kartētu pirmo svītrkoda vērtību uz atlasīto lauku. Tomēr pēc tam tā var tvert papildu lauka vērtības, kā norādīts piemērojamajā politikā.

### <a name="load-the-standard-specific-gs1-policies"></a>Standarta specifisko GS1 politiku ielāde

Lai ātri sāktu darbu, varat ielādēt GS1 politiku kopu. Pēc tam politikas pēc nepieciešamības vēlāk varat paplašināt vai rediģēt.

Lai ielādētu standarta programmas identifikatorus, veiciet tālāk minētās darbības.

1. Dodieties uz sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 politika**.
1. Darbību rūtī atlasiet **Izveidot noklusējuma iestatījumus**.

> [!WARNING]
> Ar komandu **Izveidot noklusējuma iestatījumus** tiek dzēstas visas pašlaik definētās politikas un tās tiek aizstātas ar standarta politiku kopu. Taču pēc noklusējuma iestatījumu ielādes varat pielāgot politikas pēc saviem ieskatiem.

### <a name="set-up-custom-specific-gs1-policies"></a>Pielāgotu GS1 politiku iestatīšana

> [!WARNING]
> Dažas GS1 politikas var nedarboties ar katru lietoto mobilo plūsmu. Konfigurējot pielāgotās GS1 politikas, ir jāpārbauda mobilās ierīces plūsma, izmantojot dažādus informācijas gabalus, kas tiek skenēti dažādos plūsmas punktos. Šādā veidā varat noteikt, vai plūsma ir nepieciešama.

Lai iestatītu un pielāgotu GS1 politikas, izpildiet tālāk norādītās darbības.

1. Dodieties uz sadaļu **Noliktavas pārvaldība \> Iestatījumi \> GS1 \> GS1 politika**.
1. Izpildiet kādu no šīm darbībām:

    - Lai izveidotu jaunu politiku: darbību rūtī atlasiet **Jauns**.
    - Lai rediģētu esošu politiku: atlasiet politiku saraksta rūtī.

1. Jaunās vai atlasītās politikas galvenē iestatiet tālāk norādītos laukus.

    - **Politikas nosaukums** — ievadiet politikas nosaukumu.
    - **Apraksts** — ievadiet politikas īsu aprakstu.

1. Kopsavilkuma cilnē zem galvenes kartējiet lauku nosaukumus uz programmas identifikatoriem, kā tas nepieciešams pašreizējai politikai. Izmantojiet pogas rīkjoslā, lai pēc nepieciešamības pievienotu vai noņemtu rindas. Katrā rindā iestatiet tālāk norādītos laukus:

    - **Lauks** — atlasiet vai ievadiet mobilās programmas ievades lauku, kam jāpiešķir ienākošā vērtība. Vērtība nav parādāmais nosaukums, ko redz darbinieki. Tā vietā tas ir atslēgas nosaukums, kas piešķirts pamatā esošā koda laukam. Noklusējuma iestatījumi nodrošina lauku, kas, iespējams, būs noderīgi, apkopojumu un ietver intuitīvus atslēgas nosaukumus katram laukam un atbilstošu programmētu funkcionalitāti. Tomēr, iespējams, jums būs jārunā ar saviem izstrādes partneriem, lai atrastu pareizo izvēli ieviešanai.
    - **Programmas identifikators** — atlasiet piemērojamo programmas identifikatoru, kā definēts lapā **GS1 programmas identifikatori**. Identifikators nosaka, kā svītrkods tiks interpretēts un saglabāts kā nosauktā lauka vērtība. Pēc programmas identifikatora atlases laukā **Apraksts** ir redzams tā apraksts.
    - **Kārtošana** — katrs vairāku vērtību svītrkods ietver programmas identifikatoru sērijas, un katram no tiem seko vērtība. Piemērojamā GS1 politika identificē, kurš programmas identifikators tiek kartēts uz katru datu bāzes lauku. Tomēr, ja svītrkods izmanto vienu un to pašu programmas identifikatoru vairāk nekā vienu reizi, sistēma izmanto secību, kādā programmas identifikatori tiek parādīti kodā, lai tos kartētu uz laukiem. Rindām, kurām ir kopīgs programmas identifikators ar vienu vai vairākām citām rindām, izmantojiet šo lauku, lai izveidotu secību, kādā tiek apstrādātas atbilstošās rindas. Vispirms tiks apstrādāta rinda ar zemāko kārtošanas vērtību.

> [!NOTE]
> Svītrkodiem, kas ietver vairāk nekā vienu identisku programmas identifikatoru, lai izveidotu lauku secību *obligāti* jāizmanto lauks **Kārtošana**.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1 politiku piešķire mobilās ierīces izvēlnes elementiem

Pēc noklusējuma visi mobilās ierīces izvēlnes elementi nodrošina ievades laukus, kur darbinieki var skenēt vienu vērtību atbilstoši vispārīgajiem GS1 iestatījumiem. Ja vēlaties, lai darbinieki varētu skenēt vairākas lauka vērtības vienā skenēšanā jebkuram mobilās ierīces izvēlnes elementam, ir jāpiešķir GS1 politika, veicot tālāk norādītās darbības.

1. Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.
1. Izveidojiet vai atveriet izvēlnes elementu.
1. Kopsavilkuma cilnē **Vispārīgi** iestatiet lauku **GS1 politika** uz politiku, kas attiecas uz izvēlnes elementu.

## <a name="gs1-setup-example"></a>GS1 iestatījumu piemērs

Šis piemērs attiecas uz sistēmu, kur GS1 opcijas ir iestatītas tālāk norādītajā veidā.

- Lapā **Noliktavas pārvaldības parametri** ir noteikti tālāk norādītie globālie iestatījumi.

    - **FNC1 rakstzīme:** *\]C1*
    - **Grupu atdalītājs:** *\~*

- Lapā **GS1 programmas identifikatori** uz šo piemēru attiecas tālāk norādītie programmas identifikatori.

    | Pieteikuma identifikators | Apraksts | Fiksētais garums | Ilgums | tips | Decimāldaļskaitlis |
    |---|---|---|---|---|---|
    | 01 | GTIN | Atlasītās | 14. | Skaitlisks | Nodzēsts |
    | 10. | Paketes numurs | Nodzēsts | 20 | Burtciparu | Nodzēsts |
    | 17 | Derīguma beigu datums | Atlasītās | 6 | Datums | Nodzēsts |
    | 30 | Daudzuma saņemšana | Nodzēsts | 8 | Skaitlisks | Nodzēsts |

- Lapā **GS1 vispārīgie iestatījumi** uz šo piemēru attiecas tālāk norādītie vispārīgās GS1 politikas iestatījumi.

    | Lauks | Pieteikuma identifikators | Apraksts |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Lapā **GS1 politika** ir politika, kur lauks **Politikas nosaukums** ir iestatīts uz *Pirkuma saņemšana*. Šajā politikā ir ietvertas tālāk norādītās rindas.

    | Lauks | Pieteikuma identifikators | Apraksts | Kārtošana |
    |---|---|---|---|
    | ExpDate | 17 | Derīguma beigu datums | 0 |
    | InventBatchId | 10. | Paketes numurs | 0 |
    | Daudz. | 30 | Daudzuma saņemšana | 0 |

- Lapā **Mobilās ierīces izvēlnes elementi** ir izvēlnes elements ar nosaukumu *Pirkuma saņemšana*. Tā lauks **GS1 politika** ir iestatīts uz *Pirkuma saņemšana*.

Kad pirkšanas pasūtījuma preces tiek piegādātas noliktavā, darbinieks veic tālāk norādītās darbības.

1. Mibilajā ierīcē atlasiet izvēlnes elementu **Pirkuma saņemšana**.
1. Ievadiet pirkšanas pasūtījuma numuru.
1. Atlasiet lauku **Prece** un skenējiet šādu svītrkodu: `]C10100000012345678~3030~10b1~17220215`

Ņemot vērā šim piemēram izveidotos iestatījumus, sistēma parsē skenēto svītrkodu tālāk aprakstītajā veidā.

| Lauka atslēga | Lietojumprogrammas ID | Vērtība | Piezīme |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Tā kā darbinieks veica skenēšanu uz lauku **Krājums**, pirmā svītrkoda vērtība tiek kartēta uz šo lauku. Kartēšana tiek ņemta no GS1 vispārīgajiem iestatījumiem. |
| Daudz. | 30 | 30 | Tā kā vienā skenēšanā tiek tvertas vairākas lauka vērtības, šis kartējums un visi atlikušie kartējumi tiek ņemti no GS1 politikas, kas piešķirta izvēlnes elementam **Pirkumu saņemšana**. Šī vērtība ir saņemtais daudzums. |
| InventBatchId | 10. | b1 | Šī vērtība ir partijas ID. |
| ExpDate | 17 | 220215 | Datuma formāts ir GGMMDD. Tāpēc termiņa beigu datums ir 2022. gada 15. februāris. |

Pēc tam kvīts tiek reģistrēta, un attiecīgās datu bāzes vērtības tiek ievadītas pēc vienas skenēšanas.
