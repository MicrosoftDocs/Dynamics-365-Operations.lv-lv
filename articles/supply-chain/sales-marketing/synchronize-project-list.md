---
title: Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/14/2019
ms.locfileid: "842608"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Programmā Finance and Operations ietverto projektu saraksta sinhronizēšana ar programmu Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi
Tālāk minētā veidne un pamata uzdevumi tiek izmantoti, lai veiktu risinājumā Microsoft Dynamics 365 for Finance and Operations ietverto projektu sinhronizēšanu ar Microsoft Dynamics 365 for Field Service.

**Veidne līdzeklī Datu integrācija**
- Projekti (no Fin and Ops uz Field Service)

**Uzdevums datu integrācijas projektā**
- Projekti

Lai varētu veikt projektu saraksta sinhronizāciju, ir nepieciešami tālāk norādītie sinhronizācijas uzdevumi.
- Konti (no Sales uz Fin and Ops) 

## <a name="entity-set"></a>Elementu kopa
| Field Service           | Finance and Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projekti                |

## <a name="entity-flow"></a>Elementu plūsma
Projekti tiek izveidoti programmā Finance and Operations. Projekti, kuriem vienumam **Projekta tips** atlasīts iestatījums **Laiks un materiāli** un vienumam **Projekta posms** atlasīts iestatījums **Apstrāde**, tiks sinhronizēti uz entītiju **Ārējais projekts** programmā Field Service, ieskaitot šādu informāciju: Projekta numurs, Projekta nosaukums, Projekta posms un Debitora konts. Entītijas **Ārējais projekts** saraksts tiek izmantots, lai savienotu pārī Field Service darba pasūtījumus ar Finance and Operations projektiem.

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Entītija **Ārējais projekts** iegūst visus projektus no Finance and Operations. Entītijai **Darba pasūtījums** ir pievienots lauks **Ārējais projekts**. Tas ir uzmeklēšanas lauks, tādēļ, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Finance and Operations. Pēc tam, kad vienumam **Sistēmas statuss** iestatījums **Atvērts - Notiek izpilde(690,970,000)** tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un vairs nebūs iespējams pievienot, noņemt vai mainīt vērtību.

## <a name="prerequisites-and-mapping-setup"></a>Priekšnosacījumi un kartējuma iestatījums
### <a name="finance-and-operations"></a>Finance and Operations
Iespējojiet izmaiņu izsekošanu datu elementu projektiem.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Projekti (no Fin and Ops uz Field Service): Projekti

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProject1.png)](./media/FSProject1.png)
