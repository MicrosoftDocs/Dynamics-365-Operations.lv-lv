---
title: Iestatīt PVN kodus
description: PVN kodi tiek veidoti katram netiešajam nodoklim vai nodevai, kas juridiskajai personai obligāti jāaprēķina, jāapkopo un jāmaksā PVN iestādēm.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f29442c2ef2e3d0008a74298fda218e4cbd93f8e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571587"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="f4c94-103">Iestatīt PVN kodus</span><span class="sxs-lookup"><span data-stu-id="f4c94-103">Set up sales tax codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4c94-104">PVN kodi tiek veidoti katram netiešajam nodoklim vai nodevai, kas juridiskajai personai obligāti jāaprēķina, jāapkopo un jāmaksā PVN iestādēm.</span><span class="sxs-lookup"><span data-stu-id="f4c94-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="f4c94-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="f4c94-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="f4c94-106">Pārejiet uz sadaļu Nodokļi > Netiešie nodokļi > PVN > PVN kodi.</span><span class="sxs-lookup"><span data-stu-id="f4c94-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="f4c94-107">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="f4c94-107">Click New.</span></span>
3. <span data-ttu-id="f4c94-108">Ierakstiet vērtību laukā PVN kods.</span><span class="sxs-lookup"><span data-stu-id="f4c94-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="f4c94-109">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="f4c94-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f4c94-110">Atlasiet Maksājumu periodu, lai norādītu, kurai PVN iestādei un kādos laika intervālos par šo PVN jāziņo un tas jānomaksā.</span><span class="sxs-lookup"><span data-stu-id="f4c94-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="f4c94-111">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f4c94-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f4c94-112">Lai norādītu galveno kontu PVN grāmatošanai Virsgrāmatā, atlasiet Virsgrāmatas grāmatošanas grupu.</span><span class="sxs-lookup"><span data-stu-id="f4c94-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="f4c94-113">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f4c94-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="f4c94-114">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f4c94-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f4c94-115">Izvērsiet kopsavilkuma cilni Aprēķins.</span><span class="sxs-lookup"><span data-stu-id="f4c94-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="f4c94-116">Aprēķina kopsavilkuma cilnē ir vairāki lauki, kas kontrolē, kā tiks aprēķinātas PVN summas.</span><span class="sxs-lookup"><span data-stu-id="f4c94-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="f4c94-117">Darbības rūtī noklikšķiniet uz vienuma PVN kods.</span><span class="sxs-lookup"><span data-stu-id="f4c94-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="f4c94-118">Noklikšķiniet uz vienuma Vērtības.</span><span class="sxs-lookup"><span data-stu-id="f4c94-118">Click Values.</span></span>
13. <span data-ttu-id="f4c94-119">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="f4c94-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f4c94-120">Ievadiet šī nodokļa koda vērtību.</span><span class="sxs-lookup"><span data-stu-id="f4c94-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="f4c94-121">Ja Aprēķina kopsavilkuma cilnes laukā Izcelsme ir atlasīta Summa uz vienu vienību, PVN summas rēķināšanai vērtība tiks reizināta ar transakcijā norādīto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f4c94-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="f4c94-122">Ja nodokļa kods neatbilst uz vienībām balstītam nodoklim, PVN summas vērtība tiek aprēķināta kā procenti no šī nodokļu koda Izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="f4c94-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="f4c94-123">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f4c94-123">Click Save.</span></span>
16. <span data-ttu-id="f4c94-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="f4c94-124">Close the page.</span></span>
17. <span data-ttu-id="f4c94-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f4c94-125">Click Save.</span></span>

