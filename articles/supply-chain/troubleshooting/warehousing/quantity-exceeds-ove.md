---
title: Nevar apstiprināt kravu, jo daudzums pārsniedz pasūtījuma pārsniegīšanas procentus
description: Nevar apstiprināt kravu, jo daudzums pārsniedz pasūtījuma pārsniegīšanas procentus
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938514"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="78e33-103">Nevar apstiprināt kravu, jo daudzums pārsniedz pasūtījuma pārsniegīšanas procentus</span><span class="sxs-lookup"><span data-stu-id="78e33-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="78e33-104">Kļūdas kods: WAX1687</span><span class="sxs-lookup"><span data-stu-id="78e33-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="78e33-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="78e33-105">Symptoms</span></span>

<span data-ttu-id="78e33-106">Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="78e33-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="78e33-107">Kravas nosūtīšanu %1 nevarēja apstiprināt, jo krājuma %2 daudzums pārsniedz pasūtījumam noteikto procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="78e33-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="78e33-108">Tādēļ kravas nosūtīšanu nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="78e33-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="78e33-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="78e33-109">Cause</span></span>

<span data-ttu-id="78e33-110">Kravas vai sūtījuma daudzums ir tikai daļēji izdots.</span><span class="sxs-lookup"><span data-stu-id="78e33-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="78e33-111">Daudzums pašlaik pārsniedz izdoto daudzumu par procentiem, kas ir ārpus atļautajiem pārsniegšanas procentiem.</span><span class="sxs-lookup"><span data-stu-id="78e33-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="78e33-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="78e33-112">Resolution</span></span>

<span data-ttu-id="78e33-113">Lai risināt šo problēmu, izpildiet vienu no tālāk norādītajiem uzdevumiem.</span><span class="sxs-lookup"><span data-stu-id="78e33-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="78e33-114">Iestatiet krāvas rindu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="78e33-114">Set the load line quantity.</span></span>
- <span data-ttu-id="78e33-115">Iestatiet pārsnieguma procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="78e33-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="78e33-116">Iestatiet krāvas rindu daudzumu</span><span class="sxs-lookup"><span data-stu-id="78e33-116">Set the load line quantity</span></span>

<span data-ttu-id="78e33-117">Lai uzstādītu kravas rindu daudzumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="78e33-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="78e33-118">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="78e33-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="78e33-119">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="78e33-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="78e33-120">Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentus.</span><span class="sxs-lookup"><span data-stu-id="78e33-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="78e33-121">Kopsavilkuma cilnē **Rindu detāļas** atlasiet **Pasūtījums**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="78e33-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="78e33-122">Laukā **Daudzums** iestatiet vērtību uz izdoto daudzumu (t.i., uz **Darba izveidotā daudzuma** vērtību), lai varētu notikt nosūtīšanas apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="78e33-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="78e33-123">Iestatiet pārsnieguma procentuālo vērtību</span><span class="sxs-lookup"><span data-stu-id="78e33-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="78e33-124">Lai uzstādītu nepilnu pasūtījumu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="78e33-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="78e33-125">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="78e33-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="78e33-126">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="78e33-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="78e33-127">Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz pasūtījuma pārsnieguma procentus.</span><span class="sxs-lookup"><span data-stu-id="78e33-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="78e33-128">Kopsavilkuma cilnē **Rindu detāļas** atlasiet **Vispārīgi**, lai pievienotu rindu.</span><span class="sxs-lookup"><span data-stu-id="78e33-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="78e33-129">Laukā **Pasūtījuma pārsniegšana** iestatiet lielāku procentuālo vērtību, kas atbilst izdotajam daudzumam attiecībā pret kravas daudzumu, lai varētu tikt veikta kravas apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="78e33-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
