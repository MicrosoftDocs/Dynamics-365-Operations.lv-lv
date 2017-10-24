--- 
title: "Pamatlīdzekļa sadalīšana"
description: "Šis uzdevuma ceļvedis parādīs, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---
# <a name="split-a-fixed-asset"></a>Pamatlīdzekļa sadalīšana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis uzdevuma ceļvedis parādīs, kā atdalīt procentuālu daļu no vienas pamatlīdzekļu grāmatas uz jaunu pamatlīdzekļu grāmatu.  Tas izmanto grāmatveža lomu un USMF demonstrācijas datus.


## <a name="create-a-new-fixed-asset"></a>Izveidojiet jaunu pamatlīdzekli
1. Pārejiet uz sadaļu Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi.
2. Noklikšķiniet uz Jauns.
3. Ievadiet vai atlasiet vērtību laukā Pamatlīdzekļu grupa.
4. Ievērojiet pamatlīdzekļa numuru, kuru būs nepieciešams izmantot vēlāk sadalīšanas procesā.
5. Laukā Nosaukums ierakstiet kādu vērtību.
6. Aizveriet formu.

## <a name="split-a-fixed-asset"></a>Pamatlīdzekļa sadalīšana
1. Sarakstā atrodiet un atlasiet sadalāmo pamatlīdzekli.
2. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
3. Noklikšķiniet uz Grāmatas.
    * Atlasiet grāmatu, kuru nodalīt jaunajam pamatlīdzeklim.  
4. Noklikšķiniet uz Funkcijas.
5. Noklikšķiniet uz Sadalīt pamatlīdzekli.
6. Laukā Uz pamatlīdzekli, ievadiet vai atlasiet kādu vērtību.
7. Laukā Uz grāmatu, noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
8. Ievadiet datumu laukā Transakcijas datums.
9. Ievadiet skaitli laukā Procenti.
10. Laukā Žurnāla nosaukums, ievadiet vai atlasiet kādu vērtību.
11. Noklikšķiniet uz OK.

## <a name="post-the-journal-transaction"></a>Žurnāla transakcijas grāmatošana
1. Pārejiet uz sadaļu Pamatlīdzekļi > Žurnāla ieraksti > Pamatlīdzekļu žurnāls.
2. Sarakstā atlasiet žurnālu, kas izveidots sadalīšanas procesā.
3. Noklikšķiniet uz Rindas.
    * Pārbaudiet izveidotās žurnāla rindas.  Oriģinālajam aktīvam izveidota Iegādes pielāgošanas transakcija, lai samazinātu vērtību par sadalīšanas procesā norādīto procentuālo daļu.  Jaunajam aktīvam tiek izveidota Iegādes transakcija par tādu pašu summu.  
4. Noklikšķiniet uz Grāmatot.


