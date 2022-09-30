---
title: Ierobežotas noslodzes plānošana un plānošana
description: Ierobežota noslodzes plānošana un plānošana palīdz izprast, cik daudz darba var saražot specifiskā periodā, kad tiek ņemti vērā ierobežojumi dažādiem resursiem.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: c5eebe9ef6258b43daa7c7007ee28b0278fe5b09
ms.sourcegitcommit: 1a7729a6ce4f3fcf68bdc4cfdad746a5553da3c5
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573150"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Ierobežotas noslodzes plānošana un plānošana

[!include [banner](../../includes/banner.md)]

Ierobežota noslodze ir pieeja, kas palīdz saprast, cik daudz darba var saražot specifiskā periodā, kad tiek ņemti vērā ierobežojumi dažādiem resursiem. Ierobežotas noslodzes plānošanas nolūks ir nodrošināt, lai darbs tiktu darīts vienmēr un efektīvā ražošanas procesa laikā.

Ierobežotas noslodzes plānošana un plānošana izveido reālāku ražošanas procesu grafiku, nekā izveido neierobežota noslodzes pieeja. Ja resursiem nepietiek noslodzes, piegādes datums tiks pabīdāms, un darbs tiks plānots, kad būs pietiekama noslodze.

## <a name="planning-optimization-support-for-finite-capacity-planning"></a>Plānošanas optimizācijas atbalsts ierobežotas noslodzes plānošanai

Ierobežotas noslodzes plānošana un plānošana darbojas ļoti vienādi neatkarīgi no tā, vai izmantojat plānošanas optimizāciju vai iebūvēto plānošanas programmu. Tomēr plānošanas optimizācijā netiek izmantots deficīta **laika perioda** parametrs. Izmantojot plānošanas optimizāciju, sastrēguma resursi vienmēr tiek plānoti, izmantojot tos pašus laika periodus, kas nav sastrēguma resursi (kā norādīts ar ierobežotās noslodzes laika periodu).

## <a name="set-up-finite-capacity-functionality"></a>Ierobežotās noslodzes funkcionalitātes iestatīšana

Lai izmantotu ierobežotas noslodzes funkcionalitāti, ir globāli jāiespējo noslodzes plānošana un jāiespējo ierobežotas noslodzes plānošana gan vispārējam plānam, kurā vēlaties to izmantot, gan katram resursam, uz kuru tas attiecas. Plāniem un resursiem, kuros ir aktivizēta ierobežota noslodze, plānoto ražošanas pasūtījumu plānošanā tiks apsvērta noslodze, kas jau ir rezervēta. Plānotie ražošanas pasūtījumi tiek iepriekš plānoti, sākot no pieprasījuma datuma. Ja noslodze nav pieejama saskaņā ar optimālo grafiku, sistēma mēģinās pieprasīt komponenta krājumus agrāk. Ja noslodze var mainīties kā vajadzības (piemēram, strādājot ar maiņās), nevajadzētu izmantot ierobežotās noslodzes funkcionalitāti, jo aprēķinātie apstrādes laiki nebūs pareizi. Plānošana apsver tikai noslodzi, kas jau ir rezervēta resursiem, kur ir aktivizēta ierobežota noslodze. Iespējojot resursa ierobežotu noslodzi, var modificēt ierobežotās noslodzes periodu.

### <a name="activate-master-planning-parameters"></a>Vispārējās plānošanas parametru aktivizēšana

Lai izmantotu ierobežotās noslodzes funkcionalitāti, ir jāiespējo noslodzes plānošana **vispārējās plānošanas parametru** lapā.

1. Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Vispārējas plānošanas parametri**.
1. Cilnes Plānotie **pasūtījumi** sadaļā Noslodzes **plānošana** iestatiet opciju **Ražošana** uz *Jā*.

### <a name="activate-a-master-plan"></a>Vispārējā plāna aktivizēšana

Katram vispārējai plānam, kur vēlaties to izmantot, ir jāiespējo ierobežotas noslodzes plānošana un plānošana.

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Saraksta rūtī atlasiet vispārējo plānu, kas jāiestata, lai izmantotu ierobežotās noslodzes plānošanu un plānošanu.
1. Kopsavilkuma cilnes **Vispārīgi** sadaļā Plānotie ražošanas **pasūtījumi** iestatiet opciju Ierobežota **noslodze** uz *Jā*.
1. Atkārtojiet 2. un 3. soli katram papildu vispārējai plānam, ko vēlaties iestatīt.

### <a name="activate-resources"></a>Aktivizēt resursus

Katram resursam, kur vēlaties to izmantot, ir jāiespējo ierobežota noslodzes plānošana un plānošana.

1. Dodieties uz **Ražošanas kontrole \> Uzstādīšana \> Resursi \> Resursi**.
1. Saraksta rūtī atlasiet resursu, ko vēlaties iestatīt ierobežotās noslodzes plānošanas un plānošanas izmantošanai.
1. Kopsavilkuma cilnes **Operācija** sadaļā Noslodze iestatiet **opciju** Ierobežota noslodze **uz** *Jā*.
1. Atkārtojiet 2. un 3. soli katram papildu resursam, ko vēlaties iestatīt.

## <a name="examples"></a>Piemēri

Šajā sadaļā sniegti turpmākie piemēri, kas parāda, kā strādāt gan ar neierobežoti, gan ar ierobežotu noslodzes plānošanu un plānošanu:

- 1. piemērs – neierobežotas noslodzes plānošana
- 2. piemērs – ierobežota noslodzes plānošana ar vienas dienas laika periodu
- 3. piemērs – ierobežotas noslodzes plānošana ar divu dienu laika periodu

### <a name="preconditions"></a>Priekšnosacījumi

Visi trīs piemēri pieņem šajā sadaļā aprakstītos priekšnosacījumus.

Precei *Product1* ir maršruts, kas satur šādas operācijas.

| Operācijas Nr. | Operācijas nosaukums | Resurss        | Izpildes laiks | Izlaides daudzums. | Nākamā |
|---------------|----------------|-----------------|----------|--------------|------|
| 10.            | Metināšanas        | Rindstarpas rinda    | 1        | 2            | 20   |
| 20            | Salikšana     | Salikšanas rinda | 1        | 4            |      |

Jūsu uzņēmuma darbinieki uz astoņām stundām strādā vienā maiņā (8:00–16:00).

Ieplānots ražošanas pasūtījums *24 gab.* Product1 *·*. Tā piegādes datums ir Šodiena *+ 3 dienas*.

Plānošanas rezultātā sistēma ielādē resursus šādā veidā:

- **Ierašanās rinda:** šis resurss ir ielādēts *no šodienas plkst. 8.00* *līdz šodienai + 1 plkst. 12:00*.
- **Salikšanas rinda:** šis resurss ir ielādēts no šodienas + 1 plkst. 12.00 *līdz* šodienai + 2 plkst. 10:00 *·*.

Šajā attēlā redzama iegūtā Ganta diagramma (atlasiet to lielākam skatam).

[![Ganta diagramma, kas rāda priekšnoteikumus.](media/finite-examples-conditions-small.png "Ganta diagramma, kas rāda priekšnoteikumus")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>1. piemērs – neierobežotas noslodzes plānošana

Šis piemērs parāda plānošanas rezultātus, ja ierobežotās noslodzes plānošanas vietā izmantojat neierobežotas noslodzes plānošanu.

Vispārējaim plānam ir šādi atbilstoši iestatījumi, kas deaktivizē plāna ierobežotās noslodzes plānošanu:

- **Ierobežota noslodze:** *Nē*

Opcija **Ierobežota noslodze arī** ir iestatīta uz *Nē abiem* atbilstošajiem resursiem, lai tiem atspējotu ierobežotu noslodzes plānošanu:

- Rindstarpas rinda
- Salikšanas rinda

Tagad jūs pievienojat jaunu pārdošanas pasūtījumu *8 gab* . no *Product1* un palaidiet plānu. Šī rezultāta rezultātā sistēma *no šodienas plkst. 8.00 līdz šodienai* *ielādē rindu no šodienas, plkst. 12.00*. Kad operācijas jūsu rindā ir pabeigtas, *sistēma ielādēs salikšanas rindu no šodienas plkst. 12.00* *līdz šodienai, plkst. 14:00*.

Šajā attēlā redzama iegūtā Ganta diagramma (atlasiet to lielākam skatam).

[![Ganta diagramma, kas rāda neierobežotas noslodzes plānošanas piemēru.](media/finite-examples-example1-small.png "Ganta diagramma, kas rāda neierobežotas noslodzes plānošanas piemēru")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>2. piemērs – ierobežota noslodzes plānošana ar vienas dienas laika periodu

Šis piemērs parāda plānošanas rezultātus, kad izmantojat ierobežotas noslodzes plānošanu un vienas dienas laika periodu.

Vispārējaim plānam ir šādi atbilstoši iestatījumi, kas aktivizē ierobežotas noslodzes plānošanu un iestata plānam laika periodu:

- **Ierobežota noslodze:** *Jā*
- **Ierobežotās noslodzes periods:** *1*

Opcija **Ierobežota noslodze arī** ir iestatīta uz Jā *abiem* atbilstošajiem resursiem, lai tiem iespējotu ierobežotu noslodzes plānošanu:

- Rindstarpas rinda
- Salikšanas rinda

Tagad jūs pievienojat jaunu pārdošanas pasūtījumu *8 gab* . no *Product1* un palaidiet plānu. Tādēļ sistēma noslodzi *no šodienas + 1 plkst. 8.00* *līdz šodienai + 1 plkst. 12:00*. Kad ir pabeigtas jūsu operācijas, *sistēma ielādēs salikšanas rindu no šodienas + 1 plkst. 12.00* *līdz šodienai + 1 plkst. 14.00*. Sistēma apsver ierobežoto noslodzi tikai vienai dienai.

Šajā attēlā redzama iegūtā Ganta diagramma (atlasiet to lielākam skatam).

[![Ganta diagramma, kas rāda ierobežotu noslodzes plānošanu ar vienas dienas laika periodu.](media/finite-examples-example2-small.png "Ganta diagramma, kas rāda ierobežotu noslodzes plānošanu ar vienas dienas laika periodu")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>3. piemērs – ierobežotas noslodzes plānošana ar divu dienu laika periodu

Šis piemērs parāda plānošanas rezultātus, ja izmantojat ierobežotas noslodzes plānošanu un divu dienu laika periodu.

Vispārējaim plānam ir šādi atbilstoši iestatījumi, kas aktivizē ierobežotas noslodzes plānošanu un iestata plānam laika periodu:

- **Ierobežota noslodze:** *Jā*
- **Ierobežotās noslodzes periods:** *2*

Opcija **Ierobežota noslodze arī** ir iestatīta uz Jā *abiem* atbilstošajiem resursiem, lai tiem iespējotu ierobežotu noslodzes plānošanu:

- Rindstarpas rinda
- Salikšanas rinda

Tagad jūs pievienojat jaunu pārdošanas pasūtījumu *8 gab* . no *Product1* un palaidiet plānu. Tādēļ sistēma noslogo jūsu *rindu no šodienas + 1 plkst. 12.00* *līdz šodienai + 1 plkst. 16:00*. Kad ir pabeigtas jūsu operācijas, *sistēma ielādēs salikšanas rindu no šodienas + 2 plkst. 8.00* *līdz šodienai + 2 plkst. 10:00*. Sistēma apsver ierobežoto noslodzi tikai uz divām dienām.

Šajā attēlā redzama iegūtā Ganta diagramma (atlasiet to lielākam skatam).

[![Ganta diagramma, kas rāda ierobežoto noslodzes plānošanu ar divu dienu laika periodu.](media/finite-examples-example3-small.png "Ganta diagramma, kas rāda ierobežoto noslodzes plānošanu ar divu dienu laika periodu")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Vienmēr vajadzētu iestatīt ierobežoto noslodzes periodu atbilstoši uzņēmuma vajadzībām. Šajā rakstā sniegti piemēri vienkārši attēlo funkcionalitāti. Realitātē vienas dienas laika periods, iespējams, ir pārāk zems lielākajai daļai ražotājiem, kas izmanto ierobežotās noslodzes plānošanu.
