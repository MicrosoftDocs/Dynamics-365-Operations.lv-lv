---
title: Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam
description: Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a5b78154b51252b3ac96ba28c254e823caf87019
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924379"
---
# <a name="the-last-closed-work-line-must-be-a-put"></a><span data-ttu-id="e4c3e-103">Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam</span><span class="sxs-lookup"><span data-stu-id="e4c3e-103">The last closed work line must be a put</span></span>

<span data-ttu-id="e4c3e-104">Kļūdas kods: WAX1285</span><span class="sxs-lookup"><span data-stu-id="e4c3e-104">Error code: WAX1285</span></span>

## <a name="symptoms"></a><span data-ttu-id="e4c3e-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="e4c3e-105">Symptoms</span></span>

<span data-ttu-id="e4c3e-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="e4c3e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="e4c3e-107">Pēdējās slēgtās darba rindas statusam ir jābūt izvietotam.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-107">The last closed work line must be a put.</span></span>

## <a name="cause"></a><span data-ttu-id="e4c3e-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="e4c3e-108">Cause</span></span>

<span data-ttu-id="e4c3e-109">Darbu nevar atcelt tā pašreizējā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="e4c3e-110">Pēdējā darba rindā lauks **darba statuss** ir iestatīts uz *Slēgts*, bet lauks **Darba veids** nav iestatīts kā *Ievietot*.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-110">On the last work line, the **Work status** field is set to *Closed*, but the **Work type** field isn't set to *Put*.</span></span>

## <a name="resolution"></a><span data-ttu-id="e4c3e-111">Novēršana</span><span class="sxs-lookup"><span data-stu-id="e4c3e-111">Resolution</span></span>

<span data-ttu-id="e4c3e-112">Lai atceltu darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="e4c3e-113">Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="e4c3e-114">Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="e4c3e-115">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-115">Select **OK**.</span></span>
1. <span data-ttu-id="e4c3e-116">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="e4c3e-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="e4c3e-117">Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="e4c3e-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
