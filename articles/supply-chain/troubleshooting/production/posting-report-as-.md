---
title: Kļūda pabeigtās ražošanas žurnāla grāmatošanas laikā
description: Kad grāmatojat žurnālu Ziņot kā pabeigtu, saņemat kļūdas ziņojumu, ka pasūtīto daudzumu nevar samazināt.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026700"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Kļūda pabeigtās ražošanas žurnāla grāmatošanas laikā

KB numurs: 4612891

## <a name="symptoms"></a>Simptomi

Kad jūs iegrāmatojiet žurnālu **Ziņot kā pabeigtu**, parādās kļūda un saņemat šādu kļūdas ziņojumu:

> Pasūtīto daudzumu nav iespējams samazināt, jo atvērtās krājumu darbības ar statusu Pasūtīts nav pietiekamas. Krājumi ir Nopirkti, Saņemti vai Reģistrēti.

Šī kļūda rodas tikai tad, ja lauks **Kļūdu daudzums** ir iestatīts **Ziņot kā pabeigtu** žurnāla pirmajā rindā, un lauks **Labs daudzums** ir iestatīts pēdējā rindā. Ja pēdējā rindā ir iestatīts lauks **Kļūdu daudzums**, kļūdas nenotiek.

## <a name="resolution"></a>Novēršana

Lai novērstu šo kļūdu, atveriet lapu **Ražošanas kontroles parametri** un pēc tam cilnē **Vispārīgi** iestatiet **Palielināt atlikušo daudz. ar kļūdu daudz.** opciju uz *Jā*.
