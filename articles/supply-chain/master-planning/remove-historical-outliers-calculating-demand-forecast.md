---
title: Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi
description: Šajā rakstā ir aprakstīts, kā izslēgt novirzes punktus no vēsturiskajiem datiem, kas tiek izmantoti, lai aprēķinātu pieprasījuma apjoma prognozi. Izslēdzot novirzes punktus, jūs varat uzlabot prognozes precizitāti.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup, ReqDemPlanOutlierQueryPreview
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc0826d3a0dd8ded19590867e9a8138bb772c89a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568643"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izslēgt novirzes punktus no vēsturiskajiem datiem, kas tiek izmantoti, lai aprēķinātu pieprasījuma apjoma prognozi. Izslēdzot novirzes punktus, jūs varat uzlabot prognozes precizitāti.

Varat izslēgt novirzes punktus, lai uzlabotu prognozes precizitāti. Šis uzdevums nav obligāts. Tālāk ir sniegts šī procesa apskats.

1.  Noklikšķiniet uz **Vispārējā plānošana** &gt; **Iestatījumi** &gt; **Pieprasījuma prognozēšana** &gt; **Nepiederošas personas noņemšana**, lai atvērtu lapu **Nepiederošas personas noņemšana**, kurā varat izmantot vaicājumu, lai atlasītu izslēdzamās transakcijas.
2.  Atlasiet uzņēmumu, uz kuru attiecas šis vaicājums, un pēc tam ievadiet nosaukumu un aprakstu. Lauks **Vaicājuma datums** automātiski tiek iestatīts uz pašreizējo datumu.
3.  Atzīmējiet izvēles rūtiņu **Aktīvs**, lai no vēsturiskajiem datiem izslēgtu transakcijas, ko šis vaicājums atrod. Šis iestatījums stāsies spēkā pēc bāzlīnijas prognozes izveides.
4.  Lapā **Novirzes punktu noņemšanas vaicājums** varat pievienot, noņemt un atlasīt kritērijus, kas definē, kuras transakcijas tiks izslēgtas, kad tiek aprēķināta bāzlīnijas prognoze. Piemēram, atlasiet noteiktu krājumu vai pasūtījuma transakciju, ko izslēgt.
5.  Noklikšķiniet uz **Rādīt transakcijas**. Lapā **Novirzes punktu transakcijas** ir uzskaitītas transakcijas, kas atbilst kritērijiem, kurus definējāt vaicājumā, un kas tiks izslēgtas no vēsturiskajiem datiem, kad tiek aprēķināta pieprasījuma apjoma prognoze.

**Piezīme.** Varat arī izveidot vaicājumu, kas ir balstīts uz esošu vaicājumu. Atlasiet vaicājumu, ko vēlaties kopēt, un pēc tam noklikšķiniet uz **Dublēt**. Laukā **Vaicājuma datums** tiek identificēta versija. Šo vaicājumu var lietot tādu, kāds tas ir, vai varat noklikšķināt uz **Rediģēt vaicājumu**, lai modificētu kritērijus. Pēc izvēles varat modificēt jaunā vaicājuma nosaukumu un aprakstu.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par pieprasījuma prognozēšanu](introduction-demand-forecasting.md)

[Prognozes precizitātes pārraudzība](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]