--- 
title: "Iestatīt PVN kodus"
description: "PVN kodi tiek veidoti katram netiešajam nodoklim vai nodevai, kas juridiskajai personai obligāti jāaprēķina, jāapkopo un jāmaksā PVN iestādēm."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 20033cef966a643b7735d488bc354136dc55d6b0
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="14f3f-103">Iestatīt PVN kodus</span><span class="sxs-lookup"><span data-stu-id="14f3f-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14f3f-104">PVN kodi tiek veidoti katram netiešajam nodoklim vai nodevai, kas juridiskajai personai obligāti jāaprēķina, jāapkopo un jāmaksā PVN iestādēm.</span><span class="sxs-lookup"><span data-stu-id="14f3f-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="14f3f-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="14f3f-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="14f3f-106">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > PVN > PVN kodi.</span><span class="sxs-lookup"><span data-stu-id="14f3f-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="14f3f-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="14f3f-107">Click New.</span></span>
3. <span data-ttu-id="14f3f-108">Ierakstiet vērtību laukā PVN kods.</span><span class="sxs-lookup"><span data-stu-id="14f3f-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="14f3f-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="14f3f-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="14f3f-110">Atlasiet Maksājumu periodu, lai norādītu, kurai PVN iestādei un kādos laika intervālos par šo PVN jāziņo un tas jānomaksā.</span><span class="sxs-lookup"><span data-stu-id="14f3f-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="14f3f-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="14f3f-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="14f3f-112">Lai norādītu galveno kontu PVN grāmatošanai Virsgrāmatā, atlasiet Virsgrāmatas grāmatošanas grupu.</span><span class="sxs-lookup"><span data-stu-id="14f3f-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="14f3f-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="14f3f-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="14f3f-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="14f3f-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="14f3f-115">Izvērsiet kopsavilkuma cilni Aprēķins.</span><span class="sxs-lookup"><span data-stu-id="14f3f-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="14f3f-116">Aprēķina kopsavilkuma cilnē ir vairāki lauki, kas kontrolē, kā tiks aprēķinātas PVN summas.</span><span class="sxs-lookup"><span data-stu-id="14f3f-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="14f3f-117">Darbības rūtī noklikšķiniet uz vienuma PVN kods.</span><span class="sxs-lookup"><span data-stu-id="14f3f-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="14f3f-118">Noklikšķiniet uz vienuma Vērtības.</span><span class="sxs-lookup"><span data-stu-id="14f3f-118">Click Values.</span></span>
13. <span data-ttu-id="14f3f-119">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="14f3f-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="14f3f-120">Ievadiet šī nodokļa koda vērtību.</span><span class="sxs-lookup"><span data-stu-id="14f3f-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="14f3f-121">Ja Aprēķina kopsavilkuma cilnes laukā Izcelsme ir atlasīta Summa uz vienu vienību, PVN summas rēķināšanai vērtība tiks reizināta ar transakcijā norādīto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="14f3f-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="14f3f-122">Ja nodokļa kods neatbilst uz vienībām balstītam nodoklim, PVN summas vērtība tiek aprēķināta kā procenti no šī nodokļu koda Izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="14f3f-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="14f3f-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="14f3f-123">Click Save.</span></span>
16. <span data-ttu-id="14f3f-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="14f3f-124">Close the page.</span></span>
17. <span data-ttu-id="14f3f-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="14f3f-125">Click Save.</span></span>


