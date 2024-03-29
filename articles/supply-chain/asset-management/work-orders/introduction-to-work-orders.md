---
title: Ievads par darba pasūtījumiem
description: Šajā rakstā ir sniegts pārskats par darba pasūtījumiem Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5eb911ec4ba9655c4ecaea3bf9a4f8736fa036c2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016715"
---
# <a name="introduction-to-work-orders"></a>Ievads par darba pasūtījumiem

[!include [banner](../../includes/banner.md)]



Darba pasūtījumus izmanto, lai pārvaldītu uzturēšanas darbus, sniegtu tām nepieciešamo informāciju un reģistrētu patēriņu attiecībā uz tiem. Katrs darba pasūtījums var saturēt vienu vai vairākus darba pasūtījuma darbus un katram darba pasūtījumam var pieslēgt vienu vai vairākus līdzekļus. Katrs darba pasūtījuma darbs definē uzturēšanas darbu, kas ir ieplānots līdzeklim.

Darba pasūtījumus var izveidot šādos veidos:

- Kalendāra tipa uzturēšanas plāniem, kur iestatījums “Automātiskā izveidošana” ir ieslēgts automātiski, izmantojot veidlapu [Plāna uzturēšanas plāni](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md).

- Uzturēšanas cikliem, kur iestatījums “Automātiskā izveidošana” ir ieslēgts automātiski, izmantojot veidlapu [Plāna uzturēšanas cikli](../preventive-and-reactive-maintenance/maintenance-rounds.md).

- Preventīviem uzturēšanas darbiem vai uzturēšanas pieprasījumiem, no [Uzturēšanas plāns](../preventive-and-reactive-maintenance/maintenance-schedule.md)

- Manuāli

- No **Visi uzturēšanas pieprasījumi**, **Aktīvie uzturēšanas pieprasījumi**, vai **Mani funkcionālā novietojuma uzturēšanas pieprasījumi** lapas.

>[!NOTE]
>Darba pasūtījuma darbi, kas ir saistīti ar to pašu līdzekli, ir saistīti ar tādu pašu projekta ID.

## <a name="all-work-orders"></a>Visi darba pasūtījumi

Atlasiet **Līdzekļu pārvaldības darbs** > **pasūtījumus** > **visiem darba pasūtījumiem**, lai atvērtu **saraksta lapu Visi** darba pasūtījumi. Šajā lapā tiek rādīti visi darba pasūtījumi un daļa informācijas, kas ir saistīta ar katru no tiem.

Zemāk redzamajā ilustrācijā ir parādīts sarakstu lapas **Visi darba pasūtījumi** piemērs.

![1. attēls.](media/01-work-orders.png)

Lai skatītu tikai aktīvo darba pasūtījumu sarakstu, atlasiet Līdzekļu pārvaldības **darba pasūtījumi** > **aktīvie** > **darba pasūtījumi**. 

Lai skatītu darbu pasūtījumu darbu sarakstu, kas ietver līdzekļus, kas ir instalēti funkcionālās vietās, kuras esat saistīts kā darbinieks, **·** > **·** > **atlasiet Līdzekļu vadības darba pasūtījumi Manas funkcionālās atrašanās vietas darba pasūtījuma uzturēšanas darbi.** (Saikne starp darbiniekiem un funkcionālajiem novietojumiem ir iestatīta lapā **Speciālisti** .) Papildinformāciju skatiet sadaļā [Uzturēšanas darbinieki un darbinieku grupas](../setup-for-objects/workers-and-worker-groups.md).)

Tālāk ir norādīti daži veidi, kā varat izmantot **Visi darba pasūtījumi** lapu:

- Režģa skatā atlasiet saiti kolonnā **Darba pasūtījums**, lai parādītos atlasītā ieraksta detalizēts skats. Pēc tam varat atlasīt **Rediģēt**, lai atvērtu ierakstu rediģēšanai.

- Detalizētajā skatā parādās detalizēta informācija, kas saistīta ar darba pasūtījumu.  

- Detalizētajā skatā atlasiet cilni **Rindas**, lai skatītu detalizēto informāciju par darba pasūtījuma darbu, vai atlasiet cilni **Galvene**, lai skatītu detalizēto informāciju par darba pasūtījumu.  

- Izvērsiet rūti **Saistītā informācija** lapas labajā pusē, lai skatītu papildu informāciju, kas saistīta ar atlasīto darba pasūtījumu.

Zemāk redzamajā ilustrācijā ir parādīts detalizētā skata **Visi darba pasūtījumi** piemērs.

![2. attēls.](media/02-work-orders.png)


Pogas darbības rūtī ir sakārtotas cilnēs. Šajā tabulā ir īsi aprakstītas pogas, kas saistītas ar Līdzekļu pārvaldību:



| Pogas nosaukums                     | Apraksts                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Labot                            | Rediģēt atlasīto darba pasūtījumu.                                                                                                                                                                                                                                           |
| Jaunās                             | Izveidot jaunu darba pasūtījumu.                                                                                                                                                                                                                                                  |
| Delete                          | Dzēst atlasīto darba pasūtījumu.                                                                                                                                                                                                                                         |
| Darba pasūtījumu kopa                 | Pievienot atlasīto darba pasūtījumu darba pasūtījumu kopai vai izņemt to no darba pasūtījumu kopas.                                                                                                                                                                                           |
| Koriģēt                          | Pielāgojiet informāciju par gaidāmo sākumu un beigām, servisa līmeni, atbildīgo uzturēšanas speciālistu vai atbildīgo uzturēšanas speciālistu grupu atlasītos darba pasūtījumos.                                                                                                                                     |
| Saistīts darba pasūtījums              | Izveidot jaunu darba pasūtījumu, kas saistīts ar atlasīto darba pasūtījuma darbu. Tas ir noderīgi, ja vēlaties reģistrēt primāros un sekundāros darba pasūtījumus.                                                                                                                              |
| Kopēt darba pasūtījumu                 | Izveidot darba pasūtījumu, kas ir pamatots uz esošu darba pasūtījumu.                                                                                                                                                                                                               |
| Notikumu vēsture                   | Skatīt darba pasūtījuma reģistrācijas vēsturi.                                                                                                                                                                                                                |
| Darba pasūtījuma uzturēšanas darba piezīmes                           | Izveidojiet darba pasūtījuma aprakstu vai ievadiet piezīmes par to. Vispirms atlasiet **Pievienot laikspiedolu**, lai piezīmei pievienotu savu lietotājvārdu un laikspiedolu. Piezīmes tiek rādītas cilnē **Apraksts**, kas atrodas kopsavilkuma cilnē **Detalizēta informācija par rindu** lapā **Darba pasūtījums**.         |
| Rīki                           | Izveidojiet darba pasūtījumā nepieciešamo rīku sarakstu. Rīki ir iestatīti kā resursi **Organizācijas administrēšana** > **Resursi** > **Resursi**.                                                                                                      |
| Uzturēšanas kontrolsaraksts           | Skatīt pārbaudes sarakstu līdzeklim, kas ir pievienots darba pasūtījumam.                                                                                                                                                                                                              |
| Līdzekļa defekts                     | Skatīt vai reģistrēt kļūmes informāciju pamatlīdzeklī. Informācija tiek izmantota kļūdu pārvaldībai.                                                                                                                                                                                      |
| Dīkstāve uzturēšanas dēļ            | Konkretizēt darba pasūtījuma dīkstāvi uzturēšanas dēļ.                                                                                                                                                                                                                               |
| Nosacījumu novērtējums            | Reģistrēt nosacījuma novērtējuma mērījumus darba pasūtījumā.                                                                                                                                                                                                             |
| Līdzekļu skaitītāji                 | Izveidot vai skatītāju reģistrācijas līdzeklī.                                                                                                                                                                                                                     |
| Budžets                        | Skatīt vai izveidot prognozes darba pasūtījumā.                                                                                                                                                                                                                               |
| Žurnāli                        | Skatīt vai izveidot darba pasūtījumu žurnālus. Žurnāla rindas var nokopēt no prognozēm.                                                                                                                                                                                         |
| Projektu darbības            | Skatīt visas ievietotas transakcijas, kas ir saistītas ar darba pasūtījumiem, kas ir izveidoti līdzeklim.                                                                                                                                                                                             |
| Darba pasūtījuma statusa atjaunināšana           | Atjaunināt darba pasūtījuma dzīves cikla stāvokļi.                                                                                                                                                                                                                                                |
| Dzīves cikla stāvokļa žurnāls                      | Skatiet žurnālu, kas rāda atlasītā darba pasūtījuma dzīves cikla stāvokļus.                                                                                                                                                                                                                   |
| Līdzekļu dokumenti                | Skatīt sarakstu ar dokumentiem, kas pievienoti līdzekļiem, kas saistīti ar darba pasūtījumu. Šie dokumenti ir iestatīti **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu dokumenti**.                                                                                                 |
| Ieplānošana                        | Ieplānojiet atlasītos darba pasūtījumus.                                                                                                                                                                                                                                      |
| Nosūtīt            | Ieplānojiet atlasīto darba pasūtījumu vienam speciālistam.                                                                                                                                                                                                                        |
| Dzēst grafiku                 | Dzēst izvēlētā darba pasūtījuma ieplānošanu.                                                                                                                                                                                                                          |
| Plānotie darba pasūtījuma uzturēšanas darbi             | Atvērt saraksta **Ieplānotie darba pasūtījuma uzturēšanas darbi** lapu.                                                                                                                                                                                                                             |
| Darba pasūtījuma pirkšanas pieprasījums | Atvērt saraksta **Darba pasūtījuma pieprasījums** lapu.                                                                                                                                                                                                                 |
| Darba pasūtījuma iegāde             | Atvērt saraksta **Darba pasūtījuma pirkums** lapu.                                                                                                                                                                                                                             |
| Izmaksu kontrole                    | Salīdzināt budžeta izmaksas un reālās izmaksas darba pasūtījumā.                                                                                                                                                                                                                |
| Stundu kontrole                    | Salīdziniet prognozēto un reālo laiku darba pasūtījumā.                                                                                                                                                                                                                |
| Darba pasūtījuma pārskats               | Drukāt darba pasūtījuma pārskatu.                                                                                                                                                                                                                                                |
| Darba pasūtījuma patēriņš          | Drukāt patēriņa pārskatu.                                                                                                                                                                                                                                               |


Pogas grupā **Projekts** Darbību rūts cilnē **Darba pasūtījums** ir saistīta ar prognožu, žurnālu un rēķinu funkcionalitāti modulī **Projektu pārvaldība un grāmatvedība**.

>[!NOTE]
>Lai iekļautu darba pasūtījumam izveidotās prognozes, darbinot vispārējo plānošanu, izmantojiet prognozes modeli, kas ir atlasīts lapā **Līdzekļu pārvaldības parametri**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]