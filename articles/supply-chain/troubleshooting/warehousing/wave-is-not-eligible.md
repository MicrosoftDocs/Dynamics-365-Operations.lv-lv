---
title: Kopums nav piemērots tīrīšanai
description: Kopums nav piemērots tīrīšanai
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778510"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Kopums nav piemērots tīrīšanai

Kļūdas kods: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Kopuma %1 dati nav paredzēti tīrīšanai.

Kopuma datus nevar notīrīt.  

## <a name="cause"></a>Iemesls

Kopums pašlaik tiek apstrādāts, kā norādīts vienā no šādiem nosacījumiem:

- Lauks **Kopuma statuss** ir iestatīts uz *Izpilde*.
- Atlasot **Pakešuzdevums** grupā **Kopums** darbību rūts cilnē **Kopums**, lauka **Statuss** vērtība nav iestatīta uz *Pabeigts*, *Kļūda* vai *Atcelts*. Tāpēc pakešuzdevums pašreiz tiek izpildīts.

## <a name="resolution"></a>Novēršana

Darbību rūts cilnes **Kopums** grupā **Kopums** atlasiet **Pakešuzdevums** un pēc tam veiciet vienu no tālāk minētajām darbībām.

- Ja lauka **Statuss** ir iestatīts uz *Izpilde*: darbības rūtī cilnē **Pakešuzdevums** grupā **Pakešuzdevums** atlasiet **Skatīt uzdevumus**. Jūs varat sekot līdzi progresam, atsvaidzinot lapu **Partijas uzdevumi**.
- Ja lauka **Statuss** nav iestatīts uz *Izpilde*: darbības rūtī cilnē **Pakešuzdevums** grupā **Funkcijas** atlasiet **Mainīt statusu**. Laukā **Atlasīt jaunu statusu** atlasiet *Gaidīšana*. Pēc tam atlasiet **Labi**.
