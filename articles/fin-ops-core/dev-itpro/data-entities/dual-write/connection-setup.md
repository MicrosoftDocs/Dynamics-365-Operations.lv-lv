---
title: Norādījumi par duālā ieraksta iestatīšanu
description: Šajā rakstā ir aprakstīti scenāriji, kas tiek atbalstīti duālās rakstīšanas iestatīšanai.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a0d1b4e1f093874a8fd37cf7aadb331cd1e7adc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873154"
---
# <a name="guidance-for-dual-write-setup"></a>Norādījumi par duālā ieraksta iestatīšanu

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Var iestatīt dubulto rakstīšanas savienojumu starp Finanšu un operāciju vidi un Dataverse vidi.

+ Finanšu **un operāciju vide** nodrošina pakārtotu platformu Finanšu **un operāciju** programmām (piemēram, Microsoft Dynamics 365 Finanses, Dynamics 365 Supply Chain Management Dynamics 365 Commerce un Dynamics 365 Human Resources).
+ **Dataverse vide** nodrošina pamata platformu **Customer Engagement programmās** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing un Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Personāla vadības modulis Dynamics 365 finansēs atbalsta dubultos rakstīšanas savienojumus, bet Dynamics 365 Human Resources programma neatbalsta.

Iestatīšanas mehānisms mainās atkarībā no jūsu abonementa un vides.

+ Jaunām Finanšu un operāciju programmu instancēm, Microsoft Dynamics pakalpojumā Lifecycle Services (LCS) sākas dubultās rakstīšanas savienojuma iestatīšana. Ja jums ir Microsoft Power Platform licence, jūs saņemsit jaunu Dataverse vidi, ja jūsu nomniekam tādas nav.
+ Esošajām instancēm Finanšu un operāciju programmām dubultās rakstīšanas savienojuma iestatīšana sākas Finanšu un operāciju vidē.

Pirms sākat dubulto rakstiet entītijā, varat veikt sākotnējo sinhronizāciju, lai apstrādātu esošos datus abās pusēs: Finanšu un operāciju programmas un debitoru piesaistes programmas. Varat izlaist sākotnējo sinhronizāciju, ja nav vajadzības sinhronizēt datus starp abām vidēm.

Veicot sākotnējo sinhronizāciju, varat kopēt esošos datus no vienas programmas uz citu divvirzienu formā. Ir vairāki dažādi iestatīšanas scenāriji atkarībā no tā, kādas vides jums jau ir un kāda veida dati tajās ir.

Tālāk ir norādīti atbalstītie iestatīšanas scenāriji:

+ [Jauna finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance](#new-new)
+ [Jauna finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance](#new-existing)
+ [Jauna finanšu un operāciju programmas instance, kurā ir dati un jauna debitoru iesnidņu programmas instance](#new-data-new)
+ [Jauna finanšu un operāciju programmas instance, kurā ir dati un esoša debitoru iesiešanu programmas instance](#new-data-existing)
+ [Esoša finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance](#existing-new)
+ [Esoša finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Jauna finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance

Lai iestatītu dubultās rakstīšanas savienojumu starp jaunu Finanšu un operāciju programmas instanci, kurā nav datu un jauna debitoru iesaistīšanas programmas instance, [izpildiet Duālās rakstīšanas iestatījumu darbības, izmantojot Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Ir nodrošināta jauna, tukša finanšu un operāciju vide.
- Tiek nodrošināta jauna, tukša klientu iesaistīšanas programmas instance, kurā ir instalēts CRM galvenais risinājums.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Jauna finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance

Lai iestatītu dubultās rakstīšanas savienojumu starp jaunu Finanšu un operāciju programmas instanci, kurā nav datu un esošas debitoru iesaistīšanas programmas instances, [izpildiet Duālās rakstīšanas iestatījumu darbības, izmantojot Lifecycle Services](lcs-setup.md). Kad savienojuma iestatīšana ir pabeigta, automātiski tiek veiktas tālāk norādītās darbības.

- Ir nodrošināta jauna, tukša finanšu un operāciju vide.
- Tiek izveidots duālā ieraksta savienojums DAT uzņēmuma datiem.
- Tabulas kartes ir iespējotas tiešsaistes sinhronizācijai.

Abas vides pēc tam ir gatavas tiešsaistes datu sinhronizācijai.

Lai sinhronizētu esošos Dataverse datus finanšu un operāciju programmā, sekojiet šiem soļiem.

1. Izveidojiet jaunu uzņēmumu Finanšu un operāciju programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) datus Dataverse, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Saites uz piemēru un alternatīvu pieeju skatiet tālāk šī [raksta](#example) sadaļā Piemērs.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Jauna finanšu un operāciju programmas instance, kurā ir dati un jauna debitoru iesnidņu programmas instance

Lai iestatītu duālu rakstīšanas savienojumu starp jaunu finanšu un operāciju programmas instanci, kurā ir dati un jauna debitoru iesaistīšanas programmas instance, [izpildiet](#new-new) darbības jaunā finanšu un operāciju programmas instancē un jaunajā debitoru saistību programmas instances sadaļā, kas atrodas agrāk šajā rakstu. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. Atveriet finanšu un operāciju programmu no LCS lapas, piesakieties un pēc tam dodieties uz datu **pārvaldības \> divkāju rakstiet**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Jauna finanšu un operāciju programmas instance, kurā ir dati un esoša debitoru iesiešanu programmas instance

Lai iestatītu duālu rakstīšanas savienojumu starp jaunu finanšu un operāciju programmas instanci, kurā ir dati un esoša debitoru lietojumprogrammas lietojumprogrammas instance, [izpildiet](#new-existing) jauno finanšu un operāciju programmas instances un esošas debitoru lietojumprogrammas instances sadaļā norādītās darbības, kas ir agrākas šajā rakstā. Kad savienojuma iestatīšana ir pabeigta, ja vēlaties sinhronizēt demonstrācijas datus uz klientu iesaistīšanas programmu, veiciet šādas darbības.

1. Atveriet finanšu un operāciju programmu no LCS lapas, piesakieties un pēc tam dodieties uz datu **pārvaldības \> divkāju rakstiet**.
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai sinhronizētu esošos Dataverse datus finanšu un operāciju programmā, sekojiet šiem soļiem.

1. Izveidojiet jaunu uzņēmumu Finanšu un operāciju programmā.
2. Pievienojiet uzņēmumu duālā ieraksta savienojuma iestatījumiem.
3. [Palaidiet](bootstrap-company-data.md) Dataverse datus, izmantojot trīs burtu Starptautiskās Standartizācijas organizācijas (ISO) uzņēmuma kodu.
4. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Esoša finanšu un operāciju programmas instance un jauna debitoru piesaistes programmas instance

Duālā rakstīšanas savienojuma iestatījums starp esošu Finanšu un operāciju programmas instanci un jaunu debitoru piesaistes programmas instanci rodas Finanšu un operāciju vidē.

1. [Iestatiet savienojumu no programmas Finanses un operācijas](enable-dual-write.md).
2. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Esoša finanšu un operāciju programmas instance un esoša debitoru piesaistes programmas instance

Dubultās rakstīšanas savienojuma starp esošu Finanšu un operāciju programmas instanci un esošu debitoru piesaistes programmas instanci iestatīšana notiek Finanšu un operāciju vidē.

1. [Iestatiet savienojumu no programmas Finanses un operācijas](enable-dual-write.md).
2. Lai sinhronizētu esošos Dataverse datus programmā Finanses un operācijas, [ar](bootstrap-company-data.md)Dataverse trīs burtu ISO uzņēmuma kodu nosāciet datus.
3. Palaidiet funkciju **Sākotnējās sinhronizācijas** tabulām, kam vēlaties sinhronizēt datus.

Lai skatītu saites uz piemēru un alternatīvu pieeju, skatiet sadaļu [Piemērs](#example).

## <a name="example"></a>Paraugs

Piemēru skatiet [V3 klientu iespējošana — kontaktpersonu tabulas karte](enable-entity-map.md#enable-table-map)

Lai varētu izmantot alternatīvu pieeju, kas balstās uz datu apjomu katrā elementā, kam jāpalaiž sākotnējā sinhronizāciju, skatiet [Apsvērumi par sākotnējo sinhronizāciju](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]