---
title: Pirkuma pasūtījumi neatspoguļo juridiskās personas valodas iestatījumus
description: Produkta nosaukums pirkuma pasūtījumā tiek rādīts sistēmas valodā, nevis juridiskajai personai, kurai pirkums tika izveidots, iestatītajā valodā
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
ms.openlocfilehash: 4deec493b5480dc570ac82876243bc31a2ae87aa
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476973"
---
# <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a>Pirkuma pasūtījumi neatspoguļo juridiskās personas valodas iestatījumus


## <a name="symptoms"></a>Simptomi

Preces nosaukums pirkšanas pasūtījumā tiek norādīts sistēmas valodā, nevis valodā, kas iestatīta juridiskajai personai, kurai tika izveidots pirkšanas pasūtījums.

## <a name="reproduce-the-issue"></a>Problēmas atveide

Nākamajā procedūrā ir parādīts viens šīs problēmas atveides veids.

1. Iestatiet sistēmas valodu uz *EN-US* (ASV angļu valoda).
1. Pārliecinieties, vai pastāv prece, kam preces nosaukuma tulkošanai tiek saglabātas *EN-US* un *DE* (vācu valoda) valoda.
1. Mainiet juridiskās personas valodu uz *DE*.
1. Juridiskajai personai, kurai ir iestatīta *DE* valoda, izveidojiet pirkšanas pasūtījumu, kas ietver preci.
1. Ņemiet vērā, ka preces nosaukums joprojām ir redzams ASV angļu valodā (sistēmas valoda).

## <a name="resolution"></a>Novēršana

Tas tiek darīts ar nolūku. Pirkšanas pasūtījumos prece vienmēr tiek rādīta sistēmas valodā. Pirkšanas pasūtījuma valoda tiek izmantota, kad tiek izveidots apstiprinājumu žurnāls.
