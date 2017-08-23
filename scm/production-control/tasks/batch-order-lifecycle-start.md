--- 
title: "Partijas pasūtījuma dzīves cikls no izveidošanas līdz sākšanai"
description: "Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: dcb0814ae51f5914654736a957638f7d8be81e3f
ms.contentlocale: lv-lv
ms.lasthandoff: 07/28/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Partijas pasūtījuma dzīves cikls no izveidošanas līdz sākšanai

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa.

No izveides, izmaksu novērtējuma un ražošanas darbu plānošanas līdz faktiskajam partijas pasūtījuma sākumam.



Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF. 



Lai veiktu procedūras izpildi ar citu datu kopu, ir nepieciešama izlaista prece ar aktīvu formulu un maršruta versiju.


## <a name="create-a-batch-order"></a>Partijas pasūtījuma izveide
1. Dodieties uz Visi ražošanas pasūtījumi.
2. Noklikšķiniet uz Jauns partijas pasūtījums.
3. Laukā Krājuma kods ievadiet vai atlasiet kādu vērtību.
4. Noklikšķiniet uz Izveidot.
5. Izmantojiet ātro filtru, lai filtrētu pēc lauka Ražošana ar vērtību “b”.

## <a name="view-production-formula-and-expected-co-products"></a>Ražošanas formulas un paredzamo līdzproduktu skatīšana
1. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
2. Noklikšķiniet uz Formula.
3. Aizvērt lapu.
4. Nokliksķiniet uz Līdzprodukti.
5. Aizvērt lapu.

## <a name="estimate-the-batch-order"></a>Partijas pasūtījuma novērtējums
1. Noklikšķiniet uz Novērtējums.
2. Noklikšķiniet uz OK.
3. Darbību rūtī noklikšķiniet uz Pārvaldīt izmaksas.
4. Noklikšķiniet uz Skatīt detalizētu informāciju par aprēķinu.
5. Aizvērt lapu.

## <a name="release-the-batch-order"></a>Partijas pasūtījuma izlaišana
1. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
2. Noklikšķiniet uz Nodot izpildei.
3. Noklikšķiniet uz OK.

## <a name="schedule-production-jobs"></a>Ražošanas darbu plānošana
1. Darbību rūtī noklikšķiniet uz Grafiks.
2. Noklikšķiniet uz Plānot darbus.
3. Laukā Ierobežota noslodze atlasiet Nē.
4. Laukā Ierobežots materiāls atlasiet Nē.
5. Noklikšķiniet uz Labi.
6. Darbības rūtī noklikšķiniet uz vienuma Ražošanas pasūtījums.
7. Noklikšķiniet uz Visi darbi.
8. Aizvērt lapu.

## <a name="start-the-batch-order"></a>Partijas pasūtījuma uzsākšana
1. Noklikšķiniet uz Sākt.
2. Noklikšķiniet uz cilnes Vispārīgi.
3. Laukā Grāmatot izdošanas sarakstu tagad atlasiet Nē.
4. Noklikšķiniet uz OK.
5. Darbību rūtī noklikšķiniet uz Skatīt.
6. Noklikšķiniet uz Izdošanas saraksts.
7. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
8. Aizvērt lapu.
9. Aizvērt lapu.
10. Noklikšķiniet uz Maršruta karte.
11. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
12. Aizvērt lapu.
13. Aizvērt lapu.


