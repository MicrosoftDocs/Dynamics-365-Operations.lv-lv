---
title: Ievads funkcionālajos novietojumos
description: Šajā tēmā ir sniegts pārskats par funkcionālajiem novietojumiem Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationEditSubLocations, EntAssetFunctionalLocationLookup, EntAssetFunctionalLocationRename, EntAssetFunctionalLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea318d750f1ef18f270fa246ab54ecb63aa790
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432667"
---
# <a name="introduction-to-functional-locations"></a>Ievads funkcionālajos novietojumos

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir sniegts pārskats par funkcionālajiem novietojumiem Līdzekļu pārvaldībā. Funkcionālie novietojumi ir tehniskas struktūras elementi, piemēram, funkcionālās vienības sistēmā. Funkcionālie novietojumi tiek veidoti hierarhiski, un tajos tiek uzstādīti līdzekļi. Funkcionālo novietojumu iestatīšana uzņēmumā ir atkarīga no uzņēmuma prasībām.

Tālāk ir sniegti daži piemēri tam, kā varat izmantot funkcionālos novietojumus:

- **Functional** — funkcionālie novietojumi var būt orientēti uz lietotāju un tos var izmantot, lai pārvaldītu līdzekļus, kam ir līdzīga uzvedība.
- **Process-related** — funkcionālie novietojumi var būt orientēti uz darbplūsmu.
- **Spatial** — funkcionālie novietojumi var pārstāvēt ģeogrāfiskās atrašanās vietas vai vietas.

Katrs funkcionālais novietojums tiek neatkarīgi pārvaldīts Līdzekļu pārvaldībā. Tālāk ir norādītas dažas noderīgas funkcionālo novietojumu funkcijas.

- Funkcionālā novietojuma specifikāciju iestatīšana.
- Līdzekļa specifikācijas prasību iestatīšana.
- Uzturēšanas secības profilaktiskai un reaģējošai uzturēšanai iestatīšana.
- Uzstādīto līdzekļu vadība.
- Ar uzstādītajiem līdzekļiem saistīto aktīvo pieprasījumu un darba pasūtījumu izsekošana.
- Līdzekļiem reģistrēto defektu izsekošana.
- Ar funkcionālo novietojumu saistīto līdzekļu uzturēšanas izmaksu izsekošana jebkurā noteiktā laikā.

Funkcionālie novietojumi nodrošina līdzekļu izsekojamību saistībā ar pieprasījumiem, darba pasūtījumiem, defektu reģistrāciju, nosacījumu novērtējumiem, ražošanas apturēšanas reģistrācijām un līdzekļu skaitītāju reģistrācijām.

> [!NOTE]
> Pat ja līdzeklis tā dzīves cikla laikā ir uzstādīts dažādos funkcionālajos novietojumos, izmaksas var būt saistītas ar katru vietu. Citiem vārdiem sakot, līdzekļa izmaksas vienmēr ir saistītas ar funkcionālo novietojumu, kurā līdzeklis dotajā laikā ir uzstādīts.

Funkcionālie novietojumi **nav** elastīgi. Tāpēc, kad esat iestatījis funkcionālo novietojumu hierarhiju, funkcionālos novietojumus tajā nevar pārvietot. 

Pēc funkcionālā novietojuma hierarhijas izveides nākamā darbība ir uzstādīt tajā līdzekļus. Papildinformāciju skatiet sadaļā [Līdzekļu uzstādīšana funkcionālajos novietojumos](../functional-locations/install-objects-on-functional-locations.md).

## <a name="all-functional-locations"></a>Visi funkcionālie novietojumi

Atlasiet **Līdzekļu pārvaldība** \> **Kopīgi** \> **Funkcionālie novietojumi** \> **Visi funkcionālie novietojumi**, lai atvērtu saraksta lapu **Visi funkcionālie novietojumi**. Šajā lapā tiek rādīti visi funkcionālie novietojumi un zināma informācija, kas ir saistīta ar katru no tiem. Lai skatītu tikai aktīvos funkcionālos novietojumus, atlasiet **Aktīvie funkcionālie novietojumi**. Lai skatītu tikai funkcionālos novietojumus, kuriemm esat saistīts kā darbinieks, atlasiet **Mani aktīvie funkcionālie novietojumi**. (Šī saistība ir iestatīta lapā **Darbinieki**. Papildinformāciju skatiet sadaļā [Uzturēšanas darbinieki un darbinieku grupas](../setup-for-objects/workers-and-worker-groups.md).)

Saraksta lapā **Visi funkcionālie novietojumi** atlasiet saiti kolonnā **Funkcionālais novietojums**, lai skatītu detalizētu informāciju par atlasīto ierakstu. Lai rediģētu funkcionālo novietojumu, atlasiet pogu **Rediģēt**. Detalizētajā skatā tiek parādīta detalizēta informācija, kas ir saistīta ar atrašanās vietu. Tajā labajā pusē ir arī rūts **Saistītā informācija**. Šajā rūtī ir redzama funkcionālā novietojuma hierarhija. Rūti **Saistītā informācija** var izvērst un sakļaut.

Pogas darbības rūtī ir sakārtotas cilnēs. Nākamajā tabulā ir īsi aprakstītas pogas, kas saistītas ar Līdzekļu pārvaldību.

| Pogas nosaukums                         | Apraksts                                                                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Labot                                | Pārslēgšanās starp rediģēšanas režīmu un lapas skatījuma režīmu.                                                                                         |
| Jauna                                 | Izveidot jaunu funkcionālo novietojumu.                                                                                                            |
| Dzēst                              | Dzēst atlasīto funkcionālo novietojumu.                                                                                                     |
| Pārdēvēt                              | Pārdēvēt atlasīto funkcionālo novietojumu.                                                                                                     |
| Funkcionālā novietojuma struktūras kopēšana  | Kopēt funkcionālā novietojuma hierarhiju.                                                                                                      |
| Līdzekļa uzstādīšana                       | Uzstādiet līdzekli, tostarp pakārtotos līdzekļus, funkcionālajā novietojumā.                                                                        |
| Līdzekļu aizstāšana                       | Aizstājiet līdzekļu hierarhiju ar citu līdzekļu hierarhiju funkcionālajā novietojumā.                                                         |
| Izmaksu kontrole                        | Atveriet lapu **Funkcionālā novietojuma izmaksu kontrole**, kurā varat veikt izmaksu aprēķinu atlasītajam funkcionālajam novietojumam.                |
| Stundu kontrole                        | Atveriet lapu **Funkcionālā novietojuma stundu kontrole**, kurā varat veikt izmaksu aprēķinu atlasītajam funkcionālajam novietojumam.                |
| Pamatlīdzekļu tabula                              | Atveriet lapu **Visi līdzekļi**, kur varat skatīt to līdzekļu sarakstu, kas ir saistīti ar atlasīto funkcionālo novietojumu.                      |
| Pieprasījumi                            | Atveriet lapu **Aktīvie pieprasījumi**, kur varat skatīt to pieprasījumu sarakstu, kas ir saistīti ar atlasīto funkcionālo novietojumu.               |
| Darba pasūtījumi                         | Atveriet lapu **Aktīvie darba pasūtījumi**, kur varat skatīt to darba pasūtījumu sarakstu, kas ir saistīti ar atlasīto funkcionālo novietojumu.         |
| Defekti                              | Atveriet lapu **Līdzekļu defekti**, kur varat skatīt to līdzekļu defektu reģistrāciju sarakstu, kas ir saistīti ar atlasīto funkcionālo novietojumu. |
| Funkcionālo novietojumu stāvokļa atjaunināšana    | Atjauniniet atlasītā funkcionālā novietojuma stadiju.                                                                                        |
| Dzīves cikla stāvokļa žurnāls                 | Skatiet žurnālu, kurā parādītas atlasītā funkcionālā novietojuma stadijas.                                                                        |
