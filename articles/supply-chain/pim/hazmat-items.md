---
title: Bīstamie materiāli precēs, pasūtījumos, sūtījumos un kravās
description: Šajā tēmā skaidrots, kā iestatīt bīstamas materiālu īpašības izlaistām precēm, kā likt krājumu ierobežojumus bīstamām precēm un kā iekļaut bīstamos materiālus pārdošanas pasūtījumā, sūtījumā vai kravā.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7e0564802bc53ce21236ffc6ed065bf6abac7c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243157"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Bīstamie materiāli precēs, pasūtījumos, sūtījumos un kravās

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā skaidrots, kā iestatīt bīstamas materiālu īpašības izlaistām precēm, kā likt krājumu ierobežojumus bīstamām precēm un kā iekļaut bīstamos materiālus pārdošanas pasūtījumā, sūtījumā vai kravā.

## <a name="set-hazardous-material-specifications-for-products"></a>Iestatīt bīstamo materiālu specifikācijas precēm

Pēc tam, kad esat definējis bīstamo materiālu regulējumu un iestatījis saistītos atsauces kodus, kā aprakstīts sadaļā [Iestatīt bīstamos materiālus](hazmat-setup.md), varat saistīt šo informāciju ar izlaistajiem krājumiem. Nosūtījuma dokumentu sūtīšanas teksts tiks izrakstīts no bīstamo materiālu informācijas par nodotajiem krājumiem.

Kā daļa no nodotā krājuma saistīšanas ar bīstamu materiālu, ir jānorāda Regulas kods un materiāls. Dažādi regulējošie kodi var būt saistīti ar krājumu atkarībā no transporta veida, un katru krājumu var saistīt ar vairākiem regulējumiem un materiālu kodiem.

Lai iestatītu izlaisto preci kā bīstamu materiālu, sekojiet šiem soļiem.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet vai izveidojiet preci, lai atvērtu tās lapu **Izlaisto preču detalizēta informācija**.
1. Kopsavilkuma cilnē **Pārvaldīt krājumu** iestatiet opciju **Bīstams materiāls** uz **Jā**. Šis iestatījums identificē krājumu kā bīstamu preci un tiek izmantots, drukājot piegādes dokumentāciju.
1. Grupas **Saderība** cilnes **Pārvaldīt krājumus** darbību rūtī atlasiet vienumu **Bīstamā materiāla vienība**.
1. Aizpildiet izvēlētā vienuma **Bīstamo materiālu vienība**, izmantojot laukus, kas aprakstīti šādās apakšsadaļās.

### <a name="item-hazardous-materials-header"></a>Bīstamo materiālu vienības galvene

Sekojošajā tabulā ir aprakstīti lauki, kas ir pieejami lapas **Bīstamo materiālu vienums** augšpusē.

| Lauks | Apraksts |
|---|---|
| Krājums | Izlaistā prece, ar kuru strādājat. |
| Noteikumu kods | Atlasiet bīstamo materiālu regulu, kas attiecas uz preci. Regula nosaka, kā drukāto sūtīšanas tekstu izveido krājumam un saistītajiem piegādes veidiem. Pēc piešķiršanas kodu nevar rediģēt šajā lapā. Tomēr jaunu regulu kodu var piešķirt, atlasot **Jauns**. |
| Materiāla kods | (Pēc izvēles) Atlasiet bīstamo materiālu kodu, kas attiecas uz preci. Materiāla kods nodrošina veidni, kas ietver noklusētās vērtības daudziem citiem šīs lapas laukiem. Kad atlasāt kodu, visas tā bīstamo materiālu specifikācijas tiks kopētas uz pašreizējo preci. Tomēr sistēma vispirms piedāvā apstiprināt, ka krājuma materiālu dati ir jāaizpilda no materiālu koda. |
| Grupas kods | (Pēc izvēles) Atlasiet bīstamo materiālu klasifikācijas grupas kodu, kas attiecas uz preci. Kas attiecas uz **Materiāla koda** lauku, kad atlasāt kodu, visas tā bīstamo materiālu specifikācijas tiks kopētas uz pašreizējo preci. Tomēr sistēma vispirms piedāvā apstiprināt, ka krājuma klases grupas dati ir jāaizpilda no grupas koda. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Aprakstu kopsavilkuma cilne

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Aprakstu** kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Pareizais kravas nosaukums | Ievadiet materiāla standarta aprakstu, kā norādīts atbilstošajā regulā. Varat nodrošināt tulkojumus šai vērtībai **Krājumu nosūtīšanas teksta tulkojuma** kopsavilkuma cilnē, kā aprakstīts nākamajā sadaļā. |
| Tehniskais nosaukums | Atlasiet materiāla parasto vai vispārīgo nosaukumu. Šis nosaukums varētu būt nosaukums, ko uzņēmums izmanto iekšēji materiālam. |
| N.O.S. | Atzīmējiet šo izvēles rūtiņu, lai norādītu, ka **Pareizā nosūtīšanas nosaukuma** vērtība ir necitādi specifisks (N.O.S.) nosūtīšanas nosaukums krājumam. N.O.S. sūtījumu nosaukumi tiek izmantoti līdzīgu ķīmisko vielu un materiālu grupām, kurām ir īpašs galīgais lietojums, bet kas, iespējams, nav uzskaitīti pēc nosaukuma bīstamo materiālu tabulā īpašā regulā. |

### <a name="item-ship-text-translation-fasttab"></a>Vienības sūtījuma teksta tulkojuma kopsavilkuma cilne

**Vienības sūtījuma teksta tulkojuma** kopsavilkuma cilne ietver režģi, kas parāda **Pareizu sūtīšanas nosaukumu** vērtību tulkojumus, kas ir definēti primārajai valodai **Aprakstu** kopsavilkuma cilnē. Šos tulkojumus var izmantot nosūtīšanas izdrukas tekstu vienai vai vairākām papildu valodām.

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Vienības sūtījuma teksta tulkojuma** kopsavilkuma cilnē.


| Lauks | Apraksts |
|---|---|
| Valoda | Valodas kods, ko izmanto rinda. Piemēram, **pt-br** norāda Brazīlijas portugāļu. |
| Sūtījuma apdrukas teksts | Pārtulkotā **Pareizā nosūtīšanas nosaukuma** vērtība valodā, ko izmanto rinda. |

Lai pievienotu vai rediģētu tulkojumu, izvēlieties **Tulkojumi** virs režģa, lai atvērtu **Teksta tulkojumu** lapu. Pēc tam izpildiet kādu no norādītajām darbībām.

- Lai pievienotu jaunu tulkojumu, darbību rūtī atlasiet **Pievienot**. Atlasiet pievienojamo valodu un pēc tam laukā **Tulkotais teksts** ievadiet tulkoto tekstu.
- Lai rediģētu esošu tulkojumu, atlasiet mērķa valodu laukā **Valoda** un rediģējiet tulkoto tekstu laukā **Tulkotais teksts** pēc nepieciešamības.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Materiālu pārvaldības kopsavilkuma cilne

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Materiālu pārvaldības** kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Klase | Atlasiet bīstamo materiālu klasi, kurai pieder produkts, kā noteikts regulā, kurai jūs atbilstat. Katrai precei, kurā ir bīstami materiāli, ir jāpiešķir gan dalījums, gan klase. |
| Apraksts | Apraksts, kas definēts klasei, kas atlasīta laukā **Klase**. Šis lauks ir tikai lasāms. |
| Nodaļa | Atlasiet bīstamo materiālu nodaļu, kurai pieder produkts, kā noteikts regulā, kurai jūs atbilstat. Dalījums ir klases apakškopa. Katrai precei, kurā ir bīstami materiāli, ir jāpiešķir gan dalījums, gan klase. |
| Identifikācija | Atlasiet bīstamo materiālu identifikācijas kodu. Parasti šis kods ir balstīts uz Apvienoto Nāciju organizācijas (ANO) standartu. |
| Iepakojuma grupa | Atlasiet iepakojuma grupu, kas attiecas uz pašreizējo krājumu. |
| Apraksts | Apraksts, kas definēts grupai, kas atlasīta laukā **Iepakojuma grupa**. Šis lauks ir tikai lasāms. |
| Iepakojumu apraksti | Atlasiet attiecīgo iepakojuma apraksta kodu. Šis kods atsaucas uz aprakstu, kas norāda, kā produkts ir jāiepako. |
| Bīstamo materiālu etiķetes | Atlasiet kodu, kas norāda piemērojamo bīstamo preču etiķeti, kas jāpiemēro precei. |
| Ierobežots daudzums | Iestatiet šo opciju kā **Jā**, lai paziņotu kopējo preču svaru, kas iekļauts katrā kravā un katrā kravas līnijā. |
| Daudzums | Ievadiet preces bīstamā materiāla daudzumu norādītajā vienībā. Šī vērtība tiks izmantota, lai aprēķinātu kopējo bīstamo materiālu punktu skaitu kravām un kravām, kas ietver preci. |
| Reizinātājs | Ievadiet reizinātāju, kas tiek izmantots, ja bīstamā materiāla rezultāts tiek aprēķināts katrai kravas rindai, kas ietver preci. Šī vērtība ir noteikta, izmantojot piemērojamo regulu, saskaņā ar precē ietvertā bīstamā materiāla tipu. |
| Vienība | Atlasiet mērvienību, kas attiecas uz preces bīstamā materiāla daudzumu, kā norādīts laukā **Daudzums**. Šī vērtība tiks izmantota, lai aprēķinātu kopējo bīstamo materiālu punktu skaitu kravām un kravām, kas ietver preci. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Kā tiek aprēķināts bīstamā materiāla rezultāts

Vairākas no vērtībām, kas norādītas preces **Materiālu pārvaldības** kopsavilkuma cilnē, tiek izmantotas, lai aprēķinātu *bīstamā materiāla rezultātu* katrai kravas rindai, kas iekļauj šo preci. Rezultāts tiek aprēķināts, izmantojot šādu formulu:

Bīstamā materiāla rezultāts = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Šeit ir formulas atslēga:

- *&lt;LineQty&gt;* ir preču daudzums, kas norādīts kravas rindai.
- *&lt;HazmatQty&gt;* ir bīstamā materiāla daudzums, kas ir norādīts precei laukā **Daudzums** kopsavilkuma cilnē **Materiālu pārvaldība**.
- *&lt;UnitConversion&gt;* ir pārveidošanas koeficients, kas tiek izmantots, lai konvertētu no vienības, kas tiek izmantota kravas rindas daudzumam, un vienību, kas noteikta precei laukā **Vienība** kopsavilkuma cilnē **Materiālu pārvaldība**.
- *&lt;Multiplier&gt;* ir reizinātājs, kas ir norādīts precei laukā **Reizinātājs** kopsavilkuma cilnē **Materiālu pārvaldība**.

Šis rezultāts tiek paziņots katrai kravas rindai, kas satur preci, kurā ir norādītas šīs vērtības. Lai iegūtu papildu informāciju, skatiet [Sūtījumi, kuros ir ietverti bīstami materiāli](#hazmat-shipments) un [Kravas, kas iekļauj bīstamos materiālus](#hazmat-loads) šīs tēmas turpinājumā.

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Kā tiek aprēķināts bīstamā materiāla svars

Noslodzes un noslodzes rindas, kas satur preces, kurās **Ierobežotā daudzuma** opcija kopsavilkuma cilnē **Materiālu pārvaldība** ir iestatīta uz **Jā**, parādīs kopējo bīstamo materiāla svaru, kā aprakstīts [Sūtījumi, kas ietver bīstamus materiālus](#hazmat-shipments) un [Noslodzes, kas iekļauj bīstamus materiālus](#hazmat-loads) šīs tēmas turpinājumā. Bīstamā materiāla svars tiek aprēķināts, izmantojot šādu formulu:

Bīstamā materiāla svars = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Šeit ir formulas atslēga:

- *&lt;LineQty&gt;* ir preču daudzums, kas norādīts kravas rindai.
- *&lt;ProductWeight&gt;* ir neto svars, kas norādīts precei krājuma uzskaites vienībā, kas norādīta precei.
- *&lt;UnitConversion&gt;* ir konversijas koeficients konvertēšanai starp vienību, kas tiek izmantota kravas rindas daudzumam un krājumu uzskaites vienību, kas tiek izmantota *&lt;ProductWeight&gt;*.

### <a name="transport-information-fasttab"></a>Informācija par transportu kopsavilkuma cilne

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Transportēšanas informācija** kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Transportēšanas kategorija | Atlasiet saistīto transportēšanas kategoriju. |
| Tuneļa kods | Atlasiet krājuma saistīto tuneļa ierobežojuma kodu. |
| Bīstamo materiālu glabātuve | Atlasiet atsauces kodu, kas tiek izmantots jūras kravas kraušanas apstrādei, kad krājums tiek nosūtīts ar jūras transportu. |
| Gaisa kuģa veids | Atlasiet lidaparāta ierobežojumu, kas attiecas uz materiālu, kad tas tiek nosūtīts ar gaisa transportu. |
| Iesaiņošana — tikai kravas lidmašīnas | Balstoties uz vērtību, ko izvēlējāties laukā **Lidmašīnas tips**, atlasiet iepakošanas instrukcijas kodu, kas tiek lietots, kad preci var nosūtīt tikai kravas lidmašīnas. |
| Iesaiņošana — pasažieru un kravas lidmašīnas | Balstoties uz vērtību, ko izvēlējāties laukā **Lidmašīnas tips**, atlasiet iepakošanas instrukcijas kodu, kas tiek lietots, kad preci var nosūtīt vai nu kravas lidmašīnas, vai pasažieru lidmašīnas. |
| IATA Star | Iestatiet šo opciju kā **Jā**, lai norādītu, ka šajā kopsavilkuma cilnē ievadītās gaisa satiksmes specifikācijas ir saistītas ar Starptautisko gaisa transporta asociācijas (IATA) bīstamo preču standartu. Šis lauks ir paredzēts tikai informatīviem nolūkiem. |
| Ārkārtas reaģēšana | Atlasiet kodu, kas atsaucas uz instrukcijām, kā rīkoties ar materiālu ārkārtas gadījumos. |

### <a name="environmental-information-fasttab"></a>Vides informācijas kopsavilkuma cilne

Tālāk esošajā tabula apraksta laukus, kas ir pieejami **Vides informācijas** kopsavilkuma cilnē.

| Lauks | Apraksts |
|---|---|
| Videi bīstams | Iestatiet šo opciju uz **Jā**, lai norādītu, ka prece ir bīstama videi. Lietojiet šo lauku saviem pārskatu nolūkiem. |
| Jūras piesārņotājs | Iestatiet šo opciju uz **Jā**, lai norādītu, ka prece ir jūras piesārņotājs. Lietojiet šo lauku saviem pārskatu nolūkiem. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Iestatīt bīstamo preču krājumu ierobežojumus

Drošības apsvērumu dēļ, iespējams, ir jāierobežo dotās preces kopējā summa, kuru var uzglabāt vienā vietā. Lai iestatītu krājumu ierobežojumus izlaistai precei, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet preci, lai atvērtu tās lapu **Izlaisto preču detalizēta informācija**.
1. Grupas **Saderība** cilnes **Pārvaldīt krājumus** darbību rūtī atlasiet vienumu **Ziņošanas informācija**.
1. Laukos **Bīstamo krājumu ierobežojumi** un **Bīstamības brīdinājuma ierobežojumi** iestatiet piemērotas vērtības atlasītajai precei.

**Bīstamo materiālu krājumu ierobežojumu** pārskats ļauj pārraudzīt bīstamo materiālu krājumu ierobežojumus jūsu noliktavas atrašanās vietās, lai pārliecinātos, ka tie paliek šeit noteiktajos drošos ierobežojumos. Lai iegūtu papildu informāciju, skatiet [Bīstamo materiālu krājumu ierobežojumu pārskats](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Pārdošanas pasūtījumu darbības, kas ietver bīstamus materiālus

Lai pārdošanas pasūtījumā iekļautu preci, kas ir klasificēta kā bīstams materiāls, ir jāsaista attiecīgais nosūtījuma pārvadātājs ar pārdošanas pasūtījumu. Atveriet pārdošanas pasūtījumu un pēc tam kopsavilkuma cilni **Piegāde**, pēc nepieciešamības iestatiet **Nosūtījuma pārvadātāja** un **Pārvadātāja pakalpojuma** laukus.

Nosūtīšanas pārvadātājs ir saistīts arī ar piegādes veidu. Tāpēc ir jāpārliecinās, vai šī informācija ir saskaņota ar bīstamo materiālu regulu. Citiem vārdiem sakot, bīstamo materiālu regulā noteiktajam piegādes veidam ir jāatbilst specifikācijām pārdošanas pasūtījuma virsrakstā. Šādā veidā regula, nosūtīšanas pārvadātājs un pakalpojums ir saistīti ar nosūtīšanas rindām, kas tiek izmantotas pārdošanas pasūtījumā.

Pēc tam, kad pārdošanas pasūtījums ir pabeigts un gatavs nosūtīšanai, to var izlaist noliktavā, lai norādītu pārsūtīšanu starp pārdošanas un noliktavas operācijām.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Sūtījumi, kuros ir ietverti bīstami materiāli

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Skatīt bīstamo materiālu rādītājus katrai nosūtīšanas rindai

**Nosūtīšanas detalizētas informācijas** lapā noslodzei ir parādīts kopējais bīstamā materiāla svars un punktu vērtības, kas aprēķinātas katrai noslodzes rindai, kas ir iekļauta šajā sūtījumā. Lai skatītu punktus un svaru, sekojiet šiem soļiem.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Atlasiet sūtījumu, lai atvērtu tās lapu **Sūtījuma detalizēta informācija**.
1. Kopsavilkuma cilnē **Noslodzes rindas** pārbaudiet rindas. Katrai rindai ir redzami bīstamo materiālu aprēķini šādos laukos:

    - **Bīstamo materiālu punkti** – šis lauks rāda bīstamā materiāla rādītāju noslodzes rindai. Vērtība tiek aprēķināta saskaņā ar noteikumiem un vērtībām, kas ir izveidotas piemērotajai regulai un izlaistā produkta iestatījumos. Aprēķinos tiek ņemts daudzums noslodzes rindā un atsauces reizinātājs [materiālu pārvaldības iestatījumos](#material-management) izlaistajai precei.
    - **Ierobežota daudzuma neto svars** — precēm, kas ir iezīmētas kā ierobežota daudzuma preces to bīstamā materiāla satura dēļ, šajā laukā tiek rādīts noslodzes rindā iekļautā bīstamā satura kopējais neto svars. Aprēķins ir balstīts uz precēm, kas izlaisto preču iestatījumos ir atzīmētas kā bīstami materiāli. Ja krājums ir atzīmēts ar ierobežotu daudzumu, aprēķinos tiek ņemts vērā katras noslodzes rindas daudzums, un tas atsaucas uz izlaistā produkta [materiālu pārvaldības iestatījuma](#material-management) svaru.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Pārbaudīt sūtījumā iekļauto bīstamo materiālu saderību

Sistēma var novērtēt, vai visi sūtījumā iekļautie bīstamie materiāli ir piemēroti nosūtīšanai kopā. Lai novērtētu saderību, sistēma pārbauda saderības grupu, kas piešķirta katrai noslodzē iekļautajai precei. Lai iegūtu papildu informāciju, skatiet [Bīstamo materiālu saderības grupas](hazmat-setup.md#compatibility-groups).

Lai palaistu saderības testu, sekojiet šiem soļiem.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visi sūtījumi**.
1. Atlasiet sūtījumu, lai atvērtu tās lapu **Sūtījuma detalizēta informācija**.
1. Darbību rūts cilnes **Sūtījumi** grupā **Darbības** atlasiet **Saderības tests**.

Jūs saņemat ziņojumu, kas informē par testa rezultātiem.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Noslodzes, kurās ir ietverti bīstami materiāli

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Skatīt bīstamo materiālu rādītājus katrai noslodzes rindai

**Noslodzes detalizētas informācijas** lapā noslodzei ir parādīts kopējais bīstamā materiāla svars un punktu vērtības, kas aprēķinātas katrai noslodzei un noslodzes rindai. Lai skatītu punktus un svaru, sekojiet šiem soļiem.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visas noslodzes**.
1. Atlasiet noslodzi, lai atvērtu tās lapu **Noslodzes detalizēta informācija**. (Varat arī atvērt ielādes detaļas, atlasot saiti no saistītā sūtījuma.)
1. Kopsavilkuma cilnē **Noslodzes** varat pārskatīt kopējos bīstamos materiālu punktus un svarus visai noslodzei, pārbaudot šādus laukus:

    - **Bīstamo materiālu punkti** – šis lauks rāda bīstamā materiāla rādītāju noslodzei. Vērtība tiek aprēķināta saskaņā ar noteikumiem un vērtībām, kas ir izveidotas piemērotajai regulai un izlaistā produkta iestatījumos. Aprēķinos tiek ņemts daudzums, kas ir iekļauts noslodzes rindā, un atsauces reizinātājs [materiālu pārvaldības iestatījumos](#material-management) izlaistajai precei.
    - **Ierobežota daudzuma neto svars** — precēm, kas ir iezīmētas kā ierobežota daudzuma preces to bīstamā materiāla satura dēļ, šajā laukā tiek rādīts noslodzē iekļautā bīstamā satura kopējais neto svars. Aprēķins ir balstīts uz precēm, kas izlaisto preču iestatījumos ir atzīmētas kā bīstami materiāli. Ja krājums ir atzīmēts ar ierobežotu daudzumu, aprēķinos tiek ņemts vērā katras noslodzes daudzums, un tas atsaucas uz izlaistā produkta [materiālu pārvaldības iestatījuma](#material-management) svaru.

1. Lai pārskatītu punktus un svaru atsevišķām rindām, atlasiet **Noslodzes rindas** kopsavilkuma cilni. Vērtības, kas tiek sniegtas katrai rindai, ir līdzīgas vērtībām, kas sniegtas visai noslodzei, kā aprakstīts iepriekšējā solī.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Pārbaudīt noslodzē iekļauto bīstamo materiālu saderību

Sistēma var novērtēt, vai visi noslodzē iekļautie bīstamie materiāli ir piemēroti nosūtīšanai kopā. Lai novērtētu saderību, sistēma pārbauda saderības grupu, kas piešķirta katrai noslodzē iekļautajai precei. Lai iegūtu papildu informāciju, skatiet [Bīstamo materiālu saderības grupas](hazmat-setup.md#compatibility-groups).

Lai palaistu saderības testu, sekojiet šiem soļiem.

1. Dodieties uz **Noliktavas pārvaldība \> Sūtījumi \> Visas noslodzes**.
1. Atlasiet sūtījumu, lai atvērtu tās lapu **Noslodzes detalizēta informācija**. (Varat arī atvērt ielādes detaļas, atlasot saiti no saistītā sūtījuma.)
1. Darbību rūts cilnes **Noslodzes** grupā **Darbības** atlasiet **Saderības tests**.

Jūs saņemat ziņojumu, kas informē par testa rezultātiem.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]