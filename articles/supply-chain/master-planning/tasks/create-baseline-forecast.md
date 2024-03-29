---
title: 'Rokasgrāmata: Bāzlīnijas prognozes izveide'
description: Ražošanas plānotājs var izveidot bāzlīnijas prognozes, izmantojot laika sērijas prognozes modeļus vai kopējot vēsturisko pieprasījumu.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eb2450f0e86eb4aa9a69c9c651ab1648ca0172b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469594"
---
# <a name="guide-create-a-baseline-forecast"></a>Rokasgrāmata: Bāzlīnijas prognozes izveide

[!include [banner](../../includes/banner.md)]

Ražošanas plānotājs var izveidot bāzlīnijas prognozes, izmantojot laika sērijas prognozes modeļus vai kopējot vēsturisko pieprasījumu. Šajā procedūrā ir parādīts, kā kopēt vēsturisko pieprasījumu, lai izveidotu bāzlīnijas prognozi visām precēm, izmantojot vienu krājumu sadalījuma principu.

## <a name="set-up-an-item-allocation-key"></a>Krājumu sadalījuma principa iestatīšana

1. Pārejiet uz sadaļu **Vispārējā plānošana > Iestatījumi > Starpuzņēmumu plānošanas grupas**.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka *Nosaukums*, izmantojot vērtību *10*.
    * Pieprasījuma prognozēšana darbojas visām juridiskajām personām. Tāpēc nepieciešams iestatīt visus uzņēmumus, kuriem vēlaties ģenerēt prognozes vienā starpuzņēmumu plānošanas grupā.  
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Atlasiet **Krājumu sadalījuma principi**.
    * Atlasiet visus krājumu sadalījuma principus, kuriem vēlaties izveidot prognozes.  
5. Sarakstā atzīmējiet atlasīto rindu.
    * Atlasiet D_Aloc krājumu sadalījuma principu.  
6. Atlasīt **>**.
7. Aizvērt lapu.
8. Aizvērt lapu.

## <a name="set-up-the-demand-forecasting-parameters"></a>Pieprasījuma prognozēšanas parametru iestatīšana

1. Pārejiet uz sadaļu **Vispārējā plānošana > Iestatījumi > Pieprasījuma prognozēšana > Pieprasījuma prognozēšanas parametri**.
2. Izvērsiet **Prognozes algoritma parametru** sadaļu.
3. Laukā **Prognozes ģenerēšanas stratēģija** atlasiet **Kopēt vēsturiskā pieprasījuma vietā**.
4. Atlasiet **Saglabāt**.

## <a name="create-a-baseline-forecast"></a>Bāzlīnijas prognozes izveide

1. Pārejiet uz sadaļu **Vispārējā plānošana > Prognozēšana > Pieprasījuma prognozēšana > Ģenerēt statistisko bāzlīnijas prognozi**.
2. Ievadiet datumu laukā **No datuma**.
    * Ja jums ir pārdošanas pasūtījumi, sākot ar 2015. gada 1. janvāri, ievadiet šo datumu. Ja tā nav, ievadiet agrāko datumu no saviem pārdošanas pasūtījumiem.  
3. Ievadiet datumu laukā **Līdz datumam**.
    * Ievadiet jaunāko savu pārdošanas pasūtījumu datumu, piemēram, *2015-03-31*.  
4. Ievadiet datumu laukā **No datuma**.
    * Ievadiet *2015-04-01*. Šis datums tiks automātiski aprēķināts, lai izmantotu par nākamā prognozēšanas intervāla sākuma datumu.  
5. Izvērsiet sadaļu **Iekļaujamie ieraksti**.
6. Atlasiet **Filtrēt**.
7. Sarakstā atzīmējiet atlasīto rindu.
    * Iezīmējiet rindu, kur **Field** = *Starpuzņēmumu plānošanas grupa*.  
8. Laukā **Kritēriji** ierakstiet kādu vērtību.
    * Ierakstiet starpuzņēmumu plānošanas grupu (piemēram, *10*), kuru izmantojāt pirmajā uzdevumā.  
9. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
    * Atlasiet rindu, kurā **Field** = *Krājumu sadalījuma princips*.  
10. Laukā **Kritēriji** ierakstiet kādu vērtību.
11. Atlasiet **Labi**.
12. Izvērsiet sadaļu **Papildu parametri**.
13. Laukā **Prognozes intervāls** atlasiet *Mēnesis*.
14. Laukā **Prognozes periods** ievadiet *3*.
15. Laukā **Periods bez izmaiņām** ievadiet *1*.
16. Atlasiet **Labi**.

## <a name="visualize-the-demand-forecast"></a>Pieprasījuma prognozes vizualizēšana

1. Pārejiet uz sadaļu **Vispārējā plānošana > Prognozēšana > Pieprasījuma prognozēšana > Pielāgotā pieprasījuma prognoze**.
2. Apkoptā skatījuma tabulā atlasiet šūnu 1. rindas 2. kolonnā. Šis ir otrais mēnesis, kuram esat izveidojis prognozi.
3. Iestatiet **QtyCell** vērtību uz *400*.
    * Šūnā ievadiet citu numuru, nevis prognozēto, piemēram, 400.  
4. Esat veicis manuālās prognozes korekcijas. Ievērojiet grafisko norādi nākamajā darbībā.
5. Atlasiet **Detalizēta informācija par prognozes rindu**.
    * Šajā lapā varat apskatīt precizitātes vērtības, vēsturisko pieprasījumu un prognozi. Varat arī veikt prognožu izmaiņas.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]