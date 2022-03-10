---
title: Partijas pasūtījuma dzīves cikls no izveides līdz sākšanai
description: Šajā procedūrā tiek izklāstīta partijas pasūtījuma dzīves ciklā pirmā daļa.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7ca259ca8f176cd5bc76081836adcb7d272972b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579260"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a>Partijas pasūtījuma dzīves cikls no izveides līdz sākšanai

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]