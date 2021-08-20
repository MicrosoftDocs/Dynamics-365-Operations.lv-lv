---
title: Darbs paliek bloķēts
description: Darbs paliek bloķēts
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 898390c78bb26fb8a44f77a10ad27a00720f7d1a3396cec5fff10e9d6b93364d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768574"
---
# <a name="work-remains-blocked"></a>Darbs paliek bloķēts

Kļūdas kods: WHSWorkBlockingExecutingWaveReason_ErrorMessage

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Darbs %1 paliek bloķēts, jo saistītajam kopumam %2 ir statuss %3.

## <a name="cause"></a>Iemesls

Darbs pašlaik tiek apstrādāts kopumā un nevar tikt bloķēts, kā norādīts vienā no šādiem nosacījumiem:

- Cilnē **Bloķēšanas iemesli** laukā **Darba bloķēšanas iemesls** vienai vai vairākām rindām ir iestatīta opcija *Kopuma apstrāde*.
- Atlasot **Kopums** grupā **Saistītā informācija** cilnē **Saistītā informācija** darbību rūtī, lauks **Kopuma statuss** ir iestatīts uz *Apstrāde*.

## <a name="resolution"></a>Novēršana

Darbību rūtī cilnē **Saistītā informācija** grupā **Saistīta informācija** atlasiet **Kopums**. Pēc tam, lapā **Kopumi** darbības rūtī cilnē **Kopums**, grupā **Kopums** atlasiet **Attīrīšanas kopuma dati**.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Ja iepriekšējās darbības neatrisināja problēmu, darbu var atcelt, izpildot šīs darbības.

1. Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.
1. Laukā **Darba ID** norādiet darba ID, kuru vēlaties atcelt un kura vērtība **Darba statuss** pašlaik ir *Atvērts*, *Notiek*, *Atcelts*, *Apvienots* vai *Slēgts*.
1. Atlasiet **Labi**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.

Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).
