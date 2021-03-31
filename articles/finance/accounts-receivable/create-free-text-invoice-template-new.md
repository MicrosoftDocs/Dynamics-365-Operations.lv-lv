---
title: Brīva teksta rēķina veidnes izveide
description: Šajā procedūrā ir paskaidrots, kā izveidot brīva teksta rēķina veidni.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abdcb307686800e0038212982c1eac6f1c14cf8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217486"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="49b22-103">Brīva teksta rēķina veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="49b22-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49b22-104">Šajā apskatā izmantojiet demonstrācijas uzņēmuma “USMF” datus.</span><span class="sxs-lookup"><span data-stu-id="49b22-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="49b22-105">Šī procedūra ir paredzēta lietotājam, kurš ir atbildīgs par debitoru parādu rēķinu pārvaldīšanu un apstrādi.</span><span class="sxs-lookup"><span data-stu-id="49b22-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="49b22-106">Izveidot veidni</span><span class="sxs-lookup"><span data-stu-id="49b22-106">Create a template</span></span>

1. <span data-ttu-id="49b22-107">Pārejiet uz sadaļu Debitori > Rēķini > Periodiskie rēķini > Brīva teksta rēķina veidnes.</span><span class="sxs-lookup"><span data-stu-id="49b22-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="49b22-108">Lietojiet šo veidlapu, lai izveidotu brīva teksta rēķina veidnes, kuras var saturēt rēķina rindas, maksas, uzskaites sadales veidnes un Virsgrāmatas konta informāciju.</span><span class="sxs-lookup"><span data-stu-id="49b22-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="49b22-109">Lai izveidotu jaunu brīva teksta rēķina veidni, noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="49b22-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="49b22-110">Ierakstiet vērtību laukā Veidnes nosaukums.</span><span class="sxs-lookup"><span data-stu-id="49b22-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="49b22-111">Veidnes nosaukums unikāli identificē brīvā teksta rēķina veidni.</span><span class="sxs-lookup"><span data-stu-id="49b22-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="49b22-112">Divām veidnēm nevar būt vienādi veidņu nosaukumi.</span><span class="sxs-lookup"><span data-stu-id="49b22-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="49b22-113">Laukā Apraksts ievadiet veidnes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="49b22-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="49b22-114">Izvērsiet cilni Rēķina rindas.</span><span class="sxs-lookup"><span data-stu-id="49b22-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="49b22-115">Laukā Apraksts ievadiet rēķina rindas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="49b22-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="49b22-116">Laukā Galvenais konts atlasiet ieņēmumu kontu.</span><span class="sxs-lookup"><span data-stu-id="49b22-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="49b22-117">Debitoru grāmatošanas metožu lapā varat atlasīt debitora kredīta korespondējošo transakciju kontu kopējai rēķina summai.</span><span class="sxs-lookup"><span data-stu-id="49b22-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="49b22-118">Laukā PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="49b22-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="49b22-119">PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.</span><span class="sxs-lookup"><span data-stu-id="49b22-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="49b22-120">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="49b22-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="49b22-121">Laukā Krājuma nodokļu grupa atlasiet pašreizējās rēķina rindas krājuma PVN grupu.</span><span class="sxs-lookup"><span data-stu-id="49b22-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="49b22-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="49b22-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="49b22-123">Laukā Vienības cena ievadiet vai apskatiet rēķina rindas vienas vienības cenu</span><span class="sxs-lookup"><span data-stu-id="49b22-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="49b22-124">Šī summa tiek reizināta ar vērtību laukā Daudzums, lai noteiktu rēķina rindas summu.</span><span class="sxs-lookup"><span data-stu-id="49b22-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="49b22-125">Pievienojiet jaunu rindu brīva teksta rēķina veidnei.</span><span class="sxs-lookup"><span data-stu-id="49b22-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="49b22-126">Laukā Apraksts ievadiet rēķina rindas aprakstu.</span><span class="sxs-lookup"><span data-stu-id="49b22-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="49b22-127">Laukā Galvenais konts atlasiet ieņēmumu kontu.</span><span class="sxs-lookup"><span data-stu-id="49b22-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="49b22-128">Debitoru grāmatošanas metožu lapā varat atlasīt debitora kredīta korespondējošo transakciju kontu kopējai rēķina summai.</span><span class="sxs-lookup"><span data-stu-id="49b22-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="49b22-129">Laukā PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="49b22-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="49b22-130">PVN grupa pašreizējai rēķina rindai ir noklusējuma PVN grupa šim debitora kontam.</span><span class="sxs-lookup"><span data-stu-id="49b22-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="49b22-131">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="49b22-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="49b22-132">Laukā Krājuma PVN grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="49b22-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="49b22-133">Pašreizējā rēķina rindas krājuma PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="49b22-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="49b22-134">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="49b22-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="49b22-135">Ievadiet vai apskatiet vienību skaitu rēķina rindai.</span><span class="sxs-lookup"><span data-stu-id="49b22-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="49b22-136">Šis skaitlis tiek reizināts ar vērtību laukā Vienības cena, lai noteiktu rēķina rindas summu.</span><span class="sxs-lookup"><span data-stu-id="49b22-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="49b22-137">Ievadiet vai apskatiet vienības cenu rēķina rindā.</span><span class="sxs-lookup"><span data-stu-id="49b22-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="49b22-138">Šī summa tiek reizināta ar vērtību laukā Daudzums, lai noteiktu rēķina rindas summu.</span><span class="sxs-lookup"><span data-stu-id="49b22-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="49b22-139">Apskatiet un modificējiet uzskaites sadales atsevišķai rindai un pastāvošām apakšrindām.</span><span class="sxs-lookup"><span data-stu-id="49b22-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="49b22-140">Uzskaites sadales definē, kā summa tiek uzskaitīta, piemēram, kā ieņēmumi, nodokļi vai izmaksas tiek uzskaitīti brīvā teksta rēķinā.</span><span class="sxs-lookup"><span data-stu-id="49b22-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="49b22-141">Atjauniniet atlasītās rēķina rindas uzskaites sadales.</span><span class="sxs-lookup"><span data-stu-id="49b22-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="49b22-142">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="49b22-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="49b22-143">Brīva teksta rēķina veidnes saglabāšana</span><span class="sxs-lookup"><span data-stu-id="49b22-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="49b22-144">Pašreizējo brīva teksta rēķinu varat saglabāt arī kā veidni.</span><span class="sxs-lookup"><span data-stu-id="49b22-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="49b22-145">Cilnē Rēķins atlasot Saglabāt kā veidni, ievadiet veidnes nosaukumu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="49b22-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="49b22-146">Ja veidne ar tādu nosaukumu jau pastāv, tiks parādīts paziņojums par to, ka veidne ar šādu nosaukumu jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="49b22-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="49b22-147">Jūs vienalga varat noklikšķināt uz Labi, lai to aizstātu.</span><span class="sxs-lookup"><span data-stu-id="49b22-147">You can still click on Ok to replace it.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]