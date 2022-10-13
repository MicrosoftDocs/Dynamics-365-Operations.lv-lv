---
title: Plānošanas optimizācijas atbilstības analīze
description: Šajā rakstā skaidrots, kā pārbaudīt pašreizējos iestatījumus un datus pret plānošanas optimizācijas funkcionalitātes iespējām.
author: t-benebo
ms.date: 08/11/2022
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: c160a6477dd41fac0f15f57bb0f46def500f4589
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/12/2022
ms.locfileid: "9643745"
---
# <a name="planning-optimization-fit-analysis"></a>Plānošanas optimizācijas atbilstības analīze

[!include [banner](../../includes/banner.md)]

Plānošanas optimizācijas atbilstības analīzes rezultāts ir jāanalizē kā migrācijas procesa daļa. Ievērojiet, ka plānošanas optimizācijas apjoms nav vienāds ar pašreizējo iebūvēto vispārējās plānošanas funkcionalitāti. Mēs iesakām jums strādāt ar savu partneri un lasīt dokumentāciju, lai sagatavotos migrācijai. 

Plānošanas optimizācijas atbilstības analīze palīdz identificēt, kur rezultāts var atšķirties starp iebūvēto vispārējās plānošanas programmu un plānošanas optimizāciju. Šī analīze tiek veikta, pamatojoties uz jūsu pašreizējiem iestatījumiem un datiem. 

Lai skatītu plānošanas optimizācijas atbilstības analīzes rezultātus, dodieties uz **Vispārējā plānošana** \> **Iestatījumi** \> **Plānošanas optimizācijas atbilstības analīze** un tad atlasiet **Palaist analīzi**. Ja analīze atklāj neatbilstības, tās ir uzskaitītas tajā pašā lapā. (Analīze var ilgt dažas minūtes.)

> [!NOTE]
>
> - Dažas neatbilstības nevar identificēt, izmantojot plānošanas optimizācijas atbilstības analīzi. Papildinformāciju skatiet sadaļā [Atšķirības starp vispārējo plānošanu un plānošanas optimizāciju](planning-optimization-differences-with-built-in.md).
>
> - Ja atrastas neatbilstības, joprojām varat izmantot Plānošanas optimizāciju. Saderības analīzes rezultāti tikai rāda vietas, kur plānošanas pakalpojums neievēros jūsu pašreizējos iestatījumus. Citiem vārdiem, tas rāda vietas, kur daži procesi var tikt ignorēti vai, iespējams, netiek atbalstīti.

## <a name="analysis-results-example-1"></a>Analīzes rezultāti: 1. piemērs

- **Līdzeklis:** ražošana
- **Problēma:** krājumi ar materiālu komplekta (MK) līmeni, kas lielāks par nulli: 56
- **Paskaidrojums:** saderības analīze atrada 56 krājumus, kuriem ir MK iestatījums ražošanai. Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta ražošanu, tā izveidos plānotos pirkšanas pasūtījumus, nevis plānotos ražošanas pasūtījumus. Tiks parādīts arī brīdinājums, kas uzskaita ietekmētos krājumus.

## <a name="analysis-results-example-2"></a>Analīzes rezultāti: 2. piemērs

- **Līdzeklis:** darbības
- **Problēma:** nodrošinājuma grupas ar iespējotu darbību aprēķinu: 6
- **Paskaidrojums:** saderības analīze atrada sešas nodrošinājuma grupas, kurās ir ieslēgts darbības aprēķins. Tā kā pašreizējā Plānošanas optimizācijas versija neatbalsta darbības, vispārējās plānošanas laikā netiks ģenerētas darbības.

## <a name="overview-of-possible-results-from-the-fit-analysis"></a>Pārskats par iespējamiem saderības analīzes rezultātiem

Tabulā ir redzami dažādi rezultāti, kas var tikt parādīti pēc saderības analīzes. Numura zīmes (*\#*) tiks aizstātas ar skaitli, kas norāda to ierakstu skaitu, kuriem ir uzskaitītā problēma.

> [!IMPORTANT]
> Līdzekļiem, kas vēl netiek atbalstīti, tabulā ir sniegta sagaidāmā pieejamības informācija, kas tiek novērtēta, pamatojoties uz mūsu pašreizējo vērtību. Šie novērtējumi var tikt mainīti bez iepriekšēja brīdinājuma.

| Līdzeklis | Uzskaitītā problēma | Paskaidrojums | Paredzamā pieejamība |
| --- | --- | --- | --- |
| Darbības | Vajadzības grupas ar iespējotu darbību aprēķinu: *\#* | Šis līdzeklis tagad tiek atbalstīts. | Tiek atbalstīts |
| Pamatkalendāri | Kalendāri, kas izmanto pamatkalendāru: *\#* | Šis līdzeklis tagad tiek atbalstīts. | Tiek atbalstīts | 
| Partijas atgriešanas kodi | Nepieejami partijas atriešanas metodes šabloni: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik partijas atgriešanas kodi tiek ignorēti, ja ir iespējota plānošanas optimizācija. | 20 222 laidiena 2. laidiens <!-- KFM: Now available? [Use batch disposition codes to mark batches as available or unavailable](../../inventory/batch-disposition-codes.md) --> |
| Pieejams solīšanai (CTP) | Noklusējuma pasūtījuma iestatījumi ar piegādes datuma vadīklu iestatītu uz CTP: *\#* | Piegādes ķēdes pārvaldības 10.0.28 un jaunākā procesā ar nosaukumu CTP *plānošanas optimizēšanai tiek veikti apstiprināti nosūtīšanas un saņemšanas datumi,* kas ir pieejami pēc dinamiskā plāna palaišanas. Vecākām Piegādes ķēžu pārvaldības versijām, iespējojot plānošanas optimizāciju, tiek ignorēts mantojuma CTP iestatījums. | Tiek atbalstīts |
| Kopēt statisko uz dinamisko plānu | Statiskā kopēšana uz dinamisko plānu ir iespējota vispārējās plānošanas parametros. | Plānošanas optimizācija nekopē statisko plānu uz dinamisko plānu neatkarīgi no šī iestatījuma. Parasti šī koncepcija nav tik svarīga ātruma un pilnīgas reģenerācijas dēļ, ko nodrošina plānošanas optimizācija. Ja tiek izmantoti divi vai vairāki plāni, katram plānam ir jāaktivizē vispārējā plānošana. | Nav datu |
| Apstiprināšana | Vajadzības grupas ar iestatītu automātiskās apstiprināšanas periodu: *\#* | Versijā 10.0.7 un jaunākās versijās apstiprināšana tiek atbalstīta kā atsevišķs apstiprināšanas pakešuzdevums pēc vispārējās plānošanas pabeigšanas (ar nosacījumu, ka *Automātiskās apstiprināšanas līdzeklis plānošanas optimizācijai* ir iespējots [līdzekļu pārvaldībā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Ņemiet vērā, ka automātiskā apstiprināšana plānošanas optimizācijai ir balstīta uz pasūtījuma datumu (sākuma datumu), nevis prasību datumu (beigu datumu). Tas nodrošina, ka plānoto pasūtījumu apstiprināšana notiek laikus, neiekļaujot izpildes laiku apstiprināšanas laika periodā. | Tiek atbalstīts |
| Apstiprināšana | Vienumu vajadzības ieraksti ar iestatītu automātisko apstiprināšanu: *\#* | Versijā 10.0.7 un jaunākās versijās automātiskā apstiprināšana tiek atbalstīta kā atsevišķs apstiprināšanas pakešuzdevums pēc vispārējās plānošanas pabeigšanas (ar nosacījumu, ka *Automātiskās apstiprināšanas līdzeklis plānošanas optimizācijai* ir iespējots [līdzekļu pārvaldībā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Ņemiet vērā, ka automātiskā apstiprināšana plānošanas optimizācijai ir balstīta uz pasūtījuma datumu (sākuma datumu), nevis prasību datumu (beigu datumu). Tas nodrošina, ka plānoto pasūtījumu apstiprināšana notiek laikus, neiekļaujot izpildes laiku apstiprināšanas laika periodā. | Tiek atbalstīts |
| Apstiprināšana | Vispārējie plāni ar iestatītu automātisko apstiprināšanu: *\#* | Versijā 10.0.7 un jaunākās versijās automātiskā apstiprināšana tiek atbalstīta kā atsevišķs apstiprināšanas pakešuzdevums pēc vispārējās plānošanas pabeigšanas (ar nosacījumu, ka *Automātiskās apstiprināšanas līdzeklis plānošanas optimizācijai* ir iespējots [līdzekļu pārvaldībā](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)). Ņemiet vērā, ka automātiskā apstiprināšana plānošanas optimizācijai ir balstīta uz pasūtījuma datumu (sākuma datumu), nevis prasību datumu (beigu datumu). Tas nodrošina, ka plānoto pasūtījumu apstiprināšana notiek laikus, neiekļaujot izpildes laiku apstiprināšanas laika periodā. | Tiek atbalstīts |
| FitAnalysisPlanningItems | Krājumu plānošana: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik plānošanas krājumi tiek apstrādāti līdzīgi kā parastie krājumi, kad ir iespējota plānošanas optimizācija. | 20 222 laidiena 2 vai jaunāka versija |
| Budžets | Pārklājuma grupas ar iespējotu "Iekļaut starpuzņēmumu pasūtījumus": *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Starpuzņēmumu plānošana](Intercompany-planning.md) | Tiek atbalstīts |
| Prognoze | Pārklājuma grupas ar "Samazināt prognozi pēc" iestatījuma vērtību, kas atšķiras no "Pasūtījumi": *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Vispārējā plānošana ar pieprasījuma prognozēm](demand-forecast.md) | Tiek atbalstīts |
| Prognoze | Prognožu modeļi ar apakšmodeļiem: *\#* |  Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Vispārējā plānošana ar pieprasījuma prognozēm](demand-forecast.md) | Tiek atbalstīts |
| Prognoze | Vispārējie plāni ar "Iekļaut piegādes apjoma prognozi" ir iespējoti: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik piegādes apjoma prognozes netiek atbalstīts, kad ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 20 222 laidiena 2 vai jaunāka versija |
| Periods bez izmaiņām | Vajadzības grupas ar iestatītu periodu bez izmaiņām: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik Perioda bez izmaiņām iestatījums tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 20 222 laidiena 2. laidiens |
| Periods bez izmaiņām | Vienumu vajadzības ieraksti ar iestatītu periodu bez izmaiņām: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik Perioda bez izmaiņām iestatījums tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 20 222 laidiena 2. laidiens |
| Periods bez izmaiņām | Vispārējie plāni ar iestatītu periodu bez izmaiņām: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik Perioda bez izmaiņām iestatījums tiek ignorēts, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 20 222 laidiena 2. laidiens |
| Starpuzņēmums | Vispārējie plāni, kas ietver lejupstraumes plānoto pieprasījumu *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Starpuzņēmumu plānošana](Intercompany-planning.md) | Tiek atbalstīts |
| Kanban | Vienumu vajadzības ieraksti ar plānoto pasūtījuma tipu Kanban: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik, iespējojot plānošanas optimizāciju, krājumu nodrošinājums, kas iestatīts uz Kanban, tiks ignorēts. Kanban plānotā pasūtījuma veids vispārējās plānošanas laikā radīs brīdinājumu, un tiks izveidoti plānotie pirkšanas pasūtījumi, lai nosegtu saistīto pieprasījumu. | Turpmāks kopums |
| Kanban | Vienumi ar noklusējuma pasūtījuma tipu Kanban: *\#* | Pašlaik, iespējojot plānošanas optimizāciju, noklusējuma pasūtījuma veids, kas iestatīts uz Kanban, tiks ignorēts. Kanban noklusējuma pasūtījuma veids vispārējās plānošanas laikā radīs brīdinājumu, un tiks izveidoti plānotie pirkšanas pasūtījumi, lai nosegtu saistīto pieprasījumu. | Turpmāks kopums |
| Preces dzīves cikla stāvoklis | Produkta dzīves cikla stāvokļi nav aktīvi plānošanai: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Produktu ar noteiktu preces dzīves cikla stāvokli izslēgšana](product-lifecycle-state.md) | Tiek atbalstīts |
| Ražošana | MK rindas ar noapaļošanu vai vairākkārtēju iestatīšanu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik noapaļošana un vairāki iestatījumi tiek ignorēti MK rindās, iespējojot plānošanas optimizāciju neatkarīgi no šī iestatījuma. | Turpmāks kopums|
| Ražošana | MK/formulas rindas ar formulas mērījumu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik formulas mērījumi tiek ignorēti MK un formulas rindās, iespējojot plānošanas optimizāciju neatkarīgi no šī iestatījuma. | 20 222 laidiena 2. laidiens |
| Ražošana | MK/formulas rindas ar krājumu aizstāšanu (plānu grupas): *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik krājuma aizstāšana (plānu grupas) tiek ignorēta MK un formulas rindās, iespējojot plānošanas optimizāciju neatkarīgi no šī iestatījuma. | 20 222 laidiena 2. laidiens |
| Ražošana | MK/formulas rindas ar negatīvu daudzumu: *\#* | Šī funkcija ir gaidīšanas režīmā. MK un formulas rindas, kurām ir negatīvs daudzums, tiks iekļautas ar daudzumu 0 (nulle), un tiks parādīts brīdinājums, ja ir iespējota plānošanas optimizācija. Atjauniniet pamatdatus, lai izvairītos no brīdinājumiem. | 20 222 laidiena 2. laidiens |
| Ražošana | MK/formulas rindas ar resursu patēriņu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik MK un formulas rindas ar resursu patēriņu tiek ignorētas, ja ir iespējota plānošanas optimizācija. Kad šī funkcija ir atbalstīta, materiālu vajadzības tiks iestatītas uz ražošanas sākuma datumu. Kamēr šis līdzeklis netiek atbalstīts, prasības netiks ģenerētas materiāliem, kas tiek atzīmēti ar resursu patēriņa karodziņu. | 20 222 laidiena 2. laidiens |
| Ražošana | MK/formulas rindas ar darbību patēriņu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik darbību patēriņš MK un formulas rindās tiek ignorēts, ja ir iespējota plānošanas optimizācija. | 20 222 laidiena 2. laidiens |
| Ražošana | MK ar definētu nemainīgu brāķa apjomu vai mainīgu brāķa apjomu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik definēta brāķa un mainīga brāķa apjoms kas definēti MK, tiek ignorēti, kad ir iespējota plānošanas optimizācija. | 20 222 laidiena 2. laidiens |
| Ražošana | MK ar apakšlīgumu slēgšanu: *\#* | Šis līdzeklis tagad tiek atbalstīts. | Tiek atbalstīts |
| Ražošana | MK bez vietas: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Ražošanas plānošana](production-planning.md) | Tiek atbalstīts |
| Ražošana | Pieprasījums, kurā definētas noteiktas MK vai maršruta prasības: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik noteiktās MK vai maršruta prasības, kas ir definētas pēc pieprasījuma (piemēram, pakārtots MK vai pakārtots maršruts pārdošanas pasūtījumā) tiek ignorētas, kad ir iespējota plānošanas optimizācija. Tiek izmantots standarta MK vai maršruts neatkarīgi no šī iestatījuma. | 20 222 laidiena 2. laidiens |
| Ražošana | Formulu versijas ar blakusproduktiem/līdzproduktiem: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik līdzprodukti un blakusprodukti, kas ir saistīti ar formulas versiju, tiek ignorēti, ja ir iespējota plānošanas optimizācija. | 20 222 laidiena 2. laidiens |
| Ražošana | Formulu versijas ar ienesīgumu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik ienesīgums, kas ir saistīts ar formulas versiju, tiek ignorēts, ja ir iespējota plānošanas optimizācija. | 20 222 laidiena 2. laidiens |
| Ražošana | Plāni ar secību: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik secība tiek ignorēta, ja ir iespējota plānošanas optimizācija, neņemot vērā šo iestatījumu. | 20 222 laidiena 2. laidiens |
| Ražošana | Izpildei nodotie ražošanas pasūtījumi, kas nav iesākti, ja sākšana ir ieplānota agrāk nekā šodien: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik, ja ražošanas pasūtījums tiek aizkavēts, vispārējā plānošana pieņem, ka tas tiks pabeigts šodien. Tas attiecas uz izpildei nodotajiem ražošanas pasūtījumiem, kuru piegādes datums ir pagātnē, bet tas vēl nav pabeigts. | Turpmāks kopums |
| Ražošana | Resursi, kas plānoti ar ierobežotu noslodzi: *\#* | Šis līdzeklis tagad tiek atbalstīts.| Tiek atbalstīts |
| Ražošana | Plānošanā izmantotie maršruti: *\#* | Šī funkcija tiek atbalstīta. | Tiek atbalstīts |
| Ražošana | Tirdzniecības līnijas rezervēšana, izmantojot izvēršanu: *\#* | Pārdošanas rindas rezervācija, kas izmanto izvēršanu, netiek atbalstīta, ja ir iespējota plānošanas optimizācija. | Turpmāks kopums |
| Ražošana | Plānošana ar ražošanas pasūtījumu izvēršanu: *\#* | Plānošana ar ražošanas pasūtījumu izvēršanu netiek atbalstīta, ja ir iespējota plānošanas optimizācija. Ražošanas pasūtījumus var plānot atsevišķi. | Turpmāks kopums |
| Piedāvājumu pieprasījumi | Vispārējie plāni ar iespējotu piedāvājumu pieprasījumu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik piedāvājumu pieprasījumi (PP) netiek uzskatīti par pieprasījumu, ja ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 20 222 laidiena 2. laidiens |
| Pieprasījumi | Vispārējie plāni ar iespējotiem pieprasījumiem: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet [Pirkšanas pieprasījumi](purchase-requisitions.md) | Tiek atbalstīts |
| Drošības rezerves | Vajadzības grupas ar drošības rezervi: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Drošības rezerves](safety-margins.md) | Tiek atbalstīts |
| Drošības rezerves | Vispārējie plāni ar drošības rezervi: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Drošības rezerves](safety-margins.md) |  Tiek atbalstīts |
| Drošības rezerves izpilde | Krājumu pārklājuma ieraksti ar atzīmi "Izpildīt minimālo", kas atšķiras no "Šodienas datuma + sagādes laiks": *\#* | Plānošanas optimizācija vienmēr izmanto *Šodienas datumu + sagādes laiku*. Šī izmaiņa tiek veikta, lai nākotnē sagatavotos vienkāršotai plānošanas iestatīšanai un sniegtu darbības rezultātu. Ja sagādes laiks nav iekļauts drošības krājumos, plānotie pasūtījumi, kas izveidoti pašreizējam ar zemu pieejamības līmeni esošajam krājumam, izpildes laika dēļ vienmēr tiks aizkavēti. Šī uzvedība var izraisīt ievērojamu troksni un nevēlamus plānotos pasūtījumus. Vislabākā prakse ir mainīt iestatījumu, lai tiktu izmantots *Šodienas datums + sagādes laiks*. Atjauniniet pamatdatus, lai izvairītos no brīdinājumiem. | Nav piemērojams |
| Pārdošanas piedāvājumi | Vispārējie plāni ar iespējotiem pārdošanas piedāvājumiem: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik piedāvājumi netiek ņemti vērā, ja ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 20 222 laidiena 2 vai jaunāka versija |
| Glabāšanas laiks | Vispārējie plāni ar iespējotu glabāšanas laiku: *\#* | Šis līdzeklis tagad tiek atbalstīts. | Tiek atbalstīts |

## <a name="additional-resources"></a>Papildu resursi

[Plānošanas optimizācijas apskats](planning-optimization-overview.md)

[Darba sākšana ar plānošanas optimizāciju](get-started.md)

[Atšķirības starp vispārējo plānošanu un plānošanas optimizāciju](planning-optimization-differences-with-built-in.md)

[Parametri, kas netiek izmantoti plānošanas optimizācijai](not-used-parameters.md)

[Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)

[Filtru lietošana plānam](plan-filters.md)

[Plānošanas darba atcelšana](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
