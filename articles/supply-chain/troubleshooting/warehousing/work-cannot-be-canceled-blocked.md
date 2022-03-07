---
title: Darbu nevar atcelt, jo tas ir bloķēts
description: Darbu nevar atcelt, jo tas ir bloķēts
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a24f199484c7596189b19e4cddf344e9186c6044edd2906affca9b530de44168
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722203"
---
# <a name="work-cant-be-canceled-because-its-blocked"></a>Darbu nevar atcelt, jo tas ir bloķēts

Kļūdas kods: WHSCancellationOfWorkBlockedByExecutingWave_ErrorMessage

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Darbu %1 nevar atcelt, jo to ir bloķējis iemesla veids %2. Pirms darba atcelšanas tas ir jāatbloķē.

## <a name="cause"></a>Iemesls

Darbs ir bloķēts, un to nevar atcelt.

Lapā **Darbs** cilnē **Vispārīgi** opcija **Bloķēts** ir iestatīta uz *Jā*. Šis iestatījums norāda, ka darbs ir bloķēts. Cilne **Bloķēšanas iemesli** parāda, kāpēc darbs tika bloķēts.

## <a name="resolution"></a>Novēršana

Lai atbloķētu darbu, atlasiet cilni **Bloķēšanas iemesli** un pēc tam izpildiet vienu no tālāk minētajām darbībām.

- Ja lauks **Darba bloķēšanas iemesls** ir iestatīts uz *Nedefinēts iemesls*: darbību rūtī, cilnē **Darbs** grupā **Darbs** atlasiet **Atbloķēt darbu**.
- Ja lauks **Darba bloķēšanas iemesls** ir iestatīts uz *Kopuma apstrāde*: darbību rūtī, cilnē **Saistītā informācija** grupā **Saistītā informācija** atlasiet **Kopums**. Pēc tam, lapā **Kopumi** darbības rūtī cilnē **Kopums**, grupā **Kopums** atlasiet **Attīrīšanas kopuma dati**.

## <a name="workaround"></a>Kļūdas apiešanas risinājums

Ja iepriekšējās darbības neatrisināja problēmu, darbu var atcelt, izpildot šīs darbības.

1. Pārejiet uz **Noliktavas pārvaldība \> Periodiskie uzdevumi \> Tīrīšana \> Atcelšanas darbs**.
1. Laukā **Darba ID** norādiet darba ID, kuru vēlaties atcelt un kura vērtība **Darba statuss** pašlaik ir *Atvērts*, *Notiek*, *Atcelts*, *Apvienots* vai *Slēgts*.
1. Atlasiet **Labi**.
1. Atlasiet **Jā**, lai apstiprinātu, ka vēlaties atcelt darbu.

Papildus informāciju skatiet [Noliktavas darba atcelšana izņēmuma apstrādei](../../warehousing/cancel-warehouse-work.md).
