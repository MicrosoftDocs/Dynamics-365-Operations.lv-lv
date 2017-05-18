---
title: "Prognozes precizitātes pārraudzība"
description: "Šajā tēmā ir aprakstīti prognozes precizitātes veidi, kas tiek aprēķināti programmatūrā Microsoft Dynamics 365 for Operations un ir paskaidrots, kā varat skatīt precizitātes vērtības."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7e470e05d9acb1e7417d0d77655be99e94d15e1d
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="monitor-forecast-accuracy"></a>Prognozes precizitātes pārraudzība

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīti prognozes precizitātes veidi, kas tiek aprēķināti programmatūrā Microsoft Dynamics 365 for Operations un ir paskaidrots, kā varat skatīt precizitātes vērtības.

Programmatūrā Dynamics 365 for Operations tiek aprēķināti tālāk norādītie prognozes precizitātes veidi.

-   Vēsturiskās prognozes precizitāte, salīdzinot vēsturisko prognozi, ko izmanto vispārējā plānošanā kopā ar vēsturiskā pieprasījuma datiem. Lai skatītu vēsturiskās prognozes precizitātes vērtības (gan absolūtās, gan procentuālās vērtības), noklikšķiniet uz **Rādīt precizitāti** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.
-   Prognožu ģenerēšanai izmantotā prognozēšanas modeļa aprēķināta precizitāte. Procentuālo precizitāti var skatīt sadaļā **Detalizēti modeļa dati - MAPE** lapā **Detalizēti pieprasījuma apjoma prognozes dati**. 

**Piezīme.** Ja izmantojat Dynamics 365 for Operations Microsoft Azure algoritmiskās mācīšanās pakalpojumu Pieprasījuma prognozēšana, iekšējā modeļa precizitāte tiek aprēķināta, pamatojoties uz testa datu kopu. ai norādītu testa datu kopas izmēru, iestatiet parametru **TEST\_SET\_SIZE\_PERCENT** lapā **Pieprasījuma prognozēšanas parametri**. Piemēram, ja tiek iestatīta vērtība **20**, pēdējie vēsturisko datu 20 % tiks izmantoti, lai aprēķinātu iekšējā modeļa precizitāti.


<a name="see-also"></a>Skatiet arī
--------

[Koriģētās prognozes autorizēšana](authorize-adjusted-forecast.md)

[Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi](remove-historical-outliers-calculating-demand-forecast.md)




