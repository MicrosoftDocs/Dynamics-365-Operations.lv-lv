---
title: Nolietojuma grāmatu iestatīšana (2016. gada maijs)
description: Šajā uzdevuma ceļvedī parādīts, kā izveidot jaunu nolietojuma grāmatu un sasaistīt to ar pamatlīdzekļu grupu.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6840e211847494598a81cd3228dbd3796447e18c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186904"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="f1133-103">Nolietojuma grāmatu iestatīšana (2016. gada maijs)</span><span class="sxs-lookup"><span data-stu-id="f1133-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1133-104">Šajā uzdevuma ceļvedī parādīts, kā izveidot jaunu nolietojuma grāmatu un sasaistīt to ar pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="f1133-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="f1133-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="f1133-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="f1133-106">Nolietojuma grāmatas izveide</span><span class="sxs-lookup"><span data-stu-id="f1133-106">Create a depreciation book</span></span>
1. <span data-ttu-id="f1133-107">Pārejiet uz sadaļu Pamatlīdzekļi > Iestatījumi > Nolietojuma grāmatas.</span><span class="sxs-lookup"><span data-stu-id="f1133-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="f1133-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f1133-108">Click New.</span></span>
3. <span data-ttu-id="f1133-109">Ievadiet vērtību laukā Nolietojuma grāmata.</span><span class="sxs-lookup"><span data-stu-id="f1133-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="f1133-110">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="f1133-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f1133-111">Atzīmējiet izvēles rūtiņu Aprēķināt nolietojumu vai noņemiet tās atzīmi.</span><span class="sxs-lookup"><span data-stu-id="f1133-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="f1133-112">Laukā Nolietojuma metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f1133-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f1133-113">Sarakstā atrodiet un atlasiet vajadzīgo nolietojuma metodi.</span><span class="sxs-lookup"><span data-stu-id="f1133-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="f1133-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1133-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f1133-115">Laukā Alternatīvā nolietojuma metode noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f1133-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f1133-116">Sarakstā atlasiet vajadzīgo nolietojuma metodi.</span><span class="sxs-lookup"><span data-stu-id="f1133-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="f1133-117">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1133-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f1133-118">Ārkārtas nolietojuma metode tiem izmantota līdzekļa papildu nolietošanai neparastos apstākļos.</span><span class="sxs-lookup"><span data-stu-id="f1133-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="f1133-119">Piemēram, šo opciju varat izmantot, lai reģistrētu nolietojumu, ko izraisa dabas katastrofas.</span><span class="sxs-lookup"><span data-stu-id="f1133-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="f1133-120">Atzīmējiet izvēles rūtiņu Izveidot nolietojuma korekcijas ar pamata pielāgojumiem vai noņemiet atzīmi no tās.</span><span class="sxs-lookup"><span data-stu-id="f1133-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="f1133-121">Laukā Kalendārs noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f1133-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f1133-122">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1133-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="f1133-123">Nolietojuma grāmatas sasaiste ar pamatlīdzekļu grupu</span><span class="sxs-lookup"><span data-stu-id="f1133-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="f1133-124">Noklikšķiniet uz Pamatlīdzekļu grupas.</span><span class="sxs-lookup"><span data-stu-id="f1133-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="f1133-125">Laukā Pamatlīdzekļa grupa noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="f1133-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f1133-126">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f1133-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f1133-127">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f1133-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f1133-128">Atlasiet opciju laukā Nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="f1133-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="f1133-129">Ievadiet skaitli laukā Lietošanas ilgums.</span><span class="sxs-lookup"><span data-stu-id="f1133-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="f1133-130">Ņemiet vērā, ka lauka Nolietojuma periodi vērtība tiek aprēķināta pēc vērtības Lietošanas ilgums iestatīšanas.</span><span class="sxs-lookup"><span data-stu-id="f1133-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

