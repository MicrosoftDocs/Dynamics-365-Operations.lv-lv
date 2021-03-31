---
title: Nolietojuma grāmatu iestatīšana
description: Šajā procedūrā izklāstīts jaunas nolietojuma grāmatas izveides process un tās saistīšana ar pamatlīdzekļu grupu.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd65cb77872b3e2f74402cf8c92c8b8989cea6ee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224697"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="9552c-103">Nolietojuma grāmatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9552c-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9552c-104">Šajā procedūrā izklāstīts jaunas nolietojuma grāmatas izveides process un tās saistīšana ar pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="9552c-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="9552c-105">Nolietojuma grāmatas izveide</span><span class="sxs-lookup"><span data-stu-id="9552c-105">Create a depreciation book</span></span>
1. <span data-ttu-id="9552c-106">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Nolietojuma grāmatas.</span><span class="sxs-lookup"><span data-stu-id="9552c-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="9552c-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9552c-107">Click New.</span></span>
3. <span data-ttu-id="9552c-108">Ievadiet vērtību laukā Nolietojuma grāmata.</span><span class="sxs-lookup"><span data-stu-id="9552c-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="9552c-109">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9552c-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9552c-110">Atzīmējiet izvēles rūtiņu Aprēķināt nolietojumu vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="9552c-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="9552c-111">Laukā Nolietojuma metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9552c-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9552c-112">Sarakstā atrodiet un atlasiet vajadzīgo nolietojuma metodi.</span><span class="sxs-lookup"><span data-stu-id="9552c-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="9552c-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9552c-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9552c-114">Laukā Alternatīvā nolietojuma metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9552c-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="9552c-115">Sarakstā atlasiet vajadzīgo nolietojuma metodi.</span><span class="sxs-lookup"><span data-stu-id="9552c-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="9552c-116">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9552c-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9552c-117">Ārkārtas nolietojuma metode tiem izmantota līdzekļa papildu nolietošanai neparastos apstākļos.</span><span class="sxs-lookup"><span data-stu-id="9552c-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="9552c-118">Piemēram, šo opciju varat izmantot, lai reģistrētu nolietojumu, ko izraisa dabas katastrofas.</span><span class="sxs-lookup"><span data-stu-id="9552c-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="9552c-119">Atzīmējiet izvēles rūtiņu Izveidot nolietojuma korekcijas ar pamata pielāgojumiem vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="9552c-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="9552c-120">Laukā Kalendārs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9552c-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="9552c-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9552c-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="9552c-122">Nolietojuma grāmatas sasaiste ar pamatlīdzekļu grupu</span><span class="sxs-lookup"><span data-stu-id="9552c-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="9552c-123">Noklikšķiniet uz Pamatlīdzekļu grupas.</span><span class="sxs-lookup"><span data-stu-id="9552c-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="9552c-124">Laukā Pamatlīdzekļa grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="9552c-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9552c-125">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9552c-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="9552c-126">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="9552c-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9552c-127">Atlasiet opciju laukā Nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="9552c-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="9552c-128">Ievadiet skaitli laukā Lietošanas ilgums.</span><span class="sxs-lookup"><span data-stu-id="9552c-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="9552c-129">Ņemiet vērā, ka lauka Nolietojuma periodi vērtība tiek aprēķināta pēc vērtības Lietošanas ilgums iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="9552c-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]