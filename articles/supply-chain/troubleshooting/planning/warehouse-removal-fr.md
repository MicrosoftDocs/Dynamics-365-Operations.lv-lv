---
title: Nevar noņemt noliktavas pieprasījuma apjoma prognozes dimensiju no prognozes rindām
description: Nevar noņemt noliktavas pieprasījuma apjoma prognozes dimensiju no prognozes rindām.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741217"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Nevar noņemt noliktavas pieprasījuma apjoma prognozes dimensiju no prognozes rindām

KB numurs: 4614408

## <a name="symptoms"></a>Simptomi

Šī problēma rodas, ja **Noliktavas** dimensija nav piešķirta cilnes **Prognozes dimensijas** laukā **Pieprasījuma apjoma prognozes parametri**. Tomēr kolonna **Noliktava** tiek parādīta lapā **Pieprasījuma apjoma prognoze** (**Vispārējā plānošana \> Prognozēšana \> Manuālās prognozes elements \> Pieprasījuma apjoma prognozes rindas**).

## <a name="resolution"></a>Novēršana

Cilnes **Prognozes dimensijas** iestatījumi lapā **Pieprasījuma apjoma prognozes parametri** neietekmē lapu **Pieprasījuma apjoma prognoze**. Tie kontrolē bāzlīnijas prognozi, kas tiek ģenerēta un parādīta pielāgotajā pieprasījuma apjoma prognozē. Tomēr tie nekontrolē dimensijas, kas ir nepieciešamas "reālajai" pieprasījuma apjoma prognozei. Autorizējot ierakstus, kas tiek rādīti lapā **Pielāgotā pieprasījuma apjoma prognoze**, tos var pārveidot par "reāliem" prognozes modeļa ierakstiem. Šo modeli pēc tam var izmantot vispārējai plānošanai.

Lapā **Pieprasījuma apjoma prognoze** "reālās" prognozes dimensijas, kas parādītas pieprasījuma apjoma prognožu rindās, ir daļa no krājumu dimensijām. (Šī darbība ir līdzīga pārdošanas pasūtījumu rindu uzvedībai.) Ja jūsu sistēmā nav iestatīts lietot **Noliktavu** kā obligātu krājumu dimensiju, lapu var pielāgot, lai paslēptu kolonnu.
