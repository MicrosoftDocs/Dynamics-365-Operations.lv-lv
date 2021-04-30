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
ms.openlocfilehash: 45a989604d829db715756b6cd206a5675a18acf2
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909995"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="4eb00-103">Programmā Supply Chain Management esošo produktu tieša sinhronizēšana ar produktiem programmā Field Service</span><span class="sxs-lookup"><span data-stu-id="4eb00-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4eb00-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar programmu Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="4eb00-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="4eb00-105">Izmantotā veidne **Field Service preces (no Supply Chain Management uz Field Service)** balstās uz veidni **Preces (no Supply Chain Management uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="4eb00-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="4eb00-106">Papildinformāciju skatiet sadaļā [Preces (no Supply Chain Management uz Sales) — tieši](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="4eb00-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="4eb00-107">Šajā tēmā ir aprakstītas tika atšķirības starp veidnēm **Field Service preces (no Supply Chain Management uz Field Service)** un **Preces (no Supply Chain Management uz Sales) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="4eb00-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="4eb00-108">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="4eb00-108">Templates and tasks</span></span>

<span data-ttu-id="4eb00-109">**Veidnes nosaukums līdzeklī Datu integrācija**</span><span class="sxs-lookup"><span data-stu-id="4eb00-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="4eb00-110">Field Service preces (no Supply Chain Management uz Field Service)</span><span class="sxs-lookup"><span data-stu-id="4eb00-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="4eb00-111">**Uzdevuma nosaukums datu integrācijas projektā**</span><span class="sxs-lookup"><span data-stu-id="4eb00-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="4eb00-112">Preces — Preces</span><span class="sxs-lookup"><span data-stu-id="4eb00-112">Products - Products</span></span>

<span data-ttu-id="4eb00-113">Izmantotā veidne **Field Service preces (no Supply Chain Management uz Field Service)** ietver vienu kartēšanu, kas nav iekļauta veidnē **Preces (no Supply Chain Management uz Sales) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="4eb00-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="4eb00-114">Šis kartējums nodrošina, ka obligātais Field Service iestatījums **Field Service preces tips** ir iestatīts pareizi.</span><span class="sxs-lookup"><span data-stu-id="4eb00-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="4eb00-115">Tiek izmantota šāda vērtību kartēšana.</span><span class="sxs-lookup"><span data-stu-id="4eb00-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="4eb00-116">Risinājumā Supply Chain Management datu elementa **Pārdodamas izlaistās preces** vērtību **Field Service preces tips** aprēķina šādi:</span><span class="sxs-lookup"><span data-stu-id="4eb00-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="4eb00-117">**Krājumi:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Patiess</span><span class="sxs-lookup"><span data-stu-id="4eb00-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="4eb00-118">**Krājumos neuzskaitītas preces:** Preces tips = Preču un krājumu modeļu grupa, Uzkrātā prece = Aplams</span><span class="sxs-lookup"><span data-stu-id="4eb00-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="4eb00-119">**Pakalpojums:** Preces tips = Pakalpojums</span><span class="sxs-lookup"><span data-stu-id="4eb00-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4eb00-120">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="4eb00-120">Template mapping in Data integration</span></span>

<span data-ttu-id="4eb00-121">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="4eb00-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="4eb00-122">Field Service preces (no Supply Chain Management uz Field Service): Preces — Preces</span><span class="sxs-lookup"><span data-stu-id="4eb00-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="4eb00-123">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="4eb00-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]