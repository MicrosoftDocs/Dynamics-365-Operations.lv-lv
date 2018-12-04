---
title: Project Service Automation
description: "Šajā tēmā ir sniegta informācija par integrēšanas risinājumu programmas Project Service Automation integrēšanai programmā Finance and Operations. Lai sinhronizētu datus programmu Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Project Service Automation instancēs, izmantojot Common Data Service, šis integrēšanas risinājums izmanto līdzekli Datu integrācija."
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

Lai sinhronizētu datus programmu Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Project Service Automation instancēs, izmantojot Common Data Service, integrēšanas risinājums programmas Project Service Automation integrēšanai programmā Finance and Operations izmanto līdzekli Datu integrācija. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo projektu, projekta līgumu, projekta līgumu rindu, projekta līgumu rindu atskaites punktu, projekta uzdevumu, izdevumu transakciju kategoriju, stundu novērtējumu un izdevumu novērtējumu datu plūsmu no programmas Project Service Automation uz programmu Finance and Operations.

> [!NOTE]
> - Ja izmantojat programmu Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0, pēc KB 4132657 un KB 4132660 instalēšanas varēsit izmantot veidnes, lai integrētu projekta uzdevumus, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un faktiskās vērtības, kā arī konfigurēt funkcionalitātes bloķēšanu. Ja ir nepieciešams atiestatīt uzskaites sadali, ieteicams arī instalēt KB 4131710.
> - Ja lietojat versiju Finance and Operations 7.3.0, ir jāinstalē KB 4074835. Pēc tam jūs varēsit integrēt fiksētas cenas projektus.
> - Ja izmantojat Finance and Operations versiju 7.3.0 un pārceļat maksu transakcijas no programmas Project Service Automation, ir jāinstalē KB 4345320, lai šīs maksas ietvertu projekta rēķinā.
> - Ja izmantojat programmas Microsoft Dynamics 365 for Finance and Operations versiju 8.0, varēsit izmantot projekta uzdevumu integrāciju, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un funkcionalitātes bloķēšanu.
> - Ja izmantojat programmas Microsoft Dynamics 365 for Finance and Operations versiju 8.0.1 vai jaunāku, varēsit sinhronizēt faktiskās vērtības.

Pirms programmas Project Service Automation integrēšanas ar programmu Finance and Operations ir jākonfigurē Project Service Automation integrācijas parametri. Papildinformāciju skatiet tēmā [Project Service Automation integrācijas parametri](PSA-parameters.md).

Šis integrācijas risinājums nodrošina tiešu sinhronizēšanu tālāk norādītajos scenārijos.

- Uzturiet projekta līgumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Izveidojiet projektus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet projekta līguma rindas programmā Project Service Automation un sinhronizējiet tās tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet projekta līguma rindas atskaites punktus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet projekta uzdevumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Uzturiet izdevumu transakciju kategorijas programmā Finance and Operations un sinhronizējiet tās tieši no programmas Finance and Operations ar programmu Project Service Automation.
- Izveidojiet projekta stundu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Izveidojiet projekta izdevumu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance and Operations.
- Izveidojiet projekta laiku, izdevumus un faktiskās vērtības programmā Project Service Automation un izveidojiet projekta transakcijas programmas Project Service Automation integrācijas žurnālā, lai tos varētu grāmatot programmā Finance and Operations.

## <a name="data-synchronization"></a>Datu sinhronizācija

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana integrācijas procesa ietvaros programmās Project Service Automation un Finance and Operations.

> [!NOTE]
> Šobrīd nav pieejamas visas veidnes. Veidnes tiks izlaistas pēc to pabeigšanas.

[![Programmas Project Service Automation integrēšana ar programmu Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Sistēmas prasības programmai Finance and Operations

Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance and Operations, ir jāinstalē programma Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 ar platformas 12. atjauninājumu vai jaunāku versiju.

## <a name="system-requirements-for-project-service-automation"></a>Sistēmas prasības programmai Project Service Automation

Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance and Operations, ir jāinstalē šādi komponenti.

- Microsoft Dynamics 365 for Project Service Automation versija 9.0.0.0 vai jaunāka
- Risinājums “No potenciālā klienta līdz skaidrai naudai” programmai Microsoft Dynamics 365 for Sales, versija 1.14.0.0 (v14) vai jaunāka
- Risinājums no programmas Project Service Automation uz programmu Finance and Operations programmas Microsoft Dynamics 365 for Project Service Automation versijai 1.0.0.0 vai jaunākai

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Risinājuma programmas Project Service Automation integrēšanai ar programmu Finance and Operations instalēšana jūsu Project Service Automation instancē

Lejupielādējiet Integrēšanas risinājumu programmas Project Service Automation integrēšanai programmā Finance and Operations no [Microsoft lejupielādes centra](https://www.microsoft.com/en-us/download/details.aspx?id=57016) un izpildiet šajā risinājumā ietvertos norādījumus.

