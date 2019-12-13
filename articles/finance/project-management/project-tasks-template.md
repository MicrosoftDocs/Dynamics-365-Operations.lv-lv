---
title: Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir apskatīta veidne un pamata uzdevums, kas tiek izmantoti programmā Microsoft  Dynamics 365 Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Dynamics 365 Finance.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770270"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir apskatīta veidne un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Dynamics 365 Finance.

> [!NOTE]
> - Versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.
> - Ja lietojat Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, mēs ieteicām instalēt arī KB 4131710.
> - Faktisko vērtību integrācija ir pieejama versijā 8.0.1 vai jaunākās versijās.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation datu plūsma uz programmu Finance

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation uz programmu Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance instancēs. Integrācijas veidne, kas ir pieejama līdzeklī Datu integrācija, iespējo datu plūsmu par projekta uzdevumiem no programmas Project Service Automation uz programmu Finance.

Nākamajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Veidne un uzdevums

Lai piekļūtu veidnei, Microsoft Power Apps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Programmā Project Service Automation ietverto uzdevumu sinhronizēšanai ar programmu Finance tiek izmantota tālāk norādītā veidne un pamata uzdevums.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta uzdevumi (no PSA uz Fin and Ops)
- **Uzdevuma nosaukums projektā:** Projekta uzdevumi

Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation | Finansēt                             |
|----------------------------|-------------------------------------|
| Projekta uzdevumi              | Integrācijas elements projekta uzdevumam |

## <a name="entity-flow"></a>Elementu plūsma

Projekta uzdevumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance kā projekta aktivitātes.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.

## <a name="power-query"></a>Power Query

Ja ir izpildīts tālāk norādītais nosacījums, datu filtrēšanai ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel.

- Projekta uzdevumā jums ir resursam raksturīgi ieraksti.

Ja ir jāizmanto Power Query, ievērojiet tālāk minēto norādījumu.

- Veidnē “Projekta uzdevumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas no projekta uzdevuma izslēdz resursam raksturīgus ierakstus, vienumam **IsLineTask** filtru iestatot uz **False** (Aplams). Ja izveidojat savu veidni, ir jāpievieno šis filtrs.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartējumiem līdzeklī Datu integrācija. Kartējums norāda lauku informāciju, kas tiks sinhronizēta no programmas Project Service Automation uz programmu Finance.

[![Veidnes kartēšana](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
