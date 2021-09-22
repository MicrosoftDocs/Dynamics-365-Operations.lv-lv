---
title: Vienība un vienību skaits krājumu žurnālā nedarbojas pareizi
description: Vienība un vienību skaits krājumu žurnālā nedarbojas pareizi
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476965"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Vienība un vienību skaits krājumu žurnālā nedarbojas pareizi

## <a name="symptoms"></a>Simptomi

Strādājot ar mērvienībām un daudzumiem krājumu žurnālā, varat saskarties ar vienu vai abiem šiem jautājumiem:

- Jūs krājuma žurnālā neredzat mērvienības vai vienību daudzumus, kamēr izlaistai precei ir iestatīta pārvēršanas mērvienība, un krājumu žurnālā nevarat mainīt šo mērvienību.
- Krājumu žurnālā ir redzami lauki **Daudzums** un **Mērvienība**, taču nav redzams lauks **Mērvienības daudzums**. Mainot mērvienību, ievadiet daudzumu un grāmatojiet žurnālu, žurnālā joprojām tiek parādīta sākotnējā mērvienība šim daudzumam.

## <a name="resolution"></a>Novēršana

Lai novērstu šo problēmu, izpildiet sekojošās darbības.

1. **Līdzekļu pārvaldības** darbvietā pārliecinieties, vai krājumu žurnālu līdzekļa funkcija *Izmanto mērvienību un mērvienību daudzumu* ir ieslēgta. Ar šo žurnālam tiek pievienots lauks **Mērvienība** un **Mērvienības daudzums**.
1. Kad funkcija ir ieslēgta, lietojiet lauku **Daudzums**, **Mērvienības daudzums** un **Mērvienība** šādā veidā:

    - **Daudzums** – norādiet daudzumu, izmantojot izpildei nodotai precei noteikto noklusējuma mērvienību. Tomēr noklusētā mērvienība šeit netiek rādīta. Ja ir iestatīta pārvēršana starp noklusējuma mērvienību un laukā **Mērvienība** atlasīto vienību, lauks **Daudzums** tiek automātiski atjaunināts, pamatojoties uz lauku **Mērvienība** un **Mērvienības daudzums** atlasi.
    - **Mērvienības daudzums** - norādiet daudzumu, izmantojot laukā **Mērvienība** atlasīto mērvienību.
    - **Mērvienība** – atlasiet mērvienību, ko piemērot vērtībai laukā **Mērvienības daudzums**.
