---
title: Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot pārskatīšanas darbplūsmu
description: Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot darbplūsmu ar Pārskatīšanas statusu.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026719"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a><span data-ttu-id="3a229-103">Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot pārskatīšanas darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="3a229-103">Directly derived firmed orders are processed by an in-review workflow</span></span>

<span data-ttu-id="3a229-104">KB numurs: 4612450</span><span class="sxs-lookup"><span data-stu-id="3a229-104">KB number: 4612450</span></span>

## <a name="symptoms"></a><span data-ttu-id="3a229-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="3a229-105">Symptoms</span></span>

<span data-ttu-id="3a229-106">Tieši atvasinātie apstiprinātie pasūtījumi tiek apstrādāti, izmantojot darbplūsmu ar *Pārskatīšanas* statusu.</span><span class="sxs-lookup"><span data-stu-id="3a229-106">Directly derived firmed orders are processed by a workflow that has a status of *In-review*.</span></span>

## <a name="resolution"></a><span data-ttu-id="3a229-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="3a229-107">Resolution</span></span>

<span data-ttu-id="3a229-108">Kad ir iespējota gadījuma izmaiņu izsekošana, *Pārskatīšanas* statuss tiek piešķirts apstiprinātiem atvasinātiem pasūtījumiem (pakārtotie pirkšanas pasūtījumi).</span><span class="sxs-lookup"><span data-stu-id="3a229-108">When change tracking is enabled, a status of *In-review* is assigned to firmed derived orders (subcontract purchase orders).</span></span> <span data-ttu-id="3a229-109">Tādēļ, ja pirkšanas pasūtījums ir atvasināts (pakārtots pirkšanas pasūtījums), tas tiek iesniegts tikai darbplūsmai.</span><span class="sxs-lookup"><span data-stu-id="3a229-109">Therefore, if a purchase order is derived (a subcontract purchase order), it's only submitted to a workflow.</span></span> <span data-ttu-id="3a229-110">Ja pirkšanas pasūtījums ir apstiprināts plānotais pirkšanas pasūtījums, tas tiek automātiski apstiprināts, lai nodrošinātu, ka plānošanas programma neveido jaunus plānotos pasūtījumus, kamēr pirkšanas pasūtījumam joprojām ir statuss *Melnraksts*.</span><span class="sxs-lookup"><span data-stu-id="3a229-110">If a purchase order is a firmed planned purchase order, it's automatically approved to ensure that the planning engine doesn't create new planned orders while the purchase order is still in *Draft* status.</span></span>
