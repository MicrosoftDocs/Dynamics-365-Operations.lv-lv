---
title: "Programmā Finance and Operations ietverto preču sinhronizēšana ar precēm programmā Field Service"
description: "Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Programmā Finance and Operations ietverto preču sinhronizēšana ar precēm programmā Field Service

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.

Izmantotā veidne **Field Service preces (no Fin and Ops uz Field Service)** balstās uz veidni **Preces (no Fin and Ops uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai. Papildinformāciju skatiet sadaļā [Preces (no Fin and Ops uz Sales) — tieši](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

Šajā tēmā ir aprakstītas tika atšķirības starp veidnēm **Field Service preces (no Fin and Ops uz Field Service)** un **Preces (no Fin and Ops uz Sales) — tieši**.

## <a name="templates-and-tasks"></a>Veidnes un uzdevumi

**Veidnes nosaukums līdzeklī Datu integrācija:**

- Field Service preces (no Fin and Ops uz Field Service)

**Uzdevuma nosaukums datu integrācijas projektā:**

- Preces — Preces

Veidnē **Field Service preces (no Fin and Ops uz Field Service)** ietilpst viens kartējums, kas nav ietverts veidnē **Preces (no Fin and Ops uz Sales) — tieši**. Šis kartējums nodrošina, ka obligātais Field Service iestatījums **Field Service preces tips** ir iestatīts pareizi.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

Tiek izmantota šāda vērtību kartēšana.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

Risinājumā Finance and Operations datu elementa **Pārdodamas izlaistās preces** vērtību **Field Service preces tips** aprēķina šādi:

- **Krājumi:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Patiess
- **Krājumos neuzskaitītas preces:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Aplams
- **Pakalpojums:** Preces tips = Pakalpojums

## <a name="template-mapping-in-data-integration"></a>Veidnes kartējums līdzeklī Datu integrācija

Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service preces (no Fin and Ops uz Field Service): Preces — Preces

[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct.png)](./media/FSProduct.png)

