---
title: Pārdošanas pasūtījuma izveide konfigurējamam produktam
description: Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8607de5705354aa58c985fb536f3e1d52acd1f37
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921293"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="ee9d3-103">Pārdošanas pasūtījuma izveide konfigurējamam produktam</span><span class="sxs-lookup"><span data-stu-id="ee9d3-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee9d3-104">Šajā procedūrā ir parādīts, kā pielietot konfigurācijas veidni preces pārdošanas pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="ee9d3-105">Šajā piemērā tiek izmantots D0006 skaļruņu modelis paraugdatu uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="ee9d3-106">Parasti pārdošanas pasūtījuma apstrādātājs izmanto šo procedūru.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-106">Typically, a sales order processor uses this procedure.</span></span>

## <a name="create-a-sales-order"></a><span data-ttu-id="ee9d3-107">Izveidot pārdošanas pasūtījumu</span><span class="sxs-lookup"><span data-stu-id="ee9d3-107">Create a sales order</span></span>

1. <span data-ttu-id="ee9d3-108">Dodieties uz **Pārdošana un mārketings \> Darbvietas \> Pārdošanas pasūtījumu apstrāde un pieprasījums**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-108">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="ee9d3-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-109">Select **New**.</span></span>
1. <span data-ttu-id="ee9d3-110">Atlasiet vienumu **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-110">Select **Sales order**.</span></span>
1. <span data-ttu-id="ee9d3-111">Laukā **Debitora konts** atlasiet *US-001*.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-111">In the **Customer account** field, select *US-001*.</span></span> 
1. <span data-ttu-id="ee9d3-112">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-112">Select **OK**.</span></span>
1. <span data-ttu-id="ee9d3-113">Laukā **Krājuma numurs** atlasiet *D0006*.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-113">In the **Item number** field, select *D0006*.</span></span>
    * <span data-ttu-id="ee9d3-114">Lai veiktu šo uzdevumu, nepieciešams atlasīt konfigurējamu preci.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-114">For this task, you must select a configurable product.</span></span>  
1. <span data-ttu-id="ee9d3-115">Atlasiet **Prece un piegāde**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-115">Select **Product and supply**.</span></span>
1. <span data-ttu-id="ee9d3-116">Atlasiet **Konfigurēt rindu**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-116">Select **Configure line**.</span></span>
    * <span data-ttu-id="ee9d3-117">Ievērojiet, ka cena ir mainījusies, atkarībā no konfigurācijas, kas tika atlasīta, un lauks **Iekļaut kabeli** tagad ir iestatīts uz *Patiess*.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-117">Note that the price has changed, based on the configuration that was selected, and that the **Include cable** field is now set to *True*.</span></span>  
    * <span data-ttu-id="ee9d3-118">Ievērojiet noklusējuma cenu un iestatījumus, kas ir atlasīti kabelim.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-118">Note the default price and the settings that are selected for the cable.</span></span>  
1. <span data-ttu-id="ee9d3-119">Atlasiet **Ielādēt veidni**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-119">Select **Load template**.</span></span>
    * <span data-ttu-id="ee9d3-120">Šajā piemērā ir parādīts kā jūs varat pielietot veidni, lai atlasītu iepriekš definētu konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="ee9d3-121">Ja izmantojat šo procedūru kā uzdevumu ceļvedi un vēlaties skatīt citas pieejamās atribūtu vērtības, atlasiet pogas **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must select the **Unlock** button.</span></span>  
1. <span data-ttu-id="ee9d3-122">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-122">Select **OK**.</span></span>
1. <span data-ttu-id="ee9d3-123">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-123">Select **OK**.</span></span>
1. <span data-ttu-id="ee9d3-124">Izvērsiet sadaļu **Detalizēta informācija par rindu**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-124">Expand the **Line details** section.</span></span>
1. <span data-ttu-id="ee9d3-125">Atlasīt cilni **Prece**.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-125">Select the **Product** tab.</span></span>
    * <span data-ttu-id="ee9d3-126">Krājuma konfigurācija tiek parādīta preces dimensijās.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-126">The configuration of the item is now listed under the product dimensions.</span></span>  
1. <span data-ttu-id="ee9d3-127">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="ee9d3-127">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]