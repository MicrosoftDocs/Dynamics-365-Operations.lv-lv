---
title: Uzņēmuma koncepts Dataverse
description: Šajā tēmā aprakstīta uzņēmuma datu integrācija starp programmām Finance and Operations un Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 2f0e3950f2b35dd8b8dbf50601b7d6b6d624863e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683679"
---
# <a name="company-concept-in-dataverse"></a>Uzņēmuma koncepts Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Programmā Finance and Operations koncepts *uzņēmums* ir gan juridiska konstrukcija, gan biznesa konstrukcija. Tā ir arī datu drošības un redzamības robeža. Lietotāji vienmēr strādā viena uzņēmuma kontekstā, un lielāko daļu datu izslēdz uzņēmums.

Dataverse nav līdzvērtīga koncepta. Tuvākais koncepts ir *biznesa vienība*, kas galvenokārt ir lietotāja datu drošības un redzamības robeža. Šim konceptam nav tādas pašas juridiskās vai biznesa ietekmes kā uzņēmuma konceptam.

Tā kā biznesa vienība un uzņēmums nav līdzvērtīgi koncepti, nav iespējams piespiest vienu pret vienu (1:1) kartēšanu starp tiem Dataverse integrācijas nolūkā. Tomēr, tā kā lietotājiem pēc noklusējuma ir jābūt iespējai skatīt tās pašas rindas programmā un Dataverse, Microsoft ir ieviesis jaunu entītiju Dataverse ar nosaukumu cdm\_Uzņēmums. Šī entītija ir līdzvērtīga uzņēmuma entītijai programmā. Lai palīdzētu garantēt, ka rindu redzamība ir līdzvērtīga starp programmu un Dataverse standarta komplektācijā, mēs iesakām šādu iestatīšanu datiem Dataverse:

+ Katrai Finance and Operations uzņēmuma rindai, kas ir iespējota duālajam ierakstam, tiek izveidota saistīta cmd\_uzņēmums rinda.
+ Kad CDM\_Uzņēmums rinda ir izveidota un ir iespējota duālajam ierakstam, tiek izveidota noklusējuma biznesa vienība ar tādu pašu nosaukumu. Lai gan noklusējuma grupa šim biznesa vienībai tiek izveidota automātiski, biznesa vienība netiek izmantota.
+ Tiek izveidota atsevišķa īpašnieka grupa ar tādu pašu nosaukumu. Arī tā ir saistīta ar biznesa vienību.
+ Pēc noklusējuma jebkuras rindas, kas tiek izveidota un duāli ierakstīta Dataverse, īpašnieks tiek iestatīts uz grupu "DW Owner", kas ir saistīta ar attiecīgo biznesa vienību.

Nākamajos attēlos ir parādīts šīs datu iestatīšanas piemērs Dataverse.

![Datu iestatīšana Dataverse](media/dual-write-company-1.png)

Šīs konfigurācijas dēļ jebkura ar USMF uzņēmumu saistītā rinda pieder grupai, kas ir piesaistīta USMF biznesa vienībai Dataverse. Tādēļ jebkurš lietotājs, kuram ir piekļuve šai biznesa vienībai, izmantojot drošības lomu, kas ir iestatīta uz biznesa vienības līmeņa redzamību, tagad var redzēt šīs rindas. Nākamajā piemērā parādīts, kā grupas var tikt izmantotas, lai nodrošinātu pareizo piekļuvi šīm rindām.

+ "Pārdošanas vadītāja" loma ir piešķirta "USMF pārdošanas" grupas dalībniekiem.
+ Lietotāji, kuriem ir "Pārdošanas vadītāja" loma, var piekļūt visām konta rindām, kas ir tās pašas biznesa vienības dalībnieki, kuras dalībnieki ir šie lietotāji.
+ "USMF pārdošanas" grupa ir saistīta ar iepriekš minēto USMF biznesa vienību.
+ Tādēļ "USMF pārdošanas" grupas dalībnieki var redzēt jebkuru kontu, kas pieder "USMF DW" lietotājam, kurš nācis no USMF uzņēmuma entītijas programmā Finance and Operations.

![Kā grupas var tikt izmantotas](media/dual-write-company-2.png)

Kā redzams iepriekšējā attēlā, šī 1:1 kartēšana starp biznesa vienību, uzņēmumu un grupu ir tikai sākumpunkts. Šajā piemērā jaunā "Eiropas" biznesa vienība tiek izveidota manuāli Dataverse kā DEMF un ESMF vecākelements. Šī jaunā saknes biznesa vienība nav saistīta ar duālo ierakstu. Taču to var izmantot, lai grupas "EUR Sales" dalībniekiem piešķirtu piekļuvi konta datiem gan DEMF, gan ESMF, saistītajā drošības lomā iestatot datu redzamību uz **Vecākelementa/Pakārtotā elementa BU**.

Pēdējā tēma, kas jāapspriež, ir tas, kā duālais ieraksts nosaka, kurai īpašnieka grupai būtu jāpiešķir rindas. Šo uzvedību kontrolē lauks **Noklusējuma atbildīgā darba grupa** CDM\_Uzņēmums rindā. Kad cdm\_Uzņēmums rinda ir iespējota duālam ierakstam, spraudnis automātiski izveido saistīto biznesa vienību un īpašnieka grupu (ja tādas vēl nav) un iestata lauku **Noklusējuma atbildīgā darba grupa**. Administrators var mainīt šo lauku uz citu vērtību. Tomēr administrators nevar notīrīt lauku, kamēr entītija ir iespējota duālajam ierakstam.

> [!div class="mx-imgBorder"]
![Noklusējuma atbildīgās darba grupas lauks](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Uzņēmuma svītrošana un sāknēšana

Dataverse integrācija rada uzņēmuma paritāti, izmantojot uzņēmuma identifikatoru datu svītrošanai. Kā redzams nākamajā attēlā, visas uzņēmumam specifiskās tabulas tiek izvērstas tā, lai tām būtu relācija daudzi pret vienu (N:1) ar cdm\_Uzņēmuma entītiju.

> [!div class="mx-imgBorder"]
![N:1 relācija starp uzņēmumam specifisko entītiju un entītiju cdm_Company](media/dual-write-bootstrapping.png)

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

+ Ja esat sistēmas konfigurētājs vai administrators un vēlaties automātiski aizpildīt uzņēmuma datus pielāgotā veidlapā, varat izmantot [veidlapas notikumus](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Pievienojiet JavaScript atsauci **msdyn_/DefaultCompany.js** un izmantojiet tālāk norādītos notikumus. Jūs varat izmantot jebkuru veidlapu, piemēram, **Konta** veidlapu.

    + **OnLoad** notikumu veidlapai: iestatiet **defaultCompany** lauku.
    + **OnChange** notikums **Uzņēmuma** laukam: iestatiet **updateDefaultCompany** lauku.

## <a name="apply-filtering-based-on-the-company-context"></a>Lietot filtrēšanu, pamatojoties uz uzņēmuma kontekstu

Lai lietotu filtrēšanu, pamatojoties uz uzņēmuma kontekstu pielāgotās veidlapās vai pielāgotajos uzmeklēšanas laukos, kas pievienoti standarta veidlapām, atveriet veidlapu un izmantojiet **Saistīto ierakstu filtrēšanas** sadaļu, lai pielietotu uzņēmuma filtru. Tas ir jāiestata katram uzmeklēšanas laukam, kam ir nepieciešama filtrēšana, pamatojoties uz norādītajam uzņēmumam atbilstošo rindu. Šis iestatījums tiek parādīts **Kontam** sekojošajā ilustrācijā.

:::image type="content" source="media/apply-company-context.png" alt-text="Lietot uzņēmuma kontekstu":::

