---
title: Standarta izmaksu priekšnosacījumu pārskats
description: Šajā tēmā aprakstītas pamata darbības standarta izmaksu lietošanai.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee676afbde465c1abb4fe4ae94e9f162f695d994
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263474"
---
# <a name="prerequisites-for-standard-costs-overview"></a>Standarta izmaksu priekšnosacījumu pārskats

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstītas pamata darbības standarta izmaksu lietošanai. Turpmākās darbības ir atkarīgas no uzņēmuma operācijām. Piemēram, darbības atšķiras neražošanas videi, ražošanas videi, kurā netiek izmantota maršrutēšana, un ražošanas videi, kurā tiek izmantota maršrutēšana. 

Lai iestatītu standarta izmaksas, veiciet tālāk norādītās darbības.

**1. Izveidojiet standarta izmaksu krājumu modeļa grupu.**

Izmantojiet lapu **Krājumu modeļu grupas**, lai izveidotu jaunu standarta izmaksu grupu, un piešķiriet vienuma **Standarta izmaksas** krājumu modeli. Krājumu modeļu grupas identifikatoram ir jābūt jēgpilnam, piemēram, **Std izmaksas**. Atzīmējiet izvēles rūtiņas, lai norādītu, ka šai grupai jāatļauj negatīvi finanšu krājumi un jāgrāmato fiziskie krājumi un finanšu krājumi. Šī standarta izmaksu grupa tiks piešķirta krājumiem.

**2. Definējiet ar standarta izmaksu novirzēm saistītos virsgrāmatas kontus.** 

Izmantojiet lapu **Kontu plāns**, lai definētu virsgrāmatas kontus, kas ir saistīti ar standarta izmaksu novirzēm. Šie virsgrāmatas konti jādefinē, pirms tos var piešķirti lapā **Grāmatošana**. Virsgrāmatas konti var attēlot krājuma grupas un izmaksu grupas.

**3. Piešķiriet virsgrāmatas kontus krājumu grāmatojumiem, kas ir saistīti ar standarta izmaksu novirzēm.** 

Izmantojiet lapu **Grāmatošana**, lai piešķirtu virsgrāmatas kontus, kas ir saistīti ar standarta izmaksu novirzēm. Varat norādīt novirzes virsgrāmatas kontu pēc krājuma (vai krājumu grupas) un pēc izmaksu grupas (vai izmaksu grupas tipa) vai arī varat norādīt, ka virsgrāmatas konts attiecas uz visiem krājumiem un visām izmaksu grupām. Šīs opcijas atbilst tabulu, grupu un visu elementu izmaksu relācijām. 

Pirms definējat krājumu grāmatošanas kārtulas, izmantojiet lapu **Darbību kombinācijas**, lai iespējotu izmaksu relācijas (tabulām, grupām un visiem elementiem).

**4. Definējiet ar standarta izmaksām saistītos krājumu parametrus.** 

-  Izmantojiet cilni **Krājumu uzskaite**, kas ir pieejama lapā **Krājumu uzskaites politiku iestatīšana > Parametri**, lai definētu izmaksu kontroles parametrus, kas ir saistīti ar standarta izmaksām.

    -  Laukā **Izmaksu sadalījums** atlasiet opciju **Nav** vai **Apakšgrāmata**. Atlasot opciju **Apakšgrāmata**, izmaksu sadalījums ir *aktīvs* izmaksu sadalījums. Aktīvs izmaksu sadalījums ir kritisks izmaksu grupu segmentācijas aprēķināšanai, atgūšanai un skatīšanai daudzlīmeņu struktūrā standarta izmaksu krājumiem. Ja izmaksu sadalījums ir aktīvs, varat analizēt krājumus, nepabeigto ražošanu (NP) un pārdoto preču pašizmaksu (PPPI) uz izmaksu grupu vai sniegt par tiem pārskatu vienā līmenī, vairākos līmeņos vai visā sistēmā. Ja izmaksu sadalījums ir aktīvs, aktivizējot ražotā krājuma izmaksas, izmaksu grupu segmentācija tiek saglabāta krājuma izmaksu ierakstā. 

    -  Atlasot opciju **Nav**, standarta izmaksu vienumiem netiks saglabāta izmaksu grupu segmentācija. Citiem vārdiem sakot, ražotā vienuma standarta izmaksas tiks aprēķinātas un saglabātas kā viena summa bez izmaksu grupu segmentācijas. Ražoto komponentu izmaksu ieguldījumi tiks apkopoti vienā summā.

-  Laukā **Novirzes no standarta** atlasiet opciju **Kopsavilkuma** vai **Uz izmaksu grupu**. Atlasot opciju **Uz izmaksu grupu**, varat norādīt pirkšanas cenas novirzes un ražošanas novirzes pēc izmaksu grupas. Varat arī norādīt četrus ražošanas noviržu tipus: laidiena lielumu, daudzumu, cenu un aizvietošanas novirzes. Atlasot opciju **Kopsavilkuma**, nevarat norādīt novirzes pēc izmaksu grupas un četrus ražošanas noviržu tipus. Ir iespējams skatīt tikai apkopotu ražošanas novirzi.

-  Ierobežojumi par novirzēm no standarta darbojas neatkarīgi no izmaksu sadalījuma ierobežojumiem. Citiem vārdiem sakot, varat atlasīt izmaksu sadalījuma politiku **Nav** un atlasīt novirzes pēc izmaksu grupas tā, lai ražošanas novirzes pēc izmaksu grupas joprojām tiktu paturētas.

**5. Izveidojiet izmaksu aprēķināšanas versijas standarta izmaksām.** 

Izmantojiet lapu **Izmaksu aprēķināšanas versijas iestatījums**, lai izveidotu vienu vai vairākas izmaksu aprēķināšanas versijas standarta izmaksām. Katra izmaksu aprēķināšanas versija jāizveido ar izmaksu aprēķināšanas tipu **Standarta izmaksas**, un saturā jāļauj ietvert izmaksu datus.

**6. Sagatavojiet esošu klientu standarta izmaksu lietošanai.** 

Klientiem, kas vēlas mainīt savus esošos krājumus uz standarta izmaksu krājumu modeli, jāizmanto lapa **Standarta izmaksu pārveidošana**.


<a name="related-topics"></a>Saistītās tēmas
--------

[Standarta izmaksu pārveidošanas apskats](standard-cost-conversion-overview.md)

### <a name="blogs"></a>Emuāri

#### <a name="community-blogs"></a>Kopienas emuāri

- [Tiešo materiālu standarta izmaksu iestatīšana programmā Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/06/07/how-to-set-up-standard-costs-for-direct-materials-in-dynamics-365-for-finance-and-operations)
- [Standarta tiešās darbaspēka izmaksas programmā Dynamics 365 for Finance and Operations](https://financefunction.tech/2018/07/16/standard-direct-labor-cost-in-dynamics-365-for-finance-and-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]