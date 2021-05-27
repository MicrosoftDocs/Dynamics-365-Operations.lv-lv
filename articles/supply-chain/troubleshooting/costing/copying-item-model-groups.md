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
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Trūkst lauka iestatījumu, ja krājumu modeļu grupas tiek kopētas uz citu juridisko personu

KB numurs: 4612800

## <a name="symptoms"></a>Simptomi

Kopējot krājumu modeļu grupas uz citu juridisko personu (uzņēmumu), izmantojot *Krājumu modeļu grupas krājumu politikas* entītiju, daži lauka iestatījumi (piemēram, krājumu modelis un apraksts) nav jaunajā modeļu grupā mērķa juridiskajā personā.

## <a name="resolution"></a>Novēršana

Lai izveidotu pilnīgu krājumu modeļu grupas kopiju citai juridiskajai personai, jāatlasa gan preču modeļu grupas krājumu politikas, (`InventInventoryPolicyEntity`), gan izmaksu plūsmas pieņēmuma politika (`InventCostFlowAssumptionPolicyEntity`), kas ir saistīta ar preču modeļu grupu.
