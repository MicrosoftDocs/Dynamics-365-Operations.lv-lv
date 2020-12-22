---
title: Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana
description: Šajā tēmā ir aprakstīts, kā rediģēt mazumtirdzniecības darījumu finanšu dimensijas programmā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: e26bd4eb53fa44330f15c7cda004cb3d19dfec6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459514"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Mazumtirdzniecības darījumu finanšu dimensiju rediģēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā rediģēt mazumtirdzniecības darījumu finanšu dimensijas programmā Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>Finanšu dimensiju rediģēšana

Lai rediģētu mazumtirdzniecības darījumu finanšu dimensijas komponentā Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Atveriet lapu **Finanšu dimensiju konfigurēšana programmu integrēšanai**.
1. Atlasiet aktīvo ierakstu **Noklusējuma dimensiju integrācija**.
1. Kopsavilkuma cilnē **Finanšu dimensijas** pārliecinieties, vai sarakstā **Atlasīts** ir visas dimensijas, kuras vēlaties rediģēt Excel darblapā. Plašāku informāciju skatiet sadaļā [Datu elementi](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).
1. Lejupielādējiet un atveriet Excel failu lapā **Pārskati**, lapā **Mazumtirdzniecības darījumi** vai elementā **Darījumu validācijas kļūmes** darbvietā **Veikala finanses**.
1. Lai mainītu darījuma finanšu dimensiju, atlasiet **Noformējums** un pēc tam atlasiet zīmuļa simbolu blakus rindai **Darījums (auditējams)**.
1. Atrodiet un atlasiet lauku **FinancialDimensionDisplayValue**, atlasiet šūnu Excel darblapas galvenes daļā un pēc tam atlasiet **Pievienot etiķeti**.
1. Atlasiet šūnu zem iepriekšējā darbībā atlasītās šūnas, atlasiet **Pievienot vērtību** un pēc tam atlasiet **Atsvaidzināt**. Finanšu dimensijas ir pievienotas Excel darblapai, un pēc tam tās var rediģēt un publicēt.
1. Lai mainītu dimensijas darījumu rindās, atlasiet rindu **Pārdošanas darījumi (auditējami)**, atlasiet zīmuļa simbolu un pēc tam atkārtojiet 6. un 7. darbību.
1. Lai mainītu dimensijas maksājumu rindās, atlasiet rindu **Maksājumu darījumi (auditējami)**, atlasiet zīmuļa simbolu un pēc tam atkārtojiet 6. un 7. darbību.

## <a name="additional-resources"></a>Papildu resursi

[Darījumu, kas saistīti ar pārdošanu skaidrā naudā bez piegādes, un skaidras naudas pārvaldības darījumu rediģēšana un auditēšana](edit-cash-trans.md)

[Tiešsaistes pasūtījumu un asinhrono debitoru pasūtījumu darījumu rediģēšana un auditēšana](edit-order-trans.md)

[Excel darbgrāmatas izveide, lai rediģētu mazumtirdzniecības darījumus](create-excel-edit.md)

[Lauku pievienošana Excel darbgrāmatai, lai rediģētu mazumtirdzniecības darījumus](add-fields-excel.md)
