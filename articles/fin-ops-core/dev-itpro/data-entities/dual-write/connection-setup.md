---
title: Atbalstītie scenāriji duālā ieraksta iestatījumiem
description: Šajā tēmā aprakstīti scenāriji, kas tiek atbalstīti duālā ieraksta iestatījumiem.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112479"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Atbalstītie scenāriji duālā ieraksta iestatījumiem

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varat iestatīt duālā ieraksta savienojumu starp Finance and Operations vidi un Common Data Service vidi.

+ **Finance and Operations vide** nodrošina **Finance and Operations programmu** (piemēram, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail un Dynamics 365 Human Resources) pamata platformu.
+ **Common Data Service vide** nodrošina pamata programmu **modeļa vadītām programmām pakalpojumā Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).

Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.

+ Jaunajām Finance and Operations programmu instancēm duālā ieraksta savienojuma iestatījums sākas portālā Microsoft Dynamics Lifecycle Services (LCS). Ja jums ir Microsoft Power Platform licence, jūs saņemsit jaunu Common Data Service vidi, ja jūsu nomniekam tādas nav.
+ Esošajām instancēm Finance and Operations programmās, duālā ieraksta savienojuma iestatīšana sākas Finance and Operations vidē.

Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:

+ [Jauna Finance and Operations programmas instance un jauna modeļa vadītas programmas instance](#new-new)
+ [Jauna Finance and Operations programmas instance un esoša modeļa vadītas programmas instance](#new-existing)
+ [Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un jauna modeļa vadītas programmas instance](#new-demo-new)
+ [Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un esoša modeļa vadītas programmas instance](#new-demo-existing)
+ [Esoša Finance and Operations programmas instance un jauna modeļa vadītas programmas instance](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Jauna Finance and Operations programmas instance un jauna modeļa vadītas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un jaunu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas šādas darbības:

- Tiek nodrošināta jauna, tukša Finance and Operations vide.
- Tiek nodrošināta jauna, tukša modeļa vadītas programmas instance, kurā ir instalēts CRM galvenais risinājums.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Elementa kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Jauna Finance and Operations programmas instance un esoša modeļa vadītas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un esošu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas šādas darbības:

- Tiek nodrošināta jauna, tukša Finance and Operations vide.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Elementa kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

Lai sinhronizētu esošos Common Data Service datus uz Finance and Operations programmu, rīkojieties šādi.

1. Izveidojiet jaunu uzņēmumu Finance and Operations programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md)Common Data Service datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.

Tā kā duālais ieraksts ir tiešsaistes sinhronizācijas režīmā, dati no Common Data Service automātiski sāk plūst uz Finance and Operations programmu.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un jauna modeļa vadītas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un jaunu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un jauna modeļa vadītas programmas instance](#new-new) iepriekš šajā tēmā. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz modeļa vadītu programmu, veiciet šādas darbības.

1. LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \>Duālais ieraksts**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Jauna Finance and Operations programmas instance, kurai ir demonstrācijas dati, un esoša modeļa vadītas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un esošu modeļa vadītas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un esoša modeļa vadītas programmas instance](#new-existing) iepriekš šajā tēmā. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz modeļa vadītu programmu, veiciet šādas darbības.

1. LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \>Duālais ieraksts**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** entītijām, kurām vēlaties sinhronizēt datus.

Lai sinhronizētu esošos Common Data Service datus uz Finance and Operations programmu, rīkojieties šādi.

1. Izveidojiet jaunu uzņēmumu Finance and Operations programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) Common Data Service datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.

Tā kā duālais ieraksts ir tiešsaistes sinhronizācijas režīmā, dati no Common Data Service automātiski sāk plūst uz Finance and Operations programmu.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Esoša Finance and Operations programmas instance un jauna modeļa vadītas programmas instance

Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un jaunu vai esošu modeļa vadītas programmas instanci pakalpojumu Dynamics 365 notiek Finance and Operation vidē.

1. Iestatiet savienojumu no Finance and Operations programmas.
2. Lai sinhronizētu esošos Common Data Service datus uz programmu Finance and Operations, [palaidiet](bootstrap-company-data.md) Common Data Service datus, izmantojot trīs burtu ISO uzņēmuma kodu.

Tā kā duālais ieraksts ir tiešsaistes sinhronizācijas režīmā, dati no Common Data Service automātiski sāk plūst uz Finance and Operations programmu.
