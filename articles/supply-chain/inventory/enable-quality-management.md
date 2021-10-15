---
title: Iespējot kvalitātes un neatbilstības pārvaldību
description: Šajā tēmā sniegts pārskats par kvalitātes un neatbilstības pārvaldības līdzekļu iestatīšanas un konfigurēšanas procesu Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2c8b7e9a1a8d7692e1d2215e38de1b0f4d2d82
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567419"
---
# <a name="enable-quality-and-nonconformance-management"></a>Iespējot kvalitātes un neatbilstības pārvaldību

[!include [banner](../includes/banner.md)]

Šajā tēmā sniegts pārskats par kvalitātes un neatbilstības pārvaldības līdzekļu iestatīšanas un konfigurēšanas procesu Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Iespējot kvalitātes un neatbilstības pārvaldību

Veiciet šīs darbības, lai iespējotu jūsu sistēmas kvalitātes pārvaldību.

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Krājumu un noliktavas pārvaldības parametri**.
1. Cilnē **Kvalitātes pārvaldība** iestatiet opciju **Izmantot kvalitātes pārvaldību** uz *Jā*.
1. Laukā **Stundas likme** ievadiet darbaspēka stundas likmi vietējā valūtā. Stundas likme tiek lietota, lai aprēķinātu izmaksas operācijām, kas ir saistītas ar neatbilstību. Stundas likme un aprēķinātās izmaksas nodrošina atsauces informāciju par neatbilstību. Šie vienumi nemijiedarbojas ar citām funkcijām.
1. Atlasiet **Pārskata iestātīšana**.
1. Pievienojiet jaunas rindas dažādiem pārskatu veidiem un atlasiet dokumenta veidu, ko lietot katram pārskatam.
1. Aizvērt lapu.
1. Aizvērt lapu.

## <a name="quality-management-configuration-process"></a>Kvalitātes pārvaldības konfigurācijas process

Pirms varat sākt izmantot kvalitātes pārvaldības līdzekļus un izveidot kvalitātes pasūtījumus, jums ir jākonfigurē sistēma un priekšnosacījumi. Šeit ir saraksts ar darbībam, kas nepieciešamas kvalitātes pārvaldības konfigurēšanai.

1. [Iespējot kvalitātes un neatbilstības pārvaldību](#enable-qm).
1. Nav obligāti: [Konfigurēt testa instrumentus](quality-test-instruments.md).
1. [Konfigurēt testus](quality-tests.md).
1. [Konfigurējiet testa mainīgos un iznākumus](quality-test-variables.md).
1. [Konfigurējiet testa grupas](quality-test-groups.md).
1. Nav obligāti: [Konfigurējiet kvalitātes grupas un saistiet tās ar precēm](quality-groups.md).
1. Nav obligāti: [Konfigurēt kvalitātes saistības](quality-associations.md).

Kad konfigurācija ir pabeigta, jūs varat sākt veidot un apstrādāt kvalitātes pasūtījumus. Plašāku informāciju par to, kā izveidot un strādāt ar kvalitatīviem pasūtījumiem skatiet sadaļā [Kvalitātes pārbaudes pasūtījums](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Neatbilstības pārvaldības konfigurācijas process

Pirms varat sākt izmantot neatbilstības pārvaldības līdzekļus un izveidot neatbilstības, jums ir jākonfigurē sistēma un priekšnosacījumi. Šeit ir saraksts ar darbībam, kas nepieciešamas neatbilstības pārvaldības konfigurēšanai.

1. [Iespējot kvalitātes un neatbilstības pārvaldību](#enable-qm).
1. [Konfigurēt darbiniekus, kuri ir atbildīgi par neatbilstības apstiprināšanu](quality-responsible-workers.md).
1. [Konfigurējiet problēmu veidus](quality-problem-types.md).
1. [Konfigurējiet karantīnas zonas](quality-quarantine-zones.md).
1. [Konfigurēt diagnostikas tipus](quality-diagnostic-types.md).
1. [Konfigēt operācijas](quality-operations.md).
1. Nav obligāti: [Konfigurēt kvalitātes maksas](quality-charges.md).

Kad konfigurācija ir pabeigta, jūs varat sākt veidot un apstrādāt neatbilstības. Plašāku informāciju par to, kā izveidot neatbilstības un strādāt ar tām, skatiet rakstā [Izveidot un apstrādāt neatbilstības](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Papildu resursi

- [Kvalitātes pārvaldības pārskats](quality-management-processes.md)
- [Iespējot kvalitātes un neatbilstības pārvaldību](enable-quality-management.md)
- [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
