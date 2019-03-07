---
title: Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu uzskaites vienību programmā Field Service
description: Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "359248"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a><span data-ttu-id="ab697-103">Programmā Finance and Operations ietverto preču sinhronizēšana ar krājumu vienību programmā Field Service</span><span class="sxs-lookup"><span data-stu-id="ab697-103">Synchronize products with inventory unit from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ab697-104">Šajā tēmā ir aprakstītas veidnes un pamata uzdevums, kas tiek izmantoti programmā Microsoft Dynamics 365 for Finance and Operations ietverto preču sinhronizēšanai ar krājumu uzskaites vienību programmā Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="ab697-104">This topic discusses the templates and underlying task that are used to synchronize products with inventory unit from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ab697-105">[![Biznesa procesu sinhronizēšana risinājumos Finance and Operations un Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span><span class="sxs-lookup"><span data-stu-id="ab697-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)</span></span>

<span data-ttu-id="ab697-106">Izmantotā veidne **Field Service preces (no Finance and Operations uz Field Service)** balstās uz veidni **Preces (no Finance and Operations uz Sales) — tieši** no risinājuma No potenciālā klienta līdz skaidrai naudai.</span><span class="sxs-lookup"><span data-stu-id="ab697-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="ab697-107">Papildinformāciju skatiet sadaļā [Preces (no Finance and Operations uz Sales) — tieši](products-template-mapping-direct.md).</span><span class="sxs-lookup"><span data-stu-id="ab697-107">For more information, see [Products (Finance and Operations to Sales) – Direct](products-template-mapping-direct.md).</span></span>

<span data-ttu-id="ab697-108">Šajā tēmā ir aprakstītas tikai atšķirības starp veidnēm **Field Service preces (no Finance and Operations uz Field Service)** un **Field Service preces (no Finance and Operations uz Field Service) — tieši**.</span><span class="sxs-lookup"><span data-stu-id="ab697-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ab697-109">Veidnes un uzdevumi</span><span class="sxs-lookup"><span data-stu-id="ab697-109">Templates and tasks</span></span>

<span data-ttu-id="ab697-110">**Veidnes nosaukums līdzeklī Datu integrācija:**</span><span class="sxs-lookup"><span data-stu-id="ab697-110">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ab697-111">Field Service preces ar krājumu uzskaites vienību (no programmas Finance and Operations programmā Sales)</span><span class="sxs-lookup"><span data-stu-id="ab697-111">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span>

<span data-ttu-id="ab697-112">**Uzdevuma nosaukums datu integrācijas projektā:**</span><span class="sxs-lookup"><span data-stu-id="ab697-112">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="ab697-113">Preces</span><span class="sxs-lookup"><span data-stu-id="ab697-113">Products</span></span>

<span data-ttu-id="ab697-114">Veidnē **Field Service preces ar krājumu uzskaites vienību (no Finance and Operations uz Field Service)** ietilpst viens kartējums, kas nav ietverts veidnē **Preces (no Finance and Operations uz Field Service)**.</span><span class="sxs-lookup"><span data-stu-id="ab697-114">The **Field Service Products with Inventory unit (Finance and Operations to Field Service)** template includes one mapping that isn't included in the **Field Service Products (Finance and Operations to Field Service)** template.</span></span> <span data-ttu-id="ab697-115">Šis kartējums nodrošina, ka ir iekļauta krājumu uzskaites vienība, kas nepieciešama krājumu līmeņa sinhronizēšanai.</span><span class="sxs-lookup"><span data-stu-id="ab697-115">This mapping ensures that the Inventory unit needed for inventory level synchronization is included.</span></span>

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ab697-116">Veidnes kartējums līdzeklī Datu integrācija</span><span class="sxs-lookup"><span data-stu-id="ab697-116">Template mapping in Data integration</span></span>

<span data-ttu-id="ab697-117">Tālāk esošajos attēlos ir redzams veidnes kartējums līdzeklī Datu integrācija.</span><span class="sxs-lookup"><span data-stu-id="ab697-117">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a><span data-ttu-id="ab697-118">Field Service preces ar krājumu uzskaites vienību (no Finance and Operations uz Field Service): Preces</span><span class="sxs-lookup"><span data-stu-id="ab697-118">Field Service Products with Inventory unit (Finance and Operations to Field Service): Products</span></span>

<span data-ttu-id="ab697-119">[![Veidņu kartēšana līdzeklī Datu integrācija](./media/FSProduct1.png)](./media/FSProduct1.png)</span><span class="sxs-lookup"><span data-stu-id="ab697-119">[![Template mapping in Data integration](./media/FSProduct1.png)](./media/FSProduct1.png)</span></span>
