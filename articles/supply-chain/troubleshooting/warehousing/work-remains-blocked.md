---
title: Darbs paliek bloķēts
description: Darbs paliek bloķēts
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924134"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="25271-103">Darbs paliek bloķēts</span><span class="sxs-lookup"><span data-stu-id="25271-103">Work remains blocked</span></span>

<span data-ttu-id="25271-104">Kļūdas kods: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="25271-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="25271-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="25271-105">Symptoms</span></span>

<span data-ttu-id="25271-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="25271-106">The system shows the following error message:</span></span>

> <span data-ttu-id="25271-107">Darbs %1 paliek bloķēts, jo saistītajam kopumam %2 ir statuss %3.</span><span class="sxs-lookup"><span data-stu-id="25271-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="25271-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="25271-108">Cause</span></span>

<span data-ttu-id="25271-109">Darbs pašlaik tiek apstrādāts kopumā un nevar tikt bloķēts, kā norādīts vienā no šādiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="25271-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="25271-110">Cilnē **Bloķēšanas iemesli** laukā **Darba bloķēšanas iemesls** vienai vai vairākām rindām ir iestatīta opcija *Kopuma apstrāde*.</span><span class="sxs-lookup"><span data-stu-id="25271-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="25271-111">Atlasot **Kopums** grupā **Saistītā informācija** cilnē **Saistītā informācija** darbību rūtī, lauks **Kopuma statuss** ir iestatīts uz *Apstrāde*.</span><span class="sxs-lookup"><span data-stu-id="25271-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="25271-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="25271-112">Resolution</span></span>

<span data-ttu-id="25271-113">Darbību rūtī cilnē **Saistītā informācija** grupā **Saistīta informācija** atlasiet **Kopums**.</span><span class="sxs-lookup"><span data-stu-id="25271-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="25271-114">Pēc tam, lapā **Kopumi** darbības rūtī cilnē **Kopums**, grupā **Kopums** atlasiet **Attīrīšanas kopuma dati**.</span><span class="sxs-lookup"><span data-stu-id="25271-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="25271-115">Kļūdas apiešanas risinājums</span><span class="sxs-lookup"><span data-stu-id="25271-115">Workaround</span></span>

<span data-ttu-id="25271-116">Ja iepriekšējās darbības neatrisināja problēmu, darbu var atcelt, izpildot šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="25271-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="25271-117">Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="25271-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="25271-118">Laukā **Darba ID** norādiet darba ID, kuru vēlaties atcelt un kura vērtība **Darba statuss** pašlaik ir *Atvērts*, *Notiek*, *Atcelts*, *Apvienots* vai *Slēgts*.</span><span class="sxs-lookup"><span data-stu-id="25271-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="25271-119">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="25271-119">Select **OK**.</span></span>
1. <span data-ttu-id="25271-120">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="25271-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="25271-121">Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="25271-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
