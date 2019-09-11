---
title: Iepazīšanās ar darba pasūtījumiem
description: Šajā tēmā ir sniegts pārskats darba pasūtījumiem Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875785"
---
# <a name="introduction-to-work-orders"></a>Iepazīšanās ar darba pasūtījumiem

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Darba pasūtījumus izmanto, lai pārvaldītu, sniegtu nepieciešamo informāciju un reģistrētu patēriņu attiecībā uz uzturēšanas darbiem. Darba pasūtījums var saturēt vienu vai vairākus darba pasūtījuma darbus un darba pasūtījumam var pieslēgt vienu vai vairākus līdzekļus. Katra darba pasūtījuma rinda definē uzturēšanas darbu, kas ir ieplānots līdzeklim.

Darba pasūtījumus var izveidot automātiski vai manuāli:

- Automātiski izmantojot veidlapu **Plāna uzturēšanas plāni** kalendāra tipa uzturēšanas plāniem, kas iestatīti uz "Automātisko izveidošanu".  

- Automātiski izmantojot veidlapu **Plāna uzturēšanas cikli** kalendāra tipa uzturēšanas cikliem, kas iestatīti uz "Automātisko izveidošanu".  

- Izveidot no uzturēšanas grafika, ka var būt preventīvi uzturēšanas darbi vai uzturēšanas pieprasījumi.  

- Izveidojiet darba pasūtījumu manuāli.  

- Izveidot darba pasūtījumi **Visi uzturēšanas pieprasījumi** vai **Aktīvie uzturēšanas pieprasījumi** vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi**.

>[!NOTE]
>Darba pasūtījuma darbi, ka ir saistīti ar to pašu līdzekli, ir saistīti ar tādu pašu projekta ID.

## <a name="all-work-orders"></a>Visi darba pasūtījumi

Lai atvērtu sarakstu, noklikšķiniet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi**. **Visi darba pasūtījumi** satur sarakstu ar visiem darba pasūtījumiem un uzrāda daļu informācijas, kas saistīta ar darba pasūtījumu.

![1. attēls](media/01-work-orders.png)

- Lai redzētu aktīvo darba pasūtījumu sarakstu, noklikšķiniet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Aktīvie darba pasūtījumi**.

- Noklikšķiniet **Līdzekļu pārvaldība** > **Vispārīgi** > **Darba pasūtījumi** > **Mani funkcionālā novietojuma darba pasūtījuma uzturēšanas darbi**, lai redzētu sarakstu ar darba pasūtījuma darbiem, kuri satur līdzekļus, kas instalēti funkcionālā novietojumā, ar kuru esat saistīts kā speciālists (iestatīts sadaļā [Uzturēšanas speciālisti un speciālistu grupas](../setup-for-objects/workers-and-worker-groups.md)).

- Sarakstā **Visi darba pasūtījumi** (režģa skats), noklikšķiniet uz saites kolonnā **Darba pasūtījums**, lai uzrādītu izvēlētā ieraksta Detalizētu skatu. Noklikšķiniet pogu **Rediģēt**, lai atvērtu noklusējuma skatu rediģēšanai.  

- Detalizētajā skatā ir redzama detalizēta informācija, kas saistīta ar darba pasūtījumu.  

- Detalizētajā skatā atlasiet saiti **Rindas**, lai redzētu darba pasūtījuma darba informāciju, vai atlasiet saiti **Galvene**, lai redzētu darba pasūtījuma informāciju.  

- Vertikālā rūts **Saistīta informācija** ekrāna labajā pusē satur papildu informāciju, kas saistīta ar darba pasūtījumu. Izvērsiet rūti, lai redzētu saistīto informāciju atlasītajam darba pasūtījumam.  


![2. attēls](media/02-work-orders.png)


Darbības rūts pogas ir izkārtotas cilnēs darbības rūtī.  Neliels apraksts pogām saistībā ar Enterprise Asset Management:



| Pogas nosaukums                     | Apraksts                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Labot                            | Rediģēt atlasīto darba pasūtījumu.                                                                                                                                                                                                                                           |
| Jaunās                             | Izveidot jaunu darba pasūtījumu.                                                                                                                                                                                                                                                  |
| Dzēst                          | Dzēst atlasīto darba pasūtījumu.                                                                                                                                                                                                                                         |
| Darba pasūtījumu kopa                 | Pievienot atlasīto darba pasūtījumu darba pasūtījumu kopai vai izņemt no darba pasūtījumu kopas.                                                                                                                                                                                           |
| Koriģēt                          | Pielāgojiet informāciju par gaidāmo sākumu un beigām, servisa līmeni, atbildīgo uzturēšanas speciālistu vai atbildīgo uzturēšanas speciālistu grupu atlasītos darba pasūtījumos.                                                                                                                                     |
| Saistīts darba pasūtījums              | Izveidot jaunu darba pasūtījumu, kas saistīts ar atlasīto darba pasūtījuma darbu. Tas ir noderīgi, ja vēlaties reģistrēt primāros un sekundāros darba pasūtījumus.                                                                                                                              |
| Kopēt darba pasūtījumu                 | Izveidot darba pasūtījumu, pamatojoties uz esošu darba pasūtījumu.                                                                                                                                                                                                                |
| Notikumu vēsture                   | Skatīt darba pasūtījuma reģistrēšanas vēsturi.                                                                                                                                                                                                                |
| Darba pasūtījuma uzturēšanas darba piezīmes                           | Izveidojiet aprakstu vai ievadiet piezīmes vai piezīmes darba pasūtījumā. Sāciet, noklikšķinot pogu **Pievienot laikspiedolu**, lai piezīmei pievienotu savu lietotājvārdu un laikspiedolu. Piezīmes ir attēlotas veidlapā **Darba pasūtījums** > **Rindas informācija** FastTab > cilne **Apraksts**. |
| Rīki                           | Izveidojiet darba pasūtījumā nepieciešamo rīku sarakstu. Rīki ir iestatīti kā resursi **Organizācijas administrēšana** > **Vispārīgi** > **Resursi** > **Resursi**.                                                                                                      |
| Uzturēšanas kontrolsaraksts           | Skatīt pārbaudes sarakstu līdzeklim, kas pievienots darba pasūtījumam.                                                                                                                                                                                                              |
| Līdzekļa defekts                     | Skatīt vai reģistrēt kļūmes informāciju līdzeklim, kas ir jāizmanto kļūme pārvaldībai.                                                                                                                                                                                        |
| Dīkstāve uzturēšanas dēļ            | Konkretizēt darba pasūtījuma dīkstāvi uzturēšanas dēļ.                                                                                                                                                                                                                               |
| Nosacījumu novērtējums            | Reģistrēt nosacījuma novērtējuma mērījumus darba pasūtījumā.                                                                                                                                                                                                             |
| Līdzekļu skaitītāji                 | Izveidot vai skatītāju reģistrācijas līdzeklī.                                                                                                                                                                                                                     |
| Budžets                        | Skatīt vai izveidot prognozes darba pasūtījumā.                                                                                                                                                                                                                               |
| Žurnāli                        | Skatīt vai izveidot darba pasūtījumu žurnālus. Žurnāla rindas var nokopēt no prognozēm.                                                                                                                                                                                         |
| Projektu darbības            | Skatīt visus ievietots darījumus, ka saistīti ar darba pasūtījumiem, kas izveidoti līdzeklim.                                                                                                                                                                                             |
| Darba pasūtījuma statusa atjaunināšana                | Darba pasūtījuma dzīves cikla stāvokļa atjaunināšana.                                                                                                                                                                                                                                                |
| Dzīves cikla stāvokļa žurnāls                       | Žurnāls, kurā uzrādīti atlasītā darba pasūtījuma dzīves cikla stāvokļi.                                                                                                                                                                                                                   |
| Līdzekļu dokumenti                | Skatīt sarakstu ar dokumentiem, kas pievienoti līdzekļiem, kas ir saistīti ar darba pasūtījumu. Šie dokumenti ir iestatīti **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu dokumenti**.                                                                                                 |
| Ieplānošana                        | Ieplānojiet atlasītos darba pasūtījumus.                                                                                                                                                                                                                                      |
| Nosūtīt            | Ieplānojiet atlasīto darba pasūtījumu vienam speciālistam.                                                                                                                                                                                                                        |
| Dzēst grafiku                 | Dzēst atlasītā darba pasūtījuma ieplānošanu.                                                                                                                                                                                                                          |
| Atlasītie darba pasūtījuma uzturēšanas darbi.             | Atvērt saraksta **Ieplānotie darba pasūtījuma uzturēšanas darbi** lapu.                                                                                                                                                                                                                             |
| Darba pasūtījuma pirkšanas pieprasījums | Atvērt saraksta **Darba pasūtījuma pieprasījums** lapu.                                                                                                                                                                                                                 |
| Darba pasūtījuma iegāde             | Atvērt saraksta **Darba pasūtījuma pirkums** lapu.                                                                                                                                                                                                                             |
| Izmaksu kontrole                    | Salīdzināt budžeta izmaksas un reālās izmaksas darba pasūtījumā.                                                                                                                                                                                                                |
| Stundu kontrole                    | Salīdziniet prognozēto un reālo laiku darba pasūtījumā.                                                                                                                                                                                                                |
| Darba pasūtījuma pārskats               | Drukāt darba pasūtījuma ziņojumu.                                                                                                                                                                                                                                                |
| Darba pasūtījuma patēriņš          | Drukāt patēriņa ziņojumu.                                                                                                                                                                                                                                               |


Grupas cilnes **Darba pasūtījum** > grupā **Projekts** attiecas uz funkcionalitāti modulī **Projekta pārvaldība un grāmatvedība** saistībā ar prognozēm, žurnāliem un rēķiniem.

>[!NOTE]
>Prognozes, kas izveidotas darba pasūtījumā, var iekļaut, darbinot galveno plānošanu, izmantojot prognozes modeli, kas atlasīts veidlapā **Līdzekļu pārvaldības parametri**.

