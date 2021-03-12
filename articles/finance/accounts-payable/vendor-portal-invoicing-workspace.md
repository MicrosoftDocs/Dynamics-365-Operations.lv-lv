---
title: Kreditora sadarbības rēķinu izveides darbvieta
description: Šajā tēmā izskaidrots, kā jūs varat skatīt kreditora rēķinus un iesniegt rēķinus no kreditora sadarbības rēķinu izveides darbvietas.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 30e9012845838a4d1df5f1308740b356a64433e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993167"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="2c904-103">Kreditora sadarbības rēķinu izveides darbvieta</span><span class="sxs-lookup"><span data-stu-id="2c904-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c904-104">Šajā tēmā izskaidrots, kā jūs varat skatīt kreditora rēķinus un iesniegt rēķinus no kreditora sadarbības rēķinu izveides darbvietas.</span><span class="sxs-lookup"><span data-stu-id="2c904-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="2c904-105">Darbvietu **Kreditoru sadarbības rēķinu izveidošana** var izmantot, lai skatītu kreditoru rēķinu informāciju un lai iesniegtu rēķinus sistēmā, izmantojot darbplūsmas iespējas.</span><span class="sxs-lookup"><span data-stu-id="2c904-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="2c904-106">Kreditoru sadarbības rēķinu izveidošanas darbvieta</span><span class="sxs-lookup"><span data-stu-id="2c904-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="2c904-107">Kopsavilkuma elementi</span><span class="sxs-lookup"><span data-stu-id="2c904-107">Summary tiles</span></span>

<span data-ttu-id="2c904-108">Elementi **Kopsavilkums** sniedz pārskatu par atlasītā kreditora rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="2c904-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="2c904-109">Jūs varat skatīt rēķinus pēc to stāvokļa.</span><span class="sxs-lookup"><span data-stu-id="2c904-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="2c904-110">Melnraksta rēķini netika iesniegti darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="2c904-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="2c904-111">Iesniegtie un neapstiprinātie rēķini ir rēķini, kurus kreditors ir iesniedzis, bet kas nav grāmatoti programmā.</span><span class="sxs-lookup"><span data-stu-id="2c904-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="2c904-112">Apstiprinātie un neapmaksātie rēķini ir rēķini, kuri ir grāmatoti, taču vēl nav pilnībā apmaksāti.</span><span class="sxs-lookup"><span data-stu-id="2c904-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="2c904-113">Apmaksātie rēķini ir rēķini, kas ir pilnībā apmaksāti programmā.</span><span class="sxs-lookup"><span data-stu-id="2c904-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="2c904-114">Noklikšķinot uz elementa tiks atvērts lapas **Rēķinu saraksts** filtrētais skatījums.</span><span class="sxs-lookup"><span data-stu-id="2c904-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="2c904-115">Tabulveida saraksti</span><span class="sxs-lookup"><span data-stu-id="2c904-115">Tabular lists</span></span>

<span data-ttu-id="2c904-116">Sadaļā **Tabulveida saraksti** rēķinu izrakstīšanas stāvoklis tiek sadalīts līdzīgi kā kopsavilkuma elementi: Melnraksti un Iesniegti, neapstiprināti saraksti.</span><span class="sxs-lookup"><span data-stu-id="2c904-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="2c904-117">Esot stāvoklī Melnraksts, rēķinu nevar iesniegt darbplūsmai vai dzēst.</span><span class="sxs-lookup"><span data-stu-id="2c904-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="2c904-118">Rēķinu meklēšanai var izmantot pēdējo tabulveida sarakstu.</span><span class="sxs-lookup"><span data-stu-id="2c904-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="2c904-119">Lai ātrāk iegūtu rezultātus, varat iestatīt dažādus filtrus.</span><span class="sxs-lookup"><span data-stu-id="2c904-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="2c904-120">Visu kreditora rēķinu saraksta lapa</span><span class="sxs-lookup"><span data-stu-id="2c904-120">All vendor invoices list page</span></span>

<span data-ttu-id="2c904-121">Visus grāmatotos un negrāmatotos kreditora rēķinus varat skatīt saraksta lapā **Kreditora sadarbības rēķini**.</span><span class="sxs-lookup"><span data-stu-id="2c904-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="2c904-122">Šo saraksta lapu varat izmantot, lai skatītu rēķinu maksājuma statusu.</span><span class="sxs-lookup"><span data-stu-id="2c904-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="2c904-123">Maksājumu statusi ir Negrāmatots, Neapmaksāts, Daļēji apmaksāts un Pilnībā apmaksāts.</span><span class="sxs-lookup"><span data-stu-id="2c904-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="2c904-124">Jauna kreditora rēķina izveide no pirkšanas pasūtījuma</span><span class="sxs-lookup"><span data-stu-id="2c904-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="2c904-125">Jūs varat izveidot jaunu kreditora rēķinu, atlasot darbību **Jauns** **Kreditora sadarbības rēķinu izveides** darbvietā.</span><span class="sxs-lookup"><span data-stu-id="2c904-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="2c904-126">Kreditoram jāsniedz pirkšanas pasūtījuma numurs un rēķina numurs.</span><span class="sxs-lookup"><span data-stu-id="2c904-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="2c904-127">Pēc noklusējuma visas kreditora pirkšanas pasūtījuma rindas tiek iekļautas rēķinā.</span><span class="sxs-lookup"><span data-stu-id="2c904-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="2c904-128">Daudzuma un izmaksu informāciju var rediģēt pirms kreditora rēķina iesniegšanas darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="2c904-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="2c904-129">Pirms rēķina iesniegšanas jūs varat pievienot failus, piezīmes, attēlus un URL vietrāžus.</span><span class="sxs-lookup"><span data-stu-id="2c904-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="2c904-130">Papildinformāciju skatiet šeit: [Kreditoru sadarbība ar ārējiem kreditoriem](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="2c904-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>



