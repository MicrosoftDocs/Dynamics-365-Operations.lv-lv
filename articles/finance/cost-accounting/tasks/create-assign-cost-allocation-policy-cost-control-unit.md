---
title: Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei
description: Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei.
author: twheeloc
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5082f4e80958ddb1e4a79bfe46df4a621f10fc40
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734252"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Izmaksu sadalījuma politikas izveide un piešķiršana izmaksu vadības ierīcei

[!include [banner](../../includes/banner.md)]

Izmantojiet šo procedūru, lai izveidotu un piešķirtu izmaksu sadalījuma politiku un atbilstošas kārtulas izmaksu vadības ierīcei. Šajā ierakstā tiek izmantots USP2 demonstrācijas datu uzņēmums.


## <a name="create-a-policy"></a>Politikas izveide
1. Pārejiet uz **sadaļu Izmaksu > un > izmaksu sadalījuma politikām**.
2. Klikšķiniet **Jauns**.
3. Laukā **Politikas** nosaukums ievadiet vērtību.
4. Izmaksu objektu **dimensiju hierarhijas** laukā ievadiet vai atlasiet vērtību.
    * Atlasiet Organizācija.  
5. Laukā **Statistikas dimensija** ievadiet vai atlasiet vērtību.
6. Noklikšķiniet uz **Saglabāt**.

## <a name="create-allocation-rules"></a>Sadalījuma kārtulu izveide
1. Klikšķiniet **Jauns**.
2. Sarakstā atzīmējiet atlasīto rindu.
3. Izmaksu objekta **dimensijas hierarhijas mezgla** laukā Izmaksu objektu dimensiju hierarhija ievadiet vai atlasiet vērtību.
4. Laukā **Izmaksu** uzvedība atlasiet 'Kopsumma'.
5. Laukā **Sadalījuma bāze** ievadiet vai atlasiet vērtību.
6. Klikšķiniet **Jauns**.
7. Sarakstā atzīmējiet atlasīto rindu.
8. Izmaksu objekta **dimensijas hierarhijas mezgla** laukā Izmaksu objektu dimensiju hierarhija ievadiet vai atlasiet vērtību.
9. Laukā **Izmaksu** uzvedība atlasiet 'Kopsumma'.
10. Laukā **Sadalījuma bāze** ievadiet vai atlasiet vērtību.
11. Klikšķiniet **Jauns**.
12. Sarakstā atzīmējiet atlasīto rindu.
13. Izmaksu objekta **dimensijas hierarhijas mezgla** laukā Izmaksu objektu dimensiju hierarhija ievadiet vai atlasiet vērtību.
14. Laukā **Izmaksu** uzvedība atlasiet 'Kopsumma'.
15. Laukā **Sadalījuma bāze** ievadiet vai atlasiet vērtību.
    * Turpiniet, līdz esat izveidojis visas kārtulas.  
16. Noklikšķiniet uz **Saglabāt**.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Politikas piešķiršana izmaksu vadības ierīcei
1. Noklikšķiniet **uz Politikas piešķires izmaksu kontroles vienībai**.
2. Klikšķiniet **Jauns**.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā **Derīgs no uzskaites** datuma ievadiet datumu.
    * Kārtulas ir efektīvas. Lietotājs vai sistēma var anulēt kārtulas, ja tiek izveidota jaunāka versija.  
5. Laukā **Izmaksu kontroles** vienība ievadiet vai atlasiet vērtību.
6. Noklikšķiniet uz **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
