---
title: "Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi"
description: "Šajā rakstā ir aprakstīts, kā izslēgt novirzes punktus no vēsturiskajiem datiem, kas tiek izmantoti, lai aprēķinātu pieprasījuma apjoma prognozi. Izslēdzot novirzes punktus, jūs varat uzlabot prognozes precizitāti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi

Šajā rakstā ir aprakstīts, kā izslēgt novirzes punktus no vēsturiskajiem datiem, kas tiek izmantoti, lai aprēķinātu pieprasījuma apjoma prognozi. Izslēdzot novirzes punktus, jūs varat uzlabot prognozes precizitāti.

Varat izslēgt galējos punktus, lai uzlabotu prognozes precizitāti. Šis uzdevums nav obligāts. Tālāk ir sniegts šī procesa apskats.

1.  Noklikšķiniet uz **vispārējā plānošana**&gt;**Setup**&gt;**pieprasījuma prognozēšanas**&gt;**nepiederoša noņemšanas** atvērt **nepiederoša noņemšanas** lapu, kur var izmantot vaicājumu, lai atlasītu darbības, kas neietver.
2.  Atlasiet uzņēmumu, uz kuru attiecas šis vaicājums, un pēc tam ievadiet nosaukumu un aprakstu. Lauks **Vaicājuma datums** automātiski tiek iestatīts uz pašreizējo datumu.
3.  Atzīmējiet izvēles rūtiņu **Aktīvs**, lai no vēsturiskajiem datiem izslēgtu transakcijas, ko šis vaicājums atrod. Šis iestatījums stāsies spēkā pēc bāzlīnijas prognozes izveides.
4.  Lapā **Novirzes punktu noņemšanas vaicājums** varat pievienot, noņemt un atlasīt kritērijus, kas definē, kuras transakcijas tiks izslēgtas, kad tiek aprēķināta bāzlīnijas prognoze. Piemēram, atlasiet noteiktu krājumu vai pasūtījuma transakciju, ko izslēgt.
5.  Noklikšķiniet uz **Rādīt transakcijas**. Lapā **Novirzes punktu transakcijas** ir uzskaitītas transakcijas, kas atbilst kritērijiem, kurus definējāt vaicājumā, un kas tiks izslēgtas no vēsturiskajiem datiem, kad tiek aprēķināta pieprasījuma apjoma prognoze.

**Piezīme.** Varat arī izveidot vaicājumu, kas ir balstīts uz esošu vaicājumu. Atlasiet vaicājumu, ko vēlaties kopēt, un pēc tam noklikšķiniet uz **Dublēt**. Laukā **Vaicājuma datums** tiek identificēta versija. Šo vaicājumu var lietot tādu, kāds tas ir, vai varat noklikšķināt uz **Rediģēt vaicājumu**, lai modificētu kritērijus. Pēc izvēles varat modificēt jaunā vaicājuma nosaukumu un aprakstu.

<a name="see-also"></a>Skatiet arī
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


