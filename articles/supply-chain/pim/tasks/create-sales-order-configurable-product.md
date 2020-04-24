---
title: Pārdošanas pasūtījuma izveide konfigurējamam produktam
description: Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e69fd2aa04a65d64db4d34f1839a01fb0f8e018
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213197"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="aee22-103">Pārdošanas pasūtījuma izveide konfigurējamam produktam</span><span class="sxs-lookup"><span data-stu-id="aee22-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aee22-104">Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="aee22-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="aee22-105">Šajā piemērā tiek izmantots D0006 skaļruņu modelis demonstrācijas datu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="aee22-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="aee22-106">Parasti pārdošanas pasūtījuma apstrādātājs izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="aee22-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="aee22-107">Pārdošanas pasūtījuma izveidošana</span><span class="sxs-lookup"><span data-stu-id="aee22-107">Create a sales order</span></span>
1. <span data-ttu-id="aee22-108">Noklikšķiniet uz Pārdošanas pasūtījuma apstrāde un pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="aee22-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="aee22-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="aee22-109">Click New.</span></span>
3. <span data-ttu-id="aee22-110">Noklikšķiniet uz Pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="aee22-110">Click Sales order.</span></span>
4. <span data-ttu-id="aee22-111">Laukā Debitora konts atlasiet US-001.</span><span class="sxs-lookup"><span data-stu-id="aee22-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="aee22-112">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aee22-112">Click OK.</span></span>
6. <span data-ttu-id="aee22-113">Laukā Krājuma kods atlasiet D0006.</span><span class="sxs-lookup"><span data-stu-id="aee22-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="aee22-114">Lai veiktu šo uzdevumu, nepieciešams atlasīt konfigurējamu preci.</span><span class="sxs-lookup"><span data-stu-id="aee22-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="aee22-115">Noklikšķiniet uz Preces un piegādes.</span><span class="sxs-lookup"><span data-stu-id="aee22-115">Click Product and supply.</span></span>
8. <span data-ttu-id="aee22-116">Noklikšķiniet uz Konfigurēt rindu.</span><span class="sxs-lookup"><span data-stu-id="aee22-116">Click Configure line.</span></span>
    * <span data-ttu-id="aee22-117">Ievērojiet, ka cena ir mainījusies, atkarībā no konfigurācijas, kas tika atlasīta, un lauks Iekļaut kabeli tagad ir iestatīts uz Patiess.</span><span class="sxs-lookup"><span data-stu-id="aee22-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="aee22-118">Ievērojiet noklusējuma cenu un iestatījumus, kas ir atlasīti kabelim.</span><span class="sxs-lookup"><span data-stu-id="aee22-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="aee22-119">Noklikšķiniet uz Kravas veidne.</span><span class="sxs-lookup"><span data-stu-id="aee22-119">Click Load template.</span></span>
    * <span data-ttu-id="aee22-120">Šajā piemērā ir parādīts kā jūs varat pielietot veidni, lai atlasītu iepriekš definētu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="aee22-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="aee22-121">Ja izmantojat šo procedūru kā uzdevumu ceļvedi un vēlaties skatīt citas pieejamās atribūtu vērtības, noklikšķiniet uz pogas Atbloķēt.</span><span class="sxs-lookup"><span data-stu-id="aee22-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="aee22-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aee22-122">Click OK.</span></span>
11. <span data-ttu-id="aee22-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="aee22-123">Click OK.</span></span>
12. <span data-ttu-id="aee22-124">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="aee22-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="aee22-125">Noklikšķiniet uz cilnes Prece.</span><span class="sxs-lookup"><span data-stu-id="aee22-125">Click the Product tab.</span></span>
    * <span data-ttu-id="aee22-126">Krājuma konfigurācija tiek parādīta preces dimensijās.</span><span class="sxs-lookup"><span data-stu-id="aee22-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="aee22-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="aee22-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="aee22-128">Atlasiet preces konfigurāciju</span><span class="sxs-lookup"><span data-stu-id="aee22-128">Select the product configuration</span></span>

