---
title: Prognozes precizitātes pārraudzība
description: Šajā tēmā ir aprakstīti programmā Dynamics 365 Supply Chain Management aprēķinātās prognozes precizitātes veidi un ir paskaidrots, kā varat skatīt precizitātes vērtības.
author: t-benebo
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebde5ab90b9345b3d6f28ea98650b3b29021c304
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893357"
---
# <a name="monitor-forecast-accuracy"></a>Prognozes precizitātes pārraudzība

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti prognozes precizitātes veidi, ko Microsoft Dynamics 365 Supply Chain Management aprēķina, un skaidrots, kā varat skatīt precizitātes vērtības.

Supply Chain Management tiek aprēķināti tālāk norādītie prognozes precizitātes tipi.

-   Vēsturiskās prognozes precizitāte, salīdzinot vēsturisko prognozi, ko izmanto vispārējā plānošanā kopā ar vēsturiskā pieprasījuma datiem. Lai skatītu vēsturiskās prognozes precizitātes vērtības (gan absolūtās, gan procentuālās vērtības), noklikšķiniet uz **Rādīt precizitāti** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.
-   Prognožu ģenerēšanai izmantotā prognozēšanas modeļa aprēķināta precizitāte. Procentuālo precizitāti var skatīt sadaļā **Detalizēti modeļa dati - MAPE** lapā **Detalizēti pieprasījuma apjoma prognozes dati**. 

> [!NOTE]
> Ja izmantojat Microsoft Azure algoritmiskās mācīšanās pakalpojumu Pieprasījuma prognozēšana, iekšējā modeļa precizitāte tiek aprēķināta, pamatojoties uz testa datu kopu. ai norādītu testa datu kopas izmēru, iestatiet parametru **TEST\_SET\_SIZE\_PERCENT** lapā **Pieprasījuma prognozēšanas parametri**. Piemēram, ja tiek iestatīta vērtība **20**, pēdējie vēsturisko datu 20 % tiks izmantoti, lai aprēķinātu iekšējā modeļa precizitāti.


## <a name="additional-resources"></a>Papildu resursi

[Autorizēt koriģēto pieprasījuma apjoma prognozi](authorize-adjusted-forecast.md)

[Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi](remove-historical-outliers-calculating-demand-forecast.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]