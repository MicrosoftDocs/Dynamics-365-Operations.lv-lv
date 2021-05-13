---
title: Darbs nav bloķēts
description: Darbs nav bloķēts
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924208"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="d1950-103">Darbs nav bloķēts</span><span class="sxs-lookup"><span data-stu-id="d1950-103">Work isn't blocked</span></span>

<span data-ttu-id="d1950-104">Kļūdas kods: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="d1950-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="d1950-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="d1950-105">Symptoms</span></span>

<span data-ttu-id="d1950-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="d1950-106">The system shows the following error message:</span></span>

> <span data-ttu-id="d1950-107">Darbs ar ID %1 nav bloķēts.</span><span class="sxs-lookup"><span data-stu-id="d1950-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="d1950-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="d1950-108">Cause</span></span>

<span data-ttu-id="d1950-109">Opcija **Bloķēts kopums** kopumam ir iestatīta uz *Nē*.</span><span class="sxs-lookup"><span data-stu-id="d1950-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="d1950-110">Darbu nevar atbloķēt, jo pašlaik tas nav bloķēts.</span><span class="sxs-lookup"><span data-stu-id="d1950-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="d1950-111">Novēršana</span><span class="sxs-lookup"><span data-stu-id="d1950-111">Resolution</span></span>

 <span data-ttu-id="d1950-112">Atbloķēt var tikai, ja opcija **Bloķēts kopums** ir iestatīta uz *Jā*.</span><span class="sxs-lookup"><span data-stu-id="d1950-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
