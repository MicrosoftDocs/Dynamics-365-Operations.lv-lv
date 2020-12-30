---
title: Norādījumi par duālā ieraksta iestatīšanu
description: Šajā tēmā aprakstīti scenāriji, kas tiek atbalstīti duālā ieraksta iestatījumiem.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 47c07dd0e2f311b61297340a48a5a31cb1de3903
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685669"
---
# <a name="guidance-for-dual-write-setup"></a>Norādījumi par duālā ieraksta iestatīšanu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Varat iestatīt duālā ieraksta savienojumu starp Finance and Operations vidi un Dataverse vidi.

+ **Finance and Operations vide** nodrošina **Finance and Operations programmu** (piemēram, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce un Dynamics 365 Human Resources) pamata platformu.
+ **Dataverse vide** nodrošina pamata platformu **klientu iesaistīšanas programmām** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Personāla vadības modulis Dynamics 365 Finance atbalsta duālās rakstīšanas savienojumus, bet Dynamics 365 Human Resources programma to neizmanto.

Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.

+ Jaunajām Finance and Operations programmu instancēm duālā ieraksta savienojuma iestatījums sākas portālā Microsoft Dynamics Lifecycle Services (LCS). Ja jums ir Microsoft Power Platform licence, jūs saņemsit jaunu Dataverse vidi, ja jūsu nomniekam tādas nav.
+ Esošajām instancēm Finance and Operations programmās, duālā ieraksta savienojuma iestatīšana sākas Finance and Operations vidē.

Pirms sākat duālo rakstīšanu elementā, varat palaist sākotnējo sinhronizāciju, lai apstrādātu esošos datus abās pusēs: Finance and Operations programmas un klientu iesaistīšanas programmās. Varat izlaist sākotnējo sinhronizāciju, ja nav vajadzības sinhronizēt datus starp abām vidēm.

Veicot sākotnējo sinhronizāciju, varat kopēt esošos datus no vienas programmas uz citu divvirzienu formā. Ir vairāki dažādi iestatīšanas scenāriji atkarībā no tā, kādas vides jums jau ir un kāda veida dati tajās ir.

Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:

+ [Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance](#new-new)
+ [Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance](#new-existing)
+ [Jauna Finance and Operations programmas instance, kurai ir dati, un jauna klientu iesaistīšanas programmas instance](#new-data-new)
+ [Jauna Finance and Operations programmas instance, kurai ir dati, un esoša klientu iesaistīšanas programmas instance](#new-data-existing)
+ [Esoša Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance](#existing-new)
+ [Esoša Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un jaunu klientu iesaistīšanas programmas instanci, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Tiek nodrošināta jauna, tukša Finance and Operations vide.
- Tiek nodrošināta jauna, tukša klientu iesaistīšanas programmas instance, kurā ir instalēts CRM galvenais risinājums.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurai nav datu, un esošu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, veiciet darbības, kas aprakstītas rakstā [Duālā ieraksta iestatīšana no Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Tiek nodrošināta jauna, tukša Finance and Operations vide.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

Lai sinhronizētu esošos Dataverse datus uz Finance and Operations programmu, rīkojieties šādi.

1. Izveidojiet jaunu uzņēmumu Finance and Operations programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) datus Dataverse, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example) tālāk šajā tēmā.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Jauna Finance and Operations programmas instance, kurai ir dati, un jauna klientu iesaistīšanas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un jaunu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance](#new-new) iepriekš šajā tēmā. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \> Duālais ieraksts**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Jauna Finance and Operations programmas instance, kurai ir dati, un esoša klientu iesaistīšanas programmas instance

Lai iestatītu duālā ieraksta savienojumu starp jaunu Finance and Operations programmas instanci, kurā ir demonstrācijas dati, un esošu klientu iesaistīšanas programmas instanci pakalpojumā Dynamics 365, izpildiet darbības, kas aprakstītas sadaļā [Jauna Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance](#new-existing) iepriekš šajā tēmā. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. LCS lapā atveriet Finance and Operations programmu, piesakieties un pēc tam atveriet **Datu pārvaldība \> Duālais ieraksts**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai sinhronizētu esošos Dataverse datus uz Finance and Operations programmu, rīkojieties šādi.

1. Izveidojiet jaunu uzņēmumu Finance and Operations programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) Dataverse datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Esoša Finance and Operations programmas instance un jauna klientu iesaistīšanas programmas instance

Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un jaunu vai esošu klientu iesaistīšanās programmas instanci notiek Finance and Operation vidē.

1. [Iestatiet savienojumu no Finance and Operations programmas](enable-dual-write.md).
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Esoša Finance and Operations programmas instance un esoša klientu iesaistīšanas programmas instance

Duālā ieraksta savienojuma iestatīšana starp esošo Finance and Operations programmas instanci un esošu klientu iesaistīšanās programmas instanci pakalpojumu notiek Finance and Operation vidē.

1. [Iestatiet savienojumu no Finance and Operations programmas](enable-dual-write.md).
2. Lai sinhronizētu esošos Dataverse datus uz programmu Finance and Operations, [palaidiet](bootstrap-company-data.md) Dataverse datus, izmantojot trīs burtu ISO uzņēmuma kodu.
3. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="example"></a>Paraugs

Piemēru skatiet [V3 klientu iespējošana — kontaktpersonu tabulas karte](enable-entity-map.md#enable-table-map)

Lai varētu izmantot alternatīvu pieeju, kas balstās uz datu apjomu katrā elementā, kam jāpalaiž sākotnējā sinhronizāciju, skatiet [Apsvērumi par sākotnējo sinhronizāciju](initial-sync-guidance.md).
