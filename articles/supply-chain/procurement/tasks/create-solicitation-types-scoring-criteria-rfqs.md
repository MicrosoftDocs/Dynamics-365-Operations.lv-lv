---
title: PP lūgumu tipus un punktu skaitīšanas kritēriju izveide
description: Šajā ceļvedī ir parādīts, kā izveidot lūguma tipu un saistīt to ar punktu skaitīšanas metodi.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQSolicitationType, PurchRFQCaseTableListPage, PurchCreateRFQCase, PurchRFQCaseTable, PurchRFQScoringRFQCaseCriteria, PurchRFQScoringCriteriaCopy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57abbab21a20278d77001a39e226af11994230be
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149642"
---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a>PP lūgumu tipus un punktu skaitīšanas kritēriju izveide

[!include [banner](../../includes/banner.md)]

Šajā ceļvedī ir parādīts, kā izveidot lūguma tipu un saistīt to ar punktu skaitīšanas metodi. Tajā ir arī parādīts, kā lūguma tipu lietot piedāvājuma pieprasījumā (IP), kurš pēc tam iestata noklusējuma punktu skaitīšanas metodi. Šos uzdevumus parasti veic pirkšanas vadītājs. Šo procedūru varat lietot, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus. Pirms sākšanas jums ir jābūt pieejamai punktu skaitīšanas metodei.


## <a name="create-a-solicitation-type"></a>Lūguma veida izveide
1. Pārejiet uz sadaļu Sagāde un avoti > Iestatīšana > Piedāvājuma pieprasījums > Lūguma tips.
2. Noklikšķiniet uz Jauns.
3. Laukā Nosaukums ierakstiet kādu vērtību.
4. Apraksta laukā ierakstiet vērtību.
5. Laukā Punktu skaitīšanas metode atlasiet punktu skaitīšanas metodi, kuru vēlaties izmantot šim lūguma tipam.
6. Noklikšķiniet uz Saglabāt.
7. Aizvērt lapu.

## <a name="use-the-solicitation-type"></a>Lietot lūguma tipu
1. Dodieties uz Sagāde un avoti > Piedāvājumu pieprasījumi > Visi piedāvājumu pieprasījumi.
2. Noklikšķiniet uz Jauns.
3. Laukā Lūguma tips atlasiet lūguma tipu, kuru tikko izveidojāt. 
    *   
4. Noklikšķiniet uz OK.
5. Noklikšķiniet uz Punktu skaitīšanas kritēriji.
    * Rādītie punktu skaitīšanas kritēriji ir kritēriji no punktu skaitīšanas metodes, kuru esat saistījis ar šo lūguma tipu. Kritērijus šajā lapā varat pievienot vai dzēst. Varat arī pievienot jaunus kritērijus, kopējot tās no citām punktu skaitīšanas metodēm.  
6. Noklikšķiniet uz Kopēt kritērijus.
7. Laukā Punktu skaitīšanas metode ievadiet vai atlasiet kādu vērtību.
8. Noklikšķiniet uz OK.
9. Aizvērt lapu.

