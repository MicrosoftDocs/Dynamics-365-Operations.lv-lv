--- 
title: "Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei"
description: "Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 82319d8d9c7b567f98dfd0e591cb99079fb577b7
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei

[!include[task guide banner](../../includes/task-guide-banner.md)]

Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei. Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.


## <a name="create-a-policy"></a>Politikas izveide
1. Dodieties uz Izmaksu uzskaite > Politikas > Izmaksu sadalījuma politikas.
2. Noklikšķiniet uz Jauns.
3. Laukā Politikas nosaukums ierakstiet kādu vērtību.
4. Laukā Izmaksu objekta dimensiju hierarhija ievadiet vai atlasiet kādu vērtību.
    * Atlasiet Organizācija.  
5. Laukā Statistiskā dimensija ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz Saglabāt.

## <a name="create-allocation-rules"></a>Sadalījuma kārtulu izveide
1. Noklikšķiniet uz Jauns.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
4. Laukā Izmaksu izturēšanās atlasiet "Total".
5. Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz Jauns.
7. Sarakstā atzīmējiet atlasīto rindu.
8. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
9. Laukā Izmaksu izturēšanās atlasiet "Total".
10. Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.
11. Noklikšķiniet uz Jauns.
12. Sarakstā atzīmējiet atlasīto rindu.
13. Laukā Izmaksu objekta dimensiju hierarhijas zars ievadiet vai atlasiet kādu vērtību.
14. Laukā Izmaksu izturēšanās atlasiet "Total".
15. Laukā Sadalījuma pamats ievadiet vai atlasiet kādu vērtību.
    * Turpiniet, līdz esat izveidojis visas kārtulas.  
16. Noklikšķiniet uz Saglabāt.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Politikas piešķiršana izmaksu vadības ierīcei
1. Noklikšķiniet uz Izmaksu vadības ierīces politikas piešķires.
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Derīgs no uzskaites datuma ievadiet datumu.
    * Kārtulas ir efektīvas. Lietotājs vai sistēma var anulēt kārtulas, ja tiek izveidota jaunāka versija.  
5. Laukā Izmaksu vadības ierīce ievadiet vai atlasiet kādu vērtību.
6. Noklikšķiniet uz Saglabāt.


