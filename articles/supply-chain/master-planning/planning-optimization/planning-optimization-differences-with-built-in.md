---
title: Atšķirības starp plānošanas optimizāciju un novecojušu vispārējās plānošanas programmu
description: Šajā rakstā ir uzskaitīti līdzekļi, ko neatbalsta plānošanas optimizācija un kuri nav norādīti lapā Optimizācijas plānošanas atbilstības analīze.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745366"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Atšķirības starp plānošanas optimizāciju un novecojušu vispārējās plānošanas programmu

[!include [banner](../../includes/banner.md)]

Plānošanas optimizācijas rezultāti var atšķirties no novecojušās vispārējās plānošanas programmas rezultātiem. To var izraisīt arī vēl nepabeigtas funkcijas. Šajā rakstu sarakstā ir norādīti līdzekļi, ko vēl neatbalsta plānošanas optimizācija un kuri nav norādīti lapā Optimizācijas **[plānošanas atbilstības analīze](planning-optimization-fit-analysis.md)** ].

| Funkcija | Pašreizējā funkcionalitāte plānošanas optimizācijā |
|---|---|
| Pieļaujamā svara preces | Pieļaujamā svara preces tiek uzskatītas par parastām precēm.|
| Paplašināmās dimensijas | Plānošanas optimizācijā netiek atbalstītas paplašināmās dimensijas. Ja izmantojat plānošanas optimizāciju, paplašināmās dimensijas plānotajiem pasūtījumiem ir tukšas pat tad, **·** **·** **ja izvēles rūtiņa Vajadzības plāns pa dimensijām ir atzīmēta lapā Noliktavas dimensiju grupas vai Izsekošanas dimensiju** grupas. |
| Filtrētas ražošanas izpildes | Sīkāku informāciju skatiet [Ražošanas plānošana — filtri](production-planning.md#filters). |
| Prognožu plānošana | Budžeta plānošana netiek atbalstīta. Ieteicams izmantot vispārējo plānošanu, kur budžeta modelis ir piešķirts vispārējai plānam. |
| Plānoto pasūtījumu numuru secība | Plānoto pasūtījumu numuru sērijas netiek atbalstītas. Plānoto pasūtījumu numuri tiek ģenerēti pakalpojuma pusē. Plānotais pasūtījuma numurs parasti tiek veidots no 10 cipariem, bet secība faktiski ir veidota no 20 rakstzīmēm ar 10 cipariem, kas piešķirti plānošanas izpildes skaitam, un pārējie 10 cipari plānotajam pasūtījumu skaitam. |
| Plānot plāna kopēšanu, dzēšanu un plāna versijas tīrīšanu | <p>Tālāk minētās preces ir atspējotas **Vispārējās plānošanas \> Vispārējās plānošanas \> Uzturēšanas plānu** navigācijas rūtī:</p><ul><li>Plāna kopija</li><li>Dzēst plānu</li><li>Ieplānot versijas tīrīšanu</li></ul> |
| Atgrieztie pasūtījumi | Atgriešanas pasūtījumi netiek izskatīti. |
| Ar plānošanu saistītās funkcijas | Papildinformāciju skatiet sadaļā [Plānošana ar neierobežotu noslodzi](infinite-capacity-planning.md#limitations). |
| Drošības rezerves izpilde | Plānošanas optimizācija vienmēr lieto opciju *Šodienas datums + iepirkuma laiks* lapas **Krājumu segums** laukā **Izpildīt minimumu**. Tādējādi var novērst nevēlamus plānotos pasūtījumus un citas problēmas, ja sagādes laiks nav iekļauts drošības krājumos, plānotie pasūtījumi, kas izveidoti pašreizējam ar zemu pieejamības līmeni esošajam krājumam, izpildes laika dēļ vienmēr tiks aizkavēti. |
| Drošības rezerves piesaiste un neto prasības | Prasības tips *Drošības rezerve* nav iekļauts un netiek rādīts lapā **Neto prasības**. Drošības rezerve neatspoguļo pieprasījumu, un ar to nav saistīts prasības datums. Tā vietā tā nosaka ierobežojumu tam, cik daudz krājumam ir jābūt vienmēr klātesošam. Taču lauka **Minimums** vērtība joprojām tiek ņemta vērā, aprēķinot plānotos pasūtījumus galvenās plānošanas laikā. Iesakām pārbaudīt **Uzkrātā daudzuma** kolonnu lapā **Neto prasības**, lai redzētu, vai šī vērtība tika ņemta vērā. Tā kā piesaiste atšķiras, var tikt ieteiktas dažādas darbības. |
| Transportēšanas kalendārs | Vērtība lapā **Piegādes režīmi** kolonnā **Transportēšanas kalendārs** tiek ignorēta. |
| Min./maks. vajadzību kods bez vērtībām| Ar nolietoto vispārējās plānošanas programmu, kad izmantojat min/max seguma kodu, kur nav iestatītas minimālās vai maksimālās vērtības, plānošanas programma apstrādā vajadzības kodu kā prasību un izveido vienu pasūtījumu katrai prasībai. Ar plānošanas optimizāciju sistēma izveidos vienu pasūtījumu dienā, lai segtu pilnu šīs dienas summu.  |
| Neto vajadzības un manuāli izveidoti plānotie pasūtījumi | Ar novecojušu vispārējās plānošanas programmu, manuāli izveidoti piegādes pasūtījumi krājumam automātiski parādās starp šī krājuma neto prasībām. Piemēram, veidojot pirkšanas pasūtījumu no pārdošanas pasūtījuma, pirkšanas pasūtījums tiek parādīts **Neto prasību lapā**, neprasot iepriekšējas darbības. Tas ir tāpēc, ka novecojusi vispārējās plānošanas `inventLogTTS`**programma reģistrē krājumu darbības tabulā un parāda izmaiņas dinamisko plānu** neto prasību lapā. Tomēr, izmantojot plānošanas optimizāciju, manuāli izveidotie pasūtījumi neparādīsies starp krājuma neto prasībām līdz plānošanas optimizācijas palaišanai (izmantojot plānu, kas ietver krājumu) **\>** **vai** līdz brīdim, kad atlasīsiet Atjaunināt vispārējo plānošanu darbību rūtī neto prasību lapā, kas izpildīs krājuma vispārējo plānošanu. Papildinformāciju par to, kā strādāt ar **neto prasību** lapu, skatiet tīkla [prasību un piesaistes informāciju](net-requirements.md). |
| Resursu piešķire | Strādājot ar neierobežoto noslodzi, novecojusi vispārējās plānošanas programma piešķir visus plānotos pasūtījumus tam pašam resursam attiecīgajā resursu grupā. Plānojot optimizāciju, tiek uzlaboti šie resursi, atlasot resursus nejaušā secībā, tāpēc dažādos ražošanas pasūtījumos var izmantot dažādus resursus. Ja visiem plānotajiem pasūtījumiem vēlaties izmantot vienu un to pašu resursu, maršrutā jānorāda šis resurss. |
| Paplašinātie datu tipi (EDT) | Plānošanas optimizēšana neatbalsta EDT precizitātes izmaiņas. Tas nozīmē, ka šis process netiek oficiāli atbalstīts un nav garantēts darbam. |
| Drošības rezerves izpilde | Plānošanas optimizācijā vienmēr tiek **izmantots vismaz šodienas** *datums + sagādes laiks*. Tas sagatavo sistēmu vienkāršotas plānošanas iestatīšanas izmantošanai nākotnē un nodrošina darbību izpildāmu rezultātu. Ja drošības krājumiem nav iekļauts sagādes laiks, plānotie pasūtījumi, kas ir izveidoti zema rīcībā esošo krājumu daudzumam, vienmēr būs aizkavēti izpildes laika dēļ. Šī uzvedība var izraisīt ievērojamu troksni un nevēlamus plānotos pasūtījumus. Vislabākā prakse ir mainīt iestatījumu, lai izmantotu šodienas *datumu + sagādes laiku*. Atjauniniet pamatdatus, lai izvairītos no brīdinājumiem. |
| Kopēt statisko uz dinamisko plānu | Plānošanas optimizācija nekopē statiskos plānus uz dinamiskajiem plāniem, neatkarīgi no vispārējās plānošanas **parametru lapas** iestatījuma. Parasti šī operācija ir mazāk svarīga, jo ir nodrošināts ātrums un pilna atjaunošana, ko nodrošina plānošanas optimizācija. Ja tiek izmantoti divi vai vairāki plāni, katram plānam ir jāaktivizē vispārējā plānošana. |

## <a name="additional-resources"></a>Papildu resursi

- [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)
- [Parametri, kas netiek izmantoti plānošanas optimizācijai](not-used-parameters.md)
- [Datuma un laika parametri, kas tiek izmantoti plānošanas optimizācijai](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
