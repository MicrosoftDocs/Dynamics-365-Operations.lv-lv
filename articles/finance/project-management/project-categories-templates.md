---
title: Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu programmā Microsoft Dynamics 365 Finance ietvertās projekta izdevumu kategorijas ar programmu Dynamics 365 Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770316"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu programmā Dynamics 365 Finance ietvertās projekta izdevumu kategorijas ar programmu Dynamics 365 Project Service Automation.

> [!NOTE]
> - Versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.
> - Faktisko vērtību integrācija ir pieejama versijā 8.0.1 vai jaunākās versijās.
> - Ja lietojat Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, ieteicams arī instalēt KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Datu plūsma programmas Project Service Automation sinhronizēšanai ar programmu Finance

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance instancēs. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo projekta izdevumu transakciju kategoriju datu plūsmu starp programmu Finance un programmu Project Service Automation.

Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Finance, integrācijas plūsma vispirms tiek nosūtīta no programmas Finance uz programmu Project Service Automation. Pēc tam projekta izdevumu kategoriju integrācijas ID tiek atjaunināti, veicot sinhronizāciju no programmas Project Service Automation uz Finance.

Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Project Service Automation, integrācijas plūsma vispirms tiek nosūtīta no programmas Project Service Automation uz programmu Finance. Projekta kategorijām jau ir jābūt konfigurētām programmā Finance pirms sinhronizācijas no programmas Project Service Automation. Pēc tam sinhronizējiet no programmas Finance atpakaļ uz programmu Project Service Automation un pēc tam vēlreiz no programmas Project Service Automation uz programmu Finance. Šādā veidā varat nodrošināt, ka tiek saistītas kategorijas un netiek izveidoti dublikāti.

> [!NOTE]
> Parasti projekta izdevumu kategoriju pārvaldība tiek veikta programmā Finance. Taču, ja izdevumu kategorijas netiek pārvaldītas vai tās jau ir izveidotas programmā Project Service Automation, vispirms veiciet sinhronizāciju, izmantojot veidni Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops). Pēc tam veiciet sinhronizāciju, izmantojot veidni Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA). Pēc tam vēl vienu reizi ir jāpalaiž sinhronizācija no Project Service Automation uz Finance.
>
> Ja vispirms sinhronizējat no programmas Project Service Automation, pirms sinhronizēšanas palaišanas programmā Finance ir jābūt ievērotām tālāk norādītajām prasībām.
>
> - Ir jābūt koplietojamai kategorijai, kas atbilst programmā Project Service Automation iestatītajai projekta kategorijai, un tai ir jābūt iespējotai gan vienumam **Projekts**, gan vienumam **Izdevumi**.
> - Katrai Finance juridiskajai personai, ar kuru ir jābūt veiktai integrācijai, ir jābūt tālāk norādītajām projekta kategorijām.
>
>     - Pastāv **Projekta kategorija**. 
>     - Ir iespējots vienums **Lietot izdevumos**.
>     - Ir iespējots vienums **Aktīvs žurnālā**.
>     - **Transakcijas veids** ir iestatīts uz **Izdevumi**.

Nākamajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projekta izdevumu kategoriju sinhronizēšana no programmas Finance uz Project Service Automation

### <a name="template-and-task"></a>Veidne un uzdevums

Lai piekļūtu veidnei, Microsoft Power Apps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Finance ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Project Service Automation tiek izmantota tālāk norādītā veidne un pamata uzdevums.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA)
- **Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz PSA

### <a name="entity-set"></a>Elementu kopa

| Finansēt                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrācijas elements kategorijām | Transakciju kategorijas     |

### <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas.

### <a name="power-query"></a>Power Query

Kad veicat sinhronizāciju ar programmu Project Service Automation, ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel, lai iestatītu transakciju kategorijas norēķinu veidu. Veidne Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) nodrošina noklusējuma kolonnu un kartējumu. Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna risinājumā Power Query. Veiciet tālāk norādītās darbības.

1. Noklikšķiniet uz bultiņas, lai veidnē Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) atvērtu projekta izdevumu kategoriju uzdevuma kartējumu.
2. Noklikšķiniet uz saites **Paplašinātais vaicājums un filtrēšana**, lai atvērtu Power Query.
2. Atlasiet **Pievienot nosacījuma kolonnu**.
3. Ievadiet jaunās kolonnas nosaukumu, piemēram, **BillingType**.
4. Ievadiet šādu nosacījumu: **ja CATEGORYID nav vienāds ar Null, tad 19235001; pretējā gadījumā vērtība ir Null**.
5. Noklikšķiniet **Labi** uz kolonnas.
6. Noteikti kartējiet šo jauno kolonnu uz kartējuma lapu.

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Finance ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Project Service Automation.

[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projekta izdevumu kategoriju sinhronizēšana no Project Service Automation uz programmu Finance

### <a name="template-and-task"></a>Veidne un uzdevums

Programmā Project Service Automation ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevums.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops)
- **Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz Fin Ops

### <a name="entity-set"></a>Elementu kopa

| Project Service Automation | Finansēt                           |
|----------------------------|-----------------------------------|
| Transakciju kategorijas     | Integrācijas elements kategorijām |

### <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas. Sinhronizēšana atpakaļ uz programmu Finance atjaunina programmā Finance ietverto projekta kategoriju ar Project Service Automation integrācijas ID.

### <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.

> [!NOTE]
> Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.

[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
