---
title: Plānošanas optimizācijas saderības analīze
description: Šajā tēmā skaidrots, kā verificēt jūsu pašreizējos iestatījumus un datus, salīdzinot ar Plānošanas optimizācijas funkcionalitātes iespējām.
author: ChristianRytt
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsFitAnalysis, MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 871ac40ea73c8a72e20ff495b9b7e6fe5a12159e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812983"
---
# <a name="planning-optimization-fit-analysis"></a>Plānošanas optimizācijas atbilstības analīze

[!include [banner](../../includes/banner.md)]

Plānošanas optimizācijas atbilstības analīzes rezultāts ir jāanalizē kā migrācijas procesa daļa. Ievērojiet, ka plānošanas optimizācijas apjoms nav vienāds ar pašreizējo iebūvēto vispārējās plānošanas funkcionalitāti. Mēs iesakām jums strādāt ar savu partneri un lasīt dokumentāciju, lai sagatavotos migrācijai. 

Plānošanas optimizācijas atbilstības analīze palīdz identificēt, kur rezultāts var atšķirties starp iebūvēto vispārējās plānošanas programmu un plānošanas optimizāciju. Šī analīze tiek veikta, pamatojoties uz jūsu pašreizējiem iestatījumiem un datiem. 

Lai skatītu plānošanas optimizācijas atbilstības analīzes rezultātus, dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plānošanas optimizācijas atbilstības analīze** un tad atlasiet **Palaist analīzi**. Ja analīze atklāj neatbilstības, tās ir uzskaitītas tajā pašā lapā. (Analīze var ilgt dažas minūtes.)

> [!NOTE]
> Ja atrastas neatbilstības, joprojām varat izmantot Plānošanas optimizāciju. Saderības analīzes rezultāti tikai rāda vietas, kur plānošanas pakalpojums neievēros jūsu pašreizējos iestatījumus. Citiem vārdiem, tas rāda vietas, kur daži procesi var tikt ignorēti vai, iespējams, netiek atbalstīti.

## <a name="analysis-results-example-1"></a>Analīzes rezultāti: 1. piemērs

- **Līdzeklis:** ražošana
- **Problēma:** krājumi ar materiālu komplekta (MK) līmeni, kas lielāks par nulli: 56
- **Paskaidrojums:** saderības analīze atrada 56 krājumus, kuriem ir MK iestatījums ražošanai. Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta ražošanu, tā izveidos plānotos pirkšanas pasūtījumus, nevis plānotos ražošanas pasūtījumus. Tiks parādīts arī brīdinājums, kas uzskaita ietekmētos krājumus.

## <a name="analysis-results-example-2"></a>Analīzes rezultāti: 2. piemērs

- **Līdzeklis:** darbības
- **Problēma:** nodrošinājuma grupas ar iespējotu darbību aprēķinu: 6
- **Paskaidrojums:** saderības analīze atrada sešas nodrošinājuma grupas, kurās ir ieslēgts darbības aprēķins. Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta darbības, vispārējās plānošanas laikā netiks ģenerētas darbības.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Pārskats par iespējamiem saderības analīzes rezultātiem

Tabulā ir redzami dažādi rezultāti, kas var tikt parādīti pēc saderības analīzes. Numura zīmes (_\#_) tiks aizstātas ar skaitli, kas norāda to ierakstu skaitu, kuriem ir uzskaitītā problēma. Atbalstītie vai priekšskatījuma līdzekļi ir pieejami versijā 10.0.9 vai jaunākā versijā (ja vien augstākas versijas numurs nav norādīts kolonnā Paredzamā pieejamība).

| Funkcija | Uzskaitītā problēma | Paskaidrojums | Paredzamā pieejamība |
| --- | --- | --- | --- |
| Darbības | Vajadzības grupas ar iespējotu darbību aprēķinu:  _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik darbības netiek ģenerētas vispārējās plānošanas laikā, kad ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. Galvenais darbību nolūks ir ieteikt izmaiņas esošajos pasūtījumos. Novērtējiet, vai darbības tiek aktīvi piemērotas kā daļa no jūsu biznesa procesiem un vai kavējuma informācija, kas saistīta ar pasūtījumiem, ir pietiekama. | 2021. gada oktobris - 2022. gada aprīlis |
| Pamatkalendāri | Kalendāri, kas izmanto pamatkalendāru: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik pamatkalendārs tiek ignorēts, ja ir iespējota plānošanas optimizācija. Novērtējiet, vai jūsu biznesa procesiem ir nepieciešams pamatkalendārs un vai tieša iestatīšana kalendāros ir pietiekama. | 2021. gada aprīlis - oktobris | 
| Partijas atgriešanas kodi | Nepieejami partijas atgriešanas metodes šabloni: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik partijas atgriešanas kodi tiek ignorēti, ja ir iespējota plānošanas optimizācija. | 2021. gada oktobris - 2022. gada aprīlis |
| Pieejams solīšanai (CTP) | Noklusējuma pasūtījuma iestatījumi ar piegādes datuma vadīklu iestatītu uz CTP: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik CTP tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Kopēt statisko uz dinamisko plānu | Statiskā kopēšana uz dinamisko plānu ir iespējota vispārējās plānošanas parametros. | Plānošanas optimizācija nekopē statisko plānu uz dinamisko plānu neatkarīgi no šī iestatījuma. Parasti šī koncepcija nav tik svarīga ātruma un pilnīgas reģenerācijas dēļ, ko nodrošina plānošanas optimizācija. Ja tiek izmantoti divi vai vairāki plāni, katram plānam ir jāaktivizē vispārējā plānošana. | 2021. gada oktobris - 2022. gada aprīlis |
| Apstiprināšana | Vajadzības grupas ar iestatītu automātiskās apstiprināšanas periodu: _\#_ | Versijā 10.0.7 un jaunākās versijās apstiprināšana tiek atbalstīta kā atsevišķs apstiprināšanas pakešuzdevums pēc vispārējās plānošanas pabeigšanas (ar nosacījumu, ka _Automātiskās apstiprināšanas līdzeklis plānošanas optimizācijai_ ir iespējots [līdzekļu pārvaldībā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Ņemiet vērā, ka automātiskā apstiprināšana plānošanas optimizācijai ir balstīta uz pasūtījuma datumu (sākuma datumu), nevis prasību datumu (beigu datumu). Tas nodrošina, ka plānoto pasūtījumu apstiprināšana notiek laikus, neiekļaujot izpildes laiku apstiprināšanas laika periodā. | Tiek atbalstīts |
| Apstiprināšana | Vienumu vajadzības ieraksti ar iestatītu automātisko apstiprināšanu: _\#_ | Versijā 10.0.7 un jaunākās versijās automātiskā apstiprināšana tiek atbalstīta kā atsevišķs apstiprināšanas pakešuzdevums pēc vispārējās plānošanas pabeigšanas (ar nosacījumu, ka _Automātiskās apstiprināšanas līdzeklis plānošanas optimizācijai_ ir iespējots [līdzekļu pārvaldībā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Ņemiet vērā, ka automātiskā apstiprināšana plānošanas optimizācijai ir balstīta uz pasūtījuma datumu (sākuma datumu), nevis prasību datumu (beigu datumu). Tas nodrošina, ka plānoto pasūtījumu apstiprināšana notiek laikus, neiekļaujot izpildes laiku apstiprināšanas laika periodā. | Tiek atbalstīts |
| Apstiprināšana | Vispārējie plāni ar iestatītu automātisko apstiprināšanu: _\#_ | Versijā 10.0.7 un jaunākās versijās automātiskā apstiprināšana tiek atbalstīta kā atsevišķs apstiprināšanas pakešuzdevums pēc vispārējās plānošanas pabeigšanas (ar nosacījumu, ka _Automātiskās apstiprināšanas līdzeklis plānošanas optimizācijai_ ir iespējots [līdzekļu pārvaldībā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Ņemiet vērā, ka automātiskā apstiprināšana plānošanas optimizācijai ir balstīta uz pasūtījuma datumu (sākuma datumu), nevis prasību datumu (beigu datumu). Tas nodrošina, ka plānoto pasūtījumu apstiprināšana notiek laikus, neiekļaujot izpildes laiku apstiprināšanas laika periodā. | Tiek atbalstīts |
| FitAnalysisPlanningItems | Krājumu plānošana: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik plānošanas krājumi tiek apstrādāti līdzīgi kā parastie krājumi, kad ir iespējota plānošanas optimizācija. | 2021. gada oktobris - 2022. gada aprīlis |
| Budžets | Pārklājuma grupas ar iespējotu "Iekļaut starpuzņēmumu pasūtījumus": _\#_ | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Starpuzņēmumu plānošana](Intercompany-planning.md) | Tiek atbalstīts |
| Budžets | Pārklājuma grupas ar "Samazināt prognozi pēc" iestatījuma vērtību, kas atšķiras no "Pasūtījumi": _\#_ | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Vispārējā plānošana ar pieprasījuma prognozēm](demand-forecast.md) | Tiek atbalstīts |
| Budžets | Prognozes modeļi ar apakšmodeļiem: _\#_ |  Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Vispārējā plānošana ar pieprasījuma prognozēm](demand-forecast.md) | Tiek atbalstīts |
| Budžets | Vispārējie plāni ar "Iekļaut piegādes apjoma prognozi" ir iespējoti:_\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik piegādes apjoma prognozes netiek atbalstītas, kad ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Periods bez izmaiņām | Vajadzības grupas ar iestatītu sasaldēšanas periodu: _\#_ | Iesaldētais periods netiek bieži izmantots, un pašlaik nav plānu to iekļaut plānošanas optimizācijai. Pašlaik Sasaldēšanas perioda iestatījums tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | Nav piemērojams |
| Periods bez izmaiņām | Vienumu vajadzības ieraksti ar iestatītu sasaldēšanas periodu: _\#_ | Iesaldētais periods netiek bieži izmantots, un pašlaik nav plānu to iekļaut plānošanas optimizācijai. Pašlaik Sasaldēšanas perioda iestatījums tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | Nav piemērojams |
| Periods bez izmaiņām | Vispārējie plāni ar iestatītu sasaldēšanas periodu: _\#_ | Iesaldētais periods netiek bieži izmantots, un pašlaik nav plānu to iekļaut plānošanas optimizācijai. Pašlaik Sasaldēšanas perioda iestatījums tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | Nav piemērojams |
| Starpuzņēmums | Vispārējie plāni, kas ietver lejupstraumes plānoto pieprasījumu _\#_ | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Starpuzņēmumu plānošana](Intercompany-planning.md) | Tiek atbalstīts |
| Kanban | Vienumu vajadzības ieraksti ar plānoto pasūtījuma tipu Kanban: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik, iespējojot plānošanas optimizāciju, krājumu nodrošinājums, kas iestatīts uz Kanban, tiks ignorēts. Kanban plānotā pasūtījuma veids vispārējās plānošanas laikā radīs brīdinājumu, un tiks izveidoti plānotie pirkšanas pasūtījumi, lai nosegtu saistīto pieprasījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Kanban | Vienumi ar noklusējuma pasūtījuma tipu Kanban: _\#_ | Pašlaik, iespējojot plānošanas optimizāciju, noklusējuma pasūtījuma veids, kas iestatīts uz Kanban, tiks ignorēts. Kanban noklusējuma pasūtījuma veids vispārējās plānošanas laikā radīs brīdinājumu, un tiks izveidoti plānotie pirkšanas pasūtījumi, lai nosegtu saistīto pieprasījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Preces dzīves cikla stāvoklis | Preces dzīves cikla stāvokļi nav aktīvi plānošanai: _\#_ | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Produktu ar noteiktiem produkta dzīves cikla nosacījumiem izslēgšana](product-lifecycle-state.md) | Tiek atbalstīts |
| Ražošana | MK rindas ar noapaļošanu vai vairākkārtēju iestatīšanu: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik noapaļošana un vairāki iestatījumi tiek ignorēti MK rindās, iespējojot plānošanas optimizāciju neatkarīgi no šī iestatījuma. | 2021. gada aprīlis - oktobris |
| Ražošana | MK/formulas rindas ar formulas mērījumu: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik formulas mērījumi tiek ignorēti MK un formulas rindās, iespējojot plānošanas optimizāciju neatkarīgi no šī iestatījuma. | 2021. oktobris |
| Ražošana | MK/formulas rindas ar krājumu aizstāšanu (plānu grupas): _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik krājuma aizstāšana (plānu grupas) tiek ignorēta MK un formulas rindās, iespējojot plānošanas optimizāciju neatkarīgi no šī iestatījuma. | 2021. oktobris |
| Ražošana | MK/formulas rindas ar negatīvu daudzumu: _\#_ | Šī funkcija ir gaidīšanas režīmā. MK un formulas rindas, kurām ir negatīvs daudzums, tiks iekļautas ar daudzumu 0 (nulle), un tiks parādīts brīdinājums, ja ir iespējota plānošanas optimizācija. Atjauniniet pamatdatus, lai izvairītos no brīdinājumiem. | 2021. oktobris |
| Ražošana | MK/formulas rindas ar resursu patēriņu: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik MK un formulas rindas ar resursu patēriņu tiek ignorētas, ja ir iespējota plānošanas optimizācija. Kad šī funkcija ir atbalstīta, materiālu vajadzības tiks iestatītas uz ražošanas sākuma datumu. Kamēr šis līdzeklis netiek atbalstīts, prasības netiks ģenerētas materiāliem, kas tiek atzīmēti ar resursu patēriņa karodziņu. | 2021. gada aprīlis - oktobris |
| Ražošana | MK/formulas rindas ar darbību patēriņu: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik darbību patēriņš MK un formulas rindās tiek ignorēts, ja ir iespējota plānošanas optimizācija. | 2021. oktobris |
| Ražošana | MK ar definētu nemainīgu brāķa apjomu vai mainīgu brāķa apjomu: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik definēta brāķa un mainīga brāķa apjoms kas definēti MK, tiek ignorēti, kad ir iespējota plānošanas optimizācija. | 2021. gada oktobris - 2022. gada aprīlis |
| Ražošana | MK ar apakšlīgumu slēgšanu:  _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik apakšlīguma slēgšanas iestatījums MK tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Ražošana | MK bez vietas: _\#_ | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Preču plānošana](production-planning.md) | Tiek atbalstīts |
| Ražošana | Pieprasījums, kurā definētas noteiktas MK vai maršruta prasības: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik noteiktās MK vai maršruta prasības, kas ir definētas pēc pieprasījuma (piemēram, pakārtots MK vai pakārtots maršruts pārdošanas pasūtījumā) tiek ignorētas, kad ir iespējota plānošanas optimizācija. Tiek izmantots standarta MK vai maršruts neatkarīgi no šī iestatījuma. | 2021. gada oktobris - 2022. gada aprīlis |
| Ražošana | Formulu versijas ar blakusproduktiem/līdzproduktiem: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik līdzprodukti un blakusprodukti, kas ir saistīti ar formulas versiju, tiek ignorēti, ja ir iespējota plānošanas optimizācija. | 2021. oktobris |
| Ražošana | Formulu versijas ar ienesīgumu: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik ienesīgums, kas ir saistīts ar formulas versiju, tiek ignorēts, ja ir iespējota plānošanas optimizācija. | 2021. gada oktobris - 2022. gada aprīlis |
| Ražošana | Plāni ar secību: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik secība tiek ignorēta, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Ražošana | Izpildei nodotie ražošanas pasūtījumi, kas nav iesākti, ja sākšana ir ieplānota agrāk nekā šodien: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik, ja ražošanas pasūtījums tiek aizkavēts, vispārējā plānošana pieņem, ka tas tiks pabeigts šodien. Tas attiecas uz izpildei nodotajiem ražošanas pasūtījumiem, kuru piegādes datums ir pagātnē, bet tas vēl nav pabeigts. | 2021. gada oktobris - 2022. gada aprīlis |
| Ražošana | Resursi, kas plānoti ar ierobežotu noslodzi: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik resursi, kas tiek plānoti ar ierobežotu noslodzi, tiek ignorēti, ja ir iespējota plānošanas optimizācija. Plānošana tiek veikta, pamatojoties uz noklusējuma izpildes laiku no preces. | Neierobežots: 2021. gada jūnijs, ierobežots: 2021. gada oktobris |
| Ražošana | Plānošanā izmantotie maršruti: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik maršruti tiek ignorēti, ja ir iespējota plānošanas optimizācija. Tiek izmantots preces noklusētais izpildes laiks. | 2021. jūnijs |
| Ražošana | Tirdzniecības līnijas rezervēšana, izmantojot izvēršanu: _\#_ | Pārdošanas rindas rezervācija, kas izmanto izvēršanu, netiek atbalstīta, ja ir iespējota plānošanas optimizācija. | 2021. oktobris |
| Ražošana | Plānošana ar ražošanas pasūtījumu izvēršanu:  _\#_ | Plānošana ar ražošanas pasūtījumu izvēršanu netiek atbalstīta, ja ir iespējota plānošanas optimizācija. Ražošanas pasūtījumus var plānot atsevišķi. | 2021. oktobris |
| Piedāvājumu pieprasījumi | Vispārējie plāni ar iespējotu piedāvājumu pieprasījumu: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik piedāvājuma pieprasījumi (PP) netiek uzskatīti par pieprasījumu, ja ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Pieprasījumi | Vispārējie plāni ar iespējotiem pieprasījumiem: _\#_ | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet [Pirkšanas pieprasījumi](purchase-requisitions.md) | Tiek atbalstīts |
| Drošības rezerves | Vajadzības grupas ar drošības rezervi: _\#_ | Šis līdzeklis tagad tiek daļēji atbalstīts. Papildinformāciju skatiet sadaļā [Drošības rezerves](safety-margins.md) | Ieejas plūsmas rezerve: tiek atbalstīta. Pasūtījuma rezerve un izejas plūsmas rezerve: 2021. gada aprīlis |
| Drošības rezerves | Vispārējie plāni ar drošības rezervi: _\#_ | Šis līdzeklis tagad tiek daļēji atbalstīts. Papildinformāciju skatiet sadaļā [Drošības rezerves](safety-margins.md) | Ieejas plūsmas rezerve: tiek atbalstīta. Pasūtījuma rezerve un izejas plūsmas rezerve: 2021. gada aprīlis |
| Drošības rezerves izpilde | Krājumu pārklājuma ieraksti ar atzīmi "Izpildīt minimālo", kas atšķiras no "Šodienas datuma + sagādes laiks": _\#_ | Plānošanas optimizācija vienmēr izmanto *Šodienas datumu + sagādes laiku*. Šī izmaiņa tiek veikta, lai nākotnē sagatavotos vienkāršotai plānošanas iestatīšanai un sniegtu darbības rezultātu. Ja sagādes laiks nav iekļauts drošības krājumos, plānotie pasūtījumi, kas izveidoti pašreizējam ar zemu pieejamības līmeni esošajam krājumam, izpildes laika dēļ vienmēr tiks aizkavēti. Šī uzvedība var izraisīt ievērojamu troksni un nevēlamus plānotos pasūtījumus. Vislabākā prakse ir mainīt iestatījumu, lai tiktu izmantots *Šodienas datums + sagādes laiks*. Atjauniniet pamatdatus, lai izvairītos no brīdinājumiem. | Nav piemērojams |
| Pārdošanas piedāvājumi | Vispārējie plāni ar iespējotiem pārdošanas piedāvājumiem: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik piedāvājumi netiek ņemti vērā, ja ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 2021. gada oktobris - 2022. gada aprīlis |
| Glabāšanas laiks | Vispārējie plāni ar iespējotu glabāšanas laiku: _\#_ | Šī funkcija ir gaidīšanas režīmā. Pašlaik glabāšanas laiks netiek ņemts vērā, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 2021. oktobris |

## <a name="additional-resources"></a>Papildu resursi

[Plānošanas optimizācijas apskats](planning-optimization-overview.md)

[Darba sākšana ar plānošanas optimizāciju](get-started.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Filtru lietošana plānam](plan-filters.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
