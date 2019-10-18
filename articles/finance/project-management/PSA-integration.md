---
title: Project Service Automation pārskats
description: Šajā tēmā ir sniegta informācija par integrācijas risinājumu no Dynamics 365 Project Service Automation uz Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250557"
---
# <a name="project-service-automation-overview"></a>Project Service Automation pārskats

[!include[banner](../includes/banner.md)]

Risinājums Project Service Automation integrēšanai programmā Finance, izmanto līdzekli Datu integrācija, lai sinhronizētu datus Dynamics 365 Finance un Dynamics 365 Project Service Automation instancēs, izmantojot pakalpojumu Common Data Service. Integrācijas veidnes, kas ir pieejamas līdzeklī Datu integrācija, iespējo projektu, projekta līgumu, projekta līgumu rindu, projekta līgumu rindu atskaites punktu, projekta uzdevumu, izdevumu transakciju kategoriju, stundu novērtējumu un izdevumu novērtējumu datu plūsmu no programmas Project Service Automation uz programmu Finance.

> [!NOTE]
> - Ja lietojat versiju 7.3.0, ir jāinstalē KB 4074835. Pēc tam jūs varēsit integrēt fiksētas cenas projektus.
> - Ja izmantojat versiju 7.3.0 un pārceļat maksu transakcijas no programmas Project Service Automation, ir jāinstalē KB 4345320, lai šīs maksas ietvertu projekta rēķinā.
> - Ja lietojat versiju 8.0, varat izmantot projekta uzdevumu integrāciju, izdevumu transakciju kategorijas, stundu novērtējumus, izdevumu novērtējumus un funkcionalitātes bloķēšanu.
> - Ja lietojat versiju 8.0.1 vai jaunāku versiju, varat sinhronizēt faktiskās vērtības.

Pirms programmas Project Service Automation Finance integrēšanas ir jākonfigurē Project Service Automation integrācijas parametri. Papildinformāciju skatiet tēmā [Project Service Automation integrācijas parametri](PSA-parameters.md).

Šis integrācijas risinājums nodrošina tiešu sinhronizēšanu tālāk norādītajos scenārijos.

- Uzturiet projekta līgumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.
- Izveidojiet projektus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.
- Uzturiet projekta līgumu rindas programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.
- Uzturiet projekta līgumu rindu atskaites punktus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.
- Uzturiet projekta uzdevumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.
- Uzturiet izdevumu transakciju kategorijas programmā Finance un sinhronizējiet tās tieši no programmas Finance ar programmu Project Service Automation.
- Izveidojiet projekta stundu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.
- Izveidojiet projekta izdevumu novērtējumus programmā Project Service Automation un sinhronizējiet tos tieši no programmas Project Service Automation ar programmu Finance.
- Izveidojiet projekta laiku, izdevumus un faktiskās vērtības programmā Project Service Automation un izveidojiet projekta transakcijas programmas Project Service Automation integrācijas žurnālā, lai tos varētu grāmatot programmā Finance.

## <a name="data-synchronization"></a>Datu sinhronizācija

Tālāk esošajā attēlā ir redzams, kā notiek datu sinhronizēšana integrācijas procesa ietvaros programmās Project Service Automation un Finance.

> [!NOTE]
> Šobrīd nav pieejamas visas veidnes. Veidnes tiks izlaistas pēc to pabeigšanas.

[![Project Service Automation integrācija ar programmu Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Sistēmas prasības programmai Finance

Lai izmantotu risinājumu Project Service Automation integrēšanai programmā Finance, ir jāinstalē Enterprise Edition versija 7.3 ar 12. Platformas atjauninājumu vai jaunāka versija.

## <a name="system-requirements-for-project-service-automation"></a>Sistēmas prasības programmai Project Service Automation

Lai izmantotu risinājumu programmas Project Service Automation integrēšanai ar programmu Finance, ir jāinstalē šādi komponenti.

- Dynamics 365 Project Service Automation versija 9.0.0.0 vai jaunāka versija
- Risinājums No potenciālā klienta līdz skaidrai naudai programmai Dynamics 365 Sales, versija 1.14.0.0 (v14) vai jaunāka
- Risinājuma Project Service Automation integrēšanai programmā Finance programmai Dynamics 365 Project Service Automation versija 1.0.0.0 vai jaunāka versija

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Risinājuma programmas Project Service Automation integrēšanai ar programmu Finance instalēšana jūsu Project Service Automation instancē

Lejupielādējiet Integrēšanas risinājumu programmas Project Service Automation integrēšanai programmā Finance no [Microsoft lejupielādes centra](https://www.microsoft.com/download/details.aspx?id=57016) un izpildiet šajā risinājumā ietvertos norādījumus.
