---
title: Viena no rindām jau ir kravā
description: Šajā lapā paskaidrots, kāpēc saņēmāt kļūdu "Viena no rindām jau ir kravā. Nevar palaist uz noliktavu" un kā šo problēmu novērst.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477034"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Viena no rindām jau ir kravā

## <a name="symptoms"></a>Simptomi

Strādājot ar kravas veidošanu un sūtījumiem, iespējams, saņemsit šādu kļūdas ziņojumu:

> Viena no rindām jau ir kravā. Nevar izlaist uz noliktavu.

Ja manuāli izveidojat kravas vai iestatāt procesu tā, ka krava jau ir izveidota, pirms tiek veikta pārdošanas pasūtījuma rindas ievade, pieņēmums ir tāds, ka nākamā izpilde tiks veikta manuāli, un tiks izmantota maršruta un vērtējums no kravas.

Citā iespējamajā scenārijā jūs mēģināt veikt automātisku izlaišanu noliktavā, bet kopuma procesam neizdevās izveidot darbu. Tāpēc atvērts sūtījums vai krava joprojām tiek izveidota. Šis atvērtais sūtījums vai krava pēc tam bloķē sekojošos mēģinājumus automātiski nodot pasūtījumu, līdz jūs vai nu dzēšat atvērto sūtījumu vai kravu, vai manuāli pārstrādājiet kopumu.

## <a name="resolution"></a>Novēršana

Varat veikt izlaišanu un pārdošanas pasūtījuma lapas vai automātisko izlaišanu var veikt no laidiena pārdošanas pasūtījuma lapas, ja pirms izlaišanas uz noliktavu nav nevienas kravas. Krava tiks automātiski izveidota pēc kopuma apstrādes.
