---
title: Norādījumi par duālā ieraksta iestatīšanu
description: Šajā rakstā ir aprakstīti scenāriji, kas tiek atbalstīti duālās rakstīšanas iestatīšanai.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289750"
---
# <a name="guidance-for-dual-write-setup"></a>Norādījumi par duālā ieraksta iestatīšanu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Ir iespējams izveidot dubultās rakstīšanas savienojumu starp finanšu un operāciju vidi un Dataverse vidi.

+ Finanšu **un operāciju vide** nodrošina pamata platformu finanšu **un** operāciju programmām (piemēram, Microsoft Dynamics 365 Finanses, Dynamics 365 Supply Chain Management Dynamics 365 Commerce un Dynamics 365 Human Resources).
+ **Dataverse vide** nodrošina pamata platformu **Customer Engagement programmās** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).


> [!IMPORTANT]
> Personāla vadības modulis Dynamics 365 finansēs atbalsta dubultos rakstīšanas savienojumus, bet Dynamics 365 Human Resources programma neatbalsta.

Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.

+ Jaunām finanšu un operāciju programmu instancēm, pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) sākas dubultās rakstīšanas savienojuma iestatīšana. Ja jums ir Microsoft Power Platform licence, jūs saņemsit jaunu Dataverse vidi, ja jūsu nomniekam tādas nav.
+ Jau pastāvošu gadījumu finanšu un operāciju programmām, dubultās rakstīšanas savienojuma iestatīšana sākas finanšu un operāciju vidē.

Pirms sākat dubulto rakstiet entītijā, varat veikt sākotnējo sinhronizāciju, lai apstrādātu esošos datus abās pusēs: finanšu un operāciju programmas un debitoru piesaistes programmas. Varat izlaist sākotnējo sinhronizāciju, ja nav vajadzības sinhronizēt datus starp abām vidēm.

Veicot sākotnējo sinhronizāciju, varat kopēt esošos datus no vienas programmas uz citu divvirzienu formā. Ir vairāki dažādi iestatīšanas scenāriji atkarībā no tā, kādas vides jums jau ir un kāda veida dati tajās ir.

Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:

+ [Jauna finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance](#new-new)
+ [Jauna finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance](#new-existing)
+ [Jauna finanšu un operāciju programmas instance, kurā ir dati un jauna debitoru iesnidņu programmas instance](#new-data-new)
+ [Jauna finanšu un operāciju programmas instance, kurā ir dati un esoša debitora lietojumprogrammas piesaistes programmas instance](#new-data-existing)
+ [Esoša finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance](#existing-new)
+ [Esoša finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Jauna finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance

Lai iestatītu dubultās rakstīšanas savienojumu starp jaunu finanšu un operāciju programmas instanci, kurā nav datu un jauna debitoru iesaistīšanas programmas instance, [izpildiet Duālās rakstīšanas iestatījumu darbības, izmantojot Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Tiek nodrošināta jauna, tukša finanšu un operāciju vide.
- Tiek nodrošināta jauna, tukša klientu iesaistīšanas programmas instance, kurā ir instalēts CRM galvenais risinājums.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Jauna finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance

Lai iestatītu dubultās rakstīšanas savienojumu starp jaunu finanšu un operāciju programmas instanci, kurā nav datu un esošas debitoru iesaistīšanas programmas instances, [izpildiet Duālās rakstīšanas iestatījumu darbības, izmantojot Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Tiek nodrošināta jauna, tukša finanšu un operāciju vide.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

Lai sinhronizētu esošos Dataverse datus finanšu un operāciju programmā, sekojiet šiem soļiem.

1. Izveidojiet jaunu uzņēmumu finanšu un operāciju programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) datus Dataverse, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Saites uz piemēru un alternatīvu pieeju skatiet tālāk šī [raksta](#example) sadaļā Piemērs.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Jauna finanšu un operāciju programmas instance, kurā ir dati un jauna debitoru iesnidņu programmas instance

Lai iestatītu duālu rakstīšanas savienojumu starp jaunu finanšu un operāciju programmas instanci, kurā ir dati un jauna debitoru iesaistīšanas programmas instance, izpildiet darbības, kas ir saistītas ar jauno finanšu un operāciju programmas instanci un jaunu debitoru lietojumprogrammas instanci, [kas](#new-new) atrodas agrāk šajā rakstu. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. Atveriet finanšu un operāciju programmu no LCS lapas, piesakieties un pēc tam dodieties uz **datu pārvaldības \> duālo rakstiet**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Jauna finanšu un operāciju programmas instance, kurā ir dati un esoša debitora lietojumprogrammas piesaistes programmas instance

Lai iestatītu duālu rakstīšanas savienojumu starp jaunu finanšu un operāciju programmas instanci, kurā ir dati un esoša debitoru iesaistīšanas programmas instance, [izpildiet](#new-existing) darbības jaunā finanšu un operāciju programmas instancē un jau esošajā debitoru iesnidņu programmas instances sadaļā, kas atrodas agrāk šajā rakstu. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. Atveriet finanšu un operāciju programmu no LCS lapas, piesakieties un pēc tam dodieties uz **datu pārvaldības \> duālo rakstiet**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai sinhronizētu esošos Dataverse datus finanšu un operāciju programmā, sekojiet šiem soļiem.

1. Izveidojiet jaunu uzņēmumu finanšu un operāciju programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) Dataverse datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Esoša finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance

Dubultās rakstīšanas savienojuma starp esošu finanšu un operāciju programmas instanci un jaunu debitoru piesaistes programmas instanci iestatīšana notiek Finanšu un operāciju vidē.

1. [Iestatiet savienojumu no finanšu un operāciju programmas](enable-dual-write.md).
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Esoša finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance

Dubultās rakstīšanas savienojuma starp esošu finanšu un operāciju programmas instanci un esošu debitoru piesaistes programmas instanci iestatīšana notiek Finanšu un operāciju vidē.

1. [Iestatiet savienojumu no finanšu un operāciju programmas](enable-dual-write.md).
2. Lai sinhronizētu esošos Dataverse datus finanšu un operāciju programmā, [ar](bootstrap-company-data.md)Dataverse trīs burtu ISO uzņēmuma kodu nodrošina datu sinhronizāciju.
3. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="example"></a>Paraugs

Piemēru skatiet [V3 klientu iespējošana — kontaktpersonu tabulas karte](enable-entity-map.md#enable-table-map)

Lai varētu izmantot alternatīvu pieeju, kas balstās uz datu apjomu katrā elementā, kam jāpalaiž sākotnējā sinhronizāciju, skatiet [Apsvērumi par sākotnējo sinhronizāciju](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
