---
title: Produktu plānošanā netiek ņemtas vērā drošības robežas.
description: Produktu plānošanā netiek ņemtas vērā drošības robežas, kuras ir iestatītas pieprasītās piegādes krājumu segumā
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 738296b7570ded0a4ee806e4445204a68e6a08c8
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476963"
---
# <a name="production-scheduling-doesnt-consider-the-safety-margins"></a>Produktu plānošanā netiek ņemtas vērā drošības robežas.

## <a name="symptoms"></a>Simptomi

Vispārējā plānošanā tiek aplūkotas drošības rezerves. Tomēr drošības rezerves tiek ignorētas, kad ir paredzēti plānoti ražošanas pasūtījumi.

## <a name="resolution"></a>Novēršana

Rezerves tiek apsvērtas tikai vispārējās plānošanas laikā, nevis manuālajā plānošanā. Rezerves ir paredzētas, lai tā darbotos kā buferis plānošanas fāzes laikā, lai piešķirtu kādam "rezervi" faktiskajam procesam.

Lai iegūtu vēlamo rezultātu, varat noņemt rezervi. Pēc tam maršruts ir jāatjaunina, lai tas ietvertu vēlamo laiku (piemēram, kā gaidīšanas laiku). Tad gan vispārējā plānošana, gan manuālā plānošana uzrāda tādu pašu rezultātu.
