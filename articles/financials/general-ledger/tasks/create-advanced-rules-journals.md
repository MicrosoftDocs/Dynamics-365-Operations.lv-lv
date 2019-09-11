---
title: Žurnālu papildu kārtulu izveide
description: Šajā procedūrā parādīts, kā izveidot papildu kārtulas žurnāliem.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3eb34ac419aeab3663a8931d022abf7bcbfddd37
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916153"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="f66fa-103">Žurnālu papildu kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="f66fa-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f66fa-104">Šajā procedūrā parādīts, kā izveidot papildu kārtulas žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="f66fa-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="f66fa-105">Tas ietver žurnāla pārbaudes un grāmatošanas ierobežojumu lietotājiem iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="f66fa-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="f66fa-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="f66fa-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="f66fa-107">Žurnāla pārbaudes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f66fa-107">Set up journal control</span></span>
1. <span data-ttu-id="f66fa-108">**Navigācijas rūtī** ejiet uz **Moduļi > Virsgrāmata > Žurnāla iestatīšana > Žurnāla nosaukumi**.</span><span class="sxs-lookup"><span data-stu-id="f66fa-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="f66fa-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f66fa-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f66fa-110">**Darbību rūtī** noklikšķiniet uz **Žurnāla pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="f66fa-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="f66fa-111">Kopsavilkuma cilnē **Kādus kontu veidus var publicēt** klikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f66fa-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="f66fa-112">Laukā **Uzņēmuma konti** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="f66fa-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f66fa-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f66fa-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f66fa-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f66fa-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f66fa-115">Kopsavilkuma cilnē **Kādas segmenta vērtības ir spēkā šim žurnālam**, klikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="f66fa-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="f66fa-116">Laukā **Konta struktūra** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="f66fa-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f66fa-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f66fa-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="f66fa-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f66fa-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f66fa-119">Laukā **Segments** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="f66fa-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="f66fa-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f66fa-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="f66fa-121">Laukā **No vērtība** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="f66fa-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="f66fa-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f66fa-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="f66fa-123">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f66fa-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="f66fa-124">Laukā **Līdz vērtība** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="f66fa-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="f66fa-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f66fa-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="f66fa-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f66fa-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="f66fa-127">Grāmatošanas ierobežojumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="f66fa-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="f66fa-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f66fa-128">Close the page.</span></span>
2. <span data-ttu-id="f66fa-129">Klikšķiniet uz **Publicēšanas ierobežojumi**.</span><span class="sxs-lookup"><span data-stu-id="f66fa-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="f66fa-130">Laukā **Kā vēlaties iestatīt publicēšanas ierobežojumus**, atlasiet „Pēc lietotāju grupas”.</span><span class="sxs-lookup"><span data-stu-id="f66fa-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="f66fa-131">Kokā pārbaudiet "grupu, kurai vēlaties atļaut grāmatošanu šim žurnāla nosaukumam".</span><span class="sxs-lookup"><span data-stu-id="f66fa-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="f66fa-132">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f66fa-132">Click **OK**.</span></span>

