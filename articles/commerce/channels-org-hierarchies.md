---
title: Iestatīt organizāciju hierarhijas
description: Šajā rakstā ir aprakstīts, kā iestatīt organizācijas hierarhijas Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 2555378c119e4c096c4bf0c0adc11e3a50cbfe38
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280452"
---
# <a name="set-up-organization-hierarchies"></a>Iestatīt organizāciju hierarhijas

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt organizācijas hierarhijas Microsoft Dynamics 365 Commerce.

Pirms kanālu izveides ir jāapstiprina, ka jūs vēlaties iestatīt organizācijas hierarhijas.

Varat izmantot organizācijas hierarhijas, lai apskatītu jūsu uzņēmējtransakciju no dažādām perspektīvām un veidotu pārskatus. Piemēram, varat iestatīt vienu hierarhiju nodokļu, juridiskajai vai ar likumu noteikto pārskatu veidošanai. Pēc tam varat iestatīt citu hierarhiju, lai veidotu pārskatu par finanšu informāciju, kas saskaņā ar likumu nav obligāta, bet tiek izmantota iekšējos pārskatos.

Pirms organizācijas hierarhijas izveides jāizveido organizācijas. Papildinformāciju skatiet sadaļā [Izveidot juridisku personu](channels-legal-entities.md) vai [izveidot struktūrvienības](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Papildinformāciju skatiet šādos rakstos.
- [Organizāciju un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Organizācijas hierarhijas plānošana](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Organizācijas hierarhijas izveide](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Organizāciju hierarhijas izveide

Lai izveidotu organizācijas hierarhijas, izpildiet tālāk norādītās darbības.

1. Navigācijas rūtī pārejiet uz **Moduļi \> Mazumtirdzniecība un komercija \> Kanāla iestatīšana \> Organizācijas hierarhijas**.
1. Darbību rūtī atlasiet **Jauns**.
1. Laukā **Nosaukums** ievadiet vērtību.
1. Sadaļā **Nolūks** atlasiet **Piešķirt nolūku**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet nolūku, kas tiks piešķirts jūsu organizācijas hierarhijai.
1. Sadaļā **Piešķirtās hierarhijas** atlasiet **Pievienot**.
1. Sarakstā atzīmējiet atlasīto rindu. Atrodiet tikko izveidoto hierarhiju.
1. Atlasiet **Labi**.

Tālāk esošajā attēlā redzama parauga organizācijas hierarhija, kas izveidota fiktīvai “Adventure Works” veikalu kopai.

![Organizācijas hierarhijas piemēri.](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Pievienot organizācijas hierarhijai

Lai pievienotu organizāciju hierarhijai, veiciet tālāk norādīto.

1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet hierarhiju.
1. Darbību rūtī atlasiet **Skatīt**.
1. Nepieciešamības gadījumā pievienojiet papildu organizācijas.
1. Lai pievienotu organizāciju, atlasiet **Rediģēt** un pēc tam atlasiet **Ievietot**. Kad esat pabeidzis izmaiņu veikšanu, varat saglabāt melnrakstu un publicēt izmaiņas.

Tālāk esošajā attēlā redzama juridiska persona, kas pievienota hierarhijas saknē ar četriem izmaksu centriem, kas pievienoti kanāliem “Mall”, “Outlet”, “Online” un “Call Center”. Katram no tiem var pievienot dažādus mazumtirdzniecības, zvanu centru un tiešsaistes kanālus.

![Hierarhijas dizainera piemērs.](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Papildu resursi

[Organizāciju un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organizācijas hierarhijas plānošana](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Izveidot juridiskās personas](channels-legal-entities.md)

[Pārvaldības struktūrvienību izveide](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
