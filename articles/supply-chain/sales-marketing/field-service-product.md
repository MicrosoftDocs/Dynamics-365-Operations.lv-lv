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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: lv-lv
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="82b2a-103">Programmā Finance and Operations ietverto preču sinhronizēšana ar precēm programmā Field Service</span><span class="sxs-lookup"><span data-stu-id="82b2a-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82b2a-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevumi, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar programmu Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="82b2a-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="82b2a-105">Izmantotā veidne **Field Service preces (no Fin and Ops uz Field Service)** balstās uz veidni **Preces (no Fin and Ops uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="82b2a-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="82b2a-106">Papildinformāciju skatiet sadaļā [Preces (no Fin and Ops uz Sales) — tieši](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="82b2a-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="82b2a-107">Šajā tēmā ir aprakstītas tika atšķirības starp veidnēm **Field Service preces (no Fin and Ops uz Field Service)** un **Preces (no Fin and Ops uz Sales) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="82b2a-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="82b2a-108">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="82b2a-108">Templates and tasks</span></span>

<span data-ttu-id="82b2a-109">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="82b2a-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="82b2a-110">Field Service preces (no Fin and Ops uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="82b2a-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="82b2a-111">**Uzdevuma nosaukums datu integrācijas projektā:**</span><span class="sxs-lookup"><span data-stu-id="82b2a-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="82b2a-112">Preces — Preces</span><span class="sxs-lookup"><span data-stu-id="82b2a-112">Products - Products</span></span>

<span data-ttu-id="82b2a-113">Veidnē **Field Service preces (no Fin and Ops uz Field Service)** ietilpst viens kartējums, kas nav ietverts veidnē **Preces (no Fin and Ops uz Sales) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="82b2a-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="82b2a-114">Šis kartējums nodrošina, ka obligātais Field Service iestatījums **Field Service preces tips** ir iestatīts pareizi.</span><span class="sxs-lookup"><span data-stu-id="82b2a-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="82b2a-115">Tiek izmantota šāda vērtību kartēšana.</span><span class="sxs-lookup"><span data-stu-id="82b2a-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="82b2a-116">Risinājumā Finance and Operations datu elementa **Pārdodamas izlaistās preces** vērtību **Field Service preces tips** aprēķina šādi:</span><span class="sxs-lookup"><span data-stu-id="82b2a-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="82b2a-117">**Krājumi:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Patiess</span><span class="sxs-lookup"><span data-stu-id="82b2a-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="82b2a-118">**Krājumos neuzskaitītas preces:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Aplams</span><span class="sxs-lookup"><span data-stu-id="82b2a-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="82b2a-119">**Pakalpojums:** Preces tips = Pakalpojums</span><span class="sxs-lookup"><span data-stu-id="82b2a-119">**Service:** Product type = Service</span></span>

