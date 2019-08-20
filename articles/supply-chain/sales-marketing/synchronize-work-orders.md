---
title: Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 77358513ffdf791ab10d6efe1b84f598ffb5ec26
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843413"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Izmantotā veidne **Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops)** ir izveidota, pamatojoties uz veidni **Darba pasūtījumu (no Field Service uz Fin and Ops)**. Papildinformāciju skatiet rakstā [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmā Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības.
- **Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops)**
- **Darba pasūtījumi (no Field Service uz Fin and Ops)**

Galvenā atšķirība ir tā, ka šajā veidnē ir ietverta programmā Field Service darba pasūtījumam piešķirtā projekta numura kartēšana, nodrošinot, ka pārdošanas pasūtījums, kas izveidots programmā Finance and Operations, ietver projekta numuru un ka saistītajam projektam var veikt rēķinu izrakstīšanu. Papildus tam veidne izmanto funkcionalitāti Izvērsts vaicājums un filtrēšana.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops)

**Uzdevuma nosaukums datu integrācijas projektā:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Entītijai Darba pasūtījums ir pievienots lauks **Ārējais projekts**. Šis lauks ir uzmeklēšanas lauks, un, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Finance and Operations. Kad vienumam **Sistēmas statuss** iestatījums Atvērts - Notiek izpilde(690,970,000) tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderHeader

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderHeaderProject

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderProduct

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Darba pasūtījumi ar projektu (no Field Service uz Fin and Ops): WorkOrderService

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP4.png)](./media/FSWOP4.png)
