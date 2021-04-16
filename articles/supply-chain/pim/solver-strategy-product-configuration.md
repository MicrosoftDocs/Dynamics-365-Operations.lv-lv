---
title: Risinātāja stratēģija preces konfigurācijai
description: Šajā tēmā ir aprakstīts, kā varat izmantot risinātāja stratēģiju, lai uzlabotu preču konfigurāciju.
author: cvocph
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 82332a8ac8a68f5a9092ae08a094514827f39113
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812719"
---
# <a name="solver-strategy-for-product-configuration"></a>Risinātāja stratēģija preces konfigurācijai

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā varat izmantot risinātāja stratēģiju, lai uzlabotu preču konfigurāciju.

Risinātāja stratēģiju koncepcija pirmoreiz tika ieviesta Microsoft Dynamics AX 2012 R2 7. kumulatīvajā atjauninājumā (CU7). Tā tika paplašināta Microsoft Dynamics AX 2012 R3 8. kumulatīvajā atjauninājumā (CU8) un risinājumā Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.

Risinātāja stratēģijas koncepcijā tagad ir ietvertas tālāk norādītās stratēģijas.

- Noklusētā vērtība
- Vispirms domēni ar minimālu vērtību skaitu
- No augšas uz leju
- Z3

## <a name="solver-strategy"></a>Risinātāja stratēģija 

Preces konfigurācijas modeli var formulēt kā [ierobežojuma apmierinātības problēmu (CSP — Constraint Satisfaction Problem)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf). Microsoft Solver Foundation (MSF) nodrošina divu veidu risinātāja stratēģijas CSP gadījumu atrisināšanai, ko var izmantot no preču konfigurācijas modeļiem. Šo risinātāja stratēģiju pamatā ir [heiristika](https://techterms.com/definition/heuristic), ko izmanto, lai noteiktu secību, kādā problēmas risināšanas laikā tiek ņemti vērā CSP gadījumu mainīgie. Heiristika var ievērojami ietekmēt veiktspēju, kad tiek risināta problēma vai problēmu klase.

Preču konfigurācijas modeļu risinātāja stratēģija nosaka, kurš risinātājs tiek izmantots heiristikai. Stratēģijas **Noklusējuma**, **Vispirms domēni ar minimālu vērtību skaitu** un **No augšas uz leju** izmanto divus MSF risinātājus, savukārt stratēģija **Z3** izmanto Z3 risinātāju. 

Reālu debitoru ieviešanas gadījumu pētījumi liecina, ka, mainot preces konfigurācijas modeļa risinātāja stratēģiju, reakcijas laiks var tikt samazināts no minūtēm līdz milisekundēm. Tādēļ ir vērts izmēģināt dažādas risinātāja stratēģijas, lai atrastu visefektīvāko stratēģiju savam preces konfigurācijas modelim.

## <a name="change-the-settings-for-the-solver-strategy"></a>Risinātāja stratēģijas iestatījumu maiņa

Lai mainītu risinātāja stratēģiju, lapas **Preču konfigurācijas modeļi** darbību rūtī atlasiet vienumu **Modeļa rekvizīti**. Pēc tam dialoglodziņā **Rediģēt detalizētu informāciju par modeli** atlasiet risinātāja stratēģiju.

[![Risinātāja stratēģijas maiņa](./media/solver-strategy.png)](./media/solver-strategy.png)

Pašlaik nav loģikas, kas automātiski nosaka, kura risinātāja stratēģija ir visefektīvākā stratēģija preces konfigurācijai, kuras pamatā ir ierobežojums. Tādēļ jums risinātāja stratēģijas jāizmēģina pa vienai.

Tālāk esošajā tabulā sniegti ieteikumi par risinātāja stratēģijas izmantošanu dažādos scenārijos.

| Risinātāja stratēģija      | Stratēģijas izmantošana šajā scenārijā |
|----------------------|-----------------------------------|
| Noklusētā vērtība              | Stratēģija **Noklusējuma** ir optimizēta tādu modeļu risināšanai, kuru pamatā ir tabulas ierobežojumi. Debitoru ieviešanas gadījumu pētījumi liecina, ka šī stratēģija ir visefektīvākā stratēģija scenārijos, kuros plaši tiek izmantoti tabulas ierobežojumi. |
| Vispirms domēni ar minimālu vērtību skaitu | Stratēģijas **Vispirms domēni ar minimālu vērtību skaitu** un **No augšas uz leju** ir cieši saistītas. Debitoru ieviešanas gadījumu pētījumi liecina, ka stratēģija **No augšas uz leju** sniedz labākus rezultātu nekā stratēģija **Vispirms domēni ar minimālu vērtību skaitu**. Tomēr produktā ir saglabāta stratēģija **Vispirms domēni ar minimālu vērtību skaitu**, lai nodrošinātu atpakaļsaderību. Pierādīts, ka abas šīs risinātāja stratēģijas efektīvāk risina modeļus, kas satur vairākas aritmētiskas izteiksmes bez tabulas ierobežojumiem. Taču dažos gadījumos stratēģija **Noklusējuma** pārspēj abas šīs stratēģijas. Tādēļ izmēģiniet katru stratēģiju. |
| No augšas uz leju             | Stratēģijas **Vispirms domēni ar minimālu vērtību skaitu** un **No augšas uz leju** ir cieši saistītas. Debitoru ieviešanas gadījumu pētījumi liecina, ka stratēģija **No augšas uz leju** sniedz labākus rezultātu nekā stratēģija **Vispirms domēni ar minimālu vērtību skaitu**. Tomēr produktā ir saglabāta stratēģija **Vispirms domēni ar minimālu vērtību skaitu**, lai nodrošinātu atpakaļsaderību. Pierādīts, ka abas šīs risinātāja stratēģijas efektīvāk risina modeļus, kas satur vairākas aritmētiskas izteiksmes bez tabulas ierobežojumiem. Taču dažos gadījumos stratēģija **Noklusējuma** pārspēj abas šīs stratēģijas. Tādēļ izmēģiniet katru stratēģiju. |
| Z3                   | Kā noklusējuma risinātāja stratēģiju ieteicams izmantot stratēģiju **Z3**. Ja uztraucaties par veiktspēju un mērogojamību, varat izvērtēt pārējās stratēģijas. |

## <a name="additional-resources"></a>Papildu resursi

[Preces konfigurācijas pārskats](build-product-configuration-model.md)

[Heiristika](https://techterms.com/definition/heuristic)

[Ierobežojuma apmierinātības problēma](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]