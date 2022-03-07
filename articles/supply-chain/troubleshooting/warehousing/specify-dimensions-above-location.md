---
title: Nevar izlaist noslodzi daļējam daudzumam ar hierarhiju ´partija virs´
description: Izmantojot krājumu ar rezervāciju hierarhiju ´partija virs´, noslodzes rindās ir jābūt norādītām dimensijām virs atrašanās vietas, lai varētu piešķirt krājumus.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476959"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Nevar izlaist noslodzi daļējam daudzumam ar rezervāciju hierarhiju ´partija virs´

## <a name="symptoms"></a>Simptomi

Kad izmantojat krājumu, kam ir *partija virs* rezervāciju hierarhija (ar Partijas numura dimensiju, kas novietota virs Novietojuma dimensijas), **Izlaist uz noliktavu** komanda lapā **Kravas plānošanas rīks** daļējam daudzumam nestrādā. Jūs saņemsit šādu kļūdas ziņojumu:

> Jāpiešķir kopumam, noslodzes rindām ir jānorāda dimensijas virs novietojuma. Lai piešķirtu šīs dimensijas, rezervējiet un atkārtoti izveidojiet noslodzes rindu.

Tomēr, ja izmantojat krājumu, kam ir *partija zem* rezervāciju hierarhija (ar Partijas numura dimensiju, kas novietota zem Novietojuma dimensijas), varat izlaist kravu no lapas **Kravas plānošanas rīks** daļējam daudzumam.

## <a name="cause"></a>Iemesls

Ja jūs ievietojat dimensiju virs **Novietojuma** dimensijas rezervāciju hierarhijā, tas ir jānorāda pirms izdošanas uz noliktavu. Krājumus var sekmīgi sadalīt tikai tad, ja dimensijās virs novietojuma nav atstarpju.

## <a name="resolution"></a>Novēršana

Rezervējot un vēlreiz izmantojot noslodzes rindu, pārliecinieties, vai visas dimensijas virs **Atrašanās vietas** ir piešķirtas.
