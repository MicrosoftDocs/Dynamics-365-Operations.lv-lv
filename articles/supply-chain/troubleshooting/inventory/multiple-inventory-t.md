---
title: Vairāki krājumu darījumi partiju numuriem, kad tiek atspējots fiziskais labojums
description: Vairāki krājumu darījumi tiek izveidoti pēc pirkšanas pasūtījuma rindas pielāgošanas krājumiem, kuru partijas numura grupas fiziskās atjaunināšanas opcija ir iestatīta uz Nē.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b8aef8835e90b7437bb7833c13c3d287d4ca836bf1fefc01bfeafef1c93329bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768598"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Vairāki krājumu darījumi partiju numuriem, kad tiek atspējots fiziskais labojums

KB numurs: 4613390

## <a name="symptoms"></a>Simptomi

Vairāki krājumu darījumi tiek izveidoti pēc pirkšanas pasūtījuma rindas pielāgošanas krājumiem, kuru partijas numura grupas **Fiziskās atjaunināšanas** opcija ir iestatīta uz *Nē*.

Izveidojot krājumu, kura partijas numuru grupas **fiziskās atjaunināšanas** opcija ir iestatīta uz *Nē*, sistēma automātiski izveido jaunu partijas numuru, ja modificējat pirkšanas rindas daudzumu un saglabājat pirkšanas pasūtījuma lapu.

## <a name="resolution"></a>Novēršana

**Fiziskās atjaunināšanas** iestatījums numuru grupām darbojas šādā veidā:

- Kad opcija ir iestatīta uz *Jā*, jauni partijas numuri tiek izveidoti tikai pēc fiziskās atjaunināšanas (piemēram, kad preces tiek sūtītas vai saņemtas).
- Kad opcija ir iestatīta uz *Nē*, jauns partijas numurs tiek izveidots katru reizi, kad notiek piemērojama atjaunināšana (piemēram, kad pirkšanas pasūtījumam tiek pievienots jauns daudzums).
