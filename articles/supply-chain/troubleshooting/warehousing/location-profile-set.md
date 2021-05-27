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
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026709"
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
