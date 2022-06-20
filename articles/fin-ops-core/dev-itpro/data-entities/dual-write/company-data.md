---
title: Uzņēmuma koncepcija pakalpojumā Dataverse
description: Šajā rakstā ir aprakstīta uzņēmuma datu integrācija starp Finansēm un Operācijām un Dataverse.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11355031714b7e046f70bd5840297d66aa7d32e0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873183"
---
# <a name="company-concept-in-dataverse"></a>Uzņēmuma koncepts Dataverse

[!include [banner](../../includes/banner.md)]




Programmā Finance and Operations koncepts *uzņēmums* ir gan juridiska konstrukcija, gan biznesa konstrukcija. Tā ir arī datu drošības un redzamības robeža. Lietotāji vienmēr strādā viena uzņēmuma kontekstā, un lielāko daļu datu izslēdz uzņēmums.

Dataverse nav līdzvērtīga koncepta. Tuvākais koncepts ir *biznesa vienība*, kas galvenokārt ir lietotāja datu drošības un redzamības robeža. Šim konceptam nav tādas pašas juridiskās vai biznesa ietekmes kā uzņēmuma konceptam.

Tā kā biznesa vienība un uzņēmums nav līdzvērtīgi koncepti, nav iespējams piespiest vienu pret vienu (1:1) kartēšanu starp tiem Dataverse integrācijas nolūkā. Tomēr, tā kā lietotājiem pēc noklusējuma ir jābūt iespējai skatīt tās pašas rindas programmā un Dataverse, Microsoft ir ieviesis jaunu tabulu Dataverse ar nosaukumu cdm\_Uzņēmums. Šī tabula ir līdzvērtīga uzņēmuma tabulai programmā. Lai palīdzētu garantēt, ka rindu redzamība ir līdzvērtīga starp programmu un Dataverse standarta komplektācijā, mēs iesakām šādu iestatīšanu datiem Dataverse:

+ Katrai finanšu un operāciju uzņēmuma rindai, kas ir aktivizēta duālā rakstīšanai, tiek izveidota saistītā CDM\_ uzņēmuma rinda.
+ Kad CDM\_Uzņēmums rinda ir izveidota un ir iespējota duālajam ierakstam, tiek izveidota noklusējuma biznesa vienība ar tādu pašu nosaukumu. Lai gan noklusējuma grupa šim biznesa vienībai tiek izveidota automātiski, biznesa vienība netiek izmantota.
+ Tiek izveidota atsevišķa īpašnieka grupa ar tādu pašu nosaukumu. Arī tā ir saistīta ar biznesa vienību.
+ Pēc noklusējuma jebkuras rindas, kas tiek izveidota un duāli ierakstīta Dataverse, īpašnieks tiek iestatīts uz grupu "DW Owner", kas ir saistīta ar attiecīgo biznesa vienību.

Nākamajos attēlos ir parādīts šīs datu iestatīšanas piemērs Dataverse.

![Datu iestatīšana Dataverse.](media/dual-write-company-1.png)

Šīs konfigurācijas dēļ jebkura ar USMF uzņēmumu saistītā rinda pieder grupai, kas ir piesaistīta USMF biznesa vienībai Dataverse. Tādēļ jebkurš lietotājs, kuram ir piekļuve šai biznesa vienībai, izmantojot drošības lomu, kas ir iestatīta uz biznesa vienības līmeņa redzamību, tagad var redzēt šīs rindas. Nākamajā piemērā parādīts, kā grupas var tikt izmantotas, lai nodrošinātu pareizo piekļuvi šīm rindām.

+ "Pārdošanas vadītāja" loma ir piešķirta "USMF pārdošanas" grupas dalībniekiem.
+ Lietotāji, kuriem ir "Pārdošanas vadītāja" loma, var piekļūt visām konta rindām, kas ir tās pašas biznesa vienības dalībnieki, kuras dalībnieki ir šie lietotāji.
+ "USMF pārdošanas" grupa ir saistīta ar iepriekš minēto USMF biznesa vienību.
+ Tāpēc grupas USMF pārdošanas dalībnieki var redzēt jebkuru kontu, kas pieder "USMF DW" lietotājam, kas būtu no uzņēmuma tabulas USMF Finansēs un operācijās.

![Kā grupas var tikt izmantotas.](media/dual-write-company-2.png)

Kā redzams iepriekšējā attēlā, šī 1:1 kartēšana starp biznesa vienību, uzņēmumu un grupu ir tikai sākumpunkts. Šajā piemērā jaunā "Eiropas" biznesa vienība tiek izveidota manuāli Dataverse kā DEMF un ESMF vecākelements. Šī jaunā saknes biznesa vienība nav saistīta ar duālo ierakstu. Taču to var izmantot, lai grupas "EUR Sales" dalībniekiem piešķirtu piekļuvi konta datiem gan DEMF, gan ESMF, saistītajā drošības lomā iestatot datu redzamību uz **Vecākelementa/Pakārtotā elementa BU**.

Pēdējais dokuments, kurā ir aprakstīts, kā dubultās rakstīšanas nosaka, kurai īpašnieka komandai jāpiešķir rindas. Šo uzvedību kontrolē kolonna **Noklusējuma atbildīgā darba grupa** CDM\_Uzņēmums rindā. Kad cdm\_Uzņēmums rinda ir iespējota duālam ierakstam, spraudnis automātiski izveido saistīto biznesa vienību un īpašnieka grupu (ja tādas vēl nav) un iestata kolonnu **Noklusējuma atbildīgā darba grupa**. Administrators var mainīt šo kolonnu uz citu vērtību. Tomēr administrators nevar notīrīt kolonnu, kamēr tabula ir iespējota duālajam ierakstam.

> [!div class="mx-imgBorder"]
![Noklusējuma atbildīgās darba grupas kolonna.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Uzņēmuma svītrošana un sāknēšana

Dataverse integrācija rada uzņēmuma paritāti, izmantojot uzņēmuma identifikatoru datu svītrošanai. Kā redzams nākamajā attēlā, visas uzņēmumam specifiskās tabulas tiek izvērstas tā, lai tām būtu relācija daudzi pret vienu (N:1) ar cdm\_Uzņēmuma tabulu.

> [!div class="mx-imgBorder"]
![N:1 relācija starp uzņēmumam specifisko tabulu un cdm_Uzņēmuma tabula.](media/dual-write-bootstrapping.png)

+ Pēc tam, kad uzņēmums ir pievienots un saglabāts, rindu vērtība kļūst tikai lasāma. Tādēļ lietotājiem jāpārliecinās, ka tie atlasa pareizo uzņēmumu.
+ Tikai rindas, kurās ir uzņēmuma dati, ir piemērotas duālajiem ierakstiem starp programmu un Dataverse.
+ Esošajiem Dataverse datiem drīzumā būs pieejama administratora vadītas sāknēšanas pieredze.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Automātiski pievienot uzņēmuma nosaukumu klientu iesaistīšanās lietojumprogrammās

Ir vairāki veidi, kā automātiski aizpildīt uzņēmuma nosaukumu klientu iesaistīšanās lietojumprogrammās.

+ Ja esat sistēmas administrators, varat iestatīt noklusējuma uzņēmumu, pārvietojoties uz **Papildu iestatījumi > Sistēma > Drošība > Lietotāji**. Atveriet **Lietotāja** veidlapu un sadaļā **Organizācijas informācija** iestatiet vērtību **Uzņēmuma noklusējums veidlapās**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Iestatiet noklusējuma uzņēmumu Organizācijas informācijas sadaļā.":::

+ Ja jums ir **Rakstīšanas** piekļuve **SystemUser** vienībai **Biznesa struktūrvienības** līmenī, varat mainīt noklusējuma uzņēmumu jebkurā veidlapā, atlasot uzņēmumu no **Uzņēmumu** nolaižamās izvēlnes.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Uzņēmuma nosaukuma maiņa jaunā kontā.":::

+ Ja jums ir **Rakstīšanas** piekļuve datiem vairāk nekā vienā uzņēmumā, varat mainīt noklusējuma uzņēmumu, izvēloties rindu, kas pieder citam uzņēmumam.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Izvēloties rindu, mainās noklusējuma uzņēmums.":::

+ Ja esat sistēmas konfigurētājs vai administrators un vēlaties automātiski aizpildīt uzņēmuma datus pielāgotā veidlapā, varat izmantot [veidlapas notikumus](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Pievienojiet JavaScript atsauci **msdyn_/DefaultCompany.js** un izmantojiet tālāk norādītos notikumus. Jūs varat izmantot jebkuru veidlapu, piemēram, **Konta** veidlapu.

    + **OnLoad** notikumu veidlapai: iestatiet kolonnu **defaultCompany**.
    + **OnChange** notikums **Uzņēmuma** kolonnā: iestatiet kolonnu **updateDefaultCompany**.

## <a name="apply-filtering-based-on-the-company-context"></a>Lietot filtrēšanu, pamatojoties uz uzņēmuma kontekstu

Lai lietotu filtrēšanu, pamatojoties uz uzņēmuma kontekstu pielāgotās veidlapās vai pielāgotajos uzmeklēšanas laukos, kas pievienoti standarta veidlapām, atveriet veidlapu un izmantojiet **Saistīto ierakstu filtrēšanas** sadaļu, lai pielietotu uzņēmuma filtru. Tas ir jāiestata katram uzmeklēšanas laukam, kam ir nepieciešama filtrēšana, pamatojoties uz norādītajam uzņēmumam atbilstošo rindu. Šis iestatījums tiek parādīts **Kontam** sekojošajā ilustrācijā.

:::image type="content" source="media/apply-company-context.png" alt-text="Lietot uzņēmuma kontekstu.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]