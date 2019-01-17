---
title: "Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk norādītā veidne un pamata uzdevumi tiek izmantoti, lai veiktu projektu sinhronizēšanu programmā Microsoft Dynamics 365 for Finance and Operations un Microsoft Dynamics 365 for Field Service.

**Veidnes nosaukums līdzeklī Datu integrācija:**
- Projekti (no programmas Finance and Operations programmā Field Service)

**Uzdevumu nosaukumi datu integrācijas projektā**
- Projekti

Lai varētu veikt projektu saraksta sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.
- Konti (no programmas Sales programmā Finance and Operations) 

## <a name="entity-set"></a>Elementu kopa
Field Service   Finance and Operations

| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekti                |

## <a name="entity-flow"></a>Elementu plūsma
Projekti tiek izveidoti programmā Finance and Operations. Projekti, kuriem vienumam **Projekta tips** atlasīts iestatījums Laiks un materiāli un vienumam **Projekta posms** atlasīts iestatījums Apstrāde, tiks sinhronizēti uz entītiju **Ārējais projekts** programmā Field Service, ieskaitot šādu informāciju: Projekta numurs, Projekta nosaukums, Projekta posms un Debitora konts. Entītijas **Ārējais projekts** saraksts tiek izmantots, lai savienotu pārī Field Service darba pasūtījumus ar Finance and Operations projektiem.
Risinājums Field Service CRM Entītija Ārējais projekts ir jauna entītija, kas iegūst visus projektus no programmas Operations.
Entītijai Darba pasūtījums ir pievienots lauks Ārējais projekts. Šis lauks ir uzmeklēšanas lauks, un, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Operations. Kad sistēmas statuss no Atvērts - Notiek izpilde(690,970,000) tiek mainīts uz augstāku statusu, lauks Ārējais projekts tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums
### <a name="in-finance-and-operations"></a>Programmā Finance and Operations
Iespējot izmaiņu izsekošanu datu elementu projektiem

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projekti (no programmas Finance and Operations programmā Field Service): Projekti

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProject1.png)](./media/FSProject1.png)

