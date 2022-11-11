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
ms.openlocfilehash: 4459a5d72fafe2596b7fc0cedf060b8f23bb43d2
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750712"
---
# <a name="planning-optimization-fit-analysis"></a>Plānošanas optimizācijas atbilstības analīze

[!include [banner](../../includes/banner.md)]

Plānošanas optimizācijas atbilstības analīzes rezultāts ir jāanalizē kā migrācijas procesa daļa. Ņemiet vērā, ka plānošanas optimizācijas tvērums nav vienāds ar novecojušu vispārējās plānošanas programmas funkcionalitāti. Mēs iesakām jums strādāt ar savu partneri un lasīt dokumentāciju, lai sagatavotos migrācijai.

Plānošanas optimizācijas atbilstības analīze palīdz jums noteikt, kur rezultāts var atšķirties no novecojušas vispārējās plānošanas programmas un plānošanas optimizācijas. Šī analīze tiek veikta, pamatojoties uz jūsu pašreizējiem iestatījumiem un datiem. 

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
| Partijas atgriešanas kodi | Nepieejami partijas atriešanas metodes šabloni: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Partijas atgriešanas kodu lietošana, lai atzīmētu partijas kā pieejamas vai nav pieejamas](../../inventory/batch-disposition-codes.md) | Tiek atbalstīts |
| Pieejams solīšanai (CTP) | Noklusējuma pasūtījuma iestatījumi ar piegādes datuma vadīklu iestatītu uz CTP: *\#* | Piegādes ķēdes pārvaldības 10.0.28 un jaunākā procesā ar nosaukumu CTP *plānošanas optimizēšanai tiek veikti apstiprināti nosūtīšanas un saņemšanas datumi,* kas ir pieejami pēc dinamiskā plāna palaišanas. Vecākām Piegādes ķēžu pārvaldības versijām, iespējojot plānošanas optimizāciju, tiek ignorēts mantojuma CTP iestatījums. | Tiek atbalstīts |
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
| Ražošana | Izpildei nodotie ražošanas pasūtījumi, kas nav iesākti, ja sākšana ir ieplānota agrāk nekā šodien: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik, ja ražošanas pasūtījums tiek aizkavēts, vispārējā plānošana pieņem, ka tas tiks pabeigts šodien. Tas attiecas uz izpildei nodotajiem ražošanas pasūtījumiem, kuru piegādes datums ir pagātnē, bet tas vēl nav pabeigts. | 20 222 laidiena 2. laidiens |
| Ražošana | Resursi, kas plānoti ar ierobežotu noslodzi: *\#* | Šis līdzeklis tagad tiek atbalstīts.| Tiek atbalstīts |
| Ražošana | Plānošanā izmantotie maršruti: *\#* | Šī funkcija tiek atbalstīta. | Tiek atbalstīts |
| Ražošana | Tirdzniecības līnijas rezervēšana, izmantojot izvēršanu: *\#* | Pārdošanas rindas rezervācija, kas izmanto izvēršanu, netiek atbalstīta, ja ir iespējota plānošanas optimizācija. | 20 222 laidiena 2. laidiens |
| Ražošana | Plānošana ar ražošanas pasūtījumu izvēršanu: *\#* | Plānošana ar ražošanas pasūtījumu izvēršanu netiek atbalstīta, ja ir iespējota plānošanas optimizācija. Ražošanas pasūtījumus var plānot atsevišķi. | 20 222 laidiena 2. laidiens |
| Piedāvājumu pieprasījumi | Vispārējie plāni ar iespējotu piedāvājumu pieprasījumu: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik piedāvājumu pieprasījumi (PP) netiek uzskatīti par pieprasījumu, ja ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 20 222 laidiena 2. laidiens |
| Pieprasījumi | Vispārējie plāni ar iespējotiem pieprasījumiem: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet [Pirkšanas pieprasījumi](purchase-requisitions.md) | Tiek atbalstīts |
| Drošības rezerves | Vajadzības grupas ar drošības rezervi: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Drošības rezerves](safety-margins.md) | Tiek atbalstīts |
| Drošības rezerves | Vispārējie plāni ar drošības rezervi: *\#* | Šis līdzeklis tagad tiek atbalstīts. Papildinformāciju skatiet sadaļā [Drošības rezerves](safety-margins.md) |  Tiek atbalstīts |
| Pārdošanas piedāvājumi | Vispārējie plāni ar iespējotiem pārdošanas piedāvājumiem: *\#* | Šī funkcija ir gaidīšanas režīmā. Pašlaik piedāvājumi netiek ņemti vērā, ja ir iespējota plānošanas optimizācija. Tie tiks ignorēti, neņemot vērā šo iestatījumu. | 20 222 laidiena 2. laidiens |
| Glabāšanas laiks | Vispārējie plāni ar iespējotu glabāšanas laiku: *\#* | Šis līdzeklis tagad tiek atbalstīts. | Tiek atbalstīts |

## <a name="additional-resources"></a>Papildu resursi

- [Vispārējās plānošanas sistēmas arhitektūra](../master-planning-architecture.md)
- [Sākt ar vispārējo plānošanu](get-started.md)
- [Atšķirības starp vispārējo plānošanu un plānošanas optimizāciju](planning-optimization-differences-with-built-in.md)
- [Parametri, kas netiek izmantoti plānošanas optimizācijai](not-used-parameters.md)
- [Plāna vēstures un plānošanas žurnālu skatīšana](plan-history-logs.md)
- [Krājumu apakškopas plānošanas palaišana](plan-filters.md)
- [Plānošanas darba atcelšana](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
