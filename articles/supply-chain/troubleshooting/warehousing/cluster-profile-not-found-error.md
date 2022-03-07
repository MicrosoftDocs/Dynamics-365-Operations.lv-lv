---
title: Klastera profilu nevarēja atrast
description: Strādājot ar ienākoŠajām noliktavas darbībām, iespējams, saņemsit kļūdu, kurā teikts, ka klastera profilu nevar atrast. Pārliecinieties, vai klasteru profili ir pareizi iestatīti.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477028"
---
# <a name="cluster-profile-cant-be-found"></a>Klastera profilu nevarēja atrast

## <a name="symptoms"></a>Simptomi

Strādājot ar ienākoŠajām noliktavas darbībām, iespējams, saņemsit šādu kļūdas ziņojumu:

> "Kvalitātes pasūtījums %1 ir ģenerēts. Klastera profilu nevarēja atrast. Lūdzu, pārbaudiet konfigurāciju."

Šis kļūdas ziņojums ir saistīts ar saņemšanas procesu, kurā ir ieslēgta kvalitātes pārvaldība (QMS). Atkarībā no konfigurācijas jūsu vidē papildu detaļas par transakciju, kas ģenerē kļūdas ziņojumu, var palīdzēt novērst šo problēmu.

## <a name="resolution"></a>Novēršana

Vispirms pārskatiet klastera izdošanas iestatījumus un pārliecinieties, ka klasteru profili ir pareizi iestatīti. Klastera izdošanai nevar izmantot mobilās ierīces izvēlnes vienumu, ja vien nav iestatīti klasteru profili. Atkarībā no jūsu vides, iespējams, būs jāpārskata arī citas saistītās konfigurācijas.
