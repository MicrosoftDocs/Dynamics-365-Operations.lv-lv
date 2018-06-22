---
title: Project Service Automation
description: "Šis risinājums izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Project Service Automation instancēs, izmantojot Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: lv-lv
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Risinājums, lai veiktu integrēšanu no programmas Project Service Automation programmā Finance and Operations, izmanto līdzekli Datu integrācija, lai sinhronizētu datus programmu Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Project Service Automation instancēs, izmantojot Common Data Service (CDS). Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo datu plūsmu par projektiem, projekta līgumiem, projektiem, projekta līguma rindām, projekta līguma rindas atskaites punktiem, projekta uzdevumiem, izdevumu transakciju kategorijām, stundu novērtējumiem un izdevumu novērtējumiem no programmas Project Service Automation programmā Finance and Operations.

> [!NOTE] 
> Ja izmantojat Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, jums ir jāinstalē KB 4074835. Tas ļaus integrēt fiksētas cenas projektus.
>
> Ja izmantojat programmas Dynamics 365 for Finance and Operations versiju 8.0, varēsit izmantot projekta uzdevumu integrāciju, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un funkcionalitātes bloķēšanu.
>
> Ja izmantojat programmas Dynamics 365 for Finance and Operations versiju 8.0.1, varēsit sinhronizēt faktiskās vērtības.
>
> Ja izmantojat programmu Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varēsit izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, ieteicams arī instalēt KB 4131710.

Pirms programmas Project Service Automation integrēšanas ar programmu Finance and Operations ir jākonfigurē Project Service Automation integrācijas parametri. Papildu informāciju skatiet sadaļā Project Service Automation integrācijas parametri.

Šis integrācijas risinājums nodrošina tiešu sinhronizēšanu tālāk norādītajos scenārijos.

- Uzturiet projekta līgumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Izveidojiet projektus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet projekta līguma rindas programmā Project Service Automation un sinhronizējiet tās tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet projekta līguma rindas atskaites punktus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet projekta uzdevumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet izdevumu transakciju kategorijas programmā Finance and Operations un sinhronizējiet tās tieši no programmas Finance and Operations ar programmu Project Service Automation.
- Izveidojiet projekta stundu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Izveidojiet projekta izdevumu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.

## <a name="data-synchronization"></a>Datu sinhronizācija
Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana integrācijas procesa ietvaros programmās Project Service Automation un Finance and Operations.

> [!NOTE]
> Šobrīd nav pieejamas visas veidnes. Veidnes tiks izlaistas pēc to pabeigšanas.

[![Programmas Project Service Automation integrēšana ar programmu Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations

Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance and Operations, ir jāinstalē programma Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 ar platformas 12. atjauninājumu vai jaunāku versiju.

## <a name="system-requirements-for-project-service-automation"></a>Sistēmas prasības programmai Project Service Automation

Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance and Operations, ir jāinstalē šādi komponenti.

- Microsoft Dynamics 365 for Project Service Automation, versija 9.0.0.0 vai jaunāka.
- Risinājums No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 for Sales, versija 1.14.0.0 (v14) vai jaunāka.
- Risinājums programmas Project Service Automation integrēšanai ar Finance and Operations programmai Dynamics 365 for Project Service Automation, versija 1.0.0.0 vai jaunāka.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Risinājuma programmas Project Service Automation integrēšanai ar programmu Finance and Operations instalēšana jūsu Project Service Automation instancē



