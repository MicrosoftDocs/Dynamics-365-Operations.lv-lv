---
title: Nevar atcelt lietotājam izveidotu darbu
description: Nevar atcelt lietotājam izveidotu darbu
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924405"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="f7b71-103">Nevar atcelt lietotājam izveidotu darbu</span><span class="sxs-lookup"><span data-stu-id="f7b71-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="f7b71-104">Kļūdas kods: WAX708</span><span class="sxs-lookup"><span data-stu-id="f7b71-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="f7b71-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="f7b71-105">Symptoms</span></span>

<span data-ttu-id="f7b71-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="f7b71-106">The system shows the following error message:</span></span>

> <span data-ttu-id="f7b71-107">Nevar atcelt lietotājam piešķirtu darbu.</span><span class="sxs-lookup"><span data-stu-id="f7b71-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="f7b71-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="f7b71-108">Cause</span></span>

<span data-ttu-id="f7b71-109">Darbu ir bloķējis lietotājs, un to nevar atcelt.</span><span class="sxs-lookup"><span data-stu-id="f7b71-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="f7b71-110">Lai to apstiprinātu, atveriet darba ID un pēc tam atveriet cilni **Vispārīgi**. Ja darbs ir bloķēts, lauks **Darba statuss** tiks iestatīts uz *Notiek* un lauks **Bloķēts** tiks iestatīts uz lietotāja ID.</span><span class="sxs-lookup"><span data-stu-id="f7b71-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="f7b71-111">Novēršana</span><span class="sxs-lookup"><span data-stu-id="f7b71-111">Resolution</span></span>

<span data-ttu-id="f7b71-112">Lai atceltu darbu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f7b71-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="f7b71-113">Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.</span><span class="sxs-lookup"><span data-stu-id="f7b71-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="f7b71-114">Laukā **Darba ID** norādiet darba ID, ko vēlaties atcelt.</span><span class="sxs-lookup"><span data-stu-id="f7b71-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="f7b71-115">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f7b71-115">Select **OK**.</span></span>
1. <span data-ttu-id="f7b71-116">Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.</span><span class="sxs-lookup"><span data-stu-id="f7b71-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="f7b71-117">Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="f7b71-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
