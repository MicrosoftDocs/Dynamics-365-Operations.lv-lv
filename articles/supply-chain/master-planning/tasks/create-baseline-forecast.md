--- 
title: "Bāzlīnijas prognozes izveide"
description: "Ražošanas plānotājs var izveidot bāzlīnijas prognozes, izmantojot laika sērijas prognozes modeļus vai kopējot vēsturisko pieprasījumu."
author: YuyuScheller
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: 6a712077fed4a94ae6ae6ce7ea2cfba8848e5fa5
ms.contentlocale: lv-lv
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-baseline-forecast"></a>Bāzlīnijas prognozes izveide

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ražošanas plānotājs var izveidot bāzlīnijas prognozes, izmantojot laika sērijas prognozes modeļus vai kopējot vēsturisko pieprasījumu. Šajā procedūrā ir parādīts, kā kopēt vēsturisko pieprasījumu, lai izveidotu bāzlīnijas prognozi visām precēm, izmantojot vienu krājumu sadalījuma principu. 


## <a name="set-up-an-item-allocation-key"></a>Krājumu sadalījuma principa iestatīšana
1. Pārejiet uz sadaļu Vispārējā plānošana > Iestatījumi > Starpuzņēmumu plānošanas grupas.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Nosaukums, izmantojot vērtību "10".
    * Pieprasījuma prognozēšana darbojas visām juridiskajām personām. Tāpēc nepieciešams iestatīt visus uzņēmumus, kuriem vēlaties ģenerēt prognozes vienā starpuzņēmumu plānošanas grupā.  
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Noklikšķiniet uz Krājumu sadalījuma principi.
    * Atlasiet visus krājumu sadalījuma principus, kuriem vēlaties izveidot prognozes.  
5. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet D_Aloc krājumu sadalījuma principu.  
6. Noklikšķiniet uz >.
7. Aizvērt lapu.
8. Aizvērt lapu.

## <a name="set-up-the-demand-forecasting-parameters"></a>Pieprasījuma prognozēšanas parametru iestatīšana
1. Pārejiet uz sadaļu Vispārējā plānošana > Iestatījumi > Pieprasījuma prognozēšana > Pieprasījuma prognozēšanas parametri.
2. Izvērsiet prognozes algoritma parametru sadaļu.
3. Laukā Prognozes ģenerēšanas stratēģija atlasiet Kopēt vēsturiskā pieprasījuma vietā.
4. Noklikšķiniet uz Saglabāt.

## <a name="create-a-baseline-forecast"></a>Bāzlīnijas prognozes izveide
1. Pārejiet uz sadaļu Vispārējā plānošana > Prognozēšana > Pieprasījuma prognozēšana > Ģenerēt statistisko bāzlīnijas prognozi.
2. Ievadiet datumu laukā No datuma.
    * Ja jums ir pārdošanas pasūtījumi, sākot ar 2015. gada 1. janvāri, ievadiet šo datumu. Ja tā nav, ievadiet agrāko datumu no saviem pārdošanas pasūtījumiem.  
3. Laukā Līdz datumam ievadiet datumu.
    * Ievadiet jaunāko savu pārdošanas pasūtījumu datumu, piemēram, “2015-03-31”.  
4. Ievadiet datumu laukā No datuma.
    * Ievadiet “2015-04-01”. Šis datums tiks automātiski aprēķināts, lai izmantotu par nākamā prognozēšanas intervāla sākuma datumu.  
5. Izvērsiet sadaļu Iekļaujamie ieraksti.
6. Noklikšķiniet uz Filtrēt.
7. Sarakstā atzīmējiet atlasīto rindu.
    * Iezīmējiet rindu, kur lauka vērtība ir starpuzņēmumu plānošanas grupa.  
8. Laukā Kritēriji ierakstiet kādu vērtību.
    * Ierakstiet starpuzņēmumu plānošanas grupu, piemēram, 10, kuru izmantojāt pirmajā uzdevumā.  
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet rindu, kurā lauka vērtība ir krājumu sadalījuma princips.  
10. Laukā Kritēriji ierakstiet kādu vērtību.
11. Noklikšķiniet uz OK.
12. Izvērsiet sadaļu Papildu parametri.
13. Laukā Prognozes intervāls atlasiet "Mēnesis".
14. Laukā Prognozes periods ievadiet "3".
15. Laukā Periods bez izmaiņām ievadiet “1”.
16. Noklikšķiniet uz OK.

## <a name="visualize-the-demand-forecast"></a>Pieprasījuma prognozes vizualizēšana
1. Pārejiet uz sadaļu Vispārējā plānošana > Prognozēšana > Pieprasījuma prognozēšana > Pielāgotā pieprasījuma prognoze.
2. Apkoptā skatījuma tabulā atlasiet šūnu 1. rindas 2. kolonnā. Šis ir otrais mēnesis, kuram esat izveidojis prognozi.
3. Iestatiet QtyCell vērtību "400".
    * Šūnā ievadiet citu numuru, nevis prognozēto, piemēram, 400.  
4. Esat veicis manuālās prognozes korekcijas. Ievērojiet grafisko norādi nākamajā darbībā.
5. Noklikšķiniet uz Detalizēta informācija par prognozes rindu.
    * Šajā lapā var apskatīt precizitātes, vēsturiskā pieprasījuma un prognozes vērtības. Varat arī veikt prognožu izmaiņas.  


