---
title: Noklusējuma nodokļu grupa un termiņatlaide netiek aizpildīta no rēķina konta
description: Noklusējuma nodokļu grupa un noklusējuma termiņatlaide netiek aizpildīta no rēķina konta
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb984eb17209dc92e336df5ad475bb0f70c6e35c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476977"
---
# <a name="default-tax-group-and-cash-discount-arent-filled-in-from-the-invoice-account"></a>Noklusējuma nodokļu grupa un termiņatlaide netiek aizpildīta no rēķina konta

## <a name="symptoms"></a>Simptomi

Ja izmantojat rēķina kontu, kas atšķiras no debitora konta, noklusējuma nodokļu grupa un noklusējuma termiņatlaide netiek aizpildīta no rēķina konta, kad tiek izveidots pirkšanas pasūtījums.

## <a name="resolution"></a>Novēršana

Tas tiek darīts ar nolūku. Nodokļu grupas, termiņatlaižu un citas cenu informācijas noklusējuma vērtības ir balstītas uz debitora kontu, nevis uz rēķina kontu.
