---
title: Pamatlīdzekļa pārsūtīšana
description: Šajā uzdevuma ceļvedī ir parādīts, kā pamatlīdzekļa grāmatai pārsūtīt finanšu informāciju no vienas finanšu dimensiju kopas uz jaunu finanšu dimensiju kopu.
author: saraschi2
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7588e0058713d7facf053aa269210fc88e5a3ff2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823888"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="7f839-103">Pamatlīdzekļa pārsūtīšana</span><span class="sxs-lookup"><span data-stu-id="7f839-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f839-104">Šajā uzdevuma ceļvedī ir parādīts, kā pamatlīdzekļa grāmatai pārsūtīt finanšu informāciju no vienas finanšu dimensiju kopas uz jaunu finanšu dimensiju kopu.</span><span class="sxs-lookup"><span data-stu-id="7f839-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="7f839-105">Tas izmanto grāmatveža lomu un demonstrācijas datus USMF juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="7f839-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="7f839-106">Navigācijas rūtī pārejiet uz sadaļu **Moduļi > Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="7f839-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="7f839-107">Sarakstā atrodiet un atlasiet pārsūtāmo pamatlīdzekli.</span><span class="sxs-lookup"><span data-stu-id="7f839-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="7f839-108">Darbību rūtī noklikšķiniet uz **Pamatlīdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="7f839-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="7f839-109">Noklikšķiniet uz **Pārsūtīt pamatlīdzekļus**.</span><span class="sxs-lookup"><span data-stu-id="7f839-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="7f839-110">Ievadiet datumu laukā **Pārsūtīšanas datums**.</span><span class="sxs-lookup"><span data-stu-id="7f839-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="7f839-111">Ievadiet komentārus pārsūtīšanas aprakstam.</span><span class="sxs-lookup"><span data-stu-id="7f839-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="7f839-112">Šajā sarakstā ir redzamas visas šī pamatlīdzekļa grāmatas.</span><span class="sxs-lookup"><span data-stu-id="7f839-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="7f839-113">Atzīmējiet grāmatas, kuras vēlaties pārsūtīt uz jauno finanšu dimensijas kopu.</span><span class="sxs-lookup"><span data-stu-id="7f839-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="7f839-114">Šajā sarakstā ir redzamas atlasītajai grāmatai esošās finanšu dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="7f839-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="7f839-115">Atlasiet finanšu dimensiju, kuru vēlaties atjaunināt atlasītā pamatlīdzekļa grāmatai.</span><span class="sxs-lookup"><span data-stu-id="7f839-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="7f839-116">Laukā **Finanšu dimensija** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7f839-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="7f839-117">Attiecīgi iestatiet citas finanšu dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="7f839-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="7f839-118">Notiekot pārsūtīšanai, tiek mainītas visas finanšu dimensiju vērtības, gan ievadītajām vērtībām, gan tukšajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="7f839-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="7f839-119">Piemēram, ja ievadāt vērtību BusinessUnit, bet laukus CostCenter un Nodaļas finanšu dimensijas atstājat tukšus.</span><span class="sxs-lookup"><span data-stu-id="7f839-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="7f839-120">Ja jūsu konta struktūra pieļauj tukšas vērtības CostCenter un Nodaļa laukos, tad pēc pārsūtīšanas katram vērtības modelim būtu jauna BusinessUnit vērtība un tukša vērtība laukiem CostCenter un Nodaļa.</span><span class="sxs-lookup"><span data-stu-id="7f839-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="7f839-121">Noklikšķiniet uz **Atjaunināt**.</span><span class="sxs-lookup"><span data-stu-id="7f839-121">Click **Update**.</span></span>
    * <span data-ttu-id="7f839-122">Jums ir iespēja apskatīt izmaiņas pirms pārsūtīšanas pabeigšanas.</span><span class="sxs-lookup"><span data-stu-id="7f839-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="7f839-123">Pirms pamatlīdzekļa grāmatu pārsūtīšanas pārskatiet rezultātus.</span><span class="sxs-lookup"><span data-stu-id="7f839-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="7f839-124">Noklikšķiniet uz **Pārsūtīt**.</span><span class="sxs-lookup"><span data-stu-id="7f839-124">Click **Transfer**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]