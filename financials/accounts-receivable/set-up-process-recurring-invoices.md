---
title: "Periodisko rēķinu iestatīšana un apstrāde"
description: "Šajā rakstā ir paskaidrots, kā iestatīt un apstrādāt periodiskos rēķinus. Periodiskos rēķinus varat izmantot, ja debitoriem regulāri ir jāizraksta rēķini par tādu pašu summu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 5f095b74df8b680f6e7e54520f9684298ec51aad
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="ca5a3-104">Periodisko rēķinu iestatīšana un apstrāde</span><span class="sxs-lookup"><span data-stu-id="ca5a3-104">Set up and process recurring invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ca5a3-105">Šajā rakstā ir paskaidrots, kā iestatīt un apstrādāt periodiskos rēķinus.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="ca5a3-106">Periodiskos rēķinus varat izmantot, ja debitoriem regulāri ir jāizraksta rēķini par tādu pašu summu.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="ca5a3-107">Periodiska brīva teksta rēķina veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="ca5a3-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="ca5a3-108">Lai debitoram regulāri izrakstītu rēķinu par vieniem pakalpojumiem, ir jādefinē brīvā teksta rēķina veidne, ko var atkārtoti izmantot, lai izveidotu rēķinus.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="ca5a3-109">Šajā veidnē ir ietverta šāda informācija:</span><span class="sxs-lookup"><span data-stu-id="ca5a3-109">This template contains the following information:</span></span>

-   <span data-ttu-id="ca5a3-110">galvenes informācija, piemēram, PVN grupas, apmaksas nosacījumi un maksāšanas metode;</span><span class="sxs-lookup"><span data-stu-id="ca5a3-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="ca5a3-111">rindas informācija, piemēram, pakalpojuma apraksts, ieņēmumu konti, vienības cena un rēķina summa;</span><span class="sxs-lookup"><span data-stu-id="ca5a3-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="ca5a3-112">piegādes vai apstrādes maksa;</span><span class="sxs-lookup"><span data-stu-id="ca5a3-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="ca5a3-113">uzskaites sadales kopā ar finanšu dimensiju informāciju, piemēram, izmaksu centri un biznesa vienības.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="ca5a3-114">Faktiski tiek izveidots viss rēķins un pēc tam tas tiek saglabāts kā veidne.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="ca5a3-115">Var iestatīt veidnes, izmantojot lapu **Periodiskie rēķini**.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="ca5a3-116">Brīva teksta rēķina veidnes piešķšana debitoram un periodiskuma datu ievade</span><span class="sxs-lookup"><span data-stu-id="ca5a3-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="ca5a3-117">Kad veidne ir izveidota, tā ir jāpiešķir debitoriem, kam vēlaties izrakstīt rēķinu.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="ca5a3-118">Turklāt ir jānorāda, kad un cik bieži rēķins tiks izmantots.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="ca5a3-119">Veidnes varat piešķirt lapas **Debitori** cilnē **Rēķins**.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="ca5a3-120">Pievienojiet veidni sarakstam un atjauniniet šādu informāciju:</span><span class="sxs-lookup"><span data-stu-id="ca5a3-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="ca5a3-121">periodiskas rēķinu izrakstīšanas sākuma datumu un, ja nepieciešams, beigu datumu;</span><span class="sxs-lookup"><span data-stu-id="ca5a3-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="ca5a3-122">periodiskas rēķinu izrakstīšanas biežumu (piemēram, katru dienu vai reizi mēnesī);</span><span class="sxs-lookup"><span data-stu-id="ca5a3-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="ca5a3-123">maksimālo rēķina summu (ja šī informācija ir obligāti jānorāda).</span><span class="sxs-lookup"><span data-stu-id="ca5a3-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="ca5a3-124">Debitoram var būt vairākas veidnes, kam ir iestatīti dažādi biežumi.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="ca5a3-125">Periodisko rēķinu ģenerēšana</span><span class="sxs-lookup"><span data-stu-id="ca5a3-125">Generate the recurring invoices</span></span>
<span data-ttu-id="ca5a3-126">Lapā **Periodiskie rēķini** ir uzdevums, kas apstrādā periodisko rēķinu veidnes.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="ca5a3-127">Norādiet rēķina datumu un veidni, kas jāizmanto rēķinu ģenerēšanā.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="ca5a3-128">Rēķini tiks ģenerēti, un katrai apstrādājamajai rēķinu grupai tiks piešķirts viens periodiskuma ID numurs.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>
<span data-ttu-id="ca5a3-129">Periodisko brīva teksta rēķinu grāmatošana</span><span class="sxs-lookup"><span data-stu-id="ca5a3-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="ca5a3-130">Pēc tam, kad periodiskie rēķini ir ģenerēti, rēķinu periodiskuma ID parādīsies grāmatošanas uzdevumā lapā **Periodiskie rēķini**.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="ca5a3-131">Visus rēķinus ar vienu periodiskuma ID var skatīt, noklikšķinot uz saites.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="ca5a3-132">Pārskatot rēķinus ar vienu periodiskuma ID, atsevišķus rēķinus varat dzēst.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="ca5a3-133">Debitora periodiskuma iestatījumi tiks atiestatīti šai veidnei, tādējādi vēlāk to var atkārtoti ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="ca5a3-134">Vienam periodiskuma ID var grāmatot vienu, vairākus vai visus rēķinus.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="ca5a3-135">Ja darbplūsmas ir iespējotas, lai rēķinus grāmatotu, noklikšķiniet uz **Iesniegt**.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>
<span data-ttu-id="ca5a3-136">Periodisko brīva teksta rēķinu drukāšana</span><span class="sxs-lookup"><span data-stu-id="ca5a3-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="ca5a3-137">Ja periodiskie rēķini ir iegrāmatoti, rēķinus var drukāt no brīva teksta rēķina saraksta lapas.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="ca5a3-138">Varat drukāt atlasītos rēķinus, vai arī varat atlasīt drukāšanai rēķinu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="ca5a3-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>




