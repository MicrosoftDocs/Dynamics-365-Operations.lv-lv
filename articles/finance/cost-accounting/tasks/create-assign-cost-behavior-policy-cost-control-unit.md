---
title: Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei
description: Izmaksu izturēšanās ir izmaksu klasifikācija fiksētajās vai mainīgajās izmaksās.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735147"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei

[!include [banner](../../includes/banner.md)]

Izmaksu izturēšanās ir izmaksu klasifikācija fiksētajās vai mainīgajās izmaksās. Lai politika stātos spēkā, politika un attiecīgās kārtulas ir jāpiešķir izmaksu vadības ierīcei. Izmantojiet šo procedūru, lai izveidotu un pēc tam piešķirtu politiku izmaksu vadības ierīcei.


## <a name="create-a-cost-behavior-hierarchy"></a>Izmaksu izturēšanās hierarhijas izveide
1. Dodieties uz **Izmaksu > dimensiju > dimensiju hierarhijām**.
2. Klikšķiniet **Jauns**.
3. Noklikšķiniet uz **Izveidot**.
4. Laukā **Dimensiju hierarhijas** nosaukums ierakstiet 'Izmaksu uzvedības hierarhija'.
5. Laukā **Dimensija** ievadiet vai atlasiet vērtību.
    * Atlasiet Izmaksu elementi.  
6. Noklikšķiniet uz **Saglabāt**.
7. Noklikšķiniet **uz Skatīt hierarhiju**.
8. Klikšķiniet **Jauns**.
9. Laukā **Zara** nosaukums ievadiet vērtību.
    * Ievadiet fiksētās izmaksas.  
10. Kokā atlasiet "Cost behavior hierarchy".
11. Klikšķiniet **Jauns**.
12. Laukā **Zara** nosaukums ievadiet vērtību.
    * Ievadiet mainīgās izmaksas.  
13. Noklikšķiniet uz **Saglabāt**.
14. Kokā atlasiet Cost behavior hierarchy\Fixed cost.
15. Klikšķiniet **Jauns**.
16. Sarakstā atzīmējiet atlasīto rindu.
17. Laukā **No dimensiju** dalībnieka ievadiet vai atlasiet vērtību.
    * Dimensiju dalībnieku diapazons var saturēt atstarpes, taču dalībnieki nevar pārklāties.  
18. Laukā **Līdz dimensijas** dalībniekam ievadiet vai atlasiet vērtību.
    * Dimensiju dalībnieku diapazons var saturēt atstarpes, taču dalībnieki nevar pārklāties.  
19. Kokā atlasiet Cost behavior hierarchy\Variable cost.
20. Klikšķiniet **Jauns**.
21. Sarakstā atzīmējiet atlasīto rindu.
22. Laukā **No dimensiju** dalībnieka ievadiet vai atlasiet vērtību.
    * Dimensiju dalībnieku diapazons var saturēt atstarpes, taču dalībnieki nevar pārklāties.  
23. Laukā **Līdz dimensijas** dalībniekam ievadiet vai atlasiet vērtību.
    * Dimensiju dalībnieku diapazons var saturēt atstarpes, taču dalībnieki nevar pārklāties.  
24. Noklikšķiniet uz **Saglabāt**.

## <a name="create-the-policy-and-rules"></a>Politikas un kārtulu izveide
1. Pārejiet uz **sadaļu Izmaksu > un > izmaksu funkcionalitātes politikām**.
2. Klikšķiniet **Jauns**.
3. Laukā **Politikas** nosaukums ievadiet vērtību.
4. Laukā **Izmaksu elementa dimensijas** hierarhija ievadiet vai atlasiet vērtību.
    * Atlasiet politikas hierarhiju, ko tikko izveidojāt.  
5. Izmaksu objektu **dimensiju hierarhijas** laukā ievadiet vai atlasiet vērtību.
    * Atlasiet Organizācija.  
6. Noklikšķiniet uz **Saglabāt**.
7. Klikšķiniet **Jauns**.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Izmaksu elementa **dimensijas hierarhijas zara** laukā Ievadiet vai atlasiet vērtību.
    * Izvērsiet hierarhiju, lai atlasītu Mainīgās izmaksas.  
10. Izmaksu objekta **dimensijas hierarhijas mezgla** laukā Izmaksu objektu dimensiju hierarhija ievadiet vai atlasiet vērtību.
    * Pēc noklusējuma mainīgā procentuālā vērtība ir 100 procenti.  
11. Noklikšķiniet **uz Politikas piešķires izmaksu kontroles vienībai**.
12. Klikšķiniet **Jauns**.
13. Sarakstā atzīmējiet atlasīto rindu.
14. Laukā **Derīgs no uzskaites** datuma ievadiet datumu.
    * Kārtulas ir efektīvas, un lietotājs vai sistēma var anulēt kārtulu, ja tiek izveidota jaunāka versija.  
15. Laukā **Izmaksu kontroles** vienība ievadiet vai atlasiet vērtību.
16. Noklikšķiniet uz **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
