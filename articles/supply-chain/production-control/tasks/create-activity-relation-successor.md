---
title: 'Izveidot aktivitāšu relāciju: Pēctecīga aktivitāte'
description: Racionālās ražošanas plūsmas aktivitāšu plūsma tiek dokumentēta, izmantojot aktivitāšu relācijas.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f23dc0cb4b2ea7a4a298368a56869db90dd044d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981285"
---
# <a name="create-activity-relation---successor"></a>Izveidot aktivitāšu relāciju: Pēctecīga darbība

[!include [banner](../../includes/banner.md)]

Racionālās ražošanas plūsmas aktivitāšu plūsma tiek dokumentēta, izmantojot aktivitāšu relācijas. Šajā ierakstā ir parādīts, kā izveidot aktivitāšu relācijas.

Priekšnosacījumi:

- Ražošanas plūsma un versija melnraksta režīmā. 

- Divas aktivitātes, kuras seko viena otrai ražošanas plūsmā, ir izveidotas, bet nav saistītas.


## <a name="find-the-production-flow-version"></a>Ražošanas plūsmas versijas atrašana 
1. Pārejiet uz sadaļu Ražošanas kontrole > Iestatījumi > Racionālās ražošanas plūsma > Ražošanas plūsmas.
2. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Sarakstā atzīmējiet atlasīto rindu.
5. Sarakstā atlasiet melnraksta versiju.
    * Aktivitātes relācijas var pievienot gan melnraksta, gan aktīvām ražošanas plūsmas versijām.  

## <a name="open-the-activity-overview"></a>Aktivitāšu pārskata atvēršana
1. Noklikšķiniet uz Aktivitātes.
    * Ievērojiet, ka formās tiek parādītas visas ražošanas plūsmas aktivitātes, kas piešķirtas Ražošanas plūsmu versijai, ar kuru strādājat.  

## <a name="add-a-successor"></a>Pēctecīgas aktivitātes pievienošana
1. Noklikšķiniet uz Pievienojiet pēctecīgu aktivitāti.
2. Laukā Aktivitāte noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.
3. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.
4. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
5. Atzīmējiet izvēles rūtiņu Ierobežojums.
6. Laukā Ierobežojuma vērtība ievadiet vai atlasiet kādu skaitli.
    * Ierobežojuma laiks ir laiks, kas jāieplāno starp plānotām pirmstecīgas aktivitātes beigām (izpildes datumu un laiku) un plānoto pēctecīgas aktivitātes sākumu.  
7. Laukā Vienības ierakstiet vērtību.
8. Laukā Cikla laika koeficients ievadiet skaitli.
    * Ja abas aktivitātes tiek veiktas vienā un tajā pašā izgatavošanas laikā, cikla laika koeficientam ir jābūt 1. Ja pirmstecīgu aktivitāti veic ar dubultotu pēctecīgas aktivitātes ātrumu, koeficientam ir jābūt 2.   Cikla laiks koeficientus izmanto, lai aprēķinātu ražošanas plūsmas aktivitāšu atsevišķos cikla laikus.  
9. Noklikšķiniet uz OK.
10. Aizvērt lapu.
11. Noklikšķiniet uz cilnes GridPanel.
12. Aizvērt lapu.
13. Atsvaidziniet lapu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]