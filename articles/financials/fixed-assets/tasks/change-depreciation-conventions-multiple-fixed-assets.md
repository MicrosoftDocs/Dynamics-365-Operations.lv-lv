---
title: Nolietojuma konvenciju maiņa vairākiem pamatlīdzekļiem
description: Šis uzdevums atjaunina nolietojuma nosacījumus noteiktai pamatlīdzekļu grupai.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a79b2edf64f0063253d3f2a23b0020eceb87c0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561503"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="692c6-103">Nolietojuma konvenciju maiņa vairākiem pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="692c6-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="692c6-104">Šis uzdevums atjaunina nolietojuma nosacījumus noteiktai pamatlīdzekļu grupai.</span><span class="sxs-lookup"><span data-stu-id="692c6-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="692c6-105">Šis uzdevuma ceļvedis izmanto USMF demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="692c6-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="692c6-106">Pārejiet uz sadaļu Pamatlīdzekļi > Periodiskie uzdevumi > Masveida atjaunināšana.</span><span class="sxs-lookup"><span data-stu-id="692c6-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="692c6-107">Laukā Nolietojuma grāmata noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="692c6-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="692c6-108">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="692c6-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="692c6-109">Ievadiet datumu laukā Datums, kad sākta lietošana.</span><span class="sxs-lookup"><span data-stu-id="692c6-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="692c6-110">Laukā Datums, kad beigta lietošana, ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="692c6-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="692c6-111">Tiks atjaunināti tikai tie pamatlīdzekļi, kas ir izvēlētajā nolietojuma grāmatā un kas ir nodoti lietošanai šo datumu intervālā.</span><span class="sxs-lookup"><span data-stu-id="692c6-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="692c6-112">Atlasiet opciju laukā Pašreizējā nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="692c6-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="692c6-113">Tiks atjaunināti tikai tie pamatlīdzekļi, kuriem ir pašreizējā nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="692c6-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="692c6-114">Atlasiet opciju laukā Jauna nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="692c6-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="692c6-115">Pārbaudiet, vai pārskats tiks izdrukāts vēlamajā vietā.</span><span class="sxs-lookup"><span data-stu-id="692c6-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="692c6-116">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="692c6-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="692c6-117">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="692c6-117">Click Filter.</span></span>
10. <span data-ttu-id="692c6-118">Sarakstā atlasiet pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="692c6-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="692c6-119">Laukā Kritēriji noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="692c6-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="692c6-120">Atlasiet vēlamo pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="692c6-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="692c6-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="692c6-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="692c6-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="692c6-122">Click OK.</span></span>
15. <span data-ttu-id="692c6-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="692c6-123">Click OK.</span></span>
    *  <span data-ttu-id="692c6-124">Procesa rezultāti tiek attēloti masveida atjaunināšana pārskatā.</span><span class="sxs-lookup"><span data-stu-id="692c6-124">Results of the process are shown on the Mass update report.</span></span>     

