--- 
title: "Pamatlīdzekļa pārsūtīšana"
description: "Šajā uzdevuma ceļvedī ir parādīts, kā pamatlīdzekļa grāmatai pārsūtīt finanšu informāciju no vienas finanšu dimensiju kopas uz jaunu finanšu dimensiju kopu."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b193cf6fbed810f0d5234514573d0f5c23c7b2c8
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="25b2e-103">Pamatlīdzekļa pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="25b2e-103">Transfer a fixed asset</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25b2e-104">Šajā uzdevuma ceļvedī ir parādīts, kā pamatlīdzekļa grāmatai pārsūtīt finanšu informāciju no vienas finanšu dimensiju kopas uz jaunu finanšu dimensiju kopu.</span><span class="sxs-lookup"><span data-stu-id="25b2e-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="25b2e-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="25b2e-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="25b2e-106">Pārejiet uz sadaļu Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="25b2e-106">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="25b2e-107">Sarakstā atrodiet un atlasiet pārsūtāmo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="25b2e-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="25b2e-108">Darbību rūtī noklikšķiniet uz Pamatlīdzeklis.</span><span class="sxs-lookup"><span data-stu-id="25b2e-108">On the Action Pane, click Fixed asset.</span></span>
4. <span data-ttu-id="25b2e-109">Noklikšķiniet uz Pārsūtīt pamatlīdzekļus.</span><span class="sxs-lookup"><span data-stu-id="25b2e-109">Click Transfer fixed assets.</span></span>
5. <span data-ttu-id="25b2e-110">Ievadiet datumu laukā Pārsūtīšanas datums.</span><span class="sxs-lookup"><span data-stu-id="25b2e-110">In the Transfer date field, enter a date.</span></span>
6. <span data-ttu-id="25b2e-111">Ievadiet komentārus pārsūtīšanas aprakstam.</span><span class="sxs-lookup"><span data-stu-id="25b2e-111">Enter comments to describe the transfer.</span></span>
    * <span data-ttu-id="25b2e-112">Šajā sarakstā ir redzamas visas šī pamatlīdzekļa grāmatas.</span><span class="sxs-lookup"><span data-stu-id="25b2e-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="25b2e-113">Atzīmējiet grāmatas, kuras vēlaties pārsūtīt uz jauno finanšu dimensijas kopu.</span><span class="sxs-lookup"><span data-stu-id="25b2e-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="25b2e-114">Šajā sarakstā ir redzamas atlasītajai grāmatai esošās finanšu dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="25b2e-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="25b2e-115">Atlasiet finanšu dimensiju, kuru vēlaties atjaunināt atlasītā pamatlīdzekļa grāmatai.</span><span class="sxs-lookup"><span data-stu-id="25b2e-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="25b2e-116">Laukā Finanšu dimensija noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="25b2e-116">In the Financial dimension field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="25b2e-117">Attiecīgi iestatiet citas finanšu dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="25b2e-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="25b2e-118">Notiekot pārsūtīšanai, tiek mainītas visas finanšu dimensiju vērtības, gan ievadītajām vērtībām, gan tukšajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="25b2e-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="25b2e-119">Piemēram, ja ievadāt vērtību BusinessUnit, bet laukus CostCenter un Nodaļas finanšu dimensijas atstājat tukšus.</span><span class="sxs-lookup"><span data-stu-id="25b2e-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="25b2e-120">Ja jūsu konta struktūra pieļauj tukšas vērtības CostCenter un Nodaļa laukos, tad pēc pārsūtīšanas katram vērtības modelim būtu jauna BusinessUnit vērtība un tukša vērtība laukiem CostCenter un Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="25b2e-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="25b2e-121">Noklikšķiniet uz Atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="25b2e-121">Click Update.</span></span>
    * <span data-ttu-id="25b2e-122">Jums ir iespēja apskatīt izmaiņas pirms pārsūtīšanas pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="25b2e-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="25b2e-123">Pirms pamatlīdzekļa grāmatu pārsūtīšanas pārskatiet rezultātus.</span><span class="sxs-lookup"><span data-stu-id="25b2e-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="25b2e-124">Noklikšķiniet uz Pārvest.</span><span class="sxs-lookup"><span data-stu-id="25b2e-124">Click Transfer.</span></span>


