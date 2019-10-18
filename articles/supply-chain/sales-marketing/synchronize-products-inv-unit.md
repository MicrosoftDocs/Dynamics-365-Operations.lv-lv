---
title: Sinhronizēt preces ar Krājumu uzskaites vienību no Supply Chain Management uz Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
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
ms.openlocfilehash: 8b65e9640106c5d351270074e39c121e70917228
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251228"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Sinhronizēt preces ar Krājumu uzskaites vienību no Supply Chain Management uz Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Dynamics 365 Field Service.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Izmantotā veidne **Field Service preces ar krājumu uzskaites vienību (Supply Chain Management uz Field Service)** ir izveidota, pamatojoties uz veidni **Field Service preces (no Supply Chain Management uz Field Service)**. Papildinformāciju skatiet rakstā [Field Service preces (no Supply Chain Management uz Field Service)](field-service-product.md).

Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības. 
- **Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales)**
- **Field Service preces (no Supply Chain Management uz Field Service)** 

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales)

**Uzdevuma nosaukums datu integrācijas projektā:**

- Preces

Veidne **Field Service preces ar krājumu uzskaites vienību (Supply Chain Management uz Field Service)** ietver vienu kartēšanu, kas nav iekļauta veidnē **Field Service preces (no Supply Chain Management uz Field Service)**. Šis kartējums nodrošina, ka ir iekļauta krājumu uzskaites vienība, kas nepieciešama krājumu līmeņa sinhronizēšanai.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service preces ar krājumu uzskaites vienību (no Supply Chain Management uz Field Service): Preces

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct1.png)](./media/FSProduct1.png)
