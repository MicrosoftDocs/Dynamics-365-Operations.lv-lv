---
title: Krājumu vai izejmateriālu izsekošana
description: Šajā procedūra parādīts, kā lietot krājumu izsekošanu, lai identificētu, kur krājumi vai izejmateriāli ir izmantoti vai tiek izmantoti.
author: pjacobse
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c39d34773a2b36cbf9477e4bdda8e45491d9c03
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213910"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="2fbf5-103">Krājumu vai izejmateriālu izsekošana</span><span class="sxs-lookup"><span data-stu-id="2fbf5-103">Trace an item or raw material</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2fbf5-104">Šajā procedūra parādīts, kā lietot krājumu izsekošanu, lai identificētu, kur krājumi vai izejmateriāli ir izmantoti vai tiek izmantoti.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="2fbf5-105">Izmantojot šo procedūru, varat identificēt krājumu, izsekot to atpakaļ līdz avotam un pēc tam izsekot uz priekšu līdz ražošanai un pabeigtās preces pārdošanai.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="2fbf5-106">Procesu var lietot, lai izpētītu ietekmētos klientus, skartos pārdošanas pasūtījumus un citus aspektus.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="2fbf5-107">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma USP2 dati.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="2fbf5-108">Krājuma izsekošana atpakaļ, izmantojot zināmu partijas numuru</span><span class="sxs-lookup"><span data-stu-id="2fbf5-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="2fbf5-109">**Navigācijas rūtī** dodieties uz **Moduļi > Krājuma pārvaldība > Pieprasījumi un pārskati > Izsekošanas dimensijas > Krājuma izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="2fbf5-110">Laukā **Krājuma numurs** atlasiet P9100.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="2fbf5-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2fbf5-112">Laukā **Uz priekšu vai atpakaļ** atlasiet vienumu Atpakaļ.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="2fbf5-113">Laukā **Partijas numurs** atlasiet as-12-344-01.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="2fbf5-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="2fbf5-115">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="2fbf5-116">Krājuma identificēšana, tā izsekošana uz priekšu un analīzes veikšana</span><span class="sxs-lookup"><span data-stu-id="2fbf5-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="2fbf5-117">Koka struktūras augšējais zars atspoguļo atlasītā krājuma un partijas rīcībā esošo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="2fbf5-118">Jums ir jāizvērš koka struktūras zari, lai atrastu krājumu, kuram ir jāveic uz priekšu vērstā izsekošanu.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="2fbf5-119">Koka struktūrā izvērsiet “tālāk aprakstītos zarus, un pēc tam atlasiet pēdējo zaru”.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="2fbf5-120">Izvērsiet: “P9100 / 1 / 10 / as-12-344-01 ● 2 muciņas ● 7,00 gal. \P9100 ● Izdots ● Pārdošanas pasūtījums 000072 ● 12/22/2015 ● -1 muciņa ● -4,00 gal. ● Vieta=1, Noliktava=10, Partijas numurs=as-12-344-01 \P9100 ● Ražošana B-000050 ● 12/9/2015● 7 muciņas ● 27,00 gal. ● Vieta=1,Noliktava=10,Partijas numurs=as-12-344-01 ● Līdzprodukti: P9101” un pēc tam atlasiet šo zaru.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="2fbf5-121">Koka struktūrā izvērsiet “tālāk aprakstīto zaru un pēc tam atlasiet šo zaru”.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="2fbf5-122">Sākot no jūsu atlasīta zara izvērsiet “M9103 ● Ražošanas rinda B-000050 ● 12/9/2015 ● -160,00 mārc. ● Izmērs=70, Krāsa=Labi, Vieta=1, Noliktava=10, Partijas numurs=App01'” un pēc tam atlasiet šo zaru.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-122">Starting from the node that you've just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="2fbf5-123">Noklikšķiniet uz krājuma **Izsekošana no zara**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="2fbf5-124">Nokl. **Tālāk**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-124">Click **Forward**.</span></span>
5. <span data-ttu-id="2fbf5-125">**Darbību rūtī** noklikšķiniet uz krājuma **Izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="2fbf5-126">Pastāv vairākas izsekošanas opcijas, kas sniedz informāciju par debitoriem, kurus ietekmē jūsu izsekotais krājums, kā arī ar šo krājumu saistītajiem pārdošanas pasūtījumiem, kas ir un vēl nav nosūtīti.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-126">There are several tracing options which provide information about the customers impacted by the item that you're tracing, and the sales orders related to the item which have and haven't been shipped.</span></span>   
6. <span data-ttu-id="2fbf5-127">Noklikšķiniet uz krājuma **Debitori**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-127">Click **Customers**.</span></span>
7. <span data-ttu-id="2fbf5-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-128">Close the page.</span></span>
8. <span data-ttu-id="2fbf5-129">**Darbību rūtī** noklikšķiniet uz krājuma **Izsekošana**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="2fbf5-130">Noklikšķiniet uz vienuma **Nosūtītie pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="2fbf5-131">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="2fbf5-131">Close the page.</span></span>

