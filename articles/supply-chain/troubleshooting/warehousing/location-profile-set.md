---
title: Novietojuma profilā netiek atļauti negatīvi krājumi, bet atļauti negatīvi rīcībā esošie krājumi
description: Novietojuma profila opcijas Atļaut negatīvu krājumu vērtība ir iestatīta uz Nē, bet sistēma joprojām atļauj negatīvu rīcībā esošo krājumu daudzumu.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2a7345281301ee70a512dfadcd553cb4eb33003904d0dddf6967659b693f60d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742612"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Novietojuma profilā netiek atļauti negatīvi krājumi, bet atļauti negatīvi rīcībā esošie krājumi

KB numurs: 4613622

## <a name="symptoms"></a>Simptomi

Novietojuma profila opcijas **Atļaut negatīvu krājumu** vērtība ir iestatīta uz *Nē*, bet sistēma joprojām atļauj negatīvu rīcībā esošo krājumu daudzumu.

## <a name="example-scenario"></a>Piemērs

Valdības regulētiem darījumiem sistēmai jāspēj reģistrēt negatīvus krājumus, lai uzskaitītu zaudējumus. Vēlaties, lai krājums varētu uzrādīt negatīvu krājumu, bet tikai noteiktās vietās, piemēram, tvertnēs. Tomēr, ja krājumu modeļu grupa atļauj negatīvus krājumus, jūs sapratīsiet, ka nav svarīgi, vai vieta ir iestatīta, lai atļautu negatīvus krājumus. Ja krājums ir iestatīts tā, ka netiek atļauti negatīvi krājumi, nav svarīgi, kā tiek iestatīts novietojuma profils.

## <a name="resolution"></a>Novēršana

Iestatījums **Atļaut negatīvu krājumu daudzumu** no novietojuma profila attiecas tikai uz noliktavas procesiem, piemēram, izdošanu. Tomēr krājumu modeļu grupas, kas ir iestatītas, lai atļautu negatīvu krājumu daudzumu, ietekmē visus procesus no Krājumu pārvaldības un noliktavas pārvaldības moduļiem, un novietojuma profils neignorēs šo iestatījumu.

Varat kontrolēt, vai noliktavai ir atļauts veikt negatīvu krājumu. Iestatiet savu krājumu modeļu grupas, lai neatļautu negatīvus fiziskos krājumus, un iestatiet tikai atbilstošo noliktavu, lai ļautu negatīvus krājumus.
