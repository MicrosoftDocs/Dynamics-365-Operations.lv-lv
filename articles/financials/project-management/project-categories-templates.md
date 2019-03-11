---
title: Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu programmā Microsoft Dynamics 365 for Finance and Operations ietvertās projekta izdevumu kategorijas ar programmu Microsoft Dynamics 365 for Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "347840"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu programmā Microsoft Dynamics 365 for Finance and Operations ietvertās projekta izdevumu kategorijas ar programmu Microsoft Dynamics 365 for Project Service Automation.

> [!NOTE]
> - Microsoft Dynamics 365 for Finance and Operations versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.
> - Faktisko vērtību integrācija ir pieejama Microsoft Dynamics 365 for Finance and Operations versijā 8.0.1 vai jaunākās versijās.
> - Ja lietojat Microsoft Dynamics 365 for Finance and Operations Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, ieteicams arī instalēt KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Datu plūsma programmai Project Service Automation un programmai Finance and Operations

Risinājums, lai veiktu integrēšanu starp programmām Project Service Automation un Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo projekta izdevumu transakciju kategoriju datu plūsmu starp programmu Finance and Operations un programmu Project Service Automation.

Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, integrācijas plūsma vispirms tiek nosūtīta no programmas Finance and Operations uz programmu Project Service Automation. Pēc tam projekta izdevumu kategoriju integrācijas ID tiek atjaunināti, veicot sinhronizāciju no programmas Project Service Automation uz Finance and Operations.

Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Project Service Automation, integrācijas plūsma vispirms tiek nosūtīta no programmas Project Service Automation uz programmu Finance and Operations. Projekta kategorijām jau ir jābūt konfigurētām programmā Finance and Operations pirms sinhronizācijas no programmas Project Service Automation. Pēc tam sinhronizējiet no programmas Finance and Operations atpakaļ uz programmu Project Service Automation un pēc tam vēlreiz no programmas Project Service Automation uz programmu Finance and Operations. Šādā veidā varat nodrošināt, ka tiek saistītas kategorijas un netiek izveidoti dublikāti.

> [!NOTE]
> Parasti projekta izdevumu kategoriju pārvaldība tiek veikta programmā Finance and Operations. Taču, ja izdevumu kategorijas netiek pārvaldītas programmā Finance and Operations vai tās jau ir izveidotas programmā Project Service Automation, vispirms veiciet sinhronizāciju, izmantojot veidni Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops). Pēc tam veiciet sinhronizāciju, izmantojot veidni Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA). Pēc tam vēl vienu reizi ir jāpalaiž sinhronizācija no Project Service Automation uz Finance and Operations.
>
> Ja vispirms sinhronizējat no programmas Project Service Automation, pirms sinhronizēšanas palaišanas programmā Finance and Operations ir jābūt ievērotām tālāk norādītajām prasībām.
>
> - Ir jābūt koplietojamai kategorijai, kas atbilst programmā Project Service Automation iestatītajai projekta kategorijai, un tai ir jābūt iespējotai gan vienumam **Projekts**, gan vienumam **Izdevumi**.
> - Katrai Finance and Operations juridiskajai personai, ar kuru ir jābūt veiktai integrācijai, ir jābūt tālāk norādītajām projekta kategorijām.
>
>     - Pastāv **Projekta kategorija**. 
>     - Ir iespējots vienums **Lietot izdevumos**.
>     - Ir iespējots vienums **Aktīvs žurnālā**.
>     - **Transakcijas veids** ir iestatīts uz **Izdevumi**.

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Projekta izdevumu kategoriju sinhronizēšana no programmas Finance and Operations uz Project Service Automation

### <a name="template-and-task"></a>Veidne un uzdevums

Lai piekļūtu veidnei, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Finance and Operations ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Project Service Automation tiek izmantota tālāk norādītā veidne un pamata uzdevums.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA)
- **Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz PSA

### <a name="entity-set"></a>Elementu kopa

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrācijas elements kategorijām | Transakciju kategorijas     |

### <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas.

### <a name="power-query"></a>Power Query

Kad veicat sinhronizāciju ar programmu Project Service Automation, ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel, lai iestatītu transakciju kategorijas norēķinu veidu. Veidne Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) nodrošina noklusējuma kolonnu un kartējumu. Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna risinājumā Power Query. Veiciet tālāk norādītās darbības.

1. Noklikšķiniet uz bultiņas, lai veidnē Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) atvērtu projekta izdevumu kategoriju uzdevuma kartējumu.
2. Noklikšķiniet uz saites **Paplašinātais vaicājums un filtrēšana**, lai atvērtu Power Query.
2. Atlasiet **Pievienot nosacījuma kolonnu**.
3. Ievadiet jaunās kolonnas nosaukumu, piemēram, **BillingType**.
4. Ievadiet šādu nosacījumu: **ja CATEGORYID nav vienāds ar Null, tad 19235001; pretējā gadījumā vērtība ir Null**.
5. Noklikšķiniet **Labi** uz kolonnas.
6. Noteikti kartējiet šo jauno kolonnu uz kartējuma lapu.

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Finance and Operations ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Project Service Automation.

[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Projekta izdevumu kategoriju sinhronizēšana no programmas Project Service Automation uz Finance and Operations

### <a name="template-and-task"></a>Veidne un uzdevums

Programmā Project Service Automation ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevums.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops)
- **Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz Fin Ops

### <a name="entity-set"></a>Elementu kopa

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Transakciju kategorijas     | Integrācijas elements kategorijām |

### <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas. Sinhronizēšana atpakaļ uz programmu Finance and Operations atjaunina programmā Finance and Operations ietverto projekta kategoriju ar Project Service Automation integrācijas ID.

### <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.

> [!NOTE]
> Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.

[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
