---
title: "Monitora prognoze precizitāte"
description: "Šajā rakstā sniegts budžeta precizitātes Microsoft Dynamics 365 operācijām aprēķina un izskaidrots, kā var skatīt precizitātes vērtības veidu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Monitora prognoze precizitāte

Šajā rakstā sniegts budžeta precizitātes Microsoft Dynamics 365 operācijām aprēķina un izskaidrots, kā var skatīt precizitātes vērtības veidu.

Šāda veida prognozes precizitāti aprēķina dinamika 365 operācijām:

-   Vēsturiskās prognozes precizitāte, salīdzinot vēsturisko prognozi, ko izmanto vispārējā plānošanā kopā ar vēsturiskā pieprasījuma datiem. Lai skatītu vēsturiskās prognozes precizitātes vērtības (gan absolūtās, gan procentuālās vērtības), noklikšķiniet uz **Rādīt precizitāti** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.
-   Prognožu ģenerēšanai izmantotā prognozēšanas modeļa aprēķināta precizitāte. Procentuālo precizitāti var skatīt sadaļā **Detalizēti modeļa dati - MAPE** lapā **Detalizēti pieprasījuma apjoma prognozes dati**. 

**Piezīme:** ja Dynamics 365 izmantošanai operāciju pieprasījuma prognozēšanas Microsoft Azure mašīnu apmācības pakalpojumu iekšējā modeļa precizitāti aprēķina pamatā ir testa datu kopu. Norādīt lielumu testa datu kopu, kas **TEST\_noteikt\_lielums\_procenti** parametru par **pieprasījuma prognozēšanas parametrus** lapu. Piemēram, ja tiek iestatīta vērtība **20**, pēdējie vēsturisko datu 20 % tiks izmantoti, lai aprēķinātu iekšējā modeļa precizitāti.


<a name="see-also"></a>Skatiet arī
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


