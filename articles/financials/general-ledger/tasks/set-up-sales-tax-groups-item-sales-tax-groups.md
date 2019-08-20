---
title: PVN grupu un krājumu PVN grupu iestatīšana
description: Šajā uzdevuma ierakstā parādīts, kā iestatīt PVN un Krājumu PVN grupas.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c58755be2c927de1d308576a2bff2ed3340db34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846275"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="6cd39-103">PVN grupu un krājumu PVN grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6cd39-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6cd39-104">Šajā uzdevuma ierakstā parādīts, kā iestatīt PVN un Krājumu PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="6cd39-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="6cd39-105">PVN grupas ir PVN kodu grupas, kas piesaistītas debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="6cd39-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="6cd39-106">Tās tiek arī pievienotas Virsgrāmatas kontiem transakcijām, kas nav iegrāmatotas konkrētam kreditoram vai debitoram.</span><span class="sxs-lookup"><span data-stu-id="6cd39-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="6cd39-107">Krājumu PVN grupas ir PVN kodu grupas, kas piesaistītas tādiem resursiem kā produkti.</span><span class="sxs-lookup"><span data-stu-id="6cd39-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="6cd39-108">Uz konkrētu transakciju attiecināmie PVN tiek noteikti pēc PVN kodiem, kas ietverti gan PVN grupā, gan transakcijas krājumu PVN grupā.</span><span class="sxs-lookup"><span data-stu-id="6cd39-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="6cd39-109">PVN var tikt aprēķināts tikai tad, ja PVN grupa un krājuma PVN grupa ir atlasītas katrai transakcijai, kurai jāaprēķina vai jāreģistrē PVN.</span><span class="sxs-lookup"><span data-stu-id="6cd39-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="6cd39-110">Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Pārdošanas nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="6cd39-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="6cd39-111">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6cd39-111">Click New.</span></span>
3. <span data-ttu-id="6cd39-112">Ierakstiet vērtību laukā PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="6cd39-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="6cd39-113">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6cd39-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6cd39-114">Pārslēdziet sadaļas Iestatīšana paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="6cd39-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="6cd39-115">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="6cd39-115">Click Add.</span></span>
7. <span data-ttu-id="6cd39-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6cd39-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="6cd39-117">Laukā PVN kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6cd39-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6cd39-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6cd39-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6cd39-119">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6cd39-119">Click Save.</span></span>
11. <span data-ttu-id="6cd39-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="6cd39-120">Close the page.</span></span>
12. <span data-ttu-id="6cd39-121">Dodieties uz Nodokļi > Netiešie nodokļi > Pārdošanas nodoklis > Krājumu pārdošanas nodokļa grupas.</span><span class="sxs-lookup"><span data-stu-id="6cd39-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="6cd39-122">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="6cd39-122">Click New.</span></span>
14. <span data-ttu-id="6cd39-123">Ierakstiet vērtību laukā Krājumu PVN grupa.</span><span class="sxs-lookup"><span data-stu-id="6cd39-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="6cd39-124">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="6cd39-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="6cd39-125">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="6cd39-125">Click Add.</span></span>
17. <span data-ttu-id="6cd39-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="6cd39-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="6cd39-127">Laukā PVN kods noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="6cd39-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="6cd39-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="6cd39-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="6cd39-129">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="6cd39-129">Click Save.</span></span>

