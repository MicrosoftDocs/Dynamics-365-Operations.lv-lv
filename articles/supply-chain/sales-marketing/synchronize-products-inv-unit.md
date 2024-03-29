---
title: Sinhronizēt preces ar Krājumu uzskaites vienību no Supply Chain Management uz Field Service
description: Šajā rakstā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu preces ar krājumu vienību no uz Dynamics 365 Supply Chain Management Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
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
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887259"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Sinhronizēt preces ar Krājumu uzskaites vienību no Supply Chain Management uz Field Service

[!include[banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu preces ar krājumu vienību no uz Dynamics 365 Supply Chain Management Dynamics 365 Field Service.

[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

Izmantotā veidne **Field Service preces ar krājumu uzskaites vienību (Supply Chain Management uz Field Service)** ir izveidota, pamatojoties uz veidni **Field Service preces (no Supply Chain Management uz Field Service)**. Papildinformāciju skatiet rakstā [Programmā Supply Chain Management ietverto preču sinhronizēšana ar precēm programmatūrā Field Service](field-service-product.md).

Šajā rakstā ir aprakstītas tikai atšķirības starp divām veidnēm: 
- **Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales)**
- **Field Service preces (no Supply Chain Management uz Field Service)** 

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales)

**Uzdevuma nosaukums datu integrācijas projektā:**

- Preces

Veidne **Field Service preces ar krājumu uzskaites vienību(no Supply Chain Management uz Field Service)** ietver vienu kartējumu, kas nav iekļauts veidnē **Field Service preces (no Supply Chain Management uz Field Service)**. Šis kartējums nodrošina, ka ir iekļauta krājumu uzskaites vienība, kas nepieciešama krājumu līmeņa sinhronizēšanai.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service preces ar krājumu uzskaites vienību (no Supply Chain Management uz Field Service): Preces

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]