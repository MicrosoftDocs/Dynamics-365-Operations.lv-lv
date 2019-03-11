---
title: Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "329854"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmā Finance and Operations

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Microsoft Dynamics 365 for Finance and Operations.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Izmantotā veidne **Field Service preces (no Finance and Operations uz Field Service)** balstās uz veidni **Preces (no Finance and Operations uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai. Papildinformāciju skatiet sadaļā [Preces (no Finance and Operations uz Sales) — tieši](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Šajā tēmā ir aprakstītas tikai atšķirības starp veidnēm **Field Service preces (no Finance and Operations uz Field Service)** un **Field Service preces (no Finance and Operations uz Field Service) — tieši**.

Galvenā atšķirība ir tā, ka šajā veidnē ir ietverta programmā Field Service darba pasūtījumam piešķirtā projekta numura kartēšana, nodrošinot, ka pārdošanas pasūtījums, kas izveidots programmā Finance and Operations, ietver projekta numuru un ka saistītajam projektam var veikt rēķinu izrakstīšanu. Papildus tam veidne izmanto funkcionalitāti Izvērsts vaicājums un filtrēšana.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations)

**Uzdevuma nosaukums datu integrācijas projektā:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Entītijai Darba pasūtījums ir pievienots lauks **Ārējais projekts**. Šis lauks ir uzmeklēšanas lauks, un, marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums tiks savienots ar projektu programmā Finance and Operations. Kad vienumam **Sistēmas statuss** iestatījums Atvērts - Notiek izpilde(690,970,000) tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a>Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderHeader

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a>Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderHeaderProject

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a>Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderProduct

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a>Darba pasūtījumi ar projektu (no Field Service uz Finance and Operations): WorkOrderService

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP4.png)](./media/FSWOP4.png)
