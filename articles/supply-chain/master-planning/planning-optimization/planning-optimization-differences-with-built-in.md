---
title: Papildinformāciju skatiet sadaļā Atšķirības starp vispārējo plānošanu un plānošanas optimizāciju
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
ms.openlocfilehash: cf39166dce860dbd796cb4749175628252ed96ea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897579"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Papildinformāciju skatiet sadaļā Atšķirības starp vispārējo plānošanu un plānošanas optimizāciju

[!include [banner](../../includes/banner.md)]

Optimizācijas optimizācijas rezultāti var atšķirties no iebūvētās vispārējās plānošanas programmas rezultātiem. To var izraisīt arī vēl nepabeigtas funkcijas. Šajā rakstu sarakstā ir norādīti līdzekļi, ko vēl neatbalsta plānošanas optimizācija un kuri nav norādīti lapā Optimizācijas **[plānošanas atbilstības analīze](planning-optimization-fit-analysis.md)** ].

| Funkcija | Pašreizējā funkcionalitāte plānošanas optimizācijā |
|---|---|
| Pieļaujamā svara preces | Pieļaujamā svara preces tiek uzskatītas par parastām precēm.|
| Paplašināmās dimensijas | Paplašināmās dimensijas plānotajiem pasūtījumiem ir tukšas, pat ja lapā **Noliktavas dimensiju grupas** vai **Izsekošanas dimensiju grupas** ir atzīmēta izvēles rūtiņa **Vajadzības plāns pēc dimensijas**. |
| Filtrētas ražošanas izpildes | Sīkāku informāciju skatiet [Ražošanas plānošana — filtri](production-planning.md#filters). |
| Prognožu plānošana | Budžeta plānošana netiek atbalstīta. Ieteicams izmantot vispārējo plānošanu, kur budžeta modelis ir piešķirts vispārējai plānam. |
| Plānoto pasūtījumu numuru secība | Plānoto pasūtījumu numuru sērijas netiek atbalstītas. Plānoto pasūtījumu numuri tiek ģenerēti pakalpojuma pusē. Plānotais pasūtījuma numurs parasti tiek veidots no 10 cipariem, bet secība faktiski ir veidota no 20 rakstzīmēm ar 10 cipariem, kas piešķirti plānošanas izpildes skaitam, un pārējie 10 cipari plānotajam pasūtījumu skaitam. |
| Plānot plāna kopēšanu, dzēšanu un plāna versijas tīrīšanu | <p>Tālāk minētās preces ir atspējotas **Vispārējās plānošanas \> Vispārējās plānošanas \> Uzturēšanas plānu** navigācijas rūtī:</p><ul><li>Plāna kopija</li><li>Dzēst plānu</li><li>Ieplānot versijas tīrīšanu</li></ul> |
| Atgrieztie pasūtījumi | Atgriešanas pasūtījumi netiek izskatīti. |
| Ar plānošanu saistītās funkcijas | Papildinformāciju skatiet sadaļā [Plānošana ar neierobežotu noslodzi](infinite-capacity-planning.md#limitations). |
| Drošības rezerves izpilde | Plānošanas optimizācija vienmēr lieto opciju *Šodienas datums + iepirkuma laiks* lapas **Krājumu segums** laukā **Izpildīt minimumu**. Tādējādi var novērst nevēlamus plānotos pasūtījumus un citas problēmas, ja sagādes laiks nav iekļauts drošības krājumos, plānotie pasūtījumi, kas izveidoti pašreizējam ar zemu pieejamības līmeni esošajam krājumam, izpildes laika dēļ vienmēr tiks aizkavēti. |
| Drošības rezerves piesaiste un neto prasības | Prasības tips *Drošības rezerve* nav iekļauts un netiek rādīts lapā **Neto prasības**. Drošības rezerve neatspoguļo pieprasījumu, un ar to nav saistīts prasības datums. Tā vietā tā nosaka ierobežojumu tam, cik daudz krājumam ir jābūt vienmēr klātesošam. Taču lauka **Minimums** vērtība joprojām tiek ņemta vērā, aprēķinot plānotos pasūtījumus galvenās plānošanas laikā. Iesakām pārbaudīt **Uzkrātā daudzuma** kolonnu lapā **Neto prasības**, lai redzētu, vai šī vērtība tika ņemta vērā. |
| Transportēšanas kalendārs | Vērtība lapā **Piegādes režīmi** kolonnā **Transportēšanas kalendārs** tiek ignorēta. |
| Min./maks. vajadzību kods bez vērtībām| Ar iebūvēto plānošanas programmu, kad izmantojat min/maks. seguma kodu, kur nav iestatītas minimālās vai maksimālās vērtības, plānošanas programma apstrādā seguma kodu kā prasību un izveido vienu pasūtījumu katrai prasībai. Ar plānošanas optimizāciju sistēma izveidos vienu pasūtījumu dienā, lai segtu pilnu šīs dienas summu.  |
| Neto vajadzības un manuāli izveidoti plānotie pasūtījumi | Ar iebūvēto plānošanas programmu manuāli izveidoti piegādes pasūtījumi krājumam automātiski parādās starp šī krājuma neto prasībām. Piemēram, veidojot pirkšanas pasūtījumu no pārdošanas pasūtījuma, pirkšanas pasūtījums tiek parādīts **Neto prasību lapā**, neprasot iepriekšējas darbības. Tas ir tāpēc, ka iebūvētā plānošanas programma reģistrē krājumu `inventLogTTS`**darbības tabulā un parāda izmaiņas dinamisko plānu** neto prasību lapā. Tomēr, izmantojot plānošanas optimizāciju, manuāli izveidotie pasūtījumi neparādīsies starp krājuma neto prasībām līdz plānošanas optimizācijas palaišanai (izmantojot plānu, kas ietver krājumu) **\>** **vai** līdz brīdim, kad atlasīsiet Atjaunināt vispārējo plānošanu darbību rūtī neto prasību lapā, kas izpildīs krājuma vispārējo plānošanu. Papildinformāciju par to, kā strādāt ar neto **prasību lapu**, skatiet sadaļā [Neto prasības un piesaistes informācija par plānošanas optimizāciju](net-requirements.md). |

## <a name="additional-resources"></a>Papildu resursi

- [Plānošanas optimizācijas atbilstības analīze](planning-optimization-fit-analysis.md)
- [Parametri, kas netiek izmantoti plānošanas optimizācijai](not-used-parameters.md)
- [Datuma un laika parametri, kas tiek izmantoti plānošanas optimizācijai](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
