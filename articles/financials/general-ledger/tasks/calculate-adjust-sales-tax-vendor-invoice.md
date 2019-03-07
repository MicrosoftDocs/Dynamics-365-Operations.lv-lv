---
title: PVN aprēķināšana un koriģēšana kreditora rēķinā
description: Ja sākotnējā pirmdokumentā ir parādīta atšķirīga nodokļu summa, nekā aprēķināts, pirms grāmatošanas šīs summas varat pielāgot.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "308924"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="f0a2e-103">PVN aprēķināšana un koriģēšana kreditora rēķinā</span><span class="sxs-lookup"><span data-stu-id="f0a2e-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0a2e-104">Ja sākotnējā pirmdokumentā ir parādīta atšķirīga nodokļu summa, nekā aprēķināts, pirms grāmatošanas šīs summas varat pielāgot.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="f0a2e-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums DEMF.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="f0a2e-106">Pārejiet uz sadaļu Kreditori > Rēķini > Rēķinu žurnāls.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="f0a2e-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-107">Click New.</span></span>
3. <span data-ttu-id="f0a2e-108">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f0a2e-109">Laukā Nosaukums noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f0a2e-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f0a2e-111">Noklikšķiniet uz Rindas.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-111">Click Lines.</span></span>
7. <span data-ttu-id="f0a2e-112">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="f0a2e-113">Laukā Konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="f0a2e-114">Laukā Rēķins ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="f0a2e-115">Laukā Kredīts ievadiet kādu skaitli.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="f0a2e-116">Laukā Korespondējošais konts norādiet vēlamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="f0a2e-117">Noklikšķiniet uz PVN.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-117">Click Sales tax.</span></span>
13. <span data-ttu-id="f0a2e-118">Ievadiet skaitli laukā Reālā PVN kopsumma.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="f0a2e-119">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-119">Click OK.</span></span>
15. <span data-ttu-id="f0a2e-120">Klikšķiniet Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-120">Click Save.</span></span>
16. <span data-ttu-id="f0a2e-121">Noklikšķiniet uz Pārdošanas nodoklis.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-121">Click Sales tax.</span></span>
17. <span data-ttu-id="f0a2e-122">PVN summas katram PVN kodam iespējams koriģēt cilnē Korekcija.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="f0a2e-123">Noklikšķiniet uz Atiestatīt faktiskās izmaksas no aprēķinātajām.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="f0a2e-124">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-124">Click OK.</span></span>
20. <span data-ttu-id="f0a2e-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f0a2e-125">Click Save.</span></span>

