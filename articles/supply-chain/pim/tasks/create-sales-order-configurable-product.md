---
title: Pārdošanas pasūtījuma izveide konfigurējamam produktam
description: Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 882198bf07233867b54579b986f93f5c1b46c1b6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564205"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="86a3f-103">Pārdošanas pasūtījuma izveide konfigurējamam produktam</span><span class="sxs-lookup"><span data-stu-id="86a3f-103">Create a sales order for a configurable product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86a3f-104">Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="86a3f-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="86a3f-105">Šajā piemērā tiek izmantots D0006 skaļruņu modelis demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="86a3f-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="86a3f-106">Parasti pārdošanas pasūtījuma apstrādātājs izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="86a3f-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="86a3f-107">Pārdošanas pasūtījuma izveidošana</span><span class="sxs-lookup"><span data-stu-id="86a3f-107">Create a sales order</span></span>
1. <span data-ttu-id="86a3f-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="86a3f-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="86a3f-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="86a3f-109">Click New.</span></span>
3. <span data-ttu-id="86a3f-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="86a3f-110">Click Sales order.</span></span>
4. <span data-ttu-id="86a3f-111">Laukā Debitora konts atlasiet US-001.</span><span class="sxs-lookup"><span data-stu-id="86a3f-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="86a3f-112">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="86a3f-112">Click OK.</span></span>
6. <span data-ttu-id="86a3f-113">Laukā Krājuma kods atlasiet D0006.</span><span class="sxs-lookup"><span data-stu-id="86a3f-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="86a3f-114">Lai veiktu šo uzdevumu, nepieciešams atlasīt konfigurējamu preci.</span><span class="sxs-lookup"><span data-stu-id="86a3f-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="86a3f-115">Noklikšķiniet uz Preces un piegādes.</span><span class="sxs-lookup"><span data-stu-id="86a3f-115">Click Product and supply.</span></span>
8. <span data-ttu-id="86a3f-116">Noklikšķiniet uz Konfigurēt rindu.</span><span class="sxs-lookup"><span data-stu-id="86a3f-116">Click Configure line.</span></span>
    * <span data-ttu-id="86a3f-117">Ievērojiet, ka cena ir mainījusies, atkarībā no konfigurācijas, kas tika atlasīta, un lauks Iekļaut kabeli tagad ir iestatīts uz Patiess.</span><span class="sxs-lookup"><span data-stu-id="86a3f-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="86a3f-118">Ievērojiet noklusējuma cenu un iestatījumus, kas ir atlasīti kabelim.</span><span class="sxs-lookup"><span data-stu-id="86a3f-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="86a3f-119">Noklikšķiniet uz Kravas veidne.</span><span class="sxs-lookup"><span data-stu-id="86a3f-119">Click Load template.</span></span>
    * <span data-ttu-id="86a3f-120">Šajā piemērā ir parādīts kā jūs varat pielietot veidni, lai atlasītu iepriekš definētu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="86a3f-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="86a3f-121">Ja izmantojat šo procedūru kā uzdevumu ceļvedi un vēlaties skatīt citas pieejamās atribūtu vērtības, noklikšķiniet uz pogas Atbloķēt.</span><span class="sxs-lookup"><span data-stu-id="86a3f-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="86a3f-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="86a3f-122">Click OK.</span></span>
11. <span data-ttu-id="86a3f-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="86a3f-123">Click OK.</span></span>
12. <span data-ttu-id="86a3f-124">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="86a3f-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="86a3f-125">Noklikšķiniet uz cilnes Prece.</span><span class="sxs-lookup"><span data-stu-id="86a3f-125">Click the Product tab.</span></span>
    * <span data-ttu-id="86a3f-126">Krājuma konfigurācija tiek parādīta preces dimensijās.</span><span class="sxs-lookup"><span data-stu-id="86a3f-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="86a3f-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="86a3f-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="86a3f-128">Atlasiet preces konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="86a3f-128">Select the product configuration</span></span>

