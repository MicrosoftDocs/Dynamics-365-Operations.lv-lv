---
title: Lai plānoto ražošanas pasūtījumu varētu apstiprināt, tas ir jāplāno
description: Mēģinot apstiprināt plānoto pasūtījumu, tiek parādīts kļūdas ziņojums, ka pasūtījums ir jāplāno pirms tā apstiprināšanas.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294132"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="8392a-103">Lai plānoto ražošanas pasūtījumu varētu apstiprināt, tas ir jāplāno</span><span class="sxs-lookup"><span data-stu-id="8392a-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="8392a-104">Kļūdas kods: SYS309802</span><span class="sxs-lookup"><span data-stu-id="8392a-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="8392a-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="8392a-105">Symptoms</span></span>

<span data-ttu-id="8392a-106">Mēģinot apstiprināt plānoto pasūtījumu saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="8392a-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="8392a-107">Plānotajam ražošanas pasūtījumam ir jābūt plānotam, pirms to var apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="8392a-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="8392a-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="8392a-108">Cause</span></span>

<span data-ttu-id="8392a-109">Plānotie sākuma un beigu datumi nedrīkst būt tukši.</span><span class="sxs-lookup"><span data-stu-id="8392a-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="8392a-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="8392a-110">Resolution</span></span>

<span data-ttu-id="8392a-111">Lai norādītu plānotā pasūtījuma sākuma un beigu datumus, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="8392a-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="8392a-112">Doties uz **Vispārējā plānošana \> Vispārējā plānošana \> Plānotie pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="8392a-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="8392a-113">Atveriet attiecīgo plānoto pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="8392a-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="8392a-114">Kopsavilkuma cilnes **Vispārīgi** sadaļā **Plānots** norādiet datumus laukos **Sākuma datums** un **Beigu datums**.</span><span class="sxs-lookup"><span data-stu-id="8392a-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
