---
title: Nevar apstiprināt kravu, jo daudzums ir nulle
description: Nevar apstiprināt kravu, jo daudzums ir nulle
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938510"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="f7824-103">Nevar apstiprināt kravu, jo daudzums ir nulle</span><span class="sxs-lookup"><span data-stu-id="f7824-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="f7824-104">Kļūdas kods: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="f7824-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="f7824-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="f7824-105">Symptoms</span></span>

<span data-ttu-id="f7824-106">Mēģinot apstiprināt kravu, sistēma rāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="f7824-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f7824-107">Noslodzes rinda krājumam %1 un sūtījumam %2 tika atjaunināta uz nulli nepilnas piegādes iestatījuma dēļ, kurš šim krājumam neļauj nosūtīt nekādu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="f7824-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="f7824-108">Tādēļ kravas nosūtīšanu nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="f7824-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f7824-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="f7824-109">Cause</span></span>

<span data-ttu-id="f7824-110">Sistēma novērtē, vai izdotais daudzums atbilst paredzamajiem ierobežojumiem, balstoties uz izdoto daudzumu, noslodzes rindas daudzumu un nepilnā pasūtījuma procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="f7824-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="f7824-111">Ja sistēma konstatē, ka kravas rindā izdotais daudzums ir 0 (nulle), sūtījumu nevar apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="f7824-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="f7824-112">Piemēram, šī problēma var rasties, ja darbs ir atcelts un kravas rindas nepilnā pasūtījuma procentuālā vērtība ir 100 procenti.</span><span class="sxs-lookup"><span data-stu-id="f7824-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="f7824-113">Novēršana</span><span class="sxs-lookup"><span data-stu-id="f7824-113">Resolution</span></span>

<span data-ttu-id="f7824-114">Pārbaudiet kravas rindas, lai nodrošinātu, ka nepilnā pasūtījuma procentuālā vērtība un daudzumi ir saskaņoti ar izdoto darbu.</span><span class="sxs-lookup"><span data-stu-id="f7824-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="f7824-115">Dodieties uz **Noliktavas pārvaldība \> Noslodzes \> Visas noslodzes**.</span><span class="sxs-lookup"><span data-stu-id="f7824-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f7824-116">Izvēlieties kravu, kam nevar apstiprināt nosūtījumu.</span><span class="sxs-lookup"><span data-stu-id="f7824-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f7824-117">Kopsavilkuma cilnē **Kravas rindas** atlasiet kravas rindu krājumam, kas pārsniedz nepilnā pasūtījuma procentus.</span><span class="sxs-lookup"><span data-stu-id="f7824-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="f7824-118">Pēc vajadzības koriģējiet lauka **Nepilns pasūtījums** vērtību vai lauku **Daudzums**.</span><span class="sxs-lookup"><span data-stu-id="f7824-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="f7824-119">Ja problēma vēl nav fiksēta, iespējams, būs jāpabeidz vairāk izdošanas darbu saistītajiem pārdošanas pasūtījumiem vai pārsūtīšanas pasūtījumiem, līdz pieejamais daudzums ir saskaņots ar kravu vai sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="f7824-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
