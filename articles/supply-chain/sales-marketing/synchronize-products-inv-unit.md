---
title: Sinhronizēt preces ar Krājumu uzskaites vienību no Supply Chain Management uz Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c5be622d6f62d54bcec053b93700ce0c234b8308
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010901"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a><span data-ttu-id="03998-103">Sinhronizēt preces ar Krājumu uzskaites vienību no Supply Chain Management uz Field Service</span><span class="sxs-lookup"><span data-stu-id="03998-103">Synchronize products with inventory unit from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="03998-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Dynamics 365 Supply Chain Management ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="03998-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="03998-105">[![Biznesa procesu sinhronizācija programmās Supply Chain Management un Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="03998-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="03998-106">Izmantotā veidne **Field Service preces ar krājumu uzskaites vienību (Supply Chain Management uz Field Service)** ir izveidota, pamatojoties uz veidni **Field Service preces (no Supply Chain Management uz Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="03998-106">The used **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template is based on the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="03998-107">Papildinformāciju skatiet rakstā [Programmā Supply Chain Management ietverto preču sinhronizēšana ar precēm programmatūrā Field Service](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="03998-107">For more information, see [Synchronize products in Supply Chain Management to products in Field Service](field-service-product.md).</span></span>

<span data-ttu-id="03998-108">Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības.</span><span class="sxs-lookup"><span data-stu-id="03998-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="03998-109">**Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales)**</span><span class="sxs-lookup"><span data-stu-id="03998-109">**Field Service Products with Inventory unit (Supply Chain Management to Sales)**</span></span>
- <span data-ttu-id="03998-110">**Field Service preces (no Supply Chain Management uz Field Service)**</span><span class="sxs-lookup"><span data-stu-id="03998-110">**Field Service Products (Supply Chain Management to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="03998-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="03998-111">Templates and tasks</span></span>

<span data-ttu-id="03998-112">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="03998-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="03998-113">Field Service preces ar Krājumu uzskaites vienību (no Supply Chain Management uz Sales)</span><span class="sxs-lookup"><span data-stu-id="03998-113">Field Service Products with Inventory unit (Supply Chain Management to Sales)</span></span>

<span data-ttu-id="03998-114">**Uzdevuma nosaukums datu integrācijas projektā:**</span><span class="sxs-lookup"><span data-stu-id="03998-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="03998-115">Preces</span><span class="sxs-lookup"><span data-stu-id="03998-115">Products</span></span>

<span data-ttu-id="03998-116">Veidne **Field Service preces ar krājumu uzskaites vienību(no Supply Chain Management uz Field Service)** ietver vienu kartējumu, kas nav iekļauts veidnē **Field Service preces (no Supply Chain Management uz Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="03998-116">The **Field Service Products with Inventory unit (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Supply Chain Management to Field Service)** template.</span></span> <span data-ttu-id="03998-117">Šis kartējums nodrošina, ka ir iekļauta krājumu uzskaites vienība, kas nepieciešama krājumu līmeņa sinhronizēšanai.</span><span class="sxs-lookup"><span data-stu-id="03998-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="03998-118">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="03998-118">Template mapping in Data integration</span></span>

<span data-ttu-id="03998-119">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="03998-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a><span data-ttu-id="03998-120">Field Service preces ar krājumu uzskaites vienību (no Supply Chain Management uz Field Service): Preces</span><span class="sxs-lookup"><span data-stu-id="03998-120">Field Service Products with Inventory unit (Supply Chain Management to Field Service): Products</span></span>

<span data-ttu-id="03998-121">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="03998-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
