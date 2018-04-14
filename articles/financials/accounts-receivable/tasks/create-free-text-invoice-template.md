--- 
title: "Brīva teksta rēķina veidnes izveide"
description: "Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d785922d1c6775d95ad5697eb6a872434e59c8e4
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="1c314-103">Brīva teksta rēķina veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="1c314-103">Create a free text invoice template</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c314-104">Šajā ierakstā tiek izmantots USMF demonstrācijas uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="1c314-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="1c314-105">Ieraksts ir paredzēts lietotājam, kurš ir atbildīgs par debitoru parādu rēķinu pārvaldīšanu un apstrādi.</span><span class="sxs-lookup"><span data-stu-id="1c314-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="1c314-106">Pārejiet uz sadaļu Debitori > Rēķini > Periodiskie rēķini > Brīva teksta rēķina veidnes.</span><span class="sxs-lookup"><span data-stu-id="1c314-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="1c314-107">Lietojiet šo veidlapu, lai izveidotu brīva teksta rēķina veidnes, kuras var saturēt rēķina rindas, maksas, uzskaites sadales veidnes un Virsgrāmatas konta informāciju.</span><span class="sxs-lookup"><span data-stu-id="1c314-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="1c314-108">Lai izveidotu jaunu brīva teksta rēķina veidni, noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="1c314-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="1c314-109">Ierakstiet vērtību laukā Veidnes nosaukums.</span><span class="sxs-lookup"><span data-stu-id="1c314-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="1c314-110">Veidnes nosaukums unikāli identificē brīvā teksta rēķina veidni.</span><span class="sxs-lookup"><span data-stu-id="1c314-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="1c314-111">Divām veidnēm nevar būt vienādi veidņu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="1c314-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="1c314-112">Laukā Apraksts ievadiet veidnes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1c314-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="1c314-113">Izvērsiet cilni Rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="1c314-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="1c314-114">Laukā Apraksts ievadiet rēķina rindas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1c314-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="1c314-115">Laukā Galvenais konts atlasiet ieņēmumu kontu.</span><span class="sxs-lookup"><span data-stu-id="1c314-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="1c314-116">Debitoru grāmatošanas metožu lapā varat atlasīt debitora kredīta korespondējošo transakciju kontu kopējai rēķina summai.</span><span class="sxs-lookup"><span data-stu-id="1c314-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="1c314-117">Laukā PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c314-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1c314-118">PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.</span><span class="sxs-lookup"><span data-stu-id="1c314-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="1c314-119">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c314-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="1c314-120">Laukā Krājuma nodokļu grupa atlasiet pašreizējās rēķina rindas krājuma PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="1c314-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="1c314-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c314-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="1c314-122">Laukā Vienības cena ievadiet vai apskatiet rēķina rindas vienas vienības cenu</span><span class="sxs-lookup"><span data-stu-id="1c314-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="1c314-123">Šī summa tiek reizināta ar vērtību laukā Daudzums, lai noteiktu rēķina rindas summu.</span><span class="sxs-lookup"><span data-stu-id="1c314-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="1c314-124">Pievienojiet jaunu rindu brīva teksta rēķina veidnei.</span><span class="sxs-lookup"><span data-stu-id="1c314-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="1c314-125">Laukā Apraksts ievadiet rēķina rindas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="1c314-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="1c314-126">Laukā Galvenais konts atlasiet ieņēmumu kontu.</span><span class="sxs-lookup"><span data-stu-id="1c314-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="1c314-127">Debitoru grāmatošanas metožu lapā varat atlasīt debitora kredīta korespondējošo transakciju kontu kopējai rēķina summai.</span><span class="sxs-lookup"><span data-stu-id="1c314-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="1c314-128">Laukā PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c314-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1c314-129">PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.</span><span class="sxs-lookup"><span data-stu-id="1c314-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="1c314-130">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c314-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="1c314-131">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="1c314-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1c314-132">Pašreizējā rēķina rindas krājuma PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="1c314-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="1c314-133">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="1c314-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="1c314-134">Ievadiet vai apskatiet vienību skaitu rēķina rindai.</span><span class="sxs-lookup"><span data-stu-id="1c314-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="1c314-135">Šis skaitlis tiek reizināts ar vērtību laukā Vienības cena, lai noteiktu rēķina rindas summu.</span><span class="sxs-lookup"><span data-stu-id="1c314-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="1c314-136">Ievadiet vai apskatiet vienības cenu rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="1c314-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="1c314-137">Šī summa tiek reizināta ar vērtību laukā Daudzums, lai noteiktu rēķina rindas summu.</span><span class="sxs-lookup"><span data-stu-id="1c314-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="1c314-138">Apskatiet un modificējiet uzskaites sadales atsevišķai rindai un pastāvošām apakšrindām.</span><span class="sxs-lookup"><span data-stu-id="1c314-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="1c314-139">Uzskaites sadales definē, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīvā teksta rēķinā.</span><span class="sxs-lookup"><span data-stu-id="1c314-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="1c314-140">Atjauniniet atlasītās rēķina rindas uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="1c314-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="1c314-141">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="1c314-141">Click Close.</span></span>


