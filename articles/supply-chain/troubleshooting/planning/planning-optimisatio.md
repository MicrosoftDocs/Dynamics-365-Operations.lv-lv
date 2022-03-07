---
title: Plānotais pirkšanas pasūtījums tiek izveidots, ja pirkums pastāv negatīvo dienu laikā
description: Ja seguma kods ir Min/max, plānošanas optimizācija izveido plānotu pirkšanas pasūtījumu, ja pirkums ir negatīvo dienu laikā.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 94d569684a0bfa2398e98147b9b85531954f8d56748894034a048fa627230ef0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775511"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Plānotais pirkšanas pasūtījums tiek izveidots, ja pirkums pastāv negatīvo dienu laikā

KB numurs: 4614298

## <a name="symptoms"></a>Simptomi

Ja seguma kods ir *Min/max*, plānošanas optimizācija izveido plānotu pirkšanas pasūtījumu, ja pirkums ir negatīvo dienu laikā.

## <a name="resolution"></a>Novēršana

Plānošanas optimizācijas neatbalsta negatīvas dienas. Tomēr tā vienmēr nodrošina, ka plānotie pasūtījumi netiek plānoti izpildes laikā attiecībā pret pašreizējo datumu. Piemēram, pirkšanas izpildes laiks ir 10 dienas, un pirkšanas pasūtījumu ir plānots saņemt astoņu dienu laikā no šodienas. Šajā gadījumā pirkšanas pasūtījums tiks izmantots kā pieprasījuma piedāvājums, kas ir piecu dienu laikā no šodienas.

Tāpēc ieteicams koriģēt izpildes laikus, lai segtu visus scenārijus (vai gandrīz visus).
