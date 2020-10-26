---
title: PVN kodu iestatīšana
description: Šajā tēmā paskaidrots, kā iestatīt pasūtījumu aizturēšanas kodus programmā Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3dad006b486f7cd6714c713a3bd83a95fdf0d2b5
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979642"
---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="9fb11-103">PVN kodu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9fb11-103">Set up sales tax codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fb11-104">Šajā tēmā paskaidrots, kā iestatīt pasūtījumu aizturēšanas kodus.</span><span class="sxs-lookup"><span data-stu-id="9fb11-104">This topic explains how to set up sales tax codes.</span></span> <span data-ttu-id="9fb11-105">PVN kodi tiek veidoti katram netiešajam nodoklim vai nodevai, kas juridiskajai personai obligāti jāaprēķina, jāapkopo un jāmaksā PVN iestādēm.</span><span class="sxs-lookup"><span data-stu-id="9fb11-105">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="9fb11-106">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="9fb11-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="9fb11-107">Pārejiet uz **Navigācijas rūts > Nodokļi > Netiešie nodokļi > PVN > PVN kodi**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-107">Go to **Navigation pane > Tax > Indirect taxes > Sales tax > Sales tax codes**.</span></span>
2. <span data-ttu-id="9fb11-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-108">Select **New**.</span></span>
3. <span data-ttu-id="9fb11-109">Ierakstiet vērtību laukā **PVN kods**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-109">In the **Sales tax code** field, type a value.</span></span>
4. <span data-ttu-id="9fb11-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9fb11-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9fb11-111">Atlasiet **Maksājumu periodu**, atverot nolaižamo sarakstu, lai norādītu, kurai PVN iestādei un kādos laika intervālos par šo PVN jāziņo un tas jānomaksā.</span><span class="sxs-lookup"><span data-stu-id="9fb11-111">Select a **Settlement period** by opening the pull-down list to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="9fb11-112">Lai norādītu galveno kontu PVN grāmatošanai Virsgrāmatā, atlasiet **Virsgrāmatas grāmatošanas grupu**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-112">Select a **Ledger posting group** to specify the main accounts to post sales tax to the general ledger.</span></span>
7. <span data-ttu-id="9fb11-113">Izvērsiet kopsavilkuma cilni **Aprēķins**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-113">Expand the **Calculation** FastTab.</span></span> <span data-ttu-id="9fb11-114">Tas ietver vairākus laukus, kas kontrolē, kā tiks aprēķinātas PVN summas.</span><span class="sxs-lookup"><span data-stu-id="9fb11-114">This includes multiple fields that control how sales tax amounts will be calculated.</span></span> <span data-ttu-id="9fb11-115">Aizpildiet šos laukus pēc vajadzības.</span><span class="sxs-lookup"><span data-stu-id="9fb11-115">Fill these fields out as needed.</span></span>  
8. <span data-ttu-id="9fb11-116">**Darbību rūtī**, kas atrodas interfeisa augšdaļā, atlasiet **PVN kods**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-116">On the **Action Pane** at the top of the interface, select **Sales tax code**.</span></span>
9. <span data-ttu-id="9fb11-117">Atlasiet **Vērtības**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-117">Select **Values**.</span></span>
10. <span data-ttu-id="9fb11-118">Ievadiet šī nodokļa koda vērtību kolonnā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-118">Enter the value for this tax code in the **value** column.</span></span>
    - <span data-ttu-id="9fb11-119">Kopsavilkuma cilnes **Aprēķins** laukā Izcelsme ir atlasīta Summa uz vienu vienību, PVN summas rēķināšanai vērtība tiks reizināta ar transakcijā norādīto daudzumu.</span><span class="sxs-lookup"><span data-stu-id="9fb11-119">On the **Calculation** FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="9fb11-120">Ja nodokļa kods neatbilst uz vienībām balstītam nodoklim, PVN summas vērtība tiek aprēķināta kā procenti no šī nodokļu koda Izcelsmes.</span><span class="sxs-lookup"><span data-stu-id="9fb11-120">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
11. <span data-ttu-id="9fb11-121">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-121">Select **Save**.</span></span>
12. <span data-ttu-id="9fb11-122">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="9fb11-122">Close the page.</span></span>
13. <span data-ttu-id="9fb11-123">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="9fb11-123">Select **Save**.</span></span>

