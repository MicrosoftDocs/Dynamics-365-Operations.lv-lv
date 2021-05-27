---
title: Klienta atlaižu uzkrāšana neizdodas, ja tiek izmantotas krājumu atlaižu grupas
description: Ja izmantojat klienta atlaižu līgumus kopā ar krājumu atlaižu grupām, atlaides tiek aprēķinātas, bet uzkrāšana neizdodas.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026701"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a><span data-ttu-id="3a8b6-103">Klienta atlaižu uzkrāšana neizdodas, ja tiek izmantotas krājumu atlaižu grupas</span><span class="sxs-lookup"><span data-stu-id="3a8b6-103">Cumulation of customer rebates fails when item rebate groups are used</span></span>

<span data-ttu-id="3a8b6-104">KB numurs: 4611372</span><span class="sxs-lookup"><span data-stu-id="3a8b6-104">KB number: 4611372</span></span>

## <a name="symptoms"></a><span data-ttu-id="3a8b6-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="3a8b6-105">Symptoms</span></span>

<span data-ttu-id="3a8b6-106">Ja izmantojat klienta atlaižu līgumus (*summas* tipa) kopā ar krājumu atlaižu grupām, atlaides tiek aprēķinātas, bet uzkrāšana neizdodas.</span><span class="sxs-lookup"><span data-stu-id="3a8b6-106">When you use customer rebate agreements (of the *amount* type) in combination with item rebate groups, rebates are calculated, but cumulation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="3a8b6-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="3a8b6-107">Resolution</span></span>

<span data-ttu-id="3a8b6-108">Sistēma darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="3a8b6-108">The system is behaving as designed.</span></span> <span data-ttu-id="3a8b6-109">Krājumu grupas grupē tikai krājumus, kuriem ir tāds pats sliekšņa nosacījums.</span><span class="sxs-lookup"><span data-stu-id="3a8b6-109">Item groups group only items that have the same threshold condition.</span></span> <span data-ttu-id="3a8b6-110">Atlaides nosacījums (slieksnis) tiek iestatīts pret summu katram krājumam, nevis attiecībā pret uzkrāto summu jebkuram krājumam krājumu grupā.</span><span class="sxs-lookup"><span data-stu-id="3a8b6-110">The rebate condition (threshold) is set against the amount for each item, not against the cumulated amount for any item in the item group.</span></span>
