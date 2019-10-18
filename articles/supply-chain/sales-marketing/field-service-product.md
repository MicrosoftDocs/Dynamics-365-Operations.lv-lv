---
title: Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar programmu Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: f5f6d41f3e65a3cf5b8c7c96f54b1c8c6cdfaefb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249777"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="460a9-103">Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service</span><span class="sxs-lookup"><span data-stu-id="460a9-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="460a9-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar programmu Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="460a9-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="460a9-105">Izmantotā veidne **Field Service preces (no Supply Chain Management uz Field Service)** balstās uz veidni **Preces (no Supply Chain Management uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="460a9-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="460a9-106">Papildinformāciju skatiet sadaļā [Preces (no Supply Chain Management uz Sales) — tieši](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="460a9-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="460a9-107">Šajā tēmā ir aprakstītas tika atšķirības starp veidnēm **Field Service preces (no Supply Chain Management uz Field Service)** un **Preces (no Supply Chain Management uz Sales) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="460a9-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="460a9-108">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="460a9-108">Templates and tasks</span></span>

<span data-ttu-id="460a9-109">**Veidnes nosaukums līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="460a9-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="460a9-110">Field Service preces (no Supply Chain Management uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="460a9-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="460a9-111">**Uzdevuma nosaukums datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="460a9-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="460a9-112">Preces — Preces</span><span class="sxs-lookup"><span data-stu-id="460a9-112">Products - Products</span></span>

<span data-ttu-id="460a9-113">Izmantotā veidne **Field Service preces (no Supply Chain Management uz Field Service)** ietver vienu kartēšanu, kas nav iekļauta veidnē **Preces (no Supply Chain Management uz Sales) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="460a9-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="460a9-114">Šis kartējums nodrošina, ka obligātais Field Service iestatījums **Field Service preces tips** ir iestatīts pareizi.</span><span class="sxs-lookup"><span data-stu-id="460a9-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="460a9-115">Tiek izmantota šāda vērtību kartēšana.</span><span class="sxs-lookup"><span data-stu-id="460a9-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="460a9-116">Risinājumā Supply Chain Management datu elementa **Pārdodamas izlaistās preces** vērtību **Field Service preces tips** aprēķina šādi:</span><span class="sxs-lookup"><span data-stu-id="460a9-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="460a9-117">**Krājumi:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Patiess</span><span class="sxs-lookup"><span data-stu-id="460a9-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="460a9-118">**Krājumos neuzskaitītas preces:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Aplams</span><span class="sxs-lookup"><span data-stu-id="460a9-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="460a9-119">**Pakalpojums:** Preces tips = Pakalpojums</span><span class="sxs-lookup"><span data-stu-id="460a9-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="460a9-120">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="460a9-120">Template mapping in Data integration</span></span>

<span data-ttu-id="460a9-121">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="460a9-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="460a9-122">Field Service preces (no Supply Chain Management uz Field Service): Preces — Preces</span><span class="sxs-lookup"><span data-stu-id="460a9-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="460a9-123">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="460a9-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
