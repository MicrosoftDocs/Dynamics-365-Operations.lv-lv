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
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145220"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="b5b8f-103">Žurnālu papildu kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="b5b8f-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5b8f-104">Šajā procedūrā parādīts, kā izveidot papildu kārtulas žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="b5b8f-105">Tas ietver žurnāla pārbaudes un grāmatošanas ierobežojumu lietotājiem iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="b5b8f-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="b5b8f-107">Žurnāla pārbaudes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b5b8f-107">Set up journal control</span></span>
1. <span data-ttu-id="b5b8f-108">**Navigācijas rūtī** ejiet uz **Moduļi > Virsgrāmata > Žurnāla iestatīšana > Žurnāla nosaukumi**.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="b5b8f-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b5b8f-110">**Darbību rūtī** noklikšķiniet uz **Žurnāla pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="b5b8f-111">Kopsavilkuma cilnē **Kādus kontu veidus var publicēt** klikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="b5b8f-112">Laukā **Uzņēmuma konti** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="b5b8f-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="b5b8f-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b5b8f-115">Kopsavilkuma cilnē **Kādas segmenta vērtības ir spēkā šim žurnālam**, klikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="b5b8f-116">Laukā **Konta struktūra** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="b5b8f-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="b5b8f-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b5b8f-119">Laukā **Segments** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="b5b8f-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b5b8f-121">Laukā **No vērtība** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="b5b8f-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="b5b8f-123">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b5b8f-124">Laukā **Līdz vērtība** noklikšķiniet uz nolaižamās pogas uzmeklēšanas atvēršanai.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="b5b8f-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="b5b8f-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="b5b8f-127">Grāmatošanas ierobežojumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b5b8f-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="b5b8f-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-128">Close the page.</span></span>
2. <span data-ttu-id="b5b8f-129">Klikšķiniet uz **Publicēšanas ierobežojumi**.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="b5b8f-130">Laukā **Kā vēlaties iestatīt publicēšanas ierobežojumus**, atlasiet „Pēc lietotāju grupas”.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="b5b8f-131">Kokā pārbaudiet "grupu, kurai vēlaties atļaut grāmatošanu šim žurnāla nosaukumam".</span><span class="sxs-lookup"><span data-stu-id="b5b8f-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="b5b8f-132">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b5b8f-132">Click **OK**.</span></span>

