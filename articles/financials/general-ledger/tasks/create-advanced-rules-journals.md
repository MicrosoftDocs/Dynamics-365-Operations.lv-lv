---
title: Žurnālu papildu kārtulu izveide
description: Šajā procedūrā parādīts, kā izveidot papildu kārtulas žurnāliem.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "326174"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="32283-103">Žurnālu papildu kārtulu izveide</span><span class="sxs-lookup"><span data-stu-id="32283-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32283-104">Šajā procedūrā parādīts, kā izveidot papildu kārtulas žurnāliem.</span><span class="sxs-lookup"><span data-stu-id="32283-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="32283-105">Tas ietver žurnāla pārbaudes un grāmatošanas ierobežojumu lietotājiem iestatīšanu.</span><span class="sxs-lookup"><span data-stu-id="32283-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="32283-106">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USMF” dati.</span><span class="sxs-lookup"><span data-stu-id="32283-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="32283-107">Žurnāla pārbaudes iestatīšana</span><span class="sxs-lookup"><span data-stu-id="32283-107">Set up journal control</span></span>
1. <span data-ttu-id="32283-108">Pārejiet uz sadaļu Virsgrāmata >Žurnāla iestatīšana > Žurnālu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="32283-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="32283-109">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="32283-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="32283-110">Noklikšķiniet uz Žurnāla pārbaude.</span><span class="sxs-lookup"><span data-stu-id="32283-110">Click Journal control.</span></span>
4. <span data-ttu-id="32283-111">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="32283-111">Click Add.</span></span>
5. <span data-ttu-id="32283-112">Laukā Datu faili noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="32283-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="32283-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="32283-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="32283-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="32283-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="32283-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="32283-115">Click Add.</span></span>
9. <span data-ttu-id="32283-116">Laukā Konta struktūra noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="32283-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="32283-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="32283-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="32283-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="32283-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="32283-119">Laukā Segments noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="32283-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="32283-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="32283-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="32283-121">Laukā No vērtības noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="32283-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="32283-122">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="32283-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="32283-123">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="32283-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="32283-124">Laukā Līdz vērtībai noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="32283-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="32283-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="32283-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="32283-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="32283-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="32283-127">Grāmatošanas ierobežojumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="32283-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="32283-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="32283-128">Close the page.</span></span>
2. <span data-ttu-id="32283-129">Noklikšķiniet uz Grāmatošanas ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="32283-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="32283-130">Laukā Kā jūs vēlaties noteikt grāmatošanas ierobežojumus atlasiet Pēc lietotāju grupas.</span><span class="sxs-lookup"><span data-stu-id="32283-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="32283-131">Kokā pārbaudiet "grupu, kurai vēlaties atļaut grāmatošanu šim žurnāla nosaukumam".</span><span class="sxs-lookup"><span data-stu-id="32283-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="32283-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="32283-132">Click OK.</span></span>

