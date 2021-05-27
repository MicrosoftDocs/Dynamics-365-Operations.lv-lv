---
title: Trūkst lauka iestatījumu, ja krājumu modeļu grupas tiek kopētas uz citu juridisko personu
description: Trūkst lauka iestatījumi, ja krājumu modeļu grupas tiek kopētas uz citu juridisko personu.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026706"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a><span data-ttu-id="8b77b-103">Trūkst lauka iestatījumu, ja krājumu modeļu grupas tiek kopētas uz citu juridisko personu</span><span class="sxs-lookup"><span data-stu-id="8b77b-103">Missing field settings when item model groups are copied to another legal entity</span></span>

<span data-ttu-id="8b77b-104">KB numurs: 4612800</span><span class="sxs-lookup"><span data-stu-id="8b77b-104">KB number: 4612800</span></span>

## <a name="symptoms"></a><span data-ttu-id="8b77b-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="8b77b-105">Symptoms</span></span>

<span data-ttu-id="8b77b-106">Kopējot krājumu modeļu grupas uz citu juridisko personu (uzņēmumu), izmantojot *Krājumu modeļu grupas krājumu politikas* entītiju, daži lauka iestatījumi (piemēram, krājumu modelis un apraksts) nav jaunajā modeļu grupā mērķa juridiskajā personā.</span><span class="sxs-lookup"><span data-stu-id="8b77b-106">When you copy item model groups to another legal entity (company) by using the *Item model group inventory policies* entity, some field settings (for example, the inventory model and description) are missing in the new model group in the destination legal entity.</span></span>

## <a name="resolution"></a><span data-ttu-id="8b77b-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="8b77b-107">Resolution</span></span>

<span data-ttu-id="8b77b-108">Lai izveidotu pilnīgu krājumu modeļu grupas kopiju citai juridiskajai personai, jāatlasa gan preču modeļu grupas krājumu politikas, (`InventInventoryPolicyEntity`), gan izmaksu plūsmas pieņēmuma politika (`InventCostFlowAssumptionPolicyEntity`), kas ir saistīta ar preču modeļu grupu.</span><span class="sxs-lookup"><span data-stu-id="8b77b-108">To create a complete copy of an item model group to another legal entity, you must also select both the item model group inventory policies (`InventInventoryPolicyEntity`) and the cost flow assumption policies (`InventCostFlowAssumptionPolicyEntity`) that are associated with the item model group.</span></span>
