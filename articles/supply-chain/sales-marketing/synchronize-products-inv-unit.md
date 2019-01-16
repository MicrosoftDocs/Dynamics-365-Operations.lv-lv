---
title: "Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu uzskaites vienību programmā Field Service"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: lv-lv
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu uzskaites vienību programmā Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Izmantotā veidne **Field Service preces (no Finance and Operations uz Field Service)** balstās uz veidni **Preces (no Finance and Operations uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai. Papildinformāciju skatiet sadaļā [Preces (no Finance and Operations uz Sales) — tieši](products-template-mapping-direct.md).

Šajā tēmā ir aprakstītas tikai atšķirības starp veidnēm **Field Service preces (no Finance and Operations uz Field Service)** un **Field Service preces (no Finance and Operations uz Field Service) — tieši**.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Field Service preces ar krājumu uzskaites vienību (no programmas Finance and Operations programmā Sales)

**Uzdevuma nosaukums datu integrācijas projektā:**

- Preces

Veidnē **Field Service preces ar krājumu uzskaites vienību (no Finance and Operations uz Field Service)** ietilpst viens kartējums, kas nav ietverts veidnē **Preces (no Finance and Operations uz Field Service)**. Šis kartējums nodrošina, ka ir iekļauta krājumu uzskaites vienība, kas nepieciešama krājumu līmeņa sinhronizēšanai.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Field Service preces ar krājumu uzskaites vienību (no Finance and Operations uz Field Service): Preces

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct1.png)](./media/FSProduct1.png)

