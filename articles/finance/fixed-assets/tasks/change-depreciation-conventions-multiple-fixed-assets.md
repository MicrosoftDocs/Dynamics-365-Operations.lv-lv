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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c64e4f7117c4ca70236a02b4d36a88e9f2a9906
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210027"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="17a1f-103">Nolietojuma konvenciju maiņa vairākiem pamatlīdzekļiem</span><span class="sxs-lookup"><span data-stu-id="17a1f-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17a1f-104">Šis uzdevums atjaunina nolietojuma nosacījumus noteiktai pamatlīdzekļu grupai.</span><span class="sxs-lookup"><span data-stu-id="17a1f-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="17a1f-105">Šis uzdevuma ceļvedis izmanto USMF demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="17a1f-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="17a1f-106">Pārejiet uz sadaļu Pamatlīdzekļi > Periodiskie uzdevumi > Masveida atjaunināšana.</span><span class="sxs-lookup"><span data-stu-id="17a1f-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="17a1f-107">Laukā Nolietojuma grāmata noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="17a1f-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="17a1f-108">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="17a1f-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="17a1f-109">Ievadiet datumu laukā Datums, kad sākta lietošana.</span><span class="sxs-lookup"><span data-stu-id="17a1f-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="17a1f-110">Laukā Datums, kad beigta lietošana, ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="17a1f-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="17a1f-111">Tiks atjaunināti tikai tie pamatlīdzekļi, kas ir izvēlētajā nolietojuma grāmatā un kas ir nodoti lietošanai šo datumu intervālā.</span><span class="sxs-lookup"><span data-stu-id="17a1f-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="17a1f-112">Atlasiet opciju laukā Pašreizējā nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="17a1f-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="17a1f-113">Tiks atjaunināti tikai tie pamatlīdzekļi, kuriem ir pašreizējā nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="17a1f-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="17a1f-114">Atlasiet opciju laukā Jauna nolietojuma aprēķināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="17a1f-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="17a1f-115">Pārbaudiet, vai pārskats tiks izdrukāts vēlamajā vietā.</span><span class="sxs-lookup"><span data-stu-id="17a1f-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="17a1f-116">Izvērsiet sadaļu Iekļaujamie ieraksti.</span><span class="sxs-lookup"><span data-stu-id="17a1f-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="17a1f-117">Noklikšķiniet uz Filtrēt.</span><span class="sxs-lookup"><span data-stu-id="17a1f-117">Click Filter.</span></span>
10. <span data-ttu-id="17a1f-118">Sarakstā atlasiet pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="17a1f-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="17a1f-119">Laukā Kritēriji noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="17a1f-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="17a1f-120">Atlasiet vēlamo pamatlīdzekļu grupu.</span><span class="sxs-lookup"><span data-stu-id="17a1f-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="17a1f-121">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="17a1f-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="17a1f-122">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="17a1f-122">Click OK.</span></span>
15. <span data-ttu-id="17a1f-123">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="17a1f-123">Click OK.</span></span>
    *  <span data-ttu-id="17a1f-124">Procesa rezultāti tiek attēloti masveida atjaunināšana pārskatā.</span><span class="sxs-lookup"><span data-stu-id="17a1f-124">Results of the process are shown on the Mass update report.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]