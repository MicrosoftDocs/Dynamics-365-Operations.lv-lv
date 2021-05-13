---
title: Kopums nav piemērots tīrīšanai
description: Kopums nav piemērots tīrīšanai
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924331"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="0e945-103">Kopums nav piemērots tīrīšanai</span><span class="sxs-lookup"><span data-stu-id="0e945-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="0e945-104">Kļūdas kods: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="0e945-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="0e945-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="0e945-105">Symptoms</span></span>

<span data-ttu-id="0e945-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="0e945-106">The system shows the following error message:</span></span>

> <span data-ttu-id="0e945-107">Kopuma %1 dati nav paredzēti tīrīšanai.</span><span class="sxs-lookup"><span data-stu-id="0e945-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="0e945-108">Kopuma datus nevar notīrīt.</span><span class="sxs-lookup"><span data-stu-id="0e945-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="0e945-109">Iemesls</span><span class="sxs-lookup"><span data-stu-id="0e945-109">Cause</span></span>

<span data-ttu-id="0e945-110">Kopums pašlaik tiek apstrādāts, kā norādīts vienā no šādiem nosacījumiem:</span><span class="sxs-lookup"><span data-stu-id="0e945-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="0e945-111">Lauks **Kopuma statuss** ir iestatīts uz *Izpilde*.</span><span class="sxs-lookup"><span data-stu-id="0e945-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="0e945-112">Atlasot **Pakešuzdevums** grupā **Kopums** darbību rūts cilnē **Kopums**, lauka **Statuss** vērtība nav iestatīta uz *Pabeigts*, *Kļūda* vai *Atcelts*.</span><span class="sxs-lookup"><span data-stu-id="0e945-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="0e945-113">Tāpēc pakešuzdevums pašreiz tiek izpildīts.</span><span class="sxs-lookup"><span data-stu-id="0e945-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="0e945-114">Novēršana</span><span class="sxs-lookup"><span data-stu-id="0e945-114">Resolution</span></span>

<span data-ttu-id="0e945-115">Darbību rūts cilnes **Kopums** grupā **Kopums** atlasiet **Pakešuzdevums** un pēc tam veiciet vienu no tālāk minētajām darbībām.</span><span class="sxs-lookup"><span data-stu-id="0e945-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="0e945-116">Ja lauka **Statuss** ir iestatīts uz *Izpilde*: darbības rūtī cilnē **Pakešuzdevums** grupā **Pakešuzdevums** atlasiet **Skatīt uzdevumus**.</span><span class="sxs-lookup"><span data-stu-id="0e945-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="0e945-117">Jūs varat sekot līdzi progresam, atsvaidzinot lapu **Partijas uzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="0e945-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="0e945-118">Ja lauka **Statuss** nav iestatīts uz *Izpilde*: darbības rūtī cilnē **Pakešuzdevums** grupā **Funkcijas** atlasiet **Mainīt statusu**.</span><span class="sxs-lookup"><span data-stu-id="0e945-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="0e945-119">Laukā **Atlasīt jaunu statusu** atlasiet *Gaidīšana*.</span><span class="sxs-lookup"><span data-stu-id="0e945-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="0e945-120">Pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="0e945-120">Then select **OK**.</span></span>
