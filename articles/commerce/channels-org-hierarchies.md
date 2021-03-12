---
title: Iestatīt organizāciju hierarhijas
description: Šajā tēmā ir aprakstīts, kā iestatīt organizācijas hierarhijas programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b887616ef29396ba99ca0c7428ab89df01b3008c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997779"
---
# <a name="set-up-organization-hierarchies"></a>Iestatīt organizāciju hierarhijas


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā iestatīt organizācijas hierarhijas programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Pirms kanālu izveides ir jāapstiprina, ka jūs vēlaties iestatīt organizācijas hierarhijas.

Varat izmantot organizācijas hierarhijas, lai apskatītu jūsu uzņēmējtransakciju no dažādām perspektīvām un veidotu pārskatus. Piemēram, varat iestatīt vienu hierarhiju nodokļu, juridiskajai vai ar likumu noteikto pārskatu veidošanai. Pēc tam varat iestatīt citu hierarhiju, lai veidotu pārskatu par finanšu informāciju, kas saskaņā ar likumu nav obligāta, bet tiek izmantota iekšējos pārskatos.

Pirms organizācijas hierarhijas izveides jāizveido organizācijas. Papildinformāciju skatiet sadaļā [Izveidot juridisku personu](channels-legal-entities.md) vai [izveidot struktūrvienības](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Papildinformāciju skatiet tālāk norādītajās tēmās.
- [Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
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

![Organizācijas hierarhijas piemēri](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Pievienot organizācijas hierarhijai

Lai pievienotu organizāciju hierarhijai, veiciet tālāk norādīto.

1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu. Atlasiet hierarhiju.
1. Darbību rūtī atlasiet **Skatīt**.
1. Nepieciešamības gadījumā pievienojiet papildu organizācijas.
1. Lai pievienotu organizāciju, atlasiet **Rediģēt** un pēc tam atlasiet **Ievietot**. Kad esat pabeidzis izmaiņu veikšanu, varat saglabāt melnrakstu un publicēt izmaiņas.

Tālāk esošajā attēlā redzama juridiska persona, kas pievienota hierarhijas saknē ar četriem izmaksu centriem, kas pievienoti kanāliem “Mall”, “Outlet”, “Online” un “Call Center”. Katram no tiem var pievienot dažādus mazumtirdzniecības, zvanu centru un tiešsaistes kanālus.

![Hierarhijas dizainera piemērs](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Papildu resursi

[Organizācijas un organizāciju hierarhiju pārskats](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organizācijas hierarhijas plānošana](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Izveidot juridiskās personas](channels-legal-entities.md)

[Pārvaldības struktūrvienību izveide](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanālu apskats](channels-overview.md)

[Kanālu iestatīšanas priekšnosacījumi](channels-prerequisites.md)
