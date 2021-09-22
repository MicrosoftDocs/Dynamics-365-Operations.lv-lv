---
title: Nevar veikt krājumu rezervācijas, jo ir pieejams 0,00
description: Jums tiek parādīts kļūdas ziņojums par to, ka sistēma nevar veikt rezervācijas, jo krājumos ir tikai 0,00. Šo problēmu, iespējams, izraisa atvērts darbs.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477015"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Sistēma nevar veikt krājumu rezervācijas, jo krājumos ir pieejams 0,00

## <a name="symptoms"></a>Simptomi

Šī problēma var rasties, ja sistēma nevar atjaunināt krājumu daudzumu, jo nav pietiekoši daudz krājumu darbību, kurām ir noteiktas dimensijas. Saņemsit šādu kļūdas ziņojumu:

> Fiziskais rīcībā esošais Vietne=%1, Noliktava=%2, Krājumu statuss=pieejams, Partijas numurs=%3, Īpašnieks=%4: %5 nevar rezervēt, jo krājumos ir pieejamas tikai 0,00.

## <a name="resolution"></a>Novēršana

Šo problēmu, iespējams, izraisa atvērts darbs. Vai nu pabeidziet darbu, vai saņemiet bez darba izveides. Pārliecinieties, vai krājumu darbības fiziski nerezervē daudzumu. Piemēram, šīs darbības var būt atvērti kvalitātes pasūtījumi, krājumu bloķēšanas ieraksti vai izdošanas pasūtījumi.
