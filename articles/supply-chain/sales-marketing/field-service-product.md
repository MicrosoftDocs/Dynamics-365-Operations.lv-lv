---
title: Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service
description: Šajā rakstā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu preces no Dynamics 365 Supply Chain Management uz Dynamics 365 Field Service.
author: Henrikan
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 114550f01f3aed197480fb6830fe913dbfa7b570
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860556"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service

[!include[banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti, lai sinhronizētu preces no Dynamics 365 Supply Chain Management Dynamics 365 field Service.

Izmantotā veidne **Field Service preces (no Supply Chain Management uz Field Service)** balstās uz veidni **Preces (no Supply Chain Management uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai. Papildinformāciju skatiet sadaļā [Preces (no Supply Chain Management uz Sales) — tieši](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Šajā rakstā aprakstītas tikai atšķirības **starp Field Service precēm (piegādes ķēdes pārvaldība lauka pakalpojumam)** **un precēm (piegādes ķēdes pārvaldība pārdošanai) - tiešas** veidnes.

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

[![Veidņu kartēšana līdzeklī Datu integrācija.](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]