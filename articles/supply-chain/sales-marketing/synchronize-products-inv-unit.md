---
title: Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu uzskaites vienību programmā Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2019
ms.locfileid: "836306"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="42a80-103">Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu vienību programmā Field Service</span><span class="sxs-lookup"><span data-stu-id="42a80-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="42a80-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="42a80-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="42a80-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="42a80-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="42a80-106">Izmantotā veidne **Field Service preces ar krājumu uzskaites vienību (no Finance and Operations uz Field Service)** ir izveidota, pamatojoties uz veidni **Preces (no Finance and Operations uz Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="42a80-106">The used **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template is based on the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="42a80-107">Papildinformāciju skatiet rakstā [Field Service preces (no Finance and Operations uz Field Service)](field-service-product.md).</span><span class="sxs-lookup"><span data-stu-id="42a80-107">For more information, see [Field Service Products (Finance and Operations to Field Service)](field-service-product.md).</span></span>

<span data-ttu-id="42a80-108">Šajā tēmā ir aprakstītas tikai šo divu veidņu atšķirības.</span><span class="sxs-lookup"><span data-stu-id="42a80-108">This topic only describes the differences between the two templates:</span></span> 
- <span data-ttu-id="42a80-109">**Field Service preces ar krājumu uzskaites vienību (no programmas Finance and Operations programmā Sales)**</span><span class="sxs-lookup"><span data-stu-id="42a80-109">**Field Service Products with Inventory unit (Finance and Operations to Sales)**</span></span>
- <span data-ttu-id="42a80-110">**Field Service preces (no Finance and Operations uz Field Service)**</span><span class="sxs-lookup"><span data-stu-id="42a80-110">**Field Service Products (Finance and Operations to Field Service)**</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="42a80-111">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="42a80-111">Templates and tasks</span></span>

<span data-ttu-id="42a80-112">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="42a80-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="42a80-113">Field Service preces ar krājumu uzskaites vienību (no programmas Finance and Operations programmā Sales)</span><span class="sxs-lookup"><span data-stu-id="42a80-113">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="42a80-114">**Uzdevuma nosaukums datu integrācijas projektā:**</span><span class="sxs-lookup"><span data-stu-id="42a80-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="42a80-115">Preces</span><span class="sxs-lookup"><span data-stu-id="42a80-115">Products</span></span>

<span data-ttu-id="42a80-116">Veidnē **Field Service preces ar krājumu uzskaites vienību (no Finance and Operations uz Field Service)** ietilpst viens kartējums, kas nav ietverts veidnē **Preces (no Finance and Operations uz Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="42a80-116">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="42a80-117">Šis kartējums nodrošina, ka ir iekļauta krājumu uzskaites vienība, kas nepieciešama krājumu līmeņa sinhronizēšanai.</span><span class="sxs-lookup"><span data-stu-id="42a80-117">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="42a80-118">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="42a80-118">Template mapping in Data integration</span></span>

<span data-ttu-id="42a80-119">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="42a80-119">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="42a80-120">Field Service preces ar krājumu uzskaites vienību (no Finance and Operations uz Field Service): Preces</span><span class="sxs-lookup"><span data-stu-id="42a80-120">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="42a80-121">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="42a80-121">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
