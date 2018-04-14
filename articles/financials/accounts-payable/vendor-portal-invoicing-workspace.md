---
title: "Kreditora sadarbības rēķinu izveides darbvieta"
description: "Šajā tēmā izskaidrots, kā jūs varat skatīt kreditora rēķinus un iesniegt rēķinus no kreditora sadarbības rēķinu izveides darbvietas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 57fc1c21394d91f6a8bd4726c9d948c8ae2cf4d0
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="4c28b-103">Kreditora sadarbības rēķinu izveides darbvieta</span><span class="sxs-lookup"><span data-stu-id="4c28b-103">Vendor collaboration invoicing workspace</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="4c28b-104">Šajā tēmā izskaidrots, kā jūs varat skatīt kreditora rēķinus un iesniegt rēķinus no kreditora sadarbības rēķinu izveides darbvietas.</span><span class="sxs-lookup"><span data-stu-id="4c28b-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="4c28b-105">**Kreditora sadarbības rēķinu izveides** darbvietu var izmantot, lai skatītu kreditoru rēķinu informāciju un iesniegtu rēķinus programmatūrā Microsoft Dynamics 365 for Finance and Operations, izmantojot darbplūsmas iespējas.</span><span class="sxs-lookup"><span data-stu-id="4c28b-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="4c28b-106">Kreditoru sadarbības rēķinu izveidošanas darbvieta</span><span class="sxs-lookup"><span data-stu-id="4c28b-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="4c28b-107">Kopsavilkuma elementi</span><span class="sxs-lookup"><span data-stu-id="4c28b-107">Summary tiles</span></span>

<span data-ttu-id="4c28b-108">Elementi **Kopsavilkums** sniedz pārskatu par atlasītā kreditora rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="4c28b-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="4c28b-109">Jūs varat skatīt rēķinus pēc to stāvokļa.</span><span class="sxs-lookup"><span data-stu-id="4c28b-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="4c28b-110">Melnraksta rēķini netika iesniegti darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="4c28b-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="4c28b-111">Iesniegtie un neapstiprinātie rēķini ir rēķini, kurus kreditors ir iesniedzis, bet kas nav grāmatoti programmatūrā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c28b-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="4c28b-112">Apstiprinātie un neapmaksātie rēķini ir rēķini, kuri ir grāmatoti programmatūrā Finance and Operations, taču vēl nav pilnībā apmaksāti.</span><span class="sxs-lookup"><span data-stu-id="4c28b-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="4c28b-113">Apmaksātie rēķini ir rēķini, kas ir pilnībā apmaksāti programmatūrā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4c28b-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="4c28b-114">Noklikšķinot uz elementa tiks atvērts lapas **Rēķinu saraksts** filtrētais skatījums.</span><span class="sxs-lookup"><span data-stu-id="4c28b-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="4c28b-115">Tabulveida saraksti</span><span class="sxs-lookup"><span data-stu-id="4c28b-115">Tabular lists</span></span>

<span data-ttu-id="4c28b-116">Sadaļā **Tabulveida saraksti** rēķinu izrakstīšanas stāvoklis tiek sadalīts līdzīgi kā kopsavilkuma elementi: Melnraksti un Iesniegti, neapstiprināti saraksti.</span><span class="sxs-lookup"><span data-stu-id="4c28b-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="4c28b-117">Esot stāvoklī Melnraksts, rēķinu nevar iesniegt darbplūsmai vai dzēst.</span><span class="sxs-lookup"><span data-stu-id="4c28b-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="4c28b-118">Rēķinu meklēšanai var izmantot pēdējo tabulveida sarakstu.</span><span class="sxs-lookup"><span data-stu-id="4c28b-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="4c28b-119">Lai ātrāk iegūtu rezultātus, varat iestatīt dažādus filtrus.</span><span class="sxs-lookup"><span data-stu-id="4c28b-119">You can filter as you search, to allow for faster searches.</span></span>

<a name="all-vendor-invoices-list-page"></a><span data-ttu-id="4c28b-120">Visu kreditora rēķinu saraksta lapa</span><span class="sxs-lookup"><span data-stu-id="4c28b-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="4c28b-121">Visus grāmatotos un negrāmatotos kreditora rēķinus varat skatīt saraksta lapā **Kreditora sadarbības rēķini**.</span><span class="sxs-lookup"><span data-stu-id="4c28b-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="4c28b-122">Šo saraksta lapu varat izmantot, lai skatītu rēķinu maksājuma statusu.</span><span class="sxs-lookup"><span data-stu-id="4c28b-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="4c28b-123">Maksājumu statusi ir Negrāmatots, Neapmaksāts, Daļēji apmaksāts un Pilnībā apmaksāts.</span><span class="sxs-lookup"><span data-stu-id="4c28b-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="4c28b-124">Jauna kreditora rēķina izveide no pirkšanas pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="4c28b-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="4c28b-125">Jūs varat izveidot jaunu kreditora rēķinu, atlasot darbību **Jauns** **Kreditora sadarbības rēķinu izveides** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="4c28b-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="4c28b-126">Kreditoram jāsniedz pirkšanas pasūtījuma numurs un rēķina numurs.</span><span class="sxs-lookup"><span data-stu-id="4c28b-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="4c28b-127">Pēc noklusējuma visas kreditora pirkšanas pasūtījuma rindas tiek iekļautas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="4c28b-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="4c28b-128">Daudzuma un izmaksu informāciju var rediģēt pirms kreditora rēķina iesniegšanas darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="4c28b-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="4c28b-129">Pirms rēķina iesniegšanas jūs varat pievienot failus, piezīmes, attēlus un URL vietrāžus.</span><span class="sxs-lookup"><span data-stu-id="4c28b-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="4c28b-130">Papildinformāciju skatiet šeit: [Kreditoru sadarbība ar ārējiem kreditoriem](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="4c28b-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>




