---
title: Ja pieļaujamā svara daudzums ir sadalīts, nominālā daudzuma vietā tiek izmantots minimālais daudzums
description: Kad pieļaujamā svara daudzums tiek sadalīts pakotnēs, laukā Izdošanas daudzums tiek izmantots minimālais daudzums, kas ir iestatīts krājumam, nevis nominālais daudzums.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 185365ced5c4516d8fcdbdca88794d0078615888
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026720"
---
# <a name="when-a-catch-weight-quantity-is-split-minimum-quantity-is-used-instead-of-nominal-quantity"></a><span data-ttu-id="aba7c-103">Ja pieļaujamā svara daudzums ir sadalīts, nominālā daudzuma vietā tiek izmantots minimālais daudzums</span><span class="sxs-lookup"><span data-stu-id="aba7c-103">When a catch-weight quantity is split, minimum quantity is used instead of nominal quantity</span></span>

<span data-ttu-id="aba7c-104">KB numurs: 4612073</span><span class="sxs-lookup"><span data-stu-id="aba7c-104">KB number: 4612073</span></span>

## <a name="symptoms"></a><span data-ttu-id="aba7c-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="aba7c-105">Symptoms</span></span>

<span data-ttu-id="aba7c-106">Kad pieļaujamā svara daudzums tiek sadalīts pakotnēs, laukā **Izdošanas daudzums** tiek izmantots minimālais daudzums, kas ir iestatīts krājumam, nevis nominālais daudzums.</span><span class="sxs-lookup"><span data-stu-id="aba7c-106">When a catch-weight quantity is being split into batches, the **Pick qty** field uses the minimum quantity that is set for the item, not the nominal quantity.</span></span>

## <a name="resolution"></a><span data-ttu-id="aba7c-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="aba7c-107">Resolution</span></span>

<span data-ttu-id="aba7c-108">Sistēma darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="aba7c-108">The system is behaving as designed.</span></span> <span data-ttu-id="aba7c-109">Sistēma izmanto katra krājuma minimālā daudzuma iestatījumus izdošanai.</span><span class="sxs-lookup"><span data-stu-id="aba7c-109">The system uses each item's minimum quantity setup for picking.</span></span>
