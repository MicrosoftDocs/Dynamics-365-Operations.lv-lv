---
title: Atrisināt neatbilstību rēķinu kopsummu saskaņošanas laikā
description: Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67aa0b89eed1f82290659029dfcce92ca3710aea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "331510"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching"></a><span data-ttu-id="09c37-103">Atrisināt neatbilstību rēķinu kopsummu saskaņošanas laikā</span><span class="sxs-lookup"><span data-stu-id="09c37-103">Resolve discrepancies during invoice totals matching</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09c37-104">Viens rēķinu salīdzināšanas validēšanas veids ir rēķinu kopsummu salīdzināšana.</span><span class="sxs-lookup"><span data-stu-id="09c37-104">One type of invoice matching validation is invoice totals matching.</span></span> <span data-ttu-id="09c37-105">Lai norādītu, ka sistēmai būtu jāveic rēķinu kopsummu salīdzināšana, lapā **Kreditoru moduļa parametri** cilnē **Rēķinu validēšana** iestatiet opciju **Saskaņot rēķinu kopsummas** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="09c37-105">To specify that the system should perform invoice totals matching, on the **Accounts payable parameters** page, on the **Invoice validation** tab, set the **Match invoice totals** option **Yes**.</span></span> 

<span data-ttu-id="09c37-106">Rēķinu kopsummu salīdzināšanu var izmantot, lai palīdzētu garantēt, ka rēķina kopsummas neatšķiras no paredzētajām summām vairāk par pieņemamo novirzi.</span><span class="sxs-lookup"><span data-stu-id="09c37-106">You can use invoice totals matching to help guarantee that total invoice amounts don't deviate from expected amounts by more than an acceptable variance.</span></span> <span data-ttu-id="09c37-107">Sešas kopsummas tiek salīdzinātas lapā **Detalizēta informācija par rēķinu kopsummu atbilstību**.</span><span class="sxs-lookup"><span data-stu-id="09c37-107">Six totals are compared on the **Invoice totals matching details** page.</span></span> <span data-ttu-id="09c37-108">Ja kāda no kopsummām atšķiras no paredzamās atbilstošās pirkšanas pasūtījuma kopsummas, salīdzināšanas laikā atklātā neatbilstība tiek atzīmēta.</span><span class="sxs-lookup"><span data-stu-id="09c37-108">If any one of the totals deviates from the expected corresponding purchase order total, a matching discrepancy is flagged.</span></span> 

<span data-ttu-id="09c37-109">Lai pārskatītu rēķinu, kurā ir kopsummu salīdzināšanas neatbilstības, darbvietā **Kreditora rēķina ieraksts** noklikšķiniet uz elementa **Neizlemtie rēķini**.</span><span class="sxs-lookup"><span data-stu-id="09c37-109">To review the invoice that has the totals matching discrepancies, in the **Vendor invoice entry** workspace, click the **Pending invoices** tile.</span></span> <span data-ttu-id="09c37-110">Pēc tam darbību rūtī cilnē **Pārskatīt** noklikšķiniet uz **Detalizēta informācija par atbilstību**.</span><span class="sxs-lookup"><span data-stu-id="09c37-110">Then, on the Action Pane, on the **Review** tab, click **Matching details**.</span></span> <span data-ttu-id="09c37-111">Ja ir konstatētas salīdzināšanas neatbilstības, blakus rēķina summai parādās brīdinājuma ikonas.</span><span class="sxs-lookup"><span data-stu-id="09c37-111">If matching discrepancies have been detected, warning icons appear next to the invoice amount.</span></span> <span data-ttu-id="09c37-112">Sīkāk par kopsummām varat skatīt detalizētā informācijā par rēķinu kopsummu atbilstību.</span><span class="sxs-lookup"><span data-stu-id="09c37-112">You can view more detail about the totals by viewing the invoice totals matching details.</span></span> 

<span data-ttu-id="09c37-113">Kad neatbilstība ir identificēta, var būt nepieciešams sazināties ar kreditoru, ja uzskatāt, ka rēķinā minētā informācija nav pareiza.</span><span class="sxs-lookup"><span data-stu-id="09c37-113">After you identify a discrepancy, you might have to contact the vendor if you think that the information on the invoice is incorrect.</span></span> <span data-ttu-id="09c37-114">Atkarībā no rezultātā iegūtās vienošanās ar kreditoru, varat veikt kādu no šīm darbībām:</span><span class="sxs-lookup"><span data-stu-id="09c37-114">Depending on the resulting agreement with the vendor, you can then take one of these actions:</span></span>

-   <span data-ttu-id="09c37-115">Pieņemt cenas atšķirību un grāmatot rēķinu, kurā ir salīdzināšanas neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="09c37-115">Accept the price difference, and post the invoice that has matching discrepancies.</span></span> <span data-ttu-id="09c37-116">Sistēmu var iestatīt, lai pieprasītu apstiprinājumu, pirms var grāmatot, vai pastāv salīdzināšanas neatbilstības.</span><span class="sxs-lookup"><span data-stu-id="09c37-116">Your system might be set up to require approval before it can post if there are matching discrepancies.</span></span> <span data-ttu-id="09c37-117">Šajā gadījumā jums ir jāapstiprina salīdzināšanas neatbilstība un pēc izvēles var ievadīt apstiprinājuma komentāru.</span><span class="sxs-lookup"><span data-stu-id="09c37-117">In this case, you must approve the matching discrepancy and can optionally enter an approval comment.</span></span> <span data-ttu-id="09c37-118">Pēc tam varat atlasīt rēķina grāmatošanu.</span><span class="sxs-lookup"><span data-stu-id="09c37-118">You can then select to post the invoice.</span></span>
-   <span data-ttu-id="09c37-119">Labot rēķina summu uz prognozējamo summu un grāmatot šo rēķinu.</span><span class="sxs-lookup"><span data-stu-id="09c37-119">Revise the invoice amount to the expected amount, and post the invoice.</span></span>
-   <span data-ttu-id="09c37-120">Pieprasīt no kreditora visu kredītu un jaunu, labotu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="09c37-120">Request a full credit and a new, corrected invoice from the vendor.</span></span>

<span data-ttu-id="09c37-121">Plašāku informāciju skatiet šeit: [Izpēte/izņēmumu novēršana](tasks/research-resolve-exceptions.md).</span><span class="sxs-lookup"><span data-stu-id="09c37-121">For more information, see [Research or resolve exceptions](tasks/research-resolve-exceptions.md).</span></span>


