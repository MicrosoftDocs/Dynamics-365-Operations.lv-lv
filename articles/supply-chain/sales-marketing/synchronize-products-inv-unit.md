---
title: Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu uzskaites vienību programmā Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 080672b9a6acd9fd6137580b5b7e14d12cfccf19
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/14/2019
ms.locfileid: "842466"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu vienību programmā Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service.

[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Izmantotā veidne **Field Service preces ar krājumu uzskaites vienību (no Fin and Ops uz Field Service)** ir izveidota, pamatojoties uz veidni **Field Service preces (no Fin and Ops uz Field Service)**. Papildinformāciju skatiet rakstā [Field Service preces (no Finance and Operations uz Field Service)](field-service-product.md).

Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības. 
- **Field Service preces ar krājumu uzskaites vienību (no Fin and Ops uz Sales)**
- **Field Service preces (no Fin and Ops uz Field Service)** 

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Field Service preces ar krājumu uzskaites vienību (no Fin and Ops uz Sales)

**Uzdevuma nosaukums datu integrācijas projektā:**

- Preces

Veidnē **Field Service preces ar krājumu uzskaites vienību (no Fin and Ops uz Field Service)** ietilpst viens kartējums, kas nav ietverts veidnē **Field Service preces (no Fin and Ops uz Field Service)**. Šis kartējums nodrošina, ka ir iekļauta krājumu uzskaites vienība, kas nepieciešama krājumu līmeņa sinhronizēšanai.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="field-service-products-with-inventory-unit-fin-and-ops-to-field-service-products"></a>Field Service preces ar krājumu uzskaites vienību (no Fin and Ops uz Field Service): Preces

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct1.png)](./media/FSProduct1.png)
