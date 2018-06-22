---
title: "Projekta izdevumu kategoriju sinhronizēšana no programmas Project Service Automation"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp programmām Microsoft Dynamics 365 for Finance and Operations un Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekta izdevumu kategoriju sinhronizēšana starp programmām Finance and Operations un Project Service Automation

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti projekta izdevumu kategoriju sinhronizēšanai starp programmām Microsoft Dynamics 365 for Finance and Operations un Dynamics 365 for Project Service Automation.

> [!NOTE]
> Projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana ir pieejama programmas Dynamics 365 for Finance and Operations versijā 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Datu plūsma programmai Project Service Automation un programmai Finance and Operations

Risinājums, lai veiktu integrēšanu starp programmām Project Service Automation un Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projekta izdevumu transakciju kategorijām starp programmu Finance and Operations un programmu Project Service Automation.

Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, integrācijas plūsma vispirms tiek nosūtīta no programmas Finance and Operations uz programmu Project Service Automation, un pēc tam tiek veikta projekta izdevumu kategoriju integrācijas ID atjaunināšana, sinhronizējot no programmas Project Service Automation uz programmu Finance and Operations.

Ja projekta izdevumu kategorijas tiek pārvaldītas programmā Project Service Automation, integrācijas plūsma vispirms tiek nosūtīta no programmas Project Service Automation uz programmu Finance and Operations. Projekta kategorijām jau ir jābūt konfigurētām programmā Finance and Operations pirms sinhronizācijas no programmas Project Service Automation. Pēc tam sinhronizējiet no programmas Finance and Operations atpakaļ uz programmu Project Service Automation un pēc tam vēlreiz no programmas Project Service Automation uz programmu Finance and Operations. Tas nodrošina, ka kategorijas ir saistītas un ka nav izveidoti dublikāti.

> [!NOTE]
> Parasti projekta izdevumu kategoriju pārvaldība tiek veikta programmā Finance and Operations. Ja jūsu situācija ir atšķirīga vai jums jau ir izveidotas projekta izdevumu kategorijas programmā Project Service Automation, vispirms jāveic sinhronizēšana, izmantojot Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops) un pēc jāveic sinhronizēšana, izmantojot Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA). Pēc tam vēlreiz jāpalaiž sinhronizēšana no PSA uz Fin and Ops.

> Ja vispirms tiek veikta sinhronizēšana no programmas Project Service Automation, projektu kategorijām jau ir jābūt izveidotām programmā Finance and Operations un visām projektu kategorijām, kuras nepieciešams sinhronizēt ar programmas Project Service Automation transakciju kategorijām, jābūt iestatītam vienumam **Aktīvs žurnālos**.

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

Lai piekļūtu pieejamajām veidnēm, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Finance and Operations ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Project Service Automation tiek izmantota tālāk norādītā veidne un pamata uzdevums.

-  **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA)
-  **Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz PSA

## <a name="entity-set"></a>Elementu kopa

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Integrācijas elements kategorijām    | Transakciju kategorijas        |

## <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas.

## <a name="power-query"></a>Power Query

Ir jāizmanto Microsoft Power Query, lai iestatītu transakciju kategorijas norēķinu veidu, veicot sinhronizēšanu uz programmu Project Service Automation. Veidnei Projekta izdevumu transakciju kategorijas (no Fin and Ops uz PSA) jau ir nodrošināta noklusējuma kolonna un kartēšana. Ja izveidojat savu veidni, ir jāpievieno šī nosacījuma kolonna risinājumā Power Query.
- Atveriet veidlapu Izvērsts vaicājums un filtrēšana no projekta izdevumu kategoriju uzdevuma kartējuma.
- Atlasiet **Pievienot nosacījuma kolonnu**.
- Piešķiriet jaunajai kolonnai nosaukumu, piemēram “BillingType”.
- Ievadiet šādu nosacījumu: “If **CATEGORYID not equal to null then 19235001, Otherwise null**”.
- Noklikšķiniet **Labi** uz kolonnas.
- Noteikti kartējiet šo jauno kolonnu kartēšanas lapā.

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija. Kartējums norāda programmā Finance and Operations ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Project Service Automation.

[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Programmā Project Service Automation ietverto projekta izdevumu kategoriju sinhronizēšanai ar programmu Finance and Operations tiek izmantota tālāk norādītā veidne un pamata uzdevums.

-**Veidnes nosaukums līdzeklī Datu integrācija:** Projekta izdevumu transakciju kategorijas (no PSA uz Fin and Ops) -**Projekta uzdevuma nosaukums:** Kategoriju sinhronizēšana uz Fin and Ops

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Transakciju kategorijas          | Integrācijas elements kategorijām  | 

## <a name="entity-flow"></a>Elementu plūsma

Projekta izdevumu kategorijas tiek pārvaldītas programmā Finance and Operations, un tās tiek sinhronizētas ar programmu Project Service Automation kā transakciju kategorijas. Sinhronizēšana atpakaļ uz programmu Finance and Operations atjaunina programmā Project Service Automation ietverto integrācijas ID programmas Finance and Operations projekta kategorijā.

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartēšanai līdzeklī Datu integrācija.

> [!NOTE]
> Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.

[![Veidnes kartēšana](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

