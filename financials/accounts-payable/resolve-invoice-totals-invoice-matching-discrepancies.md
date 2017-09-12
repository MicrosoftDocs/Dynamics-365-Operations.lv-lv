---
title: "Neatbilstību novēršana rēķinu kopsummu salīdzināšanas laikā"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3f7e1261838866688c97529b0edfa1354034247b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---

# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="7f2a8-102">Neatbilstību novēršana rēķinu kopsummu salīdzināšanas laikā</span><span class="sxs-lookup"><span data-stu-id="7f2a8-102">Resolve discrepancies during invoice totals matching</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="7f2a8-103">Viens rēķinu salīdzināšanas validēšanas veids ir rēķinu kopsummu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-103">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="7f2a8-104">Lai norādītu, ka sistēmai būtu jāveic rēķinu kopsummu salīdzināšana, lapā **Kreditoru moduļa parametri** cilnē **Rēķinu validēšana** iestatiet opciju **Saskaņot rēķinu kopsummas** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-104">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="7f2a8-105">Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-105">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="7f2a8-106">Sešas kopsummas tiek salīdzinātas lapā **Detalizēta informācija par rēķinu kopsummu atbilstību**.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-106">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="7f2a8-107">Ja kāda no kopsummām atšķiras no paredzamās atbilstošās pirkšanas pasūtījuma kopsummas, salīdzināšanas laikā atklātā neatbilstība tiek atzīmēta.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-107">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="7f2a8-108">Lai pārskatītu rēķinu, kurā ir kopsummu salīdzināšanas neatbilstības, darbvietā **Kreditora rēķina ieraksts** noklikšķiniet uz elementa **Neizlemtie rēķini**.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-108">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="7f2a8-109">Pēc tam darbību rūtī cilnē **Pārskatīt** noklikšķiniet uz **Detalizēta informācija par atbilstību**.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-109">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="7f2a8-110">Ja ir konstatētas salīdzināšanas neatbilstības, blakus rēķina summai parādās brīdinājuma ikonas.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-110">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="7f2a8-111">Sīkāk par kopsummām varat skatīt detalizētā informācijā par rēķinu kopsummu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-111">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="7f2a8-112">Kad neatbilstība ir identificēta, var būt nepieciešams sazināties ar kreditoru, ja uzskatāt, ka rēķinā minētā informācija nav pareiza.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-112">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="7f2a8-113">Atkarībā no rezultātā iegūtās vienošanās ar kreditoru, varat veikt kādu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="7f2a8-113">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="7f2a8-114">Pieņemt cenas atšķirību un grāmatot rēķinu, kurā ir salīdzināšanas neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-114">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="7f2a8-115">Sistēmu var iestatīt, lai pieprasītu apstiprinājumu, pirms var grāmatot, vai pastāv salīdzināšanas neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-115">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="7f2a8-116">Šajā gadījumā jums ir jāapstiprina salīdzināšanas neatbilstība un pēc izvēles var ievadīt apstiprinājuma komentāru.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-116">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="7f2a8-117">Pēc tam varat atlasīt rēķina grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-117">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="7f2a8-118">Labot rēķina summu uz prognozējamo summu un grāmatot šo rēķinu.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-118">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="7f2a8-119">Pieprasīt no kreditora visu kredītu un jaunu, labotu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="7f2a8-119">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="7f2a8-120">Plašāku informāciju skatiet šeit: [Izpēte/izņēmumu novēršana](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="7f2a8-120">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>



