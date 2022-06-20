---
title: Iepazīstināšana ar līdzekļiem
description: Šajā rakstā sniegts pārskats par pamatlīdzekļiem Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee61c43f93d68747a7095dc9317674a435553c8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874193"
---
# <a name="introduction-to-assets"></a>Iepazīstināšana ar līdzekļiem

[!include [banner](../../includes/banner.md)]

 

Šajā rakstā sniegts pārskats par pamatlīdzekļiem Līdzekļu pārvaldībā. *Līdzeklis* ir jebkura veida aprīkojums, piemēram, mašīna vai mašīnas daļa, kam nepieciešama uzturēšana, apkope vai remonts.

Līdzeklis tiek automātiski atjaunināts ar saistīto informāciju. Piemēram, šī saistītā informācija var būt par jauniem vai atjauninātiem darba pasūtījumiem. Varat izveidot līdzekļus, izmantojot izvēlnes elementu **Visi līdzekļi** vai izvēlnes elementu **Gaidošie līdzekļi**. Šajā rakstā ir izskaidrots, kā izveidot līdzekļus, izmantojot **izvēlnes elementu** Visi līdzekļi. Informāciju par to, kā veidot līdzekļus, izmantojot izvēlnes elementu **Gaidošie līdzekļi**, skatiet sadaļā [Līdzekļu izveide, pamatojoties uz pirkšanas pasūtījumiem](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Visi līdzekļi

Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Līdzekļi** \> **Visi līdzekļi**. Saraksta lapā **Visi līdzekļi** ir redzami visi līdzekļi un zināma ar tiem saistītā informācija. Lai skatītu tikai aktīvos līdzekļus, atlasiet **Aktīvie līdzekļi**. Lai skatītu tikai līdzekļus, kas uzstādīti funkcionālajos novietojumos, ar kuriem esat saistīts kā uzturēšanas darbinieks, atlasiet **Mani aktīvie līdzekļi**. (Šī saistība ir iestatīta lapā **Darbinieki**. Papildinformāciju skatiet sadaļā [Uzturēšanas darbinieki un darbinieku grupas](../setup-for-objects/workers-and-worker-groups.md).)

Režģa skatā **Visi līdzekļi** atlasiet saiti kolonnā **Līdzeklis**, lai skatītu detalizētu informāciju par atlasīto ierakstu. Lai rediģētu ierakstu, atlasiet pogu **Rediģēt**. Detalizētajā skatā tiek parādīta detalizēta informācija, kas ir saistīta ar līdzekli. Rūts labajā pusē **Saistītā informācija** ietver papildu ar līdzekli saistītu informāciju. Izvērsiet rūti, lai parādītu saistīto informāciju par atlasīto līdzekli.

Pogas darbības rūtī ir sakārtotas cilnēs. Nākamajā tabulā ir īsi aprakstītas pogas, kas saistītas ar Līdzekļu pārvaldību.

| Pogas nosaukums          | Apraksts                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Labot                 | Rediģēt atlasīto līdzekli.                                                                                                                                         |
| Jauna                  | Izveidot jaunu līdzekli.                                                                                                                                                |
| Dzēst               | Dzēst atlasīto līdzekli.                                                                                                                                       |
| Līdzekļa pārvietošana           | Pārvietojiet līdzekļus uz citu līdzekļu struktūru vai uz citu atrašanās vietu tajā pašā līdzekļu struktūrā.                                                                                         |
| Līdzekļu aizstāšana        | Aizstājiet vienu pakārtoto līdzekli līdzekļu hierarhijā ar citu līdzekli.                                                                                                  |
| Līdzekļa uzstādīšana        | Uzstādiet līdzekli funkcionālajā novietojumā.                                                                                                                          |
| Līdzekļa kopēšana           | Kopējiet līdzekļu hierarhiju uz citu līdzekli.                                                                                                                          |
| Pieprasījumi             | Atveriet saraksta lapu **Aktīvie pieprasījumi**, kur varat skatīt uzturēšanas pieprasījumus sarakstu, kas ir izveidoti atlasītajam līdzeklim.                                                                         |
| Notikuma vēsture        | Skatiet pārskatu par dažādām reģistrācijām, kas ir veiktas līdzeklim.                                                                                                         |
| Līdzekļa MK            | Skatiet visu līdzeklim izmantoto krājumu (rezerves daļu un citu vienumu) sarakstu.                                                                                  |
| Darba pasūtījumi          | Atveriet saraksta lapu **Aktīvie darba pasūtījumi**, kur varat skatīt līdzekļa darba pasūtījumus.                                                                                        |
| Kontrolsaraksts            | Skatiet pārskatu par uzturēšanas kontrolsarakstiem un mērījumiem, kas ir reģistrēti līdzeklim.                                                                                                 |
| Dīkstāve uzturēšanas dēļ | Veidojiet vai skatiet dīkstāves uzturēšanas dēļ reģistrācijas par līdzekli.                                                                                                       |
| Projektu darbības | Skatiet visas iegrāmatotās darbības, kas ir saistītas ar šim līdzeklim izveidotajiem darba pasūtījumiem.                                                                                       |
| Līdzekļu mēri       | Izveidojiet vai skatiet līdzekļa mērus līdzeklim.                                                                                                               |
| Uzturēšanas grafiks | Atveriet saraksta lapu **Atvērt uzturēšanas grafiku**, kurā var skatīt ar līdzekli saistītos uzturēšanas plānus, uzturēšanas pieprasījumus un uzturēšanas ciklus, kuru statuss ir **Izveidots**. |
| Līdzekļa stāvokļa atjaunināšana   | Atjauniniet līdzekļa dzīves cikla stāvokli. Varat atlasīt vairākus līdzekļus saraksta lapā **Visi līdzekļi** un pēc tam visiem vienlaikus atjaunināt līdzekļa dzīves cikla stāvokli.              |
| Dzīves cikla stāvokļa žurnāls  | Atveriet žurnālu, kas rāda atlasītā līdzekļa dzīves cikla stāvokļus.                                                                                                                 |
| Līdzekļa dokumenti      | Skatiet līdzeklim pievienoto dokumentu sarakstu. Šie dokumenti ir iestatīti **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa dokumenti**.                 |
| Atribūti           | Izveidojiet vai skatiet līdzekļa atribūtus.                                                                                                                             |
| Attēls                | Atlasiet līdzekļa attēlu.                                                                                                                                   |
| Primārie līdzekļi        | Skatiet primāro līdzekļu vēsturi atlasītajam līdzeklim.                                                                                                                |
| Funkcionālie novietojumi | Skatiet funkcionālo novietojumu vēsturi atlasītajam līdzeklim.                                                                                                          |
| Stāvokļa novērtējums | Reģistrējiet līdzekļa stāvokļa novērtējuma mērījumus.                                                                                                         |
| Defekti               | Atveriet saraksta lapu **Līdzekļa defekta**, kur varat skatīt līdzeklim reģistrētos defektus.                                                                                             |
| Izmaksu kontrole         | Salīdziniet līdzekļa budžeta izmaksas un faktiskās izmaksas.                                                                                                              |
| Stundu kontrole         | Salīdziniet līdzeklim prognozētās stundas un faktiskās stundas.                                                                                                              |
| Līdzekļa KPI           | Aprēķiniet un skatiet līdzekļa galvenos veiktspējas indikatorus (KPI).                                                                                              |
| Darba tipi            | Skatiet līdzekļa pašreizējo noklusējuma darba veidu pārskatu.                                                                                                            |
| Kritiskuma veidi    | Skatiet vai atjauniniet līdzekļa kritiskuma veidus.                                                                                                                              |
| Rezerves daļas          | Skatiet apstiprināto un alternatīvo rezerves daļu sarakstu, kuras var izmantot līdzeklim.                                                                               |
| Līdzekļa patēriņš    | Izdrukājiet pārskatu, kurā ir parādītas līdzekļa patēriņa reģistrācijas.                                                                                                |
| Līdzekļa defekts          | Izdrukājiet pārskatu, kurā ir parādītas līdzekļa defektu reģistrācijas.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]