---
title: "Preces konfigurācijas modeļa iestatīšana"
description: "Šajā rakstā ir aprakstītas iestatīšanas un preču konfigurācijas modeļa izveidošanas darbības."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 4051
ms.assetid: 00df5537-b148-4e32-a248-3e35876ad4e1
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3327cc0efb0fbf68f91d6e7cb1e68577b51a6613
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-a-product-configuration-model"></a>Preces konfigurācijas modeļa iestatīšana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstītas iestatīšanas un preču konfigurācijas modeļa izveidošanas darbības.

| Uzdevums                                                        | Apraksts                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Izveidojiet preces šablonu.                                    | Izveidojiet preces šablonu no saraksta **Preces šablons**. Izdodiet preces šablonu visiem saistītajiem uzņēmumiem. Preces šablonam, kas tiek izmantots kā preču konfigurācijas modeļa versija vai kā apakškomponents, ir jāatlasa konfigurācijas tehnoloģija **Konfigurācija atbilstoši ierobežojumam** un ir jāatlasa tikai preču dimensiju grupas konfigurācijas dimensija. |
| Izveidojiet komponentus.                                          | Izveidojiet komponentus lapā **Komponenti**. Komponenti ir preces konfigurācijas modeļa pamatelementi, ko var atkārtoti izmantot vairākos preču konfigurācijas modeļos.                                                                                                                                                                                                                      |
| Izveidojiet atribūtu tipus.                                     | Izveidojiet atribūtu tipus lapā **Atribūtu tipi**. Atribūtu tipi nosaka datu tipu kopu visiem atribūtiem, kas tiek izmantoti preču konfigurācijas modeļos. Atribūti, kuru tips ir **Būla**, **Teksts** ar fiksētu sarakstu un **Vesels skaitlis** ar diapazonu tipu, satur to vērtību kopu, kas ir pieejama, kad konfigurējat preces variantu, pamatojoties uz preces konfigurācijas modeli.       |
| Izveidojiet preces konfigurācijas modeli.                       | Izveidojiet preces konfigurācijas modeli lapā **Jauns preces konfigurācijas modelis**.                                                                                                                                                                                                                                                                                                              |
| Pievienojiet atribūtus preces konfigurācijas modelim.            | Izveidojiet atribūtu kopsavilkuma cilnē **Atribūti** lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli**. Atribūti nosaka preces konfigurācijas modeļa raksturlielumus.                                                                                                                                                                                                       |
| Pievienojiet ierobežojumus preces konfigurācijas modelim.           | Izveidojiet ierobežojumus kopsavilkuma cilnē **Ierobežojumi** lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli**. Ierobežojumi ir prasības, kurām ir jāatbilst preces konfigurācijas modelim. Ierobežojumi var būt izteiksmes ierobežojumi vai tabulas ierobežojumi.                                                                                                                                 |
| Pievienojiet apakškomponentus preces konfigurācijas modelim.         | Izveidojiet apakškomponentus kopsavilkuma cilnē **Apakškomponenti** lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli**. Apakškomponenti ir saistīti ar komponentiem un piesaistīti krājumiem, kas attiecas uz apakškomponentu.                                                                                                                                                                       |
| Pievienojiet lietotāju prasības preces konfigurācijas modelim.     | Lietotāju prasības līdzinās apakškomponentiem, taču tās neattiecas uz krājumu.. Lietotāju prasības var uzskatīt par fantoma MK. Visas MK rindas vai maršruta operācijas, kas ir novietotas tieši zem lietotāja prasības, tiek sakļautas primārajā komponentā.                                                                                                                       |
| Pievienojiet MK rindas preces konfigurācijas modelim.             | Izveidojiet KM rindas kopsavilkuma cilnē **MK rindas** lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli**. MK rindas attiecas uz daļu, kas ir nepieciešama, lai izgatavotu preces variantu.                                                                                                                                                                                                 |
| Pievienojiet maršruta operācijas preces konfigurācijas modelim.      | Izveidojiet maršruta operācijas kopsavilkuma cilnē **Maršruta operācijas** lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli**. Maršruta operācijas attiecas uz kādu no darbībām darbību sērijā, kas tiek veikta, lai izgatavotu preces variantu.                                                                                                                                                    |
| Izveidojiet aktīvu ražošanas konfigurācijas modeļa versiju. | Izveidojiet aktīvu preču konfigurācijas modeļa versiju lapā **Versijas**. Versija ir attiecības starp preces konfigurācijas modeli un preces šablonu. Preces konfigurācijas modeli, kam ir aktīva versija, var konfigurēt pārdošanas pasūtījumā, pārdošanas piedāvājumā, pirkšanas pasūtījumā vai ražošanas pasūtījumā.                                                               |
| Pārbaudiet preces konfigurācijas modeli.                         | Pārbaudiet preces konfigurācijas modeli lapā **Detalizēta informācija par ierobežojumam atbilstošu preces konfigurācijas modeli** vai **Preču konfigurācijas modeļu saraksts**. Veicot preču konfigurācijas modeļu pārbaudi, tiek imitēts preces modeļa konfigurācijas process, kas notiek pasūtījuma apstrādes laikā.                                                                                                |
| Izveidojiet preces konfigurācijas modeļa veidni.                | Izveidojiet preces konfigurācijas modeļa veidni lapā **Konfigurācijas veidnes**. Konfigurācijas veidnē ir ietvertas preces konfigurācijas modeļa atribūtu vērtības. Atlasiet atribūtu vērtības lapā **Konfigurēt rindu**. Preces modeļa konfigurācijas laikā varat izvēlēties ielādēt preces modeļa konfigurācijas veidni.                                                   |
| Konfigurējiet krājumu.                                          | Preču konfigurācijas modeļus var konfigurēt pārdošanas pasūtījumā, pārdošanas piedāvājumā, pirkšanas pasūtījumā vai ražošanas pasūtījumā.                                                                                                                                                                                                                                                                           |






