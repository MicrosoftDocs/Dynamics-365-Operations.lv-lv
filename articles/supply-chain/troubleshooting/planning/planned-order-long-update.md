---
title: Plānoto pasūtījumu atjaunināšanai vajadzīgs ilgs laiks
description: Atjauninot pieprasījuma daudzumu un/vai piegādes datuma plānotā pasūtījumā, parasti ir vajadzīgas vismaz 30 sekundes, lai katram pasūtījumam saglabātu atjauninājumu
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
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476997"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Plānoto pasūtījumu atjaunināšanai vajadzīgs ilgs laiks

## <a name="symptoms"></a>Simptomi

Atjauninot vajadzības daudzumu un/vai piedāvājuma datumu plānotajā pasūtījumā, parasti katrā pasūtījumā ir nepieciešamas vismaz 30 sekundes, lai saglabātu atjauninājumu.

## <a name="resolution"></a>Novēršana

Šī ir zināma problēma iebūvētajā vispārējās plānošanas programmā. Tas ir saistīts ar pamata automātisko izvēršanu rediģēšanas laikā, izmantojot MK struktūru. Šī problēma ir adresēta Plānošanas optimizācijā, kur plānotājs var atjaunināt un apstiprināt atbilstošos pasūtījumus un, ja nepieciešams, aktivizēt plānošanas izpildi, lai atjauninātu plānotos pasūtījumus pamata MK struktūrai.

Viens veids, kādā uzlabot veiktspēju ar iebūvēto galvenās plānošanas rīku, ir, izpildot šīs darbības:

1. Dodieties uz **Vispārējā plānošana \> Iestatījumi \> Plāni \> Vispārējie plāni**.
1. Atlasiet plānu.
1. Izvērsiet kopsavilkuma cilni **Laika robeža dienās**.
1. Iestatiet **Izvēršana** uz *Jā* un iestatiet lauku zem šī iestatījuma uz 0 (nulle).

> [!NOTE]
> Tas ierobežos šim vispārējam plānam veikto sprādzienu periodu uz vienu dienu.
