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
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026714"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Nevar noņemt noliktavas pieprasījuma apjoma prognozes dimensiju no prognozes rindām

KB numurs: 4614408

## <a name="symptoms"></a>Simptomi

Šī problēma rodas, ja **Noliktavas** dimensija nav piešķirta cilnes **Prognozes dimensijas** laukā **Pieprasījuma apjoma prognozes parametri**. Tomēr kolonna **Noliktava** tiek parādīta lapā **Pieprasījuma apjoma prognoze** (**Vispārējā plānošana \> Prognozēšana \> Manuālās prognozes elements \> Pieprasījuma apjoma prognozes rindas**).

## <a name="resolution"></a>Novēršana

Cilnes **Prognozes dimensijas** iestatījumi lapā **Pieprasījuma apjoma prognozes parametri** neietekmē lapu **Pieprasījuma apjoma prognoze**. Tie kontrolē bāzlīnijas prognozi, kas tiek ģenerēta un parādīta pielāgotajā pieprasījuma apjoma prognozē. Tomēr tie nekontrolē dimensijas, kas ir nepieciešamas "reālajai" pieprasījuma apjoma prognozei. Autorizējot ierakstus, kas tiek rādīti lapā **Pielāgotā pieprasījuma apjoma prognoze**, tos var pārveidot par "reāliem" prognozes modeļa ierakstiem. Šo modeli pēc tam var izmantot vispārējai plānošanai.

Lapā **Pieprasījuma apjoma prognoze** "reālās" prognozes dimensijas, kas parādītas pieprasījuma apjoma prognožu rindās, ir daļa no krājumu dimensijām. (Šī darbība ir līdzīga pārdošanas pasūtījumu rindu uzvedībai.) Ja jūsu sistēmā nav iestatīts lietot **Noliktavu** kā obligātu krājumu dimensiju, lapu var pielāgot, lai paslēptu kolonnu.
