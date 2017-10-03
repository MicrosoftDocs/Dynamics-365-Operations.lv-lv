---
title: "Prognozes precizitātes pārraudzība"
description: "Šajā rakstā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations aprēķināto prognožu precizitātes tipi, un ir paskaidrots, kā varat skatīt precizitātes vērtības."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 56d3f0312e684ab076f9116ac6638bcd67b52e58
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="monitor-forecast-accuracy"></a>Prognozes precizitātes pārraudzība

[!include[banner](../includes/banner.md)]


Šajā rakstā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations aprēķināto prognožu precizitātes tipi, un ir paskaidrots, kā varat skatīt precizitātes vērtības.

Programmatūrā Finance and Operations tiek aprēķināti tālāk norādītie prognozes precizitātes tipi.

-   Vēsturiskās prognozes precizitāte, salīdzinot vēsturisko prognozi, ko izmanto vispārējā plānošanā kopā ar vēsturiskā pieprasījuma datiem. Lai skatītu vēsturiskās prognozes precizitātes vērtības (gan absolūtās, gan procentuālās vērtības), noklikšķiniet uz **Rādīt precizitāti** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.
-   Prognožu ģenerēšanai izmantotā prognozēšanas modeļa aprēķināta precizitāte. Procentuālo precizitāti var skatīt sadaļā **Detalizēti modeļa dati - MAPE** lapā **Detalizēti pieprasījuma apjoma prognozes dati**. 

**Piezīme.** Ja izmantojat Finance and Operations Microsoft Azure algoritmiskās mācīšanās pakalpojumu Pieprasījuma prognozēšana, iekšējā modeļa precizitāte tiek aprēķināta, pamatojoties uz testa datu kopu. ai norādītu testa datu kopas izmēru, iestatiet parametru **TEST\_SET\_SIZE\_PERCENT** lapā **Pieprasījuma prognozēšanas parametri**. Piemēram, ja tiek iestatīta vērtība **20**, pēdējie vēsturisko datu 20 % tiks izmantoti, lai aprēķinātu iekšējā modeļa precizitāti.


<a name="see-also"></a>Skatiet arī
--------

[Koriģētās prognozes autorizēšana](authorize-adjusted-forecast.md)

[Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi](remove-historical-outliers-calculating-demand-forecast.md)




