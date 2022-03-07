---
title: Norādījumi par duālā ieraksta iestatīšanu
description: Šajā tēmā aprakstīti scenāriji, kas tiek atbalstīti duālā ieraksta iestatījumiem.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6de449b14bcdd82336e3e255bf62ad069d3daaf5
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061608"
---
# <a name="guidance-for-dual-write-setup"></a>Norādījumi par duālā ieraksta iestatīšanu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Var iestatīt divējādas rakstīšanas savienojumu starp finanšu un operāciju vidi un Dataverse vidi.

+ Finanšu **un operāciju vide** nodrošina finanšu un operāciju programmu **pamatā esošo platformu**(piemēram, Microsoft Dynamics 365 Finance Dynamics 365 Supply Chain Management,, Dynamics 365 Commerce un Dynamics 365 Human Resources).
+ **Dataverse vide** nodrošina pamata platformu **Customer Engagement programmās** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Personāla vadības modulis Dynamics 365 Finance atbalsta duālās rakstīšanas savienojumus, bet Dynamics 365 Human Resources programma to neizmanto.

Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.

+ Jauniem Finance and Operations programmu gadījumiem divu rakstu savienojuma iestatīšana sākas dzīves cikla pakalpojumos Microsoft Dynamics (LCS). Ja jums ir Microsoft Power Platform licence, jūs saņemsit jaunu Dataverse vidi, ja jūsu nomniekam tādas nav.
+ Esošajām instanču Finance and Operations programmām divu rakstu savienojuma iestatīšana sākas vidē Finanses un operācijas.

Pirms sākat dubultrakstot entītijā, varat veikt sākotnējo sinhronizāciju, lai apstrādātu esošos datus abās pusēs: Finance and Operations programmas un klientu piesaistes programmas. Varat izlaist sākotnējo sinhronizāciju, ja nav vajadzības sinhronizēt datus starp abām vidēm.

Veicot sākotnējo sinhronizāciju, varat kopēt esošos datus no vienas programmas uz citu divvirzienu formā. Ir vairāki dažādi iestatīšanas scenāriji atkarībā no tā, kādas vides jums jau ir un kāda veida dati tajās ir.

Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:

+ [Jauna Finance and Operations lietojumprogrammas instance un jauna klientu piesaistes lietotnes instance](#new-new)
+ [Jauna Finance and Operations lietojumprogrammas instance un esoša klientu piesaistes lietojumprogrammas instance](#new-existing)
+ [Jauna Finanšu un operāciju lietojumprogrammas instance, kurai ir dati un jauna klientu piesaistes lietojumprogrammas instance](#new-data-new)
+ [Jauna Finance and Operations lietojumprogrammas instance, kurai ir dati un esoša klientu piesaistes lietojumprogrammas instance](#new-data-existing)
+ [Esoša Finance and Operations lietojumprogrammas instance un jauna klientu piesaistes lietojumprogrammas instance](#existing-new)
+ [Esoša Finance and Operations lietojumprogrammas instance un esoša klientu piesaistes lietojumprogrammas instance](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Jauna Finance and Operations lietojumprogrammas instance un jauna klientu piesaistes lietotnes instance

Lai iestatītu divējādas rakstīšanas savienojumu starp jaunu finanšu un operāciju lietojumprogrammas gadījumu, kurā nav datu, un jaunu klientu piesaistes lietotnes gadījumu, izpildiet darbības, kas norādītas divu rakstīšanas iestatījumos [no dzīves cikla pakalpojumiem](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Tiek nodrošināta jauna, tukša finanšu un operāciju vide.
- Tiek nodrošināta jauna, tukša klientu iesaistīšanas programmas instance, kurā ir instalēts CRM galvenais risinājums.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Jauna Finance and Operations lietojumprogrammas instance un esoša klientu piesaistes lietojumprogrammas instance

Lai iestatītu divējādas rakstīšanas savienojumu starp jaunu Finanšu un operāciju lietojumprogrammas gadījumu, kurā nav datu, un esošu klientu piesaistes lietotnes gadījumu, izpildiet darbības, kas [norādītas sadaļā Divu rakstīšanas iestatīšana no dzīves cikla pakalpojumiem](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Tiek nodrošināta jauna, tukša finanšu un operāciju vide.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

Lai sinhronizētu esošos Dataverse datus ar programmu Finanses un operācijas, rīkojieties šādi.

1. Izveidojiet jaunu uzņēmumu programmā Finanses un operācijas.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) datus Dataverse, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example) tālāk šajā tēmā.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Jauna Finanšu un operāciju lietojumprogrammas instance, kurai ir dati un jauna klientu piesaistes lietojumprogrammas instance

Lai iestatītu divējādas rakstīšanas savienojumu starp jaunu Finanšu un operāciju lietojumprogrammas gadījumu, kurā ir dati, un jaunu klientu piesaistes lietojumprogrammas gadījumu, izpildiet darbības, kas [norādītas šīs tēmas sadaļā Jauna finanšu un operāciju lietojumprogramma un jauna klientu piesaistes lietojumprogrammas instance](#new-new). Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. Atveriet programmu Finanses un operācijas no LCS lapas, piesakieties un pēc tam dodieties uz **Datu pārvaldības \> divrakstīšana**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Jauna Finance and Operations lietojumprogrammas instance, kurai ir dati un esoša klientu piesaistes lietojumprogrammas instance

Lai iestatītu divējādas rakstīšanas savienojumu starp jaunu Finanšu un operāciju lietojumprogrammas gadījumu, kurā ir dati, un esošu klientu iesaistes lietojumprogrammas gadījumu, izpildiet darbības, kas [norādītas šīs tēmas sadaļā Jauna finanšu un operāciju lietojumprogramma un esoša klientu iesaistes lietojumprogrammas instance](#new-existing). Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. Atveriet programmu Finanses un operācijas no LCS lapas, piesakieties un pēc tam dodieties uz **Datu pārvaldības \> divrakstīšana**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai sinhronizētu esošos Dataverse datus ar programmu Finanses un operācijas, rīkojieties šādi.

1. Izveidojiet jaunu uzņēmumu programmā Finanses un operācijas.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) Dataverse datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Esoša Finance and Operations lietojumprogrammas instance un jauna klientu piesaistes lietojumprogrammas instance

Divu rakstu savienojuma iestatīšana starp esošu finanšu un operāciju lietojumprogrammas gadījumu un jaunu klientu piesaistes lietojumprogrammas gadījumu notiek finanšu un operācijas vidē.

1. [Iestatiet savienojumu no programmas](enable-dual-write.md) Finanses un operācijas.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Esoša Finance and Operations lietojumprogrammas instance un esoša klientu piesaistes lietojumprogrammas instance

Divu rakstu savienojuma iestatīšana starp esošu Finanšu un operāciju lietojumprogrammas gadījumu un esošu klientu iesaistes lietojumprogrammas gadījumu notiek vidē Finanses un operācija.

1. [Iestatiet savienojumu no programmas](enable-dual-write.md) Finanses un operācijas.
2. Lai sinhronizētu esošos Dataverse datus ar programmu Finanses un operācijas, sāknēšanas dati tiek [kodēti](bootstrap-company-data.md), Dataverse izmantojot trīs burtu ISO uzņēmuma kodu.
3. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="example"></a>Paraugs

Piemēru skatiet [V3 klientu iespējošana — kontaktpersonu tabulas karte](enable-entity-map.md#enable-table-map)

Lai varētu izmantot alternatīvu pieeju, kas balstās uz datu apjomu katrā elementā, kam jāpalaiž sākotnējā sinhronizāciju, skatiet [Apsvērumi par sākotnējo sinhronizāciju](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]