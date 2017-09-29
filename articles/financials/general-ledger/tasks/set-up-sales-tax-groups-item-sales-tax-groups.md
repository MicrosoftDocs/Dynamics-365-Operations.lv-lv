--- 
title: "PVN grupu un krājumu PVN grupu iestatīšana"
description: "Šajā uzdevuma ierakstā parādīts, kā iestatīt PVN un Krājumu PVN grupas."
author: twheeloc
manager: AnnBe
ms.date: 11/10/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4d7f1093edcfff65fd466fa8138b1bb5203648b3
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="43573-103">PVN grupu un krājumu PVN grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="43573-103">Set up sales tax groups and item sales tax groups</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43573-104">Šajā uzdevuma ierakstā parādīts, kā iestatīt PVN un Krājumu PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="43573-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="43573-105">PVN grupas ir PVN kodu grupas, kas piesaistītas debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="43573-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="43573-106">Tās tiek arī pievienotas Virsgrāmatas kontiem transakcijām, kas nav iegrāmatotas konkrētam kreditoram vai debitoram.</span><span class="sxs-lookup"><span data-stu-id="43573-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="43573-107">Krājumu PVN grupas ir PVN kodu grupas, kas piesaistītas tādiem resursiem kā produkti.</span><span class="sxs-lookup"><span data-stu-id="43573-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="43573-108">Uz konkrētu transakciju attiecināmie PVN tiek noteikti pēc PVN kodiem, kas ietverti gan PVN grupā, gan transakcijas krājumu PVN grupā.</span><span class="sxs-lookup"><span data-stu-id="43573-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="43573-109">PVN var tikt aprēķināts tikai tad, ja PVN grupa un krājuma PVN grupa ir atlasītas katrai transakcijai, kurai jāaprēķina vai jāreģistrē PVN.</span><span class="sxs-lookup"><span data-stu-id="43573-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="43573-110">Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Pārdošanas nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="43573-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="43573-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="43573-111">Click New.</span></span>
3. <span data-ttu-id="43573-112">Ierakstiet vērtību laukā PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="43573-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="43573-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="43573-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="43573-114">Pārslēdziet sadaļas Iestatīšana paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="43573-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="43573-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="43573-115">Click Add.</span></span>
7. <span data-ttu-id="43573-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="43573-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="43573-117">Laukā PVN kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43573-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="43573-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="43573-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="43573-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="43573-119">Click Save.</span></span>
11. <span data-ttu-id="43573-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="43573-120">Close the page.</span></span>
12. <span data-ttu-id="43573-121">Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Krājumu pārdošanas nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="43573-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="43573-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="43573-122">Click New.</span></span>
14. <span data-ttu-id="43573-123">Ierakstiet vērtību laukā Krājumu PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="43573-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="43573-124">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="43573-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="43573-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="43573-125">Click Add.</span></span>
17. <span data-ttu-id="43573-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="43573-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="43573-127">Laukā PVN kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="43573-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="43573-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="43573-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="43573-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="43573-129">Click Save.</span></span>


