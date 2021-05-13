---
title: Darbu nevar atcelt, tā statusa dēļ
description: Darbu nevar atcelt, tā statusa dēļ
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924259"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="5c652-103">Darbu nevar atcelt, tā statusa dēļ</span><span class="sxs-lookup"><span data-stu-id="5c652-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="5c652-104">Kļūdas kods: WAX2190</span><span class="sxs-lookup"><span data-stu-id="5c652-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="5c652-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="5c652-105">Symptoms</span></span>

<span data-ttu-id="5c652-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="5c652-106">The system shows the following error message:</span></span>

> <span data-ttu-id="5c652-107">Darbu %1 nevar atcelt, jo tā statuss ir %2.</span><span class="sxs-lookup"><span data-stu-id="5c652-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="5c652-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="5c652-108">Cause</span></span>

<span data-ttu-id="5c652-109">Darbu nevar atcelt tā pašreizējā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="5c652-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="5c652-110">Darba virsrakstam vai darba rindām nav paredzamā vērtība **Darba statuss**.</span><span class="sxs-lookup"><span data-stu-id="5c652-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="5c652-111">Lauks **Darba statuss** darba virsrakstā nav iestatīts uz *Atvērts* vai *Notiek*.</span><span class="sxs-lookup"><span data-stu-id="5c652-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="5c652-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="5c652-112">Resolution</span></span>

<span data-ttu-id="5c652-113">Lai atceltu darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5c652-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="5c652-114">Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="5c652-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="5c652-115">Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt.</span><span class="sxs-lookup"><span data-stu-id="5c652-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="5c652-116">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="5c652-116">Select **OK**.</span></span>
1. <span data-ttu-id="5c652-117">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="5c652-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="5c652-118">Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="5c652-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
