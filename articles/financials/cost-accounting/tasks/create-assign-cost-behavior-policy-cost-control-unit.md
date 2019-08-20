---
title: Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei
description: Izmaksu izturēšanās ir izmaksu klasifikācija fiksētajās vai mainīgajās izmaksās.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16d9dceb4c2a22eab9a5ecb8501393444f20498b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841373"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Izmaksu izturēšanās politikas izveide un piešķiršana izmaksu vadības ierīcei

[!include [task guide banner](../../includes/task-guide-banner.md)]

Izmaksu izturēšanās ir izmaksu klasifikācija fiksētajās vai mainīgajās izmaksās. Lai politika stātos spēkā, politika un attiecīgās kārtulas ir jāpiešķir izmaksu vadības ierīcei. Izmantojiet šo procedūru, lai izveidotu un pēc tam piešķirtu politiku izmaksu vadības ierīcei.


## <a name="create-a-cost-behavior-hierarchy"></a>Izmaksu izturēšanās hierarhijas izveide
1. Dodieties uz Izmaksu uzskaite > Dimensijas > Dimensiju hierarhijas.
2. Noklikšķiniet uz Jauns.
3. Noklikšķiniet uz Izveidot.
4. Laukā Dimensiju hierarhijas nosaukums ierakstiet "Cost behavior hierarchy".
5. Laukā Dimensija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Izmaksu elementi.  
6. Noklikšķiniet uz Saglabāt.
7. Noklikšķiniet uz Skatīt hierarhiju.
8. Noklikšķiniet uz Jauns.
9. Laukā Zara nosaukums ierakstiet kādu vērtību.
    * Ievadiet fiksētās izmaksas.  
10. Kokā atlasiet "Cost behavior hierarchy".
11. Noklikšķiniet uz Jauns.
12. Laukā Zara nosaukums ierakstiet kādu vērtību.
    * Ievadiet mainīgās izmaksas.  
13. Noklikšķiniet uz Saglabāt.
14. Kokā atlasiet Cost behavior hierarchy\Fixed cost.
15. Noklikšķiniet uz Jauns.
16. Sarakstā atzīmējiet atlasīto rindu.
17. Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.
    * Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.  
18. Laukā Mērķa dimensijas elements ievadiet vai atlasiet kādu vērtību.
    * Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.  
19. Kokā atlasiet Cost behavior hierarchy\Variable cost.
20. Noklikšķiniet uz Jauns.
21. Sarakstā atzīmējiet atlasīto rindu.
22. Laukā Avota dimensijas elements ievadiet vai atlasiet kādu vērtību.
    * Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.  
23. Laukā Mērķa dimensijas elements ievadiet vai atlasiet kādu vērtību.
    * Dimensijas elementu diapazons var saturēt atstarpes, bet elementi nedrīkst pārklāties.  
24. Noklikšķiniet uz Saglabāt.

## <a name="create-the-policy-and-rules"></a>Politikas un kārtulu izveide
1. Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu izturēšanās politikas.
2. Noklikšķiniet uz Jauns.
3. Laukā Politikas nosaukums ierakstiet kādu vērtību.
4. Laukā Izmaksu elementa dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet politikas hierarhiju, ko tikko izveidojāt.  
5. Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Organizācija.  
6. Noklikšķiniet uz Saglabāt.
7. Noklikšķiniet uz Jauns.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Laukā Izmaksu elementa dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Izvērsiet hierarhiju, lai atlasītu Mainīgās izmaksas.  
10. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
    * Pēc noklusējuma mainīgā procentuālā vērtība ir 100 procenti.  
11. Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.
12. Noklikšķiniet uz Jauns.
13. Sarakstā atzīmējiet atlasīto rindu.
14. Laukā Derīgs no uzskaites datuma ievadiet datumu.
    * Kārtulas ir efektīvas, un lietotājs vai sistēma var anulēt kārtulu, ja tiek izveidota jaunāka versija.  
15. Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.
16. Noklikšķiniet uz Saglabāt.

