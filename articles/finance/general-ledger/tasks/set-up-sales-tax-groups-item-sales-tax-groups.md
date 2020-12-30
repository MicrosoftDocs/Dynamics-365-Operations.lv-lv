---
title: PVN grupu un krājumu PVN grupu iestatīšana
description: Šajā uzdevuma ierakstā parādīts, kā iestatīt PVN un Krājumu PVN grupas.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24210129f7595c6544234c20915f4003bf0e1eb8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445440"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="99d25-103">PVN grupu un krājumu PVN grupu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="99d25-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99d25-104">Šajā uzdevuma ierakstā parādīts, kā iestatīt PVN un Krājumu PVN grupas.</span><span class="sxs-lookup"><span data-stu-id="99d25-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="99d25-105">PVN grupas ir PVN kodu grupas, kas piesaistītas debitoriem un kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="99d25-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="99d25-106">Tās tiek arī pievienotas Virsgrāmatas kontiem transakcijām, kas nav iegrāmatotas konkrētam kreditoram vai debitoram.</span><span class="sxs-lookup"><span data-stu-id="99d25-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="99d25-107">Krājumu PVN grupas ir PVN kodu grupas, kas piesaistītas tādiem resursiem kā produkti.</span><span class="sxs-lookup"><span data-stu-id="99d25-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="99d25-108">Uz konkrētu transakciju attiecināmie PVN tiek noteikti pēc PVN kodiem, kas ietverti gan PVN grupā, gan transakcijas krājumu PVN grupā.</span><span class="sxs-lookup"><span data-stu-id="99d25-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="99d25-109">PVN var tikt aprēķināts tikai tad, ja PVN grupa un krājuma PVN grupa ir atlasītas katrai transakcijai, kurai jāaprēķina vai jāreģistrē PVN.</span><span class="sxs-lookup"><span data-stu-id="99d25-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="99d25-110">Pārejiet uz **Navigācijas rūts > Moduļi >Nodokļi > Netiešie nodokļi > PVN > PVN grupas**.</span><span class="sxs-lookup"><span data-stu-id="99d25-110">Go to **Navigation pane > Modules > Tax > Indirect taxes > Sales tax > Sales tax groups**.</span></span>
2. <span data-ttu-id="99d25-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="99d25-111">Click **New**.</span></span>
3. <span data-ttu-id="99d25-112">Ierakstiet vērtību laukā **PVN grupa**.</span><span class="sxs-lookup"><span data-stu-id="99d25-112">In the **Sales tax group** field, type a value.</span></span>
4. <span data-ttu-id="99d25-113">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="99d25-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="99d25-114">Pārslēdziet sadaļas **Iestatīšana** paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="99d25-114">Toggle the expansion of the **Setup** section.</span></span>
6. <span data-ttu-id="99d25-115">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="99d25-115">Click **Add**.</span></span>
7. <span data-ttu-id="99d25-116">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="99d25-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="99d25-117">Laukā **PVN kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="99d25-117">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="99d25-118">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="99d25-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="99d25-119">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="99d25-119">Click **Save**.</span></span>
11. <span data-ttu-id="99d25-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="99d25-120">Close the page.</span></span>
12. <span data-ttu-id="99d25-121">Dodieties uz **Nodokļi > Netiešie nodokļi > PVN > Krājuma PVN grupas**.</span><span class="sxs-lookup"><span data-stu-id="99d25-121">Go to **Tax > Indirect taxes > Sales tax > Item sales tax groups**.</span></span>
13. <span data-ttu-id="99d25-122">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="99d25-122">Click **New**.</span></span>
14. <span data-ttu-id="99d25-123">Ierakstiet vērtību laukā **Krājuma PVN grupa**.</span><span class="sxs-lookup"><span data-stu-id="99d25-123">In the **Item sales tax group** field, type a value.</span></span>
15. <span data-ttu-id="99d25-124">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="99d25-124">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="99d25-125">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="99d25-125">Click **Add**.</span></span>
17. <span data-ttu-id="99d25-126">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="99d25-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="99d25-127">Laukā **PVN kods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="99d25-127">In the **Sales tax code** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="99d25-128">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="99d25-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="99d25-129">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="99d25-129">Click **Save**.</span></span>

