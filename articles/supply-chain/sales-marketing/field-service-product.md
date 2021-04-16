---
title: Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 9cc8e93259119236093e02924d29df64dcc876bb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810898"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar programmu Dynamics 365 Field Service.

Izmantotā veidne **Field Service preces (no Supply Chain Management uz Field Service)** balstās uz veidni **Preces (no Supply Chain Management uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai. Papildinformāciju skatiet sadaļā [Preces (no Supply Chain Management uz Sales) — tieši](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Šajā tēmā ir aprakstītas tika atšķirības starp veidnēm **Field Service preces (no Supply Chain Management uz Field Service)** un **Preces (no Supply Chain Management uz Sales) — tieši**.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija**

- Field Service preces (no Supply Chain Management uz Field Service)

**Uzdevuma nosaukums datu integrācijas projektā**

- Preces — Preces

Izmantotā veidne **Field Service preces (no Supply Chain Management uz Field Service)** ietver vienu kartēšanu, kas nav iekļauta veidnē **Preces (no Supply Chain Management uz Sales) — tieši**. Šis kartējums nodrošina, ka obligātais Field Service iestatījums **Field Service preces tips** ir iestatīts pareizi.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Tiek izmantota šāda vērtību kartēšana.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Risinājumā Supply Chain Management datu elementa **Pārdodamas izlaistās preces** vērtību **Field Service preces tips** aprēķina šādi:

- **Krājumi:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Patiess
- **Krājumos neuzskaitītas preces:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Aplams
- **Pakalpojums:** Preces tips = Pakalpojums

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service preces (no Supply Chain Management uz Field Service): Preces — Preces

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]