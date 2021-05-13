---
title: Darbu nevar atcelt, jo tas ir bloķēts
description: Darbu nevar atcelt, jo tas ir bloķēts
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a7ab4c7263947767164702fb7dd6da7573175253
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924283"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a><span data-ttu-id="352da-103">Darbu nevar atcelt, jo tas ir bloķēts</span><span class="sxs-lookup"><span data-stu-id="352da-103">Work can't be canceled because it's blocked</span></span>

<span data-ttu-id="352da-104">Kļūdas kods: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="352da-104">Error code: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="352da-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="352da-105">Symptoms</span></span>

<span data-ttu-id="352da-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="352da-106">The system shows the following error message:</span></span>

> <span data-ttu-id="352da-107">Darbu %1 nevar atcelt, jo to ir bloķējis iemesla veids %2.</span><span class="sxs-lookup"><span data-stu-id="352da-107">Work %1 cannot be cancelled because it is blocked by reason type %2.</span></span> <span data-ttu-id="352da-108">Pirms darba atcelšanas tas ir jāatbloķē.</span><span class="sxs-lookup"><span data-stu-id="352da-108">The work must be unblocked before it can be cancelled.</span></span>

## <a name="cause"></a><span data-ttu-id="352da-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="352da-109">Cause</span></span>

<span data-ttu-id="352da-110">Darbs ir bloķēts, un to nevar atcelt.</span><span class="sxs-lookup"><span data-stu-id="352da-110">The work is blocked and can't be canceled.</span></span>

<span data-ttu-id="352da-111">Lapā **Darbs** cilnē **Vispārīgi** opcija **Bloķēts** ir iestatīta uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="352da-111">On the **Work** page, on the **General** tab, the **Blocked** option is set to *Yes*.</span></span> <span data-ttu-id="352da-112">Šis iestatījums norāda, ka darbs ir bloķēts.</span><span class="sxs-lookup"><span data-stu-id="352da-112">This setting indicates that the work is blocked.</span></span> <span data-ttu-id="352da-113">Cilne **Bloķēšanas iemesli** parāda, kāpēc darbs tika bloķēts.</span><span class="sxs-lookup"><span data-stu-id="352da-113">The **Blocking reasons** tab shows why the work was blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="352da-114">Novēršana</span><span class="sxs-lookup"><span data-stu-id="352da-114">Resolution</span></span>

<span data-ttu-id="352da-115">Lai atbloķētu darbu, atlasiet cilni **Bloķēšanas iemesli** un pēc tam izpildiet vienu no tālāk minētajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="352da-115">To unblock the work, select the **Blocking reasons** tab, and then follow one of these steps:</span></span>

- <span data-ttu-id="352da-116">Ja lauks **Darba bloķēšanas iemesls** ir iestatīts uz *Nedefinēts iemesls*: darbību rūtī, cilnē **Darbs** grupā **Darbs** atlasiet **Atbloķēt darbu**.</span><span class="sxs-lookup"><span data-stu-id="352da-116">If the **Work blocking reason** field is set to *Undefined reason*: On the Action Pane, on the **Work** tab, in the **Work** group, select **Unblock work**.</span></span>
- <span data-ttu-id="352da-117">Ja lauks **Darba bloķēšanas iemesls** ir iestatīts uz *Kopuma apstrāde*: darbību rūtī, cilnē **Saistītā informācija** grupā **Saistītā informācija** atlasiet **Kopums**.</span><span class="sxs-lookup"><span data-stu-id="352da-117">If the **Work blocking reason** field is set to *Processing wave*: On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="352da-118">Pēc tam, lapā **Kopumi** darbības rūtī cilnē **Kopums**, grupā **Kopums** atlasiet **Attīrīšanas kopuma dati**.</span><span class="sxs-lookup"><span data-stu-id="352da-118">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="352da-119">Kļūdas apiešanas risinājums</span><span class="sxs-lookup"><span data-stu-id="352da-119">Workaround</span></span>

<span data-ttu-id="352da-120">Ja iepriekšējās darbības neatrisināja problēmu, darbu var atcelt, izpildot šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="352da-120">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="352da-121">Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="352da-121">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="352da-122">Laukā **Darba ID** norādiet darba ID, kuru vēlaties atcelt un kura vērtība **Darba statuss** pašlaik ir *Atvērts*, *Notiek*, *Atcelts*, *Apvienots* vai *Slēgts*.</span><span class="sxs-lookup"><span data-stu-id="352da-122">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="352da-123">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="352da-123">Select **OK**.</span></span>
1. <span data-ttu-id="352da-124">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="352da-124">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="352da-125">Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="352da-125">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
