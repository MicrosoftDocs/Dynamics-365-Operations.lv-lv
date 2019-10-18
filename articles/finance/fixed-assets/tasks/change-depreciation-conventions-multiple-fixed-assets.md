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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178821"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="3a6f3-103">Nolietojuma konvenciju maiņa vairākiem pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="3a6f3-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a6f3-104">Šis uzdevums atjaunina nolietojuma nosacījumus noteiktai pamatlīdzekļu grupai.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="3a6f3-105">Šis uzdevuma ceļvedis izmanto USMF demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="3a6f3-106">Pārejiet uz sadaļu Pamatlīdzekļi > Periodiskie uzdevumi > Masveida atjaunināšana.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="3a6f3-107">Laukā Nolietojuma grāmata noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3a6f3-108">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3a6f3-109">Ievadiet datumu laukā Datums, kad sākta lietošana.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="3a6f3-110">Laukā Datums, kad beigta lietošana, ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="3a6f3-111">Tiks atjaunināti tikai tie pamatlīdzekļi, kas ir izvēlētajā nolietojuma grāmatā un kas ir nodoti lietošanai šo datumu intervālā.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="3a6f3-112">Atlasiet opciju laukā Pašreizējā nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="3a6f3-113">Tiks atjaunināti tikai tie pamatlīdzekļi, kuriem ir pašreizējā nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="3a6f3-114">Atlasiet opciju laukā Jauna nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="3a6f3-115">Pārbaudiet, vai pārskats tiks izdrukāts vēlamajā vietā.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="3a6f3-116">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="3a6f3-117">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-117">Click Filter.</span></span>
10. <span data-ttu-id="3a6f3-118">Sarakstā atlasiet pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="3a6f3-119">Laukā Kritēriji noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="3a6f3-120">Atlasiet vēlamo pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="3a6f3-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3a6f3-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-122">Click OK.</span></span>
15. <span data-ttu-id="3a6f3-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-123">Click OK.</span></span>
    *  <span data-ttu-id="3a6f3-124">Procesa rezultāti tiek attēloti masveida atjaunināšana pārskatā.</span><span class="sxs-lookup"><span data-stu-id="3a6f3-124">Results of the process are shown on the Mass update report.</span></span>     

