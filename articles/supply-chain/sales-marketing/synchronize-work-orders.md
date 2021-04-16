---
title: Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmatūrā Supply Chain Management
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 03/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d733bf3256fa1f6c572bd0aa35c228490d409bbc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836498"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar projektu programmatūrā Supply Chain Management

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Field Service ietverto darba pasūtījumu sinhronizēšanai ar projekta numuru programmā Dynamics 365 Supply Chain Management.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

Izmantotā veidne **Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management)** ir izveidota, pamatojoties uz veidni **Darba pasūtījumu (no Field Service uz Supply Chain Management)**. Papildinformāciju skatiet rakstā [Programmā Field Service ietverto darba pasūtījumu sinhronizēšana ar pārdošanas pasūtījumiem programmatūrā Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības.
- **Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management)**
- **Darba pasūtījumi (no Field Service uz Supply Chain Management)**

Galvenā atšķirība ir tā, ka šajā veidnē ir ietverta programmā Field Service darba pasūtījumam piešķirtā projekta numura kartēšana, nodrošinot, ka pārdošanas pasūtījums, kas izveidots programmatūrā Supply Chain Management, ietver projekta numuru un ka saistītajam projektam var veikt rēķinu izrakstīšanu. Papildus tam veidne izmanto funkcionalitāti Izvērsts vaicājums un filtrēšana.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management)

**Uzdevuma nosaukums datu integrācijas projektā:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Risinājums Field Service CRM
Entītijai Darba pasūtījums ir pievienots lauks **Ārējais projekts**. Šis lauks ir uzmeklēšana, un marķējot darba pasūtījumu ar projektu, pārdošanas pasūtījums pēc tam tiks savienots ar projektu programmatūrā Supply Chain Management. Kad vienumam **Sistēmas statuss** iestatījums Atvērts - Notiek izpilde(690 970 000) tiek mainīts uz augstāku statusu, lauks **Ārējais projekts** tiks slēgts un nebūs iespējams pievienot, noņemt vai mainīt vērtību.

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderHeader

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderHeaderProject

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderProduct

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Darba pasūtījumi ar projektu (no Field Service uz Supply Chain Management): WorkOrderService

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]