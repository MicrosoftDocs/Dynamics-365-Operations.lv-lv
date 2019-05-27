---
title: Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations
description: Šajā tēmā ir apskatīta veidne un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557928"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projekta uzdevumu sinhronizēšana tieši no Project Service Automation uz Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir apskatīta veidne un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Project Service Automation ietverto projekta uzdevumu tiešai sinhronizēšanai ar programmu Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Microsoft Dynamics 365 for Finance and Operations versijā 8.0 ir pieejama projekta uzdevumu integrācija, izdevumu transakciju kategorijas, stundu novērtējumi, izdevumu novērtējumi un funkcionalitātes bloķēšana.
> - Ja lietojat Microsoft Dynamics 365 for Finance and Operations Enterprise Edition versiju 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varat izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, mēs ieteicām instalēt arī KB 4131710.
> - Faktisko vērtību integrācija ir pieejama Microsoft Dynamics 365 for Finance and Operations versijā 8.0.1 vai jaunākās versijās.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Datu plūsma programmas Project Service Automation sinhronizēšanai ar programmu Finance and Operations

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Project Service Automation un Finance and Operations instancēs. Integrācijas veidne, kas ir pieejama līdzeklī Datu integrācija, iespējo datu plūsmu par projekta uzdevumiem no programmas Project Service Automation uz programmu Finance and Operations.

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana programmās Project Service Automation un Finance and Operations.

[![Datu plūsma programmas Project Service Automation integrēšanai ar programmu Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Veidne un uzdevums

Lai piekļūtu veidnei, Microsoft PowerApps administrēšanas centrā atlasiet vienumu **Projekti** un pēc tam augšējā labajā stūrī atlasiet vienumu **Jauns projekts**, lai atlasītu publiskās veidnes.

Lai projekta uzdevumus no Project Service Automation sinhronizētu uz Finance and Operations, ir jāizmanto tālāk norādītā veidne un pamata uzdevums.

- **Veidnes nosaukums līdzeklī Datu integrācija:** Projekta uzdevumi (no PSA uz Fin and Ops)
- **Uzdevuma nosaukums projektā:** Projekta uzdevumi

Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.

## <a name="entity-set"></a>Elementu kopa

| Project Service Automation | Finance and Operations              |
|----------------------------|-------------------------------------|
| Projekta uzdevumi              | Integrācijas elements projekta uzdevumam |

## <a name="entity-flow"></a>Elementu plūsma

Projekta uzdevumi tiek pārvaldīti programmā Project Service Automation, un tie tiek sinhronizēti ar programmu Finance and Operations kā projekta aktivitātes.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums

Pirms projekta uzdevumu sinhronizēšanas ir jāveic projekta līgumu un projektu sinhronizēšana.

## <a name="power-query"></a>Power Query

Ja ir izpildīts tālāk norādītais nosacījums, datu filtrēšanai ir jāizmanto pievienojumprogramma Microsoft Power Query programmai Excel.

- Projekta uzdevumā jums ir resursam raksturīgi ieraksti.

Ja ir jāizmanto Power Query, ievērojiet tālāk minēto norādījumu.

- Veidnē “Projekta uzdevumi” (no PSA uz Fin and Ops) ir noklusējuma filtrs, kas no projekta uzdevuma izslēdz resursam raksturīgus ierakstus, vienumam **IsLineTask** filtru iestatot uz **False** (Aplams). Ja izveidojat savu veidni, ir jāpievieno šis filtrs.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajā attēlā ir redzams piemērs veidnes uzdevuma kartējumiem līdzeklī Datu integrācija. Kartējums norāda programmā Project Service Automation ietverto lauku informāciju, kas tiks sinhronizēta ar programmu Finance and Operations.

[![Veidnes kartēšana](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
