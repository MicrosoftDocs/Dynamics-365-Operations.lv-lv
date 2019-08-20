---
title: Uzņēmuma koncepts Common Data Service
description: Šajā tēmā ir aprakstīta uzņēmuma datu integrācija starp Finance and Operations un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6eddd87c3ad3ea9de8aec2874b0514faa65374f1
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789219"
---
## <a name="company-concept-in-common-data-service"></a>Uzņēmuma koncepts Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Programmā Microsoft Dynamics 365 for Finance and Operations koncepts *uzņēmums* ir gan juridiska konstrukcija, gan biznesa konstrukcija. Tā ir arī datu drošības un redzamības robeža. Lietotāji vienmēr strādā viena uzņēmuma kontekstā, un lielāko daļu datu izslēdz uzņēmums.

Common Data Service nav līdzvērtīga koncepta. Tuvākais koncepts ir *biznesa vienība*, kas galvenokārt ir lietotāja datu drošības un redzamības robeža. Šim konceptam nav tādas pašas juridiskās vai biznesa ietekmes kā uzņēmuma konceptam Finance and Operations.

Tā kā biznesa vienība un uzņēmums nav līdzvērtīgi koncepti, nav iespējams piespiest vienu pret vienu (1:1) kartēšanu starp tiem Common Data Service integrācijas nolūkā. Tomēr, tā kā lietotājiem pēc noklusējuma ir jābūt iespējai skatīt tos pašus ierakstus programmā Finance and Operations un Common Data Service, Microsoft ir ieviesis jaunu entītiju Common Data Service ar nosaukumu cdm\_Uzņēmums. Šī entītija ir līdzvērtīga uzņēmuma entītijai programmā Finance and Operations. Lai palīdzētu garantēt, ka ierakstu redzamība ir līdzvērtīga starp Finance and Operations un Common Data Service standarta komplektācijā, mēs iesakām šādu iestatīšanu datiem Common Data Service:

+ Katram Finance and Operations uzņēmuma ierakstam, kas ir iespējots duālajam ierakstam, tiek izveidots saistītais CDM\_Uzņēmums ieraksts.
+ Kad CDM\_Uzņēmuma ieraksts ir izveidots un ir iespējots duālajam ierakstam, tiek izveidota noklusējuma biznesa vienība ar tādu pašu nosaukumu. Lai gan noklusējuma grupa šim biznesa vienībai tiek izveidota automātiski, biznesa vienība netiek izmantota.
+ Tiek izveidota atsevišķa īpašnieka grupa ar tādu pašu nosaukumu. Arī tā ir saistīta ar biznesa vienību.
+ Pēc noklusējuma jebkura ieraksta, kas tiek izveidots programmā Finance and Operations un duāli ierakstīts Common Data Service, īpašnieks tiek iestatīts uz grupu "DW Owner", kas ir saistīta ar attiecīgo biznesa vienību.

Nākamajos attēlos ir parādīts šīs datu iestatīšanas piemērs Common Data Service.

![Datu iestatīšana Common Data Service](media/dual-write-company-1.png)

Šīs konfigurācijas dēļ jebkurš ar USMF uzņēmumu saistītais Finance and Operations ieraksts pieder grupai, kas ir piesaistīta USMF biznesa vienībai Common Data Service. Tādēļ jebkurš lietotājs, kuram ir piekļuve šai biznesa vienībai, izmantojot drošības lomu, kas ir iestatīta uz biznesa vienības līmeņa redzamību, tagad var redzēt šos ierakstus. Nākamajā piemērā parādīts, kā grupas var tikt izmantotas, lai nodrošinātu pareizo piekļuvi šiem ierakstiem.

+ "Pārdošanas vadītāja" loma ir piešķirta "USMF pārdošanas" grupas dalībniekiem.
+ Lietotāji, kuriem ir "Pārdošanas vadītāja" loma, var piekļūt visiem konta ierakstiem, kas ir tās pašas biznesa vienības dalībnieki, kuras dalībnieki ir šie lietotāji.
+ "USMF pārdošanas" grupa ir saistīta ar iepriekš minēto USMF biznesa vienību.
+ Tādēļ "USMF pārdošanas" grupas dalībnieki var redzēt jebkuru kontu, kas pieder "USMF DW" lietotājam, kurš nācis no USMF uzņēmuma entītijas programmā Finance and Operations.

![Kā grupas var tikt izmantotas](media/dual-write-company-2.png)

Kā redzams iepriekšējā attēlā, šī 1:1 kartēšana starp biznesa vienību, uzņēmumu un grupu ir tikai sākumpunkts. Šajā piemērā jaunā "Eiropas" biznesa vienība tiek izveidota manuāli Common Data Service kā DEMF un ESMF vecākelements. Šī jaunā saknes biznesa vienība nav saistīta ar duālo ierakstu. Taču to var izmantot, lai grupas "EUR Sales" dalībniekiem piešķirtu piekļuvi konta datiem gan DEMF, gan ESMF, saistītajā drošības lomā iestatot datu redzamību uz **Vecākelementa/Pakārtotā elementa BU**.

Pēdējā tēma, kas jāapspriež, ir tas, kā duālais ieraksts nosaka, kurai īpašnieka grupai būtu jāpiešķir ieraksti. Šo uzvedību kontrolē lauks **Noklusējuma atbildīgā darba grupa** CDM\_Uzņēmuma ierakstā. Kad cdm\_Uzņēmuma ieraksts ir iespējots duālam ierakstam, spraudnis automātiski izveido saistīto biznesa vienību un īpašnieka grupu (ja tādas vēl nav) un iestata lauku **Noklusējuma atbildīgā darba grupa**. Administrators var mainīt šo lauku uz citu vērtību. Tomēr administrators nevar notīrīt lauku, kamēr entītija ir iespējota duālajam ierakstam.

![Noklusējuma atbildīgās darba grupas lauks](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Uzņēmuma svītrošana un sāknēšana

Common Data Service integrācija rada uzņēmuma paritāti, izmantojot uzņēmuma identifikatoru datu svītrošanai. Kā redzams nākamajā attēlā, visas uzņēmumam specifiskās entītijas tiek izvērstas tā, lai tām būtu relācija daudzi pret vienu (N:1) ar cdm\_Uzņēmuma entītiju.

![N:1 relācija starp uzņēmumam specifisko entītiju un entītiju cdm_Company](media/dual-write-bootstrapping.png)

+ Pēc tam, kad uzņēmums ir pievienots un saglabāts, ierakstiem vērtība kļūst tikai lasāma. Tādēļ lietotājiem jāpārliecinās, ka tie atlasa pareizo uzņēmumu.
+ Tikai ieraksti, kuriem ir uzņēmuma dati, ir tiesīgi uz duālajiem ierakstiem starp Finance and Operations un Common Data Service.
+ Esošajiem Common Data Service datiem drīzumā būs pieejama administratora vadītas sāknēšanas pieredze.
